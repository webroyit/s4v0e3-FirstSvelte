<script>
	import Navbar from './Navbar.svelte';
	import Player from './Player.svelte';
	import AddPlayer from './AddPlayer.svelte';

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

	const addPlayer = e => {
		// get the value from another component
		const newPlayer = e.detail;

		// merge the array with newPlayer data
		players = [newPlayer, ...players];
	};

</script>

<Navbar />
<div class="container">
	<AddPlayer on:addplayer={addPlayer} />
	{#if players.length === 0}
		<p>No Players yet</p>
	{:else}
		{#each players as player}
			<Player name={player.name} points={player.points} />
		{/each}
	{/if}
</div>