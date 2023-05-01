## eslint and prettier

> Install eslint and prettier packages

```bash
yarn add eslint eslint-config-prettier eslint-plugin-prettier prettier @typescript-eslint/eslint-plugin
@typescript-eslint/parser -D
```

> copy `eslintrc.js` and `.prettierrc`  files

## lint staged and Husky

> Install lint-staged and husky packages

```bash
yarn add lint-staged husky -D
```

> Edit `package.json` adding the prepare script

```bash
npm pkg set scripts.prepare="husky install"

npm run prepare
```

> Create `pre-commit` script with lint-staged

```bash
npx husky add .husky/pre-commit "npx lint-staged"
```

> If you are on Linux (and maybe MACOS), give execution permission to `pre-commit` script.

```bash
chmod +x .husky/pre-commit
```
