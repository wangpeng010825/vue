<template>
  <div class="container">
   <header></header>
   <div class="body">
    <aside>
      <aside-cop></aside-cop>
    </aside>
    <main>
      <router-view/>
    </main>
   </div>
  </div>
</template>
 <script>
 import AsideCop from '@/components/AsideCop.vue'
 export default{
  name:'MainView',
  components:{
    AsideCop
  }
 }


</script>

<style lang="scss" scoped>
html,body,.container{
  height: 100vh;
  width: 100%;
}
.body{
  display: flex;
  height: calc( 100% - 60px );
  
}
header{
  height: 60px;
  background-color: black;
  color: white;
}
aside{
  width: 260px;
  
  ul{
    height: 100%;
    overflow-y: auto;
  }
  
}
main{
  width: calc(100% - 260px);
  // background-color: blue;
  overflow-y: auto;
  height: calc( 100% - 60px );
}



  

</style>