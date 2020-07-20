<template>
  <div class="info-wrapper" :style="reverse ? 'flexDirection: row-reverse' : ''">
    <div class="info" :style="reverse ? 'textAlign: right' : ''">
      <h1 class="info__title">
        {{ title }}
        <span class="info__span">{{ span }}</span>
      </h1>
      <p class="info__text" :style="reverse ? 'paddingLeft: 5rem' : 'paddingRight: 5rem'">{{ text }}</p>
      <a href="#" class="info__btn" v-if="btnTwo"> {{ btnOne }} </a>
      <a href="#" class="info__btn info__btn--filled" v-if="btnTwo">{{ btnTwo }}</a>
    </div>
    <img src="../assets/images/travel_insurance.jpg" alt="Vacation Photo" />
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    span: String,
    text: String,
    btnOne: String,
    btnTwo: String,
    reverse: Boolean,
  },
};
</script>

<style lang="scss" scoped>
.info-wrapper {
  width: 100%;
  max-width: 1120px;
  display: flex;
  align-items: center;
  padding: 12rem 0;
}

.info {
  width: 60%;
  line-height: 1.5;
  &__title {
    font-size: 4.5rem;
    font-weight: 600;
    margin-bottom: 3rem;
  }
  &__text {
    font-size: 1.6rem;
    font-weight: 400;
    margin-bottom: 6rem;
  }
  &__btn {
    border: 1px solid #ff7700;
    padding: 1.8rem 4.3rem;
    font-size: 1.6rem;
    border-radius: 0.75rem;
    font-weight: 500;
    color: #ff7700;
    margin-right: 2rem;
    &--filled {
      color: #fff;
      background: #ff7700;
    }
  }
  &__span {
    color: #ff7700;
  }
}

img {
  height: 53.4rem;
  width: 47rem;
  border-radius: 0 20% 0 0;
}
</style>
