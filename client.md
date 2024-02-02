- [Installation](./installation.md)
  - [Client](#client)
    - [Tailwind CSS](https://tailwindcss.com/docs/guides/vite)
  - [Server](server)
- [Project Structure](#project-structure)

## Client

Creat a folder on your computer for you project

```
mkdir folder_name
```

### [Vite](https://vitejs.dev/guide/)

Inside your project folder

```
npm create vite@latest
```

> This **npm create vite@latest** comment use for creat react using vite latest version.

> 1. Project name **client**
> 2. Select a framework **React** ( if we want to use React)
> 3. Select a varition **JavaScript + SWC** or what ever you want .

<br>
Then you should go to client folder, the run npm i and for install all node_module package. After that npm run dev is use for run react using vite in the client side.

<br>

```
cd client
npm install
npm run dev
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
6. App.jsx (delete everything) and write `rfc` means reactFunctionalComponent

**For run our applaction use** `npm run dev`

_Previous: [File 4](file4.md)_ | _Next: [File 5](file5.md)_