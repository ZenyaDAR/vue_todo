<template>
  <div>
   
  <post-item :key="post.id" v-for="post in posts" :post="post"/>
  </div>
 
</template>

<script>

import PostItem from '@/components/PostItem'
  export default {
    components:{
      PostItem
    },
      props: {
        posts: {
            type: Array,
            required: true
        }
      }
  }
</script>

<style scoped>
.post{
  width: 100%;
  height: 60px;
  border: solid red 2px;
  padding: 10px;
  margin: 25px;
}
.title{
  font-size: 20px;
}
.body{
  font-size: 16px;
}
</style>