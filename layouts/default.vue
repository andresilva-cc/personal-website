<template>
  <v-app>
    <v-app-bar flat fixed app color="transparent">
      <v-spacer />
      <v-btn
        :ripple="false"
        icon
        @click.stop="$vuetify.theme.dark = !$vuetify.theme.dark"
      >
        <v-icon>mdi-brightness-6</v-icon>
      </v-btn>
    </v-app-bar>
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
  </v-app>
</template>
