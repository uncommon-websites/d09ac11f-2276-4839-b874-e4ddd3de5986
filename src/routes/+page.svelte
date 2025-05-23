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
	generating
	title="Use Cases"
	subtitle="Real-world applications for your business needs"
	useCases={[
		{
			title: "Streamlined Workflows",
			description:
				"Automate repetitive tasks and connect systems to improve productivity with our industry-leading 87% time savings.",
			image:
				"https://images.unsplash.com/photo-1552664730-d307ca884978?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2940&q=80",
			link: {
				href: "/use-cases/workflows",
				label: "Learn more"
			}
		},
		{
			title: "Data Analysis",
			description:
				"Extract meaningful insights from your data with powerful analytical tools backed by proprietary AI algorithms that are 3x more accurate than competitors.",
			image:
				"https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2488&q=80",
			link: {
				href: "/use-cases/data-analysis",
				label: "Explore analytics"
			}
		},
		{
			title: "Secure Collaboration",
			description:
				"Work together seamlessly while maintaining strict data privacy standards with our zero-knowledge architecture and military-grade encryption.",
			image:
				"https://images.unsplash.com/photo-1522202176988-66273c2fd55f?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2940&q=80",
			link: {
				href: "/use-cases/collaboration",
				label: "See security features"
			}
		}
	]}
/>

<AboutTeaser generating />
<CallToAction generating />
