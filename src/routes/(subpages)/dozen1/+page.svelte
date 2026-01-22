<script>
	let money = $state(1000000);
	let bet = $state(1);
	let winProbability = 0.39;
	let loseProbability = 0.68;
	let expectedWin = winProbability * bet;
	let expectedLoss = loseProbability * bet;
	let expectedValue = (expectedWin - expectedLoss) * 100;
</script>

<h1 class=" mt-2 text-center font-serif text-5xl text-white">You have chosen to bet on the first dozen!</h1>
<h2 class="max-w-fit rounded-2xl bg-white p-[0.5em] text-left text-xl text-black">money = ${money - bet}</h2>

<div class="text-center">
	<input
		id="bet"
		class="mx-auto w-20 rounded-3xl invalid:outline-red-500 disabled:cursor-not-allowed"
		bind:value={bet}
		type="number"
		min="1"
	/>
</div>
{#if bet !== null && bet > 1 && bet !== ""}
	<p class="mx-auto max-w-fit text-2xl text-white text-shadow-2xs md:text-3xl">
		You are going to bet {bet}!
	</p>
{/if}
{#if bet <= 0}
	<p class="mx-auto max-w-fit text-2xl text-white text-shadow-2xs md:text-3xl">You cannot bet that much!</p>
{/if}

<h2 class="text-center text-3xl text-white">
	Your expected win is ${expectedWin} and your expected loss is ${expectedLoss} and your expected loss is {expectedValue}%
</h2>
<h2 class="text-center text-3xl text-white">
	This is because there is one green in roulette which gives the house an edge every time.
</h2>
