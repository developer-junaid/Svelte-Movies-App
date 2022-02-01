<script>
	export async function load({ fetch, params }) {
		console.log('Params: ', params);
	}
</script>

<nav>
	<a href="/">Movie Database</a>
</nav>

<style>
	nav {
		display: flex;
		min-height: 10vh;
		align-items: center;
		justify-content: center;
	}

	a {
		font-size: 1rem;
		font-weight: bold;
		font-family: 'Poppins';
		color: black;
		text-decoration: none;
	}
</style>
