    <template>
      <nuxt-link :to="'/event/' + event.id">
        <div class="-shadow">
          <span class="eyebrow">
          {{ event.completed ? 'Completed' : 'Not completed' }}
          </span>
          <h4 class="title">
            {{ event.title }}
          </h4>
          
        </div>
      </nuxt-link>
    </template>
    <script>
    export default {
      name: 'EventCard',
      props: {
        event: Object
      },
    }
    </script>
    <style scoped>
    div {
      padding: 20px;
      margin-bottom: 24px;
      transition: all 0.2s linear;
      cursor: pointer;
      box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2), 0 1px 15px 0 rgba(0, 0, 0, 0.19);
    }
    div:hover {
      transform: scale(1.01);      
    }
    .title {
      margin: 0;
      color: lightblue;
      
    }
    a {
      text-decoration: none;
    }
    </style>