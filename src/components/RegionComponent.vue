<template>
  <div class="region_container">
    <div v-for="city in region" :key="city.id" @click="changeCity(city.id)">
      <img :src="city.url" :alt="city.alt">
    </div>
  </div>
</template>

<script>
export default {
  name: "RegionComponent.vue",
  data() {
    return {
      region: [
        {id: 1, name:"Белогорск", url: "@/assets/img/man/belog.png", alt: "belog"},
        {id: 2, name:"Симферополь", url: "@/assets/img/man/simf.png", alt: "simf"},
        {id: 3, name:"Джанкой", url: "@/assets/img/man/djank.png", alt: "djank"},
        {id: 4, name:"Саки", url: "@/assets/img/man/saki.png", alt: "saki"},
        {id: 29, name:"Севастополь", url: "@/assets/img/man/sevas.png", alt: "sevas"},
        {id: 22, name:"Херсон", url: "@/assets/img/man/hers.png", alt: "hers"},
        {id: 23, name:"Кубань", url: "@/assets/img/man/kuban.pngg", alt: "kuban"}
      ],
      currentRegionId: 2
    }
  },
  methods: {
    changeCity(id) {
      this.currentCityId = id
    }
  }
}
</script>

<style scoped>

</style>