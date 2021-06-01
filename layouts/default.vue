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
    <v-main>
      <v-container fill-height>
        <nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  created() {
    const hours = new Date().getHours()
    if (hours >= 18 || hours < 6) this.$vuetify.theme.dark = true
  }
}
</script>
