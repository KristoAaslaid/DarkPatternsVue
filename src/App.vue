<script setup>

</script>


<script>
export default{
  data(){
    return {
      cum: false,
      count: 0,
    }
  },
  methods: {
    funnistuff(){
      this.count++;
    }
  }
}


</script>

<template>

<button class="button1" @click="funnistuff()">{{count}}</button>
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

</style>