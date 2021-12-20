<template>
  <div>
    <h1>
      event: {{event.title}}
    </h1>
  </div>
</template>

<script>
    export default {
        head() {
            return {
                title: 'Event #' + this.id,
                meta: [
                    {
                        hid: 'description',
                        name: 'description',
                        content: 'description number' + this.id

                    }
                ]
            }
        },

        async asyncData({ $axios, error, params }) {
            try {
            const response = await $axios.get(`https://jsonplaceholder.typicode.com/todos/${params.id}`);
            return {
                event: response.data
            }
            } catch(e) {
                console.log(e)
            }
        },

        computed: {
            id() {
                return this.$route.params.id
            }
        }
}
</script>