<script>
	import { Card, Img } from 'flowbite-svelte';

	let baseIconsURL = 'https://cdn.simpleicons.org/';
	let skillsWithIcons = [
		{
			name: 'Flutter',
			icon: `${baseIconsURL}/flutter`,
			site: 'https://flutter.dev'
		},
		{
			name: 'Dart',
			icon: `${baseIconsURL}/dart`,
			site: 'https://dart.dev'
		},
		{
			name: 'Kotlin',
			icon: `${baseIconsURL}/kotlin`,
			site: 'https://kotlinlang.org'
		},
		{
			name: 'Javascript',
			icon: `${baseIconsURL}/javascript`,
			site: 'https://developer.mozilla.org/en-US/docs/Web/JavaScript'
		},
		{
			name: 'SvelteKit',
			icon: `${baseIconsURL}/svelte`,
			site: 'https://kit.svelte.dev/'
		},
		{
			name: 'Git',
			icon: `${baseIconsURL}/git`,
			site: 'https://git-scm.com/'
		},
		{
			name: 'Firebase',
			icon: `${baseIconsURL}/firebase`,
			site: 'https://firebase.google.com/'
		}
	];
</script>

<!-- Education Card -->
<Card class="mt-5 mx-auto md:mx-0">
	<div class="heading flex">
		<svg
			class="w-6 h-6 mr-2 text-ctp-mauve"
			aria-hidden="true"
			fill="none"
			stroke="currentColor"
			stroke-width="1.5"
			viewBox="0 0 24 24"
			xmlns="http://www.w3.org/2000/svg"
		>
			<path
				d="M4.26 10.147a60.436 60.436 0 00-.491 6.347A48.627 48.627 0 0112 20.904a48.627 48.627 0 018.232-4.41 60.46 60.46 0 00-.491-6.347m-15.482 0a50.57 50.57 0 00-2.658-.813A59.905 59.905 0 0112 3.493a59.902 59.902 0 0110.399 5.84c-.896.248-1.783.52-2.658.814m-15.482 0A50.697 50.697 0 0112 13.489a50.702 50.702 0 017.74-3.342M6.75 15a.75.75 0 100-1.5.75.75 0 000 1.5zm0 0v-3.675A55.378 55.378 0 0112 8.443m-7.007 11.55A5.981 5.981 0 006.75 15.75v-1.5"
				stroke-linecap="round"
				stroke-linejoin="round"
			/>
		</svg>
		<h3 class="tracking-tight font-semibold text-gray-900 dark:text-ctp-mauve">Education</h3>
	</div>
	<div
		class="items-center mt-5 hover:scale-[1.02] transition-transform ease-in-out duration-200 hover:bg-gray-100 dark:hover:bg-gray-700 p-2 hover:rounded-md cursor-pointer"
	>
		<a
			href="https://maktabahjafariyah.org"
			class="text-lg font-medium tracking-tight text-gray-900 dark:text-white hover:text-latte-lavender dark:hover:text-mocha-lavender focus-visible:text-mocha-lavender"
		>
			BS, Information Technology
		</a>
		<p class="text-sm mt-1 font-normal tracking-tight text-gray-900 dark:text-white">
			PHINMA-University of Pangasinan
		</p>
		<p class="text-sm mt-1 font-normal tracking-tight text-gray-700 dark:text-gray-300">
			2021 - 2025
		</p>
	</div>
</Card>
<!-- skills card -->
<Card class="mt-5 mx-auto md:mx-0">
	<div class="heading flex">
		<svg
			class="w-6 h-6 mr-2 text-ctp-mauve"
			aria-hidden="true"
			fill="none"
			stroke="currentColor"
			stroke-width="1.5"
			viewBox="0 0 24 24"
			xmlns="http://www.w3.org/2000/svg"
		>
			<path
				d="M16.862 4.487l1.687-1.688a1.875 1.875 0 112.652 2.652L6.832 19.82a4.5 4.5 0 01-1.897 1.13l-2.685.8.8-2.685a4.5 4.5 0 011.13-1.897L16.863 4.487zm0 0L19.5 7.125"
				stroke-linecap="round"
				stroke-linejoin="round"
			/>
		</svg>
		<h3 class="tracking-tight font-semibold text-gray-900 dark:text-ctp-mauve">Skills</h3>
	</div>
	<div class="items-center mt-5">
		<!-- map skills and icons -->
		{#each skillsWithIcons as skill}
			<a
				href={skill.site}
				class="flex space-x-3 items-center hover:bg-gray-100 dark:hover:bg-gray-600 p-3 rounded-md cursor-pointer hover:scale-[1.02] transition-transform ease-in-out duration-200"
			>
				<Img src={skill.icon} alt={skill.name + ' logo'} class="h-8 w-8" />
				<h4
					class="text-base tracking-tight text-gray-900 dark:text-white hover:text-latte-lavender dark:hover:text-mocha-lavender focus-visible:text-mocha-lavender"
				>
					{skill.name}
				</h4>
			</a>
		{/each}
	</div>
</Card>
