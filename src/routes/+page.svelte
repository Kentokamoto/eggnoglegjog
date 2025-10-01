<script>
	import Story from '$lib/Story.svelte';
	import Details from '$lib/Details.svelte';
	import FAQ from '$lib/FAQ.svelte';
	import Registration from '$lib/Registration.svelte';
	import Title from '$lib/Title.svelte';
	import Counter from '$lib/Counter.svelte';

	// Placeholders:
	const eventDate = new Date('November 15, 2025 10:00 AM PDT');
	const eventLocation = 'Lower Woodland Park Shelter';
	const storyTitle = 'Eggnog Leg Jog';
	const storyParagraphs = [``];

	import { base } from '$app/paths';
	const mailtoLink = `<a href="mailto:seattlesliceathon@gmail.com"
	                       class="text-holiday-red hover:text-red-700 underline">
						   seattlesliceathon@gmail.com
						</a>`;
	const gpxLink = `<a href="${base}/Seattle-Slice-a-Thon-2025.gpx"
	                 	class="text-holiday-red hover:text-red-700 underline">
						Eggnog Leg Jog route
					</a>`;

	const faqs = [''];

	// JotForm
	let jotformIframeId = 'JotFormIFrame-250816626970059';
</script>

<svelte:head>
	<title>2025 Seattle Eggnog Leg Jog</title>
	<meta name="description" content="Start the holiday season off on the right foot" />
</svelte:head>

<Title iteration="First Annual" title="Seattle Eggnog Leg Jog" />
<Counter judgementDate={eventDate.getTime()} />
<div></div>
<div class="flex justify-center">
	<div class="item-center mx-10 w-4xl flex-col">
		<Story {storyParagraphs} {storyTitle} />
		<Details {eventDate} {eventLocation}>
			<div
				class="strava-embed-placeholder"
				data-embed-type="route"
				data-embed-id="3406145129692623686"
				data-style="standard"
				data-map-hash="12.41/47.675/-122.34166"
				data-from-embed="true"
			></div>
		</Details>
		<FAQ {faqs} />
		<Registration iframeId={jotformIframeId}>
			<iframe
				id="JotFormIFrame-250816626970059"
				title="2025 Slice-A-Thon Registration"
				allowtransparency
				allow=""
				src="https://form.jotform.com/252468546155161"
				frameborder="0"
				style="border:none;"
				scrolling="no"
				width="100%"
				height="200px"
				class="rounded-lg"
			>
			</iframe>
		</Registration>
	</div>
</div>
