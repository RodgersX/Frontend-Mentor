<template>
  <v-app id="app">
    <v-app-bar app color="white" flat class="app-bar"> 
      <p class="title">Snap</p>
      <div class="nav-tags">
        <ul>
          <li>
            Features
            <span><i class="bx bxs-chevron-down"></i></span>
          </li>
          <li>
            Company
            <span><i class="bx bxs-chevron-down"></i></span>
          </li>
          <li>
            Careers
          </li>
          <li>About</li>
        </ul>
      </div>
      <div class="auth-div">
        <v-btn text class="mr-5">Login</v-btn>
        <v-btn outlined>Register</v-btn>
      </div>
    </v-app-bar>

    <v-main class="mt-10">
      <main-contents />
    </v-main>
  </v-app>
</template>

<script>
import MainContent from './components/MainContent.vue'

export default {
  name: "App",

  components: {
    "main-contents": MainContent
  }

};
</script>

<style scoped lang="sass">
#app
  font-size: 18px
  font-family: 'Epilogue', sans-serif

.app-bar
  padding: 1rem 2rem

.title
  font-weight: 700

.nav-tags ul
  list-style-type: none
  display: flex
  align-items: center


.nav-tags ul li
  display: inline-block
  margin: 0 30px

.auth-div
  margin-left: auto

</style>
