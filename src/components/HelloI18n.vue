<template>
  <div>
    <p>{{ $t("hello") }}</p>
    <p>{{ $t("message") }}</p>
    <p>{{ $t("goodbye") }}</p>
    <p>{{ $t("apples") }}</p>
    <p>{{ $t("fruit.green.apple") }}</p>
    <p>{{ $t("fruit.yellow.banana") }}</p>
    <p>{{ $t("fruit.green.kiwi") }}</p>
  </div>
</template>

<script>
export default {
  name: "HelloI18n"
};
</script>

<i18n>
{
  "en": {
    "hello": "Hello i18n in SFC!"
  },
  "es":{
    "hello": "Hola"
  }
}
</i18n>
