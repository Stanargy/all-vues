<template @scroll="scrollEvent">
  <div id="navWrapper">
    <div id="vNavigation" v-bind:class="[isActive]">
      <router-link to="/" class="navItem">
        <p>Home</p>
      </router-link>
      <router-link to="/about" class="navItem">
        <p>About</p>
      </router-link>
      <router-link to="/" class="navItem">
        <p>Products</p>
      </router-link>
      <router-link to="/about" class="navItem">
        <p>Roadmap</p>
      </router-link>
    </div>
  </div>
</template>
<script>
export default {
  name: "vNavigation",
  props: {
      },
  methods: {
    scrollEvent: function(event) {
      if(isActive === ""){
     this.isActive = "newStyle";
     }
     console.log(isActive)
    }
  },
  created() {
    window.addEventListener("scroll", this.scrollEvent);
  },
  destroyed() {
    window.removeEventListener("scroll", this.scrollEvent);
  },
  data(){
      return{
        isActive: "",

      }
  },
};

</script>

<style scoped>
.newStyle {
  color: red;
}

#navWrapper {
  margin-top: 30vh;
  width: 30vw;
}
#vNavigation {
  display: flex;
  flex-direction: column;
  position: fixed;
  height: 20vh 20%;
  top: 200px;
  padding: 10px 0px;
  margin-left: 10px;
  align-items: center;
  box-sizing: border-box;
  width: 100px;
}

.navItem {
  text-decoration: none;
  top: 50vh;
  padding: 5px 10px;
  background: greenyellow;
  width: 80px;
  margin: 5px 5px;
  border: 2px solid green;
  transition: 0.3s;
}
.navItem p {
  font-weight: 500;
}
.navItem:hover {
  margin: 20px 20px;
  height: 110%;
}
</style>

