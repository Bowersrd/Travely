<template>
  <nav class="nav">
    <img class="nav__logo" src="@/assets/images/logo.svg" alt="Company Logo" />
    <ul class="nav__list">
      <li class="nav__item">
        <a href="#" class="nav__link">Home</a>
      </li>
      <li class="nav__item">
        <a href="#" class="nav__link">About</a>
      </li>
      <li class="nav__item">
        <a href="#" class="nav__link">Page</a>
      </li>
      <li class="nav__item">
        <a href="#" class="nav__link">Insurance</a>
      </li>
      <li class="nav__item">
        <a href="#" class="nav__link">Blog</a>
      </li>
      <li class="nav__item">
        <a href="#" class="nav__link">Contact</a>
      </li>
      <li class="nav__item">
        <a href="#" class="nav__link">Book Now</a>
        <font-awesome-icon :icon="['fas', 'paper-plane']" />
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "NavBar",
};
</script>

<style lang="scss" scoped>
.nav {
  width: 100%;
  max-width: 1140px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: fixed;
  margin: 2% auto;
  left: 0;
  right: 0;
  &__logo {
    width: 16rem;
  }
  &__list {
    display: flex;
    align-items: center;
  }
  &__item {
    margin-right: 3rem;
    font-size: 1.8rem;
    font-weight: 500;
    color: #fff;
    &:last-child {
      padding: 1.8rem 2.5rem;
      border: 2px solid #fff;
      border-radius: 1rem;
    }
    & svg {
      margin-left: 1rem;
    }
  }
}
</style>
