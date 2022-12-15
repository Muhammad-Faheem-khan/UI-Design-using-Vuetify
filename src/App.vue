<template>
  <v-app>
    <div class="hidden-lg-and-up">
      <div class="d-flex flex-column align-center mt-5">
        <v-avatar size="45">
          <img src="./assets/logo.jpg" alt="not found"
        /></v-avatar>
        <h3 class="mt-2 mb-4 text-h5 font-weight-bold">SOLARIUS</h3>
      </div>
      <v-expansion-panels>
        <v-expansion-panel>
          <v-expansion-panel-header> Menu</v-expansion-panel-header>
          <v-expansion-panel-content>
            <SideBar />
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </div>
    <div class="main-container">
      <v-row class="ma-0">
        <v-col class="col-lg-2 hidden-md-and-down">
          <div class="d-flex flex-column align-center">
            <v-avatar size="45">
              <img src="./assets/logo.jpg" alt="not found"
            /></v-avatar>
            <h3 class="mt-2 text-h5 font-weight-bold">SOLARIUS</h3>
          </div>
          <SideBar />
        </v-col>
        <v-col class="col-lg-4 col-md-6">
          <PlannerPart />
        </v-col>
        <v-col class="col-lg-5 col-md-6">
          <div class="d-flex">
            <MonthlyPinned />
            <v-spacer class="hidden-md-and-down"></v-spacer>
            <v-divider vertical class="hidden-md-and-down"></v-divider>
          </div>
        </v-col>
        <v-col class="col-lg-1 hidden-md-and-down">
          <UserInfo />
        </v-col>
      </v-row>
    </div>
  </v-app>
</template>

<script>
import SideBar from "./components/SideBar.vue";
import PlannerPart from "./components/PlannerPart.vue";
import MonthlyPinned from "./components/MonthlyPinned.vue";
import UserInfo from "./components/UserInfo.vue";

export default {
  name: "App",

  components: {
    SideBar,
    PlannerPart,
    MonthlyPinned,
    UserInfo,
  },

  data: () => ({
    //
  }),
};
</script>

<style>
.main-container {
  background-color: #fbf7f4;
}
</style>
