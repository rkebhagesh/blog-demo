-- setup node project:
    npm init -y
    npm install express ejs

-- Project structure: 
    /blog-demo-dode
    /helpers
        routes.js
    /public
        /assets
            /css
            /scripts
    /views
        blog-detail.ejs
        blog-listing.ejs
    
    server.js

=======================  Using Tailwind css ========================
   
        1. Install Tailwind CSS
            npm install tailwindcss postcss autoprefixer postcss-cli
        2. Configure Tailwind
            npx tailwindcss init
        3. Create a CSS File for Tailwind
            In your public/css folder, create a style.css file where you’ll add the necessary Tailwind directives.
            - public/css/style.css
                /* public/css/style.css */
                /* Add the Tailwind base, components, and utilities */
                @tailwind base;
                @tailwind components;
                @tailwind utilities;
        4. Configure PostCSS
            Create a postcss.config.js file in the root of your project.
            - postcss.config.js
                module.exports = {
                    plugins: [
                        require('tailwindcss'),
                        require('autoprefixer'),
                    ]
                };
        5. Build Tailwind CSS
            Add a build script in your package.json to compile Tailwind.
                {
                    "scripts": {
                        "build:css": "postcss public/assets/css/style.css -o public/assets/css/tailwind.css"
                    }
                }

# blog-demo
