<template>
  <div id="app">
    <Header />
    <Banner />
    <Discover />
    <Contact />
  </div>
</template>

<script>
import Header from './components/header/index.vue'
import Banner from './components/banner.vue'
import Discover from './components/discover.vue'
import Contact from './components/contact.vue'

export default {
  name: 'App',
  components: {
    Header,
    Banner,
    Discover,
    Contact
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.heading {
  img {
    width: 35px;
    margin-bottom: 10px;
  }
  h2 {
    font-size: 19px;
    font-weight: 600;
  }
  p {
    font-size: 14px;
  }
}
</style>
