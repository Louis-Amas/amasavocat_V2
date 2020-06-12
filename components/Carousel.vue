<template>
  <v-carousel cycle height="400" hide-delimiter-background hide-delimiters show-arrows-on-hover>
    <v-carousel-item v-for="(img, i) in imgs" :key="i" :src="img"></v-carousel-item>
  </v-carousel>
</template>
<script>
export default {
  data() {
    return {
      imgs: [
        "vieux_port.jpg",
        "corniche.jpg",
        "palais.jpg",
        "palais-exterieur.jpg"
      ]
    };
  }
};
</script>