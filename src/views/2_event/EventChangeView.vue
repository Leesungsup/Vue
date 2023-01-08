<template>
  <div>
    <select name="" id="" @change="changecity($event)" v-model="selectedCity">
      <option value="">도시선택</option>
      <option value="city.code" :key="city.code" v-for="city in cityList">{{ city.title }}</option>
    </select>
    <select name="" id="">
      <option :value="dong.dongCode" :key="dong.dongCode" v-for="dong in dongList">
        {{ dong.dongtitle }}
      </option>
    </select>
    <select name="" id="">
      <option :value="dong.dongCode" :key="dong.dongCode" v-for="dong in dongList.filter(dong => dong.code === selectedCity)">
        {{ dong.dongtitle }}
      </option>
    </select>
  </div>
</template>
<script>
export default {
  data() {
    return {
      selectedCity: '',
      cityList: [
        { title: '서울', code: '02' },
        { title: '부산', code: '051' },
        { title: '제주', code: '064' }
      ],
      dongList: [
        { dongcode: '1', code: '02', dongtitle: '서울 1동' },
        { dongcode: '2', code: '02', dongtitle: '서울 2동' },
        { dongcode: '3', code: '02', dongtitle: '서울 3동' },
        { dongcode: '4', code: '02', dongtitle: '서울 4동' },
        { dongcode: '1', code: '051', dongtitle: '부산 1동' },
        { dongcode: '2', code: '051', dongtitle: '부산 2동' },
        { dongcode: '3', code: '051', dongtitle: '부산 3동' },
        { dongcode: '1', code: '064', dongtitle: '제주 1동' },
        { dongcode: '2', code: '064', dongtitle: '제주 2동' },
      ],
      selectDongList: []
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    changecity(event) {
      console.log("이벤트받기",event.target.tagName);
      this.selectDongList = this.dongList.filter(dong => dong.code === this.selectedCity)
    }
  }
}
</script>
<style scoped>

</style>
