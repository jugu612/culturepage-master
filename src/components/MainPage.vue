<template>
  <div :class="['landing', scrollHandler ? 'mobile-menu-on' : '']">
    <main>
        <section class="first">
            <div>
                <ImageBg :backgroundImage="require('../images/team/hero_background.jpg')" section="Culture" />
            </div>
        </section>
      <section class="vision">
        <div class="vision-overlay">
          <img src="@/images/edits/circle.svg" class="circle-overlay" />
          <img src="@/images/edits/circleblur.svg" class="circleblur-overlay" />
          <img src="@/images/edits/squaredot.svg" class="squaredot-overlay" />
        </div>
        <div class="vision-content">
          <h2 class="vision-title">VISION</h2>
          <p class="vision-paragraph">
            Lorem ipsum dolor sit amet. Ab mollitia exercitationem
            quo velit beata et error molestias qui possimus
            suscipit id excepturi dignissimos. Lorem ipsum dolor sit amet. Ab mollitia exercitationem
            quo velit beata et error molestias qui possimus
            suscipit id excepturi dignissimos.
          </p>
        </div>
      </section>
      <section class="quote">
        <div class="quote-overlay">
          <img src="@/images/edits/circle.svg" class="circle2-overlay" />
          <img src="@/images/edits/blueblur.svg" class="blueblur-overlay" />
          <img src="@/images/edits/bluedots.svg" class="bluedots-overlay" />
          <img src="@/images/edits/bluedots.svg" class="bluedots2-overlay" />
        </div>
        <div class="quote-content">
          <p class="quote-phrase gray-word align-left">driven by <span class="blue-word"> innovation</span></p>
          <p class="quote-phrase gray-word align-center">fueled by <span class="blue-word"> collaboration</span></p>
          <p class="quote-phrase gray-word align-right">empowered by <span class="blue-word"> passion</span></p>
          <p class="quote-paragraph">
            at HQZen, we strive to create something meaningful and impactful
          </p>
        </div>
        <div class="image slide">
          <div class="slider-container">
            <div class="slider-wrapper" :style="{ transform: `translateX(-${currentSlideIndex * (100 / slidesToShow)}%)` }">
              <div v-for="(image, index) in sliderImages" :key="index" class="slide-item">
                <img :src="image" alt="Slider Image" class="slider-image" />
              </div>
            </div>
          </div>
        </div>
      </section>
      <section class="quote">
        <div class="quote-overlay">
            <img src="@/images/edits/roundrectangle.svg" class="rectangle-overlay" />
          <img src="@/images/edits/circle.svg" class="circle2-overlay" />
          <img src="@/images/edits/blueblur.svg" class="blueblur-overlay" />
          <img src="@/images/edits/bluedots.svg" class="bluedots-overlay" />
          <img src="@/images/edits/bluedots.svg" class="bluedots2-overlay" />
        </div>
        <div class="quote-content">
          <p class="quote-margin">
            Work-life balance <span class="gray-word"> and </span> <br> 
            employee well-being <span class="gray-word"> <br>  are paramount </span><br> 
            at <span class="blue-word">HQZEN</span>.
          </p>
        </div>
        <div class="full-image-wrapper" style="margin-top: 10rem;">
            <img src="@/images/edits/activities.svg" alt="activities" class="full-image" />
        </div>
      </section>
      <div>
                <ImageBg :backgroundImage="require('../images/team/work_background.svg')" section="Works" />
            </div>
        <section class="quote">
        <div class="quote-overlay">
          <img src="@/images/edits/circle.svg" class="circle2-overlay" />
          <img src="@/images/edits/blueblur.svg" class="blueblur-overlay" />
          <img src="@/images/edits/bluedots.svg" class="bluedots-overlay" />
          <img src="@/images/edits/bluedots.svg" class="bluedots2-overlay" />
        </div>
        <div class="full-image-wrapper" style="margin: 4vw;">
            <img src="@/images/edits/tech.svg" alt="activities" class="full-image" />
        </div>
        <div class="image slide" style="margin-top: 10vw; margin-bottom: 10vw;">
          <div class="slider-container">
            <div class="slider-wrapper" :style="{ transform: `translateX(-${currentSlideIndex * (100 / slidesToShow)}%)` }">
              <div v-for="(image, index) in sliderImages2" :key="index" class="slide-item">
                <img :src="image" alt="Slider Image" class="slider-image" />
              </div>
            </div>
          </div>
        </div>
      </section>
      <div>
                <ImageBg :backgroundImage="require('../images/team/people_background.jpg')" section="Teams" />
            </div>
        <section class="quote">
        <div class="quote-overlay">
          <img src="@/images/edits/circle.svg" class="circle2-overlay" />
          <img src="@/images/edits/blueblur.svg" class="blueblur-overlay" />
          <img src="@/images/edits/bluedots.svg" class="bluedots-overlay" />
          <img src="@/images/edits/bluedots.svg" class="bluedots2-overlay" />
        </div>
        <div class="people-image-container" style="margin-bottom: 8rem;">
      <button v-for="(image, index) in peopleImages" :key="index" class="people-image-button" @click="toggleImage(index)">
        <div class="people-image-wrapper">
            <img :src="image" alt="People Image" class="people-image" />
        </div>
        </button>

      <div class="people-image-wrapper">
        <button @click="toggleImage(1)">
          <img src="@/images/team/g-design.svg" alt="Image 1" class="people-image" />
        </button>
      </div>
      <div class="people-image-wrapper">
        <button @click="toggleImage(2)">
          <img src="@/images/team/g-developer.svg" alt="Image 2" class="people-image" />
        </button>
      </div>
      <div class="people-image-wrapper">
        <button @click="toggleImage(3)">
          <img src="@/images/team/g-qa.svg" alt="Image 3" class="people-image" />
        </button>
      </div>
      </div>
      <div v-if="showPicture" class="people-image-details">
      <img :src="selectedImage" alt="Selected Image" class="selected-image" />
    </div>
    <section class="vision">
        <div class="vision-overlay">
          <img src="@/images/edits/circle.svg" class="circle-overlay" />
          <img src="@/images/edits/circleblur.svg" class="circleblur-overlay" />
          <img src="@/images/edits/squaredot.svg" class="squaredot-overlay" />
        </div>
        <div class="vision-content">
          <h2 class="vision-title">JOIN US NOW!</h2>
          
        </div>
      </section>
    
    </section>
      
    </main>
  </div>
