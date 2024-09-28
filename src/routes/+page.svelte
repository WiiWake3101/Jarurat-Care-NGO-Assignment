<script>
	let services = [
	  { id: 1, name: "General Checkup", description: "Routine health check", price: 100 },
	  { id: 2, name: "X-Ray", description: "Chest X-ray scan", price: 200 }
	];
  
	let newService = { name: '', description: '', price: '' };
	let editingIndex = null;
  
	function addService() {
	  if (!newService.name || !newService.description || !newService.price) return;
	  services = [...services, { ...newService, id: Date.now() }];
	  newService = { name: '', description: '', price: '' };
	}
  
	function deleteService(id) {
	  services = services.filter(service => service.id !== id);
	}
  
	function editService(index) {
	  newService = { ...services[index] };
	  editingIndex = index;
	}
  
	function updateService() {
	  if (editingIndex !== null) {
		services[editingIndex] = { ...newService, id: services[editingIndex].id };
		newService = { name: '', description: '', price: '' };
		editingIndex = null;
	  }
	}
  </script>
  
  <div>
	<form class="mb-6" on:submit|preventDefault={editingIndex === null ? addService : updateService}>
	  <div class="mb-4">
		<input class="w-full p-2 border" type="text" placeholder="Service Name" bind:value={newService.name} required />
	  </div>
	  <div class="mb-4">
		<input class="w-full p-2 border" type="text" placeholder="Description" bind:value={newService.description} required />
	  </div>
	  <div class="mb-4">
		<input class="w-full p-2 border" type="number" placeholder="Price" bind:value={newService.price} required />
	  </div>
	  <button class="bg-blue-500 text-white p-2 rounded" type="submit">
		{editingIndex === null ? 'Add Service' : 'Update Service'}
	  </button>
	</form>
  
	<ul>
	  {#each services as service, index}
		<li class="mb-4 p-4 bg-gray-100 rounded">
		  <div class="flex justify-between items-center">
			<div>
			  <h3 class="font-bold">{service.name}</h3>
			  <p>{service.description}</p>
			  <p class="font-bold">${service.price}</p>
			</div>
			<div>
			  <button class="bg-green-500 text-white p-2 rounded mr-2" on:click={() => editService(index)}>Edit</button>
			  <button class="bg-red-500 text-white p-2 rounded" on:click={() => deleteService(service.id)}>Delete</button>
			</div>
		  </div>
		</li>
	  {/each}
	</ul>
  </div>  