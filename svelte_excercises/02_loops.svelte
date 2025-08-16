<script lang="ts">
	let names: String = ["Alice","Bobo","Carl","Duke"];
</script>

<ul>
{#each names as name}
	<li>Hello {name}</li>
{/each}
</ul>