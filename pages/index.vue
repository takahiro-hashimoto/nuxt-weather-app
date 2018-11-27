<template>
<div>
<h1>日本全国の天気</h1>
<ul>
  <li><nuxt-link :to="`/city/sapporo`">札幌</nuxt-link></li>
  <li><nuxt-link :to="`city/tokyo`">東京</nuxt-link></li>
  <li><nuxt-link :to="`city/nagoya`">名古屋</nuxt-link></li>
  <li><nuxt-link :to="`city/osaka`">大阪</nuxt-link></li>
  <li><nuxt-link :to="`city/fukuoka`">福岡</nuxt-link></li>
</ul>
</div>
</template>

<style media="screen">
  .page-enter-active, .page-leave-active {
    transition: opacity .5s;
  }
  .page-enter, .page-leave-to {
    opacity: 0;
  }
</style>
