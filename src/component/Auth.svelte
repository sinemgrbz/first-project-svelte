<script>
    let user = {
        loggedIn : false
    }

    const login = () => {
        user.loggedIn = true
    }

    const logout = () => {
        user.loggedIn = false
    }

</script>

{#if user.loggedIn}
    <button on:click={logout}>çıkış yap</button>
{:else}
    <button on:click={login}>giriş yap</button>
{/if}