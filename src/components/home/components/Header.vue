<template>
    <div class="header">
      <div class="header-left">返回</div>
      <input class="header-input" type="text" placeholder="     输入城市/景点/游玩主题">
      <div class="header-right">城市</div>
    </div>
</template>
<script>
    export default {
      name:'Header',
        data() {
            return {}
        },
        methods: {},
        computed: {},
        components: {}
    }
</script>
<style scoped lang="less">
@import "~style/common.less";

.header{
  display: flex;
  height: .86rem;
  line-height: .86rem;
  background: @bg-color;
  color: #fff;

  .header-left{
    width: .64rem;
    flex: 1;
    text-align: center;
  }

  .header-input{
    flex: 9;
    height: .64rem;
    margin-top: .12rem;
    background: #FFF;
    border-radius:.1rem;
    border: none;
    font-size: .25rem;
  }

  .header-right{
    width:1.24rem;
    flex: 1;
    text-align: center;
  }


}
</style>
