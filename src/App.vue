<template>
  <div id="app">
    <div class="navbar has-shadow is-primary">
      <div class="container">
        <div class="navbar-start has-text-weight-bold">
          <div class="navbar-brand">
          <a class="navbar-item is-size-4"><i class="fab fa-vuejs"></i>&nbsp; VUEJS COMPANY SITE</a>
        </div>

        <a role="button" class="navbar-burger" aria-label="menu" aria-expanded="false" v-on:click="toggleNav" v-bind:class="{ 'is-active': isActive }">
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
        </div>

        <div class="navbar-end navbar-menu has-text-weight-bold" v-bind:class="{ 'is-active': isActive }">
          <router-link to="/" class="navbar-item right-item">HOME</router-link>
          <router-link to="faq" class="navbar-item right-item">SERVICES</router-link>
          <router-link to="faq" class="navbar-item right-item">ABOUT</router-link>
          <router-link to="faq" class="navbar-item right-item">FAQ</router-link>

          <div class="navbar-item">
            <p class="control">
              <a class="button is-outlined">
                <span class="icon">
                  <i class="fas fa-envelope"></i>
                </span>
                <span>CONTACT US</span>
              </a>
            </p>
          </div>

        </div>
      </div>
    </div>

    <router-view></router-view>

    <footer class="footer is-primary">
      <div class="container">
        <div class="columns">
          <div class="column">
            <p><i class="far fa-copyright"></i>&nbsp; 2018 VueJS Company Site</p>
          </div>
          <div class="column has-text-right">
            <a href="#" class="icon"><i class="fab fa-facebook fa-lg"></i></a>
            <a href="#" class="icon"><i class="fab fa-twitter-square fa-lg"></i></a>
            <a href="#" class="icon"><i class="fab fa-instagram fa-lg"></i></a>
          </div>
        </div>
      </div>
    </footer>

  </div>
</template>

<script>
export default {
  name: 'App',
  data: function() {
    return {
      isActive: false
    }
  },
  methods: {
    toggleNav: function() {
      this.isActive = !this.isActive;
    }
  }
}
</script>

<style lang="sass">
@import '../node_modules/bulma/bulma.sass'
@import 'mq'

a.right-item
  +mobile
    color: gray
    &hover
      background-color: #F1F1F1
      color: black

.navbar-burger span
      color: #FFFFFF  

footer
  background-color: $primary !important
  color: #FFFFFF

.icon
  color: #FFFFFF
  margin-left: 20px


</style>
