<template>
  <div class="home">
    <HeaderGadiel />
    <HeroCarousel />
    <BannerGadiel />
    <InstagramGadiel />
    <PartnerlogoGadiel />
    <FooterGadiel />
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import HeaderGadiel from "@/components/HeaderGadiel.vue";
import HeroCarousel from "@/components/HeroCarousel.vue";
import BannerGadiel from "@/components/BannerGadiel.vue";
import InstagramGadiel from "@/components/InstagramGadiel.vue";
import PartnerlogoGadiel from "@/components/PartnerlogoGadiel.vue";
import FooterGadiel from "@/components/FooterGadiel.vue";

export default {
  name: "Home",
  components: {
    HeaderGadiel,
    HeroCarousel,
    BannerGadiel,
    InstagramGadiel,
    PartnerlogoGadiel,
    FooterGadiel,
  },
};
</script>
