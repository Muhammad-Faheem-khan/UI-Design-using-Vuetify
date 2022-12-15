<template>
  <div class="d-flex flex-column align-center pt-6">
    <v-badge
      bordered
      bottom
      color="green accent-4"
      dot
      offset-x="8"
      offset-y="50"
    >
      <v-avatar size="60">
        <v-img src="../assets/7.jpg"></v-img>
      </v-avatar>
    </v-badge>
    <h3 class="text-h6 font-weight-medium">Dr. Riddle</h3>
    <p class="text-subtitle-1">Scientist</p>

    <div class="d-flex flex-column icons-grp">
      <v-avatar
        class="mb-3"
        v-for="icon in icons"
        :key="icon.name"
        :color="icon.bgColor"
      >
        <v-icon :color="icon.iconColor">
          {{ icon.name }}
        </v-icon>
      </v-avatar>
    </div>
  </div>
</template>

<script>
export default {
  name: "UserInfo",
  data() {
    return {
      icons: [
        {
          name: "mdi-circle-edit-outline",
          bgColor: "white",
          iconColor: "black",
        },
        {
          name: "mdi-message-processing",
          bgColor: "white",
          iconColor: "black",
        },
        {
          name: "mdi-plus",
          bgColor: "black",
          iconColor: "white",
        },
      ],
    };
  },
};
</script>

<style scoped>
.icons-grp {
  position: absolute;
  bottom: 5rem;
}

.main-container {
  position: relative;
}
</style>