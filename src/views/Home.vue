<template>
  <div class="home">

    <HeaderShayna />
    <CarouselShayna />
    <ProdukShayna />
    <Instagram />
    <Support />
    <Footer />
  </div>

</template>


<script>
// @ is an alias to /src
//import HelloWorld from '@/components/HelloWorld.vue'
import HeaderShayna from '@/components/HeaderShayna.vue'
import CarouselShayna from '@/components/CarouselShayna.vue'
import ProdukShayna from '@/components/ProdukShayna.vue'
import Instagram from '@/components/InstagramShayna.vue'
import Support from '@/components/SupportShayna.vue'
import Footer from '@/components/FooterShayna.vue'


export default {
  name: 'Home',
  components: {
    //HelloWorld
    HeaderShayna,
    CarouselShayna,
    ProdukShayna,
    Instagram,
    Support,
    Footer
  }
}
</script>
