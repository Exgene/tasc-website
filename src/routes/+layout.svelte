<script lang="ts">
	import { navigating } from '$app/stores';
	import { called, user, userData, userLoaded } from '$lib/firebase/firebase';
	import darkLoader from '$lib/loader/spinnerDark.svg';
	import lightLoader from '$lib/loader/spinnerLight.svg';
	import { loading } from '$lib/stores/loading';
	import { darkTheme } from '$lib/stores/theme';
	import '../app.css';

	/* Subscribe to stores in root layout */
	$darkTheme;
	$user;
	$userData;
	$userLoaded;
	$called;
	$: $loading = !!$navigating;
</script>

{#if $loading}
	{#if $darkTheme}
		<div class="flex h-[100vh] items-center justify-center"><img src={darkLoader} alt="spinDark" class=" w-24" /></div>
	{:else}
		<div class="flex h-[100vh] items-center justify-center"><img src={lightLoader} alt="spinLight" class=" w-24" /></div>
	{/if}
{:else}
	<slot />
{/if}
