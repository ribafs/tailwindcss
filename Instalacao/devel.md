# Ambiente de desenvolvimento

Como criar um ambiente de desenvolvimento local para o tailwindcss, sem a estrutura de pastas, tudo no raiz

## Criar e acessar a pasta

mkdir devel3

cd devel3

## Instalar o tailwind na pastaa atual

npm init -y

npm i tailwindcss

mkdir src

## Criar o script de configuração

npx tailwindcss init

Criará o script talwind.config.js

```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [],
  theme: {
    extend: {},
  },
  plugins: [],
}
```
Configurar para que o content seja varrido assim (mudar a linha do content para):

  content: ["./src/*.{html,js}"],

Para que todos os arquivos html e js de src sejam varridos. Caso o src tenha subpastas devemos usar 
  content: ["./src/**/*.{html,js}"],

O arquivo acima deverá ser alterado para a customização do Tailwind

Acessar o VSCode

code .

Criar o src/input.css, assim:
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```
Teremos então

src/input.css

tailwiind.config.js

package.json

Criar o src/index.html
```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="../public/output.css">
    <title>Tailwind CSS</title>
</head>
<body>
    <h1 class="m-10 w-32 h32 bg-red-500">teste</h1>
</body>
</html>
```
Executar pelo terminal do VSCode:

npx tailwindcss -i ./src/input.css -o .public/output.css --watch

O comando acima pegará as diretivas das camadas do Tailwind no input.css e as compilará gerando o public/output.css. Então deveremos linkar o output.css no index.html

Quando aparecer Done in ... está OK. Ele ficaará em segundo plano atualizando automaticamente após cada alteração. Sempre que salvar uma alteração ele exibirá
Rebuilding no terminal

Agora, após linkara output.css no index.html, nosso ambiente está pronto para trabalhar com cnforto e produtividade no VSCode.

Instale a extensão TailwindCSS Intellisense.

Expeprimente no VSCode se o autocomplete está funcionando.

Agora nosso index.html está pronto para receber código do Tailwind

Caso feche o terminal, deverá, antes de executar novamente o projeto, executar o comando:

npx tailwindcss -i ./src/input.css -o ./assets/css/output.css --watch


