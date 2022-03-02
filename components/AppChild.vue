<template>
  <div class="item">
    <h2>{{item}}</h2>
    <img :src="url" width="235" height="300" alt="">
    <div class="quantity">
        <button class="inc" @click="counter > 0 ? decrementing() : 0">-</button>
        <span>Quantity: {{counter}}</span>
        <button class="inc" @click="incrementing()">+</button>
    </div>
    <button class="submit">Submit</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      counter: 0
    }
  },
  props: ['item', 'url'],
  methods: {
    decrementing () {
      this.counter -= 1;
    },
    incrementing () {
      this.counter += 1;
    }
  }
}
</script>

