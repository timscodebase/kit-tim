<script>
	import { page } from '$app/stores';
	import Logo from '$lib/Logo.svelte';
	import Nav from '$lib/Nav.svelte';
</script>

{#if $page.path === '/'}
	<header class="wrapper home">
		<Logo />
		<Nav />
	</header>
{:else}
	<header class="wrapper not-home">
		<Logo />
		<Nav />
	</header>
{/if}

<style>
	.home {
		height: 80vh;
		display: flex;
		flex-direction: column;
		justify-content: center;
	}

	.not-home {
		display: flex;
		justify-content: space-between;
		padding-left: 2rem;
	}
</style>
