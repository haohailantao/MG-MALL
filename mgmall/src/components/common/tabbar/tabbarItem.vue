<template>
  <div class="tabbar-item" @click="itemClick">
   <div class="item-icon" v-if="!isActive"><slot name="icon"></slot></div>
   <div class="item-icon-active" v-else><slot name="icon-active"></slot></div>
   <div class="item-text" :style='activeStyle'><slot name="text"></slot> </div> 
  </div>
</template>

<script>
export default {
  name: 'tabbarItem',
  props: {
    path: String,
    color: {
      type: String,
      default: "red",
    }

  },
  
  computed: {
    isActive() {
      return (this.$route.path.indexOf(this.path) !=-1);
    },
    activeStyle(){
      return this.isActive? {color:this.color} :{};
    }
  },

  methods: {
    itemClick() {
      this.$router.replace(this.path);
    }
  }

}
</script>

<style>
.tabbar-item {
  /* flex布局 */
  flex: 1;

}

.item-icon img,
.item-icon-active img {
  width: 24px;
  height: 24px;
  margin-top: 5px;
  vertical-align: middle;
  
}

.item-text {
  margin-top: 3px;
  font-size: 12px;
  color: #333;
}
.item-text.active {
  color: red;
}

</style>