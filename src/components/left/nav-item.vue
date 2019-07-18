<template>
  <v-list-tile @click="clicked">
    <v-list-tile-action>
      <v-icon large>{{icon}}</v-icon>
    </v-list-tile-action>
    <v-list-tile-content>
      <v-list-tile-title style="font-size: 18px">{{navtitle}}</v-list-tile-title>
    </v-list-tile-content>
  </v-list-tile>
</template>

<script>
export default {
  props: ["icon", "navtitle"],
  data: () => ({}),
  methods: {
    clicked() {
      console.log("navitem-clicked");
    }
  }
};
</script>

<style scoped>
</style>
