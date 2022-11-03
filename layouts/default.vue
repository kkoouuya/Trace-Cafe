<template>
  <div class="wapper">
    <Header class="header" />
    <slot class="main" />
    <Footer />
  </div>
</template>
<style lang="scss" scoped>
.header {
  //   position: fixed;
  z-index: 100;
}
</style>
