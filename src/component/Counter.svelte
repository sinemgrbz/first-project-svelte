<script>
    export let count =0

    // let double = count * 2 >> bu şekilde olmaz
    // computed value kullanımı
    $: double = count * 2

    const handleCount = () => {
        count +=1
    }
</script>

<button on:click={handleCount}>
    bu butona {count} kez tıklandı
</button>

<br>
{#if count === 10}
    <p style="background:red;">tebrikler {count} kez tıklandı</p>

{:else if count===20}
    <p style="background:lime;">tebrikler {count} kez tıklandı</p>
    
{:else}
    <p style="background:green;">tıklamaya devam et</p>

{/if}

<!-- <p>bu değerin iki katı {count * 2}</p> -->
 <p> deneme{double}</p>