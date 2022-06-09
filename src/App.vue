<script setup>

</script>


<script>
export default{
  data(){
    return {
      cum: false,
      count: 0,
      kasutajanimi: "",
      settingsmenu: false,
      startgame: false,
    }
  },
  methods: {
    funnistuff(){
      this.count++;
    },
    kasutajabaasi(){
      this.startgame = !this.startgame;
    },
    settingsfunc(){
      this.settingsmenu = !this.settingsmenu;
      this.startgame = !this.startgame;
    }
  }
}


</script>

<template>
<button class="settings" @click="settingsfunc"></button>
<div class="settingsmenu" v-if="settingsmenu">
  <button name="settingsfunni" class="buttonfunnisetting" @click="funnistuff()">Language</button>
  <div class="switch">
  <input class="slider" type="checkbox" name="Sound" id="Sound">
  </div>
</div>

<div v-if="settingsmenu != true && startgame != true">
  <button name="avaleht" class="button1" @click="funnistuff()">{{count}}</button>
  <input class="kasutaja" v-model="kasutajanimi" placeholder="Kasutajanimi" maxlength="14">
  <button class="enterkasutaja" @click="kasutajabaasi()">Alusta mängu</button>
</div>

<div class="story" v-if="startgame == true">
  <div class="localisation">
  <p>Nüüd see on gaming, POG</p>
  </div>
</div>

  <main>
    
  </main>
</template>


<style>
@import './assets/base.css';

#app {
  margin: 0;
  padding: 2rem;
  font-weight: normal;
}

html {
  background-color: rgba(4, 22, 99, 0.87);
  background-size: cover;
  overflow: hidden;
}

.button1 {
  display: flex;
  background-color: #a14337;
  border-color: yellow;
  border-radius: 9px;
  color: rgb(0, 0, 0);
  text-align: center;
  text-decoration: none;
  display: inline-block;
  padding: 0.2rem;
  width: 10vw;
  height: 5vh;
  font-size: 1.5vw;
  cursor: pointer;
  top:50%;
  left: 50%;
  position: absolute;
}

.kasutaja {
  display: flex;
  background-color: #a14337;
  border-color: yellow;
  border-radius: 9px;
  color: rgb(0, 0, 0);
  text-align: center;
  text-decoration: none;
  display: inline-block;
  padding: 0.2rem;
  width: 10vw;
  height: 5vh;
  font-size: 1.5vw;
  cursor: pointer;
  top:40%;
  left: 40%;
  position: absolute;
}

.enterkasutaja {
  display: flex;
  background-color: #a14337;
  border-color: yellow;
  border-radius: 9px;
  color: rgb(0, 255, 76);
  text-align: center;
  text-decoration: none;
  display: inline-block;
  padding: 0.2rem;
  width: 10vw;
  height: 4vh;
  font-size: 1.5vw;
  cursor: pointer;
  top:40%;
  left: 52%;
  position: absolute;
}

.settings{
  background-image: url("././static/settings.png");
  background-position: 0% 0%;
  background-repeat: no-repeat;
  background-size: contain;
  background-color: transparent;
  border-color: rgba(0, 0, 0, 0);
  display: flex;
  width: 3vw;
  height: 3vw;
  cursor: pointer;
  top: 0%;
  left: 0%;
  position: absolute;
}

.buttonfunnisetting {
  display: flex;
  background-color: #a14337;
  border-color: yellow;
  border-radius: 9px;
  color: rgb(0, 255, 76);
  text-align: center;
  text-decoration: none;
  display: inline-block;
  padding: 0.2rem;
  width: 10vw;
  height: 4vh;
  font-size: 1.5vw;
  cursor: pointer;
  top:10%;
  left: 5%;
  position: absolute;
}

.slider{
  position: absolute;
  cursor: pointer;
  top: 12%;
  left: 25%;
  right: 0;
  bottom: 0;
  background-color: #ccc;
  -webkit-transition: .4s;
  transition: .4s;
}

.localisation{
  position: absolute;
  top: 72%;
  left: 50%;
}

/* .switch vaja lisada, praegu lihtsalt checkbox, send help!!!!! */
</style>