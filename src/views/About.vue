<template>
  <div class="about">
    <v-container>
      <v-row class="text-center">
        <v-col cols="12">
          <h1>このサイトについて</h1>
          <v-card class="pa-7 mt-3">
            <p class="description">
              浜松市の有志のエンジニアによって、
              開発・保守されて居ます。
              下記のGitHubのリポジトリに対して
              issueやpull requestを
              追加していただくことで開発に
              貢献していただくことができます。
            </p>
            <v-btn
              href="https://github.com/matsuihidetoshi/covid19support"
              target="_blank"
              class="primary"
            >
              repository
            </v-btn>
            <p class="description mt-7">
              また、こちらのリポジトリをフォークしていただき、
              ご自由に書き換えてお使いいただくことで、
              他の地域等でも同様のサイトを構築していただいて構いません。
              こちらのサイトは、Vue.js + AWS Amplifyで環境構築しております。
              同様の環境を構築する場合、下記がご参考になります。
            </p>
            <v-btn
              href="https://github.com/matsuihidetoshi/vueamplifydev"
              target="_blank"
              class="primary"
            >
              how to launch
            </v-btn>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<style>
.description > span {
  display: inline-block;
}
</style>
