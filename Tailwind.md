# Tailwind CSS

https://tailwindcss.com/

https://tailwindcss.com/docs/

https://www.youtube.com/watch?v=1qH3wAtX4So

## Utiliity-first

Construir componentes complexos a partir de um conjunto restrito de utilitários primitivos.

Algumas classes

Texto
    text-center
    text-blue-500
    text underline
    text overline
    tracking-* - espacamento entre letras
    leading-* - espaçamento entre linhas

Padding - https://tailwindcss.com/docs/padding
    pt, pr, pb, pl
    px, py
    p - todos os 4 lados
    ps, pe

<h1 class="py-96 px-96">Teste</h1>

Grid - https://tailwindcss.com/docs/grid-template-columns

container - é responsivo, muito diferente do bootstrap. Usado como breakpoint e não fica centrado automaticamente. Para centralizar usar mx-auto

https://tailwindcss.com/docs/container

columns

https://tailwindcss.com/docs/columns

Flexbox permite maior controle sobre o layout e de forma responsiva

https://tailwindcss.com/docs/flex-basis

Exemplo
```html
<div class="flex flex-row">
  <div class="basis-1/4">01</div>
  <div class="basis-1/4">02</div>
  <div class="basis-1/2">03</div>
</div>
```

flex flex-row - itens na horizntal

flex flex-col - itens na vertical

Normalmente 1/4 e quando chegar a sm mudar para 1/2

basis-1/4 sm:basis-1/2 

Quando a soma dos basis for maior que 1, então devemos usar o flex-wrap

flex flex-row flex-wrap

- basis-1/2
- basis-1/2
- basis-1/2

Background

- bg-sky-500
- bg-sky-500/75
- bg-sky-500/50

Para usar valores intermediários aos da lista, usar

bg-sky-500/[52]

Mudar a cor ao mover o mouse

bg-sky-500 hover:bg-sky-200

75 e 50 são transparências

Display

    flex-grow - a div ocua todoo tamanho horizontal
    flex - itens alinhados ao centro
    flex-1 - tamanho máximo
    flex-shrink-0 - para não diminuir mais que deve

Alinhamento - https://tailwindcss.com/docs/vertical-align

    flex align-itens justify-center

Size

    font-size - https://tailwindcss.com/docs/font-size

Horizontal e vertical
```html
<div class="flex h-screen">
  <div class="m-auto">
    <h1>Title</h1>
  </div>
</div>

<div class="grid place-items-center h-screen">
  Centered using Tailwind Grid
</div>

<div class="flex items-center justify-center h-screen">
  Centered using Tailwind Flex
</div>
```
    flex: Adds the display: flex CSS property
    justify-center: This centers the div horizontally
    items-center: This centers the content vertically
    h-screen: Sets the 100vh (screen-height) as the height

Respoonsive

    usando pelo menos doois tamanhos: o original e um coom sm:...que é maior (com duas colunas)

Breakpoint prefix	Minimum width	CSS

- sm	640px	@media (min-width: 640px) { ... }
- md	768px	@media (min-width: 768px) { ... }
- lg	1024px	@media (min-width: 1024px) { ... }
- xl	1280px	@media (min-width: 1280px) { ... }
- 2xl	1536px	@media (min-width: 1536px) { ... }

box-shadow - https://tailwindcss.com/docs/box-shadow-color

rounded

    roundedfull

border

margens - https://tailwindcss.com/docs/margin

    ml
    mr
    mx
    m
m{t|r|b|l|x|y}-{size}

To center a container, use the mx-auto utility:

border border-red-400

buttons

Obs: para alternativa usar :. Exemplo: text-red-500 hover:text-white

fonts
    font-semibold
    font-sans
w
    w-full
    w-screen - ocupa toda a tela

Dicas

outline-none - sem linha de contorno


Usando @apply podemos tetr classes que agrupam utilitáriioos
```css
/* Input */
.btn {
  @apply font-bold py-2 px-4 rounded !important;
}

/* Output */
.btn {
  font-weight: 700 !important;
  padding-top: .5rem !important;
  padding-bottom: .5rem !important;
  padding-right: 1rem !important;
  padding-left: 1rem !important;
  border-radius: .25rem !important;
```

Então rodar o build novamente

Components

Hover, focus, active e outros estados:
    bg-sky-700 hover:bg-sky-300

First, last, odd, and even


Dark mode
```html
<div class="bg-white dark:bg-slate-800 rounded-lg px-6 py-8 ring-1 ring-slate-900/5 shadow-xl">
  <div>
    <span class="inline-flex items-center justify-center p-2 bg-indigo-500 rounded-md shadow-lg">
      <svg class="h-6 w-6 text-white" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" aria-hidden="true"><!-- ... --></svg>
    </span>
  </div>
  <h3 class="text-slate-900 dark:text-white mt-5 text-base font-medium tracking-tight">Writes Upside-Down</h3>
  <p class="text-slate-500 dark:text-slate-400 mt-2 text-sm">
    The Zero Gravity Pen can be used to write in any orientation, including upside-down. It even works in outer space.
  </p>
</div>

<!-- Dark mode not enabled -->
<html>
<body>
  <!-- Will be white -->
  <div class="bg-white dark:bg-black">
    <!-- ... -->
  </div>
</body>
</html>

<!-- Dark mode enabled -->
<html class="dark">
<body>
  <!-- Will be black -->
  <div class="bg-white dark:bg-black">
    <!-- ... -->
  </div>
</body>
</html>
```

