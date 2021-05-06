<script>

	let nextPhoto = 1

	function toggleNext() {
		nextPhoto++
	}

	function togglePrev() {
		nextPhoto--
	}
</script>
<style>
	button:last-of-type {
		float: right;
	}

	button {
		display: inline-block;
		background-color: #6666cc;
		color: white;
		font-family: "Roboto Light";
		font-size: 36px;
		border-radius: 10px;
		padding: 2px 8px;
		margin-top: 20px;
		font-weight: 400;
		box-shadow: 1px 4px 4px -2px #8E6D8A;
	}

	.button-class {
		text-align: center;
	}

	h1 {
		text-align: center;
		padding: 1em;
		font-family: 'Roboto Slab', serif;
		font-weight: 900;
		color: #000000;
		font-size: 36px;
		text-transform: uppercase;
	}

	.container {

		position: relative;
		margin: auto;
		text-align: center;

	}

	.image-class {
		/*position: center;*/
		/*display: inline;*/
		height: 300px;
		width: 500%;
		border: 3px solid black;
		/*margin-left: 75px;*/
	}

	img {
		padding: 5px;
		/*max-width:150px;*/
		position: relative;
		/*top:0px;*/
		/*left:0;*/
		/*right:0;*/
		/*bottom:0px;*/
		transition: width 2s, height 6s, transform 2s;
		transition-delay: 10s;
		/*transition: top 2000ms cubic-bezier(1,1.67,0,-0.49), left 2000ms cubic-bezier(1,2.67,0,-0.49);*/
	}

	.button {
		/*display:inline-block;*/
		background-color: #6666cc;
		color: white;
		font-family: "Roboto Light";
		font-size: 36px;
		border-radius: 10px;
		padding: 2px 8px;
		margin-top: 20px;
		font-weight: 400;
		box-shadow: 1px 4px 4px -2px #8E6D8A;
	}

	h1 {
		text-align: center;
		padding: 1em;
		font-family: 'Roboto Slab', serif;
		font-weight: 900;
		color: #000000;
		font-size: 36px;
		text-transform: uppercase;
	}

	/*.active {*/
	/*	border: 1px solid black;*/
	/*	top:120px;*/
	/*	left:120px;*/
	/*	right:-120px;*/
	/*	text-transform: capitalize;*/
	/*	bottom:200px;*/
	/*	width: 40px;*/
	/*}*/


	.active1 {
		border: 2px solid black;
		height: 400px;
		left: 0;
	}

</style>
<main>
	<div class="container">
		<h1>welcome to the future</h1>
		<ul class="image-class">
			<img alt="2" {nextPhoto} class="active1"
				 src="https://images.unsplash.com/photo-1550103560-199ddb5aded5?ixid=MnwxMjA3fDB8MHxzZWFyY2h8NHx8aXNyYWVsfGVufDB8fDB8fA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60">
			<img alt="1" {nextPhoto / 2} class="active2"
				 src="https://images.unsplash.com/photo-1542743409-158c1d9b2c61?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTl8fGlzcmFlbHxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60">
			<img alt="1" {nextPhoto} class="active3"
				 src="https://images.unsplash.com/photo-1542743409-158c1d9b2c61?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTl8fGlzcmFlbHxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60">
			<img alt="1" {nextPhoto} class="active4"
				 src="https://images.unsplash.com/photo-1542743409-158c1d9b2c61?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTl8fGlzcmFlbHxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60">
			<img alt="1" {nextPhoto} class="active5"
				 src="https://images.unsplash.com/photo-1542743409-158c1d9b2c61?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTl8fGlzcmFlbHxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60">
		</ul>
		<div class="button-class">
			<button on:click={toggleNext} class="button">next</button>
			<button class="button">{nextPhoto}/5</button>
			<button on:click={togglePrev} class="button">prev</button>
		</div>
	</div>

</main>

