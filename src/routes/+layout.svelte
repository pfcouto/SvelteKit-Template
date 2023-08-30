<script lang="ts">
	import '../app.postcss';
	import '../app.postcss';
	import { page } from '$app/stores';
	import { onMount } from 'svelte';
	import {
		Navbar,
		NavBrand,
		NavLi,
		NavUl,
		NavHamburger,
		Sidebar,
		SidebarGroup,
		SidebarBrand,
		SidebarCta,
		SidebarDropdownItem,
		SidebarItem,
		SidebarWrapper,
		SidebarDropdownWrapper,
		Drawer,
		CloseButton,
		DarkMode,
		DropdownHeader,
		Avatar,
		Dropdown,
		DropdownItem,
		DropdownDivider
	} from 'flowbite-svelte';
	import { sineIn } from 'svelte/easing';
	import { Icon } from 'flowbite-svelte-icons';

	let hidden2 = true;
	let spanClass = 'flex-1 ml-3 whitespace-nowrap';
	let transitionParams = {
		x: -320,
		duration: 200,
		easing: sineIn
	};
</script>

<Navbar let:hidden let:toggle>
	<NavHamburger on:click={() => (hidden2 = false)} btnClass="ml-3" />
	<NavBrand href="/">
		<span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">PFCouto</span>
	</NavBrand>
	<div class="flex items-center md:order-2">
		<NavUl {hidden}>
			<!-- <NavLi href="/">Home</NavLi> -->
			<a
				href="https://www.linkedin.com/in/pedro-couto-2b7301222/"
				class="focus:outline-none whitespace-normal m-0.5 rounded-lg focus:ring-2 p-2.5 focus:ring-gray-400 hover:bg-gray-100 dark:hover:bg-gray-600 hidden sm:inline-block dark:hover:text-white hover:text-gray-900"
				aria-label="View on GitHub"
				target="_blank"
				rel="noreferrer"
			>
				<Icon name="linkedin-solid" />
			</a>
			<a
				href="https://github.com/pfcouto"
				class="focus:outline-none whitespace-normal m-0.5 ml-2 rounded-lg focus:ring-2 p-2.5 focus:ring-gray-400 hover:bg-gray-100 dark:hover:bg-gray-600 hidden sm:inline-block dark:hover:text-white hover:text-gray-900"
				aria-label="View on GitHub"
				target="_blank"
				rel="noreferrer"
			>
				<Icon name="github-solid" />
			</a>
			<a
				href="mailto:pedrocouto2001@gmail.com"
				class="focus:outline-none whitespace-normal m-0.5 ml-2 rounded-lg focus:ring-2 p-2.5 focus:ring-gray-400 hover:bg-gray-100 dark:hover:bg-gray-600 hidden sm:inline-block dark:hover:text-white hover:text-gray-900"
				aria-label="View on GitHub"
				target="_blank"
				rel="noreferrer"
			>
				<Icon name="mail-box-solid" />
			</a>
		</NavUl>
		<DarkMode />
		<NavHamburger on:click={toggle} class1="w-full md:flex md:w-auto md:order-1" />
	</div>
	<!-- <Dropdown placement="bottom" triggeredBy="#avatar-menu">
		<DropdownHeader>
			<span class="block text-sm">Bonnie Green</span>
			<span class="block truncate text-sm font-medium">name@flowbite.com</span>
		</DropdownHeader>
		<DropdownItem>Dashboard</DropdownItem>
		<DropdownItem>Settings</DropdownItem>
		<DropdownItem>Earnings</DropdownItem>
		<DropdownDivider />
		<DropdownItem>Sign out</DropdownItem>
	</Dropdown> -->
</Navbar>

