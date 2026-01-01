<script>
	import { goto } from "$app/navigation";
	let money = $state(1000000);
	let bet = $state(1);
	let winProbability = 0.39
	let loseProbability = 0.68
	let expectedWin = winProbability * bet;
	let expectedLoss = loseProbability * bet;
	let expectedValue = (expectedWin - expectedLoss)* 100;
</script>
<button class="text-black text-left text-xl rounded-2xl p-[0.5em] bg-white max-w-fit" onclick={goto("/")}>Back to home</button>
<h1 class=" text-white font-serif text-center text-5xl mt-2">You have chosen to bet on the second dozen!</h1>
<h2 class="text-black text-left text-xl rounded-2xl p-[0.5em] bg-white max-w-fit">money = ${money-bet}</h2>

<div class="text-center">
	<input
		id="bet"
		class="mx-auto w-20 invalid:outline-red-500 disabled:cursor-not-allowed rounded-3xl"
		bind:value={bet}
		type="number"
		min="1"
	/></div>
{#if bet !== null && bet > 1 && bet !== ""}
	<p class="mx-auto max-w-fit text-2xl text-white text-shadow-2xs md:text-3xl">
		You are going to bet {bet}!
	</p>
{/if}
{#if bet<=0}
	<p class="mx-auto max-w-fit text-2xl text-white text-shadow-2xs md:text-3xl">
		You cannot bet that much!
	</p>
{/if}

<h2 class="text-white text-3xl text-center">Your expected win is ${expectedWin} and your expected loss is ${expectedLoss} and your expected loss is {expectedValue}%</h2>
<h2 class="text-white text-3xl text-center">This is because there is one green in roulette which gives the house an edge every time.</h2>