</template>

<script>
    import ImageBg from "./inside/ImageBg.vue"

    export default {
        name: 'MainPage',
        components: {
            ImageBg
        },
        data() {
            return {
            sliderImages: [
                require('../images/team/IMG_3821.jpg'),
                require('../images/team/IMG_4921.jpg'),
                require('../images/team/IMG_3825.jpg'),
            ],
            sliderImages2: [
                require('../images/works/1.svg'),
                require('../images/works/2.svg'),
                require('../images/works/3.svg'),
                require('../images/works/1.svg'),
            ],
            showPicture: false,
            peopleImage: [
                require('../images/team/p-des.svg'),
                require('../images/team/p-dev.svg'),
                require('../images/team/p-qa.svg'),
            ],
            currentImageIndex: 0,
            slidesToShow: 3, // Number of images to show at a time
            autoSlideInterval: 10 // Track the index of the currently displayed image
            }
            
        },
        methods: {
            startAutoSlide() {
            setInterval(() => {
                this.currentImageIndex = (this.currentImageIndex + 1) % this.sliderImages.length // Correct calculation
            }, this.autoSlideInterval)
            },
            toggleImage(imageIndex) {
            this.showPicture = !this.showPicture;
            if (this.showPicture) {
                this.selectedImage = this.peopleImage[imageIndex - 1]; // -1 because index is 0-based
            } else {
                this.selectedImage = '';
            }
            },
        },

        mounted() {
            this.startAutoSlide()
        }
        }
</script>

