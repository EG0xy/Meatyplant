<template>
  <div id="search">
    <div class="SearchBox"><input type="text" placeholder="搜索" class="search"></div>
    <ul class="item layui-row">

         	<li class="filterItem layui-col-xs4" @click="toggleFilerMenue">
					<span>{{ filterMenueChecked }}</span>
					<i class="icon arrow" :class="{checked: filterMenueShow}"></i>
				</li>
     	<li class="filterItem layui-col-xs4" @click="toggleFilerMenue">
					<span>{{ classMenueChecked }}</span>
					<i class="icon arrow" :class="{checked: filterMenueShow}"></i>
				</li>

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

  name: 'Search',
  data(){
    return{
    filterMenueChecked: '综合排序',
    classMenueChecked:"全部",
    // 排序菜单
    filterMenue:['综合排序','价格升序','价格降序'],
    // 分类
    classMenue:['全部','百合科','菊科','番杏科','景天科'],
     // 筛选二级导航显示状态
        filterMenueShow: false
  }},
  methods:{
     toggleFilerMenue() {
            this.filterMenueShow = !this.filterMenueShow;
        },
  }
=======
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