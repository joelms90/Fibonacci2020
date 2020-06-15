<template>
	<div>
		  <b-form-input v-model="number" placeholder="Ingresa un número entero"></b-form-input>
		  <div class="links">
        <button
          
          class="button--blue"
        >
         
          Calcular
        </button>
      
      </div>
		  
	</div>
</template>
<script>
	export default{
		data() {
	      return {
	        number: null
	      }
	    },
	    methods:{

	    }

	}

</script>