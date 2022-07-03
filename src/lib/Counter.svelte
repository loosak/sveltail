<script>
  let count = 0
  const increment = () => {
    count += 1
  }
</script>

<button 
  on:click={_ => count++} 
  class="btn btn-neutral"
  >
  Clicks: {count}
</button>

