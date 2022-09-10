<template>
  <div class="man_container">
    <div v-for="partman in mans" :key="partman.id" @click="changePartman(partman.id)">
<!-- https://codeguru.info/vue-js-i-dinamicheskij-src-dlya-kartinok/?ysclid=l7vn29x0qn287280233 -->
      <img :src="require(`../assets/img/man/${partman.file}`)" :alt="partman.alt">
    </div>
  </div>
</template>

<script type="text/javascript">
export default {
  name: 'ManComponent',
  data() {
    return {
      mans: [
        {id: 1, file: "moon.png", alt: "moon"},
        {id: 2, file: "cloud.png", alt: "cloud"},
        {id: 3, file: "cross.png", alt: "cross"},
        {id: 4, file: "book.png", alt: "book"}
      ],
      currentPartmanId: 2
    }
  },
  /*created: () => {
    this.currentPartmanIndex = 1
  },*/
  calculated: {
    manHeigh() {
      let result = 100;
      if (typeof window.innerWidth != 'undefined') {
        // viewPortWidth = window.innerWidth,
        // viewPortHeight = window.innerHeight
        result = window.innerWidth / 4 - 6;
      }
      return result
    }
  },
  methods: {
    changePartman(id) {
      this.currentPartmanId = id
    }
  }
}
</script>

<style scoped lang="scss">
$man-cnt: 4;
.man_container {
  display: flex;
}
.man_container div {
  //background: gray;
  margin-left: 3px;
  width: calc(25% - 6px);
  //height: 0;
  //padding-top: calc(25% - 6px);
  border-radius: 50%;
  //border: 6px solid darkblue;
}
.man_container div:first-child {
  //background: red;
}
.man_container div:last-child {
  //background: green;
  margin-right: 3px;
}
</style>
