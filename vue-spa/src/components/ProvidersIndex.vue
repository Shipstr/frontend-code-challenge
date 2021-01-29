<template>
  <div>
    <h1>Rates</h1>
    <ul>
      <li class="title">
        <div>Company Name</div>
        <div>Total</div>
      </li>
      <li v-for="p in providers" :key="p.name">
        <div>{{ p.name }}</div>
        <div>{{ p.rate.total }} {{ p.rate.currency }}</div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'ProvidersIndex',
  data () {
    return {
      providers: [
        {
          name: 'company name',
          rate: {
            total: 100,
            currency: 'USD'
          }
        }
      ]
    }
  },
  methods: {}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: flex;
  justify-content: space-between;
  margin: 0 10px;
}

.title {
  font-weight: bold;
  border-bottom: 1px solid #c0c0c0;
  margin-bottom: 10px;
  text-transform: uppercase;
}
</style>
