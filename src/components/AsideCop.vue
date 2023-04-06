<template>
  <div class="aside-container">
    <el-menu
      router
      default-active="1"
      class="el-menu-vertical-demo"
      @open="handleOpen"
      @close="handleClose"
      @select="active">
      
      <el-menu-item index="1" route="default">
        <i class="el-icon-menu"></i>
        <span slot="title">首页</span>
      </el-menu-item>
      <el-menu-item index="2" route="data">
        <i class="el-icon-document"></i>
        <span slot="title">管理</span>
      </el-menu-item>
      <el-menu-item index="3">
        <i class="el-icon-setting"></i>
        <span slot="title">导航三</span>
      </el-menu-item>
    </el-menu>
    <div class="aside-footer">@Copyright 2023</div>
  </div>
   

</template>
<script>


export default {
    name:'AsideCop',
   
  data(){
    return{
      pathurl:''
    }
   
  }
}


</script>
<style lang="scss" scoped> 
.aside-container{
  height: 100%;
  ul{
    height: 100%;
    height: calc( 100% - 60px );
    overflow-y: auto;
    padding-bottom: 60px;
    // box-sizing: border-box;
  }
}


.aside-footer{
  width: 260px;
  line-height: 60px;
  position: fixed;
  left: 0;
  bottom: 0;
  border-top: 1px solid #e6e6e6;
  text-align: center;
}




</style>