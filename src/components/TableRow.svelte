<script>
	export let rows;
</script>

{#each rows as row}
<tr>
	<td><img src={row.avatar} alt='{row.name}' /></td>
	<td>{row.name}</td>
	<td>{row.email}</td>
</tr>
{/each}

<style>
	td {
  	border: 1px solid;
	}
</style>