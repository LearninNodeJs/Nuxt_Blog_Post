<template>
  <section id="posts">
    <PostPreview v-for="post in posts"
    :key="post.id"
    :title="post.title"
    :excerpt="post.previewText"
    :thumbnailImage="post.thumbnailUrl"
    :id="post.id"/>
  </section>
</template>

<script>

import PostPreview from "@/components/Blog/PostPreview"
export default {
  components:{
    PostPreview
  },
  data(){
    return{
      posts:[
        {
          title:'A New Beginning',
          previewText:'This will be awesome, don\'t miss it!',
          thumbnailUrl:'',
          id:'a-new-beginning'
        },
        {
          title:'A Second Beginning',
          previewText:'This will be awesome too,, don\'t miss it!',
          thumbnailUrl:'',
          id:'a-second-beginning'
        },
        {
          title:'A Third Beginning',
          previewText:'This will be awesome tooooo,, don\'t miss it!',
          thumbnailUrl:'',
          id:'a-third-beginning'
        }
      ]
    }
  }

}
</script>

<style scoped>
#posts{
  padding-top: 2rem;
  display:flex;
  justify-content: center;
  align-items: center;
  flex-direction:column;
}
@media(min-width: 35rem){
  #posts{
    flex-direction: row;
  }
}
</style>
