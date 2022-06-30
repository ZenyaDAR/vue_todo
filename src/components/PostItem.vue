<template>
    <div class="post">
      <div class="title"><strong>Название: {{post.title}}</strong></div>
      <div class="body"><p>Описание: {{post.body}}</p></div>
    </div>
</template>

<script>
    export default {
        props:{
            post:{
                type:Object,
                required: true
            }
        }
    }
</script>

<style scoped>

</style>