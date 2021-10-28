<script>
	import Jenerator from './Jenerator.svelte';
</script>

<svelte:head>
	<title>Jeeves Jenerator</title>
</svelte:head>

<main>
	<div class="title-container">
		<h1><span id="jeeves">Jeeves</span> Jenerator</h1>
		<img
			src="./images/jeeves-and-wooster-illustration.jpg"
			alt="Ink illustration of Jeeves and Wooster"
		/>
	</div>
	<Jenerator />
</main>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Poiret+One&display=swap');
	main {
		font-family: Georgia, 'Times New Roman', Times, serif;
		width: 25%;
		margin: auto;
	}

	#jeeves {
		color: #fe151b;
		font-weight: bold;
	}

	h1 {
		font-family: 'Poiret One', cursive;
		text-align: center;
		font-size: 3rem;
	}

	img {
		width: 100%;
	}
</style>
