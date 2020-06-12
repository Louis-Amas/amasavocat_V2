<template>
  <div>
    <!-- <Carousel></Carousel> -->
    <v-container class="main-content">
    <v-container>
      <Team></Team>
    </v-container>
    <v-container>
      <InfoWorkplace></InfoWorkplace>
    </v-container>
    <v-container>
      <Pricing></Pricing>
    </v-container>
    <v-container>
      <Info></Info>
    </v-container>
    </v-container>
  </div>
</template>

<script>
import Carousel from '../components/Carousel'
import Team from '../components/Team'
import InfoWorkplace from '../components/InfoWorkplace'
import Info from '../components/Info'
import Pricing from '../components/Pricing'

export default {
  components: {
    Team,
    Carousel,
    Info,
    Pricing,
    InfoWorkplace
  }
};
</script>
<style>
.main-content {
  width: 60%;
}

</style>