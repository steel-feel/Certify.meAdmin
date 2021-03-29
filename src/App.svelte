<script>
	let files;
	//export let name;
</script>

<main>
	<div class="navbar">
		<div class="container">
			<a class="logo">Cerify Me</a>
			<h4>Admin</h4>
		</div>
	</div>

	<section class="IPFSupload">
		<div class="file-selector">
			<input type="file" bind:files />

			{#if files && files[0]}
				
				<p>{files[0].name}</p>
				<img src={URL.createObjectURL(files[0])} />
				
			{/if}
		</div>
	</section>
</main>

<style lang="scss">
	.navbar {
		background: var(--bg-color);
		padding: 1em;

		.container {
			display: flex;
			place-content: space-between;

			a {
				text-decoration: none;
				font-weight: bold;
				color: var(--primary-color);
				font-size: 1.2rem;
			}

			h4 {
				margin: 0;
			}
		}
	}

	.IPFSupload {
		display: block;

		.file-selector {
			display: block;

			img{
				width: 90vw;
				height: 20em;
			}

		}
	}
</style>
