<template>
  <v-card flat>
    <v-row align="center" justify="space-between">
      <v-col class="lg-3 md-3 sm-1" v-for="(person,i) in team" :key="i">
        <v-card>
          <v-img :src="team[i].img" class="white--text align-end" height="250px">
          <v-card-title>{{team[i].name}}</v-card-title>

          </v-img>
          <v-card-text class="text--primary">
            <div>{{ team[i].description }}</div>
            <div>{{ team[i].tel }}</div>
            <div>{{ team[i].email }}</div>
          </v-card-text>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn icon :href="getToTel(team[i].tel)">
              <v-icon>mdi-phone</v-icon>
            </v-btn>
            <v-btn icon :href="getToMail(team[i].email)">
              <v-icon>mdi-email</v-icon>
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-card>
</template>

<script>
export default {
  methods: {
    getToTel(tel) {
        return 'tel:' + tel
    },
    getToMail(mail) {
      return 'mail:' + mail
    }
  },
  data() {
    return {
      team: [
        {
          name: "Miche Amas",
          description: `Lauréat de la conférence du stage, ancien membre du conseil de l'ordre`,
          tel: "04.91.33.27.00",
          email: 'amas.schenone@wanadoo.fr',
          img: "/michel.jpg"
        },
        {
          name: "Isabelle Schenone",
          description: `Avocat ancien présidente de l'UJA, membre du conseil de l'ordre.`,
          tel: "04.91.33.37.44",
          email: 'isabelle.schenone@orage.fr',
          img: "/isabelle.jpg"
        },
        {
          name: "Karine Laignel",
          description: `Avocat.`,
          tel: "06.63.72.88.38 ",
          img: "/karine.jpg"
        }
      ]
    };
  }
};
</script>