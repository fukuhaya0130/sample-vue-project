<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div v-on:click="changeValue">ここをクリック</div>
    <div v-for="article in articles" :key="article.id">
      <CardComponent
        :id="article.id" 
        :title="article.title" 
        :image="article.image" 
        :description="article.description"
      />
    </div>
  </div>
</template>

<script>
import CardComponent from "./CardComponent.vue";

export default {
    name: "HelloWorld",
    props: {
        msg: String,
        articles: Object
    },
    methods: {
        changeValue: function () {
            this.$emit("changeValue", "裏Vueへようこそ。新しいVueが始まる。。。");
        }
    },
    components: { CardComponent }
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
