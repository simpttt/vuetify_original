<template>
  <v-app>
    <v-navigation-drawer app v-model="drawer" clipped>
      <v-container>
        <v-list-item>
          <v-list-item-content>
            <v-list-item-title class="title">
              Navigation lists
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-divider></v-divider>
      </v-container>
    </v-navigation-drawer>
    <v-app-bar color="green" dark app clipped-left>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>Todoapp</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items>
        <v-btn text style="text-transform: none">Login</v-btn>
        <v-btn text style="text-transform: none">Help</v-btn>
      </v-toolbar-items>
    </v-app-bar>
    <v-content class="my-3">
      <Board></Board>
    </v-content>
    <v-footer color="green" dark app>
      simp_t
    </v-footer>
  </v-app>
</template>

<script>
import Board from "./components/Board.vue";
export default {
  name: "App",
  components: {
    Board,
  },
  data() {
    return {
      drawer: false,
    };
  },
};
</script>
