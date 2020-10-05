
<script>
	import { count } from './store.js'

	function increment() {
		count.update(n => n+1)
	}

	let count_value
	const unsuscribe = count.subscribe(value => {
		count_value = value
	})
</script>

<div class="bg-white rounded p-4">
	<div>test</div>
	<div>Count is {count_value}</div>
	<button on:click={increment}
		class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded" >+1</button>
	
</div>

<div>info page</div>