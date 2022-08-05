<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <v-toolbar-title>我的网站</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn href="https://wuyuan.dev" target="_blank" text>
        <span class="mr-2">作者博客</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>


      <template>



        <v-container >
          <v-row>
            <v-col v-for="card in cards" :key="card.title" cols="12" sm="4">
              <v-card>
                <v-img :src="card.src" class="white--text align-end"
                  gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.2)" height="auto">
                  <v-card-title v-text="card.title"></v-card-title>
                </v-img>

                <v-card-actions><v-text v-text="card.text" class="mx-2"></v-text>
                  <v-spacer></v-spacer>

                  <v-btn :href="card.link">访问
                    <v-icon>mdi-open-in-new</v-icon>
                  </v-btn>

 
                </v-card-actions>
              </v-card>
            </v-col>
          </v-row>
        </v-container>

      </template>
    </v-main>
  </v-app>
</template>

<script>
export default {
}
</script>

<script>
  export default {
    data: () => ({
      cards: [
        { title: '博客', src: 'https://cdn.wuyuan.dev/img/wz_wuyuan~dev.jpeg',  link: 'https://wuyuan.dev' , text: '我的博客，也是个人主页哦'},
        { title: '网站状态', src: 'https://cdn.wuyuan.dev/img/网页捕获_31-7-2022_143648_status.wuyuan.dev.jpeg',  link: 'https://status.wuyuan.dev/', text: '我的博客，也是个人主页哦'},
        { title: '网页sans启动器', src: 'https://cdn.wuyuan.dev/img/20220731144055.png',  link: 'https://sans.wuyuan.dev', text: '我的博客，也是个人主页哦'},
        { title: 'Best airlines', src: 'https://codeyuan.tk/bj.png',  link: '', text: '我的博客，也是个人主页哦'},
      { title: 'Best airlines', src: 'https://codeyuan.tk/bj.png',  link: '', text: '我的博客，也是个人主页哦'},
      
      ],
    }),
  }
</script>