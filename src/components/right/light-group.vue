<template>
  <v-layout align-start justify-center>
    <v-card>
      <v-toolbar color="teal" dark min-width="200px" height="50px">
        <v-toolbar-side-icon></v-toolbar-side-icon>
        <v-toolbar-title>Engine</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn icon>
          <v-icon>search</v-icon>
        </v-btn>
      </v-toolbar>

      <v-list two-line>
        <template v-for="(item, index) in items">
          <v-subheader v-if="item.header" :key="item.header" height="10px">{{ item.header }}</v-subheader>
          <v-divider v-else-if="item.divider" :key="index" :inset="item.inset"></v-divider>
          <v-list-tile v-else :key="item.title" avatar @click>
            <v-list-tile-action>
              <v-icon large mr-2>wb_sunny</v-icon>
            </v-list-tile-action>

            <v-list-tile-content>
              <v-list-tile-title v-text="'HELLO'"></v-list-tile-title>
            </v-list-tile-content>

            <v-btn round color="teal" dark>
              <v-icon>wb_sunny</v-icon>
            </v-btn>
          </v-list-tile>
        </template>
      </v-list>
    </v-card>
  </v-layout>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { header: "Today" },
        {
          avatar: "https://cdn.vuetifyjs.com/images/lists/1.jpg",
          title: "Brunch this weekend?",
          subtitle:
            "<span class='text--primary'>Ali Connors</span> &mdash; I'll be in your neighborhood doing errands this weekend. Do you want to hang out?"
        },
        { divider: true, inset: true },
        {
          avatar: "https://cdn.vuetifyjs.com/images/lists/2.jpg",
          title: 'Summer BBQ <span class="grey--text text--lighten-1">4</span>',
          subtitle:
            "<span class='text--primary'>to Alex, Scott, Jennifer</span> &mdash; Wish I could come, but I'm out of town this weekend."
        },
        { divider: true, inset: true },
        {
          avatar: "https://cdn.vuetifyjs.com/images/lists/3.jpg",
          title: "Oui oui",
          subtitle:
            "<span class='text--primary'>Sandra Adams</span> &mdash; Do you have Paris recommendations? Have you ever been?"
        }
      ]
    };
  }
};
</script>