<template>
  <article>
    <header>
      <h3>
        <nuxt-link to="`blog/${excerpt.slug}`">{{ excerpt.title }}</nuxt-link>
      </h3>
      <p>
        <small>{{ excerpt.date }}</small>
      </p>
    </header>
    <p>{{ excerpt.description }}</p>
  </article>
</template>

<script>
export default {
  props: {
    excerpt: { type: Object, required: true }
  }
}
</script>

<style scoped>
header h3 {
  text-align: left;
}
p {
  text-align: left;
  margin-bottom: 1em;
}
</style>
