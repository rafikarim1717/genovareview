<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section class="container mx-auto mb-4">
    <nav class="flex ml-3 mt-5 mb-10 md:ml-10" aria-label="Breadcrumb">
      <ol class="inline-flex items-center space-x-1 md:space-x-3">
        <li class="inline-flex items-center">
          <a
            href="/"
            class="inline-flex items-center text-sm font-medium hover:text-yellow-600"
          >
            <svg
              class="w-4 h-4 mr-2"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M10.707 2.293a1 1 0 00-1.414 0l-7 7a1 1 0 001.414 1.414L4 10.414V17a1 1 0 001 1h2a1 1 0 001-1v-2a1 1 0 011-1h2a1 1 0 011 1v2a1 1 0 001 1h2a1 1 0 001-1v-6.586l.293.293a1 1 0 001.414-1.414l-7-7z"
              ></path>
            </svg>
            Home
          </a>
        </li>
        <li aria-current="page">
          <div class="flex items-center">
            <svg
              class="w-6 h-6 text-gray-400"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                fill-rule="evenodd"
                d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
                clip-rule="evenodd"
              ></path>
            </svg>
            <span
              class="ml-1 text-sm font-medium md:ml-2 pcolor hover:text-yellow-600"
              >Recype</span
            >
          </div>
        </li>
      </ol>
    </nav>
    <div class="mt-6 p-4 lg:p-6 lg:py-12 xl:p-12">
      <div class="flex flex-row">
        <h1 class="pcolor mb-2 text-lg md:text-xl lg:text-xxl">
          Standart Recipe
        </h1>
        <!-- <div class="rating space-y-6">
          <p class="slider1"></p>
          <p class="slider2"></p>
          <p class="slider3"></p>
        </div> -->
      </div>
      <hr class="h-1 rounded w-32 background-navbar border-0" />
      <div class="flex flex-col my-12 gap-8">
        <div
          class="flex flex-col border md:flex p-4 gap-12 items-center md:px-6"
        >
          <div class="max-w-lg my-2">
            <h3 class="text-xl md:text-xxl">Ice Shakes</h3>
          </div>
          <div
            class="flex flex-col my-2 md:mx-5 md:flex-row gap-2 lg:gap-12 items-center center"
          >
            <div class="flex flex-col items-center">
              <img src="../../assets/images/recipes/recipe-powder.png" />
              <div class="flex flex-col my-2 gap-1">
                <h2 class="text-lg lg:text-xl">Powder</h2>
                <p class="text-lg lg:text-xl text-gray-600">30gr</p>
              </div>
            </div>
            <img src="../../assets/images/icon/recipe_plus.png" class="my-2" />
            <div class="flex flex-col items-center">
              <img src="../../assets/images/recipes/recipe-hot-water.png" />
              <div class="flex flex-col my-2 gap-1">
                <h2 class="text-lg lg:text-xl">Hot Water</h2>
                <p class="text-lg lg:text-xl text-gray-600">30ml</p>
              </div>
            </div>
            <img src="../../assets/images/icon/recipe_plus.png" class="my-2" />
            <div class="flex flex-col items-center">
              <img src="../../assets/images/recipes/recipe-milk.png" />
              <div class="flex flex-col my-2 gap-1">
                <h2 class="text-lg lg:text-xl">Fresh Milk</h2>
                <p class="text-lg lg:text-xl text-gray-600">90ml</p>
              </div>
            </div>
            <img src="../../assets/images/icon/recipe_plus.png" class="my-2" />
            <div class="flex flex-col items-center">
              <img src="../../assets/images/recipes/recipe-ice-cube.png" />
              <div class="flex flex-col my-2 gap-1">
                <h2 class="text-lg lg:text-xl">Ice</h2>
                <p class="text-lg lg:text-xl text-gray-600">1 Glass</p>
              </div>
            </div>
            <img src="../../assets/images/icon/recipe_plus.png" class="my-2" />
            <div class="flex flex-col items-center">
              <img src="../../assets/images/recipes/recipe-shakes.png" />
              <div class="flex flex-col my-2 gap-1">
                <h2 class="text-lg lg:text-xl">Shakes</h2>
              </div>
            </div>
          </div>
        </div>
        <div
          class="flex flex-col border md:flex p-4 gap-12 items-center md:px-6"
        >
          <div class="max-w-lg my-2">
            <h3 class="text-xl md:text-xxl">Ice Blended</h3>
          </div>
          <div
            class="flex flex-col my-2 md:mx-5 md:flex-row gap-2 lg:gap-12 items-center center"
          >
            <div class="flex flex-col items-center">
              <img src="../../assets/images/recipes/recipe-powder.png" />
              <div class="flex flex-col my-2 gap-1">
                <h2 class="text-lg lg:text-xl">Powder</h2>
                <p class="text-lg lg:text-xl text-gray-600">30gr</p>
              </div>
            </div>
            <img src="../../assets/images/icon/recipe_plus.png" class="my-2" />
            <div class="flex flex-col items-center">
              <img src="../../assets/images/recipes/recipe-sugar.png" />
              <div class="flex flex-col my-2 gap-1">
                <h2 class="text-lg lg:text-xl">Sugar Flavoured</h2>
                <p class="text-lg lg:text-xl text-gray-600">15ml</p>
              </div>
            </div>
            <img src="../../assets/images/icon/recipe_plus.png" class="my-2" />
            <div class="flex flex-col items-center">
              <img src="../../assets/images/recipes/recipe-milk.png" />
              <div class="flex flex-col my-2 gap-1">
                <h2 class="text-lg lg:text-xl">Fresh Milk</h2>
                <p class="text-lg lg:text-xl text-gray-600">90ml</p>
              </div>
            </div>
            <img src="../../assets/images/icon/recipe_plus.png" class="my-2" />
            <div class="flex flex-col items-center">
              <img src="../../assets/images/recipes/recipe-ice-cube.png" />
              <div class="flex flex-col my-2 gap-1">
                <h2 class="text-lg lg:text-xl">Ice</h2>
                <p class="text-lg lg:text-xl text-gray-600">1 Glass</p>
              </div>
            </div>
            <img src="../../assets/images/icon/recipe_plus.png" class="my-2" />
            <div class="flex flex-col items-center">
              <img src="../../assets/images/recipes/recipe-blender.png" />
              <div class="flex flex-col my-2 gap-1">
                <h2 class="text-lg lg:text-xl">Blends All</h2>
              </div>
            </div>
          </div>
        </div>
        <div
          class="flex flex-col border md:flex p-4 gap-12 items-center md:px-6"
        >
          <div class="max-w-lg my-2">
            <h3 class="text-xl md:text-xxl">Mocktail</h3>
          </div>
          <div
            class="flex flex-col my-2 md:mx-5 md:flex-row gap-2 lg:gap-12 items-center center"
          >
            <div class="flex flex-col items-center">
              <img src="../../assets/images/recipes/recipe-fruit-blend.png" />
              <div class="flex flex-col my-2 gap-1">
                <h2 class="text-lg lg:text-xl">Fruit Blend</h2>
                <p class="text-lg lg:text-xl text-gray-600">40ml</p>
              </div>
            </div>
            <img src="../../assets/images/icon/recipe_plus.png" class="my-2" />
            <div class="flex flex-col items-center">
              <img src="../../assets/images/recipes/recipe-syrup.png" />
              <div class="flex flex-col my-2 gap-1">
                <h2 class="text-lg lg:text-xl">Syrup</h2>
                <p class="text-lg lg:text-xl text-gray-600">30ml</p>
              </div>
            </div>
            <img src="../../assets/images/icon/recipe_plus.png" class="my-2" />
            <div class="flex flex-col items-center">
              <img src="../../assets/images/recipes/recipe-soda.png" />
              <div class="flex flex-col my-2 gap-1">
                <h2 class="text-lg lg:text-xl">Soda</h2>
                <p class="text-lg lg:text-xl text-gray-600">+-90ml</p>
              </div>
            </div>
            <img src="../../assets/images/icon/recipe_plus.png" class="my-2" />
            <div class="flex flex-col items-center">
              <img src="../../assets/images/recipes/recipe-ice-cube.png" />
              <div class="flex flex-col my-2 gap-1">
                <h2 class="text-lg lg:text-xl">Ice</h2>
                <p class="text-lg lg:text-xl text-gray-600">1 Glass</p>
              </div>
            </div>
            <img src="../../assets/images/icon/recipe_plus.png" class="my-2" />
            <div class="flex flex-col items-center">
              <img src="../../assets/images/recipes/recipe-shakes.png" />
              <div class="flex flex-col my-2 gap-1">
                <h2 class="text-lg lg:text-xl">Shakes</h2>
              </div>
            </div>
          </div>
        </div>
        <div
          class="flex flex-col border md:flex p-4 gap-12 items-center md:px-6"
        >
          <div class="max-w-lg my-2">
            <h3 class="text-xl md:text-xxl">Fruit Smoothies</h3>
          </div>
          <div
            class="flex flex-col my-2 md:mx-5 md:flex-row gap-2 lg:gap-12 items-center center"
          >
            <div class="flex flex-col items-center">
              <img src="../../assets/images/recipes/recipe-fruit-blend.png" />
              <div class="flex flex-col my-2 gap-1">
                <h2 class="text-lg lg:text-xl">Fruit Blend</h2>
                <p class="text-lg lg:text-xl text-gray-600">40ml</p>
              </div>
            </div>
            <img src="../../assets/images/icon/recipe_plus.png" class="my-2" />
            <div class="flex flex-col items-center">
              <img src="../../assets/images/recipes/recipe-frape-base.png" />
              <div class="flex flex-col my-2 gap-1">
                <h2 class="text-lg lg:text-xl">Frape Base</h2>
                <p class="text-lg lg:text-xl text-gray-600">10gr</p>
              </div>
            </div>
            <img src="../../assets/images/icon/recipe_plus.png" class="my-2" />
            <div class="flex flex-col items-center">
              <img src="../../assets/images/recipes/recipe-water.png" />
              <div class="flex flex-col my-2 gap-1">
                <h2 class="text-lg lg:text-xl">Water</h2>
                <p class="text-lg lg:text-xl text-gray-600">90ml</p>
              </div>
            </div>
            <img src="../../assets/images/icon/recipe_plus.png" class="my-2" />
            <div class="flex flex-col items-center">
              <img src="../../assets/images/recipes/recipe-ice-cube.png" />
              <div class="flex flex-col my-2 gap-1">
                <h2 class="text-lg lg:text-xl">Ice</h2>
                <p class="text-lg lg:text-xl text-gray-600">1 Glass</p>
              </div>
            </div>
            <img src="../../assets/images/icon/recipe_plus.png" class="my-2" />
            <div class="flex flex-col items-center">
              <img src="../../assets/images/recipes/recipe-shakes.png" />
              <div class="flex flex-col my-2 gap-1">
                <h2 class="text-lg lg:text-xl">Shakes</h2>
              </div>
            </div>
          </div>
        </div>
        <div
          class="flex flex-col border md:flex p-4 gap-12 items-center md:px-6"
        >
          <div class="max-w-lg my-2">
            <h3 class="text-xl md:text-xxl">Special Tea</h3>
          </div>
          <div
            class="flex flex-col my-2 md:mx-5 md:flex-row gap-2 lg:gap-12 items-center center"
          >
            <div class="flex flex-col items-center">
              <img src="../../assets/images/recipes/recipe-syrup.png" />
              <div class="flex flex-col my-2 gap-1">
                <h2 class="text-lg lg:text-xl">Syrup</h2>
                <p class="text-lg lg:text-xl text-gray-600">30ml</p>
              </div>
            </div>
            <img src="../../assets/images/icon/recipe_plus.png" class="my-2" />
            <div class="flex flex-col items-center">
              <img src="../../assets/images/recipes/recipe-sugar.png" />
              <div class="flex flex-col my-2 gap-1">
                <h2 class="text-lg lg:text-xl">Sugar Flavoured</h2>
                <p class="text-lg lg:text-xl text-gray-600">10gr</p>
              </div>
            </div>
            <img src="../../assets/images/icon/recipe_plus.png" class="my-2" />
            <div class="flex flex-col items-center">
              <img src="../../assets/images/recipes/recipe-green-tea.png" />
              <div class="flex flex-col my-2 gap-1">
                <h2 class="text-lg lg:text-xl">Tea Water</h2>
                <p class="text-lg lg:text-xl text-gray-600">+-90ml</p>
              </div>
            </div>
            <img src="../../assets/images/icon/recipe_plus.png" class="my-2" />
            <div class="flex flex-col items-center">
              <img src="../../assets/images/recipes/recipe-ice-cube.png" />
              <div class="flex flex-col my-2 gap-1">
                <h2 class="text-lg lg:text-xl">Ice</h2>
                <p class="text-lg lg:text-xl text-gray-600">1 Glass</p>
              </div>
            </div>
            <img src="../../assets/images/icon/recipe_plus.png" class="my-2" />
            <div class="flex flex-col items-center">
              <img src="../../assets/images/recipes/recipe-shakes.png" />
              <div class="flex flex-col my-2 gap-1">
                <h2 class="text-lg lg:text-xl">Shakes</h2>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  data() {
    return {};
  },
};
</script>

<style scoped>
.border {
  border-style: solid 2px;
  border-color: #bdb76b;
}
h3 {
}
</style>
