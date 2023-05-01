<template>
  <v-container fluid>

  <v-app-bar class="border-b" flat>
    <v-spacer></v-spacer>
    <v-app-bar-title class="ma-5 ml-5">
      <v-badge color="purple" dot location="bottom end" offset-x="-8" offset-y="6">

        <h2>Yusif</h2>
      </v-badge>
    </v-app-bar-title>
    <v-btn>Home</v-btn>
    <v-btn>Works</v-btn>
    <v-btn>Projects</v-btn>
    <v-btn>Services</v-btn>
    <v-spacer></v-spacer>
    <v-btn variant="outlined">Lets' Chat</v-btn>

    <v-spacer></v-spacer>

  </v-app-bar>

  <top-section-component></top-section-component>


  <v-row>
    <v-col cols="12">

      <v-card flat color="purple darken-4" style="border-radius: 15px">
        <v-card-title>
          <h2 class="font-weight-light">Professional Experience</h2>
        </v-card-title>
        <v-divider></v-divider>
        <v-card-text>
          <v-row dense>
            <v-col v-for="item in experiencList" :key="item.url" cols="12" sm="4">
              <v-card flat class="bg-purple-lighten-5" style="border-radius: 15px">
                <v-card-text>
                  <h2>{{item.position}}</h2>
                  <h5>{{item.companyName}}</h5>
                  <p>{{item.startDate}} - {{item.endDate}}</p>
                  <v-chip rounded color="indigo">{{item.type}}</v-chip>
                  <v-btn class="mt-2" variant="tonal" target="_blank" flat color="purple" :href="item.url">Visit website<sup><v-icon>mdi-arrow-right-top</v-icon></sup></v-btn>

                </v-card-text>
              </v-card>
            </v-col>
          </v-row>

        </v-card-text>
      </v-card>

    </v-col>


  </v-row>

  </v-container>

</template>

<script>
import ImageDiplayComponent from "@/components/ImageDiplayComponent";
import TopSectionComponent from "@/components/TopSectionComponent";

export default {
  name: "MainPage",
  components: {TopSectionComponent, ImageDiplayComponent},
  data() {
    return {
      experiencList: [
        {
          companyName: "Built Financial Technologies Ltd.",
          startDate: "Oct. 2019",
          endDate: "Present",
          type:"Full-Time",
          position: "CTO",
          url: "https://built.africa"

        },

        {
          companyName: "Nuna Technologies Ltd.",
          startDate: "Oct. 2022",
          endDate: "Present",
          type:"Full-Time",
          position: "CTO & Co-Founder",
          url: "https://mynunaa.com"

        },

        {
          companyName: "Seed of Hope Foundation",
          startDate: "Jun. 2021",
          endDate: "Sep. 2021",
          type:"Contract",
          position: "Web developer",
          url: "https://sohgh.org"

        },
        {
          companyName: "Tour Sissala-Kasena",
          startDate: "Jul. 2021",
          endDate: "Nov. 2021",
          type:"Contract",
          position: "Web developer",
          url: "https://sohgh.org"

        },


      ]
    }
  }
}
</script>
<style>
.large-text {
  font-size: 76px;
}
</style>


