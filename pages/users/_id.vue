<template>
  <section>
    <h1>{{ message }}</h1>
    <p>id: {{ this.$route.params.id }}</p>
  </section>  
</template>

<script>
export default {
  data: function() {
    return {
      message: '/users/_id.vue を表示中'
    }
  },
  validate({ params }) {
    // testメソッドはjavascriptのメソッド（この例では、正規表現のパターンにマッチしているか検証している）
    return /^\d+$/.test(params.id)
  }
}
</script>