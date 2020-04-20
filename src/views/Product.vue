<template>
  <div class="product">
    <HeaderGadiel />
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
    <section class="product-shop spad page-details">
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
            <div class="row">
              <div class="col-lg-6">
                <div class="product-pic-zoom">
                  <img class="product-big-img" v-bind:src="default_product_picture" alt />
                </div>
                <div class="product-thumbs">
                  <carousel
                    class="product-thumbs-track ps-slider"
                    :loop="true"
                    :autoplay="true"
                    :nav="false"
                    :dots="false"
                    :margin="10"
                  >
                    <div
                      class="pt"
                      @click="changeImage(product_thumbs[0])"
                      :class="product_thumbs[0]==default_product_picture ? 'active' : '' "
                    >
                      <img src="img/mickey1.jpg" alt />
                    </div>

                    <div
                      class="pt"
                      @click="changeImage(product_thumbs[1])"
                      :class="product_thumbs[1]==default_product_picture ? 'active' : '' "
                    >
                      <img src="img/mickey2.jpg" alt />
                    </div>

                    <div
                      class="pt"
                      @click="changeImage(product_thumbs[2])"
                      :class="product_thumbs[2]==default_product_picture ? 'active' : '' "
                    >
                      <img src="img/mickey3.jpg" alt />
                    </div>

                    <div
                      class="pt"
                      @click="changeImage(product_thumbs[3])"
                      :class="product_thumbs[3]==default_product_picture ? 'active' : '' "
                    >
                      <img src="img/mickey4.jpg" alt />
                    </div>
                  </carousel>
                </div>
              </div>
              <div class="col-lg-6">
                <div class="product-details text-left">
                  <div class="pd-title">
                    <span>oranges</span>
                    <h3>Pure Pineapple</h3>
                  </div>
                  <div class="pd-desc">
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis, error officia. Rem aperiam laborum voluptatum vel, pariatur modi hic provident eum iure natus quos non a sequi, id accusantium! Autem.</p>
                    <p>
                      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quam possimus quisquam animi, commodi, nihil voluptate nostrum neque architecto illo officiis doloremque et corrupti cupiditate voluptatibus error illum. Commodi expedita animi nulla aspernatur.
                      Id asperiores blanditiis, omnis repudiandae iste inventore cum, quam sint molestiae accusamus voluptates ex tempora illum sit perspiciatis. Nostrum dolor tenetur amet, illo natus magni veniam quia sit nihil dolores.
                      Commodi ratione distinctio harum voluptatum velit facilis voluptas animi non laudantium, id dolorem atque perferendis enim ducimus? A exercitationem recusandae aliquam quod. Itaque inventore obcaecati, unde quam
                      impedit praesentium veritatis quis beatae ea atque perferendis voluptates velit architecto?
                    </p>
                    <h4>$495.00</h4>
                  </div>
                  <div class="quantity">
                    <router-link to="/shoppingcart" class="primary-btn pd-cart">Add To Cart</router-link>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Product Shop Section End -->
    <RelatedProductGadiel />
    <FooterGadiel />
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import HeaderGadiel from "@/components/HeaderGadiel.vue";
import FooterGadiel from "@/components/FooterGadiel.vue";
import RelatedProductGadiel from "@/components/RelatedProductGadiel.vue";
import carousel from "vue-owl-carousel";

export default {
  name: "Product",
  components: {
    HeaderGadiel,
    carousel,
    RelatedProductGadiel,
    FooterGadiel
  },
  data() {
    return {
      default_product_picture: "img/mickey1.jpg",
      product_thumbs: [
        "img/mickey1.jpg",
        "img/mickey2.jpg",
        "img/mickey3.jpg",
        "img/mickey4.jpg"
      ]
    };
  },
  methods: {
    changeImage(urlImage) {
      this.default_product_picture = urlImage;
    }
  }
};
</script>
