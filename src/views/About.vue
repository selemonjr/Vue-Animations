<template>
  <div>
    <h1 class="aboutEl">This is an about page</h1>
  </div>
</template>
<script>
import gsap from "gsap";
export default {
    name:"Home",
    mounted: function () {
        this.startAnimation();
    },
    methods: {
        startAnimation: function () {
            var tl = gsap.timeline();
            tl.to(".aboutEl", {duration:2, y:-15,opacity:1})
        }
    }

}
</script>
<style scoped>
.aboutEl {
  text-align:center;
  margin-top:10%;
  opacity:0;
}
</style>
