<template>
  <div class="img-container">
    <a
      class="img-link"
      :href="href"
      target="_blank"
      rel="noopener noreferrer"
      :aria-label="name + ' Link'"
    >
      <img class="img" border="0" :alt="name" :src="img" />
    </a>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: {
    name: {
      type: String,
      default: '',
    },
    href: {
      type: String,
      default: '',
    },
    img: {
      type: String,
      default: '',
    },
  },
})
</script>

<style>
.img-container {
  display: flex;
  justify-content: center;
  margin-bottom: 3rem;
}
.img-link {
  width: 50%;
  max-width: 500px;
}
.img {
  width: 100%;
}
</style>
