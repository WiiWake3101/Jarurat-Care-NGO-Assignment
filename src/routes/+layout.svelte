<script>
	export const data = {};
	import "../app.css";
  </script>
  <nav class="bg-gray-800 text-white p-4">
	<div class="container mx-auto flex justify-between">
	  <div class="text-xl font-bold">Healthcare Management</div>
	  <ul class="flex space-x-4">
		<li><a href="/" class="hover:underline">Home</a></li>
		<li><a href="./contact" class="hover:underline">Contact</a></li>
	  </ul>
	</div>
  </nav>
  <main class="p-6 max-w-lg mx-auto">
	<slot />
  </main>
  <footer class="bg-gray-800 text-white text-center py-10 mt-5">
	Done By @ Vivek M G
  </footer>