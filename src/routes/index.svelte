
<script context="module">
	export async function preload(page) {
		
		const res = await this.fetch("https://api.openbrewerydb.org/breweries/")
		const data = await res.json()
		return { data }
	}
</script>

<script>
	export let data
	console.log(data) 
</script>

<div>
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