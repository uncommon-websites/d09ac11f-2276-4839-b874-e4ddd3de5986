<script lang="ts">
	// Types
	import type { PageProps } from "./$types";

	// Components
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import Pricing from "$lib/components/layout/Pricing.svelte";

	// Props
	const { data }: PageProps = $props();
</script>

<Pricing />

<Testimonials
	testimonials={[
  {
    name: "Naomi Keene",
    position: "Head of Product",
    company: "Revise Analytics",
    quote:
      "We integrated Claude across engineering, product, and design in two days. Compared to other tools we trialed, the ramp-up time was basically zero.",
    image: "/generated/image-a-professional-headshot-of-a-black-woman.webp"
  },
  {
    name: "Lars Delacroix",
    position: "CTO",
    company: "Bitmerch Systems",
    quote:
      "Claude saves us over 40 hours a week in internal QA and documentation tasks. Even with the Pro Max plan—it's 10x ROI at minimum.",
    image: "/generated/image-a-professional-headshot-of-an-east-asian.webp"
  },
  {
    name: "Kamryn Varro",
    position: "Operations Lead",
    company: "Leafry Supply",
    quote:
      "We were nervous about price, but Claude outperforms two other AI platforms we tried—at half the cost and with better answers. It pays for itself in days.",
    image: "/generated/image-a-professional-headshot-of-a-hispanic-wo.webp"
  }
]}
/>

<CallToAction
  title="AI you can trust. From the team building for humanity’s future."
  subtitle="Smarter work starts with Claude"
  description="Experience AI designed for your success—helping you write, code, and research faster, always grounded in safety and responsible development. Ready to see real value? Join other forward-thinking teams using Claude to elevate their work today."
  imageSrc="/generated/image-a-happy-business-customer-in-a-bright-an.webp"
  callsToAction=[
    { href: "/signup", label: "Get started", variant: "primary" },
    { href: "/contact", label: "Talk to sales", variant: "secondary" }
  ]
/>
