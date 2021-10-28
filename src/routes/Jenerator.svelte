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
	<button on:click={randomStory}>New story</button>
	<p>
		The old bird Percy Wooster is rather in the soup because <span
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
	}
</style>
