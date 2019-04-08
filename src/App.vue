<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" style="height: 550px;padding: -80px;"><br/>
    <div id="first">
      <h1> Welcome !</h1>

      <div class="boite"><p>Welcome to my little mini-game created with Javascript.
        You'll probably just spend a few minutes before leaving this game
        but this game won't ever forget you (Except if you delete the cookies. Please don't do that).</p></div>

      <character-creator></character-creator>


    </div>
    <a id="restore" v-on:click="restart()">Click here to start again your doll. [CLICK + RELOAD]</a>



  </div>
</template>

<script>
import CharacterCreator from './components/CharacterCreator.vue'

export default {
  name: 'app',
  components: {
    CharacterCreator
  },
  data: function () {
    return {}
  },
  mounted() {
    if (!localStorage.noFirstVisit) {
      document.getElementById('first').style.display = 'block';

      localStorage.noFirstVisit = "1";
    }
  },
  methods: {
    restart() {
      localStorage.noFirstVisit = "";
      document.getElementById('restore').innerHTML = "You can now reload the page";
    }
  }
}
</script>

<style>
  ::selection {
    background: crimson; /* WebKit/Blink Browsers */
  }
  body{
    background-color: black;
    color: white;
  }
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
  h3 {
    margin: 40px 0 0;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: deeppink;
  }
  p{
    padding: 20px;
    font-size: 16px;
    margin-right: auto;
    margin-left: auto;
    color: white;
  }

  h1{
    margin-right: auto;
    margin-left: auto;
    width: 80%;
    background: crimson;
    font-size: 24px;
    text-align: center;
    color: white;
  }
  .boite{
    width: 80%;
    margin-right: auto;
    margin-left: auto;

  }
  #first {
    display: none;
  }
</style>
