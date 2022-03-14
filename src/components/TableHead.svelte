<script>
	export let columns;
</script>

{#each columns as column}
	<th>{column}</th>
{/each}

<style>
	th {
  	border: 1px solid;
	}
</style>