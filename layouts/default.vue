<template>
  <v-app>
    <v-card>
      <v-app-bar
        absolute
        dark
        height="200px"
        shrink-on-scroll
        src="https://www.turascandinavia.com/storage/7C6ACE1E90CE0A9FB9BBEACF0CBD22AE42C4BA575D261172B9F693DE925F770F/93b8964eca5d4451a067e6cf2d2e8961/jpg/media/8ed8e637aa3d4b02b46eac6e6ae3afe7/AVENGERS_COVER.jpg"
      >

      <template v-slot:extension>
        <v-tabs align-with-title>
          <v-tab><v-icon>mdi-magnify</v-icon></v-tab>
        </v-tabs>
      </template>

      </v-app-bar>

    </v-card>

    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>

    <v-footer>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
      title: 'MARVEL',
    }
  },
}
</script>

<style>

</style>

