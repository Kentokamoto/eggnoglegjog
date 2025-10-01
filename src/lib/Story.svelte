<script>
	let { storyTitle, storyParagraphs } = $props();
</script>

<article class="text-ornament-green">
	<h1 class="text-ornament-green mt-5 text-center text-2xl font-bold sm:text-left">
		{storyTitle}
	</h1>
	{#each storyParagraphs as paragraph, index (index)}
		<p class="mb-3">{paragraph}</p>
	{/each}
</article>
