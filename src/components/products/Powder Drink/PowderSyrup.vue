<template>
  <section class="container mx-auto">
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
        <li class="inline-flex items-center">
          <a
            href="/products"
            class="inline-flex items-center text-sm font-medium hover:text-yellow-600"
          >
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
            Products
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
              >Powder Drink</span
            >
          </div>
        </li>
      </ol>
    </nav>
    <div class="p-4 lg:p-6 lg:py-12 xl:p-12">
      <div
        class="flex flex-col gap-y-12 md:flex md:flex-row md:justify-between md:gap-x-2"
      >
        <div class="p-2">
          <h1 class="pcolor mb-1 text-lg md:text-xl lg:text-2xl">
            Powder Drink
          </h1>
          <hr class="h-1 rounded w-28 background-navbar border-0" />
        </div>
      </div>

      <div class="py-10 px-12">
        <div
          class="grid grid-flow-row gap-12 text-neutral-600 sm:grid-cols-2 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4"
        >
          <div
            v-for="product in resultQuery"
            :key="product.id"
            class="my-8 bg-white center"
          >
            <router-link
              :to="{
                name: 'productDetailPage',
                query: {
                  dataProduk: JSON.stringify({
                    name: product.name,
                    price: product.price,
                    category: product.category,
                    info: product.info,
                    packaging: product.packaging,
                    weight: product.weight,
                    color: product.color,
                    image: product.image,
                    link: product.link,
                    serving: product.serving,
                    tasting: product.tasting,
                    penyimpanan: product.penyimpanan,
                  }),
                },
              }"
            >
              <div class="cursor-pointer">
                <figure>
                  <!-- Image -->
                  <img
                    :src="product.image + '?auto=format&fit=crop&w=400&q=50'"
                    :alt="product.name"
                    class="rounded-t h-64 w-full object-contain"
                  />

                  <figcaption class="p-4 mt-2">
                    <!-- Title -->
                    <h2
                      class="mb-2 text-lg lg:text-xl tracking-tight text-black"
                    >
                      {{ product.name }}
                    </h2>

                    <p class="text-xl text-gray-600">RP. {{ product.price }}</p>
                  </figcaption>
                </figure>
              </div>
            </router-link>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  components: {},
  data: () => {
    return {
      products: [
        {
          id: 1,
          name: "Powder Avocado",
          image: "../powder_avocado.jpg",
          price: "150,000",
          categoryId: "powder",
          info: "Cocok Digunakan untuk :\n- Untuk Meng-explore Minuman Terkini\n- Pembuatan Kue\n- Pembuatan Minuman\n- Aneka Olahan Lainnya",
          link: "https://www.tokopedia.com/genovaindonesia/genova-avocado-frappe-powder-1000-gram?extParam=whid%3D8872969",
          packaging: "1 Pack Powder",
          weight: "1000 Gram",
          serving:
            "- Masukkan 20-30 Gram Powder\n- Dicampur 120-150ML Susu\n- Aduk/shake hingga tercampur rata dan sajikan",
          color: "",
          tasting: "",
          penyimpanan:
            "- Simpan Produk ditempat yang sejuk dan terhindar dari Sinar Matahari langsung\n- Hindari dari tempat yang berbau tajam.",
        },
        {
          id: 2,
          name: "Powder Cappuccino",
          image: "../powder_cappuccino.jpg",
          price: "139,000",
          categoryId: "powder",
          info: "Cocok Digunakan untuk :\n- Untuk Meng-explore Minuman Terkini\n- Pembuatan Kue\n- Pembuatan Minuman\n- Aneka Olahan Lainnya",
          link: "https://www.tokopedia.com/genovaindonesia/genova-cappuccino-frappe-powder-1000-gram?extParam=whid%3D8872969",
          packaging: "1 Pack Powder",
          weight: "1000 Gram",
          serving:
            "- Masukkan 20-30 Gram Powder\n- Dicampur 120-150ML Susu\n- Aduk/shake hingga tercampur rata dan sajikan",
          color: "",
          tasting: "",
          penyimpanan:
            "- Simpan Produk ditempat yang sejuk dan terhindar dari Sinar Matahari langsung\n- Hindari dari tempat yang berbau tajam.",
        },
        {
          id: 3,
          name: "Powder Charcoal",
          image: "../powder_charcoal.jpg",
          price: "159,000",
          categoryId: "powder",
          info: "Cocok Digunakan untuk :\n- Untuk Meng-explore Minuman Terkini\n- Pembuatan Kue\n- Pembuatan Minuman\n- Aneka Olahan Lainnya",
          link: "https://www.tokopedia.com/genovaindonesia/genova-charcoal-frappe-powder-1000-gram?extParam=whid%3D8872969",
          packaging: "1 Pack Powder",
          weight: "1000 Gram",
          serving:
            "-Masukkan 20-30 Gram Powder\n-Dicampur 120-150ML Susu\n-Aduk/shake hingga tercampur rata dan sajikan",
          color: "",
          tasting: "",
          penyimpanan:
            "- Simpan Produk ditempat yang sejuk dan terhindar dari Sinar Matahari langsung\n- Hindari dari tempat yang berbau tajam.",
        },
        {
          id: 4,
          name: "Powder Chocolate",
          image: "../powder_chocolateclassic.jpg",
          price: "139,000",
          categoryId: "powder",
          info: "Cocok Digunakan untuk :\n- Untuk Meng-explore Minuman Terkini\n- Pembuatan Kue\n- Pembuatan Minuman\n- Aneka Olahan Lainnya",
          link: "https://www.tokopedia.com/genovaindonesia/genova-chocolate-classic-frappe-powder-1000-gram?extParam=whid%3D8872969",
          packaging: "1 Pack Powder",
          weight: "1000 Gram",
          serving:
            "- Masukkan 20-30 Gram Powder\n- Dicampur 120-150ML Susu\n- Aduk/shake hingga tercampur rata dan sajikan",
          color: "",
          tasting: "",
          penyimpanan:
            "- Simpan Produk ditempat yang sejuk dan terhindar dari Sinar Matahari langsung\n- Hindari dari tempat yang berbau tajam.",
        },
        {
          id: 5,
          name: "Powder Cookies",
          image: "../powder_cookiescream.jpg",
          price: "155,000",
          categoryId: "powder",
          info: "Cocok Digunakan untuk :\n- Untuk Meng-explore Minuman Terkini\n- Pembuatan Kue\n- Pembuatan Minuman\n- Aneka Olahan Lainnya",
          link: "https://www.tokopedia.com/genovaindonesia/genova-cookies-cream-frappe-powder-1000-gram?extParam=whid%3D8872969",
          packaging: "1 Pack Powder",
          weight: "1000 Gram",
          serving:
            "- Masukkan 20-30 Gram Powder\n- Dicampur 120-150ML Susu\n- Aduk/shake hingga tercampur rata dan sajikan",
          color: "",
          tasting: "",
          penyimpanan:
            "- Simpan Produk ditempat yang sejuk dan terhindar dari Sinar Matahari langsung\n- Hindari dari tempat yang berbau tajam.",
        },
        {
          id: 6,
          name: "Powder Cotton Candy",
          image: "../powder_cottoncandy.jpg",
          price: "139,000",
          categoryId: "powder",
          info: "Cocok Digunakan untuk :\n- Untuk Meng-explore Minuman Terkini\n- Pembuatan Kue\n- Pembuatan Minuman\n- Aneka Olahan Lainnya",
          link: "https://www.tokopedia.com/genovaindonesia/genova-cotton-candy-frappe-powder-1000-gram?extParam=whid%3D8872969",
          packaging: "1 Pack Powder",
          weight: "1000 Gram",
          serving:
            "- Masukkan 20-30 Gram Powder\n- Dicampur 120-150ML Susu\n- Aduk/shake hingga tercampur rata dan sajikan",
          color: "",
          tasting: "",
          penyimpanan:
            "- Simpan Produk ditempat yang sejuk dan terhindar dari Sinar Matahari langsung\n- Hindari dari tempat yang berbau tajam.",
        },
        {
          id: 7,
          name: "Powder Dark Chocolate",
          image: "../powder_darkchocolate.jpg",
          price: "139,000",
          categoryId: "powder",
          info: "Cocok Digunakan untuk :\n- Untuk Meng-explore Minuman Terkini\n- Pembuatan Kue\n- Pembuatan Minuman\n- Aneka Olahan Lainnya",
          link: "https://www.tokopedia.com/genovaindonesia/genova-dark-chocolate-frappe-powder-1000-gram?extParam=whid%3D8872969",
          packaging: "1 Pack Powder",
          weight: "1000 Gram",
          serving:
            "- Masukkan 20-30 Gram Powder\n- Dicampur 120-150ML Susu\n- Aduk/shake hingga tercampur rata dan sajikan",
          color: "",
          tasting: "",
          penyimpanan:
            "- Simpan Produk ditempat yang sejuk dan terhindar dari Sinar Matahari langsung\n- Hindari dari tempat yang berbau tajam.",
        },
        {
          id: 8,
          name: "Powder Frappe Base",
          image: "../powder_frappebase.jpg",
          price: "139,000",
          categoryId: "powder",
          info: "Cocok Digunakan untuk :\n- Untuk Meng-explore Minuman Terkini\n- Pembuatan Kue\n- Pembuatan Minuman\n- Aneka Olahan Lainnya",
          link: "https://www.tokopedia.com/genovaindonesia/genova-base-frappe-powder-1000-gram?extParam=whid%3D8872969",
          packaging: "1 Pack Powder",
          weight: "1000 Gram",
          serving:
            "- Masukkan 20-30 Gram Powder\n- Dicampur 120-150ML Susu\n- Aduk/shake hingga tercampur rata dan sajikan",
          color: "",
          tasting: "",
          penyimpanan:
            "- Simpan Produk ditempat yang sejuk dan terhindar dari Sinar Matahari langsung\n- Hindari dari tempat yang berbau tajam.",
        },
        {
          id: 9,
          name: "Powder Greentea",
          image: "../powder_greentea.jpg",
          price: "150,000",
          categoryId: "powder",
          info: "Cocok Digunakan untuk :\n- Untuk Meng-explore Minuman Terkini\n- Pembuatan Kue\n- Pembuatan Minuman\n- Aneka Olahan Lainnya",
          link: "https://www.tokopedia.com/genovaindonesia/genova-greentea-frappe-powder-1000-gram?extParam=whid%3D8872969",
          packaging: "1 Pack Powder",
          weight: "1000 Gram",
          serving:
            "- Masukkan 20-30 Gram Powder\n- Dicampur 120-150ML Susu\n- Aduk/shake hingga tercampur rata dan sajikan",
          color: "",
          tasting: "",
          penyimpanan:
            "- Simpan Produk ditempat yang sejuk dan terhindar dari Sinar Matahari langsung\n- Hindari dari tempat yang berbau tajam.",
        },
        {
          id: 10,
          name: "Powder Macchiato",
          image: "../powder_macchiato.jpg",
          price: "139,000",
          categoryId: "powder",
          info: "Cocok Digunakan untuk :\n- Untuk Meng-explore Minuman Terkini\n- Pembuatan Kue\n- Pembuatan Minuman\n- Aneka Olahan Lainnya",
          link: "https://www.tokopedia.com/genovaindonesia/genova-macchiato-frappe-powder-1000-gram?extParam=whid%3D8872969",
          packaging: "1 Pack Powder",
          weight: "1000 Gram",
          serving:
            "- Masukkan 20-30 Gram Powder\n- Dicampur 120-150ML Susu\n- Aduk/shake hingga tercampur rata dan sajikan",
          color: "",
          tasting: "",
          penyimpanan:
            "- Simpan Produk ditempat yang sejuk dan terhindar dari Sinar Matahari langsung\n- Hindari dari tempat yang berbau tajam.",
        },
        {
          id: 11,
          name: "Powder Matcha Latte",
          image: "../powder_matchalatte.jpg",
          price: "169,000",
          categoryId: "powder",
          info: "Cocok Digunakan untuk :\n- Untuk Meng-explore Minuman Terkini\n- Pembuatan Kue\n- Pembuatan Minuman\n- Aneka Olahan Lainnya",
          link: "https://www.tokopedia.com/genovaindonesia/genova-matcha-latte-frappe-powder-1000-gram?extParam=whid%3D8872969",
          packaging: "1 Pack Powder",
          weight: "1000 Gram",
          serving:
            "- Masukkan 20-30 Gram Powder\n- Dicampur 120-150ML Susu\n- Aduk/shake hingga tercampur rata dan sajikan",
          color: "",
          tasting: "",
          penyimpanan:
            "- Simpan Produk ditempat yang sejuk dan terhindar dari Sinar Matahari langsung\n- Hindari dari tempat yang berbau tajam.",
        },
        {
          id: 12,
          name: "Powder Matcha Premium",
          image: "../powder_matchapremium.jpg",
          price: "245,000",
          categoryId: "powder",
          info: "Cocok Digunakan untuk :\n- Untuk Meng-explore Minuman Terkini\n- Pembuatan Kue\n- Pembuatan Minuman\n- Aneka Olahan Lainnya",
          link: "https://www.tokopedia.com/genovaindonesia/genova-matcha-premium-frappe-powder-1000-gram?extParam=whid%3D8872969",
          packaging: "1 Pack Powder",
          weight: "1000 Gram",
          serving:
            "- Masukkan 20-30 Gram Powder\n- Dicampur 120-150ML Susu\n- Aduk/shake hingga tercampur rata dan sajikan",
          color: "",
          tasting: "",
          penyimpanan:
            "- Simpan Produk ditempat yang sejuk dan terhindar dari Sinar Matahari langsung\n- Hindari dari tempat yang berbau tajam.",
        },
        {
          id: 13,
          name: "Powder Mocha",
          image: "../powder_mocha.jpg",
          price: "139,000",
          categoryId: "powder",
          info: "Cocok Digunakan untuk :\n- Untuk Meng-explore Minuman Terkini\n- Pembuatan Kue\n- Pembuatan Minuman\n- Aneka Olahan Lainnya",
          link: "https://www.tokopedia.com/genovaindonesia/genova-mocha-frappe-powder-1000-gram?extParam=whid%3D8872969",
          packaging: "1 Pack Powder",
          weight: "1000 Gram",
          serving:
            "- Masukkan 20-30 Gram Powder\n- Dicampur 120-150ML Susu\n- Aduk/shake hingga tercampur rata dan sajikan",
          color: "",
          tasting: "",
          penyimpanan:
            "- Simpan Produk ditempat yang sejuk dan terhindar dari Sinar Matahari langsung\n- Hindari dari tempat yang berbau tajam.",
        },
        {
          id: 14,
          name: "Powder Mochaccino",
          image: "../powder_mochaccino.jpg",
          price: "139,000",
          categoryId: "powder",
          info: "Cocok Digunakan untuk :\n- Untuk Meng-explore Minuman Terkini\n- Pembuatan Kue\n- Pembuatan Minuman\n- Aneka Olahan Lainnya",
          link: "https://www.tokopedia.com/genovaindonesia/genova-mochaccino-frappe-powder-1000-gram?extParam=whid%3D8872969",
          packaging: "1 Pack Powder",
          weight: "1000 Gram",
          serving:
            "- Masukkan 20-30 Gram Powder\n- Dicampur 120-150ML Susu\n- Aduk/shake hingga tercampur rata dan sajikan",
          color: "",
          tasting: "",
          penyimpanan:
            "- Simpan Produk ditempat yang sejuk dan terhindar dari Sinar Matahari langsung\n- Hindari dari tempat yang berbau tajam.",
        },
        {
          id: 15,
          name: "Powder Red Velvet",
          image: "../powder_redvelvet.jpg",
          price: "139,000",
          categoryId: "powder",
          info: "Cocok Digunakan untuk :\n- Untuk Meng-explore Minuman Terkini\n- Pembuatan Kue\n- Pembuatan Minuman\n- Aneka Olahan Lainnya",
          link: "https://www.tokopedia.com/genovaindonesia/genova-red-velvet-frappe-powder-1000-gram?extParam=whid%3D8872969",
          packaging: "1 Pack Powder",
          weight: "1000 Gram",
          serving:
            "- Masukkan 20-30 Gram Powder\n- Dicampur 120-150ML Susu\n- Aduk/shake hingga tercampur rata dan sajikan",
          color: "",
          tasting: "",
          penyimpanan:
            "- Simpan Produk ditempat yang sejuk dan terhindar dari Sinar Matahari langsung\n- Hindari dari tempat yang berbau tajam.",
        },
        {
          id: 16,
          name: "Powder Swiss Chocholate",
          image: "../powder_swisschocholate.jpg",
          price: "139,000",
          category: 0,
          info: "Cocok Digunakan untuk : - Untuk Meng-explore Minuman Terkini - Pembuatan Kue - Pembuatan Minuman - Aneka Olahan Lainnya, Brand : Genova - Naturally Flavored Sertifikat Halal MUI : YA",
          link: "https://www.tokopedia.com/genovaindonesia/genova-swiss-chocolate-frappe-powder-1000-gram?extParam=whid%3D8872969",
          packaging: "1 Pack Powder",
          weight: "1000 Gram",
          serving:
            "- Masukkan 20-30 Gram Powder - Dicampur 120-150ML Susu - Aduk/shake hingga tercampur rata dan sajikan",
          color: "",
          tasting: "",
        },
        {
          id: 17,
          name: "Powder Taro",
          image: "../powder_taro.jpg",
          price: "139,000",
          category: 0,
          info: "Cocok Digunakan untuk : - Untuk Meng-explore Minuman Terkini - Pembuatan Kue - Pembuatan Minuman - Aneka Olahan Lainnya, Brand : Genova - Naturally Flavored Sertifikat Halal MUI : YA",
          link: "https://www.tokopedia.com/genovaindonesia/genova-taro-frappe-powder-1000-gram?extParam=whid%3D8872969",
          packaging: "1 Pack Powder",
          weight: "1000 Gram",
          serving:
            "- Masukkan 20-30 Gram Powder - Dicampur 120-150ML Susu - Aduk/shake hingga tercampur rata dan sajikan",
          color: "",
          tasting: "",
        },
        {
          id: 18,
          name: "Powder Thai Tea",
          image: "../powder_thaitea.jpg",
          price: "139,000",
          categoryId: "powder",
          info: "Cocok Digunakan untuk :\n- Untuk Meng-explore Minuman Terkini\n- Pembuatan Kue\n- Pembuatan Minuman\n- Aneka Olahan Lainnya",
          link: "https://www.tokopedia.com/genovaindonesia/genova-thai-tea-frappe-powder-1000-gram?extParam=whid%3D8872969",
          packaging: "1 Pack Powder",
          weight: "1000 Gram",
          serving:
            "- Masukkan 20-30 Gram Powder\n- Dicampur 120-150ML Susu\n- Aduk/shake hingga tercampur rata dan sajikan",
          color: "",
          tasting: "",
          penyimpanan:
            "- Simpan Produk ditempat yang sejuk dan terhindar dari Sinar Matahari langsung\n- Hindari dari tempat yang berbau tajam.",
        },
        {
          id: 19,
          name: "Powder Tiramisu",
          image: "../powder_tiramisu.jpg",
          price: "139,000",
          categoryId: "powder",
          info: "Cocok Digunakan untuk :\n- Untuk Meng-explore Minuman Terkini\n- Pembuatan Kue\n- Pembuatan Minuman\n- Aneka Olahan Lainnya",
          link: "https://www.tokopedia.com/genovaindonesia/genova-tiramisu-frappe-powder-1000-gram?extParam=whid%3D8872969",
          packaging: "1 Pack Powder",
          weight: "1000 Gram",
          serving:
            "- Masukkan 20-30 Gram Powder\n- Dicampur 120-150ML Susu\n- Aduk/shake hingga tercampur rata dan sajikan",
          color: "",
          tasting: "",
          penyimpanan:
            "- Simpan Produk ditempat yang sejuk dan terhindar dari Sinar Matahari langsung\n- Hindari dari tempat yang berbau tajam.",
        },
      ],
      searchQuery: "",
    };
  },
  computed: {
    // Get the filtered projects
    resultQuery() {
      if (this.searchQuery) {
        return this.products.filter((item) => {
          return this.searchQuery
            .toLowerCase()
            .split(" ")
            .every((v) => item.name.toLowerCase().includes(v));
        });
      } else {
        return this.products;
      }
    },
  },
  methods: {
    shareData() {
      // this.$router.push({
      //   name: "detail-product",
      //   // eslint-disable-next-line no-undef
      //   params: JSON.stringify(product),
      // });
      this.$router.push({
        name: "detail-product",
        // params: {
        //   objectParam: JSON.stringify({ a: "a" }),
        // },
      });
    },
  },
};
</script>

<style scoped></style>
