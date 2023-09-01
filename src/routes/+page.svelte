<script>
	import { P, Span } from 'flowbite-svelte';
</script>

<div class="p-8">
	<div class="flex justify-center">
		<div class="w-80">
			<div class="flex flex-col justify-center">
				<P>Hello! My name is Pedro Couto, I'm 22 years old.</P>
				<P>Currently a MSc student and Researcher in Computer Engineering @Polytechnic of Leiria.</P
				>
				<div class="inline">
					<img
						src="/images/linux-logo.png"
						width="30"
						alt="Linux logo"
						style="margin-right: 8px;"
					/>
					<P>user.</P>
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
