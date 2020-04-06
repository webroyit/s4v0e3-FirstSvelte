<script>
	import Navbar from './Navbar.svelte';
	import Player from './Player.svelte';

	let players = [
		{
			name: "Roy Web",
			points: 100
		},
		{
			name: "Mike Doe",
			points: 88
		},
		{
			name: "Jill Smith",
			points: 91
		}
	];

</script>

<Navbar />
<div class="container">
	{#if players.length === 0}
		<p>No Players yet</p>
	{:else}
		{#each players as player}
			<Player />
		{/each}
	{/if}
</div>