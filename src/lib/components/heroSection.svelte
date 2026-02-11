<script lang="ts">
    import cookie from "../assets/images/cookie.webp";
    import chocoChips from "../assets/images/choco-chips.png";
    import peanut from "../assets/images/peanut.png";
    import gem from "../assets/images/gem.png";
</script>


 <section class="hero-section">
  <div class="hero-content">
    <h1>Donuts</h1>
    <img src={cookie} alt="" class="cookie" id="cookie" />
    <img src={chocoChips} class="choco-chips" id="chips" alt="" />
    <img src={peanut} class="peanut" alt="" />
    <img src={gem} class="gem" alt="" />
  </div>
</section>

<style lang="scss">
.hero-section { height: 100vh; }

.hero-content {
  height: 100%;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
}

.hero-content h1 {
  font-size: 20.5vw;
  color: #552c10;
}

.hero-content img {
  position: absolute;
  filter: drop-shadow(0 10px 5px #25252513);
}

.hero-content .cookie {
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%) rotate(-60deg);
  width: 22vw;
  z-index: 1;
}

.hero-content .choco-chips {
  top: 60%;
  left: 35%;
  width: 12vw;
  z-index: 0;
}

.hero-content .peanut {
  left: 90%;
  top: 45%;
  transform: translate(-40%, -90%);
  width: 12vw;
  z-index: -1;
}

.hero-content .gem {
  left: 15%;
  top: 60%;
  width: 3vw;
}
</style>
