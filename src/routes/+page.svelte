<script>
	import { pokéPage } from './title';
	import { generations } from './generations';
</script>

<div class="header">
	<h1>Welcome to {pokéPage}</h1>
	<div>
		{#each generations as generation (generation.id)}
			<div>
				<h2>{generation.name}</h2>
				<p>Region: {generation.main_region}</p>
				<p>Games: {generation.games.join(', ')}</p>
			</div>
		{/each}
	</div>
</div>

<style>
	h1 {
		color: papayawhip;
	}
</style>
