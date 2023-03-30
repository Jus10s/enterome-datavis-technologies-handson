<script>
  let lastClickedButton = null;

  const handleClick = (event) => {
    if (lastClickedButton) {
    lastClickedButton.classList.remove('clicked');
  }

  event.target.classList.add('clicked');
    lastClickedButton = event.target;
    current = event.target.dataset.player;
  };
</script>

<style>
  .clicked {
    background-color: green;
  }
</style>

<!-- We will cover buttons later on! -->
<button class="btn btn-secondary" on:click={() => (current = "messi")}>
  Messi
</button>

<button class="btn btn-secondary" on:click={() => (current = "ronaldo")}>
  Ronaldo
</button>

<button class="btn btn-secondary" on:click={() => (current = "neymar")}>
  Neymar
</button>
