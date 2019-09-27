<template>
<div>
  <h2>New Quote</h2>
  <h3>Counter: {{ counter }}</h3>
  <button @click="counter++" class="btn btn-primary">Increase!</button>
  <!-- <button @click="addCounter" class="btn btn-primary">Increase!</button> -->
</div>
</template>

<script>
export default {
  data: function() {
    return {
      counter: 0
    }
  },
  // methods: {
  //   addCounter() {
  //     return this.counter++;
  //   }
  // }
}
</script>

<style scoped>

</style>