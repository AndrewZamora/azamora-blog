<template>
  <div class="container">
    <header>
      <h1>
        <nuxt-link to="/home">Some Title</nuxt-link>
      </h1>
    </header>
    <aside class="home-aside">
      <p>
        I'm Andrew Zamora a Web Developer from California. This is my blog where
        I write about programming.
      </p>
    </aside>
    <main>
      <blog-excerpt
        v-for="(excerpt, index) in excerpts"
        :key="index"
        :excerpt="excerpt"
      />
    </main>
  </div>
</template>

<script>
import BlogExcerpt from '../components/BlogExcerpt'
export default {
  components: {
    BlogExcerpt
  },
  data() {
    return {
      excerpts: [
        {
          title: 'this is a test',
          date: 'april 12, 2020',
          description:
            'lorem ipsum, dolor sit amet consectetur adipisicing elit. praesentium error dolor velit, ea atque cumque.'
        },
        {
          title: 'this is a test',
          date: 'april 12, 2020',
          description:
            'lorem ipsum, dolor sit amet consectetur adipisicing elit. praesentium error dolor velit, ea atque cumque.'
        }
      ]
    }
  },
  methods: {}
}
</script>

<style>
a {
  text-decoration: none;
  color: inherit;
}

h1 {
  text-align: center;
}

main {
  display: flex;
  flex-direction: column;
  max-width: 50rem;
  margin: 0 auto;
}

.home-aside {
  max-width: 50rem;
  margin: 0 auto;
}
.container {
  margin: 0 auto;
  min-height: 100vh;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
