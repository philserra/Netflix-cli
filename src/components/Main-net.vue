<template>
  <main class="Main-net">
    <div class="presentation" v-if="showPresentation === 'lol'">
      <h1>DECOUVREZ NOS OFFRES</h1>
      <p>A partir de 9,99€/MOIS</p>
      <button @click="handleShowPresentation('ok')">EN SAVOIR PLUS</button>
    </div>

    <div v-if="showPresentation === 'ok'" class="Offres">
      <div class="offre">
        <Offrenet title="SOLO" text="1 ecran video HD" price="9,99€/MOIS" />
        <button @click="handleShowPresentation('SOLO')">S'ABONNER</button>
      </div>

      <div class="offre">
        <Offrenet title="FAMILY" text="4 ecrans video HD" price="12,99€/MOIS" />
        <button @click="handleShowPresentation('FAMILY')">S'ABONNER</button>
      </div>

      <div class="offre">
        <Offrenet
          title="FAMILY 4K"
          text="4 ecran video 4K"
          price="15,99€/MOIS"
        />
        <button @click="handleShowPresentation('FAMILY 4K')">S'ABONNER</button>
      </div>
    </div>
    <div class="box-offres">
      <div v-if="showPresentation === 'SOLO'" class="Offres-net">
        <Offrenet
          title="SOLO"
          text="1 ecran video HD"
          price="9,99€/MOIS"
          text1="Tous les films et séries"
          text2="Visionnage hors-ligne"
        />
        <button @click="handleShowPresentation('ok')">Retour</button>
      </div>
      <div v-if="showPresentation === 'FAMILY'" class="Offres-net">
        <Offrenet
          title="FAMILY"
          text="4 ecrans video HD"
          price="12,99€/MOIS"
          text1="Tous les films et séries"
          text2="Visionnage hors-ligne"
        />
        <button @click="handleShowPresentation('ok')">Retour</button>
      </div>
      <div v-if="showPresentation === 'FAMILY 4K'" class="Offres-net">
        <Offrenet
          title="FAMILY 4K"
          text="4 ecrans video 4K"
          price="15,99€/MOIS"
          text1="Tous les films et séries"
          text2="Visionnage hors-ligne"
        />
        <button @click="handleShowPresentation('ok')">Retour</button>
      </div>
    </div>
  </main>
</template>

<script>
import Offrenet from "./Offre-net.vue";

export default {
  name: "Main-net",
  components: {
    Offrenet,
  },
  data() {
    return {
      showPresentation: "lol",
      showOffrenet: "",
    };
  },
  methods: {
    handleShowPresentation: function (ok) {
      this.showPresentation = ok;
    },
    handleShowOffreNet: function (lol) {
      this.showOffrenet = lol;
    },
  },
  mounted() {
    setTimeout(() => {
      this.num = 20;
    }, 4000);
    console.log(`main mounted`);
  },
  updated() {
    console.log(`main updated ${this.iChange}`);
  },
  unmounted() {
    console.log(`main unmounted `);
  },
};
</script>

<style scoped>
main {
  height: 60%;
  color: red;
  display: flex;
  justify-content: center;
  align-items: center;
}

.presentation {
  height: 200px;
  width: 800px;
  border: 2px solid red;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 20px;
}

button {
  width: 60%;
  color: black;
  border: solid 1px red;
  border-radius: 20px;
  transition: border-width 0.1s linear;
}
button:hover {
  border-width: 5px;
}

.Offres {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-around;
}

.offre {
  height: 300px;
  width: 300px;
  border: solid 2px red;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
  border-radius: 20px;
  transition: border-width 0.1s linear;
}
.offre:hover {
  border-width: 5px;
}

.Offres-net {
  height: 250px;
  width: 900px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
  border: solid 1px red;
  border-radius: 20px;
}
</style>
