<template>
  <div class="app">
    <header>Under construction</header>
    <man-component/>
    <div class="midle">
      <main class="main">
        <region-component/>
      </main>
      <aside class="aside">
        Татьяна,
        <a href="tel:+79787925315" class="phone">+7(978)792-53-15</a>
      </aside>
    </div>
    <footer>
      2022, eugen borisov, mcapple@yandex.ru
    </footer>
  </div>
</template>

<script>
import ManComponent from '@/components/ManComponent'
import RegionComponent from '@/components/RegionComponent'
export default {
  components: {
    ManComponent, RegionComponent
  }, created() {
  }
}
</script>

<style>
main {
  float: left;
  width: 80%;
}
aside {
  /*width: 19%;*/
}
</style>
