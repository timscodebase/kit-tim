<script>
	import { page } from '$app/stores';
</script>

<h1 class:active={$page.path === '/'}>SmithDesign</h1>

<style>
	h1 {
		font-size: 5rem;
		font-variant: small-caps;
		margin: 0;
		padding: 0;
		text-shadow: 0 0 4px var(--neon-2), 0 0 10px var(--neon-2), 0 0 18px var(--neon-2),
			0 0 38px var(--neon-2), 0 0 73px var(--neon-2);
	}

	.active {
		animation: pulse 0.21s ease-in-out infinite alternate;
	}

	@keyframes pulse {
		100% {
			text-shadow: 0 0 4px var(--neon-2), 0 0 11px var(--neon-2), 0 0 19px var(--neon-2),
				0 0 40px var(--neon), 0 0 80px var(--neon);
		}
		0% {
			text-shadow: 0 0 4px var(--neon-2), 0 0 10px var(--neon-2), 0 0 18px var(--neon-2),
				0 0 38px var(--neon-2), 0 0 73px var(--neon-2);
		}
	}
</style>
