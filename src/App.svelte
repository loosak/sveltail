<script>
  import logo from './assets/svelte.png'

  let name = 'svelte';
  let count = 0;
  let upperCase = true;
</script>

<div class="hero min-h-screen bg-base-200">
  <div class="hero-content text-center flex-col lg:flex-row">
    <h1 class="text-5xl font-bold">Hello {upperCase ? name.toUpperCase() : name}!</h1>
    <input
      type=text
      bind:value={name} 
      placeholder={name} 
      class="input input-bordered w-full max-w-xs"
    />
    <label>
      <input
      type=checkbox
      bind:checked={upperCase}
    /> upper case
    </label>
    <img src={logo} class="max-w-sm rounded-lg shadow-2xl" alt="svelte"/>
    <button 
      on:click={_ => count++} 
      class="btn btn-neutral py-4"
      >
      Clicked: {count} {count === 1 ? 'time': 'times'}
    </button>
  </div>
</div>

<style lang="postcss">
</style>
