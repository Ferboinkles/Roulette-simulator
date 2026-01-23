<script>
	import { goto } from "$app/navigation";
	let money = $state(1000000);
</script>

<p class="max-w-fit rounded-full bg-white p-3 text-cyan-600">
	You have ${money} left!
</p>
<h1 class="text-center font-serif text-5xl text-cyan-600">Welcome to the Roulette Simulator!</h1>
<h2 class="text-center font-serif text-2xl text-cyan-600">Click on a button to see the probability of your bet!</h2>
<div class="@container min-h-full flex-row text-center font-serif">
	<img alt="wheel" src="/images/wheel.webp" class=" mx-auto my-4 aspect-square w-[35%] animate-spin object-cover" />
	<div class="@container mr-15 flex-row text-center font-serif">
		<button
			onclick={goto("/black-button")}
			class="my-1 max-w-fit rounded-[0.5em] bg-black p-[0.5em] font-serif whitespace-normal text-white hover:animate-bounce"
		>
			Black (2, 4, 6, 8, 10, 11, 13, 15, 17, 20, 22, 24, 26, 28, 29, 31, 33 and 35)
		</button>
		<button
			onclick={goto("/green-button")}
			class="my-1 max-w-fit rounded-[0.5em] bg-green-700 p-[0.5em] font-serif whitespace-normal hover:animate-bounce"
		>
			Green (0)
		</button>
		<button
			class="my-1 max-w-fit rounded-[0.5em] bg-red-700 p-[0.5em] font-serif whitespace-normal hover:animate-bounce"
			onclick={goto("/red-button")}
		>
			Red (1, 3, 5, 7, 9, 12, 14, 16, 18, 19, 21, 23, 25, 27, 30, 32, 34, and 36)
		</button>
	</div>
	<div class="@container mr-15 flex-row text-center font-serif">
		<button
			onclick={goto("/even")}
			class="my-1 max-w-fit rounded-[0.5em] bg-green-700 p-[0.5em] font-serif whitespace-normal hover:animate-bounce"
		>
			Even (Even numbers between 1-36)
		</button>
		<button
			onclick={goto("/odd")}
			class="my-1 max-w-fit rounded-[0.5em] bg-black p-[0.5em] font-serif whitespace-normal text-white hover:animate-bounce"
		>
			Odd (Odd numbers between 1-36)
		</button>
	</div>
	<div class="@container mr-15 flex-row text-center font-serif">
		<button
			onclick={goto("/high")}
			class="my-1 max-w-fit rounded-[0.5em] bg-red-700 p-[0.5em] font-serif whitespace-normal hover:animate-bounce"
		>
			High (19-36)
		</button>
		<button
			onclick={goto("/low")}
			class="my-1 max-w-fit rounded-[0.5em] bg-green-700 p-[0.5em] font-serif whitespace-normal hover:animate-bounce"
		>
			Low (1-18)
		</button>
		<div class="@container flex-row text-center font-serif">
			<button
				onclick={goto("/dozen1")}
				class="my-1 max-w-fit rounded-[0.5em] bg-green-700 p-[0.5em] font-serif whitespace-normal hover:animate-bounce"
			>
				First dozen (1-12)
			</button>
			<button
				onclick={goto("/dozen2")}
				class="my-1 max-w-fit rounded-[0.5em] bg-green-700 p-[0.5em] font-serif whitespace-normal hover:animate-bounce"
			>
				Second dozen (12-24)
			</button>
			<button
				onclick={goto("/dozen3")}
				class="my-1 max-w-fit rounded-[0.5em] bg-green-700 p-[0.5em] font-serif whitespace-normal hover:animate-bounce"
			>
				Third dozen (24-36)
			</button>
		</div>
	</div>
</div>
