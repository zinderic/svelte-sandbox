<script context="module" lang="ts">
	export const prerender = true;
	export const movies = [
		{
			"Name": "Morbius",
			"Poster": "https://www.themoviedb.org/t/p/w600_and_h900_bestv2/6JjfSchsU6daXk2AKX8EEBjO3Fm.jpg"
		},
	]
	
</script>

<svelte:head>
	<title>Movies</title>
</svelte:head>

<h1>Movies:</h1>

<article class="movies">
	<div class="movie">
		{#each movies as movie }
			<p>{movie.Name}</p>
			<img src={movie.Poster} alt=""/>
		{/each}
	</div>
</article>

<style>
	/* TODO fix the poster size by wrapping it in something */
	.movies {
		display: flex;
		margin: auto;
	}
	.movie {
		display: grid;
		grid-template-columns: 2rem 1fr 2rem;
		grid-gap: 0.5rem;
		align-items: center;
		margin: 0 0 0.5rem 0;
		padding: 0.5rem;
		background-color: white;
		border-radius: 8px;
		filter: drop-shadow(2px 4px 6px rgba(0, 0, 0, 0.1));
		transform: translate(-1px, -1px);
		transition: filter 0.2s, transform 0.2s;
	}
</style>