<template>
  <div>
    <div class="container pb-5">
      <div>
        <router-link
          :to="{ name: 'Products', params: { id: option.id } }"
          class="card mb-4 p-2 shadow"
          v-for="option in menu"
          :key="option.name"
        >
          <div class="row g-0">
            <div class="col-3 col-md-2 d-flex align-items-center">
              <div class="ratio ratio-1x1">
                <img
                  :src="option.img"
                  class="rounded-3 img-fluid"
                  style="width: 5rem; height: 5rem; object-fit: cover"
                  alt=""
                />
              </div>
            </div>
            <div class="col-8 d-flex align-items-center">
              <div class="card-body">
                <h5 class="card-title fw-bold">{{ option.name }}</h5>
              </div>
            </div>
          </div>
        </router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  methods: {
    scrollToTop(option) {
      window.scrollTo(0, 0);
      if (option != null) this.selectedProducts = option.products;
      else this.selectedProducts = null;
    },
  },
  data() {
    return {
      selectedProducts: null,
      menu: [
        {
          img: require("../assets/images/juice.jpg"),
          name: "БЕЗАЛКОХОЛНИ ПИЈАЛОЦИ",
          id: 0,
        },
        {
          img: require("../assets/images/beer.jpeg"),
          name: "ПИВО",
          id: 1,
        },
        {
          img: require("../assets/images/wine.jpeg"),
          name: "ВИНАРИЈА",
          id: 2,
        },
        {
          img: require("../assets/images/coffee.jpg"),
          name: "ТОПЛИ НАПИТОЦИ",
          id: 3,
        },
        {
          img: require("../assets/images/alcochol.jpg"),
          name: "АЛКОХОЛНИ ПИЈАЛОЦИ",
          id: 4,
        },

        {
          img: require("../assets/images/salad.jpg"),
          name: "САЛАТИ",
          id: 5,
        },
        {
          img: require("../assets/images/meat.jpg"),
          name: "ЈАДЕЊА НА СКАРА",
          id: 6,
        },
        {
          img: require("../assets/images/breakfast.jpg"),
          name: "ПРИЛОЗИ И ДОРУЧЕК",
          id: 7,
        },
        {
          img: require("../assets/images/ajvar.jpg"),
          name: "ЗА НЕ МНОГУ ГЛАДНИ",
          id: 8,
        },
        {
          img: require("../assets/images/speciality.jpg"),
          name: "СПЕЦИАЛИТЕТИ И ЈАДЕЊА ПО НАРАЧКА",
          id: 9,
        },
        {
          img: require("../assets/images/fish.jpg"),
          name: "РИБА",
          id: 10,
        },
        {
          img: require("../assets/images/dessert.jpg"),
          name: "ДЕСЕРТИ",
          id: 11,
        },
      ],
    };
  },
};
</script>

<style scoped>
.back {
  font-size: 1.2rem;
}
</style>
