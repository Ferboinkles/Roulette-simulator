<script>
	let bets = $state(0);
</script>

<h1
	class="text-center font-serif text-4xl text-blue-800"
>
	Welcome to the Roulette Simulator!
</h1>
<div
	class="@container flex-row text-center font-serif"
>
	<button class=" fixed hover:animate-spin"
		><img alt="wheel" src="/images/wheel.webp" />
	</button>
	<div
		class="@container mr-15 flex-row text-right font-serif"
	>
		<button
			class="my-1 max-w-fit rounded-[0.5em] bg-black font-serif whitespace-normal text-white hover:scale-110 hover:animate-bounce"
		>
			Black
		</button>
		<button
			class="my-1 max-w-fit rounded-[0.5em] bg-red-700 font-serif whitespace-normal hover:scale-110 hover:animate-bounce"
		>
			Red
		</button>
	</div>
	<div
		class="@container mr-15 flex-row text-right font-serif"
	>
		<button
			class=" my-1 max-w-fit rounded-[0.5em] bg-green-800 font-serif whitespace-normal hover:scale-110 hover:animate-bounce"
		>
			Even
		</button>
		<button
			class="my-1 max-w-fit rounded-[0.5em] bg-black font-serif whitespace-normal text-white hover:scale-110 hover:animate-bounce"
		>
			Odd
		</button>
	</div>
	<div
		class="@container mr-15 flex-row text-right font-serif"
	>
		<button
			class=" my-1 max-w-fit rounded-[0.5em] bg-red-700 font-serif whitespace-normal hover:scale-110 hover:animate-bounce"
		>
			High
		</button>
		<button
			class=" my-1 max-w-fit rounded-[0.5em] bg-green-800 font-serif whitespace-normal hover:scale-110 hover:animate-bounce"
		>
			Low
		</button>
	</div>
</div>
