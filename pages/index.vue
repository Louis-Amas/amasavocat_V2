<template>
  <div>
    <Carousel></Carousel>
    <v-container>
    <Team></Team>
    </v-container>
  </div>
</template>

<script>
import Carousel from '../components/Carousel'
import Team from '../components/Team'
export default {
  components: {
    Team,
    Carousel
  }
};
</script>