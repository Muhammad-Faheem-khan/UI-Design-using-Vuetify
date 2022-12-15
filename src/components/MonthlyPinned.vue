<template>
  <div class="pl-12 pr-4 pt-4">
    <div class="d-flex">
      <h3 class="text-h5 font-weight-medium">Monthly Pinned</h3>
      <v-spacer></v-spacer>
      <p class="text-body2">View all</p>
    </div>

    <v-card
      class="mb-3 pb-0 px-4 b-color"
      outlined
      elevation="0"
      v-for="task in tasks"
      :key="task.work"
    >
      <v-card-text>
        <div class="d-flex">
          <p class="text-subtitle-1">{{ task.topic }}</p>
          <v-spacer></v-spacer>
          <p class="text-subtitle-1">{{ task.day }}</p>
        </div>
        <p class="text-h6 font-weight-medium text--primary mb-0">
          {{ task.work }}
        </p>
        <div class="text--primary d-flex">
          <v-icon :color="task.icon.color">{{ task.icon.name }}</v-icon>
          <p class="ml-2 pt-4 text-subtitle-1 mb-0">{{ task.status }}</p>
        </div>
      </v-card-text>
    </v-card>

    <div class="d-flex">
      <div class="mt-4">
        <h3 class="text-h5 font-weight-medium">My learnings</h3>
        <p class="text-body-1">Your progress of medical lectures</p>
      </div>
      <v-spacer></v-spacer>
      <v-btn fab color="#fbf7f4" elevation="0">
        <v-icon color="grey">mdi-dots-horizontal</v-icon>
      </v-btn>
    </div>
    <v-row>
      <v-col class="col-md-5 d-flex">
        <div class="pa-4 virus">
          <v-icon color="#475e83" size="30">mdi-pencil-ruler</v-icon>
        </div>
        <div class="ml-3">
          <h4 class="text-h6 font-weight-medium">Viruses</h4>
          <p>96% progress</p>
        </div>
      </v-col>
      <v-spacer></v-spacer>
      <v-col class="col-md-5 d-flex">
        <div class="pa-4 bact-cells">
          <v-icon color="#fbbc8b" size="30">mdi-material-design</v-icon>
        </div>
        <div class="ml-3">
          <h4 class="text-h6 font-weight-medium">Bacterial Cells</h4>
          <p>33% progress</p>
        </div>
      </v-col>
    </v-row>

    <v-row>
      <v-col class="col-md-5 d-flex">
        <div class="pa-4 med-science">
          <v-icon color="#deaaae" size="30">mdi-go-kart-track</v-icon>
        </div>
        <div class="ml-3">
          <h4 class="text-h6 font-weight-medium">Med Science</h4>
          <p>7% progress</p>
        </div>
      </v-col>
      <v-spacer></v-spacer>
      <v-col class="col-md-5 d-flex">
        <div class="pa-4 gens">
          <v-icon color="#99aeb4" size="30">mdi-hand-okay</v-icon>
        </div>
        <div class="ml-3">
          <h4 class="text-h6 font-weight-medium">Human Gens</h4>
          <p>58% progress</p>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "MonthlyPinned",
  data() {
    return {
      tasks: [
        {
          topic: "Next-gen immuno",
          work: "Multispecific liquids analysis",
          day: "5d",
          icon: {
            name: "mdi-numeric-1-circle",
            color: "orange",
          },
          status: "New feedback",
        },
        {
          topic: "Harmony",
          work: "Protein characterization during childhood and pregnancy",
          day: "1h",
          icon: {
            name: "mdi-alert-circle",
            color: "black",
          },
          status: "Deadline is today",
        },
        {
          topic: "Pharmaceutical",
          work: "Quick element dissolution testing",
          day: "7h",
          icon: {
            name: "mdi-check-circle",
            color: "green",
          },
          status: "Accepted",
        },
      ],
    };
  },
};
</script>

<style scoped>
.b-color {
  background-color: #fbf7f4;
}
.virus {
  background-color: #e9e9e9;
  width: 4rem;
  height: 4rem;
}
.bact-cells {
  background-color: #fceee5;
  width: 4rem;
  height: 4rem;
}
.med-science {
  background-color: #f7ebea;
  width: 4rem;
  height: 4rem;
}
.gens {
  background-color: #e8ebea;
  width: 4rem;
  height: 4rem;
}
</style>