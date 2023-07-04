<script>
	let principal = 0;
	let taxa = 0;
	let tempo = 0;
	let resultado = 0;
  
	function calcular() {
	  const calculatarTaxa = 1 + taxa / 100;
	  resultado = principal * Math.pow(calculatarTaxa, tempo);
	}
  </script>
  
  <div class="container">
	<h1>Calculadora de Juros Composto</h1>
  
	<div class="receber">
	  <label for="principal">Principal:</label>
	  <input type="number" id="principal" bind:value="{principal}" />
	</div>
  
	<div class="receber">
	  <label for="rate">Taxa de Juros (%):</label>
	  <input type="number" id="rate" bind:value="{taxa}" />
	</div>
  
	<div class="receber">
	  <label for="time">Tempo (anos):</label>
	  <input type="number" id="time" bind:value="{tempo}" />
	</div>
  
	<button on:click="{calcular}"><svg xmlns="http://www.w3.org/2000/svg" width="26" height="26" fill="currentColor" class="bi bi-play-fill" viewBox="0 0 16 16">
		<path d="m11.596 8.697-6.363 3.692c-.54.313-1.233-.066-1.233-.697V4.308c0-.63.692-1.01 1.233-.696l6.363 3.692a.802.802 0 0 1 0 1.393z"/>
	  </svg></button>
  
	{#if resultado}
	  <div class="result">
		<p>O valor total é: {resultado.toFixed(2)}</p>
	  </div>
	{/if}

	<p class="group">BY: ELISON, ARTHUR, RUAN LUIZ.</p>
  </div>
  
