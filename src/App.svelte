<script>

	let nextPhoto=false;
	function toggleNext() {
		nextPhoto = !nextPhoto;
	}
</script>
<style>
button:last-of-type{
		float:right;
}
button{
		display:inline-block;
		background-color: #6666cc;
		color:white;
		font-family: "Roboto Light";
		font-size:36px;
		border-radius: 10%;
		padding:2px 8px;
		margin-top:20px;
		font-weight:400;
		box-shadow: 1px 4px 4px -2px #8E6D8A;
}
.button-class{
		margin-left: 75px;
		width: 400px;
}
h1 {
		padding: 1em;
		font-family: "Roboto Light";
		font-weight:900;
		color: #000000;
		font-size: 36px;
		text-transform: uppercase;
}

.container {
		height: 1280px;
		/*border: 2px solid red;*/
		width: 600px;
		margin-left:40%;
}
.image-class{
		overflow: hidden;
		/*border:3px solid black;*/
		display: inline-block;
		horiz-align: left;
		margin-left: 75px;
		max-height: 300px;
		max-width: 400px;
}
img{
		padding:5px;
		max-width:150px;
		position: relative;
		top:0px;
		left:0;
		right:0;
		bottom:0px;
		transition: width 2s, height 6s, transform 2s;

		transition-delay: 10s;

		/*transition: top 2000ms cubic-bezier(1,1.67,0,-0.49), left 2000ms cubic-bezier(1,2.67,0,-0.49);*/
}
.active {
		/*border: 1px solid black;*/
		top:120px;
		left:120px;
		right:-120px;
		text-transform: capitalize;
		bottom:200px;
		width: 40px;
}




</style>
<main>
	<div class="container">
		<h1>welcome to the future</h1>

		<ul class="image-class">


			<img class="activeMain"  alt ="2" src="https://images.unsplash.com/photo-1550103560-199ddb5aded5?ixid=MnwxMjA3fDB8MHxzZWFyY2h8NHx8aXNyYWVsfGVufDB8fDB8fA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60">


			<img alt ="1" class:active={nextPhoto} src="https://images.unsplash.com/photo-1542743409-158c1d9b2c61?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTl8fGlzcmFlbHxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60">
			<!--		<li class="individual-image active2"><img src="#" class:active={nextPhoto}></li>-->
			<!--		<li class="individual-image active3"><img src="#" class:active={nextPhoto}></li>-->
			<!--		<li class="individual-image active4"><img src="#" class:active={nextPhoto}></li>-->

		</ul>
		<div class="button-class">
			<button class="button">PREV</button>
			<button  on:click={toggleNext} class="button">NEXT </button>
		</div>
	</div>

</main>

<