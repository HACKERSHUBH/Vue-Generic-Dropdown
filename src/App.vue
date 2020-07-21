<template>
  <div id="app">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <!-- {{selectedOption}} -->
     <dropdown :options="dataOptions" v-model="selectedOption"/>
  </div>
</template>

<script>
import dropdown from './components/dropdown.vue'
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    dropdown
  },
  data(){
    return{
      selectedOption: '',
       dataOptions: {
        'Data1': 'Data1',
        'Data2': 'Data2',
        'Data3': 'Data3',
        'Data4': 'Data4',
        'Data5': 'Data5',
        'Data6': 'Data6',
        'Data7': 'Data7'
      }
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
