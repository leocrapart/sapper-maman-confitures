
<script context="module">
	export async function preload(page) {
		
		const res = await this.fetch("https://api.openbrewerydb.org/breweries/")
		const data = await res.json()
		return { data }
	}
</script>

<script>
	export let data
</script>

<div class="rounded bg-gray-200 mb-4 p-4">
	<div>Valerie confiture</div>
	<div class="text-sm">
		super confitures
	</div>
</div>


<div class="bg-gray-200 rounded p-4 ">
	<div>data is here</div>
	{#each data as bear, i}
		<div>{i}</div>
		{#each Object.entries(bear) as bear_data}
			<div>{bear_data[0]} => {bear_data[1]}</div>
		{/each}
	{/each}
</div>
<svelte:head>
	<title>maman confitures</title>
</svelte:head>

<div>homepage</div>