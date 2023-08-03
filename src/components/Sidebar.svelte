<script>
	// import NavbarItem from './NavbarItem.svelte';
	// import NavbarSection from './NavbarSection.svelte';
</script>

<div class="sb-sidebar">
	<div class="sb-logo">
		<slot name="sb-logo" />
	</div>
	<div class="sb-top">
		<slot name="sb-top" />
	</div>
	<div class="sb-spacer"></div>
	<div class="sb-bottom">
		<slot name="sb-bottom" />
	</div>
</div>

<style>
	.sb-sidebar {
		width: var(--sb-width);
		background: var(--gray-2);
		padding-top: 5px;
		padding-bottom: 25px;

		display: flex;
		flex-direction: column;
	}
	.sb-logo,
	.sb-top,
	.sb-bottom {
		flex-shrink: 0;
	}
	.sb-spacer {
		flex-grow: 1;
	}
</style>

<!-- <NavbarSection title="Admin">
		<NavbarItem
			link="managers"
			name="Managers"
			classStyle="fa-sharp fa-solid fa-users sidebarIcon lightBlue"
			isActive="false"
		/>
	</NavbarSection> -->