<style lang="scss" scoped>
    @import "../stylesheets/bpo-variables.scss";
    @import "../stylesheets/variables.scss";
    @import "../stylesheets/reset.scss";
    $landing-heading: #03183F;
    $l-blue: $accent;
    $accent-solid: #008FF5;
    $l-light-blue: #EEF7FE;
    .landing {
        &.mobile-menu-on {
            overflow: hidden;
            height: 100vh;
        }
    }
    button {
        background: none;
        border: none;
        outline: none;
        cursor: pointer;
        }


    .vision {
        position: relative;
        display: flex;
        align-items: center;
        justify-content: center;
        height: 50vh;
        background: linear-gradient(to bottom, #6aacfb, #6aacfb);
        background-size: 100% auto;
        overflow: hidden;
    }

    .vision-overlay {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        display: flex;
        justify-content: space-between;
        align-items: flex-start;
        pointer-events: none;
        z-index: 1; 
    }

    .circle-overlay,
    .circleblur-overlay,
    .squaredot-overlay {
        object-fit: contain;
        position: absolute; 
    }

    .circle-overlay {
        width: 30vw;
        height: 30vw;
        left: 8vw; 
        top: -10vw;
    }

    .circleblur-overlay {
        width: 20vw;
        height: 10vw;
        right: 5vw; 
        top: 5vw;
    }

    .squaredot-overlay {
        width: 25vw;
        height: 25vw;
        right: 6vw; 
        bottom: -10vw;
    }

    .vision-content {
        text-align: center;
        z-index: 1;
    }

    .vision-title {
    color: white;
    font-size: 3em;
    margin-bottom: 1vw;
    }

    .vision-paragraph {
    color: black;
    font-weight: 500;
    font-size: 1.5em;
    padding: 0rem 24vw;
    }

    .quote {
        background-color: $l-light-blue;
        font-weight: bold;
        padding-top: 12vw;
        position: relative;
        overflow: hidden;
    }

    .quote-overlay {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        display: flex;
        justify-content: space-between;
        align-items: flex-start;
        pointer-events: none;
        z-index: 0;
    }

    .blueblur-overlay,
    .circle2-overlay,
    .bluedots2-overlay,
    .bluedots-overlay{
        object-fit: contain;
        position: absolute; 
        z-index: -2;
    }

    .blueblur-overlay {
        width: 50vw;
        height: 50vw;
        right: 60vw; 
        top: 2vw;
    }

    .circle2-overlay {
        width: 30vw;
        height: 30vw;
        right: 0vw; 
        bottom: 35vw;
        z-index: -1;
    }

    .bluedots-overlay {
        width: 25vw;
        height: 25vw;
        right: 80vw; 
        top: 40vw;
    }

    .bluedots2-overlay {
        width: 20vw;
        height: 20vw;
        left: 80vw; 
        bottom: 52vw;
        transform: rotate(-90deg);
    }

    .rectangle-overlay{
        width: 70vw;
        height: 70vw;
        object-fit: contain;
        position: absolute;
        top: 27%;
        left: 50%;
        transform: translate(-50%, -50%);
    }

    .quote-content {
    text-align: center;
    padding: 4rem 0;
    z-index: 1;
    }

    .quote-phrase {
    margin: 0;
    position: relative;
    padding: 0.5vw 1vw;
    }

    .gray-word {
    color: gray;
    font-size: 2.5vw;
    }

    .blue-word {
    color: $l-blue;
    font-size: 2.5vw;
    }

    .quote-paragraph-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 0 4rem;
    width: 50%;
    max-width: 1200px;
    margin: 0 auto;
    z-index: 2;
    }

    .quote-paragraph {
        color: black;
        font-size: 2.5vw;
        text-align: center;
        margin-top: 2rem;
        padding: 2vw 24vw;
        display: inline-block;
        max-width: 100%;
    }
    .quote-margin {
        color: black;
        font-size: 2.5vw;
        text-align: center;
        margin-top: 2rem;
        padding: 2vw 30vw;
        display: inline-block;
        max-width: 100%;
    
    }

    .align-left {
    padding-right: 30vw;
    }

    .align-center {
    text-align: center;
    }

    .align-right {
    padding-left: 30vw;
    }

    .slider-container {
        margin-top: 12vw;
        overflow: hidden;
        position:relative
    }

    .slider-wrapper {
    display: flex;
    transition: transform 0.5s ease-in-out;
    width: 100%;
   
    }

    .slide-item {
    flex: 0 0 calc((100% - 1rem) / 3);
    margin: 0.5rem;
    z-index: 1;
    }

    .slider-image {
    width: 100%;
    height: 100%;
    object-fit: cover;
    }
    .full-image-wrapper {
        position: relative;
        text-align: center;
    }

    .full-image {
        max-width: 100%;
        max-height: 100%;
        object-fit: contain;
    }


    .people-image-container {
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 4vw 12vw;
        flex-wrap: wrap;
        margin: 0 auto; 
        z-index: 5;
        }



    .people-image-wrapper {
        flex: 1;
        margin: 1vw; 
    }

    .people-image {
        max-width: 100%;
        height: auto;
    }
    .people-image-details {
    display: flex;
    justify-content: center;
    margin-top: 2rem;
    }

    .selected-image {
    max-width: 100%;
    height: auto;
    z-index: 4;
    margin-bottom: 10rem;
    }

</style>
