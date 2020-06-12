<template>
  <v-app class="primary">
     <v-navigation-drawer dark class="primary" v-model="drawer" absolute temporary>
        <v-list-item>
          <v-list-item-content>
            <v-list-item-title class="headline">Menu</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list>
          <v-list-item v-for="(item, i) in menu" :key="i" :href="item.path" nuxt>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

            <v-list-item-content>
              <v-list-item-title>{{ item.name }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-navigation-drawer>
    <v-app-bar dark class="primary" height="75">
      <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
      <div class="logo">
        <v-img src="/logo.svg" aspect-ratio="2"></v-img>
      </div>
      <v-toolbar-title>Cabinet Amas Schenone Amas</v-toolbar-title>

     
      <v-divider></v-divider>

      <v-spacer />
    </v-app-bar>
    <v-main>
      <v-container fluid class="ma-0 pa-0">
        <nuxt />
      </v-container>
    </v-main>
    <v-footer class="primary white--text">
      Chaqu'un des avocats exerce à titre individuel. Tout droit des images reservé au cabinet AMAS SCHENONE AMAS. MIT License.
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      menu: [
        {
          path: "/",
          name: "Contacts",
          icon: 'mdi-contacts'
        },
        {
          path: "/",
          name: "Domaine d'activités",
          icon: 'mdi-scale-balance'
        },
        {
          path: "/",
          name: "Honoraire",
          icon: 'mdi-cash-multiple'
        },
        {
          path: "/",
          name: "Articles",
          icon: 'mdi-book-open-outline'
        }
      ]
    };
  }
};
</script>
<style>
.logo {
  width: 100px;
  height: 75px;
  margin-top: 20px;
  margin-right: 15px;
}
</style>
