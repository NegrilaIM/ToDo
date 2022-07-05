<template>
  <div class="blog"> 
   <h1>Lists of posts:</h1>
   <ul>
    <li v-for="post in posts">
      <h2>
        <router-link to="'/post/${post.id}'" >{{ post.title }}</router-link>
        <p>{{ post.body }}</p>
      </h2>
    </li>
   </ul>
  </div>
</template>


<script>
import axios from 'axios'
  export default {
    name: 'BlogView',
     data () {
        return{
            posts: []
        }
     },
      created () {
        const url = 'https://jsonplaceholder.typicode.com/posts'
         axios.get(url)
          .then (resp => {
            this.posts = resp.data
          })
          .catch (err => {
             console.log(err.response ? err.response.data : e)
          })
      }

  }
</script>

<style lang="scss">
 li{
    list-style-type: none;
    p {
    font-size: 16px;
    text-align: center;
    max-width: 700px;
    margin: 0 auto;
 }
 a {
    text-decoration: none;
 }
 
 }
</style>