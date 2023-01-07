<template>
  <div>
  <div>
    <input type="radio" name="" id="html" value="HTML" v-model="favoriteLang" />
    <label for="html">HTML</label>
  </div>
  <div>
    <input type="radio" name="" id="css" value="css" v-model="favoriteLang" />
    <label for="css">CSS</label>
  </div>
  <div>
    <input type="radio" name="" id="js" value="js" v-model="favoriteLang" />
    <label for="js">JavaScript</label>
  </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      favoriteLang: ''
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
