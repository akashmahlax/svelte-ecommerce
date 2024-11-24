<script>
	import { onMount } from "svelte";
	import Navbar from "./components/Navbar.svelte";
	import Footer from "./components/Footer.svelte";
	import Home from "./pages/Home.svelte";
	import About from "./pages/About.svelte";
  
	let currentPage = "home";
  
	onMount(() => {
	  currentPage = window.location.pathname.includes("about") ? "about" : "home";
	});
  </script>
  
  <Navbar {currentPage} />
  
  <main class="flex-grow">
	{#if currentPage === "home"}
	  <Home />
	{:else}
	  <About />
	{/if}
  </main>
  
  <Footer />  