
1. Package.json is a configuration for npm.
2. packagelock.json keeps the record of the exact version that is installed. integrity is sha512 verifies whether the same dependencies in my local are deployed on production.
3. npm is a package manager. It is a big repository where all packages are available.
4. Transitive dependencies -> In the Node Modules Folder we can see multiple packages even if we install one package. So the installed package needs some other packages and so on.
5. Bundler - Webpack, babel, parcel
6. Bundler minifies, builds our app for production ready.
7. parcel - dev build, local server, hmr(hot module replacement), file watching algorithm(c++), Faster builds (caching), Image obtimization, minification, bundling, compress, consistent hashing, cod e splitting, differential bundling to support of older browsers, diagnostics, error handling, https, tree shaking algorithm remove unused files, differernt dev and prod bundles.
8. dev / normal dependencies -> dev dependencies used in the development phase.
9. tilde ~ minor versions update automatically
10. caret ^ Major version updates automatically
11. node modules is a collection of dependencies.
12. npx -> execute a package



Questions:
 What is Emmet?
- emmet is somthing that automates and reduces our work of typing evering.
● Difference between a Library and Framework?
 - Library is tool you can use in your application if required
 - framework means it has complete front and back end with guildlines and restriction which make you to stay in that ecosystem like apple.
● What is CDN? Why do we use it?
cdn is content deliver network. we use that to fetch and use libraries 
● Why is React known as React?
React is a library for UI.
● What is crossorigin in script tag?
- its allowing to download from other domains
● What is diference between React and ReactDOM
- React has core functionality like state management and react dom give browser methods for rendering react componets, interacting with dom etc.
- 
● What is difference between react.development.js and react.production.js files via CDN?
-react.development.js gives unminified code
-react.production.js gives minified and optimized code.

● What is async and defer? - see my Youtube video 
 - async means asyncronously fetch all scripts without interepting other tasks
 - defer means scrpits will be executed after html parsing.

● - What is `NPM`?
npm is a package manager used to install, share and manage packages.
● - What is `Parcel/Webpack`? Why do we need it?
- parcel/webpack is a bundler. we need it to because it auomates so many things like hmr, minifing, bundles for dev & prod, code spliiting, compress code, diagnises code, etc. they mange dependencies
● - What is `.parcel-cache`
- it caches some thing that allows hmr works faster. it is like a data base of older builds. It helps to speed up subsequent builds.
● - What is `npx` ?
- 
● - What is difference between `dependencies` vs `devDependencies`
- dependencies available only on dev env are dev dependencies, which are avalable or used in prod are called dependencies
● - What is Tree Shaking?
- it will removes unused code while building
● - What is Hot Module Replacement?
- changes done on code will quickly shown on the screen
● - List down your favourite 5 superpowers of Parcel and describe any 3 of them in your
own words.
● - What is `.gitignore`? What should we add and not add into it?
- basically it ignores files pussing to github. node modules, dist, .env etc
● - What is the difference between `package.json` and `package-lock.json`
- package.json is configuration file for npm and has approximate verisons of depencies.
● - Why should I not modify `package-lock.json`?
- it has tracked all the details of packages strickely.
● - What is `node_modules` ? Is it a good idea to push that on git?
- coolection of dependencies required for our project. No.
● - What is the `dist` folder?
- dist folder contains build files html,jss,css fully minified and optimised
● - What is `browserlists`
Read about dif bundlers: vite, webpack, parcel
- it is package that give power to run an application on all browsers
● Read about: ^ - caret and ~ - tilda
- ^ updated major versions, ~ for minor version
● Read about Script types in html (MDN Docs)


 - Emmet:

Emmet is a tool that helps web developers write HTML and CSS code faster. It allows you to use shortcuts to create code snippets more efficiently.
Library vs. Framework:

Library: A collection of code for specific tasks that developers can use as needed (e.g., jQuery).
Framework: A pre-built structure that dictates how developers should write their code (e.g., React, Angular).
CDN (Content Delivery Network):

