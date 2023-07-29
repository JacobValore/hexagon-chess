<div class="app-content">
    <div class="app-sidebar">
        Sidebar Text
    </div>
    <div class="app-page">
        <slot />
    </div>
</div>

<style>
    .app-content{
        display: flex;
        flex-direction: row;
        height: 100%;

        /* background: var(); */
    }
    .app-sidebar{
        flex-shrink: 0;
        width: 150px;
    }
    .app-page{
        flex-grow: 1;
    }
</style>