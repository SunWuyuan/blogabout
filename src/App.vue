<template>
  <v-app>
    <!-- <v-app-bar app color="primary" dark>
     <img src="https://cdn.wuyuan.dev/img/logoyuan.png" width="30"> <v-toolbar-title>孙悟元-知识创造一切</v-toolbar-title>
      <v-spacer></v-spacer>

      <v-btn href="https://github.com/sunwuyuan" target="_blank" text>
        <span class="mr-2">GitHub</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>-->


    <v-main>
      <template>
        <v-carousel cycle height="400" hide-delimiter-background show-arrows-on-hover v-ripple>
          <v-carousel-item v-for="(slide, i) in slides" :key="i">
            <v-sheet :color="colors[i]" height="100%">
              <v-row class="fill-height" align="center" justify="center">
                <div class="text-h2" style="color:#ffffff">
                  {{ slide }}
                </div>
              </v-row>
            </v-sheet>
          </v-carousel-item>
        </v-carousel>
      </template>
      <template>
        <v-row justify="center">


          <v-container>
            <v-row v-bind="attrs" v-on="on">
              <v-col v-for="card in cards" :key="card.title" :sm="card.flex">
                <v-col>
                  <v-card v-ripple min-height="150" @click="LinkTo(card.link)">
                    <v-card-title class="text-h5">
                      {{ card.title }}
                    </v-card-title>

                    <v-card-subtitle>{{ card.about }}</v-card-subtitle>
                    <v-card-text>点击访问</v-card-text>
                  </v-card>
                </v-col>

              </v-col>
            </v-row>

          </v-container>

        </v-row>

      </template>


    </v-main>
  </v-app>
</template>



<script>

export default {
  data: () => ({
    cards: [
      { title: '博客', link: 'wuyuan.dev', about: '我的博客', flex: "3" },
      { title: '网站状态', link: 'uptime.wuyuan.dev', about: '我的网站状态监控', flex: "3" },
      { title: '网页sans启动器', link: 'sans.wuyuan.dev', about: '快速找到你想要的网页版sans游戏', flex: "3" },
      { title: '元长', link: 'longlink.wuyuan.dev', about: '沙雕长链接', flex: "3" },
      { title: '悟元短链接', link: 'url.wuyuan.dev', about: '一个自己在用的短链接服务', flex: "3" },
      { title: '2103班', link: '2103.wuyuan.dev', about: '班级(非)官网', flex: "3" },
      { title: 'cdm', link: 'cdm.wuyuan.dev', about: '快速下载网易云音乐资源', flex: "3" },
      { title: '元启', link: 'yuanqi.wuyuan.dev', about: '浏览器起始页', flex: "3" },
      { title: '资源站', link: 'drive.wuyuan.dev', about: '个人资源站', flex: "3" },
      { title: '私有Alist', link: 'alist.wuyuan.dev', about: '私有Alist服务', flex: "3" },
      { title: '私有密码管理', link: '这个服务悟元不给链接哈哈哈', about: '私有密码管理服务', flex: "3" },
    ],
    colors: [
      'primary',

    ],
    slides: [
      '孙悟元 知识创造一切',

    ],
    dialog: false,
    notifications: false,
    sound: true,
    widgets: false,

    LinkTo(url) {
      window.open("https://" + url, '_blank') // 新窗口打开外链接
    },
  }),


}
</script>