CDN is a network of servers that delivers web content (images, scripts) to users based on their location. It makes websites faster by reducing load times.
Why React is Named React:

React is named for its "reactive" approach to building user interfaces. Components react to changes in data, updating the UI efficiently.
crossorigin in the script tag:

It's used for loading external scripts from different domains. It specifies whether the browser should include credentials (like cookies) when fetching the script.
React vs. ReactDOM:

React: Core library for building user interfaces, managing state, etc.
ReactDOM: Package for interacting with the DOM, rendering and updating React components.
react.development.js vs. react.production.js via CDN:

development: Unminified version with warnings, for easier debugging during development.
production: Minified and optimized version without warnings, for faster loading in production.
async and defer in <script> tag:

async: Downloads script asynchronously and executes it as soon as it's downloaded.
defer: Downloads script asynchronously but waits to execute until the HTML document is fully parsed.


Certainly! Let's go through each question:

What is NPM?

NPM stands for Node Package Manager. It is a package manager for JavaScript and Node.js, used to install, share, and manage packages or libraries of code.
What is Parcel/Webpack? Why do we need it?

Parcel and Webpack are bundlers, tools that take your source code, including styles, scripts, and assets, and package them together for the browser. They help manage dependencies, optimize code, and enable features like code splitting.
What is .parcel-cache?

The .parcel-cache directory is created by Parcel and stores cached data to speed up subsequent builds. It can be safely deleted to clear the cache.
What is npx?

npx is a tool that comes with NPM and is used to execute packages from the NPM registry. It is particularly useful for running binaries of packages without installing them globally.
Difference between dependencies vs devDependencies:

dependencies: Packages required for the application to run in production.
devDependencies: Packages used for development and testing, not necessary for the production build.
What is Tree Shaking?

Tree Shaking: It's a technique used by bundlers to eliminate dead code (unused exports) from the final bundle, reducing its size.
What is Hot Module Replacement?

Hot Module Replacement (HMR): It's a feature that allows the replacement of modules in an application without a full page refresh. It speeds up development by preserving the application state.
List down your favorite 5 superpowers of Parcel and describe any 3 of them in your own words:

Parcel's superpowers include zero-config setup, automatic dependency resolution, blazing fast speed, hot module replacement, and support for various file types.
What is .gitignore? What should we add and not add into it?

.gitignore is a file that specifies intentionally untracked files to be ignored by Git. It should include files like logs, build artifacts, and sensitive information. It should not include essential configuration files or files required for the project.
Difference between package.json and package-lock.json:

package.json: Describes the project and its dependencies. It includes metadata and high-level information about the project.
package-lock.json: Locks down the version of each package's dependencies, ensuring consistent installations across different environments.
Why should I not modify package-lock.json?

package-lock.json is automatically generated and managed by NPM. Modifying it directly is not recommended, as it could lead to dependency conflicts and inconsistencies.
What is node_modules? Is it a good idea to push that on git?

node_modules is a directory where NPM installs project dependencies. It's generally not a good idea to push it to Git, as it can be large and is easily regenerated using npm install based on the package.json and package-lock.json.
What is the dist folder?

The dist folder (short for distribution) contains the distribution-ready files, often the minified and optimized version of the source code. It is what is deployed to a production environment.
What is browserslist?

browserslist is a configuration file used by tools like Autoprefixer and Babel to determine which browser versions to support when transpiling and prefixing CSS and JavaScript code.
Read about different bundlers: Vite, Webpack, Parcel.

These are popular JavaScript bundlers that help manage and optimize web application code. They have different features and configurations suited to different use cases.
Read about ^ (caret) and ~ (tilde).

These are versioning prefixes used in package.json. ^ allows updates for compatible versions, while ~ allows only patch updates.
Read about Script types in HTML.

Script types in HTML include text/javascript (default), module (for ECMAScript modules), and type="text/babel" (for Babel-processed scripts). They define how the browser should interpret the script content.
