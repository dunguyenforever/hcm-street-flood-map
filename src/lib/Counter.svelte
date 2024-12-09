<!-- <script>
  let count = 0
  const increment = () => {
    count += 1
  }
</script>

<button on:click={increment}>
  count is {count}
</button>

<style>
  button{
    height: 100px;
    width: 100px;
  }
</style> -->

<script>
  let count = 0;
  const images = [
    'src/assets/man_riding_clear_sky.png',
    'src/assets/man_riding_light_rain.png',
    'src/assets/man_riding_heavy_rain.png' 
  ];
  let currentImageIndex = 0;
  let showPopup = false;

  const increment = () => {
    count += 1;
    showPopup = true;
  };

  const nextImage = () => {
    currentImageIndex = (currentImageIndex + 1) % images.length;
  };

  const previousImage = () => {
    currentImageIndex = (currentImageIndex - 1 + images.length) % images.length;
  };
</script>

<button on:click={increment}>
  count is {count}
</button>

{#if showPopup}
  <div id="popup" style="position:fixed; top:50%; left:50%; transform:translate(-50%, -50%); background:white; padding:20px; border:1px solid black;">
    <img src={images[currentImageIndex]} alt="Motorcycle Image" style="width:100%; height:auto;">
    <button on:click={previousImage}>Previous</button>
    <button on:click={nextImage}>Next</button>
    <button on:click={() => showPopup = false}>Close</button>
  </div>
{/if}

<style>
  button {
    height: 100px;
    width: 100px;
  }
</style>