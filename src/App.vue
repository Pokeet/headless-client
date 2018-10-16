<template>
  <div id="app">
    <b-navbar toggleable="md" type="dark" variant="primary">
      <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>
      <b-navbar-brand href="#">Headless-client</b-navbar-brand>
    </b-navbar>
    <div class="container-fluid">
      <div class="row">
        <div class="col">
          <HelloWorld v-if="loggedIn"/>
          <Login v-if="!loggedIn"/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Login from './components/Login.vue'
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    Login,
    HelloWorld
  },
  data: () => {
    return {
      loggedIn: false
    }
  }
}
</script>

<style>
</style>
