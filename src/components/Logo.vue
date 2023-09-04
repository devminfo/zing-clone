<template>
  <span></span>
</template>

<style lang="scss" scoped>
@import '~/assets/scss/mixin.scss';

span {
  @include logo-small;

  @screen md {
    @include logo-medium;
  }
}
</style>
