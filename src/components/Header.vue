/* eslint-disable vue/multi-word-component-names */
<template>
  <header>
    <img src="../assets/netflix-logo.png" alt="" />
    <h1>Netflix</h1>
    <p>Bienvenu sur votre plate-forme de streaming</p>
  </header>
  <hr />
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Header",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
header {
  height: 20%;
  color: red;
  display: flex;
  flex-flow: wrap;
  align-items: center;
  font-size: x-large;
}

header img {
  width: 100px;
}

h1 {
  letter-spacing: 2px;
  margin-left: 10px;
  font-size: 60px;
  text-transform: uppercase;
  font-weight: 700;
  font-family: "Josefin Sans", sans-serif;
  background: linear-gradient(to right, #cc231d 10%, #891d1c 50%, #5c0909 60%);
  background-size: 200% auto;
  color: #fff;
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  display: inline-block;
}

p {
  letter-spacing: 2px;
  margin-left: 220px;
}

hr {
  margin: 0 auto;
  width: 80%;
  border: 0;
  height: 2px;
  background-image: linear-gradient(
    to right,
    rgba(225, 24, 24, 0.666),
    rgba(255, 255, 255, 0.75),
    rgba(225, 24, 24, 0.666)
  );
}
</style>
