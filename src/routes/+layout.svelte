<script>
	import { page } from '$app/stores';

	$page;
	const navList = [
		{
			id: '/colors',
			label: 'Colors'
		},
		{
			id: '/typography',
			label: 'Typography'
		},
		{
			id: '/spaces',
			label: 'Spaces'
		},
		{
			id: '/buttons',
			label: 'Buttons'
		},
		{
			id: '/inputs',
			label: 'Inputs'
		},
		{
			id: '/grid',
			label: 'Grid'
		}
	];
</script>

<main>
	<nav>
		<a class="nav-brand" href="/"><span>Dev</span><span>challenges.io</span></a>
		{#each navList as nav (nav.id)}
			<a class="nav-link" class:active={nav.id === $page.url.pathname} href={nav.id}>{nav.label}</a>
		{/each}
	</nav>
	<section>
		<article>
			<slot />
		</article>
		<footer>Created by iamvishal345 - devChallenges.io</footer>
	</section>
</main>

<style lang="scss">
	:global(*) {
		box-sizing: border-box;
	}
	:global(body) {
		margin: 0;
		padding: 0;
		font-family: 'Poppins', sans-serif;
	}
	nav {
		background-color: #fafbfd;
		padding: 3.5rem;
		display: flex;
		flex-direction: column;
		gap: 1.75rem;
		.nav-brand {
			text-decoration: none;
			font-weight: 700;
			color: #090f31;
			margin-bottom: 7rem;
			:first-child {
				color: #f7542e;
			}
		}
		.nav-link {
			text-decoration: none;
			color: #9e9e9e;
			font-size: 14px;
			&.active {
				color: #090f31;
				font-weight: 700;
			}
		}
	}
	main {
		min-height: 100vh;
		display: grid;
		grid-template-columns: 14.5rem auto;
	}

	section {
		padding: 3rem 5rem;
		display: flex;
		flex-direction: column;
	}

	footer {
		color: #a9a9a9;
		margin-top: auto;
	}
</style>
