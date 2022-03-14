<script>
	import TableHead from "./TableHead.svelte";
	import TableRow from "./TableRow.svelte";
	import faker from '@faker-js/faker';
	const numberOfRows = 10;
	const columns = [];
	columns.push('Picture');
	columns.push('Name');
	columns.push('Email');
	const rows = [];
	for(let i = 1; i<=numberOfRows; i++) {
		rows.push({
			avatar: faker.image.avatar(),
			name: faker.name.findName(),
			email: faker.internet.email()
		});
	}
</script>

<h1>People Table</h1>
<table>
	<tr>
		<TableHead columns={columns} />
	</tr>
	{#each rows as row}
	<TableRow rows={rows}/>
	{/each}
</table>

<style>
	table {
  	border: 1px solid;
		margin-left: auto;
  	margin-right: auto;
	}
</style>