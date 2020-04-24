<script>
  import Nav from "../components/Nav.svelte";
  export let segment;
</script>

<style lang="scss" global>
  @import "./style/global.scss";
  main {
    position: relative;
    background-color: white;
    box-sizing: border-box;
  }
</style>

<svelte:head>
  <link
    href="https://fonts.googleapis.com/css2?family=Chivo:ital,wght@0,400;0,700;0,900;1,400;1,700&family=Zilla+Slab:ital,wght@0,500;0,600;0,700;1,600;1,700&display=swap"
    rel="stylesheet" />
</svelte:head>

<Nav {segment} />

<main>
  <slot />
</main>
