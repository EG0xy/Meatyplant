<template>
  <div id="search">
    <div class="SearchBox"><input type="text" placeholder="搜索" class="search"></div>
    <ul class="item layui-row">
      <li class="layui-col-xs4">综合
        <ul class="list">
          <li>综合</li>
          <li>价格升序</li>
          <li>价格降序</li>
        </ul>
      </li>
      <li class="layui-col-xs4">分类
        <ul>
          <li>全部</li>
          <li>百合科</li>
          <li>菊科</li>
          <li>番杏科</li>
          <li>景天科</li>
        </ul>
      </li>
       <li class="layui-col-xs4">销量</li>
    </ul>
  </div>
</template>

<script>
 import "layui-css";
export default {
  name: 'Search'
}
</script>

<style lang="scss">

  .search{
  width:300px;
  height: 40px;
  border: 0px;
  border-bottom: 1px solid  #ccc;
  }
  .item>li{
    float: left;
  }
</style>