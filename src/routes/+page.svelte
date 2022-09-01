<script>
	import Newsletter from '../components/Newsletter.svelte';
	import FeatureCard from '../components/FeatureCard.svelte';
	import {
		SITE_URL,
		REPO_URL,
		SITE_TITLE,
		SITE_DESCRIPTION,
		DEFAULT_OG_IMAGE,
		MY_TWITTER_HANDLE
	} from '$lib/siteConfig';
	export const prerender = true; // index page is most visited, lets prerender

</script>

<svelte:head>
	<title>{SITE_TITLE}</title>
	<link rel="canonical" href={SITE_URL} />
	<link rel="alternate" type="application/rss+xml" href={SITE_URL + '/rss.xml'} />
	<meta property="og:url" content={SITE_URL} />
	<meta property="og:type" content="article" />
	<meta property="og:title" content={SITE_TITLE} />
	<meta name="Description" content={SITE_DESCRIPTION} />
	<meta property="og:description" content={SITE_DESCRIPTION} />
	<meta property="og:image" content={DEFAULT_OG_IMAGE} />
	<meta name="twitter:card" content="summary" />
	<meta name="twitter:creator" content={'@' + MY_TWITTER_HANDLE} />
	<meta name="twitter:title" content={SITE_TITLE} />
	<meta name="twitter:description" content={SITE_DESCRIPTION} />
	<meta name="twitter:image" content={DEFAULT_OG_IMAGE} />
</svelte:head>

<div
	class="mx-auto flex max-w-2xl flex-col items-start justify-center border-gray-200 px-4 pb-16 dark:border-gray-700 sm:px-8"
>
	<div class="flex flex-col-reverse items-start sm:flex-row">
		<div class="flex flex-col pr-8">
			<h1 class="mb-3 text-3xl font-bold tracking-tight text-black dark:text-white md:text-6xl">

				<!-- <span
					class="relative ml-2 inline-block before:absolute before:-inset-1 before:block before:-skew-y-3 before:bg-red-500"
				> -->
					<span class="relative skew-y-3 text-yellow-400">{SITE_TITLE}</span>
				<!-- </span> -->
				
			</h1>
			<h2 class="mb-4 text-gray-700 dark:text-gray-200">
				<p> I am switching up the blog. A lot of the old posts aren't here yet but they will be eventually. If you must see them, check out <a href="https://github.com/technovangelist/technovangelist.com/tree/master/src/posts">the older GitHub repo</a>. </p>
        <p>Why the need to change? I tried to post something to the old blog and Netlify failed to publish. It was an older Gatsby and I couldn't be bothered to relearn and upgrade so I just grabbed a cool looking sample of a Svelte site and went with it.</p>
			</h2>
			
		</div>
		<!-- <div
				class="w-[80px] h-[80px] rounded-full sm:w-[176px] sm:h-[136px] relative mb-8 sm:mb-0 mr-auto bg-cyan-300 bg-opacity-25"
			/> -->
	</div>

	<section class="mb-16 w-full">

		<a
			class="mt-8 flex h-6 rounded-lg leading-7 text-gray-600 transition-all dark:text-gray-400 dark:hover:text-gray-200"
			href="/blog"
			>See latest posts<svg
				xmlns="http://www.w3.org/2000/svg"
				fill="none"
				viewBox="0 0 24 24"
				class="ml-1 h-6 w-6"
				><path
					stroke="currentColor"
					stroke-linecap="round"
					stroke-linejoin="round"
					stroke-width="2"
					d="M17.5 12h-15m11.667-4l3.333 4-3.333-4zm3.333 4l-3.333 4 3.333-4z"
				/></svg
			></a
		>
	</section>
	<!-- <Newsletter /> -->
</div>
