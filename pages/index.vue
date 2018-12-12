<template>
  <div class="full-height full-width">
    <home-desktop
      v-if="$device.isDesktop || $device.isTablet"/>
    <home-mobile
      v-if="$device.isMobile"/>
  </div>
</template>

<script>
import HomeDesktop from '@/platform/desktop/Home.vue'
import HomeMobile from '@/platform/mobile/Home.vue'

export default {
  components: {
    HomeMobile,
    HomeDesktop,
  },
  data() {
    return {
      images: [
        { src: '/css.png', alt: 'css3' },
        { src: '/html5.png', alt: 'html5' },
        { src: '/react.png', alt: 'react' },
        { src: '/redux.png', alt: 'redux' },
        { src: '/vue.png', alt: 'vue' },
        { src: '/vuetify.png', alt: 'vuetify' },
      ]
    }
  },
}
</script>

<style scoped lang="stylus">
.profile-section
  box-sizing border-box
  margin-top 60px
  height 50vh
  background white
  position relative
  display flex
  border 1px solid grey
  font-family 'Nunito'
.profile-image
  height 100%
  width 100%
  background url('/profile.jpg') no-repeat
  background-size cover
.general-info
  >>>.label
      font-style italic
  >>>.label-info
      font-weight 400
</style>
