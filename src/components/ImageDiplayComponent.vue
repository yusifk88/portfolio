<template>
<div class="pt-6">

  <v-avatar  class="icon-container pa-4 laravel" size="90" color="white">
 <v-img  src="@/assets/icon/laravel.svg"></v-img>
  </v-avatar>


  <v-avatar  class="icon-container pa-4 vue" size="90" color="white">
 <v-img  src="@/assets/icon/vuejs.svg"></v-img>
  </v-avatar>



  <v-avatar  class="icon-container pa-4 docker" size="90" color="white">
 <v-img  src="@/assets/icon/js.svg"></v-img>
  </v-avatar>

  <v-avatar  class="icon-container pa-4 bootstrap" size="90" color="white">
 <v-img  src="@/assets/icon/bootstrap.svg"></v-img>
  </v-avatar>

  <v-avatar  class="icon-container pa-4 linux" size="90" color="white">
 <v-icon color="orange darken-5" size="x-large" style="font-size: 60px">mdi-penguin</v-icon>
  </v-avatar>


  <v-img src="@/assets/img/yusif.png" eager class="mt-6"></v-img>
</div>

</template>

<script>
export default {
  name: "ImageDiplayComponent"
}
</script>

<style>
@keyframes paulse {

  0%{
    transform: scale(1);
  }

  50%{
    transform: scale(1.2);
  }

  100%{
    transform: scale(1);
  }


}

.icon-container{
  box-shadow: -1px -1px 26px 2px rgba(0,0,0,0.16);
  -webkit-box-shadow: -1px -1px 26px 2px rgba(0,0,0,0.16);
  -moz-box-shadow: -1px -1px 26px 2px rgba(0,0,0,0.16);
  position: absolute!important;
  margin: 10px;
  z-index: 99;
  transition: 0.3s ease-in-out;
  animation: paulse 3s ease-in-out infinite;
}
.docker{
  top: 1rem;
  left: 1.5rem;

}

.laravel{
  top: 20rem;
  left: 1rem;
}
.bootstrap{
  top: 1rem;
  right: 5rem;
}

.linux{
  top: 26rem;
  right: 6rem;
}
.vue{
  top: 10rem;
  right:0!important;
}
</style>
