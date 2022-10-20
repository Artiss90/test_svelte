<script>
  let user = { loggedIn: false };

  function toggle() {
    user.loggedIn = !user.loggedIn;
  }
</script>

<!-- реализация отбражений компонентов с помощью условий -->

<!-- {#if user.loggedIn}
  <button on:click={toggle}> Выйти </button>
{/if}

{#if !user.loggedIn}
  <button on:click={toggle}> Войти </button>
{/if} -->

<!-- реализация через if else -->
<!-- Символ # всегда обозначает открывающий тег. Символ / обозначает закрывающий тег. Символ :, как в {:else} — тег разделения блока -->

{#if user.loggedIn}
  <button on:click={toggle}> Выйти </button>
{:else}
  <button on:click={toggle}> Войти </button>
{/if}
