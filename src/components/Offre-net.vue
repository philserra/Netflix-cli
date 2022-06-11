<template>
  <div class="Offre-net">
    <h1>{{ title }}</h1>
    <p>{{ text }}</p>
    <p>{{ price }}</p>
    <p>{{ text1 }}</p>
    <p>{{ text2 }}</p>
  </div>
</template>

<script>
export default {
  name: "Offre-net",
  components: {},
  props: {
    title: String,
    text: String,
    price: String,
    text1: String,
    text2: String,
  },
  data() {
    return {};
  },
  methods: {},
  mounted() {
    setTimeout(() => {
      this.num = 20;
    }, 4000);
  },
  updated() {
    console.log(`card updated`);
  },
  unmounted() {
    console.log(`card unmounted `);
  },
};
</script>

<style scoped>
/* .Offre-net {
  height: 300px;
  width: 300px;
  border-radius: 20px;

  border: 2px solid #ff0000;
  transition: border-width 0.1s linear;
} */
.Offre-net:hover {
  border-width: 5px;
}
.Offre-net button {
  border-radius: 20px;
  width: 50%;
  height: 30px;
  color: #ff0000;
}
</style>
