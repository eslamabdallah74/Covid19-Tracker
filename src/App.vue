<template>
  <Header/>
  <div class="container mx-auto">
    <Content />
  </div>
</template>

<script>
import Header from '@/components/Header'
import Content from '@/components/Content'



export default {
  name: 'App',

  components: {
    Header,
    Content
  },
}
</script>

<style>
 body{
   background: #f1f2f6;
 }
</style>
