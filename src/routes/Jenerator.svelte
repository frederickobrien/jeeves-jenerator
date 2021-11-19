<script>
	import { onMount } from 'svelte';
	import { dilemmas } from '/lists/dilemmasList.js';
	import { clothing } from '/lists/clothingList.js';
	import { mishaps } from '/lists/mishapsList.js';
	import { solutions } from '/lists/solutionsList.js';

	function randomStory() {
		document.getElementById('dilemma-text').innerHTML =
			dilemmas[Math.floor(Math.random() * dilemmas.length)];
		document.getElementById('clothing-text').innerHTML =
			clothing[Math.floor(Math.random() * clothing.length)];
		document.getElementById('mishap-text').innerHTML =
			mishaps[Math.floor(Math.random() * mishaps.length)];
		document.getElementById('solution-text').innerHTML =
			solutions[Math.floor(Math.random() * solutions.length)];
	}

	onMount(randomStory);
</script>

<div>
	<div class="container">
		<div class="center">
			<button on:click={randomStory}>New story</button>
		</div>
	</div>

	<p>
		The old bird Bertie Wooster is rather in the soup because <span
			id="dilemma-text"
			class="random-text">...</span
		>. Usually Jeeves would take care of it, but relations have been icy since Wooster started
		wearing
		<span id="clothing-text" class="random-text">...</span>. Wooster tries to solve the problem
		himself but only makes it worse by <span id="mishap-text" class="random-text">... </span>. Just
		when things are at their rummiest Jeeves saves the day by
		<span id="solution-text" class="random-text">...</span>. Unspeakably grateful for the help,
		Wooster gets rid of the offending item of clothing.
	</p>
</div>

<style>
	.random-text {
		color: #fe151b;
		font-weight: bold;
	}

	p {
		line-height: 1.5;
		padding-bottom: 50px;
	}

	.container {
		height: 100px;
		position: relative;
	}

	.center {
		margin: 0;
		position: absolute;
		top: 50%;
		left: 50%;
		-ms-transform: translate(-50%, -50%);
		transform: translate(-50%, -50%);
	}

	button {
		padding: 10px 20px;
		font-family: Georgia, 'Times New Roman', Times, serif;
		background-color: #fe151b;
		color: white;
		font-size: 1.1em;
		border-radius: 30px;
		font-weight: bold;
	}
</style>
