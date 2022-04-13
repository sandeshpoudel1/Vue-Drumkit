<template>
  <div id="app">
    <h1> Vue Drumkit</h1>
    <div class="keys">
     <key v-for="(key,i) in keys" :sound="key" :key="i" />
   </div>
  </div>
</template>

<script>

import key from './components/key.vue'
export default {
  name: 'App',
  data(){
  return{
    keys:[
        {
          name:"boom",
          audio: require("./assets/sounds/src_assets_sounds_boom.wav"),
          letter:"A"
        },
        {
          name:"clap",
          audio: require("./assets/sounds/src_assets_sounds_clap.wav"),
          letter:"S"
        },
          {
          name:"hihat",
          audio: require("./assets/sounds/src_assets_sounds_hihat.wav"),
          letter:"D"
        },
          {
          name:"kick",
          audio: require("./assets/sounds/src_assets_sounds_kick.wav"),
          letter:"F"
        },
          {
          name:"openhat",
          audio: require("./assets/sounds/src_assets_sounds_openhat.wav"),
          letter:"G"
        },  {
          name:"ride",
          audio: require("./assets/sounds/src_assets_sounds_ride.wav"),
          letter:"H"
        },  {
          name:"snare",
          audio: require("./assets/sounds/src_assets_sounds_snare.wav"),
          letter:"J"
        },
          {
          name:"tink",
          audio: require("./assets/sounds/src_assets_sounds_tink.wav"),
          letter:"K"
        },
          {
          name:"tom",
          audio: require("./assets/sounds/src_assets_sounds_tom.wav"),
          letter:"L"
        },
        


      ]
    }
  },
  components: {
    key
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.keys{
  display:flex;
  align-items:center;
  justify-content: center;
}
</style>
