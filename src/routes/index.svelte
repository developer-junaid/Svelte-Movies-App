<script context="module">
	// API requests here
	export async function load({ fetch }) {
		const res = await fetch(
			`https://api.themoviedb.org/3/movie/popular/?api_key=${import.meta.env.VITE_API}`
		);

		const data = await res.json();

		if (res.ok) {
			return {
				// These will be available everywhere
				props: { popular: data.results }
			};
		}
	}
</script>

<script>
	import PopularMovies from '../components/PopularMovies.svelte';
	import SearchMovies from '../components/SearchMovies.svelte';
	import global from '../global.css';
	import { fly } from 'svelte/transition';
	// The prop from the module
	export let popular;
</script>

<section in:fly={{ y: 50, duration: 500 }} out:fly={{ duration: 500 }}>
	<SearchMovies />
	<PopularMovies {popular} />
</section>
