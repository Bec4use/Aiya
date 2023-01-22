<script>
    let title = "Joe Netiphong"
    const updateTitle = () => {
        title = "JOe-AiYa"
    }
    
    import Layout from './__layout.svelte';
    
</script>
<Layout>

<div class="index">
    <h1>Welcome to {title}</h1>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Vitae blanditiis, totam nihil expedita ipsam repudiandae obcaecati voluptate accusamus beatae quo tempora, rem facere quam fugit enim iure corrupti. Recusandae voluptas perferendis debitis suscipit provident sequi sunt hic pariatur amet ipsa, id dolor sint harum asperiores culpa in dignissimos voluptate aliquam perspiciatis tempore aut praesentium? Quae, quisquam delectus. Facere, beatae ex.</p>
    <button on:click={updateTitle}>Change Title</button>
    <input type="text"bind:value={title}>
    <a href="./about">About</a>
    <a href="./guide">Guide</a>
</div>
</Layout>    
<style>
    .index {
        text-align: center;
        display: block;
        margin: 20px auto;
        padding: 20px;
    }
</style>
