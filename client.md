## Table of Contents

- [Installation](./installation.md)
  - [Client](#client)
    - [Tailwind CSS](https://tailwindcss.com/docs/guides/vite)
    - [React Router DOM](https://reactrouter.com/en/main)
    - [Flowbite React](https://www.flowbite-react.com/)
    - [React Icons](https://www.npmjs.com/package/react-icons)
    - [Redux Toolkit](https://redux-toolkit.js.org/tutorials/quick-start)
  - [Server](server)
- [Project Structure](#project-structure)

## Client

Creat a folder on your computer for you project

```
mkdir folder_name
```

### [Vite Website](https://vitejs.dev/guide/)

### [Vite Page](./client.md)

Inside your project folder

```
npm create vite@latest
```

> This **npm create vite@latest** comment use for creat react using vite latest version.

> 1. Project name `client`
> 2. Select a framework `React` ( if we want to use React)
> 3. Select a varition `JavaScript + SWC` or what ever you want. Use SWC for make faster JavaScript.

<br>
Then you should go to client folder, the run npm i and for install all node_module package. After that npm run dev is use for run react using vite in the client side.

<br>

```
cd client
npm install
npm run dev
```

> This is one line comment.

```
npm create vite@latest client -- --template react && cd client && npm install && npm run dev

```

### [Install Tailwind CSS with Vite](https://tailwindcss.com/docs/guides/vite)

1. we already done the 1st steap so now we fllow the 2nd steap

2. **Install Tailwind CSS**
   Install tailwindcss and its peer dependencies, then generate your `tailwind.config.js` and `postcss.config.js` files.

```
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

3. Configure your template paths
   Add the paths to all of your template files in your tailwind.config.js file.

> `tailwind.config.js` (File name)

```
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

4. Add the Tailwind directives to your CSS
   Add the @tailwind directives for each of Tailwind’s layers to your `./src/index.css` file.
   Delete everything from the `./src/index.css` and add this code to the file

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### Delete

1. `App.css`
2. public/ `vite.svg`
3. index.html (delet link `href="/vite.svg"`)
4. Change the title
5. src/ assets/ `react.svg`

6. - In `index.html` delete `<link rel="icon" type="image/svg+xml" href="/vite.svg" /> `
   - change the `<title> Give a name according to your project </title>`
7. src/ App.jsx (delete everything) and write `rfc` means reactFunctionalComponent

**For run our applaction use** `npm run dev`

## Flowbite React

### Install Flowbite React

1. Run the following command to install `flowbite-react`:
   `npm i flowbite-react`

2. Add the Flowbite plugin to `tailwind.config.js`, and include content from `flowbite-react`

```
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    // This one for followbite-react
    'node_modules/flowbite-react/lib/esm/**/*.js',
  ],
  plugins: [
    // This one also for followbite-react
    require('flowbite/plugin'),
  ],
};
```

**For run our applaction use** `npm run dev`

_Previous: [npm Package ](./npmPackage.md)_ | _Previous: [Getting Started](./gettingStarted.md)_ | _Next: [Server](./server.md)_
