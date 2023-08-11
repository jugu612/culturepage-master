<template>
    <div :class="['landing', scrollHandler ? 'mobile-menu-on' : '']">
        <ExternalNav @toggle-mobile-menu="toggleScrollHandler" />
        <main>
            <!-- Hero section -->
            <section class="hero">
                <img
                    src="images/team/hero-background.jpg"
                    alt="Find Zen in your workforce"
                    class="hero__background"
                >
                <h1 class="hero__title">
                    Find Zen in your workforce
                </h1>
                <div class="hero__cta">
                    <p class="hero__cta--description t-regular">
                        Managed Productivity Engine: An entire ecosystem of tools for engaged custom solutions for the
                        individual or scaling teams.
                    </p>
                    <Button
                        class="hero__cta--button large primary rounded"
                        @click="getStarted"
                    >
                        Manage your team now
                    </Button>
                </div>
                <div class="hero__graphic">
                    <figure class="hero__graphic--lid">
                        <div class="screen">
                            <img
                                src="~images/landing/carousel/messages.png"
                                alt="HQzen Board"
                                class="hero-image"
                            >
                        </div>
                        <figcaption>MacBook Pro</figcaption>
                    </figure>
                    <span class="hero__graphic--chassis">
                        <span class="groove"></span>
                    </span>
                    <span class="hero__graphic--bottom">
                        <span class="curve"></span>
                    </span>
                    <span class="hero__graphic--shadow"></span>
                </div>
            </section>
            <!-- Goal section -->
            <section class="goal">
                <div class="goal__header">
                    <h1>
                        Our goal is to help you manage your team
                    </h1>
                    <p class="t-regular">
                        We are a team of managers, executives, and engineers committed to
                        developing a tool to help everyone boost team productivity with these attributes in mind:
                    </p>
                </div>
                <ul class="goal__attributes">
                    <li class="attribute">
                        <img
                            src="~images/landing/measure-productivity.png"
                            alt="Measures productivity"
                            class="attribute__image"
                        >
                        <div class="attribute__info">
                            <h2 class="attribute__title">
                                Measures productivity
                            </h2>
                            <p class="attribute__description t-regular">
                                Conveniently track and measure productivity of your workforce by utilizing our project
                                management tools.
                            </p>
                        </div>
                    </li>
                    <li class="attribute">
                        <img
                            src="~images/landing/generate-revenue.png"
                            alt="Generates Revenue"
                            class="attribute__image"
                        >
                        <div class="attribute__info">
                            <h2 class="attribute__title">
                                Generates Revenue
                            </h2>
                            <p class="attribute__description t-regular">
                                Leverage on our network of trusted partners' expertise to find a scaleable, beneficial
                                and repetitive business model that drives revenue growth.
                            </p>
                        </div>
                    </li>
                    <li class="attribute">
                        <img
                            src="~images/landing/free-to-use.png"
                            alt="Free to use"
                            class="attribute__image"
                        >
                        <div class="attribute__info">
                            <h2 class="attribute__title">
                                Free to use
                            </h2>
                            <p class="attribute__description t-regular">
                                We will help you build, grow, and manage your organization at zero charge.
                            </p>
                        </div>
                    </li>
                </ul>
            </section>
            <section class="feature">
                <img
                    src="~/images/landing/background-circle.svg"
                    class="bg-circle"
                />
                <div class="header">
                    <h1> Boost the level of productivity </h1>
                    <p> Level up the productivity in your workforce through HQZen's seemless features. </p>
                </div>
                <FeatureList />
            </section>
            <section class="downloads">
                <div class="header">
                    <h1> Track productivity in your workforce </h1>
                    <p>
                        We make it easy for you to track the productivity of your workforce using mobile and desktop
                        applications. With our proprietary time tracking technology, make sure that you know how your
                        employees spend their logged time.
                    </p>
                    <div class="header__actions">
                        <Button
                            class="rounded large l-primary"
                            @click="goToReleaseNote"
                        >
                            <p> Download Desktop app </p>
                        </Button>
                        <Button
                            class="rounded large l-primary"
                            @click="goToGooglePlay"
                        >
                            <p> Download Mobile app </p>
                        </Button>
                    </div>
                </div>
                <div class="content">
                    <img src="~/images/landing/downloads.png">
                </div>
            </section>
            <section class="next-step">
                <div class="header">
                    <h1> Let us help you with your next step! </h1>
                    <p> These may be the possible next steps for you. </p>
                </div>
                <div class="content-container">
                    <router-link :to="{name: 'get-started'}">
                        <div class="content">
                            <img src="~/images/landing/next-step-job-application.png" />
                            <div class="content__heading-container">
                                <div class="content__heading">
                                    <h2> Look for a job </h2>
                                    <p> Browse for job postings </p>
                                </div>
                                <Button
                                    class="iconic rounded l-primary"
                                    icon="arrow-right"
                                />
                            </div>
                        </div>
                    </router-link>
                    <a
                        href="https://scalema.com/"
                        target="__blank"
                    >
                        <div class="content">
                            <img src="~/images/landing/next-step-upscale.png" />
                            <div class="content__heading-container">
                                <div class="content__heading">
                                    <h2> Upscale my team </h2>
                                    <p> Grow your team using HQZen </p>
                                </div>
                                <Button
                                    class="iconic rounded l-primary"
                                    icon="arrow-right"
                                />
                            </div>
                        </div>
                    </a>
                </div>
            </section>
            <section class="get-started">
                <img
                    src="~/images/logo-white.svg"
                    alt="HQZen"
                    class="logo"
                />
                <img
                    src="~/images/landing/background-dots.svg"
                    class="bg bg-dots"
                />
                <img
                    src="~/images/landing/background-circle.svg"
                    class="bg bg-circle"
                />
                <div class="header">
                    <h1 class="white">
                        Start your journey now!
                    </h1>
                    <p class="white">
                        It is 100% free with guaranteed revenue.
                    </p>
                    <div class="header__actions">
                        <Button
                            class="semibold block large"
                            @click="getStarted"
                        >
                            Get Started
                        </Button>
                    </div>
                </div>
            </section>
            <section class="faq">
                <div class="header">
                    <h1> Got any questions? </h1>
                    <p> Perhaps these are some of your queries. </p>
                </div>
                <FAQSection class="content" />
            </section>
        </main>
        <Footer />
    </div>
