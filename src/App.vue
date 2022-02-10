<template>
  <div id="app">
    <app-menu></app-menu>
    <app-main></app-main>
    <app-profile></app-profile>
  </div>
</template>

<script>
import Menu from "./components/Menu.vue";
import Main from "./components/main.vue";
import Profile from "./components/profile.vue";
export default {
  components: {
    "app-menu": Menu,
    "app-main": Main,
    "app-profile": Profile,
  },
};
</script>

<style lang="scss">
*{
  box-sizing: border-box;
  margin: 0;
}
#app{
  display: flex;
  flex-direction: row;
}
</style>
