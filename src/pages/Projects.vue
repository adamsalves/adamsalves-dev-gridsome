<template>
  <Layout :show-logo="true">
    <!-- Author intro -->
    <Author :show-title="true" />

  </Layout>
</template>

<script>
import Author from '~/components/Author.vue'

export default {
  components: {
    Author
  },
  metaInfo: {
    title: 'Projetos'
  }
}
</script>
