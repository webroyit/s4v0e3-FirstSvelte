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
</style>

<div class="container">
	<div class="card">
		<h1>Hello {name}!</h1>
		<h3>{points}</h3>
		<button class="btn" on:click={addPoint}>+1</button>
		<button class="btn btn-dark" on:click={removePoint}>-1</button>
	</div>
</div>