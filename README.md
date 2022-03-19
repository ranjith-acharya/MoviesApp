## Installation and Execution
: Installing TailwindCSS
: Create 'tailwind.config.js' File
```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init
```
: Add Tailwind into 'webpack.min.js' File
```js
mix.js("resources/js/app.js", "public/js")
  .postCss("resources/css/app.css", "public/css", [
    require("tailwindcss"),
  ]);
```
: Add Paths to 'tailwind.config.js' File
```js
module.exports = {
  content: [
    "./resources/**/*.blade.php",
    "./resources/**/*.js",
    "./resources/**/*.vue",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```
: Add Tailwind Directives to 'app.css' File in 'resources/css/app.css'
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```
: Run the Dev
```bash
npm run dev
OR
npm run watch
```
