<template>
  <section class="">
    <div
      class="z relative w-full height-banner background flex items-center justify-center text-center bg-cover bg-center opacity-75"
    >
      <main class="px-4 sm:px-6 lg:px-8 z-10">
        <div class="text-center border-h2 p-2">
          <h2
            class="text-4xl tracking-tight leading-10 font-medium sm:text-5xl text-white sm:leading-none md:text-6xl"
          >
            Lorem Ipsum Tani Tanu Hore Hari
          </h2>
        </div>
      </main>
    </div>
  </section>
</template>
<script>
export default {
  components: {},
  data() {
    return {};
  },
};
</script>
<style scoped>
.background {
  background-image: url(../../assets/images/banner/recipe-page-banner.jpg);
}
.border-h2 {
  border: 2px solid #997f11;
  border-radius: 8px;
}
h2 {
  font-family: "Josefin Sans";
  font-style: normal;
  font-weight: 400;
  font-size: 43px;
  line-height: 160%;
  /* identical to box height, or 69px */

  /* Accents/Yellow/7 */

  color: #997f11;
}
</style>
