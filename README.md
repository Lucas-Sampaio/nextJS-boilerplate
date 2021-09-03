This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.js`. The page auto-updates as you edit the file.

[API routes](https://nextjs.org/docs/api-routes/introduction) can be accessed on [http://localhost:3000/api/hello](http://localhost:3000/api/hello). This endpoint can be edited in `pages/api/hello.js`.

The `pages/api` directory is mapped to `/api/*`. Files in this directory are treated as [API routes](https://nextjs.org/docs/api-routes/introduction) instead of React pages.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.

## Configs

Depois do projeto criado pelo comando [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app). 
Precisamos agora configurar o [`typescript`](https://nextjs.org/docs/basic-features/typescript)
#### Typescript
1. Adicionar o arquivo tsconfig.json
2. Rodar comando > yarn add --dev typescript @types/react @types/node
3. rodar o projeto **yarn dev** para executar o projeto e ele configurar o tsconfig automaticamente
4. Mudar arquivo index para tsx
5. [Opcional] no tsconfig pode setar o strict como true para ele deixar os arquivos fortemenet tipados(ex: não aceitando any)

#### Configurar o editorconfig
1. adicione o arquivo .editorconfig no seu codigo para que todos os novos arquivos que forem cirados seguirem um padrão
2. 
``` 
root = true

[*]
indent_style = spaces
indent_size = 2
end_of_line = lf
charset = utf-8
trim_trailing_whitespace = true
insert_final_newline = true
```

#### Eslint
1. instalar o [`eslint`](https://eslint.org/) no vs code de Dirk Baeumer e habilitar
2. rodar o comando npx eslint --init
3. respostas que usei no questionario para configurar
- √ How would you like to use ESLint? · To check syntax and find problems    
- √ What type of modules does your project use? · js modules (import/export)
- √ Which framework does your project use? · react 
- √ Does your project use TypeScript? ·  Yes
- √ Where does your code run? · browser
- √ what format do you want your config file? · json
- √ Would you like to install them now with npm? · No (se tiver usando o npm marque yes)
4.Caso use o yarn rode > yarn add --dev eslint-plugin-react@latest @typescript-eslint/eslint-plugin@latest @typescript-eslint/parser@latest
5. instalar [plugin](https://www.npmjs.com/package/eslint-plugin-react-hooks) para webhook que nem a [documentação](https://www.npmjs.com/package/eslint-plugin-react-hooks)
6. Adicionar essas configs no arquivo eslint
 ``` 
 "settings": {
    "react": {
      "version": "detect"
    }
  },
   "rules": {
        "react-hooks/rules-of-hooks": "error",
        "react-hooks/exhaustive-deps": "warn",
        "react/prop-types":"off", //desabilita o prop-types do react será usado do typescript
        "react/react-in-jsx-scope":"off", //desabilita a importação do react nos arquivos no next ja importa globalmente
        "@typescript-eslint/explicit-module-boundary-types": "off" //permite a ts inferi o tipo das props
    }
 ``` 
   
