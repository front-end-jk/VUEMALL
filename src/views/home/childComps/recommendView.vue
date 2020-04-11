<template>
  <div class="recommends">
    <div v-for="item in recommends" class="recommends-item">
      <a :href="item.link">
        <img :src="item.image" alt="">
        <div>{{item.title}}</div>
      </a>
    </div>
  </div>
</template>

<script>
  export default {
    name: "HomeRecommendView",
    props: {
      recommends: {
        type: Array,
        default() {
          return [];
        }
      }
    }
  }
</script>

<style scoped>
  .recommends {
    display: flex;
    width: 100%;
    font-size: 12px;

    padding: 10px 0 20px;
    border-bottom: 10px solid #eee;
  }
  .recommends-item {
    flex: 1;
    text-align: center;
  }
  .recommends-item img {
    margin-bottom: 10px;
    width: 70px;
    height: 70px;
  }
</style>
