<template>
  <div class="container">
    <div>
      <h2 class="title">
        FIBONACCI
      </h2>
      <b-img src="/logo.png" fluid alt="Logo"></b-img>

      <h3 class="subtitle mt-4">
        Obten el número inmediato de la serie de Fibonacci
      </h3>
      <fibo/>
      
    </div>
  </div>
</template>

<script>

import fibo from '@/components/fibonacci.vue'
export default {
  components:{
    fibo
  }
}
</script>