</template>

<script>
    import Footer from 'source/components/landing/Footer.vue';
    import ExternalNav from 'source/components/landing/ExternalNav.vue';
    import Button from 'source/components/_generics/Button.vue';
    import FAQSection from 'source/components/landing/FAQSection.vue';
    import FeatureList from 'source/components/landing/FeatureList.vue';

    const releaseNotesUrl = 'https://hqzen.com/release-notes';
    const googlePlayUrl = 'https://play.google.com/store/apps/details?id=com.bposeats.applybpo';

    export default {
        name: 'LandingPageNew',

        components: {
            Button,
            Footer,
            ExternalNav,
            FAQSection,
            FeatureList,
        },

        data() {
            return {
                scrollHandler: false
            };
        },

        methods: {
            goToReleaseNote() {
                window.location.href = releaseNotesUrl;
            },

            goToGooglePlay() {
                window.location.href = googlePlayUrl;
            },

            getStarted() {
                this.$router.push({
                    name: 'get-started'
                }).catch(() => {console.error('Failed to redirect');});
            },

            toggleScrollHandler(isOpened) {
                this.scrollHandler = isOpened? !this.scrollHandler : false;
            }
        }
    };
</script>

<style lang="scss" scoped>
    @import "source/stylesheets/sass/abstract/bpo-variables.scss";

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

    .hero {
        @include flex-align-justify-center(column);
        gap: 24px;
        margin-top: 72px;
        text-align: center;

        @media #{$tablet} {
            padding: 80px 16px;
        }

        &__background {
            width: 100%;
            position: absolute;
            inset: 0;
            z-index: -1;
            user-select: none;
        }

        &__title {
            font-weight: 800;
            font-size: $sp-36;
            color: $landing-primary;

            @media #{$tablet} {
                font-size: 24px;
            }
        }

        &__cta {
            @include flex-align-justify-center(column);
            gap: $sp-24;

            &--description {
                max-width: 622px;
                font-weight: 500;
                font-size: $sp-20;
                color: $landing-primary;

                @media #{$tablet} {
                    font-size: $sp-16;
                }
            }

            &--button {
                background-color: $accent-solid !important;
                font-weight: 700;

                &:hover {
                    background-color: darken($accent-solid, 5%) !important;
                }
            }
        }

        &__graphic {
            @include flex-align-center(column);
            width: calc(100vw * 0.55);
            height: calc(100vw * 0.33);
            margin-top: 20px;

            @media #{$desktop-small} {
                width: calc(100vw * 0.95);
                height: calc(100vw * 0.56);
            }

            &--lid {
                @include flex-align-justify-center;
                width: 80%;
                height: 85%;
                background: #1A202C;
                border: 2px solid #4A5568;
                border-radius: 1.5vw 1.5vw 0 0;
                transform: translateY(2px);
                position: relative;
                margin-block-start: 0;
                margin-block-end: 0;
                margin-inline-start: 0;
                margin-inline-end: 0;

                @media #{$tablet} {
                    border-radius: 2.7vw 2.7vw 0 0;
                }

                .screen {
                    width: 95%;
                    height: 92%;
                    overflow: hidden;
                    background-color: $light-container;

                    img {
                        width: 100%;
                        height: auto;
                        user-select: none;
                    }
                }

                figcaption {
                    color: rgba($white, .5);
                    font-size: 0.5vw;
                    position: absolute;
                    bottom: 1%;
                    user-select: none;

                    @media #{$desktop-small} {
                        font-size: 0.7vw;
                    }
                }
            }

            &--chassis {
                position: relative;
                width: 100%;
                height: 3%;
                background: linear-gradient(90deg, #0D1012 0%, #CAD4DB 3%, #242729 6%, #A3ACB1 13%, #A3ACB1 86%,
                    #242729 94%, #CAD4DB 97%, #0D1012 99%), #A3ACB1;
                border-radius: 0.12rem 0.12rem 0 0;

                .groove {
                    position: absolute;
                    width: 16%;
                    height: 77%;
                    left: 50%;
                    transform: translateX(-50%);
                    top: 0;
                    border-radius: 0 0 2rem 2rem;
                    background: linear-gradient(90deg, #3C3C3C 10%, transparent 36%, transparent 64%, #444444 92%),
                    #96A1A8;
                }
            }

            &--bottom {
                width: 100%;
                height: 2%;
                overflow: hidden;
                position: relative;

                .curve {
                    position: absolute;
                    inset: 0;
                    transform: translateY(-50%);
                    height: 200%;
                    border-radius: 0 0 50% 50%;
                    background: linear-gradient(180deg, #7A7F83 50%, #0B0B0E 100%), #647279;
                }
            }

            &--shadow {
                width: 90%;
                height: 2%;
                background: $black;
                filter: blur($sp-24);
            }
        }
    }

    .goal {
        @include flex-align-justify-center(column);
        background-color: $accent-solid;
        justify-content: center;

        @media #{$desktop-small} {
            padding: $sp-80 $sp-40;
        }

        @media #{$tablet} {
            padding: $sp-80 $sp-16;
        }

        &__header {
            @include flex-align-justify-center(column);
            gap: $sp-20;
            text-align: center;
            color: $white;
            max-width: 622px;

            h1 {
                font-weight: 600;
                font-size: $sp-32;
                letter-spacing: -0.014em;
            }

            p {
                font-weight: 400;
                font-size: $sp-16;
                color: $white;
            }
        }

        &__attributes {
            @include clear-list-formatting;
            display: flex;
            flex-wrap: wrap;
            align-items: flex-start;
            justify-content: center;
            column-gap: $sp-24;
            row-gap: $sp-40;

            @media #{$mobile} {
                flex-direction: column;
            }

            .attribute {
                @include flex-align-justify-center(column);
                text-align: center;
                color: $white;

                @media #{$mobile} {
                    flex-direction: row;
                    gap: $sp-20;
                }

                &__info {
                    max-width: 342px;

                    @media #{$desktop-small} {
                        max-width: 200px;
                    }

                    @media #{$mobile} {
                        max-width: unset;
                        text-align: left;
                    }
                }

                &__image {
                    width: 300px;
                    height: 400px;
                    border-radius: 2px;

                    @media #{$desktop-small} {
                        width: 150px;
                        height: 200px;
                    }
                }

                &__title {
                    font-weight: 600;
                    font-size: $sp-24;
                    margin-top: $sp-24;
                }

                &__description {
                    font-weight: 400;
                    font-size: $sp-16;
                    margin-top: $sp-12;
                    color: $white;
                }
            }
        }
    }

    .next-step {
        background: $l-light-blue;

        .content {
            display: flex;
            width: fit-content;
            gap: 24px;
            padding: 16px 12px;
            border-radius: 8px;

            &-container {
                display: flex;
                gap: 100px;
                padding: 24px 0;

                @media #{$desktop-small} {
                    gap: 32px;
                }

                @media #{$tablet} {
                    flex-direction: column;
                    gap: 68px;
                }

                a {
                    text-decoration: none;
                }
            }

            &__heading {
                display: flex;
                flex-direction: column;
                gap: 4px;

                &-container {
                    display: flex;
                    justify-content: space-between;
                    width: 100%;

                    h2 {
                        font-weight: 600;
                        font-size: 24px;
                        color: $l-blue;
                    }

                    p {
                        font-size: 14px;
                        color: $primary;
                    }
                }
            }

            &:hover {
                background: darken($l-light-blue, 2.5%);
                cursor: pointer;
            }

            img {
                width: inherit;

                @media #{$desktop-medium} {
                    width: 100%;
                }
            }
        }

        @media #{$desktop-medium} {
            padding: 80px 80px;
        }

        @media #{$desktop-small} {
            padding: 80px 40px;
        }
    }

    .downloads {
        .header {
            max-width: 1112px;

            &__actions {
                @media #{$mobile} {
                    display: flex;
                    flex-direction: column;
                }
            }
        }

        .content {
            width: 100%;

            img {
                @media #{$desktop-small} {
                    width: 100%;
                }
            }
        }
    }


    .get-started {
        @include flex-align-center(column);
        position: relative;
        overflow: hidden;
        gap: 4px;
        padding: 240px;
        background: $l-blue;

        .logo {
            height: 56px;
        }

        .bg {
            position: absolute;
            mix-blend-mode: soft-light;

            &-dots {
                top: 20%;
                left: 10%;

                @media #{$tablet} {
                    left: -28%;
                }

                @media #{$mobile} {
                    left: -44%;
                }
            }

            &-circle {
                right: -15%;
                top: 44%;

                @media #{$tablet} {
                    right: -72%;
                }

                @media #{$mobile} {
                    right: -112%;
                }
            }
        }

        .header {
            h1 {
                @media #{$mobile} {
                    font-size: 24px;
                }
            }

            p {
                @media #{$mobile} {
                    font-size: 16px;
                }
            }
        }

        @media #{$desktop-small} {
            padding: 240px 40px;
        }
    }

    .feature {
        position: relative;
        background: $l-light-blue;

        @media screen and (max-width: 980px) {
            gap: 20px;
            padding: 80px 52px;
        }

        .bg-circle {
            position: absolute;
            mix-blend-mode: multiply;
            left: -1%;

            @media #{$desktop-medium} {
                left: -35%;
            }

            @media #{$tablet} {
                left: -64%;
            }
        }
    }

    section {
        @include flex-align-center(column);
        gap: 52px;
        padding: 80px 140px;

        .header {
            @include flex-align-center(column);
            gap: 20px;
            text-align: center;

            .white {
                color: $white;
            }

            h1 {
                font-weight: 600;
                font-size: 32px;
                color: $landing-heading;
            }

            &__actions {
                display: flex;
                gap: 12px;
            }
        }

        .content {
            @include flex-align-center(column);
            gap: 20px;
            width: fit-content;
        }

        .content {
            @include flex-align-center(column);
            gap: 20px;
            width: fit-content;
        }

        p {
            font-size: 20px;
            line-height: 150%;
            color: $secondary;
        }

        @media #{$tablet} {
            gap: 40px;
            padding: 80px 30px;
        }
    }

    ::v-deep button.l-primary {
        background: $accent-solid;
        color: $white;
        border: none;

        &:hover {
            background: darken($accent-solid, 7.5%);
        }

        p {
            font-size: 16px;
            color: $white;
            font-weight: 700;
            width: 100%;
        }
    }

    input {
        height: 50px;
        width: 370px;
        padding: 0px 12px;
        outline: none;
        font-size: 14px;
        color: $primary;
        border-radius: 4px;
        border: 1px solid $quaternary;
        transition-duration: .2s;

        &:hover {
            border-color: $gray;
        }

        &:focus {
            border-color: $accent;
            box-shadow: 0 0 0 4px rgba($white, .25);
        }
    }
</style>
