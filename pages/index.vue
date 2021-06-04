<template>
  <div>
    <p>{{ info }}</p>
  </div>
</template>

<script>
  export default {
    async asyncData({ $http }) {
      const info = await $http.$get(`https://covid-api.mmediagroup.fr/v1//cases?country=Brazil`)
      return { info }
    }
  }
</script>