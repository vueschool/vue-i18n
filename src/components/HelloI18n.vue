<template>
  <div>
    <!-- <p>{{ $t("hello", { name }) }}</p>
    <p>{{ $t("email", { email }) }}</p>
    <p>{{ $t("goodbye") }}</p> -->

    <!-- <p>{{ $tc("car", 2) }}</p>
    <p>{{ $tc("person", 0) }}</p>
    <p>{{ $tc("person", 1) }}</p>
    <p>{{ $tc("person", 10, { n: "too many" }) }}</p>

    <p>{{ $tc("apple", 0) }}</p>
    <p>{{ $tc("apple", 1) }}</p>
    <p>{{ $tc("apple", 2) }}</p> -->

    <!-- <p>{{ $d(new Date(), "long") }}</p> -->
    <!-- <p>{{ $d(new Date(), "long", "en-GB") }}</p> -->

    <p>{{ product.name }}: {{ $n(product.price, "currency") }}</p>
    <p>{{ product.stock }} left in stock</p>

    <button @click="setLocale('en-GB')" class="button">UK</button>
    <button @click="setLocale('en-US')" class="button">USA</button>
    <button @click="setLocale('es-ES')" class="button">Spain</button>
  </div>
</template>

<script>
const products = {
  "en-GB": {
    name: "Red Jeans",
    stock: 4,
    price: 89
  },
  "en-US": {
    name: "Red Jeans",
    stock: 2,
    price: 109
  },
  "es-ES": {
    name: "Vaqueros Rojos",
    stock: 9,
    price: 99
  }
};

export default {
  name: "HelloI18n",
  data() {
    return {
      name: "Peter",
      email: "info@vueschool.com"
    };
  },
  methods: {
    setLocale(locale) {
      this.$i18n.locale = locale;
      localStorage.setItem("locale", locale);
    }
  },
  computed: {
    product() {
      return products[this.$i18n.locale];
    }
  }
};
</script>
