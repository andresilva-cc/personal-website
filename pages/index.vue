<template>
  <v-row justify="center" align="center" class="text-center content">
    <!-- Profile Picture -->
    <v-col cols="12">
      <v-avatar size="250">
        <img src="/profile.jpg">
      </v-avatar>
    </v-col>

    <!-- Personal Info -->
    <v-col cols="12">
      <div class="text-h3 primary--text">
        {{ name }}
      </div>
      <div class="text-h5 pt-2">
        {{ title }}
      </div>
      <div v-if="currentJob" class="text-body-1 pt-2">
        {{ currentJob.title }} @ {{ currentJob.company }}
      </div>
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

    <!-- Resume -->
    <v-col cols="12">
      <v-btn text color="primary" href="/resume.pdf" target="_blank">
        Resume
      </v-btn>
      <v-btn text color="primary" href="/curriculo.pdf" target="_blank">
        Currículo
      </v-btn>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data () {
    return {
      name: 'André Luiz da Silva',
      title: 'Software Engineer',
      currentJob: false,

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

<style scoped>
.content {
  margin-top: -100px;
}
</style>
