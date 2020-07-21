<template>
  <div>
    <select
      class="w-full form-control form-select"
      v-model="selectedOption"
      @input="event => { $emit('input', event.target.value) }"
    >
      <option v-for="(option, name) in options" :value="option" :key="name">{{ name }}</option>
    </select>
  </div>
</template>

<script>
export default {
  name: "dropdown",
  props: {
    value: null,
    options: {
      type: Object,
      required: true
    }
  },
  data() {
    return {
      isOpen: false,
      selectedOption: null
    };
  },
  mounted() {
    this.selectedOption = this.value;
  },

  watch: {
    value: function(newValue) {
      this.selectedOption = newValue;
    }
  }
};
</script>

<style>
</style>
