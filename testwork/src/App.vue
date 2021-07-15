<template>
  <div id="app">
    <Nav></Nav>
    <router-view/>
  </div>
</template>

<script>
  import './assets/ubuntu/ubuntu.css'
  import './assets/style.css'
  import Nav from './components/Nav'
  export default {
    components:{
      Nav
    }
  }
</script>
