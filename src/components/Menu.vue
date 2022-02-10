<template>
  <div id="sidebar">
    <div class="header">
      <h1 id="logo">betterPay</h1>
      <div class="nav drop-nav" @click="toggle">Menu</div>
    </div>

    <div class="menu">
      <h3 class="pt-2">Home</h3>
      <h3 id="dashboard" class="text-white">Dashboard</h3>
      <h3>Profile</h3>
      <h3>Settings</h3>
      <h3>Logout</h3>
      <div
        class="
          premium-card
          bg-gradient-to-br
          from-gray-500
          via-transparent
          to-gray-500
        "
      >
        <h4 class="text-dark">Diamond member</h4>
        <p class="text-left px-4 pt-1">CK Molinga</p>
        <p class="text-left px-4">
          4358719077829 <span class="pl-5">04/12/25</span>
        </p>
        <button class="gold bg-yellow-400 p-1 my-1 text-black">
          Upgrade Gold
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import "./main.vue";
export default {
  name: "Menu",
  components: {},
  data() {
    return {
      emits: ["toggleData"],
    };
  },
  methods: {
    toggle(){
      this.$emit('toggleData', {name:"Menu Data"})
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Ubuntu:wght@300;400;500;700&display=swap");
#sidebar {
  height: 100vh;
  width: 0vw;
  font-family: "Ubuntu", sans-serif;
}
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
#logo {
  color: #0c1f2b;
  text-align: center;
  padding: 10px 25px;
  font-weight: bold;
  font-size: 24px;
  cursor: pointer;
}
.nav {
  color: #0c1f2b;
  text-align: center;
  padding: 10px 0;
  margin-left: 45vw;
  font-weight: bold;
  font-size: 18px;
  font-family: monospace;
  cursor: pointer;
  display: block;
}
.menu {
  background: #0c1f2b;
  color: rgba(255, 255, 255, 0.733);
  height: 100vh;
  text-align: center;
  border-radius: 0 50px 0 0;
  display: none;
}
h3 {
  // padding: 25px 0;
  margin: 0 0 25px 0;
  cursor: pointer;
}
h3:hover {
  color: #fff;
}
div.premium-card {
  margin: 0 15px;
  margin-top: 150px;
  height: 120px;
  border-radius: 15px;
  display: none;
}
.gold {
  border-radius: 6px;
  font-weight: bold;
}
.gold:hover {
  background: #ffdf00;
}
@media (min-width: 768px) {
  #sidebar {
    height: 100vh;
    width: 20vw;
    font-family: "Ubuntu", sans-serif;
  }
  #logo {
    color: #0c1f2b;
    text-align: center;
    padding: 25px 25px;
    font-weight: bold;
    font-size: 24px;
    cursor: pointer;
  }
  .nav {
    display: none;
  }
  .menu {
    background: #0c1f2b;
    color: rgba(255, 255, 255, 0.733);
    height: 100vh;
    text-align: center;
    border-radius: 0 50px 0 0;
    display: block;
  }
  h3 {
    // padding: 25px 0;
    margin: 0 0 25px 0;
    cursor: pointer;
  }
}

@media (min-width: 992px) {
  div.premium-card {
    margin: 0 15px;
    margin-top: 150px;
    height: 120px;
    border-radius: 15px;
    font-size: 14px;
    display: block;
  }
  span {
    padding-left: 1px;
  }
  button {
    padding: 2px;
  }
}
</style>
