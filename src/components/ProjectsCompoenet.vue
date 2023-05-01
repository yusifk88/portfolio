<template>
  <v-row class="bg-purple-lighten-5">
    <v-col cols="12" class="text-center">
      <h2>Projects</h2>
      <p class="text-disabled">
        This section is made of a collection of projects i worked on together with a team or solo.
      </p>
    </v-col>

    <v-col cols="12" sm="6" v-for="project in projects" :key="project.src">
      <v-card flat class="ma-3" style="border-radius: 15px">
        <v-card-text class="text-center">
          <h2>{{project.title}}</h2>
          <p class="text-disabled">{{project.description}}</p>
          <v-btn v-if="project.link" target="_blank" variant="text" color="purple">Preview <sup><v-icon size="small">mdi-arrow-right-top</v-icon></sup></v-btn>

        </v-card-text>
        <v-img :src="project.src"></v-img>

      </v-card>


    </v-col>


  </v-row>

</template>

<script>
export default {
  name: "ProjectsCompoenet",
  data(){
    return{
      projects: [
        {
          title: "Accounting SAAS",
          description: "Cloud accounting and finance platform",
          link: "https://built.africa",
          src: "/screens/built.png"
        },
        {
          title: "Nuna Landing page",
          description: "Landing page for Nuna the digital wedding registry app",
          link: "https://mynunaa.com",
          src: "/screens/nuna.png"
        },
        {
          title: "Seed of Hope Foundation website",
          description: "NGO Website for Seed of hope a child support and child rights support NGO",
          link: "https://sohgh.org",
          src: "/screens/soh.png"
        },
        {
          title: "Tour Sissala Kasena",
          description: "A tourism display website for sites in the Northern part of Ghana",
          link: "https://toursissalakasena.com/",
          src: "/screens/tour.png"
        },
        {
          title: "Sales and income Tax Calculator",
          description: "Sales and income tax calculator for over 36 countries",
          link: null,
          src: "/screens/tax.png"
        },
        {
          title: "Nuna Mobile App",
          description: "Mobile for Nuna the digital wedding registry",
          link: "https://play.google.com/store/apps/details?id=com.nuna.app",
          src: "/screens/nuna_mobile.png"
        }

      ],

    }
  }
}
</script>

<style scoped>

</style>
