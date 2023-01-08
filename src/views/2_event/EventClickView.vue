<template>
  <div>
    <button @click="increasCounter">Add 1</button>
    {{ count }}
  </div>
</template>
<script>
export default {
  data() {
    return {
      count: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    increasCounter() {
      this.count+=1
    }
  }
}
</script>
<style scoped>

</style>
