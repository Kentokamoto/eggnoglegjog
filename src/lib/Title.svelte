<script>
	import { base } from '$app/paths';
	import mascotThumb from '$lib/assets/gingerbread.webp?inline';
	let { iteration, title } = $props();
</script>

<a href="{base}/">
	<header class="bg-holiday-red flex w-full flex-row">
		<img
			class="m-1 w-12 flex-none place-content-center object-scale-down"
			src={mascotThumb}
			alt="eggnog leg jog mascot"
		/>
		<div class="flex-1 place-content-center">
			<h2 class="text-eggnog-cream text-center text-xl font-extrabold sm:text-3xl">
				{iteration}
			</h2>
			<h1 class="text-eggnog-cream text-center text-2xl font-black sm:text-4xl">
				{title}
			</h1>
		</div>
		<img
			class="m-1 w-12 flex-none place-content-center object-scale-down"
			src={mascotThumb}
			alt="eggnog leg jog mascot"
		/>
	</header>
</a>
