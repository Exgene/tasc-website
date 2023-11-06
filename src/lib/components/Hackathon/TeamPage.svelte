<script>
	import { Input } from '$lib/components/ui/input';
	import MainButton from './MainButton.svelte';
</script>

<!-- Not in a team -->
<div class="flex h-full w-full flex-col items-center justify-center">
	<h2 class="pb-6 pt-4 font-jbExtrabold text-4xl">Team Details</h2>
	<div class="gradient_border mx-5 w-auto cursor-default bg-[#d1f2f9] bg-opacity-5 p-10 backdrop-blur-sm transition duration-300 md:w-[600px]">
		<ul class="mt-5 space-y-2">
			<p class="font-jbRegular text-lg sm:text-2xl">Team Name : <span class="text-[#fffba4]">Team XYZ</span></p>
			<p class="font-jbRegular text-lg sm:text-2xl">Team ID : <span class="text-[#fffba4]">****</span></p>
			<h2 class="bg-gradient-to-tr pt-4 font-jbExtrabold text-2xl drop-shadow-[0_0_0.15rem_#d2b863]">Team Members</h2>
			<div class="grid grid-cols-2 grid-rows-2 gap-4">
				<p class="font-jbRegular text-lg sm:text-2xl">Member 1 : <span class="text-[#fffba4]">Rajesh shankar gowda</span></p>
				<p class="font-jbRegular text-lg sm:text-2xl">Member 1 : <span class="text-[#fffba4]">Rajesh shankar gowda</span></p>
				<p class="font-jbRegular text-lg sm:text-2xl">Member 1 : <span class="text-[#fffba4]">Rajesh shankar gowda</span></p>
				<p class="font-jbRegular text-lg sm:text-2xl">Member 1 : <span class="text-[#fffba4]">Rajesh shankar gowda</span></p>
			</div>
		</ul>
	</div>

	<MainButton hrefId="/createteam">Solution Submission</MainButton>
</div>
