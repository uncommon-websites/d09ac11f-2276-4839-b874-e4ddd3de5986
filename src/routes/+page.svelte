<script lang="ts">
	// Components
	import UseCases from "$lib/components/layout/UseCases.svelte";
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import Hero from "$lib/components/layout/hero-sections/Hero.svelte";
</script>

<Hero
	title="Elevate your business with thoughtful design"
	subtitle="Solutions that enhance user experience, and improve visual communication."
	imageSrc="/sample.png"
	generating
/>
<LogoScroller label="" generating />

<Summary
	title="What we do"
	text="Anthropic builds trustworthy AI that helps people solve problems, write, and code. Our models are designed with safety and responsibility in mind, so businesses and individuals can work smarter and more confidently."
/>

<Testimonials
	testimonials={[
		{
			name: "Theo Varela",
			position: "Head of Engineering",
			company: "Draftform",
			quote: "Claude cuts 12–15 hours a week from our code review cycle. It flags edge cases, suggests tests, and adds docstrings our team used to miss.",
			image: "/generated/image-man-in-a-modern-office-wearing-a-casual-.webp"
		},
		{
			name: "Sohini Marek",
			position: "Director of Clinical AI",
			company: "Xymetri",
			quote: "We rely on Claude because it actually respects our research boundaries. It refuses unsafe requests before we have to double-check. That saves us time and liability.",
			image: "/generated/image-woman-in-a-lab-wearing-glasses-and-a-res.webp"
		},
		{
			name: "Ren Otani",
			position: "VP of Product",
			company: "Zepho Core",
			quote: "We integrated Claude’s API for internal support and budgeting tasks. It replaced expensive software and cut monthly ops costs by 26%.",
			image: "/generated/image-non-binary-person-in-a-coworking-space-d.webp"
		}
	]}
/>

<Features
	title="AI that works for you"
	subtitle="Core features that set Claude apart"
	features={[
		{
			title: "Human-first AI design",
			description: "Every Claude model is made to serve people—safety and meaningful benefit come first, not after-thoughts."
		},
		{
			title: "Advanced Claude 4 models",
			description: "Claude helps you code, write, and research with powerful models built for both complex tasks and everyday speed."
		},
		{
			title: "Responsible by default",
			description: "We are fully transparent about how we train, test, and deploy AI—responsibility is built into everything we do."
		},
		{
			title: "Seamless developer tools",
			description: "APIs and apps let you build, launch, or scale new ideas fast—so you spend less time wrestling with code."
		},
		{
			title: "Works everywhere you do",
			description: "Claude integrates with Google Workspace, web resources, and business tools to fit right into your existing workflow."
		},
		{
			title: "Openness and research",
			description: "We share alignment science, safety work, and ongoing research so you can build on a foundation you trust."
		}
	]}
/>

<UseCases
	title="Use Cases"
	subtitle="Real-world applications for your business needs"
	useCases={[
		{
			title: "AI-powered compliance reviews",
			description: "Use Claude to scan contracts, policies, or technical documentation for gaps, inconsistencies, or regulatory risks. Save hours of manual checks with structured, explainable outputs.",
			image: "/generated/image-a-diverse-business-team-engaged-in-a-dis.webp",
			link: {
				href: "/use-cases/compliance",
				label: "Learn more"
			}
		},
		{
			title: "Fast technical support summaries",
			description: "Summarize support tickets, extract key errors, and provide suggested fixes your agents can trust. Claude helps teams respond faster across channels with consistent answers.",
			image: "/generated/image-a-group-of-people-working-together-helpi.webp",
			link: {
				href: "/use-cases/support",
				label: "Learn more"
			}
		},
		{
			title: "Custom codebase Q&A",
			description: "Let Claude answer detailed questions about your codebase by uploading files directly or connecting to your repo. Ideal for onboarding developers, reviewing architecture, and understanding legacy code.",
			image: "/generated/image-a-team-of-developers-focused-on-their-la.webp",
			link: {
				href: "/use-cases/codebase-qna",
				label: "Learn more"
			}
		}
	]}
/>

<AboutTeaser />
<CallToAction
  title="AI you can trust for thoughtful, productive work"
  subtitle="Safety, speed, and collaboration—always built in"
  description="Claude helps you code faster, write clearer, and research smarter—without compromising on safety. Built with responsible AI principles at its core, Claude gives individuals and teams the peace of mind to work confidently."
  imageSrc="/generated/image-a-cheerful-professional-in-a-contemporar.webp"
  callsToAction={[
    { href: "/get-started", label: "Try Claude free", variant: "primary" },
    { href: "/contact", label: "Contact sales", variant: "secondary" }
  ]}
/>

