<template>
    <div class="product">
    <HeaderShayna />
     <!-- Breadcrumb Section Begin -->
    <div class="breacrumb-section text-left">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="breadcrumb-text product-more">
                        <router-link to="/">
                        <i class="fa fa-home"></i> Home
                        </router-link>
                        <span>Detail</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- Breadcrumb Section Begin -->

    <!-- Product Shop Section Begin -->
    <section class="product-shop spad page-details text-justify">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="row">
                        <div class="col-lg-6">
                            <div class="product-pic-zoom">
                                <img class="product-big-img" :src="gambar_default" alt="">
                            </div>
                            <div class="product-thumbs">
                                <carousel :dots="false" :nav="false" class="product-thumbs-track ps-slider">
                                    <div class="pt" @click="changeImage(thumbs[0])" :class="thumbs[0] == gambar_default ? 'active' : '' ">
                                        <img src="img/Kerudung-cherry/ZPL4.B2.888500_-_CHERRY_SCARF_-_RED_-_69.000_2_800x.jpg" alt="" />
                                    </div>

                                    <div class="pt" @click="changeImage(thumbs[1])" :class="thumbs[1] == gambar_default ? 'active' : '' ">
                                        <img src="img/Kerudung-cherry/ZPL4.B2.888500_-_CHERRY_SCARF_-_PEACH_-_69.000_1_800x.jpg" alt="" />
                                    </div>

                                    <div class="pt" @click="changeImage(thumbs[2])" :class="thumbs[3] == gambar_default ? 'active' : '' ">
                                        <img src="img/Kerudung-cherry/ZPL4.B2.888500_-_CHERRY_SCARF_-_NAVY_-_69.000_1_3648x.jpg" alt="" />
                                    </div>
                                    
                                    <div class="pt" @click="changeImage(thumbs[3])" :class="thumbs[3] == gambar_default ? 'active' : '' ">
                                        <img src="img/Kerudung-cherry/ZPL4.B2.888500_-_CHERRY_SCARF_-_NAVY_-_69.000_1_3648x.jpg" alt="" />
                                    </div>
                                </carousel>
                            </div>
                        </div>
                        <div class="col-lg-6">
                            <div class="product-details">
                                <div class="pd-title">
                                    <span>oranges</span>
                                    <h3>Pure Pineapple</h3>
                                </div>
                                <div class="pd-desc">
                                    <p>
                                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis, error officia. Rem aperiam laborum voluptatum vel, pariatur modi hic provident eum iure natus quos non a sequi, id accusantium! Autem.
                                    </p>
                                    <p>
                                        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quam possimus quisquam animi, commodi, nihil voluptate nostrum neque architecto illo officiis doloremque et corrupti cupiditate voluptatibus error illum. Commodi expedita animi nulla aspernatur.
                                        Id asperiores blanditiis, omnis repudiandae iste inventore cum, quam sint molestiae accusamus voluptates ex tempora illum sit perspiciatis. Nostrum dolor tenetur amet, illo natus magni veniam quia sit nihil dolores.
                                        Commodi ratione distinctio harum voluptatum velit facilis voluptas animi non laudantium, id dolorem atque perferendis enim ducimus? A exercitationem recusandae aliquam quod. Itaque inventore obcaecati, unde quam
                                        impedit praesentium veritatis quis beatae ea atque perferendis voluptates velit architecto?
                                    </p>
                                    <h4>$495.00</h4>
                                </div>
                                <div class="quantity">
                                    <router-link to="/cart" class="primary-btn pd-cart">Add To Cart
                                    </router-link>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <!-- Product Shop Section End -->

    <Produkrelatif />
    <Footer />

    </div>
</template>

<script>
import HeaderShayna from '@/components/HeaderShayna.vue'
import Footer from '@/components/FooterShayna.vue'
import Produkrelatif from '@/components/produk-relatif.vue'
import carousel from 'vue-owl-carousel';

export default {
    name: "product",
    components:{
        HeaderShayna,
        Footer,
        Produkrelatif,
        carousel
    },

    data(){
        return {
            gambar_default: "img/Kerudung-cherry/ZPL4.B2.888500_-_CHERRY_SCARF_-_MAROON_-_69.000_2_3648x.jpg",
            thumbs: [
                "img/Kerudung-cherry/ZPL4.B2.888500_-_CHERRY_SCARF_-_MAROON_-_69.000_2_3648x.jpg",
                "img/Kerudung-cherry/ZPL4.B2.888500_-_CHERRY_SCARF_-_RED_-_69.000_2_800x.jpg",
                "img/Kerudung-cherry/ZPL4.B2.888500_-_CHERRY_SCARF_-_NAVY_-_69.000_1_3648x.jpg",
                "img/Kerudung-cherry/ZPL4.B2.888500_-_CHERRY_SCARF_-_NAVY_-_69.000_1_3648x.jpg"

            ]
        
        }
    },
    methods:{
        changeImage(urlImage){
            this.gambar_default = urlImage;
        }
    }

}

</script>

<style>
    .pt{
        margin: 5px;
    }
</style>