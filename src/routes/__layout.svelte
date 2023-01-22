<script>
    import Title from '$lib/+page.svelte'
    import '../Style/global.css'
</script>

<header>
    <Title title="AIYA GAMING Guide"/>
</header>

<main>
    <!--Page Content-->
    <slot></slot>
</main>
<footer>
    Copyright 2023 Netiphong Ch.
</footer>

<style>
    header{
        display: flex;
        justify-content: center;
    }
    main {
        max-width: 960px;
        margin: 20px auto;
    }
    footer {
        text-align: center;
    }
</style>