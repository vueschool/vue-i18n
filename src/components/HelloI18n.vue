<template>
  <div>
    <p>{{ $t("hello", { name }) }}</p>
    <p>{{ $t("email", { email }) }}</p>
    <p>{{ $t("goodbye") }}</p>
    <button @click="setLocale('en')" class="button">English</button>
    <button @click="setLocale('es')" class="button">Spanish</button>
    <button @click="setLocale('de')" class="button">German</button>
  </div>
</template>

<script>
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
  }
};
</script>
