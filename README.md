Requirements

Node.js
 (v18+ recommended)

npm or yarn

📦 Installation
# 1. Initialize project
npm init -y

# 2. Install Tailwind CSS and PostCSS CLI
npm install -D tailwindcss postcss postcss-cli

🛠 Project Structure
.
├── src/
│   └── input.css        # Tailwind entry file
├── dist/
│   └── output.css       # Compiled CSS
├── package.json
└── index.html

🎨 Add Tailwind Directives

In src/input.css add:

@import "tailwindcss";


(In v4 you don’t need @tailwind base; @tailwind components; @tailwind utilities; — a single import is enough.)

🚀 Build CSS

Compile your CSS with:

npx postcss src/input.css -o dist/output.css --watch


Or add this shortcut in package.json:

"scripts": {
  "dev": "postcss src/input.css -o dist/output.css --watch"
}


Run it:

npm run dev

📄 Use in HTML

Link the compiled CSS in your index.html:

<link href="./dist/output.css" rel="stylesheet">
