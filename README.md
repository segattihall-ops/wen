'''
# Bruno Santos - Professional Massage Therapist Website

This repository contains the source code for the professional portfolio website for Bruno Santos, a licensed massage therapist based in Dallas, TX. The website is designed to be clean, professional, mobile-responsive, and SEO-optimized, with a strong focus on creating a safe and welcoming space for the LGBTQ+ community.

## Key Features

-   **LGBTQ+ Friendly Messaging:** Content and design tailored to create a safe and inclusive environment for gay and queer clients.
-   **Mobile-First Responsive Design:** A seamless experience across all devices, from desktops to smartphones.
-   **Live Chat Widget:** A simulated chat feature to engage visitors and encourage booking inquiries.
-   **Multiple CTAs:** Prominent "Book Your Session" and "Call Now" buttons to drive conversions.
-   **Clear Business Information:** Availability (7 AM - 11 PM) and starting price ($150) are clearly displayed.
-   **Professional Credentials:** Highlights Bruno's experience, licensing, and certifications to build trust.
-   **Dynamic Testimonials Section:** Displays 6 reviews initially with a "See More" button to reveal a total of 22 reviews.
-   **SEO Optimized:** Includes schema markup for local business and reviews, and is optimized for relevant keywords like "gay massage Dallas."

## File Structure

```
/bruno-santos-website
|-- /images
|   |-- hero-outdoor.jpg
|   |-- about-studio.jpeg
|   |-- gallery-casual.jpeg
|   |-- gallery-professional.jpg
|-- index.html
|-- privacy.html
|-- terms.html
|-- package.json
|-- README.md
```

## Deployment

This is a static HTML/CSS/JS website and can be deployed to any static hosting provider. Below are instructions for some popular platforms.

### Vercel (Recommended)

Vercel is a great platform for deploying static sites with zero configuration.

1.  **Sign up for Vercel:** Create an account at [vercel.com](https://vercel.com).
2.  **Install Vercel CLI:** Open your terminal and run:
    ```bash
    npm install -g vercel
    ```
3.  **Login to Vercel:** In your terminal, run:
    ```bash
    vercel login
    ```
4.  **Deploy:** Navigate to the `bruno-santos-website` directory in your terminal and run:
    ```bash
    vercel --prod
    ```

Vercel will provide you with a unique URL for your deployed site. To use a custom domain like `www.masseurmatch.com/dallas/massage/brunosantos`, you would typically set this up within the MasseurMatch.com domain's DNS settings to point to the Vercel deployment. This usually involves a reverse proxy or similar setup on the main domain.

### Netlify

Netlify offers a simple drag-and-drop deployment process.

1.  **Sign up for Netlify:** Create an account at [netlify.com](https://netlify.com).
2.  **Drag and Drop:** Zip the `bruno-santos-website` directory and drag the ZIP file into the Netlify dashboard's deployment area.
3.  **Configure:** Netlify will automatically unzip and deploy the site. You can then configure your domain settings.

### GitHub Pages

If you are using Git, you can easily deploy to GitHub Pages.

1.  **Create a GitHub Repository:** Create a new repository on [github.com](https://github.com).
2.  **Push Your Code:** Add the `bruno-santos-website` files to the repository and push them.
    ```bash
    git init
    git add .
    git commit -m "Initial commit"
    git branch -M main
    git remote add origin https://github.com/your-username/your-repo-name.git
    git push -u origin main
    ```
3.  **Enable GitHub Pages:** In your repository's settings, go to the "Pages" section and select the `main` branch as the source. Your site will be deployed at `https://your-username.github.io/your-repo-name/`.

## Local Development

To run the website locally, you can use a simple HTTP server. If you have Python installed, you can run the following command from the `bruno-santos-website` directory:

```bash
# For Python 3
python -m http.server
```

This will start a local server, and you can view the site at `http://localhost:8000` in your browser.

Alternatively, you can use the `serve` package from npm:

```bash
npm install -g serve
serve .
```

This will also start a local server, typically at `http://localhost:3000`.
'''
