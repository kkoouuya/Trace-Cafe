<template>
  <header class="header">
    <div class="headerContainer">
      <nuxt-link to="/">
        <img class="logo" src="../assets/images/nco_logo.png" />
      </nuxt-link>

      <nav>
        <ul class="menu">
          <li v-for="head in headers" :key="head.id">
            <nuxt-link :to="head.slug" class="menu__link">{{
              head.title
            }}</nuxt-link>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script setup lang="ts">
const headers = ref([
  {
    title: "商品情報",
    id: "001",
    slug: "item_info",
  },
  {
    title: "Blog",
    id: "002",
    slug: "blog",
  },
  {
    title: "アクセス",
    id: "003",
    slug: "access",
  },
  {
    title: "会社理念",
    id: "004",
    slug: "philosophy",
  },
  {
    title: "お問い合わせ",
    id: "005",
    slug: "contact",
  },
]);
</script>

<style lang="scss" scoped>
/* todo 画像の比率を保ったまま小さくする方法 */
.logo {
  width: 256px;
  height: 30px;
}
.headerContainer {
  display: flex;
  justify-content: space-between;
}

a {
  color: inherit;
  text-decoration: none;
}

.menu {
  list-style: none;
  display: flex;

  &__link {
    display: inline-block;
    margin-right: 30px;
    position: relative;
  }
}
</style>
