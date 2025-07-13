<!-- src/routes/+layout.svelte -->
<script>
	import '../app.css';
	import { page } from '$app/stores';
	import { onMount } from 'svelte';

	let isMenuOpen = false;
	let scrollY = 0;

	onMount(() => {
		const handleScroll = () => (scrollY = window.scrollY);
		window.addEventListener('scroll', handleScroll);
		return () => window.removeEventListener('scroll', handleScroll);
	});

	const toggleMenu = () => {
		isMenuOpen = !isMenuOpen;
	};

	const closeMenu = () => {
		isMenuOpen = false;
	};
</script>

<svelte:window bind:scrollY />

<nav
	class="fixed top-0 right-0 left-0 z-50 transition-all duration-300 {scrollY > 50
		? 'bg-gray-900/95 shadow-lg backdrop-blur-md'
		: 'bg-transparent'}"
>
	<div class="container mx-auto px-4 sm:px-6 lg:px-8">
		<div class="flex h-16 items-center justify-between">
			<a href="/" class="text-2xl font-bold text-white transition-colors hover:text-cyan-400">
				Muhammad Gifary
			</a>

			<!-- Desktop Menu -->
			<div class="hidden space-x-8 md:flex">
				<a
					href="/"
					class="text-white transition-colors hover:text-cyan-400 {$page.url.pathname === '/'
						? 'text-cyan-400'
						: ''}">Home</a
				>
				<a
					href="/about"
					class="text-white transition-colors hover:text-cyan-400 {$page.url.pathname === '/about'
						? 'text-cyan-400'
						: ''}">About</a
				>

				<a
					href="/contact"
					class="text-white transition-colors hover:text-cyan-400 {$page.url.pathname === '/contact'
						? 'text-cyan-400'
						: ''}">Contact</a
				>
			</div>
			<!-- Tombol menu mobile -->
			<button class="text-white md:hidden" on:click={toggleMenu} aria-label="Toggle Menu">
				<svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
					<path
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						d="M4 6h16M4 12h16M4 18h16"
					/>
				</svg>
			</button>

			<!-- Mobile Menu -->
			{#if isMenuOpen}
				<div class="bg-gray-900/95 backdrop-blur-md md:hidden">
					<div class="space-y-1 px-2 pt-2 pb-3">
						<a
							href="/"
							class="block px-3 py-2 text-white transition-colors hover:text-cyan-400"
							on:click={closeMenu}>Home</a
						>
						<a
							href="/about"
							class="block px-3 py-2 text-white transition-colors hover:text-cyan-400"
							on:click={closeMenu}>About</a
						>
						<a
							href="/contact"
							class="block px-3 py-2 text-white transition-colors hover:text-cyan-400"
							on:click={closeMenu}>Contact</a
						>
					</div>
				</div>
			{/if}
		</div>
	</div>
</nav>

<main class="min-h-screen">
	<slot />
</main>

<footer class="bg-gray-900 py-8 text-white">
	<div class="container mx-auto px-4 text-center">
		<p>&copy; 2025 Muhammad Gifary. All rights reserved.</p>
		<div class="mt-4 flex justify-center space-x-6">
			<a href="https://github.com/gifary500D" class="transition-colors hover:text-cyan-400"
				>GitHub</a
			>
			<a href="mailto:gifary024@example.com" class="transition-colors hover:text-cyan-400">Email</a>
		</div>
	</div>
</footer>

<style>
	:global(body) {
		margin: 0;
		font-family:
			'Inter',
			-apple-system,
			BlinkMacSystemFont,
			'Segoe UI',
			Roboto,
			sans-serif;
		background: linear-gradient(135deg, #0f172a 0%, #1e293b 100%);
		color: white;
	}

	:global(html) {
		scroll-behavior: smooth;
	}

	:global(*) {
		box-sizing: border-box;
	}
</style>
