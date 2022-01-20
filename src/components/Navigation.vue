<template>
<div>
      <nav>
    <div class="nav_logo">
        <h1 class="gsap"><span class="logo">Vue</span>Transitions</h1>
        </div>
    <div class="nav_link">
      <ul>
        <li class="home"><router-link to="/">Home</router-link></li>
        <li class="about"><router-link to="/about">About</router-link></li>
      </ul>
    </div>
  </nav>
</div>
</template>
<script>
import gsap from "gsap";
export default {
    name:"Navigation",
    mounted: function () {
        this.startAnimation();
    },
    methods: {
        startAnimation: function () {
            var tl = gsap.timeline();
            tl.to(".gsap", {duration:1, x:15})
            tl.to(".home", {duration:1, opacity:1})
            tl.to(".about", {duration:1, opacity:1})
        }
    }

}
</script>
<style scoped>
nav {
    display:flex;
    justify-content:space-between;
    width:100%;
    height:10vh;
    padding:1px;
    align-items:center;
    background:#eee;
}
.logo {
    color:rgb(9, 221, 9);
    margin-right:3px;
}
ul {
    display:inline-flex;
    list-style:none;
}
.home,.about {
    opacity:0;
}
ul li {
    margin:10px;
}
ul li a {
    text-decoration:none;
    color:#000;
}
a.router-link-active {
    border-bottom:2px solid #5eff00;
}
</style>