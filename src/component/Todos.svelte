<script>
    import TodoItem from "./TodoItem.svelte";
    // let todos = ["todo1", "todo2", "todo3"]
    let todos = [
        {
            id:1,
            title:'todo1'
        },
        {
            id:2,
            title:'todo2'
        },
        {
            id:3,
            title:'todo3'
        }
    ]
</script>

<ul>
    {#each todos as todo, i (todo.id) }
        <TodoItem {todo} {i}/>
    {/each}
</ul>

{#each Array(5) as _, i}
    <div>{i}</div>
{/each}