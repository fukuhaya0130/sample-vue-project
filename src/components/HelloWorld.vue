<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div v-on:click="changeValue">ここをクリック</div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  methods:{
    changeValue: function(){
      this.$emit("changeValue", "裏Vueへようこそ。新しいVueが始まる。。。");
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
