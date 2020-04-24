<script>
  export let tip;
</script>

<style lang="scss">
  @import "../style/theme";
  div {
    background: $light-green;
    display: grid;
    padding: 1rem;
    margin-bottom: 4rem;

    h3 {
      font-size: 1.6rem;
      font-weight: 700;
    }
  }
</style>

<div>
  <h3>{tip}</h3>
  <article>
    <slot />
  </article>
</div>
