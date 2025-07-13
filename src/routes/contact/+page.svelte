<script>
	import { onMount } from 'svelte';

	let visible = false;

	const contactMethods = [
		{
			title: 'Email',
			value: 'gifary024@gmail.com',
			icon: '📧',
			href: 'mailto:gifary024@gmail.com'
		},
		{
			title: 'Phone',
			value: '+62 851 8274 8023',
			icon: '📱',
			href: 'tel:+6281234567890'
		},
		{
			title: 'Location',
			value: 'Binjai Timur, Sumatera Utara, Indonesia',
			icon: '📍',
			href: 'https://maps.google.com/?q=Binjai Timur, Sumatera Utara'
		}
	];

	const socialLinks = [
		{
			name: 'GitHub',
			url: 'https://github.com/gifary500D',
			icon: '🐙'
		},
		{
			name: 'Instagram',
			url: 'https://instagram.com/gif_ry02',
			icon: '📸'
		}
	];

	onMount(() => {
		visible = true;
	});
</script>

<svelte:head>
	<title>Contact - Muhammad Gifary</title>
	<meta
		name="description"
		content="Hubungi Muhammad Gifary untuk kolaborasi web development dan fotografi"
	/>
</svelte:head>

<section class="pt-24 pb-16">
	<div class="container mx-auto px-4">
		<div class="mx-auto max-w-6xl">
			<h1
				class="mb-8 text-center text-4xl font-bold md:text-5xl {visible
					? 'animate-fade-in-up'
					: 'opacity-0'}"
			>
				Contact <span
					class="bg-gradient-to-r from-cyan-400 to-purple-600 bg-clip-text text-transparent"
					>Me</span
				>
			</h1>

			<p
				class="mx-auto mb-16 max-w-3xl text-center text-xl text-gray-300 {visible
					? 'animate-fade-in-up animation-delay-500'
					: 'opacity-0'}"
			>
				Saya selalu terbuka untuk diskusi proyek baru, kolaborasi, atau sekadar ngobrol seputar web
				development dan fotografi.
			</p>

			<div class="grid grid-cols-1 gap-12 lg:grid-cols-2">
				<!-- Contact Information -->
				<div class="space-y-8 {visible ? 'animate-fade-in-up animation-delay-1000' : 'opacity-0'}">
					<div class="rounded-lg bg-gray-800/50 p-8">
						<h2 class="mb-6 text-2xl font-bold">Informasi Kontak</h2>
						<div class="space-y-6">
							{#each contactMethods as method}
								<a
									href={method.href}
									target="_blank"
									rel="noopener noreferrer"
									class="group flex items-center space-x-4 rounded-lg bg-gray-700/50 p-4 transition-colors hover:bg-gray-700"
								>
									<div class="text-2xl">{method.icon}</div>
									<div>
										<h3
											class="font-semibold text-white transition-colors group-hover:text-cyan-400"
										>
											{method.title}
										</h3>
										<p class="text-gray-300">{method.value}</p>
									</div>
								</a>
							{/each}
						</div>
					</div>

					<!-- Social Media -->
					<div class="rounded-lg bg-gray-800/50 p-8">
						<h2 class="mb-6 text-2xl font-bold">Follow Me</h2>
						<div class="flex space-x-4">
							{#each socialLinks as social}
								<a
									href={social.url}
									target="_blank"
									rel="noopener noreferrer"
									class="group flex items-center space-x-2 rounded-lg bg-gray-700/50 px-4 py-2 transition-colors hover:bg-gray-700"
								>
									<span class="text-xl">{social.icon}</span>
									<span class="text-gray-300 transition-colors group-hover:text-white"
										>{social.name}</span
									>
								</a>
							{/each}
						</div>
					</div>
				</div>

				<!-- Additional Info -->
				<div class="space-y-8 {visible ? 'animate-fade-in-up animation-delay-1500' : 'opacity-0'}">
					<div class="rounded-lg bg-gray-800/50 p-8">
						<h2 class="mb-6 text-2xl font-bold">Ketersediaan</h2>
						<div class="space-y-4">
							<div class="flex items-center space-x-3">
								<div class="text-cyan-400">🕐</div>
								<div>
									<h3 class="font-semibold text-white">Jam Kuliah</h3>
									<p class="text-sm text-gray-300">Senin - Jumat: 09.00 - 18.00 WIB</p>
								</div>
							</div>
							<div class="flex items-center space-x-3">
								<div class="text-purple-400">⏰</div>
								<div>
									<h3 class="font-semibold text-white">Waktu Respons</h3>
									<p class="text-sm text-gray-300">Biasanya dalam 8-24 jam</p>
								</div>
							</div>
							<div class="flex items-center space-x-3">
								<div class="text-green-400">🌍</div>
								<div>
									<h3 class="font-semibold text-white">Zona Waktu</h3>
									<p class="text-sm text-gray-300">WIB (UTC+7)</p>
								</div>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>

<style>
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
</style>
