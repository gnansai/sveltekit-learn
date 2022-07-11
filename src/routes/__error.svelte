<script context="module">
  export function load({ error }) {
    return {
      props: { error },
    };
  }
</script>

<script>
  export let error;
</script>

<div class="error">
  <h2>Oopss</h2>
  <p>{error.message}</p>
  <a href="/guides">View all Guides...</a>
</div>
