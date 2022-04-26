<template>
  <div>
    <div class="main-content hidden-sm-and-down">
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
            <button type="button" class="rounded-btn">Learn more</button>
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
          height="100%"
          :src="require('../assets/images/image-hero-desktop.png')"
        />
      </div>
    </div>
    <div class="hidden-md-and-up">
      <div class="text-center">
        <img
          width="100%"
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
            <button type="button" class="rounded-btn">Learn More</button>
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
  width: 70%
  margin: auto
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
  width: 100%
  object-fit: contain

.rounded-btn
  background-color: black
  color: white
  border-radius: 15px
  padding: 15px 30px

.rounded-btn:hover,
.rounded-btn:active
  color: black
  border: 1px solid black
  background-color: white
  border-radius: 10px


.partners
  width: 80%
  position: absolute
  bottom: 0
</style>
