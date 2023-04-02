<template>
  <div id="personaje">
    <List/>
  </div>
</template>


<script>
import List from '../components/List'

export default {
  name: 'Personaje',
  components: {
    List
  }
}
</script>

<style>
#personaje {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  height: 150%;
}
</style>