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
	const storyParagraphs = [
		`The Egg Nog Leg Jog is the world’s first race that not only tests your physical fitness, 
     but also your capacity to experience holiday joy! Are you training for a longer winter 
     race, like the Seattle Marathon or CIM? Are you preparing for a cross-country flight to 
     celebrate traditions with family on the east coast? Are you gearing up to enjoy numerous 
     Thanksgiving/Christmas/Hanukkah parties, right here in Seattle? Nothing is going to 
    prepare you for  all of the holiday magiclike the Egg Nog Leg Jog. `,
		`This 10K on November 15th will be run by 100+ family, friends, and soon to be friends. 
     Bring your best holiday themed costume (ie Santa / Scrooge / Menorah) or favorite  Christmas 
     sweater and join us at Woodland Park for a festive Leg Jog. We’ll run through Greenlake and
     Woodland Park,  stopping at four  holiday cheer stations along the way to consume cookies, 
     egg nog and other classic holiday treats, which will warm your body and grow your heart at 
     least three sizes.  `
	];

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
