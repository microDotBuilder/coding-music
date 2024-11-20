This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

-   [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
-   [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.

## adding prettier for linting:

# step 1:

```bash
pnpm add -D eslint-config-prettier
```

# step 2:

```bash
pnpm add -D @trivago/prettier-plugin-sort-imports
```

# step 3:

```.prettierrc.json
{
    "semi": true,
    "singleQuote": false,
    "trailingComma": "es5",
    "printWidth": 80,
    "tabWidth": 4,
    "importOrder": [
        "^(react|next?/?([a-zA-Z/]*))$",
        "<THIRD_PARTY_MODULES>",
        "^@/components/(.*)$",
        "^@/lib/(.*)$",
        "^@/hooks/(.*)$",
        "^@/types/(.*)$",
        "^@/utils/(.*)$",
        "^@/(.*)$",
        "^[./]"
    ],
    "importOrderSeparation": true,
    "importOrderSortSpecifiers": true,
    "plugins": ["@trivago/prettier-plugin-sort-imports"]
}

```

# step 4:

```.eslintrc.json
{
  "extends": ["next/core-web-vitals", "next/typescript", "prettier"],
  "rules": {
    "no-unused-vars": "off",
    "prefer-arrow-callback": ["error"],
    "prefer-template": ["error"]
  }
}
```

## ESLINT:FIX all auto-fixable errors using ctrl+shift+p -> eslint:fix

## File naming convention: eslint rule

```bash
pnpm add -D eslint-plugin-check-file
```

```json
'check-file/filename-naming-convention': [
  'error',
  {
      '**/*.{ts,tsx}': 'KEBAB_CASE',
  },
  {
      // ignore the middle extensions of the filename to support filename like bable.config.js or smoke.spec.ts
      ignoreMiddleExtensions: true,
  },
],
'check-file/folder-naming-convention': [
  'error',
  {
    // all folders within src (except __tests__)should be named in kebab-case
    'src/**/!(__tests__)': 'KEBAB_CASE',
  },
],
```

## structure of the project

```url
https://github.com/alan2207/bulletproof-react/blob/master/docs/project-structure.md
```

src
|\
+-- app # application layer containing:\
| | # this folder might differ based on the meta framework used\
| +-- routes # application routes / can also be pages\
| +-- app.tsx # main application component\
| +-- provider.tsx # application provider that wraps the entire application with\ different global providers - this might also differ based on meta framework used\
| +-- router.tsx # application router configuration\
+-- assets # assets folder can contain all the static files such as images, fonts,\ etc.\
|\
+-- components # shared components used across the entire application\
|\
+-- config # global configurations, exported env variables etc.\
|\
+-- features # feature based modules\
|\
+-- hooks # shared hooks used across the entire application\
|\
+-- lib # reusable libraries preconfigured for the application\
|\
+-- stores # global state stores\
|\
+-- testing # test utilities and mocks\
|\
+-- types # shared types used across the application\
|\
+-- utils # shared utility functions\

## environment variables typesafe way using T3env.gg:

# esling plugin to stop ussage of process.env

```bash
pnpm add -D eslint-plugin-n
```

## TO VIEW DATABASE RELATIONSHIPS GO TO:

```url
https://dbdocs.io/
```
