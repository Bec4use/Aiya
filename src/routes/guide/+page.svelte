<script context="module">
export async function load() {
        const res = await fetch('https://jsonplaceholder.typicode.com/posts')
        .then((x)=>{console.log(x)})
        const guides = await res.json()
        console.log(guides);
        if (res.ok) {
            return guides;
        }
        return {
            status: res.status,
            error: new Error ('Could not fetch the guides')
        }
    }
</script>
<script>
import Layout from "./__layout.reset.svelte"
</script>

<Layout>
    {#await load()}
        <p>loading</p>
    {:then guides} 
        {#each guides as guide}
        <li>
            <a href="/">{guide.id}.{guide.title}</a>
        </li>
        {/each}
    {:catch error}
  <p style="color: red">{error.message}</p>
    {/await}
<div class="guides">

</div>
</Layout>

<style>
    a {
        display: block;
        text-align: center;
        padding: 10px 20px;
        font-size: larger;
        border: 1px solid;
        border-radius: 2px;
        margin: 10px;
        text-decoration: none;
        
    }
    .guides {
        display: grid;
        justify-content: center;
    }
</style>