<script>
  import Button from './components/Button/Button.svelte';
  import Info from './components/Info/Info.svelte';
  import SumNumbers from './components/SumNumbers/SumNumbers.svelte';
  import UserButton from './components/UserButton/UserButton.svelte';
  export let name;

  //  передача сразу нескольких пропсов
  const pkg = {
    name: 'svelte',
    version: 3,
    speed: 'невероятно',
    website: 'https://svelte.dev',
  };
</script>

<main>
  <h1>Hello {name}!</h1>
  <p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
  <Button count={5} />
  <SumNumbers />
  <!-- <Info name={pkg.name} version={pkg.version} speed={pkg.speed} website={pkg.website}/> -->
  <Info {...pkg} />
  <UserButton />
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
