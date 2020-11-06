<script>
	export let name;
	export const layout1 = [
		['ESC',  '1', '2', '3', '4', '5', '6', '7', '8', '9', '0', '←'],
		['TAB',  'Q', 'W', 'F', 'P', 'G', 'J', 'L', 'U', 'Y', ';', '\''],
		['CTRL', 'A', 'R', 'S', 'T', 'D', 'H', 'N', 'E', 'I', 'O', '⏎'],
		['(',    'Z', 'X', 'C', 'V', 'B', 'K', 'M', ',', '.', '/', ')'],
		['[',    '{', '<', '', '␠', '␠', '␠', '␠', '', '>', '}', '}']
	]
</script>

<main>
	<h1>Hello {name}!</h1>
	<table>
		<tbody>
			{#each layout1 as row, i}
			<tr>
				{#each row as letter}
				<td>{letter}</td>
				{/each}
			</tr>
			{/each}
		</tbody>
	</table>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>