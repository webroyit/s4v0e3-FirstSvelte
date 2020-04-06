<script>
	// variables
	let name = "Roy";
	let points = 100;

	const addPoint = () => points += 1;
	const removePoint = () => points -= 1;
</script>

<style>
	h1{
		color: #1b11a5;
	}

	h3{
		margin-bottom: 1rem;
	}
</style>

<div class="container">
	<div class="card">
		<h1>Hello {name}!</h1>
		<h3>{points}</h3>
		<button class="btn" on:click={addPoint}>+1</button>
		<button class="btn btn-dark" on:click={removePoint}>-1</button>
		<!-- bind:value for two way binding -->
		<input type="number" bind:value={points} />
	</div>
</div>