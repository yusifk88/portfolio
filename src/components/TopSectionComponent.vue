<template>
  <v-row>
    <v-col cols="12" sm="6">
      <v-sheet class="pa-6 ma-6">
        <h1 class="font-weight-bold">Hi! I Am </h1>
        <h1 class="font-weight-bold large-text">Yusif Katulie</h1>
        <h4 class="font-weight-light mb-3">A fullstack web developer with over
          8 years of experience in web application development.</h4>
        <h2 class="mb-3 mt-4">Technology stack:</h2>
        <v-chip color="error lighten-5 red--text" class="ma-2">Laravel</v-chip>
        <v-chip color="green lighten-5 green--text" class="ma-2">Vue JS</v-chip>
        <v-chip color="primary lighten-5 green--text" class="ma-2">Vuetify</v-chip>
        <v-chip color="purple lighten-5 purple--text" class="ma-2">Boostrap</v-chip>
        <v-chip color="secondary lighten-5 secondary--text" class="ma-2">Ionic Framework</v-chip>
        <v-chip color="blue lighten-5 blue--text" class="ma-2">Mysql</v-chip>

        <v-divider></v-divider>


        <h2>Socials:</h2>

            <v-btn href="https://www.linkedin.com/in/yusif-katulie-00a90414b/" target="_blank" color="primary" class="ma-2" variant="text"><v-icon>mdi-linkedin</v-icon>Linkedin <sup><v-icon>mdi-arrow-right-top</v-icon></sup></v-btn>
            <v-btn href="https://twitter.com/@ykatulie" target="_blank" color="blue" class="ma-2" variant="text"><v-icon>mdi-twitter</v-icon>Twitter <sup><v-icon>mdi-arrow-right-top</v-icon></sup></v-btn>
            <v-btn href="https://github.com/yusifk88" target="_blank" color="black" class="ma-2" variant="text"><v-icon>mdi-github</v-icon>Github <sup><v-icon>mdi-arrow-right-top</v-icon></sup></v-btn>




        <h2 class="mt-4">Contact:</h2>


            <v-list class="mt-4">

              <v-list-item href="mailto:ykatulie@gmail.com" class="border-b">
                <template v-slot:prepend>
                  <v-icon color="blue">mdi-email-check-outline</v-icon>
                </template>

                <v-list-item-title class="font-weight-bold">
                  Ykatulie@gmail.com
                </v-list-item-title>
                <v-list-item-subtitle>Email</v-list-item-subtitle>
              </v-list-item>
              <v-list-item>
                <template v-slot:prepend>
                  <v-icon color="red">mdi-map-marker-multiple-outline</v-icon>
                </template>
                <v-list-item-title class="font-weight-bold">
                  Accra,Ghana
                </v-list-item-title>
                <v-list-item-subtitle>Address</v-list-item-subtitle>
              </v-list-item>


            </v-list>



      </v-sheet>


    </v-col>

    <v-col cols="12" sm="6" >

      <v-card color="#ECC9EE" flat mx-height="86vh" style="border-radius: 15px">
        <image-diplay-component></image-diplay-component>

      </v-card>

    </v-col>

  </v-row>

</template>

<script>
import ImageDiplayComponent from "@/components/ImageDiplayComponent";
export default {
  name: "TopSectionComponent",
  components: {ImageDiplayComponent}
}
</script>

<style scoped>

</style>
