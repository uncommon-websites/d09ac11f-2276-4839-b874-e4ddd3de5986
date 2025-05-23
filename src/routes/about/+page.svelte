<script lang="ts">
	// Components
	import CallToAction from "$lib/components/layout/CallToAction.svelte";

	// Icons
	import StakeholderGrid from "$lib/components/layout/StakeholderGrid.svelte";
	import Story from "./Story.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";

	// Constants
	const values = [
		{
			title: "Innovation",
			description: "Constantly challenging the status quo to create better solutions."
		},
		{
			title: "Integrity",
			description: "Building trust through transparent actions and honest communication."
		},
		{
			title: "Impact",
			description: "Measuring our success by the positive change we create for our clients."
		}
	];
</script>

<SecondaryHero
  title="AI designed for humanity’s future"
  subtitle="Responsible, helpful models for developers, businesses, and everyday work"
  imageSrc="/generated/image-a-diverse-team-of-professionals-engaged-.webp"
/>

<!-- Story Section -->
<Story
  paragraphs={[
    "We founded Anthropic because we believe AI should be built differently—from the ground up to be helpful, understandable, and safe. As AI systems became more capable, we saw a simple but urgent problem: most were getting more powerful, but not necessarily more aligned with human needs. We started Anthropic to change that—to build AI that puts people first, both in how it works and why it’s built.",
    "That’s why our work begins with a focus on human well-being. Our team—made up of researchers, engineers, and policy experts—develops AI in ways that are transparent, grounded in collaboration, and open about the challenges ahead. We’ve spent years studying how to build models that are clearer in their decision-making and more predictable in their behavior, so they can play a reliable role in everyday tools and critical decisions alike.",
    "Claude, our AI assistant, reflects those values. It helps people write better, code faster, and think more deeply—supporting individuals and teams in fields from education to software development to policy. And we’re just getting started. As our models evolve, we’ll continue to work with the broader community to make sure AI remains safe, useful, and focused on what matters: the people using it."
  ]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- StakeholderGrid Section -->
<StakeholderGrid
	stakeholderType="team"
	title="Our team."
	subtitle="Your partners in innovation."
	stakeholders={[
		{
			name: "Alex Morgan",
			position: "Founder & CEO",
			bio: "Alex founded Anthropic to build AI that prioritizes safety, responsibility, and long-term human well-being. With over a decade in AI systems design and research leadership, Alex helped launch scalable model training pipelines and advanced safety efforts—ensuring Anthropic’s work focuses on real, human benefit.",
			image:
				"/generated/image-professional-headshot-of-a-young-thought.webp"
		},
		{
			name: "Jamie Chen",
			position: "Chief Design Officer",
			bio: "Jamie builds thoughtful user experiences so AI empowers, not overwhelms. At Anthropic, Jamie leads design for usability and trust, making every Claude interaction clear, approachable, and safe—championing accessible, intuitive design across all interfaces.",
			image:
				"/generated/image-studio-headshot-of-a-diverse-creative-le.webp"
		},
		{
			name: "Taylor Wright",
			position: "Head of Engineering",
			bio: "Taylor builds and scales the infrastructure for Claude. They lead teams uniting advanced research and engineering—making safe, reliable AI work at scale and collaborating across disciplines to keep Anthropic’s systems robust and responsible.",
			image:
				"/generated/image-a-confident-and-technical-leader-capture.webp"
		}
	]}
/>

<StakeholderGrid
	stakeholderType="investor"
	title="Backed by the best."
	subtitle="Supported by leading investors who believe in responsible AI for society"
	stakeholders={[
		{
			name: "Point Nine Capital",
			image: "https://cdn.brandfetch.io/pointnine.com/w/400/h/400/logo?c=1id_elLz2Bd5Ej-dWo7"
		},
		{
			name: "TSIC Ventures",
			image: "https://cdn.brandfetch.io/tiny.vc/w/400/h/400/logo?c=1a2b3c4d5e"
		},
		{
			name: "Sequoia Capital",
			image: "https://cdn.brandfetch.io/sequoiacap.com/w/400/h/400/logo"
		}
	]}
/>

<!-- CTA Section -->
<CallToAction
	title="Ready to collaborate?"
	subtitle="Let's create something amazing"
	description="Join the companies already leveraging our expertise to transform their digital presence and achieve their business goals."
/>
