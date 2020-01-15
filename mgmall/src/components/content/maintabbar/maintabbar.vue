<template>
  <div class="main-tabbar">
     <tabbar>  
        <tabbar-item path="/home" color="red">
          <img src="~assets/images/tabbar/home.svg" alt="" slot="icon">
          <img src="~assets/images/tabbar/home_active.svg" alt="" slot="icon-active">
          <p slot="text">首页</p>      
        </tabbar-item>         
        <tabbar-item path="/category" color="red">
          <img src="~assets/images/tabbar/category.svg" alt="" slot="icon">
          <img src="~assets/images/tabbar/category_active.svg" alt="" slot="icon-active">
          <p slot="text">分类</p>    
        </tabbar-item>
        <tabbar-item path="/cart"  color="red"> <img src="~assets/images/tabbar/cart.svg" alt="" slot="icon">
          <img src="~assets/images/tabbar/cart_active.svg" alt="" slot="icon-active">
          <p slot="text">购物车</p>    
        </tabbar-item>
        <tabbar-item path="/profile"  color="red">
           <img src="~assets/images/tabbar/profile.svg" alt="" slot="icon">
           <img src="~assets/images/tabbar/profile_active.svg" alt="" slot="icon-active">
           <p slot="text">我的</p>    
        </tabbar-item>
    </tabbar> 
  </div>
</template>

<script>
import tabbar from 'common/tabbar/tabbar';
import tabbarItem from 'common/tabbar/tabbarItem';

export default {
  components: {
    tabbar,
    tabbarItem,
  }

}
</script>

<style>

</style>