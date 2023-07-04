<script>
	let principal = 0;
	let rate = 0;
	let time = 0;
	let result = 0;
  
	function calculate() {
	  const calculatedRate = 1 + rate / 100;
	  result = principal * Math.pow(calculatedRate, time);
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
	  <input type="number" id="rate" bind:value="{rate}" />
	</div>
  
	<div class="receber">
	  <label for="time">Tempo (anos):</label>
	  <input type="number" id="time" bind:value="{time}" />
	</div>
  
	<button on:click="{calculate}"><svg xmlns="http://www.w3.org/2000/svg" width="26" height="26" fill="currentColor" class="bi bi-play-fill" viewBox="0 0 16 16">
		<path d="m11.596 8.697-6.363 3.692c-.54.313-1.233-.066-1.233-.697V4.308c0-.63.692-1.01 1.233-.696l6.363 3.692a.802.802 0 0 1 0 1.393z"/>
	  </svg></button>
  
	{#if result}
	  <div class="result">
		<p>O valor total é: {result.toFixed(2)}</p>
	  </div>
	{/if}

	<p class="group">BY: ELISON, ARTHUR, RUAN LUIZ.</p>
  </div>
  
