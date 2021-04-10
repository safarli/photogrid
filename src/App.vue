
<template>
  <div class="header">
    <h1>WAVEVO</h1>
    <ul class="nav">
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Contact</a></li>
      <li><a href="#">Fun</a></li>
    </ul>
  </div>

  <div class="photogrid">
    <div v-for="i in col_count" :key="i">
      <p>Photo-{{ i }}</p>
    </div>
    <button v-on:click="loadMore()">Load More</button>
  </div>
</template>


<script>
export default {
  data: function () {
    return {
      col_count: 10,
    };
  },
  methods: {
    loadMore() {
      this.col_count += 10;
    },
  },
};
</script>

<style lang="scss">
@use '@/scss/main.scss';
</style>
