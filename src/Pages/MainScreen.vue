<template>
  <h1>POKE MEMORIES</h1>
  <h3>SELECT MODE TO START</h3>
  <div>
    <button @click="chooseSetting(16)">
      <div>4x4</div>
      <div>Easy</div>
    </button>
    <button @click="chooseSetting(36)">
      <div>6x6</div>
      <div>Normal</div>
    </button>
    <button @click="chooseSetting(64)">
      <div>8x8</div>
      <div>Hard</div>
    </button>
    <button @click="chooseSetting(100)">
      <div>10x10</div>
      <div>Super Hard</div>
    </button>
  </div>
</template>
<script>
export default {
  name: "MainScreen",
  data: () => {
    return {

    }
  },
  methods: {
    chooseSetting(setting) {
      this.$emit('chooseSetting',setting );
    }
  }
}
</script>
<style>

</style>