<template>
    <div class="inputs">
      <input type="text" v-model="post.title" placeholder="Название">
      <input type="text" v-model="post.body" placeholder="Описание">
      <button @click="createPost">Создать</button>
    </div>
</template>

<script>
  export default {
    data(){
      return{
        post:{
          title:'',
          body:''
        }
      }
    },
    methods: {
      createPost(){
        this.post.id = Date.now(),
        this.$emit('create', this.post)
        this.post = {
          title:'',
          body:''
        }
      }
    },
  }
</script>

<style scoped>
input{
  width: 100%;
  height: 30px;
  padding: 10px;
  margin-top: 10px;
  border: green solid 2px;
}
button{
  padding: 15px;
  background: none;
  border: green solid 2px;
  margin-top: 20px;
}
</style>