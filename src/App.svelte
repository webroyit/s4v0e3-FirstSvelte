<script>
	import Navbar from './Navbar.svelte';

	// variables
	let name = "Roy";
	let points = 100;
	let showControls = false;

	const addPoint = () => (points += 1);
	const removePoint = () => (points -= 1);
	const toggleControls = () => (showControls = !showControls);
</script>

<style>
	h1{
		color: #1b11a5;
	}

	h3{
		margin-bottom: 1rem;
	}
</style>

<Navbar />
<div class="container">
	<div class="card">
		<h1>
			{name}
			<button class="btn btn-sm" on:click={toggleControls}>
				{#if showControls}Hide{:else}Show{/if}
			</button>
		</h1>
		<h3>Points: {points}</h3>

		{#if showControls}
			<button class="btn" on:click={addPoint}>+1</button>
			<button class="btn btn-dark" on:click={removePoint}>-1</button>
			<!-- bind:value for two way binding -->
			<input type="number" bind:value={points} />
		{/if}
	</div>
</div>