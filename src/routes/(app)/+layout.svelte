<script>
    import Sidebar from "$components/Sidebar.svelte";
    import SidebarItem from "../../components/SidebarItem.svelte";

    import icoPlay from "$lib/assets/HC-Play.svg";
    import icoRules from "$lib/assets/HC-Rules.svg";
    import icoCollapse from "$lib/assets/HC-Collapse.svg";
    import icoSettings from "$lib/assets/HC-Settings.svg";
    import icoLogOut from "$lib/assets/HC-LogOut.svg";
    import icoHelp from "$lib/assets/HC-Help.svg";

    let isLoggedIn = true;
</script>

<div class="app-content">
    <Sidebar --sb-width=200px>
        <!-- <div class="sb-logo" slot="sb-logo"></div> -->
        <div class="sb-top" slot="sb-top">
            <SidebarItem text="Play" func="link" link="/play" size="big" img={icoPlay}/>
            <SidebarItem text="Rules" func="link" link="/rules" size="big" img={icoRules}/>
        </div>
        <div slot="sb-bottom">
            {#if (isLoggedIn)}
                <SidebarItem text="Collapse" func="collapse" size="small" img={icoCollapse}/>
                <SidebarItem text="Settings" func="link" link="/settings" size="small" img={icoSettings}/>
                <SidebarItem text="Log Out" func="logout" size="small" img={icoLogOut}/>
                <SidebarItem text="Help" func="link" link="/help" size="small" img={icoHelp}/>
            {:else}
                <SidebarItem text="Light UI" func="lightUI" size="small"/>
                <SidebarItem text="English" func="lang" size="small"/>
                <SidebarItem text="Help" func="link" link="/help" size="small"/>
            {/if}
        </div>
    </Sidebar>
    <div class="app-page">
        <slot />
    </div>
</div>

<style>
    .app-content{
        display: flex;
        flex-direction: row;
        height: 100%;
        background: var(--gray-1);
    }
    .app-page{
        flex-grow: 1;
    }
</style>