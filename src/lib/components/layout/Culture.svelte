<script lang="ts">
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";
	import { animate, stagger } from "motion";
	import { onMount } from "svelte";

	// Types
	export type Value = {
		title: string;
		description: string;
	};

	// Props
	const { values = [
  {
    title: "Responsibility first",
    description: "We design and deploy AI with a steadfast commitment to human well-being and safety, always prioritizing the public good over speed."
  },
  {
    title: "Curiosity with rigor",
    description: "We encourage open inquiry and creative problem-solving, supported by meticulous research and a drive to understand how and why systems work."
  },
  {
    title: "Long-term impact",
    description: "We weigh every decision for its lasting consequences, shaping technology to benefit generations—not just the next quarter."
  },
  {
    title: "Transparency & trust",
    description: "We share our research and decisions openly, earning trust through honest dialogue and openness about what we know and don’t."
  },
  {
    title: "Collaboration always",
    description: "Our work thrives on ideas shared across backgrounds, disciplines, and perspectives—believing we go further, together."
  },
  {
    title: "Diversity strengthens decisions",
    description: "A wide range of voices and experiences drives better outcomes. We welcome disagreement and value respectful debate."
  }
]: { values: Value[] } = $props();

	let cards: HTMLElement[] = $state([]);

	onMount(() => {
		if (!cards.length) return;
		animate(
			cards,
			{
				y: ["1.5rem", 0],
				filter: ["blur(2px)", "blur(0px)"],
				opacity: [0, 1]
			},
			{
				duration: 0.3,
				ease: "easeOut",
				delay: stagger(0.1, {
					ease: "easeInOut"
				})
			}
		);
	});
</script>

<section class="bg-white dark:bg-gray-950">
	<div
		class="section-py section-px container mx-auto grid gap-8 [--gap:--spacing(8)] [--radius:var(--radius-2xl)]"
	>
		<SectionHeader title="A culture of responsibility" subtitle="These are the values that guide Anthropic" />

		<div
			class="grid gap-(--gap)"
			style:grid-template-columns="repeat(auto-fit, minmax(280px, 1fr))"
		>
			<img src="/generated/image-a-diverse-group-of-researchers-engaged-i.webp" alt="Anthropic culture team" class="rounded-xl w-full object-cover mb-8 lg:mb-0 col-span-full"/>
			{#each values as value, i}
				<div
					bind:this={cards[i]}
					class="relative border-t border-gray-200 pt-4 dark:border-gray-900"
				>
					<!-- Content -->
					<div class="text-caption z-10">
						<div>
							<div class="text-headline mb-[1em]">{value.title}</div>
							<div class="text-body text-gray-500 dark:text-gray-400">{value.description}</div>
						</div>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>
