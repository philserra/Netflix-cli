<template>
  <div class="wrapper">
    <Header />
    <Mainnet />
    <Footernet />
  </div>
</template>

<script>
import Header from "./components/Header";
import Mainnet from "./components/Main-net";
import Footernet from "./components/Footer-net";

export default {
  name: "App",
  components: {
    Header,
    Mainnet,
    Footernet,
  },
};
</script>

<style>
body {
  margin: 0;
  padding: 0;
  background-color: rgba(2, 2, 2, 0.936);
  font-family: "Josefin Sans", sans-serif;
}
.wrapper {
  height: 100vh;
}
</style>
