<template>
   <nav class="main-nav">
    <span><img src="../assets/logo.png" alt="Logo"></span>
    <ul>
        <li v-for="item in menu">
            <router-link :to="item.path">
                {{item.name}}
            </router-link>
        </li>
    </ul>
   </nav>
</template>


<script>
export default {
    name: 'MainNav',
       data () {
        return {
            menu: [
                {
                    name:'Home',
                    path: '/' 
                
                },
                {
                    name: 'About',
                    path: '/about'
                },
                {
                    name: 'Contact',
                    path: '/contact'
                },
                {
                    name: 'Blog',
                    path: '/blog'
                }
            ]
        }
    }
}
</script>

<style lang="scss">
  .main-nav {
    margin: 0;
    border: 1px solid lightgray;
    display: flex;
    justify-content: space-between;
    align-items: center;
     img {
       width: 25px;
       margin-left: 24px;
    }
     ul {
        display: flex;
        li {
            font-weight: bold;
            display: inline-block;
            list-style-type: none;
            margin-right: 24px;
            a {
                text-decoration: none;
                color: black;
            }
        }
     }
  }
</style>