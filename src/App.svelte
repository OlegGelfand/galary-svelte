<script>

    let nextPhoto = 1

    function toggleNext() {
        nextPhoto++;
        if (nextPhoto > 5) nextPhoto = 5;
    }

    function togglePrev() {
        nextPhoto--
        if (nextPhoto < 1) nextPhoto = 1;
    }
</script>
<style>


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
        /*position: relative;*/
        /*margin: auto;*/
        text-align: center;

    }
	.photostrip {
        display:inline-block;
        position:relative;
        width:400px;
		height:300px;
		/*width:calc(400%/5);*/
		border: 2px solid blue;
		overflow: hidden;

	}
    .photos {
        position:absolute;
        top:0;
        left:0;
        width:calc(100% * 5);
        height: 100%;


    }

    img {
        height:100%;
        width:calc(100%/5);
        margin: 0;
        padding: 0;
    }
    .activate-photo1{
        left:0;
    }
    .activate-photo2 {
        left:-100%;
    }
    .activate-photo3 {
        left:-200%;
        /*left:300%;*/
    }
    .activate-photo4 {
        left:-300%;
    }
    .activate-photo5 {
        left:-400%;
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






</style>
<main>
    <div class="container">
        <h1>welcome to the future</h1>
        <div class="photostrip">
            <ul class="photos activate-photo{nextPhoto}">
                <img alt="2"  class="active1"
                     src="https://images.unsplash.com/photo-1550103560-199ddb5aded5?ixid=MnwxMjA3fDB8MHxzZWFyY2h8NHx8aXNyYWVsfGVufDB8fDB8fA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60">
                <img alt="1"  class="active2"
                     src="https://images.unsplash.com/photo-1542743409-158c1d9b2c61?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTl8fGlzcmFlbHxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60">
                <img alt="1"  class="active3"
                     src="https://images.unsplash.com/photo-1542743409-158c1d9b2c61?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTl8fGlzcmFlbHxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60">
                <img alt="1"  class="active4"
                     src="https://images.unsplash.com/photo-1542743409-158c1d9b2c61?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTl8fGlzcmFlbHxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60">
                <img alt="1"  class="active5"
                     src="https://images.unsplash.com/photo-1542743409-158c1d9b2c61?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTl8fGlzcmFlbHxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60">
            </ul>
        </div>
        <div class="button-class">
            <button on:click={toggleNext} class="button">next</button>
            <button class="button">{nextPhoto}/5</button>
            <button on:click={togglePrev} class="button">prev</button>
        </div>
    </div>

</main>

