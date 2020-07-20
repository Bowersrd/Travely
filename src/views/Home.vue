<template>
  <div id="home-wrapper">
    <AppHeader></AppHeader>
    <InfoSection
      title="Take The Worry Out of Life with"
      span="Insurance Protection"
      text="Quisque libero justo, iaculis at justo sed, eleifend dictum odio. Duis
        pharetra justo id justo rutrum, sed egestas urna sagittis. Nunc tempor
        posuere ultricies. Nullam aliquet fringilla pulvinar. Donec sit amet
        augue id tortor interdum facilisis vitae porta odio. Fusce congue porta
        tempus. Nulla nec interdum eros, vitae pretium ante. Curabitur accumsan
        velit purus."
      btnOne="Get Started"
      btnTwo="Find an agent"
    ></InfoSection>
  </div>
</template>

<script>
import AppHeader from "../components/AppHeader";
import InfoSection from "../components/InfoSection";

export default {
  name: "Home",
  components: {
    AppHeader,
    InfoSection,
  },
};
</script>

<style lang="scss" scoped>
#home-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
