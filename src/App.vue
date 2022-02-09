<template>
  <v-app>
    <v-app-bar app color="yellow lighten-3" dark>
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
        to ="/"
        color="blue lighten-3"
        
      >
        <span class="mr-2">Home</span>
        </v-btn>
        &nbsp;
      <v-btn
        to ="/about"
        color="blue lighten-3"
      >
        <span class="mr-2">About</span>
      </v-btn>
      &nbsp;
      <v-btn
        to ="/todo"
        color="blue lighten-3"
      >
        <span class="mr-2">Todo</span>
      </v-btn>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    
  }),
};
</script>
