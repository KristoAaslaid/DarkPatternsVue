<script setup>

</script>


<script>
export default{
  data(){
    return {
      cum: false,
      count: 0,
      kasutajanimi: "",
    }
  },
  methods: {
    funnistuff(){
      this.count++;
    },
    kasutajabaasi(){

    },
  }
}


</script>

<template>
<button class="settings"></button>
<div>
<button class="button1" @click="funnistuff()">{{count}}</button>
<input class="kasutaja" v-model="kasutajanimi" placeholder="Kasutajanimi">
<button class="enterkasutaja" @click="kasutajabaasi()">Enter</button>
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
  background: url("././assets/FirstPageD.png") no-repeat center center fixed;
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
  top:1%;
  left: 1%;
  position: absolute;
}
</style>