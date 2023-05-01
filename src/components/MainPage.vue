<template>
  <v-container fluid>

    <v-app-bar rounded floating scroll-behavior="hide" class="border-b" flat>
      <v-spacer></v-spacer>
      <v-app-bar-title class="ma-5 ml-5">
        <v-badge color="purple" dot location="bottom end" offset-x="-8" offset-y="6">

          <h2>Yusif</h2>
        </v-badge>
      </v-app-bar-title>
      <v-btn class="d-none d-md-block">Home</v-btn>
      <v-btn class="d-none d-md-block" @click="$vuetify.goTo({target:'#exp-card'})">Experience</v-btn>
      <v-btn class="d-none d-md-block">Projects</v-btn>
      <v-btn class="d-none d-md-block">Services</v-btn>
      <v-spacer class="d-sm-none d-md-block"></v-spacer>
      <v-btn href="mailto:ykatulie@gmail.com" variant="outlined">Let's Chat</v-btn>

      <v-spacer></v-spacer>

    </v-app-bar>

    <top-section-component></top-section-component>


    <v-row>
      <v-col cols="12">

        <v-card id="exp-card" class="bg-purple-darken-4" flat style="border-radius: 15px">
          <v-card-title>
            <h2 class="font-weight-light text-center">Professional Experience</h2>
          </v-card-title>
          <v-divider></v-divider>
          <v-card-text>
            <v-row dense>
              <v-col v-for="item in experiencList" :key="item.url" cols="12" sm="4">
                <v-card class="bg-purple-lighten-5" flat style="border-radius: 15px">
                  <v-card-text>
                    <h2 class="font-weight-light">{{ item.position }}</h2>
                    <h5 class="font-weight-light">{{ item.companyName }}</h5>
                    <p>{{ item.startDate }} - {{ item.endDate }}</p>
                    <v-chip color="indigo" rounded size="small">{{ item.type }}</v-chip>
                    <v-btn :href="item.url" class="mt-2" color="purple" flat size="small" target="_blank"
                           variant="text">Visit
                      website<sup>
                        <v-icon>mdi-arrow-right-top</v-icon>
                      </sup></v-btn>

                  </v-card-text>
                </v-card>
              </v-col>
            </v-row>

          </v-card-text>
        </v-card>

      </v-col>
    </v-row>

    <projects-compoenet></projects-compoenet>

  </v-container>

  <v-footer
    class="bg-black"
  >
    <div>
      <v-btn
        v-for="icon in icons"
        :key="icon.name"
        :icon="icon.name"
        class="mx-4"
        variant="text"
      ></v-btn>
    </div>

    <div class="pt-0">
      This portfolio website was made with Vue JS using the Vuetify component library with inspirations from <a
      href="https://dribbble.com/shots/18363312-Richard-Freelancer-Portfolio?showSimilarShots=true&_=1681594681783">Richard's
      design on Dribble</a>
    </div>

    <v-divider></v-divider>

    <div>
      {{ new Date().getFullYear() }} —
      <v-badge color="purple" dot location="bottom end" offset-x="-8" offset-y="6">

        <strong>Yusif</strong>
      </v-badge>
    </div>
  </v-footer>

</template>

<script>
import ImageDiplayComponent from "@/components/ImageDiplayComponent";
import TopSectionComponent from "@/components/TopSectionComponent";
import ProjectsCompoenet from "@/components/ProjectsCompoenet";

export default {
  name: "MainPage",
  components: {ProjectsCompoenet, TopSectionComponent, ImageDiplayComponent},
  data() {
    return {
      icons: [
        {
          name: 'mdi-twitter',
          url: ""
        },
        {
          name: 'mdi-linkedin',
          url: ""
        },
        {
          name: 'mdi-github',
          url: ""
        }
      ],
      experiencList: [
        {
          companyName: "Built Financial Technologies Ltd.",
          startDate: "Oct. 2019",
          endDate: "Present",
          type: "Full-Time",
          position: "CTO",
          url: "https://built.africa"

        },

        {
          companyName: "Nuna Technologies Ltd.",
          startDate: "Oct. 2022",
          endDate: "Present",
          type: "Full-Time",
          position: "CTO & Co-Founder",
          url: "https://mynunaa.com"

        },

        {
          companyName: "Seed of Hope Foundation",
          startDate: "Jun. 2021",
          endDate: "Sep. 2021",
          type: "Contract",
          position: "Web developer",
          url: "https://sohgh.org"

        },
        {
          companyName: "Tour Sissala-Kasena",
          startDate: "Jul. 2021",
          endDate: "Nov. 2021",
          type: "Contract",
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


