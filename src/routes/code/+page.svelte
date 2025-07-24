<style>
/*
#3B1E5C – deep purple

#70286D – medium plum

#E5E4C7 – light cream / beige

#2278A6 – denim blue

#4D90AE – steel blue

#67B0CC – sky blue

#88C7D8 – pastel cyan
*/	

	body, html {
	    margin: 0;
	    padding: 0;
	    height: 100vh;
	    width: 100vw;
	    box-sizing: border-box !important;
	    overflow: hidden;
	}

	.container {
	    display: flex;
	    flex-direction: column;
	    height: 100vh;
	    width: 100vw;
	}

	.code {
	    flex: 1 1 auto;
	    background: #2278A6; /* denim blue */
	    color: #E5E4C7;      /* light cream for contrast */
	    font-family: monospace;
	    padding: 4px 8px;
	}

	.text {
	    flex: 0 0 2rem;
	    background: #4D90AE;      /* steel blue or your preferred bar color */
	    color: #E5E4C7;
	    font-size: 1rem;
	    line-height: 2rem;
	    padding-left: 8px;
	}

	.tail {
	    flex: 0 0 1rem;
	    background: #2278A6;      /* sky blue or another accent color */
	    min-height: 1rem;
	}
</style>

<script>
	let text = "";
</script>

<div class="container">
    <div 
	class="code" 
	contenteditable = "true"
	bind:innerText={text}
    ></div>
    <div class="text">:</div>
    <div class="tail"></div>
</div>

