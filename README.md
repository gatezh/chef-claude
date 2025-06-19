# Chef Claude app

<img src="src/images/chef-claude-icon.png" alt="Chef Calude"/>



> **Live Demo:** See the deployed link in the repository description.

This app fetches recipe suggestions based on user-provided ingredients. The frontend sends requests to a Cloudflare Worker, which queries the Hugging Face API and returns recipe data.



## Features

- Input a list of ingredients (e.g., `chicken, garlic, lemon`) to get recipe suggestions.
- Simple React UI with fast Vite development.
- Secure API calls: frontend calls Cloudflare Worker; Worker holds Hugging Face API key.
- Uses Bun for dependency management and scripts.



## Tech Stack

- **Frontend:** React + Vite
- **Runtime & Package Manager:** Bun
- **API Layer:** Cloudflare Worker (handles Hugging Face requests)



## Setup & Development

1. **Clone repository:**

   ```bash
   git clone https://github.com/gatezh/chef-claude.git
   cd chef-claude
   ```

2. **Install dependencies:**

   ```bash
   bun install
   ```

3. **Run dev server:**

   ```bash
   bun run dev
   ```

   - Open [http://localhost:5173](http://localhost:5173/) (or shown port) and test ingredient input.



## Usage

- Enter available ingredients
- When you enter at least 4 ingredients **Get a recipe** button appears; press to get a recipe
- Frontend sends request to the Worker URL; Worker queries Hugging Face API and returns recipe suggestions.
- Display results in a clear format.



## Deployment

Deployment is handled via GitHub Actions (using Bun).

Check `.github/deploy-to-gh-pages.yml` file for more details.