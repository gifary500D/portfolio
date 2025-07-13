<script>
	import { onMount } from 'svelte';

	let visible = false;
	let typedText = '';
	const fullText = 'Web Developer & Fotografer';

	onMount(() => {
		visible = true;

		function startTyping() {
			let i = 0;
			typedText = '';
			const typeInterval = setInterval(() => {
				if (i < fullText.length) {
					typedText += fullText.charAt(i);
					i++;
				} else {
					clearInterval(typeInterval);
					// Restart animasi ketik setelah 2 detik
					setTimeout(startTyping, 2000);
				}
			}, 100);
		}

		startTyping();
	});
</script>

<svelte:head>
	<title>Muhammad Gifary - Portfolio</title>
	<meta
		name="description"
		content="Portfolio pribadi Muhammad Gifary - Web Developer & Fotografer"
	/>
</svelte:head>

<!-- Hero Section -->
<section class="relative flex min-h-screen items-center justify-center overflow-hidden">
	<!-- Animated Background -->
	<div class="absolute inset-0 opacity-10">
		<div
			class="absolute top-10 left-10 h-72 w-72 animate-pulse rounded-full bg-cyan-500 mix-blend-multiply blur-xl filter"
		></div>
		<div
			class="animation-delay-2000 absolute top-40 right-20 h-72 w-72 animate-pulse rounded-full bg-purple-500 mix-blend-multiply blur-xl filter"
		></div>
		<div
			class="animation-delay-4000 absolute bottom-20 left-20 h-72 w-72 animate-pulse rounded-full bg-pink-500 mix-blend-multiply blur-xl filter"
		></div>
	</div>

	<div class="relative z-10 container mx-auto px-4 text-center">
		<div class="mx-auto max-w-4xl">
			<h1
				class="mb-6 text-5xl font-bold md:text-7xl"
				class:animate-fade-in-up={visible}
				class:opacity-0={!visible}
			>
				Halo, saya <span
					class="bg-gradient-to-r from-cyan-400 to-purple-600 bg-clip-text text-transparent"
					>Muhammad Gifary</span
				>
			</h1>

			<!-- Efek ketik untuk profesi -->
			<p
				class="mb-8 h-8 text-xl font-semibold tracking-widest text-gray-300 uppercase md:text-2xl"
				class:animate-fade-in-up={visible}
				class:animation-delay-500={visible}
				class:opacity-0={!visible}
			>
				{typedText}<span class="animate-pulse">|</span>
			</p>

			<p
				class="mx-auto mb-12 max-w-2xl text-lg text-gray-400"
				class:animate-fade-in-up={visible}
				class:animation-delay-1000={visible}
				class:opacity-0={!visible}
			>
				Saya mahasiswa Sistem Informasi yang suka mengembangkan aplikasi web dan mengambil gambar
				dengan perspektif yang indah. Menggabungkan teknologi dan seni dalam karya digital.
			</p>

			<div
				class="flex flex-col justify-center gap-4 sm:flex-row"
				class:animate-fade-in-up={visible}
				class:animation-delay-1500={visible}
				class:opacity-0={!visible}
			>
				<a
					href="/contact"
					class="rounded-full border-2 border-cyan-400 px-8 py-3 font-semibold text-cyan-400 transition-colors hover:bg-cyan-400 hover:text-gray-900"
					>Hubungi Saya</a
				>
			</div>
		</div>
	</div>

	<div class="absolute bottom-8 left-1/2 -translate-x-1/2 transform animate-bounce">
		<svg class="h-6 w-6 text-cyan-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
			<path
				stroke-linecap="round"
				stroke-linejoin="round"
				stroke-width="2"
				d="M19 14l-7 7m0 0l-7-7m7 7V3"
			/>
		</svg>
	</div>
</section>

<!-- Quick About Section -->
<section class="bg-gray-800/50 py-20">
	<div class="container mx-auto px-4">
		<div class="mx-auto max-w-4xl text-center">
			<h2 class="mb-8 text-3xl font-bold md:text-4xl">Tentang Saya</h2>
			<p class="mb-8 text-lg text-gray-300">
				Saya senang membangun website modern, responsif, dan fungsional. Juga aktif dalam dunia
				fotografi yang artistik dan kreatif.
			</p>
			<div class="grid grid-cols-1 gap-8 md:grid-cols-3">
				<div class="rounded-lg bg-gray-700/50 p-6 transition-colors hover:bg-gray-700">
					<div
						class="mx-auto mb-4 flex h-12 w-12 items-center justify-center rounded-lg bg-cyan-500"
					>
						<svg class="h-6 w-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"
							/>
						</svg>
					</div>
					<h3 class="mb-2 text-xl font-semibold">Web Development</h3>
					<p class="text-gray-400">Membangun website yang interaktif dan responsif</p>
				</div>

				<div class="rounded-lg bg-gray-700/50 p-6 transition-colors hover:bg-gray-700">
					<div
						class="mx-auto mb-4 flex h-12 w-12 items-center justify-center rounded-lg bg-pink-500"
					>
						<svg class="h-6 w-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"
							/>
						</svg>
					</div>
					<h3 class="mb-2 text-xl font-semibold">Fotografi</h3>
					<p class="text-gray-400">Menangkap momen dengan perspektif dan pencahayaan yang tepat</p>
				</div>

				<div class="rounded-lg bg-gray-700/50 p-6 transition-colors hover:bg-gray-700">
					<div
						class="mx-auto mb-4 flex h-12 w-12 items-center justify-center rounded-lg bg-purple-500"
					>
						<svg class="h-6 w-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M5 12h14M5 12a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v4a2 2 0 01-2 2M5 12a2 2 0 00-2 2v4a2 2 0 002 2h14a2 2 0 002-2v-4a2 2 0 00-2-2m-2-4h.01M17 16h.01"
							/>
						</svg>
					</div>
					<h3 class="mb-2 text-xl font-semibold">UI/UX Design</h3>
					<p class="text-gray-400">Mendesain antarmuka yang estetik dan ramah pengguna</p>
				</div>
			</div>
		</div>
	</div>
</section>

<style>
	@keyframes fade-in-up {
		from {
			opacity: 0;
			transform: translateY(30px);
		}
		to {
			opacity: 1;
			transform: translateY(0);
		}
	}
	.animate-fade-in-up {
		animation: fade-in-up 0.6s ease-out forwards;
	}
	.animation-delay-500 {
		animation-delay: 0.5s;
	}
	.animation-delay-1000 {
		animation-delay: 1s;
	}
	.animation-delay-1500 {
		animation-delay: 1.5s;
	}
	.animation-delay-2000 {
		animation-delay: 2s;
	}
	.animation-delay-4000 {
		animation-delay: 4s;
	}
</style>
