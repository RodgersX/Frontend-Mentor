<template>
  <div>
    <v-layout row no-gutters class="main-content hidden-sm-and-down">
      <div class="welcome-text">
        <div>
          <div class="remote-work mb-10">
            Make <br />
            remote work
          </div>
          <div class="grey--text mb-10">
            Get your team in sync, no matter your location. <br />
            Streamline processes, createteam rituals, and <br />
            watch productivity soar.
          </div>
          <div class="learn-more">
            <v-btn dark class="rounded-btn">Learn more</v-btn>
          </div>
        </div>

        <div class="d-flex justify-space-between partners">
          <img :src="require('../assets/images/client-databiz.svg')" />
          <img :src="require('../assets/images/client-audiophile.svg')" />
          <img :src="require('../assets/images/client-meet.svg')" />
          <img :src="require('../assets/images/client-maker.svg')" />
        </div>
      </div>
      <div class="hero-image">
        <img
          class="image"
          :src="require('../assets/images/image-hero-desktop.png')"
        />
      </div>
    </v-layout>
    <div class="hidden-md-and-up" style="width: 100%">
      <div class="text-center">
        <img
          width="100%"
          height="500px"
          :src="require('../assets/images/image-hero-desktop.png')"
        />
        <div class="px-3">
          <div class="my-8" style="font-weight: 600; font-size: 40px">
            Make remote work
          </div>
          <div class="grey--text mb-8">
            Get your team in sync, no matter your location. <br />
            Streamline processes, createteam rituals, and <br />
            watch productivity soar.
          </div>
          <div class="learn-more">
            <v-btn dark class="rounded-btn">Learn more</v-btn>
          </div>

          <div class="d-flex justify-space-between mt-8 mb-13">
            <img :src="require('../assets/images/client-databiz.svg')" />
            <img :src="require('../assets/images/client-audiophile.svg')" />
            <img :src="require('../assets/images/client-meet.svg')" />
            <img :src="require('../assets/images/client-maker.svg')" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="sass">
.main-content
  padding: 5rem 10rem
  display: flex
  justify-content: space-between

.welcome-text
  width: 40%
  position: relative

.remote-work
  font-weight: 700
  font-size: 80px

.hero-image
  width: 40%

.image
  width: 80%
  object-fit: contain

.rounded-btn
  border-radius: 10px
  padding: 4px 7px


.partners
  width: 80%
  position: absolute
  bottom: 0

  // position: relative
  // bottom: -30%
</style>
