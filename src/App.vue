<template>
  <div>
    <post-form  @create="createPost"/>

    <div class="err" v-if="this.posts.length <= 0">

      <h2>Задач нету</h2>

    </div>

    <div v-else>

      <post-list v-bind:posts="posts"/>

    </div>
    
  </div>
</template>

<script>
import PostForm from '@/components/PostForm'
import PostList from '@/components/PostList'
export default{
  components:{
    PostForm ,
    PostList
  },
  data (){
    return{
      posts: [
        
      ],
    }
  },
  methods: {
    createPost(post){
      this.posts.push(post)
    }
  }
}
</script>

<style>
body{
  margin: 0;
  padding: 10px;
}
.err{
  text-align: center;
  font-size: 20px;
}
</style>
