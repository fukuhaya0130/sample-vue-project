<template>
    <div class="cards">
        {{ id }} <br/>
        {{ title }} <br/>
        {{ image }} <br/>
        {{ description }} <br/>
    </div>
</template>

<script>
export default {
    name: 'HelloWorld',
    props: {
        id: Number,
        title: String,
        image: String,
        description: String
    },
    methods:{
        changeValue: function(){
            this.$emit("changeValue", "裏Vueへようこそ。新しいVueが始まる。。。");
        }
    }

}
</script>
<style scoped>
.cards{
    border: 2px solid black;
    margin: 10px auto;
}
</style>