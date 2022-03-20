# create-svelte

Everything you need to build a Svelte project, powered by [`create-svelte`](https://github.com/sveltejs/kit/tree/master/packages/create-svelte).

## Creating a project

If you're seeing this, you've probably already done this step. Congrats!

```bash
# create a new project in the current directory
npm init svelte@next

# create a new project in my-app
npm init svelte@next my-app
```

> Note: the `@next` is temporary

## Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

To create a production version of your app:

```bash
npm run build
```

You can preview the production build with `npm run preview`.

> To deploy your app, you may need to install an [adapter](https://kit.svelte.dev/docs/adapters) for your target environment.

## Tailwind CSS setup

```bash
npm install -D tailwindcss autoprefixer
```

Create a file

`postcss.config.cjs`

with content:

```js
module.exports = {
    plugins: {
        autoprefixer: {},
        tailwindcss: {},
    },
}
```

```bash
npx tailwind init
```

Put this inside `tailwind.config.cjs`

```js
module.exports = {
  mode: 'jit',
  content: ['./src/**/*.svelte']
}
```

Inside `__layout.svelte`:

```html
<style>
@tailwind base;
@tailwind components;
@tailwind utilities;
</style>
```
