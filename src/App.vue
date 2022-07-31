<template>
  <v-app>
    <v-row>
      <v-btn color="primary" class="ma-3" href="https://status.wuyuan.dev/">网站状态</v-btn>
      <v-col cols="auto">
        <v-dialog transition="dialog-bottom-transition" max-width="600">
          <template v-slot:activator="{ on, attrs }">
            <v-btn color="primary" v-bind="attrs" v-on="on">作品</v-btn>
          </template>
          <template v-slot:default="dialog">
            <v-card>
              <v-toolbar color="primary" dark>我的作品</v-toolbar>

<div style="height: 300px;overflow: auto;">
              <v-btn color="primary" class="ma-2" href="https://baidu.com">工具1</v-btn>
              <v-btn color="primary" class="ma-2" href="https://baidu.com">工具1</v-btn>

</div>

              <v-card-actions class="justify-end">
                <v-btn text @click="dialog.value = false">关闭</v-btn>
              </v-card-actions>
            </v-card>
          </template>
        </v-dialog>
      </v-col>
      <v-btn color="primary" class="ma-3" href="https://wuyuan.dev/about/">关于我</v-btn>
    </v-row>
  </v-app>
</template>

