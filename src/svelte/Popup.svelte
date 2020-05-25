<style>
  a {
    text-decoration: none;
    color: black;
  }

  div {
    width: 15rem;
    text-align: center;
  }

  h3 {
    color: rgb(0, 0, 0);
  }

  button {
    background-color: powderblue;
    border: 1px black solid;
    border-radius: 1rem;
    padding: 1rem;
  }
</style>

<script>
  export let pages = [
    // {name:"Andrew", time:new Date().toLocaleString()},
    // {name:"Andrew II", time:new Date().toLocaleString()},
    // {name:"Andrew III", time:new Date().toLocaleString()},
    // {name:"Andrew IIII", time:new Date().toLocaleString()}
  ];

  export let otherexplorers = 7;
</script>

<div>
  <h3>Wikipedia Tracker</h3>
  {#if pages.length}
    <h6>Current rabbit hole:</h6>
    {#each pages as page}
      <p>{page.name} {page.time}</p>
    {/each}
    <br />
    <p>{otherexplorers} other explorers have walked this path</p>
    <p>Follow the rabbit:</p>
    <p>/insert other links from other continuing paths/</p>
  {:else}
    <a href="https://en.wikipedia.org/wiki/Special:Random" target="_blank">
      <button>Get a Random Article</button>
    </a>
  {/if}

</div>
