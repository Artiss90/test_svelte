<script>
  export let count = 0;

  function handleClick() {
    count += 1;
  }
</script>

<button on:click={handleClick}>
	{count === 0 ? 'Кликни по мне' : `Кликов: ${count}`}
</button>

<style>
  button {
    text-align: center;
    padding: 6px;
    margin: 0 auto;
    background-color: #212121;
    color: #fff;
  }
</style>
