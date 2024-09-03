<template>
  <div>
    <div class="container pb-5">
      <router-link
        :to="{ name: 'Home' }"
        class="mb-4 back btn btn-warning shadow border-radius-14px fw-bold px-3"
      >
        &lt; Назад кон менито
      </router-link>
      <div>
        <div
          class="card mb-4 p-4 shadow"
          v-for="(product, i) in products[this.$route.params.id]"
          :key="i"
        >
          <div
            class="d-flex flex-row align-items-center justify-content-between"
          >
            <div class="d-flex flex-column">
              <div class="fw-bold">
                {{ product.name }}
              </div>
              <div class="fst-italic ingredients">
                {{ product.ingredients }}
              </div>
            </div>
            <div class="fw-bold fst-italic text-nowrap">
              {{ product.price }} ден.
            </div>
          </div>
        </div>
      </div>
      <router-link
        :to="{ name: 'Home' }"
        class="back mb-2 btn btn-warning shadow border-radius-14px fw-bold px-3"
      >
        &lt; Назад кон менито
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "Products",
  data() {
    return {
      products: [
        // НЕГАЗИРАНИ ПИЈАЛОЦИ/SOFT DRINKS
        [
          {
            name: "Вода (голема)/Water 0.75",
            price: "120",
            ingredients: "Безалкохолни пијалоци",
          },
          {
            name: "Вода (мала)/Water 0.25",
            price: "80",
            ingredients: "Безалкохолни пијалоци",
          },
          {
            name: "Пепси",
            price: "120",
            ingredients: "Безалкохолни пијалоци",
          },
          {
            name: "Пепси Макс",
            price: "120",
            ingredients: "Безалкохолни пијалоци",
          },
          {
            name: "Газоза/Gazoza",
            price: "100",
            ingredients: "Безалкохолни пијалоци",
          },
          {
            name: "Леден Чај/Ice Tea",
            price: "120",
            ingredients: "Безалкохолни пијалоци",
          },
          {
            name: "7уп",
            price: "120",
            ingredients: "Безалкохолни пијалоци",
          },
          {
            name: "Негазирани сокови/Juice",
            price: "140",
            ingredients: "Безалкохолни пијалоци",
          },
          {
            name: "Цеден Лимон/Fresh Lemon Juice",
            price: "90",
            ingredients: "Безалкохолни пијалоци",
          },
          {
            name: "Цеден портокал/Fresh Orange Juice",
            price: "180",
            ingredients: "Безалкохолни пијалоци",
          },
          {
            name: "Mirinda/Mirinda",
            price: "120",
            ingredients: "Безалкохолни пијалоци",
          },
          {
            name: "Домашна лимонада со вкус/Homemade lemonade",
            price: "160",
            ingredients: "Безалкохолни пијалоци",
          },
          {
            name: "Овошна сода",
            price: "140",
            ingredients: "Безалкохолни пијалоци"
          }
        ],
        // ПИВО
        [
          {
            name: "Крали Марко 0.5",
            price: "140",
            ingredients: "Пиво",
          },
          {
            name: "Златен Даб 0.33",
            price: "130",
            ingredients: "Пиво",
          },
          {
            name: "Златен Даб Драфт 0.33",
            price: "140",
            ingredients: "Пиво",
          },
          {
            name: "Златен Даб Драфт 0.5",
            price: "170",
            ingredients: "Пиво",
          },
          {
            name: "Fox Pale ale draft 0.5",
            price: "240",
            ingredients: "Пиво",
          },
          {
            name: "Veda White ipa draft 0.5",
            price: "260",
            ingredients: "Пиво",
          },
          {
            name: "Corona",
            price: "250",
            ingredients: "Пиво",
          },
          {
            name: "Kalesh-Black ipa 0.33",
            price: "250",
           ingredients: "Пиво",
        
          },
          {
            name: "Tuborg 0.33",
            price: "170",
            ingredients: "Пиво",

          },
          {
            name: "Tuborg Draft 0.4",
            price: "220",
            ingredients: "Пиво",
          },
          {
            name: "Carlsberg 0.33",
            price: "190",
            ingredients: "Пиво",
          },
          {
            name: "Holsten 0.5",
            price: "260",
            ingredients: "Пиво",

          },
          {
            name: "Kozel 0.5",
            price: "220",
            ingredients: "Пиво",
          },
          {
            name: "Franziskaner 0.5",
            price: "280",
            ingredients: "Пиво",
          },
        ],
        // ВИНАРИЈА
        [
          {
            name: "Synthesis cuvee barrique(dry)",
            price: "1900",
            ingredients: "Винарија",
          },
          {
            name: "Dionis vranec barrique(dry)",
            price: "2200",
            ingredients: "Винарија",
          },
          {
            name: "Hermes vranec(dry)",
            price: "1300",
            ingredients: "Винарија",
          },
          {
            name: "Hermes cabernet sauvignon(dry)",
            price: "1300",
            ingredients: "Винарија",
          },
          {
            name: "Amfora vranec(semi-dry)",
            price: "900",
            ingredients: "Винарија",
          },
          {
            name: "Chardonnay barrique fermented(dry)",
            price: "2400",
            ingredients: "Винарија",
          },
          {
            name: "Muscat temjanika(semi-dry)",
            price: "1350",
            ingredients: "Винарија",
          },
          {
            name: "Elegija chardonnay(dry)",
            price: "1300",
            ingredients: "Винарија",
          },
          {
            name: "Elegija traminer(dry)",
            price: "1300",
            ingredients: "Винарија",
          },
          {
            name: "Elegija zupljanka(dry)",
            price: "1300",
            ingredients: "Винарија",
          },
          {
            name: "Amphora cuvee(semi-dry)",
            price: "900",
            ingredients: "Винарија",
          },
          {
            name: "Temjanika(dry)",
            price: "1400",
            ingredients: "Винарија",
          },
          {
            name: "Chardonnay(dry)",
            price: "1400",
            ingredients: "Винарија",
          },
          {
            name: "Sauvignon blanc(dry)",
            price: "1400",
            ingredients: "Винарија",
          },
          {
            name: "Amfora Rose(dry)",
            price: "900",
            ingredients: "Винарија",
          },
          {
            name: "Elegija syrah(dry)",
            price: "1200",
            ingredients: "Винарија",
          },
          {
            name: "Muscat rolinger(dry)",
            price: "1250",
            ingredients: "Винарија",
          },
          {
            name: "Muscat rolinger red(semi-dry)",
            price: "1250",
            ingredients: "Винарија",
          },
        ],
        // КАФЕ И ЧАЈ/COFFEE AND TEA
        [
          {
            name: "Чај/Tea",
            price: "80",
            ingredients: "Топли напитоци",
          },
          {
            name: "Еспресо/Espresso",
            price: "90",
            ingredients: "Топли напитоци",
          },
          {
            name: "Макијато/Macchiato",
            price: "100",
            ingredients: "Топли напитоци",
          },
          {
            name: "Големо Макијато",
            price: "110",
            ingredients: "Топли напитоци",
          },
          {
            name: "Latte macchiato",
            price: "160",
            ingredients: "Топли напитоци",
          },
          {
            name: "Нес кафе",
            price: "140",
            ingredients: "Топли напитоци",
          },
          {
            name: "Капучино",
            price: "120",
            ingredients: "Топли напитоци",
          
          },
          {
            name: "Ладно макијато",
            price: "110",
            ingredients: "Топли напитоци",

          },
          {
            name: "Ирско кафе",
            price: "260",
            ingredients: "Топли напитоци",
          },
          {
            name: "Американо",
            price: "120",
            ingredients: "Топли напитоци",
          },
          {
            name: "Македонско кафе",
            price: "90",
            ingredients: "Топли напитоци",
          },
        ],
        // АЛКОХОЛНИ ПИЈАЛОЦИ
        [
          {
            name: "Лозова Жолта",
            price: "120",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Лозова бела",
            price: "120",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Мастика",
            price: "120",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Ракија Азбука",
            price: "130",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Гордион амбер ракија",
            price: "160",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Бадел Вилијамс ракија",
            price: "170",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Џин бадел",
            price: "120",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Смидџин",
            price: "250",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Џин беефеатер",
            price: "170",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Џин Гордонс",
            price: "190",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Џин пинк Гордонс",
            price: "180",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Џин Бомбај",
            price: "240",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Водка бадел",
            price: "120",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Бејлис",
            price: "180",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Фенејс",
            price: "150",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Крушковац пеар ликер",
            price: "140",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Текила",
            price: "130",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Амарето",
            price: "150",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Корлат Шливовица",
            price: "220",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Корлат мараска",
            price: "220",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Шот",
            price: "100",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Смирноф",
            price: "160",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Џек Даниелс",
            price: "280",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Џемјсон",
            price: "180",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Џејмсон Блек",
            price: "290",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Џони Ред",
            price: "160",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Џони Блек",
            price: "260",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "4 Рози",
            price: "200",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Вилијам Пеел",
            price: "150",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Рум Морган",
            price: "160",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Јегермајстер",
            price: "210",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Пелинковац бадел",
            price: "120",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Пелинковац антик",
            price: "170",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Коњак бадел",
            price: "120",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Коњак бадел блек",
            price: "160",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Рум бадел",
            price: "120",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Шток 84",
            price: "150",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Текила олмека",
            price: "170",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Аперол",
            price: "160",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Корлат лоза",
            price: "220",
            ingredients: "Алкохолни пијалоци",
          },
          {
            name: "Кампари",
            price: "160",
            ingredients: "Алкохолни пијалоци",
          },
        ],
        // САЛАТИ
        [
          {
            name: "Мешана свежа салата",
            price: "180",
            ingredients: "Сезонски зеленчук",
          },
          {
            name: "Шопска салата",
            price: "180",
            ingredients: "Домати, краставица, кравјо сирење",
          },
          {
            name: "Грчка салата",
            price: "180",
            ingredients: "Домати, краставица, кравјо сирење, маслинки, кромид",
          },
          {
            name: "Македонска салата",
            price: "150",
            ingredients: "Домати, кромид, печени пиперки",
          },
          {
            name: "Селска салата",
            price: "200",
            ingredients: "Домати, краставица, сирење, пиперка",
          },
          {
            name: "Овчарска салата",
            price: "280",
            ingredients:
              "Домати, краставица, сирење, јајце, кашкавал, печурки, сланина",
          },
          {
            name: "Цезар салата",
            price: "250",
            ingredients:
              "Марула, пилешко, кубети, дресинг сос, врат, кашкавал, сусам ",
          },
          {
            name: "Туршија",
            price: "140",
            ingredients: "Зеленчук",
          },
          {
            name: "Павлака со пиперка",
            price: "120",
            ingredients: "Павлака, пиперка",
          },
          {
            name: "Преслап салата",
            price: "1200",
            ingredients:
              "Сезонски зеленчук, сезонски пинџур, тиквички, патлиџан, печурки, домашно лепче, павлака со пиперка, овчо сирење",
          },
          {
            name: "Таратор",
            price: "160",
            ingredients: "Павлака, краставица, лук",
          },
        ],

        // ЈАДЕЊЕ НА СКАРА
        [
          {
            name: "Преслап плескавица (500 гр.)",
            price: "350",
            ingredients: "Свинско, телешко, кашкавал, печурки, сланина, кулен",
          },
          {
            name: "Осоговска плескавица (350 гр.)",
            price: "280",
            ingredients: "Свинско, телешко, кашкавал",
          },
          {
            name: "Лута плескавица (350 гр.)",
            price: "240",
            ingredients: "Свинско, телешко, сува лута пиперка",
          },
          {
            name: "Ќебап",
            price: "20",
            ingredients: "Свинско, телешко месо",
          },
          {
            name: "Бифтек 1кг.",
            price: "1300",
            ingredients: "Свинско месо",
          },
          {
            name: "Бела вешалица (250гр.)",
            price: "250",
            ingredients: "Свинско месо, кашкавал",
          },
          {
            name: "Ребро 1кг.",
            price: "1000",
            ingredients: "Свинско месо",
          },
          {
            name: "Ложено месо 1кг.",
            price: "1000",
            ingredients: "Врат, бут, памфлак",
          },
          {
            name: "Домашен дебел колбас",
            price: "150",
            ingredients: "Свинско, пилешко и кашкавал",
          },
        ],

        // ПРИЛОЗИ И ДОРУЧЕК
        [
          {
            name: "Рестован помфрит",
            price: "130",
            ingredients: "Прилози и доручек",
          },
          {
            name: "Рестован помфрит со сирење",
            price: "160",
            ingredients: "Прилози и доручек",
          },
          {
            name: "Пекарски компир",
            price: "150",
            ingredients: "Прилози и доручек",
          },
          {
            name: "Пекарски компир со луг",
            price: "160",
            ingredients: "Прилози и доручек",
          },
          {
            name: "Македонски доручек",
            price: "200",
            ingredients: "Тост лепче, јајца на око, ајвар овчо сирење",
          },
          {
            name: "Домашно лепче",
            price: "30",
            ingredients: "Прилози и доручек",
          },
          {
            name: "Додаток",
            price: "20",
            ingredients: "Прилози и доручек",
          },
          {
            name: "Гарнир",
            price: "30",
            ingredients: "Прилози и доручек",
          },
          {
            name: "Варено јајце",
            price: "20",
            ingredients: "Прилози и доручек",
          },
          {
            name: "Пиперка",
            price: "30",
            ingredients: "Прилози и доручек",
          },
          {
            name: "Омлет по желба",
            price: "180",
            ingredients: "Прилози и доручек",
          },
        ],

        // ЗА НЕ МНОГУ ГЛАДНИ
        [
          {
            name: "Овчо сирење 1кг.",
            price: "1400",
            ingredients: "За не многу гладни",
          },
          {
            name: "Биено сирење 1кг.",
            price: "1600",
            ingredients: "Кравјо сирење",
          },
          {
            name: "Кравји кашкавал 1кг.",
            price: "1600",
            ingredients: "За не многу гладни",
          },
          {
            name: "Кајмак порција",
            price: "140",
            ingredients: "За не многу гладни",
          },
          {
            name: "Сирење по селски",
            price: "300",
            ingredients: "Домати, сирење кравјо, сланина, кашкавал, јајце",
          },
          {
            name: "Топено грне",
            price: "300",
            ingredients: "Сирење кравјо, зденка, ајвар, маслинки. кашкавал",
          },
          {
            name: "Пинџур сезонски",
            price: "120",
            ingredients: "За не многу гладни",
          },
          {
            name: "Лутеница",
            price: "120",
            ingredients: "За не многу гладни",
          },
          {
            name: "Ајвар",
            price: "120",
            ingredients: "За не многу гладни",
          },
          {
            name: "Тиквички",
            price: "180",
            ingredients: "За не многу гладни",
          },
          {
            name: "Похована пирошка",
            price: "90",
            ingredients: "За не многу гладни",
          },
          {
            name: "Похован кашкавал",
            price: "160",
            ingredients: "За не многу гладни",
          },
          {
            name: "Поховано сирење",
            price: "120",
            ingredients: "За не многу гладни",
          },
          {
            name: "Похована зденка",
            price: "30",
            ingredients: "За не многу гладни",
          },
          {
            name: "Поховани прсти",
            price: "250",
            ingredients: "За не многу гладни",
          },
          {
            name: "Поховани тиквички",
            price: "200",
            ingredients: "За не многу гладни",
          },
          {
            name: "Поховани печурки",
            price: "220",
            ingredients: "За не многу гладни",
          },
          {
            name: "Похована даска",
            price: "1200",
            ingredients: "За не многу гладни",
          },
          {
            name: "Печурки на скара",
            price: "200",
            ingredients: "За не многу гладни",
          },
          {
            name: "Фурнаринки",
            price: "150",
            ingredients: "За не многу гладни",
          },
          {
            name: "Перничиња",
            price: "280",
            ingredients: "Со кајчак и свинска пршута",
          },
          {
            name: "Перничиња",
            price: "280",
            ingredients: "Со моцарела и маслинки",
          },
        ],
        // ПРЕДЈАДЕЊА
        [
          {
            name: "Тава Преслап за 2 лица",
            price: "900",
            ingredients:
              "Свинско, пилешко, кашкавал, печурки, сланина, зеленчук, млеко, јајца",
          },
          {
            name: "Свинско месо со праз (500 гр.)",
            price: "700",
            ingredients: "Свинско, праз, сува пиперка",
          },
          {
            name: "Пржено месо 1 кг.",
            price: "1400",
            ingredients: "Пржено месо во бакарна тава",
          },
          {
            name: "Ребро во фурна 1кг.",
            price: "1200",
            ingredients: "Свинско месо",
          },
          {
            name: "Ребро во фурна со барбику сос 1кг.",
            price: "1400",
            ingredients: "Свинско месо со барбику сос",
          },
          {
            name: "Селско месо (СВИНСКО ИЛИ ПИЛЕШКО)",
            price: "300",
            ingredients: "Свинско месо, печурки, кромид, вино, зачини",
          },
          {
            name: "Мучкалица (СВИНСКО ИЛИ ПИЛЕШКО)",
            price: "300",
            ingredients:
              "Свинско месо, печурки, домати, кашкавал, кромид, вино, зачини",
          },
        ],
        // РИБА
        [
          {
            name: "Пастрмка 1кг.",
            price: "1000",
            ingredients: "Риба",
          },
          {
            name: "Крап кременадла 1кг.",
            price: "1500",
            ingredients: "Риба",
          },
        ],
        // ДЕСЕРТИ
        [
          {
            name: "Палачинка со крем и банана",
            price: "130",
            ingredients: "Десерти",
          },
          {
            name: "Палачинка со мед и ореви",
            price: "160",
            ingredients: "Десерти",
          },
          {
            name: "Палачинка со овошје",
            price: "130",
            ingredients: "Десерти",
          },
          {
            name: "Торта баунти",
            price: "100",
            ingredients: "Десерти",
          },
          {
            name: "Раваниа",
            price: "80",
            ingredients: "Десерти",
          },
          {
            name: "Баклава со овошје",
            price: "100",
            ingredients: "Десерти",
          },
        ],
      ],
    };
  },
};
</script>

<style scoped></style>
