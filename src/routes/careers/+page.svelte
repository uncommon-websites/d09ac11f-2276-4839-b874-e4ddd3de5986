<script lang="ts">
	// Types

	// Components
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Card from "$lib/components/ui/Card.svelte";
	import JobList, { type JobOpening } from "./JobList.svelte";

	// Icons
	import IconBriefcase from "~icons/lucide/briefcase";
	import IconUsers from "~icons/lucide/users";
	import IconHeart from "~icons/lucide/heart";
	import IconGlobe from "~icons/lucide/globe";

	// Constants
	const SECTION_BASE_CLASSES = "section-py section-px container mx-auto";
	const GRADIENT_BG_CLASSES =
		"bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800";
	const ICON_CONTAINER_CLASSES =
		"bg-primary-50 text-primary-600 dark:bg-primary-950 dark:text-primary-400 flex items-center justify-center rounded-full";

	const benefits = [
  {
    title: "Make meaningful impact",
    description: "Shape technology that prioritizes humanity's long-term well-being—your work powers safe, responsible AI for society.",
    icon: IconHeart
  },
  {
    title: "Principled innovation",
    description: "Thrive in an environment where science, ethics, and product decisions align. Collaboration, transparency, and care drive every project.",
    icon: IconUsers
  },
  {
    title: "Room to grow, from anywhere",
    description: "Advance your skills through research, cross-functional teamwork, and continuous learning, all on a remote-first team.",
    icon: IconBriefcase
  }
];

	const openings: JobOpening[] = [
		// Engineering
		{
			title: "Senior Frontend Developer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Backend Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Design Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Design
		{
			title: "UX/UI Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Product
		{
			title: "Product Manager",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Analyst",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Marketing
		{
			title: "Marketing Specialist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Content Strategist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Social Media Manager",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		}
	];

	const employeeTestimonials = [
  {
    name: "Aarya Sen",
    position: "Product Designer",
    company: "Design",
    quote: "As a product designer, I've had real scope to lead explorations and shape solutions—even early on. It's incredibly motivating to work on a team where people trust your instincts, but are always around to collaborate.",
    image: "/generated/image-aarya-sen-product-designer.jpg"
  },
  {
    name: "Darius Knight",
    position: "Engineering Lead",
    company: "Platform",
    quote: "I've seen major technical growth since joining. Leading projects is encouraged here, and there's always room to try new approaches and learn from others across engineering, AI research, and beyond.",
    image: "/generated/image-darius-knight-engineering-lead.jpg"
  },
  {
    name: "Em Casey",
    position: "Marketing Coordinator",
    company: "Brand and Communications",
    quote: "Something clicked for me here—the transparency, the focus on thoughtful communication, and how leadership genuinely listens. I feel safe being myself and balancing great work with a healthy life.",
    image: "/generated/image-a-white-non-binary-marketing-coordinator.webp"
  }
];

	const processSteps = [
  {
    step: 1,
    title: "Apply online",
    description: "Submit your resume and a short note about why you're excited to join Anthropic. We thoughtfully review every application."
  },
  {
    step: 2,
    title: "Initial conversation",
    description: "If there’s a potential fit, a recruiter will reach out for a quick chat about your background and interests."
  },
  {
    step: 3,
    title: "Interviews",
    description: "Meet the team over video calls, which may include technical or role-specific discussions."
  },
  {
    step: 4,
    title: "Decision and offer",
    description: "We communicate outcomes promptly and provide feedback, aiming for a process that's clear and welcoming."
  }
];

	const values = [
  {
    icon: IconHeart,
    title: "Principled innovation",
    description: "We make every decision through the lens of trust, impact, and long-term safety."
  },
  {
    icon: IconUsers,
    title: "Science and curiosity",
    description: "We think rigorously, share openly, and learn from each other every day."
  },
  {
    icon: IconGlobe,
    title: "Care and honesty",
    description: "Transparency and respect shape how we collaborate and build together."
  }
];
</script>

<!-- Hero Section -->

<SecondaryHero
	title="Build AI that makes a difference"
	subtitle="Join a team shaping safe, human-centered technology"
	imageSrc="/generated/image-a-diverse-team-of-employees-collaboratin.webp"
/>

<!-- Why Join Us Section -->
<section class={SECTION_BASE_CLASSES}>
	<SectionHeader title="Why join us?" subtitle="Build your career while making an impact" />

	<div class="mt-16 grid gap-4 md:grid-cols-3">
		{#each benefits as benefit}
			<Card {...benefit} />
		{/each}
	</div>
</section>

<!-- Culture Section -->
<Culture {values} />

<Testimonials testimonials={employeeTestimonials} />

<!-- Application Process -->
<section class={SECTION_BASE_CLASSES}>
	<div class="mx-auto">
		<h2 class="text-title1 mb-16">Our application process</h2>

		<div class="grid gap-12 md:grid-cols-3">
			{#each processSteps as { step, title, description }, i}
				<div class="flex flex-col">
					<div class="{ICON_CONTAINER_CLASSES} mb-6 size-11">
						<span class="text-headline">{step}</span>
					</div>
					<h3 class="text-headline mb-3">{title}</h3>
					<p class="text-body text-emphasis-low">{description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
<!-- Current Openings Section -->
<section class={GRADIENT_BG_CLASSES}>
	<div class="section-px section-py container mx-auto grid w-full items-start lg:grid-cols-2">
		<SectionHeader title="Current openings" subtitle="Find your perfect role" />

		<JobList {openings} />
	</div>
</section>
