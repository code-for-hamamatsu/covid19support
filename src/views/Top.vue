<template>
  <v-container>
    <v-row class="text-center">

      <v-flex xs12 sm12 md4 text-center class="pa-3 mh-10">
        <v-card min-height="400px" class="pa-3">
          <h2 class="headline font-weight-bold mb-3 mt-7">
            大事なページ
          </h2>
          <p class="description">
            浜松市では、新型コロナウイルス
            感染症防止のために各種の
            対策サイトを公開して居ます。
            オープンソースプロジェクトとして
            進行しており、下記リンクより
            開発に貢献していただくことができます。
          </p>
          <p
            v-for="(link, i) in importantLinks"
            :key="i"
            class="mx-1"
            target="_blank"
          >
            <a :href="link.href" target="_blank">{{ link.text }}</a>
          </p>
        </v-card>
      </v-flex>

    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: 'Top',

    data: () => ({
      importantLinks: [
        {
          text: '新型コロナウイルス感染症拡大防止サイト',
          href: 'https://stopcovid19-hamamatsu.netlify.com/',
        },
        {
          text: '防止サイトGitHub',
          href: 'https://github.com/code-for-hamamatsu',
        },
        {
          text: 'このサイトのGitHub',
          href: 'https://github.com/matsuihidetoshi/mochikaeru20200414',
        },
      ],
      map: "https://www.google.com/maps/d/embed?mid=1znYQhKGizcZab2ZTFwQ8r88Kekl1IiQn&hl=ja",
    }),
  }
</script>
<style>
.description span {
  display: inline-block;
}
.map {
    width: 90%;
    margin: 5%;
    height: 400px;
}
</style>