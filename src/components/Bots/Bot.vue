<template>
  <div>
      <div>
          <button @click='onFight'>FIGHT</button>
      </div>
      <div v-for='bot in battleBots' :key='bot.id'>
        <p>Selected: {{bot.name, bot.name}}</p>
        <hr>
      </div>
  </div>
</template>

<script>
export default {
props: ['battleBots'],

methods: {
    onFight(){
        var winner = this.battleBots[Math.floor(Math.random()*this.battleBots.length)];
       alert(winner.name + ' ' + "is the winner!")
    }
}
}
</script>

<style>

</style>
