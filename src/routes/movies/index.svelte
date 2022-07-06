<script context="module" lang="ts">
	export const prerender = true;
	export const movies = [
		{
			"Name": "Morbius",
			"Poster": "https://www.themoviedb.org/t/p/w600_and_h900_bestv2/6JjfSchsU6daXk2AKX8EEBjO3Fm.jpg"
		},
		{
			"Name": "Top Gun Maverick",
			"Poster": "https://www.themoviedb.org/t/p/w1280/kqVncEM5t00mbaNR0UB1iAz7nOi.jpg"
		},
		{
			"Name": "The Ledge",
			"Poster": "https://www.themoviedb.org/t/p/w1280/dHKfsdNcEPw7YIWFPIhqiuWrSAb.jpg"
		},
		{
			"Name": "Dark Cloud",
			"Poster": "https://www.themoviedb.org/t/p/w1280/q1ngkvPCnOYKeyNZjg8QqvaSnuZ.jpg"
		},
		{
			"Name": "Heatwave",
			"Poster": "https://www.themoviedb.org/t/p/w1280/AeeXeyiiPOyybnjSnJoSTixOZQq.jpg"
		}
	]
	
</script>

<svelte:head>
	<title>Movies</title>
</svelte:head>

<h1>Movies:</h1>

<article class="movies">
	<div class="movie">
		{#each movies as movie }
		<div>
			<p>{movie.Name}</p>
			<img src={movie.Poster} alt=""/>
		</div>
		{/each}
	</div>
</article>

<style>
	.movies {
		display: flex;
		flex-direction: row;
		flex-flow: column wrap;
	}
	.movie {
		display: grid;
		grid-template-columns: 0.5fr 0.5fr 0.5fr;
		grid-gap: 0.5rem;
		align-items: baseline;
		margin: 0 0 0.5rem 0;
		padding: 0.5rem;
		background-color: white;
		border-radius: 8px;
		filter: drop-shadow(2px 4px 6px rgba(0, 0, 0, 0.1));
		transform: translate(-1px, -1px);
		transition: filter 0.2s, transform 0.2s;
	}
	.movie img {
		height: 15rem;
	}
</style>