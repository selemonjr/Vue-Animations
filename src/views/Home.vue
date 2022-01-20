<template>
<section>
    <div class="home">
    <div class="wrapper">
      <h1 class="hello">Welcome To Vue Animations</h1>
      <p class="content">A Vue Animation Tutorial created using Gsap and Vue-smooth-scroll</p>
       <a href="#div-id" v-smooth-scroll="{ duration: 1000, offset: 50,}"><button class="button">Vue Smooth Scroll</button></a>
    </div>
</div>
</section>
<section id="div-id">
  <div>
    <h2 class="smooth">Vue-Smooth-Scroll</h2>
    <div class="flex">
      <div>
        <p class="lorem">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor 
incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis 
nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. 
Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore 
eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, 
sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
      </div>

        <div>
        <p class="lorem">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor 
incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis 
nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. 
Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore 
eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, 
sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
      </div>

        <div>
        <p class="lorem">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor 
incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis 
nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. 
Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore 
eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, 
sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
      </div>
    </div>
  </div>
</section>

<!-- <section class="onscroll">
  <div v-animate-onscroll="'animated flash'">
  Animate me
</div>
</section> -->

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
            tl.to(".hello", {duration:2, y:-15})
            tl.to(".content", {duration:1, y:-10,opacity:1})
            tl.to(".button", {duration:1, y:-20,opacity:1,delay:1})
        }
    }

}
</script>
<style scoped>
.wrapper {
  text-align:center;
  margin-top:10%;
}
.hello {
  font-size:5em;
}
button {
  padding:7px 20px;
  border:none;
  font-size:18px;
  opacity:0;
  color:#000;
  border: 1px solid #000;
  border-radius:4px;
  margin-top:2%;
}
button:hover {
    background:#008000;
    color:#fff;
    transition:0.5s;
}
#div-id {
  margin-top:20%;
  text-align:center;
}
.smooth {
  text-align:center;
  margin-bottom:2%;
}
.content {
  font-weight:700;
  line-height:20px;
  margin-top:1%;
  font-size:1em;
  opacity:0;
}
.lorem {
  padding:1em;
}

.flex {
  display:flex;
  justify-content:space-between;
  align-items:center;
}

@media(max-width:760px) {
  .hello {
    font-size:20px;
  }
  .content {
    margin-bottom:10px;
    font-size:15px;
  }
}
</style>
