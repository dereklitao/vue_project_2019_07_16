<template>
  <v-card class="mx-auto" color="#26c6da" dark max-width="400">
    <v-card-title>
      <v-icon large left>mdi-twitter</v-icon>
      <span class="title font-weight-light">Twitter</span>
    </v-card-title>

    <v-card-text class="headline font-weight-bold">"KSQ"</v-card-text>

    <v-card-actions>
      <v-list-tile class="grow">
        <v-list-tile-avatar color="grey darken-3">
          <v-img
            class="elevation-6"
            src="https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light"
          ></v-img>
        </v-list-tile-avatar>

        <v-list-tile-content>
          <v-list-tile-title>Evan You</v-list-tile-title>
        </v-list-tile-content>

        <v-layout align-center justify-end>
          <v-btn color="success" round>Success</v-btn>
        </v-layout>
      </v-list-tile>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  props: ["name"]
};
</script>

<style scoped>
</style>
