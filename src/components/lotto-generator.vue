<template>
    <div class="container">    
        <h1>{{title}}</h1>       
        <div class="submit">
         <button @click="generate(6, 1, 42);">Generate Numbers</button>      
       </div>
       <div id="numbers"></div>
    </div>
</template>
    
<script>    
      export default {
        data(){
             return{
              title:'My Lotto Generator',             
          }        
        },
        methods: {
         generate(size,lowest,highest){
               var numbers = [];
               for(var i = 0; i < size; i++) {var add = true;var randomNumber = Math.floor(Math.random() * highest) + 1;
		for(var y = 0; y < highest; y++) {
			if(numbers[y] == randomNumber) {
				add = false;}}
        if(add) {
			numbers.push(randomNumber);
		} else {
			i--;
		}
	}

var highestNumber = 0;
	for(var m = 0; m < numbers.length; m++) {
		for(var n = m + 1; n < numbers.length; n++) {
			if(numbers[n] < numbers[m]) {
				highestNumber = numbers[m];
				numbers[m] = numbers[n];
				numbers[n] = highestNumber;
			}
		}
	} 
	document.getElementById("numbers").innerHTML = numbers.join("    ");

          }
        }
      }
           
</script>    
<style lang="css">

h1{
    margin-top: -200px;
    margin-bottom: 40px;
    font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif ;
}

button{
    padding-top: 10px;
    padding-bottom: 10px;
    padding-left: 10px;
    padding-right: 10px;
    border-radius: 5px;
    cursor:pointer;
}

.submit{
  margin-bottom:10px;
}

button:hover{
  background:#999;
  color:#fff;
}
#numbers{
  font-size:21px;
  color:black;
  font-family:'Times New Roman', Times, serif;
}

</style>

