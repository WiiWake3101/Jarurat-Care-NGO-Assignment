<!-- src/routes/contact.svelte -->
<script>
    let name = '';
    let email = '';
    let message = '';

    function submitForm() {
        alert(`Thank you for contacting us, ${name}!`);
        // Reset fields
        name = '';
        email = '';
        message = '';
    }
</script>

<div class="max-w-lg mx-auto mt-10">
    <h1 class="text-3xl font-bold mb-6 text-center">Contact Us</h1>
    
    <p class="mb-4">For any inquiries, please contact us at:</p>
    
    <div class="bg-gray-100 p-4 rounded">
        <h2 class="font-bold">Jarurat Care NGO</h2>
        <p><strong>Address:</strong> 123 Compassion Lane, Heart City, State, ZIP Code: 45678, India</p>
        <p><strong>Phone:</strong> +91-98765-43210</p>
        <p><strong>Email:</strong> <a href="mailto:contact@jaruratcare.org" class="text-blue-500 hover:underline">contact@jaruratcare.org</a></p>
        <p><strong>Website:</strong> <a href="http://www.jaruratcare.org" class="text-blue-500 hover:underline">www.jaruratcare.org</a></p>
    </div>

    <form on:submit|preventDefault={submitForm} class="space-y-4 mt-6">
        <div>
            <input
                class="w-full p-2 border rounded"
                type="text"
                placeholder="Your Name"
                bind:value={name}
                required
            />
        </div>
        <div>
            <input
                class="w-full p-2 border rounded"
                type="email"
                placeholder="Your Email"
                bind:value={email}
                required
            />
        </div>
        <div>
            <textarea
                class="w-full p-2 border rounded"
                rows="4"
                placeholder="Your Message"
                bind:value={message}
                required
            ></textarea>
        </div>
        <button class="bg-blue-500 text-white p-2 rounded w-full" type="submit">Send Message</button>
    </form>
</div>
