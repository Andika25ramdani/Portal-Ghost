<template>
  <!-- <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </div> -->
  <transition name="slide-up">
    <router-view/>
  </transition>
</template>

<style lang="sass">
html
  background: url('/../img/bg_logo_BW 1.png') center center no-repeat fixed
  background-color: #111827
  background-size: 860px, contain
  font-family: 'Montserrat', sans-serif
#app
  text-align: center
  color: #2c3e50
  background: radial-gradient(circle, #064E3B99, black 35%) no-repeat center fixed
  min-height: 100vh
  width: 100%
  position: absolute
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
