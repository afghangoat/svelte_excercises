<script lang="ts">
	let name: String = 'world';
	let count: int = 0;

	function addOne(){
		count++;
	}
</script>

<h1>Hello {name}!</h1>
<button on:click={addOne}>Clicked {count} times!</button>
{#if count > 0}
	<p>Don't be lazy! Click it harder!</p>
{/if}
