<script>
	import Nav from '../components/Nav.svelte';

</script>
<Nav/>
<main class="lg:mt-20 container mx-auto p-4">
	<slot></slot>
</main>
<sapper:body>
	<style>
		body {
			background-image: url('https://ik.imagekit.io/pl6zwucqxr/grass-background_tveE3-0zCxI.jpg');
			background-position: center center;
			background-repeat: no-repeat;
			background-attachment: fixed;
			background-size: cover;
		}
	</style>
</sapper:body>
