<template>
  <v-app>
    <v-navigation-drawer clipped app width="200">
      <v-img>
        <img :src="$store.state.user.image" alt="Foto de perfil" class="pa-2 ma-2">
      </v-img>
      <v-list-item dense v-for="mn in menu" :key="mn.value">
        <v-list-item-icon>
          <v-icon v-text="mn.icon"></v-icon>
        </v-list-item-icon>
        <v-list-item-title v-text="mn.text"></v-list-item-title>
      </v-list-item>
    </v-navigation-drawer>
    <v-app-bar app clipped-left dense color="primary" dark class="elevation-2">
      <v-app-bar-nav-icon class="hidden-lg-and-up"></v-app-bar-nav-icon>
      Jícara<strong>BOOK</strong>
      <v-spacer></v-spacer>

     
    </v-app-bar>

    <v-content>
      
    </v-content>
  </v-app>
</template>

<script>


export default {
  name: "App",
  data: () => ({
    menu:[
      {value:1,text:"Perfil",icon:"mdi-account"},
      {value:2,text:"Noticias",icon:"mdi-newspaper"},
      {value:3,text:"Fotos",icon:"mdi-camera-burst"},
      {value:4,text:"Vídeos",icon:"mdi-video"},
      {value:5,text:"Notas",icon:"mdi-file"},
      {value:6,text:"Opciones",icon:"mdi-cog"},
      {value:7,text:"Salir",icon:"mdi-close-circle"},
    ]
  })
};
</script>
