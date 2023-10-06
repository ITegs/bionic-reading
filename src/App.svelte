<script lang="ts">
  import Header from "./lib/Header.svelte";

  var text = "";
</script>

<main>
  <Header />
  <div class="output">
    {#each text.split(/[ \n]+/) as t}
      <b>{t.substring(0, t.length / 2)}</b>{t.substring(t.length / 2, t.length)}
      {" "}
    {/each}
  </div>
  <textarea bind:value={text} placeholder="Your text here." />
</main>

<style>
  .output {
    text-align: left;
    font-size: 1.2rem;
    padding: 5rem;
    padding-inline: 2vw;
  }

  b {
    font-weight: 800;
  }
  textarea {
    width: 70vw;
    min-height: 20vh;
  }
</style>
