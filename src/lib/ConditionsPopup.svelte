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
  import ManRidingClearSky from '../assets/1.svelte';
  import ManRidingLightRain from '../assets/2.svelte';
  import ManRidingHeavyRain from '../assets/3.svelte';

  let count = 0;
  const images = [
    ManRidingClearSky,
    ManRidingLightRain,
    ManRidingHeavyRain 
  ];
  let currentImageIndex = 0;
  let showPopup = false;

  const displayPopup = () => {
    showPopup = true;
  };

  const nextImage = () => {
    currentImageIndex = (currentImageIndex + 1) % images.length;
  };

  const previousImage = () => {
    currentImageIndex = (currentImageIndex - 1 + images.length) % images.length;
  };
</script>

{#if !showPopup} 
  <button class="nice-button" on:click={displayPopup}>
    Flood level of each roads
  </button>
{/if}

{#if showPopup}
  <div class="popup-overlay">
    <div class="popup" style="position:fixed; top:50%; left:50%; transform:translate(-50%, -50%); background:white; padding:20px; border:1px solid black;">
      <div class="popup-header" style={"display: block"}>
        <button class="close-button" on:click={() => showPopup = false}>X</button>
      </div>

      <div style="display: block;">
        <svelte:component this={images[currentImageIndex]} />
      </div>

      <div class="popup-footer" style="display: block;">
        <button class="nice-button" on:click={previousImage}>Previous</button>
        <button class="nice-button" on:click={nextImage}>Next</button>
      </div>
    </div>
  </div>
{/if}

<style>

  button {
    height: 100px;
    width: 100px;
    justify-content: center;
    align-items: center;
  }
  
  .popup-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 10;
  }
  
  .popup {
    background: white;
    padding: 20px 0;
    border-radius: 20px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    overflow-Y: auto;
  }

  .popup-header{
    display: flex;
    padding: 0;
    text-align: right;
  }
  .popup-content{
      padding: 5px 20px;
  }

  .close-button{
    background-color: #9370DB; 
    color: white;
    border: none;
    border-radius: 50%;
    width: 30px;
    height: 30px;
    font-size: 20px;
    cursor: pointer;
    transition: background-color 0.3s ease;
  }
  
  .nice-button {
    background-color: #9370DB;
    color: white;
    border: none;
    border-radius: 5px;
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
    transition: background-color 0.3s ease;
  }

  .nice-button:hover {
    background-color: #7B68EE;;
  }

  .nice-button:active {
    background-color: #6A5ACD;
  }

</style>