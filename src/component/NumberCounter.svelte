<script>
    let numbers =[1,2,3,4]

    const clickHandle = ()=> {
        // numbers.push(numbers.length +1)
        numbers = [...numbers, numbers.length +1]
    }


    $: totalNumber = numbers.reduce((prev, current) => prev += current, 0)

</script>


<button on:click={clickHandle}>
    ekle
</button>

<p>toplam numara = {totalNumber}</p>