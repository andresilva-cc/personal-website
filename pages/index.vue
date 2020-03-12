<template>
  <v-row justify="center" align="center" class="text-center">
    <!-- Profile Picture -->
    <v-col cols="12">
      <v-avatar size="250">
        <img src="/profile.jpg" />
      </v-avatar>
    </v-col>

    <!-- Personal Info -->
    <v-col cols="12">
      <div class="display-2">André Luiz da Silva</div>
      <div class="headline pt-2">CEO & Co-Founder @ Nuxstep</div>
    </v-col>

    <!-- Links -->
    <v-col cols="12">
      <v-btn
        v-for="(link, i) in links"
        :key="i"
        :ripple="false"
        icon
        :href="link.to"
        :target="link.target"
      >
        <v-icon>{{ link.icon }}</v-icon>
      </v-btn>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data() {
    return {
      links: [
        {
          icon: 'mdi-whatsapp',
          to: 'https://wa.me/5547999001415',
          target: '_blank'
        },
        {
          icon: 'mdi-instagram',
          to: 'https://www.instagram.com/andresilva.cc/',
          target: '_blank'
        },
        {
          icon: 'mdi-facebook',
          to: 'https://www.facebook.com/andresilva.cc',
          target: '_blank'
        },
        {
          icon: 'mdi-linkedin',
          to: 'https://www.linkedin.com/in/andresilvacc/',
          target: '_blank'
        },
        {
          icon: 'mdi-github',
          to: 'https://github.com/andresilva-cc',
          target: '_blank'
        },
        {
          icon: 'mdi-email',
          to: 'mailto:andreluiz.97@outlook.com',
          target: 'self'
        }
      ]
    }
  }
}
</script>
