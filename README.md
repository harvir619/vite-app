# Vite-app


Webpack can take all of our JavaScript files and modules as well as our CSS, Sass and other assets and bundle them into a single or a sometimes few files.
We use a webpack.config.js file to configure and tell Webpack how to bundle our files. We can also install plugins and loaders to help Webpack do its job.

Webpack and other traditional module bundlers is that they can be slow as they have to bundle our files every time we make a change.

1. Vite serves our files directly to the browser, built on top of esbuild, a JavaScript bundler written in Go that bundles dependencies 10 to 100 times faster than JavaScript-based bundlers.
2. Esbuild takes advantage of native ES modules in the browser. This means that Vite can serve our files directly to the browser without bundling them.
3. Takes advantage of code splitting on the fly to only load the code that we need.
4. Performs optimizations like minification and tree shaking to make our files as small as possible.

When it comes time to build your files for production, Vite uses an actual module bundler called Rollup.

Steps
1. yarn create vite@latest my-vite-app
2. Select framework and variant , i used react and plain javascript
3. npm install
4. npm i -D sass
5. npm run dev
6. npm run build
7. npm run preview

Folder Structure

1. The src folder is where we write our code including all of our React components, etc.
2. The index.html
  a. Single div with an id of "root", similar to any other React application.
  b. <script> tag using the type="module" attribute. This tells the browser that we are using ES modules
  c. src attribute to point to the main.jsx file.
3. The vite.config.js
  a. Add plugins, configure the development server
  b. Change some settings, including the port that the development server runs on.
  
Create React Component
 A new folder called components and then create a new file called Header.jsx. I'll just create a simple component that renders a div with some text.
     const Header = () => {
      return <div>Hello World</div>;
    };

    export default Header;

Environment Variables
 Create a .env file, must begin with VITE_
  a. VITE_API_KEY=123456789
  b. Use return <div>{import.meta.env.VITE_API_KEY}</div>; to access
  
    
Using SASS
Sass support is built into Vite. We can use it by installing the sass package. Created scss folder and scss file
