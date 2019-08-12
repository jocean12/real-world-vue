<template>
  <div id="app">
    <transition name="fade" mode="out-in">
      <router-view />
    </transition>
  </div>
</template>
<style>
@import url('https://fonts.googleapis.com/css?family=Cormorant+Garamond:400,400i&display=swap');
#app {
  font-family: 'Cormorant Garamond', serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  font-size: 24px;
}
a {
  text-decoration: none;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #bebebe;
}
.fade-enter-active,
.fade-leave-active {
  transition-duration: 0.5s;
  transition-property: opacity;
  transition-timing-function: ease;
  transition: all 0.5s ease;
}

.fade-enter,
.fade-leave-active {
  opacity: 0;
  transform: scale(2);
}
</style>
