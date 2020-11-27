<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <div class="text-center">
        <logo />
      </div>
      <v-card>
        <v-card-title class="headline"> Welcome to Chordbook </v-card-title>
        <v-card-text>
          <p>
            Powered by Vue and Vuetify.js
            <img
              width="10px"
              class="VuetifyLogo"
              alt="Vuetify Logo"
              src="/vuetify-logo.svg"
            />
          </p>
        </v-card-text>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo,
  },
}
</script>
