<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld 
    :msg="message"
    :articles="articles"
    @changeValue="changeValue"
  />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  data(){
    return{
      message: "Welcome to Your Vue.js App",
      articles:[
        {
          id: 1,
          title: 'タイトル1',
          image: 'img1.jpg',
          description: '詳細1'
        },
        {
          id: 2,
          title: 'タイトル2',
          image: 'img2.jpg',
          description: '詳細2'
        },
        {
          id: 3,
          title: 'タイトル3',
          image: 'img3.jpg',
          description: '詳細3'
        },
      ]
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
