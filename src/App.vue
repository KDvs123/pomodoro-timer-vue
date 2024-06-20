<template>
  <HomeVue />
</template>

<script>
import HomeVue from "./components/Home.vue";

export default {
  name: "App",
  components: {
    HomeVue,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Lobster&display=swap");

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Lobster", cursive;
  color: #f85959;
}

#app {
  background: #fff8ec;
}

.container {
  height: 100vh;
  display: flex;
  align-items: center;
  flex-direction: column;
}

.title {
  margin-top: 50px;
}

h1 {
  font-size: 64px;
  color: #c44747;
  margin-right: 10px;
}

.timer {
  position: relative;
  margin-top: 100px;
  width: 330px;
  height: 330px;
}

button{
  margin-top: 50px;
  width: 200px;
  height: 60px;
  background: #f85959;
  border-radius: 20px;
  border: none;
  cursor: pointer;
  font-size: 36px;
  line-height: 45px;
  text-align: center;
  color: #fff8ec;
}

button:focus{
  outline: none;
}

</style>
