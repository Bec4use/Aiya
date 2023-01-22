<script>
    import Title from '$lib/+page.svelte'
    import '../../Style/global.css'
</script>

<header>
    <nav>
        <Title title="AIYA GAMING Guide"/>
        <div class="links">
            <a href="/">Home</a>
            <a href="../about">About</a>
            <a href="../guide">Guide</a>
        </div>
    </nav>
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
        text-align: center;
        background-color: rgba(0, 0, 0, 0.1);
    }
    main {
        max-width: 960px;
        margin: 20px auto;
    }
    footer {
        text-align: center;
    }
    .links{
        margin-left: auto;
    }
    a{
        margin-left: 10px;
    }
    nav {
        display: flex;
        align-items: center;
        margin: 0 auto;
    }
</style>