<template>
  <v-container>
    <v-row>
      <v-col>
        <v-card>
          <v-card-title>
            <h1 style="line-height: initial;" id="title">
              Welcome to 
              <br class="d-flex d-sm-none">
              <span style="font-size:50px;">YUSUKE's</span>
               portfolio!
            </h1>
          </v-card-title>
          <v-card-text>
            <v-row justify="space-between">
              <v-col cols="10" sm="3">
                <v-avatar size="150">
                  <img src="../assets/profile/img/faceIR.jpg" alt="yusuke">
                </v-avatar>
              </v-col>
              <v-col cols="10" sm="9">
                <v-card-text>
                  本業の傍らプログラムやWeb関連の知識、デザインを学習中。<br>
                  主に書籍、Udemy、paiza等から学び、webサービスやアプリを作りながら独学しています。<br>
                  没頭するタイプで、プログラムでものをつくっている時がとにかく楽しくて大好き！<br>
                  得意な言語はJavaScriptです。<br>
                  現在はサーバーサイドにPHPを猛勉強中です。
                </v-card-text>
              </v-col>
               <v-col cols="12">
                <v-card-text class="pa-0">
                  <span class="green--text title">学習開始から...</span>
                  <clock-box class="black--text"></clock-box>
                </v-card-text>
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import ClockBox from './ClockBox.vue'
import ShuffleText from "shuffle-text"

export default {
  components: { ClockBox },
  name: 'ProfileBox',
  data: function() {
    return {
    }
  },
  mounted: function() {
    const title = document.getElementById('title')
    const shulle =  new ShuffleText(title)
    shulle.start()
  }
}
</script>

