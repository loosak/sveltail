<script>
  import logo from './assets/svelte.png'

  let name = 'svelte';
  let count = 0;
</script>

<div class="hero min-h-screen bg-base-200">
  <div class="hero-content text-center flex-col lg:flex-row">
    <h1 class="text-5xl font-bold">Hello {name}!</h1>
    <input
      bind:value={name}
      type="text" 
      placeholder={name} 
      class="input input-bordered w-full max-w-xs"
    />
    <img src={logo} class="max-w-sm rounded-lg shadow-2xl" alt="svelte"/>
    <button 
      on:click={_ => count++} 
      class="btn btn-neutral py-4"
      >
      Clicked: {count} {count === 1 ? 'time': 'times'}
    </button>
  </div>
</div>

<style lang="less">
  .rounded_corners {
    -moz-border-radius: 38px;
    -webkit-border-radius: 38px;
    border-radius: 8px;
  }

  button {
    .rounded_corners;
  }
</style>
