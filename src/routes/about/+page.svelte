<script>
	import { onMount } from 'svelte';

	let visible = false;

	onMount(() => {
		visible = true;
	});
</script>

<svelte:head>
	<title>About - Muhammad Gifary</title>
	<meta name="description" content="Tentang Muhammad Gifary - Web Developer & Fotografer" />
</svelte:head>

<section class="pt-24 pb-16">
	<div class="container mx-auto px-4">
		<div class="mx-auto max-w-6xl">
			<h1
				class={`mb-8 text-center text-4xl font-bold md:text-5xl ${
					visible ? 'animate-fade-in-up' : 'opacity-0'
				}`}
			>
				About <span
					class="bg-gradient-to-r from-cyan-400 to-purple-600 bg-clip-text text-transparent"
					>Me</span
				>
			</h1>

			<div class="grid grid-cols-1 items-center gap-12 lg:grid-cols-2">
				<!-- Foto -->
				<div
					class={`flex justify-start ${visible ? 'animate-fade-in-up animation-delay-500' : 'opacity-0'}`}
				>
					<div class="h-96 w-96 rounded-2xl bg-gradient-to-br from-cyan-400 to-purple-600 p-1">
						<div class="flex h-full w-full items-center justify-center rounded-2xl bg-gray-800">
							<img
								src="/images/foto.JPG"
								alt="Foto Muhammad Gifary"
								class="h-94 w-94 rounded-2xl object-cover"
							/>
						</div>
					</div>
				</div>

				<!-- Biodata -->
				<div
					class={`space-y-6 ${visible ? 'animate-fade-in-up animation-delay-1000' : 'opacity-0'}`}
				>
					<div>
						<h2 class="mb-4 text-2xl font-bold">Hello, I'm Muhammad Gifary</h2>
						<p class="leading-relaxed text-gray-300">
							Saya adalah seorang Web Developer dan Fotografer yang berdomisili di Binjai,
							Indonesia. Saya menyukai pengembangan antarmuka web yang modern, serta memiliki
							passion dalam menciptakan tampilan visual yang estetis dan interaktif.
						</p>
					</div>
					<div>
						<h3 class="mb-3 text-xl font-semibold">Perjalanan Saya</h3>
						<p class="leading-relaxed text-gray-300">
							Perjalanan saya dimulai dari ketertarikan terhadap dunia desain dan teknologi. Dari
							memotret hingga membangun website, saya terus belajar dan berkembang, menggabungkan
							kreativitas dan logika.
						</p>
					</div>
					<div>
						<h3 class="mb-3 text-xl font-semibold">Apa yang Saya Lakukan</h3>
						<p class="leading-relaxed text-gray-300">
							Saya membuat website UMKM, dokumentasi proyek, dan antarmuka visual yang responsif
							dengan teknologi seperti SvelteKit dan Tailwind CSS. Selain itu, saya juga aktif
							sebagai fotografer freelance.
						</p>
						<p class="leading-relaxed text-gray-300">
							Saya membuat website UMKM, dokumentasi proyek, dan antarmuka visual yang responsif
							dengan teknologi seperti SvelteKit dan Tailwind CSS. Selain itu, saya juga aktif
							sebagai fotografer freelance.
						</p>

						<!-- Link ke proyek Warkop TVB -->
						<div class="mt-6">
							<h4 class="text-lg font-semibold text-white">
								Contoh Proyek UMKM Yang Saya Kerjakan:
							</h4>
							<a
								href="https://warkoptvb.wuaze.com/"
								target="_blank"
								class="mt-2 inline-block text-cyan-400 transition duration-200 hover:text-cyan-300 hover:underline"
								>🔗 Website Warkop TVB</a
							>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>

<!-- Pengalaman -->
<section class="bg-gray-800/50 py-16">
	<div class="container mx-auto px-4">
		<div class="mx-auto max-w-4xl">
			<h2 class="mb-12 text-center text-3xl font-bold">Pengalaman & Pendidikan</h2>

			<div class="space-y-8">
				<div class="flex flex-col gap-6 rounded-lg bg-gray-700/50 p-6 md:flex-row md:items-center">
					<div class="md:w-1/3">
						<div class="font-semibold text-cyan-400">2023 - Sekarang</div>
						<div class="text-sm text-gray-400">Web Developer & Fotografer</div>
					</div>
					<div class="md:w-2/3">
						<h3 class="mb-2 text-xl font-semibold">Freelancer</h3>
						<p class="text-gray-300">
							Mengerjakan proyek website UMKM, dokumentasi bisnis, dan jasa fotografi produk serta
							event. Fokus pada tampilan estetis dan pengalaman pengguna.
						</p>
					</div>
				</div>

				<div class="flex flex-col gap-6 rounded-lg bg-gray-700/50 p-6 md:flex-row md:items-center">
					<div class="md:w-1/3">
						<div class="font-semibold text-cyan-400">2023 - Sekarang</div>
						<div class="text-sm text-gray-400">Sistem Informasi</div>
					</div>
					<div class="md:w-2/3">
						<h3 class="mb-2 text-xl font-semibold">Mahasiswa</h3>
						<p class="text-gray-300">
							Belajar pemrograman, sistem pendukung keputusan, dan pengembangan perangkat lunak.
							Aktif dalam proyek kampus dan lomba UI/UX serta coding.
						</p>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>

<!-- Nilai-nilai -->
<section class="py-16">
	<div class="container mx-auto px-4">
		<div class="mx-auto max-w-4xl">
			<h2 class="mb-12 text-center text-3xl font-bold">Nilai Hidup Saya</h2>

			<div class="grid grid-cols-1 gap-8 md:grid-cols-2 lg:grid-cols-3">
				<!-- Nilai 1 -->
				<div class="p-6 text-center">
					<div
						class="mx-auto mb-4 flex h-16 w-16 items-center justify-center rounded-full bg-gradient-to-br from-cyan-400 to-purple-600"
					>
						<svg class="h-8 w-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"
							/>
						</svg>
					</div>
					<h3 class="mb-2 text-xl font-semibold">Kreativitas</h3>
					<p class="text-gray-400">
						Berpikir kreatif dalam menyelesaikan masalah dan menghasilkan karya.
					</p>
				</div>

				<!-- Nilai 2 -->
				<div class="p-6 text-center">
					<div
						class="mx-auto mb-4 flex h-16 w-16 items-center justify-center rounded-full bg-gradient-to-br from-purple-400 to-pink-600"
					>
						<svg class="h-8 w-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"
							/>
						</svg>
					</div>
					<h3 class="mb-2 text-xl font-semibold">Ketelitian</h3>
					<p class="text-gray-400">
						Fokus pada detail agar menghasilkan karya yang rapi dan profesional.
					</p>
				</div>

				<!-- Nilai 3 -->
				<div class="p-6 text-center">
					<div
						class="mx-auto mb-4 flex h-16 w-16 items-center justify-center rounded-full bg-gradient-to-br from-green-400 to-blue-600"
					>
						<svg class="h-8 w-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197m13.5-9a2.5 2.5 0 11-5 0 2.5 2.5 0 015 0z"
							/>
						</svg>
					</div>
					<h3 class="mb-2 text-xl font-semibold">Kolaborasi</h3>
					<p class="text-gray-400">
						Senang bekerja dalam tim dan berbagi ide untuk hasil yang lebih baik.
					</p>
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
</style>
