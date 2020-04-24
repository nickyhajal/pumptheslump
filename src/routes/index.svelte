<script>
  import MissionHero from "../components/MissionHero.svelte";
  import Content from "../components/Content.svelte";
  import Bullet from "../components/Bullet.svelte";
</script>

<style>
  h1,
  figure,
  p {
    text-align: center;
    margin: 0 auto;
  }

  h1 {
    font-size: 2.8em;
    text-transform: uppercase;
    font-weight: 700;
    margin: 0 0 0.5em 0;
  }

  p {
    margin: 1em auto;
  }

  @media (min-width: 480px) {
    h1 {
      font-size: 4em;
    }
  }
</style>

<svelte:head>
  <title>#PumpTheSlump</title>
</svelte:head>

<MissionHero />
<Content>
  <Bullet
    tip="Donate Meals from restaurants to healthcare workers with Frontline
    Foods">
    <a href="https://www.frontlinefoods.org/">Check it out here</a>
  </Bullet>
  <Bullet tip="The tip" />
  <Bullet tip="The tip" />
  <Bullet tip="The tip" />
</Content>
