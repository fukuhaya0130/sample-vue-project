<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld 
    :msg="message"
    @changeValue="changeValue"
  />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  data(){
    return{
      message: "Welcome to Your Vue.js App"
    }
  },
  components: {
    HelloWorld
  },
  methods:{
    changeValue: function(_message){
      this.message = _message;
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
