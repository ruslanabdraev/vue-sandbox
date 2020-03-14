<template>
  <v-app>
    <v-app-bar app color="primary" dark></v-app-bar>

    <v-content>
      <v-container>
        <v-row style="border: solid 1px red">
          <v-col cols="3" style="border: solid 1px green">first column</v-col>
          <v-col cols="9" style="border: solid 1px green">
            <v-row>
              second column
              <v-bottom-navigation dark>
                <v-btn @click="cameraState=!cameraState">
                  <v-icon
                    v-bind:color="cameraState? 'white': 'red'"
                    x-large
                  >{{cameraState? 'mdi-video' : 'mdi-video-off'}}</v-icon>
                </v-btn>
                <v-btn @click="phoneState=!phoneState">
                  <v-icon
                    v-bind:color="!phoneState? 'green':'red'"
                    x-large
                  >{{!phoneState? 'mdi-phone': 'mdi-phone-hangup'}}</v-icon>
                </v-btn>
                <v-btn @click="microphoneState=!microphoneState">
                  <v-icon
                    v-bind:color="microphoneState? 'white':'red'"
                    x-large
                  >{{microphoneState? 'mdi-microphone': 'mdi-microphone-off'}}</v-icon>
                </v-btn>
              </v-bottom-navigation>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </v-content>
  </v-app>
</template>


<script>
export default {
  // video - [ mdi-video | mdi-video-off ]
  // phone - [ mdi-phone | mdi-phone-hangup ]
  // microphone - [ mdi-microphone | mdi-microphone-off ]

  name: "App",

  components: {},

  data: () => ({
    cameraState: true,
    phoneState: false,
    microphoneState: true
  })
};
</script>
