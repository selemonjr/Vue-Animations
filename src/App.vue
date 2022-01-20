<template>
  <div id="nav">
    <Navigation/>
     <router-view v-slot="{Component}">
       <transition name="slide" mode="out-in">
        <component :is="Component"/>
       </transition>
     </router-view>
  </div>
</template>
<script>
import Navigation from "./components/Navigation.vue"
export default {
  name:"App",
  components: {
    Navigation
  }
}
</script>
<style>
* {
  margin:0;
  padding:0;
  box-sizing:border-box;
}

body {
  height:100vh;
  width:100%;
  position:relative;
  font-family:sans-serif;
}
.slide-enter-from,
.slide-leave-to {
  opacity:0;
}

.slide-enter-active,
.slide-leave-active {
  transition: all 0.75s ease-out;
}
</style>
