<template>
  <div>
    <Header></Header>
    <HomeSwiper></HomeSwiper>
    <HomeIcon></HomeIcon>
  </div>
</template>
<script>
  import Header from './components/Header'
  import HomeSwiper from './components/Swiper'
  import HomeIcon from './components/Icons'

  export default {
    name: 'Home',
    data() {
      return {}
    },
    methods: {},
    computed: {},
    components: {
      Header,
      HomeSwiper,
      HomeIcon
    }
  }
</script>
<style scoped></style>


