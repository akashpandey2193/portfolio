<template>
  <v-layout
    column>
    <header-comp/>
    <div class="profile-section">
      <v-flex
        sm4
        lg2>
        <div class="profile-image"/>
      </v-flex>
      <v-flex
        sm8
        lg10
        class="pa-4">
        <div class="display-3">AKASH PANDEY</div>
        <div class="general-info font-weight-light">
          <div class="title pb-2">
            <span class="label">Current Designation: </span>
            <span class="label-info">Software Developer at CatchThatBus</span>
          </div>
          <div class="title py-2">
            <span class="label">Location: </span>
            <span class="label-info">Hyderabad,Telangana</span>
          </div>
          <div class="title py-2">
            <span class="label">About Me:</span>
            <span
              class="label-info">
              An enthusiastic individual with leadership skills. Can easily adapt to change and possesses
              eagerness towards learning and contributing to the organization.
            </span>
          </div>
        </div>

      </v-flex>
    </div>
    <footer-comp/>
  </v-layout>
</template>

<script>
import FooterComp from '@/components/common/footer'
import HeaderComp from '@/components/common/header'
export default {
  components: {
    FooterComp,
    HeaderComp
  }
}
</script>

<style scoped lang="stylus">
.profile-section
  margin-top 60px
  height 50vh
  background white
  position relative
  display flex
.profile-image
  height 100%
  width 100%
  background url('/profile.jpg') no-repeat
  background-size contain
.general-info
  >>>.label
      font-style italic
  >>>.label-info
      font-weight 400
</style>
