<script>
	import { P, Span } from 'flowbite-svelte';
</script>

<div class="p-8">
	<div class="flex justify-center">
		<div class="w-1/5">
			<div class="flex flex-col">
				<P>Hello! I'm Pedro Couto, a 22 years.</P>
				<P>MSc student and Researcher in Computer Engineering @Polytechnic of Leiria.</P>
				<div class="inline">
					<img
						src="/images/linux-logo.png"
						width="30"
						alt="Linux logo"
						style="margin-right: 8px;"
					/>
					<span>user.</span>
				</div>
				<div class="mt-10">
					<img src="/images/pedro.png" alt="Pedro Couto" />
				</div>
			</div>
		</div>
	</div>
</div>

<style>
	.inline {
		display: inline-flex;
		align-items: center;
	}
</style>
