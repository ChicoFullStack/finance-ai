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

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.

## Setup do Projeto Next.js:

## comandos utilizados:

- `npm install prisma@5.21.1`: Instala o prisma .
- `npx prisma init`: Roda o prisma.
- `npx prisma migrate dev -- name init_db`: Migra o schema db para o banco de dados do projeto para produção.
---------------------------------------------------------------------------------------------------

## Commits

Para gerar commits automaticamente, utilize o `husky` e o `commitlint`.
Utilizar o Conventional Commits 1.0.0
- `https://www.conventionalcommits.org/en/v1.0.0/#specification`
---------------------------------------------------------------------------------------------------

Instale as dependências:

- `npm install -D husky@9.1.6`
- `npm install -D lint-staged@12.3.2`
- `npx husky init`
- `npm install git-commit-msg-linter@5.0.8`
Comando:
- `npx husky add .husky/commit-msg ".git/hooks/commit-msg \$1"` ou
  Adicionar o arquivo `commit-msg` na pasta `.husky` com o conteúdo:
- `.git/hooks/commit-msg $1`

Configurar o `pre-commit` na pasta `.husky`:
- npx lint-staged
Criar arquivo `.lintstagedrc.json`:
- `
{
    "*.ts?(x)": [
        "eslint --fix",
        "prettier --write"
    ]
}
`
---------------------------------------------------------------------------------------------------


Plugins:
- `https://tailwindcss.com/blog/automatic-class-sorting-with-prettier`

Comandos:
- `npm install -D prettier prettier-plugin-tailwindcss`
---------------------------------------------------------------------------------------------------


Instale shadcn-ui component library:
- `https://ui.shadcn.com/docs/installation/next`
Comandos:
- `npx shadcn@2.1.3 init`
---------------------------------------------------------------------------------------------------

Modificar o arquivo components.json:
-`para - "aliases": {
    "components": "@/app/_components",
    "utils": "@/app/_lib/utils",
    "ui": "@/app/_components/ui",
    "lib": "@/app/_lib",
    "hooks": "@/app/_hooks"
  }`

Autenticação de usuários com Clerk:
- `https://clerk.dev/docs/authentication/nextjs`
Comandos:
- `npm install @clerk/nextjs@5.7.5`
---------------------------------------------------------------------------------------------------
Migrando o banco de dados para o docker:
- `docker-compose up -d` 
- `npx prisma migrate dev` desenvolvimento
- `npx prisma migrate deploy` produção




