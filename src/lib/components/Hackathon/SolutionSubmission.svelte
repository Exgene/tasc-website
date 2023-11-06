<script>
	import * as DropdownMenu from '$lib/components/ui/dropdown-menu';
	import { Input } from '$lib/components/ui/input';
	import { Textarea } from '$lib/components/ui/textarea';
	import { Button } from '../ui/button';
	import MainButton from './MainButton.svelte';

	let statement = '01';

	const statementID = ['01', '02', '03', '04', '05', '06', '07', '08', '09'];
	const statementNames = ['Problem Statement 1', 'Problem Statement 2', 'Problem Statement 3', 'Problem Statement 4', 'Problem Statement 5', 'Problem Statement 6', 'Problem Statement 7', 'Problem Statement 8', 'Problem Statement 9'];
</script>

<!-- Not in a team -->
<div class="flex h-full w-full flex-col items-center justify-center">
	<h2 class="pb-6 pt-4 font-jbExtrabold text-4xl">Solutions</h2>
	<div>
		<div class="flex flex-col sm:flex-row sm:gap-8">
			<Input type="text" placeholder="Solution Title" class="mb-4 h-14 w-full rounded-2xl bg-gray-600 p-4 font-jbMedium text-white sm:w-96" />
			<Input type="link" placeholder="Link to your ppt" class="mb-4 h-14 w-80 rounded-2xl bg-gray-600 p-4 font-jbMedium text-white sm:w-96" />
		</div>

		<Textarea placeholder="Solution Description" class="w-96resize-none mb-4 h-40 rounded-2xl bg-gray-600 p-4 font-jbMedium text-white sm:w-full" />
		<DropdownMenu.Root>
			<DropdownMenu.Trigger asChild let:builder>
				<Button variant="outline" builders={[builder]} class="mb-4 h-14 w-full rounded-2xl bg-gray-600 p-4 font-jbMedium text-slate-400 sm:w-full">Problem Statements</Button>
			</DropdownMenu.Trigger>
			<DropdownMenu.Content class="w-56">
				<DropdownMenu.Label>Panel Position</DropdownMenu.Label>
				<DropdownMenu.Separator />
				<DropdownMenu.RadioGroup bind:value={statement}>
					{#each statementNames as item, index}
						<DropdownMenu.RadioItem value={statementID[index]}>{item}</DropdownMenu.RadioItem>
					{/each}
				</DropdownMenu.RadioGroup>
			</DropdownMenu.Content>
		</DropdownMenu.Root>
	</div>

	<MainButton hrefId="/createteam">Submit</MainButton>
</div>
