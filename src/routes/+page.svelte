<script lang="ts">
	
	
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
	<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@500&display=swap" rel="stylesheet">

</svelte:head>

<section>
	<div class="left-side">
		<img src="/bg-main-desktop.png" alt="bg photo" class="bg" />
		<div class="cards">
			<img src="/bg-card-front.png" alt="card front" class="card-front" />
			<img src="/bg-card-back.png" alt="card back" class="card-back"/>
		</div>
	</div>
	
	<div class="card"> 
		<label>CARDHOLDER NAME</label>
		<input type="text" placeholder="e.g. Janee Appleseed" />
		<label>CARD NUMBER</label>
		<input type="number" placeholder="e.g. 1234 5678 9123 0000" />
		<div class="date-cvc">
			<div>
				<lable>EXP. DATE (MM/YY) </lable>
				<div class="date-fields">
					<input type="text" placeholder="MM" />
					<input type="text" placeholder="YY" />
				</div>
				
			</div>
			<div>
				<label>CVC </label>
				<input type="number" placeholder="e.g. 123" />
			</div>
			
		</div>
		
		<button>Confirm</button>
	</div>
</section>

<style>
	section {
		display: flex;
		align-items: center;	
		min-height: 100vh;
		font-family: 'Space Grotesk', sans-serif;
		font-weight: 500;
		
	}
	.bg {
		width: 80%;
		height: 100vh;
		object-fit: cover;
		
	}
	.left-side {
		position: relative;
		width: 40%;
	}


	.card {
		background-color: white;
		border-radius: 10px;
		padding: 20px;
		margin: 20px;
		width: 30%;
		
		
	}
	input {
		width: 100%;
		padding: 10px;
		margin: 5px 0;
		border: 1px solid #ccc;
		border-radius: 5px;
		margin-bottom: 1.5rem;
	}
	button {
		background-color: hsl(278, 68%, 11%);
		color: white;
		padding: 10px 20px;
		border: none;
		border-radius: 5px;
		cursor: pointer;
		width: 100%;
		margin-top: 1rem;
	}
	button:hover {
		background-color: white;
		color: hsl(278, 68%, 11%);
	}
	.date-cvc {
		display: flex;
		justify-content: space-between;
		gap: 10px;
		
	}
	.cards {
		position: absolute;
		top: 50%;
		left: 50%;
	
	}

	.card-front {
		
		position: relative;
		z-index: 2;
		transform: translate(-10%, -120%);
		margin-bottom: 10px;
	}

	.card-back {
		
		position: relative;
		transform: translate(10%, -100%);
		z-index: 1;
		
	}
	.date-fields {
		display: flex;
		gap: 10px;
	}

	label {
		font-size: 12px;
		letter-spacing: 2px;
	}	


	
	
</style>
