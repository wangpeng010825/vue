<template>
  <div class="page">
    <div class="bg-video">
        <video src="//s3plus.meituan.net/zhaopin-official-website-prod/video/campusTV/zippedHomeVideo.mp4" autoplay loop ></video>
      </div>
  <div class="container">
      <div class="left">
        
      </div>
      <div class="right">
         <div class="right-bg">
          <el-form  :model="form" label-width="80px">
    <el-form-item label="用户名">
    <el-input v-model="form.name"></el-input>
  </el-form-item>
  <el-form-item label="密码">
    <el-input  placeholder="请输入密码" show-password v-model="form.password"></el-input>
  </el-form-item>
    </el-form>
    <div class="tooldiv1">
      <el-button  plain size="small" type="success" @click="login">登录</el-button>
    </div>
         </div>
    
  </div>
  
  
  </div>
  </div>
  

</template>

<script>


export default {
  name: 'HomeView',
 
  methods: {
    login(){
      if(this.form.name &&this.form.password){
        this.$notify({
          title: '成功',
          message: `${this.form.name}登录成功`,
          type: 'success'
        });
        this.$router.push(`main/${this.form.name}`)
      }
      else{
        this.$notify.error({
          title: '错误',
          message: '登录失败'
        });
      }
      
    

    }

    
  },
  data(){
    return{
      form:{
          name:'',
          password:''
        }
    }
  }
}
</script>

<style lang="scss" scoped >


.container{
  display: flex;
}
.left{
  width: 60%;
}
.right{
  padding-top: 250px;
  .right-bg{
    background-color: #fff;
    width: 400px;
    padding: 40px;
    border-radius: 10px;
    opacity: 0.8;


  }
}
.tooldiv1{
  display: flex;
  justify-content: center;
}
.bg-video{
  position: absolute;
  top:0;
  left: 0;
  z-index: -1;
  
  video{
    width: 100%;
  }


}
</style>

