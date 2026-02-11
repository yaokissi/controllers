<script lang="ts">
    import frostedSugar from "../lib/assets/images/frosted-sugar.webp";
    import oreo from "../lib/assets/images/oreo.webp";
    import HeroSection from "../lib/components/heroSection.svelte";
    import { onMount } from "svelte";
    import { gsap } from "gsap";
    import { ScrollTrigger } from "gsap/dist/ScrollTrigger";

    onMount(() => {
        gsap.registerPlugin(ScrollTrigger);
        
        const cookie = document.getElementById("cookie");
        const chips = document.getElementById("chips");

        // Animation du cookie qui suit le scroll
        gsap.to(cookie, {
            y: 800, // distance vers le bas (ajustez selon vos besoins)
            x: -500, // distance vers la droite (valeur positive) ou gauche (valeur négative)
            rotation: 360, // rotation optionnelle
            scrollTrigger: {
                trigger: ".hero-section",
                start: "top top", // commence quand le haut de hero-section atteint le haut du viewport
                end: "bottom top", // termine quand le bas de hero-section atteint le haut du viewport
                scrub: 1, // l'animation suit le scroll (1 = 1 seconde de latence douce)
                markers: true // mettez true pour voir les marqueurs de debug
            }
        });

        // Animation des chips qui suit le scroll
        gsap.to(chips, {
            y: 500, // distance vers le bas (ajustez selon vos besoins)
            x: 650, // distance vers la droite (valeur positive) ou gauche (valeur négative)
            rotation: -360, // rotation optionnelle
            scrollTrigger: {
                trigger: ".hero-section",
                start: "top top", // commence quand le haut de hero-section atteint le haut du viewport
                end: "bottom top", // termine quand le bas de hero-section atteint le haut du viewport
                scrub: 1, // l'animation suit le scroll (1 = 1 seconde de latence douce)
                markers: true // mettez true pour voir les marqueurs de debug
            }
        });
    });
</script>

<HeroSection></HeroSection>
<section class="second-section">
    <div class="container">
        <div class="content-wrapper">
            <div class="img-section"></div>
            <div class="content-section">
                <h2>TASTE THE DIFFERENCE.</h2>
                <div class="sub-heading">
                    Real Eggs, Real Butter, Real Sugar.
                </div>
                <p>
                    Cookie Co. was founded in 2020 during the height of the
                    Covid-19 pandemic by Elise and Matt Thomas. Working behind
                    the scenes to open the first Cookie Co. location, Elise
                    baked her signature cookie recipes using real eggs, real
                    butter, and real cane sugar in her home, preparing hundreds
                    of boxes weekly by hand for driveway pick-up.
                </p>
            </div>
        </div>
    </div>
</section>

<section class="third-section">
    <div class="container">
        <div class="content-wrapper">
            <div class="product-card">
                <img src={frostedSugar} class="cooki-sm" id="cookism" alt="" />
                <h4>FROSTED SUGAR</h4>
                <a href="" class="cta-btn">Buy Now</a>
            </div>
            <div class="product-card">
                <h4>MONSTER</h4>
                <a href="" class="cta-btn">Buy Now</a>
            </div>
            <div class="product-card">
                <img src={oreo} class="cooki-sm" id="cookism" alt="" />
                <h4>OREO</h4>
                <a href="" class="cta-btn">Buy Now</a>
            </div>
        </div>
    </div>
</section>

<style lang="scss">
    @import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;900&display=swap");

    $brand-color: #552c10;
    $black: #000;
    $white: #fff;
    $main-font: "Montserrat", sans-serif;

    // global properties

    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    body {
        font-family: $main-font;
        font-weight: 500;
        // height: 100%;
        // overflow: hidden;
    }

    .container {
        width: 80vw;
        margin: auto;
        padding: 0 1vw;
    }

    ul {
        list-style-type: none;
    }

    a {
        text-decoration: none;
    }

    .cta-btn {
        border: 1px solid;
        padding: 0.8rem 1.8rem;
        border-radius: 2rem;
        color: $brand-color;
        &:hover {
            background-color: $brand-color;
            color: $white;
        }
    }

    // local properties

    .hero-section {
        height: 100vh;
        .container {
            height: 100%;
            nav {
                padding: 1.5vh 0;
                display: flex;
                justify-content: space-between;
                align-items: center;
                .logo {
                    a {
                        font-size: 2rem;
                        font-weight: 800;
                        color: $brand-color;
                    }
                }
                .menu {
                    ul {
                        display: flex;
                        li {
                            margin: 0 1vw;
                            a {
                                color: $black;
                                transform: 2s;
                                &:hover {
                                    color: $brand-color;
                                    font-weight: 600;
                                }
                            }
                        }
                    }
                }
            }
            .hero-content {
                display: flex;
                align-items: center;
                justify-content: center;
                height: calc(100% - 90px);
                position: relative;
                h1 {
                    font-size: 20.5vw;
                    color: $brand-color;
                }
                img {
                    position: absolute;
                    filter: drop-shadow(0 10px 5px #25252513);
                }
                .cookie {
                    width: 22vw;
                    transform: rotate(-60deg);
                    z-index: 1;
                    transition: all 0.1s;
                }
                .choco-chips {
                    z-index: 0;
                    width: 12vw;
                    top: 60%;
                    left: 35%;
                    transition: all 0.1s;
                }
                .peanut {
                    left: 90%;
                    top: 45%;
                    transform: translate(-40%, -90%);
                    width: 12vw;
                    z-index: -1;
                }
                .gem {
                    left: 4%;
                    top: 60%;
                    width: 3vw;
                }
            }
        }
    }

    .second-section {
        height: 100vh;
        background-color: #552c1033;
        .container {
            height: 100%;
            .content-wrapper {
                height: 100%;
                display: flex;
                justify-content: space-between;
                align-items: center;
                .img-section {
                    flex-basis: 50%;
                }
                .content-section {
                    flex-basis: 50%;
                    h2 {
                        font-size: 5vw;
                        line-height: 1;
                        color: $brand-color;
                    }
                    .sub-heading {
                        font-size: 1.5vw;
                        margin: 1vh 0 2vh;
                        color: $brand-color;
                    }
                    p {
                        line-height: 30px;
                    }
                }
            }
        }
    }

    .third-section {
        height: 100vh;
        background-color: $white;
        .container {
            height: 100%;
        }
        .content-wrapper {
            height: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .product-card {
            background-color: $brand-color;
            color: $white;
            text-align: center;
            flex-basis: 30%;
            height: 35vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: end;
            padding: 5vh 2vh;
            border-radius: 30px;
            position: relative;
            h4 {
                font-size: 2vw;
            }
            .cta-btn {
                color: $white;
                margin-top: 1.5rem;
                &:hover {
                    background-color: $white;
                    color: $brand-color;
                }
            }
            .cooki-sm {
                width: 13vw;
                position: absolute;
                top: -35%;
                filter: drop-shadow(0 10px 5px #25232213);
                transition: all 0.1s;
            }
        }
    }
</style>
