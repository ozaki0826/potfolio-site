<template>
  <header class="main-header">
    <h1 class="main-title"><a href="/">ozaki's portfolio</a></h1>
  </header> 
</template>

<style lang="scss" scoped>
.main-header {
  background: #333;
}

.main-title {
  padding: 17px 16px;
  font-size: 18px;
  max-width: 896px;
  margin: 0 auto;
  & a {
    color: #fff;
    text-decoration: none;
    &:hover {
      opacity: 0.8;
    }
  }
}
</style>