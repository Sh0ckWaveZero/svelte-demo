<script lang="ts">
  import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte'
  import Counter from './lib/Counter.svelte'
  import svelteLogo from './assets/svelte.svg'
</script>

<main>
  <Navbar let:hidden let:toggle>
    <NavBrand href="/">
      <img src={svelteLogo} class="mr-3 h-6 sm:h-9" alt="Flowbite Logo" />
      <span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white"> Svelte </span>
    </NavBrand>
    <NavHamburger on:click={toggle} />
    <NavUl {hidden}>
      <NavLi href="/" active={true}>Home</NavLi>
      <NavLi href="/about">เกี่ยวกับ</NavLi>
      <NavLi href="/services">Services</NavLi>
      <NavLi href="/pricing">Pricing</NavLi>
      <NavLi href="/contact">Contact</NavLi>
    </NavUl>
  </Navbar>
 
  <div class="card">
    <Counter />
  </div>
</main>
