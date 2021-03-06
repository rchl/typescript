# Lint

If you're using ESLint to lint your project, here is how you can make ESLint lint your TypeScript files.

All you need is to install `@nuxtjs/eslint-config-typescript`:

::: tip
If you're already using `@nuxtjs/eslint-config`, remove it from your dependencies, the Nuxt TypeScript ESLint config includes it.
:::

```sh
npm i -D @nuxtjs/eslint-config-typescript
# OR
yarn add -D @nuxtjs/eslint-config-typescript
```

Then, create or edit your ESLint configuration `.eslintrc.js` by extending `@nuxtjs/eslint-config-typescript` :
```js
module.exports = {
  extends: [
    '@nuxtjs/eslint-config-typescript'
  ]
}
```

Finally, edit the `lint` script of your `package.json`:

```json
"lint": "eslint --ext .ts,.js,.vue ."
```

</div>

You can now lint your TypeScript files by running `npm run lint` (or `yarn lint`).

::: tip
If you need to edit/override TypeScript ESLint rules, You can find [here](https://github.com/typescript-eslint/typescript-eslint/tree/master/packages/eslint-plugin#supported-rules) the list of all supported rules.
:::