Customizações

São adicionadas n arquivo

tailwiind.config.js

Exemplo:

talwiind.config.js

module.exports = {
  content: ['./src/**/*.{html,js}'],
  theme: {
    colors: {
      'blue': '#1fb6ff',
      'purple': '#7e5bef',
      'pink': '#ff49db',
      'orange': '#ff7849',
      'green': '#13ce66',
      'yellow': '#ffc82c',
      'gray-dark': '#273444',
      'gray': '#8492a6',
      'gray-light': '#d3dce6',
    },
    fontFamily: {
      sans: ['Graphik', 'sans-serif'],
      serif: ['Merriweather', 'serif'],
    },
    extend: {
      spacing: {
        '8xl': '96rem',
        '9xl': '128rem',
      },
      borderRadius: {
        '4xl': '2rem',
      }
    }
  },
}

Para criar o config

npx tailwindcss init

Customizar coores - https://tailwindcss.com/docs/customizing-colors

https://tailwindcss.com/docs/

src/input.css

@tailwind base;

@tailwind components;

@tailwind utilities;

Exemplos do Play
```html
<div class="">
  <h1 class="text-4xl bg-sky-600 w-32 bg-contain text-white m-28 p-10 ml-72">OK</h1>
</div>
```
Como saber a faixa de valores aceitos por cada classe?

Uma opção é usar o Playground, que autocompletaa as classes:

https://play.tailwindcss.com/

Quando digitamos py- ele mostra a faixa de valores.

Ou então usando o editor VSCode com a extensão Tailwind CSS Intellisense

Cuidado - nem sempre é uma sequência. Algumas não seguem ordem


Observar que geralmente usamos as classes aos pares, uma para a cor e outra para a dimensão: 

Cursor
    cursor-pointer - ao mover o mouse fica umamãozinha


Responsive

Exemplo

Em duas colunas por default/computador e quando num celulas fica em linhas/row, uma abaixo da outra

flex flex-col md:flex-row

```html
<!-- Width of 16 by default, 32 on medium screens, and 48 on large screens -->
<img class="w-16 md:w-32 lg:w-48" src="...">

<div class="max-w-md mx-auto bg-white rounded-xl shadow-md overflow-hidden md:max-w-2xl">
  <div class="md:flex">
    <div class="md:shrink-0">
      <img class="h-48 w-full object-cover md:h-full md:w-48" src="/img/building.jpg" alt="Modern building architecture">
    </div>
    <div class="p-8">
      <div class="uppercase tracking-wide text-sm text-indigo-500 font-semibold">Company retreats</div>
      <a href="#" class="block mt-1 text-lg leading-tight font-medium text-black hover:underline">Incredible accommodation for your team</a>
      <p class="mt-2 text-slate-500">Looking to take your team away on a retreat to enjoy awesome food and take in some sunshine? We have a list of places to do just that.</p>
    </div>
  </div>
</div>
```
Customizando

tailwind.config.js
```js
module.exports = {
  theme: {
    screens: {
      'tablet': '640px',
      // => @media (min-width: 640px) { ... }

      'laptop': '1024px',
      // => @media (min-width: 1024px) { ... }

      'desktop': '1280px',
      // => @media (min-width: 1280px) { ... }
    },
  }
}
```
Arbitrary values

If you need to use a one-off breakpoint that doesn’t make sense to include in your theme, use the min or max modifiers to generate a custom breakpoint on the fly using any arbitrary value.
```html
<div class="min-[320px]:text-center max-[600px]:bg-sky-300">
  <!-- ... -->
</div>

Learn more about arbitrary value support in the arbitrary values documentation.


 <ul class="list-disc [&>*:nth-child(even)]:text-blue-600 [&>*:nth-child(even)]:font-bold [&>*:nth-child(odd)]:text-green-600 [&>*:nth-child(odd)]:italic  ">
        <li>Even List Item</li>
        <li>Odd List Item</li>
        <li>Even List Item</li>
        <li>Odd List Item</li>
        <li>Even List Item</li>
        <li>Odd List Item</li>
  </ul>

<ul>
    <li class="odd:bg-slate-500 even:bg-slate-300">B</li>
    <li class="odd:bg-slate-500 even:bg-slate-300">B</li>
    <li class="odd:bg-slate-500 even:bg-slate-300">B</li>
    <li class="odd:bg-slate-500 even:bg-slate-300">B</li>
    <li class="odd:bg-slate-500 even:bg-slate-300">B</li>
    <li class="odd:bg-slate-500 even:bg-slate-300">B</li>
</ul>
```
Usando cores em hexadecimal

bg-[#ff00ff]

Podemos também criar novas cores no config

Tamanho de texto

text-[32px]

