<script>
	import { pokéPage } from './title';
	let radNumber = 31;
	let radDude = `${radNumber} Dude this is rad`;
	let svltTag = '#svelte';
	console.log('Rad Pokedex!');

	const salutationsObj = {
		 salutation: "Hey there!",
		 name: "Friend"
	};

	const rgb = ['red', 'green', 'blue'];
</script>

<div class="header">
	<h1>Welcome to {pokéPage}</h1>
	<h3 class="salutations">{salutationsObj.salutation} Nice of you to drop by, {salutationsObj.name}!</h3>
	<h4>{radDude} <a href="https://kit.svelte.dev" target="_blank" rel="noreferrer">{svltTag}</a></h4>
	{#each rgb as color, i (color)}
		<h3>{i}: {color.toUpperCase()}</h3>
	{/each}
</div>

<style>
	h1 {
		color: papayawhip;
	}

	.salutations {
		color: aqua;
	}
</style>
