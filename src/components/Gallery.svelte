<script>
  const initializeLightGallery = () => {
    new window.lightGallery(
      document.querySelector('.l-gallery .l-gallery__container')
    )
  }
</script>

<svelte:head>
  <script
    src="https://cdnjs.cloudflare.com/ajax/libs/lightgallery-js/1.4.0/js/lightgallery.min.js"
    on:load="{initializeLightGallery}"></script>
</svelte:head>

<section class="l-gallery" id="gallery">
  <h1 class="c-heading">our <span>gallery</span></h1>

  <div class="l-gallery__container">
    <a href="images/g-img-1.jpg" class="l-gallery__box"
      ><img src="images/g-img-1.jpg" alt="" class="l-gallery__image" />
    </a>
    <a href="images/g-img-2.jpg" class="l-gallery__box"
      ><img src="images/g-img-2.jpg" alt="" class="l-gallery__image" />
    </a>
    <a href="images/g-img-3.jpg" class="l-gallery__box"
      ><img src="images/g-img-3.jpg" alt="" class="l-gallery__image" />
    </a>
    <a href="images/g-img-4.jpg" class="l-gallery__box"
      ><img src="images/g-img-4.jpg" alt="" class="l-gallery__image" />
    </a>
    <a href="images/g-img-5.jpg" class="l-gallery__box"
      ><img src="images/g-img-5.jpg" alt="" class="l-gallery__image" />
    </a>
    <a href="images/g-img-6.jpg" class="l-gallery__box"
      ><img src="images/g-img-6.jpg" alt="" class="l-gallery__image" />
    </a>
  </div>
</section>
