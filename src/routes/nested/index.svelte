<script>
  function handleSubmit() {
    alert("Default prevented!");
  }
</script>

<style>
  h1,
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
</style>

<svelte:head>
  <title>Sapper project template</title>
</svelte:head>

<h1>Form in route in folder with nested _layout.svelte</h1>

<p>
  If you navigate from this page from another page within the Sapper app, the
  form will prevent default. If you load this page first (or refresh) the
  preventDefault will fail, and the form will reload the page on submit.
</p>

<form on:submit|preventDefault={handleSubmit}>
  <input type="text" />
  <button type="submit">Submit</button>
</form>
