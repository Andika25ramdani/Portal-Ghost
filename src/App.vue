<template>
  <!-- <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </div> -->
  <router-view/>
</template>

<style lang="sass">
html
  background: url('/../img/bg_logo_BW 1.png') center center no-repeat fixed
  background-color: #111827
  background-size: auto
  font-family: 'Montserrat', sans-serif
#app
  text-align: center
  color: #2c3e50
#nav 
  padding: 30px
  a
    font-weight: bold
    color: #2c3e50
    &.router-link-exact-active 
      color: #42b983
.slide-up-enter-active,
.slide-up-leave-active,
.slide-left-enter-active,
.slide-left-leave-active,
.slide-right-enter-active,
.slide-right-leave-active
  transition: all 2.5s ease 1s
.slide-up-enter-from,
.slide-up-leave-to
  opacity: 0
  transform: translateY(10%)
.slide-left-enter-from,
.slide-left-leave-to
  opacity: 0
  transform: translateX(-10%)
.slide-right-enter-from,
.slide-right-leave-to
  opacity: 0
  transform: translateX(10%)
</style>
