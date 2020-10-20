<template>
  <div>
    <h1>Total de ventas</h1>
    <h2>Tus juegos comprados:</h2>
    <ul>
      <li v-for="(number, game) in totalGamesSold" :key="game.id">{{game}} - {{number}}</li>
    </ul>
    <ul>
      <h2>Ventas totales</h2>
      <li v-for="game in sales" :key="game.id">Id: {{game.id}} |Name: {{game.name}} |Price: {{game.price}}</li>
    </ul>
    <ul>
      <p>Monto total: $ {{totalAmount}}</p>
    </ul>
  </div>
</template>

<script>
import{
  mapGetters,
  mapState
} from 'vuex'
export default {
  computed: {
    ...mapGetters(['totalGamesSold','totalAmount']),
    ...mapState(['sales']),
  }
}
</script>

<style>

</style>