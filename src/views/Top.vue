<template>
  <v-container>
    <h2 class="headline font-weight-bold mb-3 ma-7 text-center">
      各種行政機関の<br>COVID-19対策まとめ
    </h2>
    <v-row class="text-center">
      <v-flex 
        v-for="(information, index) in informations"
        v-bind:key="index"
        xs12 sm6 md4 text-center
        class="pa-3 mh-10"
      >
        <v-card class="pa-3">
          <v-card-title>
            {{ information.title }}
          </v-card-title>
          <v-card-text>
            <p class="scrollArea">
              {{ information.text }}
            </p>
            <v-btn
              :href="information.url"
              target="_blank"
              class="primary"
            >
              go
            </v-btn>
          </v-card-text>
        </v-card>
      </v-flex>

    </v-row>
  </v-container>
</template>

<script>
  import informations from '../data/informations.json'
  export default {
    name: 'Top',
    data () {
      return {
        informations: informations,
        offsetTop: 0,
      }
    }
  }
</script>
<style>
.scrollArea {
  height:200px;
  overflow:scroll;
}
</style>