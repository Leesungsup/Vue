<template>
  <div>
    <div style="color: red; font-size: 30px;">
    스타일
    </div>
    <div :style="style1">
    스타일
    </div>
    <button @click="style1.color='blue'">색상바꾸기</button>
  </div>
</template>
<script>
export default {
  data() {
    return{
      style1: {
        color: 'green',
        fontSize: '30px'
      }
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
<style scoped>

</style>