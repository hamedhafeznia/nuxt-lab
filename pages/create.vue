<template>
  <div>
    <h1>
      Create
      <nuxt-link to="/">Home page</nuxt-link>
    </h1>
  </div>
</template>

<script>
export default {
  head() {
    return {
        title: 'Create a new one',
        meta: [
            {
                hid: 'description',
                name: 'description',
                content: 'This is create page'

            }
        ]
    }
  },
};
</script>
