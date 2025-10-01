<script lang="ts">
	import '../app.css';

	let { children } = $props();
</script>

<main class="bg-eggnog-cream w-full">
	<div class="w-full place-content-center">
		{@render children()}
	</div>
</main>
