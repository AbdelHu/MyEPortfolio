<style>
	* {
		box-sizing: border-box;
	}
	section {
		min-height: 5em;
		height: fit-content;
		padding: 0.6em;
		width: 12em;
		background: black;
	}
	div {
		position: relative;
		height: 2.5em;
		width: 10em;
		text-align: center;
		border: 1px solid black;
		border-radius: 3px;

		margin: 0.2em;
		padding: 0.3em;
		background: white;
		color: black;

		transition: all 0.2s;
	} div:hover {
		background: rgb(217, 217, 217);
	}
	.custom-shadow-item {
		position: absolute;
		top: 0; left:0; right: 0; bottom: 0;
		visibility: visible;
		border: 1px dashed grey;
		background: lightblue;
		opacity: 0.5;
		margin: 0;
	}
</style>

<script>
	// @ts-ignore
	import {dndzone, SHADOW_ITEM_MARKER_PROPERTY_NAME} from 'svelte-dnd-action';
	import {fade} from 'svelte/transition';
	// fade in works fine but don't add svelte's fade-out (known issue)
	import {cubicIn} from 'svelte/easing';
	import {flip} from 'svelte/animate';

	const flipDurationMs = 150;
	function handleSort(e) {
		items = e.detail.items;
	}
	let items = [
		{id:1, title: 'I'},
		{id:2, title: 'Am'},
		{id:3, title: 'Yoda'},
		{id:4, title: 'Haha'},
	];
</script>


<section use:dndzone={{items, flipDurationMs}} on:consider={handleSort} on:finalize={handleSort}>
	{#each items as item(item.id)}
		<div animate:flip={{duration:flipDurationMs}}>
			{item.title}	
			{#if item[SHADOW_ITEM_MARKER_PROPERTY_NAME]}
				<div in:fade={{duration:200, easing: cubicIn}} class='custom-shadow-item'>{item.title}</div>
			{/if}
		</div>
	{/each}
</section>