<script context="module">
  export async function load({ fetch }) {
    const res = await fetch("https://jsonplaceholder.typicode.com/posts");

    const guides = await res.json();

    if (res.ok) {
      return {
        props: {
          guides: guides,
        },
      };
    }

    return {
      status: res.status,
      error: new Error("could not fetch the guides"),
    };
  }
</script>

<script>
  export let guides;
</script>

<div class="guides">
  <ul>
    {#each guides as guide}
      <li>
        <a sveltekit:prefetch href={`/guides/${guide.id}`}>{guide.title}</a>
      </li>
    {/each}
  </ul>
</div>

<style>
  .guides {
    margin-top: 2px;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  a {
    display: inline-block;
    margin-top: 10px;
    padding: 10px;
    border: 1px solid rgb(58, 58, 58);
  }
</style>
