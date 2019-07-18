    
<template>
  <v-app id="inspire">
    <v-navigation-drawer class="teal lighten-3" v-model="drawer" fixed app width="230px">
      <v-layout row wrap>
        <v-toolbar color="teal" dark>
          <v-icon x-large>money</v-icon>
        </v-toolbar>
      </v-layout>

      <v-list dark two-line>
        <navitem navtitle="Home" icon="home"></navitem>
        <navitem navtitle="About" icon="info"></navitem>
        <navitem navtitle="List" icon="menu"></navitem>
        <navitem navtitle="Analyse" icon="fingerprint"></navitem>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar color="teal" dark fixed app>
      <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
      <v-toolbar-title>Application</v-toolbar-title>
    </v-toolbar>
    <v-content>
      <v-container fill-height align-start justify-start>
        <lightgroup></lightgroup>
      </v-container>
    </v-content>
    <v-footer color="teal" app justify-center>
      <v-layout row wrap justify-space-around>
        <span class="white--text">CSPI Copyright &copy; 2019</span>
      </v-layout>
    </v-footer>
  </v-app>
</template>

<script>
import navitem from "./components/left/nav-item";
import lightgroup from "./components/right/light-group";
export default {
  data: () => ({
    drawer: null
  }),
  props: {
    source: String
  },
  methods: {
    buttonclick() {
      console.log("buttong clicked");
    }
  },
  components: {
    navitem,
    lightgroup
  }
};
</script>

<style>
</style>

