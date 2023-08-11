<template>
  <div class="hero">
    <div class="hero__background">
      <img
        :src="backgroundImage"
        alt="HQZEN"
        class="hero__background-image"
      >
    </div>

    <div class="background_blur"></div>

    <div class="hero__content">
      <img
        src="../../images/edits/HQZENlogo.png"
        alt="HQZEN"
        class="hero_image"
      >
      <p class="hero__title">{{ section }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ImageBg',
  props: {
    backgroundImage: String,
    section: String,
  },
};
</script>

<style lang="scss" scoped>
@import "../../stylesheets/bpo-variables.scss";
@import "../../stylesheets/variables.scss";
@import "../../stylesheets/reset.scss";
$landing-heading: #03183F;
$l-blue: $accent;
$accent-solid: #008FF5;
$l-light-blue: #EEF7FE;
.hero {
  position: relative;
  width: 100%;
  height: 100vh;
  overflow: hidden;

  &__background {
    width: 100%;
    height: 100%;
    position: absolute;
    inset: 0;
    z-index: -1;
    user-select: none;
    overflow: hidden; /* Hide any potential overflow */
    display: flex;
    justify-content: center;
    align-items: center;

    &-image {
      width: 100%; /* Ensure the image takes up the full width */
      height: 100%; /* Ensure the image takes up the full height */
      object-fit: cover; /* Fill the container without whitespace */
    }
  }

  .background_blur {
    position: absolute;
    width: 100%;
    height: 100%;
    background: url("../../images/edits/backgroundblur.png");
    background-size: cover;
    z-index: -1;
  }

  &__content {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    display: flex;
    align-items: center;
    z-index: 1;
    color: white;
    font-size: 14vw; /* Responsive font size based on viewport width */

    .hero_image {
      max-width: 70%;
      height: auto;
    }

    .hero__title {
      font-size: 5vw; /* Responsive font size based on viewport width */
      font-weight: bold; 
      margin-left: 4px;
    }
  }
}
</style>
