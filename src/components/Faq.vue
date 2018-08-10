<template>
  <div class="faq">
    <div class="container">
      <section class="section">
        <h1 class="title">FAQ</h1>
        <h2 class="subtitle is-4">THIS IS OUR FAQ PAGE</h2>

        <div class="columns" v-if="faqs && faqs.lenght">
          <div class="column is-one-third" v-for="faq in faqs" :key="faq.title">
            <div class="card">
              <div class="card-content">
                <p class="title">{{ faq.title }}</p>
                <p class="answer">{{ faq.body }}</p>
              </div>
            </div>
          </div>
        </div>

      </section>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'faq',
  data: () => ({
    faqs: [],
    errors: []
  }),

  created() {
    axios.get('http://jsonplaceholder.typicode.com/posts')
      .ten(response => {
        this.faqs = response.data.slice(0, 10);
      })
      .catch(e =>  {
        this.errors.push(e)
      })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
@import '../mq'


</style>
