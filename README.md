# Healthcare Services Management App

## Overview

This is a simple Svelte web application that allows users to manage a list of healthcare services. Users can add, update, and delete services, and it features a contact page for inquiries.

## Features

- Display a list of healthcare services including name, description, and price.
- Add new healthcare services via a form.
- Edit existing service details.
- Delete services from the list.
- Contact form to send inquiries.

## Technology Stack

- **Frontend:** Svelte
- **Styling:** Tailwind CSS

## Installation

Follow these steps to set up the project on your local machine.

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Run the application:**
   ```bash
   npm run dev
   ```
   Open your browser and go to `http://localhost:5000`.

## Project Structure

```plaintext
├── src
│   ├── routes
│   │   ├── +page.svelte       # Main page for managing services
│   │   ├── contact.svelte     # Contact page
│   ├── app.html               # Main HTML template
│   └── ...                    # Other project files
├── tailwind.config.js         # Tailwind CSS configuration
├── postcss.config.js          # PostCSS configuration
└── package.json               # Project dependencies and scripts
```

## Usage

### Managing Services

- **Add Service:** Fill in the form with the service name, description, and price, then click "Add Service."
- **Edit Service:** Click the "Edit" button next to a service to modify its details.
- **Delete Service:** Click the "Delete" button next to a service to remove it from the list.

### Contact Us

For any inquiries, fill out the contact form on the contact page, and your message will be sent to the designated email.

## Deployment

To deploy your application, you can use platforms like Vercel, Netlify, or any other service that supports Svelte apps. Follow their documentation for deployment instructions.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.

## Acknowledgements

- Svelte Team for their amazing framework.
- Tailwind CSS for styling utilities.

## Contact

For further questions or suggestions, feel free to reach out at:

- **Email:** contact@jaruratcare.org