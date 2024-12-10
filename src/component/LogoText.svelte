<script>
    export let name 
</script>

<div>
    <h1>{name.toUpperCase()}</h1>
</div>

<style>

    /* compopnent base css */
     .h1 {
       color: #888;
     }
   
     /* global bir css için */
     :global(h1) {
       color: red;
     }
   </style>