## typescript

> Install typescript and node types

```bash
npm install typescript @types/node -D
```

## commitlint

> Install commitlint

```bash
npm install commitlint commitlint-config-gitmoji -D
```

## eslint and prettier

> Install eslint and prettier packages

```bash
npm install eslint eslint-plugin-import-helpers eslint-config-prettier eslint-plugin-prettier prettier @typescript-eslint/eslint-plugin @typescript-eslint/parser -D
```

> copy `eslintrc.js` and `.prettierrc`  files

## lint staged and Husky

> Install lint-staged and husky packages

```bash
npm install lint-staged husky -D
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

## swagger and morgan with express

> Install swagger, morgan and express

```bash
npm install express morgan tsoa swagger-ui-express
npm install @types/express @types/morgan @types/swagger-ui-express -D  
```

> Init swagger and morgan

```ts
import express from 'express';
import morgan from 'morgan';
import swaggerUI from 'swagger-ui-express';

const app = express();
app.use(morgan('tiny'));
app.use(express.static('public'));

app.use(
  '/docs',
  swaggerUI.serve,
  swaggerUI.setup(undefined, {
    swaggerOptions: {
      url: '/swagger.json',
    },
  }),
);
```
