<script>
	import { goto } from "$app/navigation";

	let { children } = $props();
</script>

<button class="max-w-fit rounded-2xl bg-white p-[0.5em] text-left text-xl text-black" onclick={goto("/")}
	>Back to home</button
>
{@render children?.()}
