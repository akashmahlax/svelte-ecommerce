<script>
    export let current = "home"; // Receives the current page name as a prop
  </script>
  
  <nav class="bg-blue-600 text-white p-4">
    <ul class="flex space-x-4">
      <li>cd 
        <a
          href="/"
          class="hover:underline {current === 'home' ? 'font-bold underline' : ''}"
        >
          Home
        </a>
      </li>
      <li>
        <a
          href="/about"
          class="hover:underline {current === 'about' ? 'font-bold underline' : ''}"
        >
          About
        </a>
      </li>
    </ul>
  </nav>  