<script>
  import Title from "$lib/title.svelte";
  import "../../styles/global.css";
</script>

<header>
  <nav>
    <Title title="Gnana Gaming Guides" />
    <div class="links">
      <a href="/">Home</a>
      <a href="/about">About</a>
      <a href="/guides">Guides</a>
    </div>
  </nav>
</header>

<main>
  <slot />
</main>

<footer>
  <p>CopyRight</p>
</footer>

<style>
  header {
    text-align: center;
    background-color: rgba(14, 49, 70, 0.171);
  }
  main {
    max-width: 960px;
    margin: 20px auto;
  }

  .links {
    margin-left: auto;
  }

  a {
    margin-left: 10px;
  }

  footer {
    text-align: center;
  }

  nav {
    display: flex;
    align-items: center;
    max-width: 960px;
    margin: 0 auto;
  }
</style>
