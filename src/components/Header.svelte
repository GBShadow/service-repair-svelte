<script lang="ts">
  let activeButton = false
  let activeHeader = false
  let iconClass = 'fa-bars'

  $: {
    iconClass = activeButton ? 'fa-times' : 'fa-bars'
  }

  window.onscroll = () => {
    iconClass = 'fa-bars'
    activeButton = false

    if (window.scrollY > 60) {
      activeHeader = true
    } else {
      activeHeader = false
    }
  }
</script>

<header class="l-header">
  <div class="l-header__contact-info">
    <p class="l-header__info">
      <i class="fas fa-map icon"></i> São Paulo, Brasil
    </p>
    <p class="l-header__info">
      <i class="fas fa-envelope icon"></i> gbs.shadow@gmail.com
    </p>

    <p class="l-header__info">
      <i class="fas fa-phone icon"></i> +55 11 95674-8392
    </p>
  </div>

  <nav class="{`l-header__navbar ${activeHeader && 'active'}`}">
    <a href="#home" class="l-header__logo">
      <i class="fas fa-tools icon"></i> fixpro
    </a>

    <div class="{`l-header__links ${activeButton && 'active'}`}">
      <a href="#home" class="link">home</a>
      <a href="#about" class="link">about</a>
      <a href="#services" class="link">services</a>
      <a href="#gallery" class="link">gallery</a>
      <a href="#team" class="link">team</a>
      <a href="#reviews" class="link">reviews</a>
      <a href="#contact" class="link">contact</a>
    </div>

    <div
      class="{`fa ${iconClass} menu-button`}"
      on:click="{() => (activeButton = !activeButton)}"
    ></div>
  </nav>
</header>
