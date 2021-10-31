<template>
  <div>
    <Header></Header>
    <Main></Main>
    <Footer></Footer>
  </div>
</template>

<style>
  *{
    margin: 0;
    padding: 0;
  }
</style>

<script>
import Header from '@/components/header/header.vue'
import Main from '@/components/main/main.vue'
import Footer from '@/components/footer/footer.vue'

export default{

components:{
  Header,
  Main,
  Footer
}

}
</script>
