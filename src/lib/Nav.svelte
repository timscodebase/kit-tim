<script>
  import { page } from '$app/stores';
</script>

<nav>
  <ul>
    <li class:active={$page.path === '/'}><a sveltekit:prefetch href="/">Home</a></li>
    <li class:active={$page.path === '/about'}><a sveltekit:prefetch href="/about">About</a></li>
    <li class:active={$page.path === '/work'}><a sveltekit:prefetch href="/work">Work</a></li>
    <li class:active={$page.path === '/uses'}><a sveltekit:prefetch href="/uses">Uses</a></li>
  </ul>
</nav>

<style>
  nav {
		display: flex;
		justify-content: center;
	}

	ul {
    height: 100%;
		position: relative;
		padding: 0;
		margin: 0;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
	}

	li {
		position: relative;
		height: 100%;
	}

	li.active {
    animation: pulse 0.21s ease-in-out infinite alternate;
  }

	a {
		display: grid;
		height: 100%;
		place-items: center;
		color: var(--foreground);
    padding: 0 1rem;
    font-size: 1.75rem;
    font-variant: small-caps;
    font-family: 'M PLUS Rounded 1c', sans-serif;
	  font-weight: 700;
	}

	a:hover {
    animation: pulse 0.21s ease-in-out infinite alternate;
	}

  @keyframes pulse {
    100% {
      text-shadow:
      0 0 4px var(--neon-2),
      0 0 11px var(--neon-2),
      0 0 19px var(--neon-2),
      0 0 40px var(--neon);
    }
    0% {
      text-shadow:
      0 0 4px var(--neon-2),
      0 0 10px var(--neon-2),
      0 0 18px var(--neon-2),
      0 0 38px var(--neon-2);
    }
  }
</style>