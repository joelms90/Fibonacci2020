<template>
	<div>
		<b-form-input type="number" v-model="number" placeholder="Ingresa un número entero"></b-form-input>
		<h2 v-show="result!=null" v-bind:class="{myresult:result!=null}">
        El número de la serie es: {{result}}
      	</h2>
		<h2 v-show="error!=null" v-bind:class="{myerror:error!=null}">
        {{error}}
      	</h2>
		
		<div class="links">
	        <button  class="button--blue" @click="getFibo()">
	          Calcular
	        </button>
      	</div>
	</div>
</template>
<script>
var fib = function(n) {
  if (isFibonacci(n)){
    return n
  }
  else{
  	return fib(n-1)
  }
};

var isPerfectSquare= function(x) 
{ 
    var s = Math.sqrt(x); 
    return (s%1== 0); 
} 
  

var isFibonacci= function(n) 
{ 
    return isPerfectSquare((5*n*n) + 4) ||
           isPerfectSquare((5*n*n) - 4); 
} 
  

	export default{
		data() {
	      return {
	        number: null,
	        result:null,
	        error:null,
	      }
	    },
	    methods:{
	    	getFibo(){
	    		let temp=this.number
	    		if(temp%1 != 0&&temp!=null||temp==null||temp===""||temp<0)
	    		{
	    		this.error='Por favor ingrese un número entero'
	    		this.result=null
	    		}
	    		else{
	    			this.error=null
	    			if(isFibonacci(temp))
	    			{	
	    				console.log(isFibonacci(temp));
	    				this.result=temp

	    			}
	    			else{
	    				console.log(fib(temp));
	    				this.result= fib(temp)	
	    			}	
	    		
	    		}
	    	}
	    }

	}

</script>