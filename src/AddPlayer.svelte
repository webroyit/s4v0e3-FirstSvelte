<script>
    let player = {
        name: "",
        points: 0,
    }
</script>

<form class="grid-3">
    <input type="text" placeholder="Name" bind:value={player.name}>
    <input type="number" placeholder="Points" bind:value={player.points}>
    <input type="submit" class="btn btn-primary" value="Add Player">
</form>