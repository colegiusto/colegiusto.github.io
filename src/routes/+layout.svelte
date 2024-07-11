<script>
  import Footer from "../lib/Footer.svelte";
  import Navbar from "../lib/Navbar.svelte";

  export const prerender = true;
</script>

<Navbar />
<div class="mainbody">
  <slot></slot>
</div>
<Footer />

<style>
  .mainbody {
    width: max(10em, 70%);
    margin: auto;
    padding-top: 1.5em;
    font-size: min(3vw, 20px);
  }
</style>
