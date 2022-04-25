<template>
  <v-app id="app">
    <v-app-bar app color="white" flat class="app-bar">
      <p class="title">Snap</p>
      <div class="nav-tags">
        <ul>
          <div class="dropdown">
            <li>
              Features
              <span class="ml-2">
                <i class="bx bxs-chevron-down icon-down"></i>
                <i class="bx bxs-chevron-up icon-up"></i>
              </span>
            </li>
            <div class="dropdown-content">
              <ul style="">
                <li
                  v-for="(ftr, i) in features"
                  :key="i"
                  class="d-flex justify-space-around my-5"
                >
                  <i :class="[ftr.icon, ftr.color]" class="mr-4"></i>
                  <p class="mb-0">{{ ftr.title }}</p>
                </li>
              </ul>
            </div>
          </div>

          <div class="dropdown">
            <li class="company">
              Company
              <span class="ml-2">
                <i class="bx bxs-chevron-down icon-down"></i>
                <i class="bx bxs-chevron-up icon-up"></i>
              </span>
            </li>
            <div class="dropdown-content">
              <ul style="">
                <li
                  v-for="(plc, i) in company"
                  :key="i"
                  class="my-5 text-start"
                >
                  <p class="mb-0">{{ plc }}</p>
                </li>
              </ul>
            </div>
          </div>
          <li>Careers</li>
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
import MainContent from "./components/MainContent.vue";

export default {
  name: "App",

  components: {
    "main-contents": MainContent,
  },

  data() {
    return {
      features: [
        {
          icon: "bx bxs-calendar-minus",
          title: "Todo List",
          color: "purple--text",
        },
        { icon: "bx bx-calendar", title: "Calendar", color: "teal--text" },
        { icon: "bx bxs-bell-ring", title: "Reminders", color: "blue--text" },
        {
          icon: "bx bx-loader-circle",
          title: "Planning",
          color: "purple--text",
        },
      ],

      company: ["History", "Our Team", "Blog"],
    };
  },
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
  display: flex
  align-items: center
  cursor: pointer

.auth-div
  margin-left: auto

.dropdown
  position: relative
  display: inline-block

.dropdown-content
  display: none
  overflow: hidden
  border-radius: 7px
  position: absolute
  background-color: white
  cursor: pointer
  width: 200px
  box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2)
  z-index: 1

.dropdown-content ul
  list-style: none
  display: inline-block
  padding: 0px
  width: 100%

.dropdown:hover .dropdown-content,
.dropdown:active .dropdown-content
  display: block

.dropdown:hover .icon-down,
.dropdown .icon-up
  display: none

.dropdown:hover .icon-up
  display: inline
</style>
