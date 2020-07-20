<template>
  <div id="header">
    <div class="hero">
      <transition name="slide-fade" mode="out-in">
        <h1 class="hero__title" :key="titles[el]">{{ titles[el] }}</h1>
      </transition>
      <transition name="slide-fade" mode="out-in">
        <h2 class="hero__subtitle" :key="subtitles[el]">{{ subtitles[el] }}</h2>
      </transition>
      <transition name="slide-fade" mode="out-in">
        <p class="hero__text" :key="text[el]">{{ text[el] }}</p>
      </transition>
      <button class="hero__btn" @click="changeHero(0)">
        <font-awesome-icon :icon="['fas', 'angle-left']" size="2x" />
      </button>
      <button class="hero__btn" @click="changeHero(1)">
        <font-awesome-icon :icon="['fas', 'angle-right']" size="2x" />
      </button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      el: 0,
      titles: ["Wild life", "Travel", "Explore"],
      subtitles: [
        "Beautiful Sea Nature",
        "Across the World",
        "Hidden Gem Treasures",
      ],
      text: [
        "Set your sights on beautiful wild life as you make the trip across the open sea. Experience nature in its most beautiful form and see firsthand what beauty lies beneath the surface. Make your trip something you won't forget.",
        "With many locations to visit, you are never short on memories that will last forever. Travely offers a wide range of tourist destinations that are suited for you and your family. Traveling alone? No problem, we have something for you.",
        "With Travely, every trip is a hidden treasure just waiting to be discoverd. Embark on a wild adventure through the jungles or relax on the beach soaking in the sun. No matter what you are looking for, you will find something for the entire family. ",
      ],
      isManual: false,
    };
  },
  methods: {
    changeHero(value) {
      if (value === 0) {
        this.el === 0 ? (this.el = 2) : this.el--;
        this.isManual = true;
      } else {
        this.el === 2 ? (this.el = 0) : this.el++;
        this.isManual = true;
      }
    },
  },
  mounted() {
    setInterval(() => {
      this.changeHero(1);
    }, 7500);
  },
};
</script>

<style lang="scss" scoped>
#header {
  width: 100%;
  height: 100vh;
  background: linear-gradient(rgba(49, 132, 228, 0.5), rgba(0, 10, 74, 0.5)),
    url("../assets/images/background.jpg");
  background-size: cover;
  background-position: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.hero {
  width: 100%;
  max-width: 1120px;
  margin-top: 8.5rem;
  &__title {
    color: #ff7700;
    font-size: 24rem;
    font-weight: 800;
    margin-bottom: -2rem;
  }
  &__subtitle {
    color: #fff;
    font-size: 8rem;
    font-weight: 800;
    max-width: 59rem;
    margin-bottom: 2.2rem;
    line-height: 0.9;
  }
  &__text {
    color: #fff;
    font-size: 1.6rem;
    font-weight: 400;
    max-width: 59rem;
    margin-bottom: 2.5rem;
    line-height: 1.4;
  }
  &__btn {
    width: 4rem;
    height: 4rem;
    border: 2px solid #ff7700;
    border-radius: 50%;
    margin-right: 1.2rem;
    outline: none;
    -webkit-appearance: none;
    -moz-appearance: none;
    color: #fff;
  }
}

.slide-fade-enter-active {
  transition: all 0.4s ease;
}
.slide-fade-leave-active {
  transition: all 0.5s cubic-bezier(1, 0.5, 0.8, 1);
}
.slide-fade-enter,
.slide-fade-leave-to {
  transform: translateX(10px);
  opacity: 0;
}
</style>
