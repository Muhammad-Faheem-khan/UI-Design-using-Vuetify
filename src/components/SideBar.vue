<template>
  <div class="px-4 pt-6">
    <v-list nav class="mt-10 b-color">
      <v-list-item v-for="item in items" :key="item.title" link>
        <v-list-item-icon>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-item-icon>

        <v-list-item-content>
          <v-list-item-title class="font-weight-bold">{{
            item.title
          }}</v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-list-group :value="true" color="black" prepend-icon="mdi-chart-bubble">
        <template v-slot:activator>
          <v-list-item-title class="font-weight-bold" color="black"
            >Resourses</v-list-item-title
          >
        </template>

        <v-list class="ml-6 b-color">
          <v-list-item-group link>
            <v-list-item v-for="(item, i) in subItems" :key="i">
              <v-list-item-icon>
                <v-icon v-text="item.icon" :color="item.color"></v-icon>
              </v-list-item-icon>
              <v-list-item-content>
                <v-list-item-title v-text="item.text"></v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-list-group>
      <v-list-item link>
        <v-list-item-icon>
          <v-icon>mdi-cog</v-icon>
        </v-list-item-icon>

        <v-list-item-content>
          <v-list-item-title class="font-weight-bold">
            Settings
          </v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>

    <div class="d-flex mt-10">
      <v-btn filled fab color="black" elevation="0">
        <v-icon color="white">mdi-logout</v-icon>
      </v-btn>
      <h3 class="pt-3 ml-3">Logout</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: "SideBar",
  data() {
    return {
      items: [
        { title: "Dashboard", icon: "mdi-view-dashboard" },
        { title: "Education", icon: "mdi-book-education-outline" },
      ],
      subItems: [
        {
          text: "Genetics 101",
          icon: "mdi-checkbox-blank",
          color: "green darken-2",
        },
        {
          text: "DNA Synthesis",
          icon: "mdi-checkbox-blank",
          color: "purple darken-2",
        },
        { text: "Events", icon: "mdi-checkbox-blank", color: "black darken-2" },
      ],
    };
  },
};
</script>

<style scoped>
.b-color {
  background-color: #fbf7f4;
}
</style>