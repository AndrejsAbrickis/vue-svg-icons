<template>
  <span>
    <img :src="src" />
  </span>
</template>

<script>
export default {
  props: {
    name: String
  },
  computed: {
    src() {
      return require(`../assets/iconmonstr-${this.name}.svg`);
    }
  }
};
</script>
