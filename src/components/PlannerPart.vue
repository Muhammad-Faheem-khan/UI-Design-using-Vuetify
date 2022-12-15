<template>
  <div class="px-8 my-4 py-6 rounded b-color">
    <div class="d-flex">
      <div>
        <h3 class="text-h5 font-weight-medium">Today's Plan</h3>
        <p class="text-body-1">June 14th, 2022</p>
      </div>
      <v-spacer></v-spacer>
      <v-btn filled fab color="black" elevation="0">
        <v-icon color="white">mdi-plus</v-icon>
      </v-btn>
    </div>
    <h3 class="text-h5 font-weight-medium my-5">
      Sustainable development goals and health innovation
    </h3>

    <div class="d-flex">
      <v-avatar class="ml-n4">
        <img src="../assets/1.jpg" alt="not found" />
      </v-avatar>
      <v-avatar class="ml-n4">
        <img src="../assets/3.jpg" alt="not found" />
      </v-avatar>
      <v-avatar class="ml-n4">
        <img src="../assets/6.jpg" alt="not found" />
      </v-avatar>
      <v-avatar color="pink ml-n4">
        <v-icon color="white">+5</v-icon>
      </v-avatar>

      <v-spacer></v-spacer>

      <v-divider vertical></v-divider>

      <div class="ml-5">
        <h5 class="text-body-1 font-weight-medium">Medi Team meeting</h5>
        <p class="text-body-1">13:30 - 14:50</p>
      </div>
    </div>
    <v-card color="#beccc9" class="pa-5 mt-7 card-height" border="0">
      <v-card-title class="text-h5 mb-3"> Weekly Report </v-card-title>
      <v-card-subtitle class="text-h6 font-weight-regular"
        >Track your performance</v-card-subtitle
      >
      <v-card-actions>
        <v-btn outlined elevation="0" class="mt-8 font-weight-bold">
          View Report
        </v-btn>
      </v-card-actions>
    </v-card>
    <v-row>
      <v-col class="col-md-6">
        <v-card color="#fadbc6" class="pa-5 mt-7 card-height" border="0">
          <v-card-title class="text-h5 mb-3"> Study 78X </v-card-title>
          <v-card-subtitle class="text-h6 font-weight-regular">
            <v-icon>mdi-clock-time-three</v-icon> Progress</v-card-subtitle
          >
        </v-card>
      </v-col>
      <v-col class="col-md-6">
        <v-card color="#fadbc6" class="pa-5 mt-7 card-height" border="0">
          <v-card-title class="text-h5 mb-3">Analyses </v-card-title>
          <v-card-subtitle class="text-h6 font-weight-regular"
            ><v-icon>mdi-check-circle</v-icon> Completed</v-card-subtitle
          >
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "PlannerPart",
};
</script>

<style scoped>
.card-height {
  height: 15rem;
}
.b-color {
  background-color: #ffffff;
}
</style>