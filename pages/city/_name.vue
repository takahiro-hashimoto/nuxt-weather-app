<template>
<div>
  <h1>{{item.name}}の天気</h1>
  <ul>
    <li>天気：{{item.weather[0].main}}</li>
    <li>温度：{{item.main.temp}}℃</li>
    <li>湿度：{{item.main.humidity}}％</li>
    <li>風速：{{item.wind.speed}}m</li>
  </ul>
  <nuxt-link to="/">トップに戻る</nuxt-link>
</div>
</template>

<script>
export default{
  async asyncData({route, app}) {
    const item = await app.$axios.$get(`https://api.openweathermap.org/data/2.5/weather?q=${route.params.name},jp&units=metric&appid=9c5838c2ce61b917f325ec05e5521ab9`)
    return {
      item
    }
  }
}
</script>

<style media="screen">
  .page-enter-active, .page-leave-active {
    transition: opacity .5s;
  }
  .page-enter, .page-leave-to {
    opacity: 0;
  }
</style>
