<script lang="ts">
	const quotes_start:String =["The","A","One"];
	const quotes_subject: String=["lion","human","small dog","dragon","little pig"];
	const quotes_smth: String=["never","always","only"];
	const quotes_what: String=["rapes","barks","roars","kills","drinks","defeats"];
	const quotes_second_subject: String=["the small dog","a glass of water","its kind","the king","the traitors","the wild boar","himself","itself","herself"];
	const quotes_end: String=["when it barks.","after the fight.","before the dark.","before the light.","in the jungle.","on the rails.","in its throne."];

	function getRandomInt(max: int): int {
		return Math.floor(Math.random() * max);
	}

	function generateQuote(): String {
		return quotes_start[getRandomInt(quotes_start.length)]+" "+
			quotes_subject[getRandomInt(quotes_subject.length)]+" "+
			quotes_smth[getRandomInt(quotes_smth.length)]+" "+
			quotes_what[getRandomInt(quotes_what.length)]+" "+
			quotes_second_subject[getRandomInt(quotes_second_subject.length)]+" "+
			quotes_end[getRandomInt(quotes_end.length)];
	}
	let curQuote:String="";
	function storeQuote(){
		curQuote=generateQuote();
	}
	
</script>

<h1>Random quote generator!</h1>
<button on:click={storeQuote}>Click me!</button>
<i>{curQuote}</i>