<Drawer transitionType="fly" {transitionParams} bind:hidden={hidden2} id="sidebar2">
	<div class="flex items-center">
		<h5
			id="drawer-navigation-label-3"
			class="text-base font-semibold text-gray-500 uppercase dark:text-gray-400"
		>
			Menu
		</h5>
		<CloseButton on:click={() => (hidden2 = true)} class="mb-4 dark:text-white" />
	</div>
	<Sidebar>
		<SidebarWrapper divClass="overflow-y-auto py-4 px-3 rounded dark:bg-gray-800">
			<SidebarGroup>
				<SidebarItem label="Dashboard">
					<svelte:fragment slot="icon">
						<Icon
							name="chart-pie-solid"
							class="w-5 h-5 text-gray-500 transition duration-75 dark:text-gray-400 group-hover:text-gray-900 dark:group-hover:text-white"
						/>
					</svelte:fragment>
				</SidebarItem>
				<SidebarDropdownWrapper label="E-commerce">
					<svelte:fragment slot="icon">
						<Icon
							name="shopping-cart-solid"
							class="w-5 h-5 text-gray-500 transition duration-75 dark:text-gray-400 group-hover:text-gray-900 dark:group-hover:text-white"
						/>
					</svelte:fragment>
					<SidebarDropdownItem label="Products" />
					<SidebarDropdownItem label="Billing" />
					<SidebarDropdownItem label="Invoice" />
				</SidebarDropdownWrapper>
				<SidebarItem label="Kanban" {spanClass}>
					<svelte:fragment slot="icon">
						<Icon
							name="grid-solid"
							class="w-5 h-5 text-gray-500 transition duration-75 dark:text-gray-400 group-hover:text-gray-900 dark:group-hover:text-white"
						/>
					</svelte:fragment>
					<svelte:fragment slot="subtext">
						<span
							class="inline-flex justify-center items-center px-2 ml-3 text-sm font-medium text-gray-800 bg-gray-200 rounded-full dark:bg-gray-700 dark:text-gray-300"
						>
							Pro
						</span>
					</svelte:fragment>
				</SidebarItem>
				<SidebarItem label="Inbox" {spanClass}>
					<svelte:fragment slot="icon">
						<Icon
							name="mail-box-solid"
							class="w-5 h-5 text-gray-500 transition duration-75 dark:text-gray-400 group-hover:text-gray-900 dark:group-hover:text-white"
						/>
					</svelte:fragment>
					<svelte:fragment slot="subtext">
						<span
							class="inline-flex justify-center items-center p-3 ml-3 w-3 h-3 text-sm font-medium text-primary-600 bg-primary-200 rounded-full dark:bg-primary-900 dark:text-primary-200"
						>
							3
						</span>
					</svelte:fragment>
				</SidebarItem>
				<SidebarItem label="Users">
					<svelte:fragment slot="icon">
						<Icon
							name="users-solid"
							class="w-5 h-5 text-gray-500 transition duration-75 dark:text-gray-400 group-hover:text-gray-900 dark:group-hover:text-white"
						/>
					</svelte:fragment>
				</SidebarItem>
				<SidebarItem label="Products">
					<svelte:fragment slot="icon">
						<Icon
							name="bag-solid"
							class="w-5 h-5 text-gray-500 transition duration-75 dark:text-gray-400 group-hover:text-gray-900 dark:group-hover:text-white"
						/>
					</svelte:fragment>
				</SidebarItem>
				<SidebarItem label="Sign In">
					<svelte:fragment slot="icon">
						<Icon
							name="arrow-right-to-bracket-solid"
							class="w-5 h-5 text-gray-500 transition duration-75 dark:text-gray-400 group-hover:text-gray-900 dark:group-hover:text-white"
						/>
					</svelte:fragment>
				</SidebarItem>
				<SidebarItem label="Sign Up">
					<svelte:fragment slot="icon">
						<Icon
							name="file-edit-solid"
							class="w-5 h-5 text-gray-500 transition duration-75 dark:text-gray-400 group-hover:text-gray-900 dark:group-hover:text-white"
						/>
					</svelte:fragment>
				</SidebarItem>
			</SidebarGroup>
		</SidebarWrapper>
	</Sidebar>
</Drawer>

<slot />

<style>
	:focus {
		outline: none;
	}
</style>
