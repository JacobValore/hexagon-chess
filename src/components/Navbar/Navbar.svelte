<script>
	import NavbarItem from './NavbarItem.svelte';
	import NavbarSection from './NavbarSection.svelte';
</script>

<div id="sidebar" class="bgColorLighterDark flex-shrink">
	<!--<img class="img-fluid" src="assets/logo.png">-->

	<div id="tabs">
		<!-- 570px required to have all tabs open comletely -->
		<NavbarSection title="Management">
			<NavbarItem
				name="Homepage"
				classStyle="fa-sharp fa-solid fa-chart-pie sidebarIcon lightGreen"
				isActive="true"
			/>
			<NavbarItem
				link="creators"
				name="Creators"
				classStyle="fa-sharp fa-solid fa-users sidebarIcon lightOrange"
				isActive="false"
			/>
			<NavbarItem
				link="onlyfans"
				name="Onlyfans"
				classStyle="fa-sharp fa-solid fa-comment sidebarIcon lightBlue"
				isActive="false"
			/>
		</NavbarSection>

		<NavbarSection title="User">
			<NavbarItem
				link="account"
				name="Account"
				classStyle="fa-solid fa-user-tie sidebarIcon lightGreen"
				isActive="false"
			/>
			<NavbarItem
				link="settings"
				name="Settings"
				classStyle="fa-solid fa-wrench sidebarIcon lightOrange"
				isActive="false"
			/>
			<NavbarItem
				link="organization"
				name="Organization"
				classStyle="fa-solid fa-building sidebarIcon lightBlue"
				isActive="false"
			/>
			<NavbarItem
				link="logout"
				name="Log Out"
				classStyle="fa-solid fa-right-from-bracket sidebarIcon lightRed"
				isActive="false"
			/>
		</NavbarSection>

		<NavbarSection title="Admin">
			<NavbarItem
				link="managers"
				name="Managers"
				classStyle="fa-sharp fa-solid fa-users sidebarIcon lightBlue"
				isActive="false"
			/>
		</NavbarSection>
	</div>
</div>

<style>
	#sidebar {
		display: flex;
		flex-direction: column;
		gap: 1rem;
		height: auto;
	}
	#tabs {
		color: #b0bec5;
		padding: 1rem;
		display: flex;
		flex-direction: column;
		gap: 1rem;
	}
</style>
