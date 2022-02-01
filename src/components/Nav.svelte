<script>
	import { goto } from '$app/navigation';

	function redirectToHome() {
		goto('/');
	}
</script>

<nav>
	<h2 on:click={redirectToHome}>Movie Database</h2>
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
