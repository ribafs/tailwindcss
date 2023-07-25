# Comparando os frameworks Tailwind CSS e Bootstrap

Bootstrap é o framework HTML, CSS e JavaScript mais popular para construir projetos responsivos e mobile-first na web. Tailwind CSS, por outro lado, é o framework CSS mais popular para o desenvolvimento rápido de interface do usuário.

A principal diferença entre o TailwindCSS e o Bootstrap é que o Tailwind CSS não é um kit de interface do usuário. Ao contrário dos kits de interface do usuário, como Bootstrap, Bulma e Foundation, o Tailwind CSS não possui um template padrão ou componentes de interface do usuário integrados. Em vez disso, ele vem com widgets predefinidos que você pode usar para criar seu site do zero.

## Tailwind CSS é melhor que Bootstrap?

Frameworks como o Bootstrap abstraíram a criação de componentes ao ponto de obrigar os desenvolvedores a usar apenas os padrões disponíveis fornecidos. O mesmo vale para outros frameworks do tipo kit de interface do usuário. Alguns podem argumentar que sobrescrever o framework com nosso próprio CSS é uma opção, mas se sobrescrevermos muito, então há algum sentido em usar o framework? Estaríamos puxando a biblioteca e ainda escrevendo nosso próprio código  —  isso é apenas mais arquivos para se preocupar, e não estamos economizando tempo.

Outro problema que encontrei com os sites com Bootstrap é que eles quase sempre são parecidos, então isso inibe nossa capacidade de incorporar criatividade no ambiente de desenvolvimento. Esta é uma das vantagens do Tailwind CSS: sua capacidade de construir facilmente interfaces de usuário complexas sem encorajar dois sites a parecerem iguais.

Outra vantagem importante de usar o Tailwind CSS sobre o Bootstrap é que, como aplicativos e sites são compostos de widgets pré-projetados, o Tailwind CSS não impõe decisões de design difíceis de reverter.

Trabalhar com Tailwind CSS significa usar um conjunto de classes utilitárias que permitem trabalhar exatamente com o que você precisa. Na minha opinião, essa é uma maneira legal de criar interfaces de usuário mais flexíveis para a criatividade dos desenvolvedores.

Outra vantagem que eu realmente aprecio  —  e tenho certeza que todo desenvolvedor frontend também apreciaria  —  é nunca ter que se preocupar com mudanças em um elemento afetando outro elemento relacionado. Não há mais tabulação para frente e para trás entre HTML e folhas de estilo em seu editor, não há mais volta para verificar e ver o que você nomeou esse outro elemento. Na minha opinião, este é o futuro.

O que significa utilidade em primeiro lugar/utility first?

Tailwind CSS é uma biblioteca utilitária, o que significa simplesmente que, ao contrário do Bootstrap, o Tailwind não fornece componentes pré-estilizados automaticamente. Em vez disso, fornece classes utilitárias que nos ajudam a estilizar nossos componentes de determinadas maneiras e nos permitem construir nossas próprias classes.

Bootstrap é conhecido por sua capacidade de resposta, enquanto os defensores do Tailwind CSS normalmente valorizam a personalização do framework. A melhor escolha para você depende de suas prioridades e requisitos do projeto, mas vamos falar sobre por que o Tailwind CSS está rapidamente ganhando popularidade e uso mais difundido.

A primeira versão alfa do Tailwind CSS apareceu em 1º de novembro de 2017, de acordo com seu histórico de lançamentos do GitHub. Após mais 43 lançamentos/releases e mais de 2.200 commits de 88 colaboradores, o primeiro lançamento estável, Tailwind CSS v1.0, foi feito em 13 de maio de 2019. Assim como o Bootstrap, o Tailwind é um projeto de código aberto e gratuito com licença MIT.

O Tailwind CSS pode ser melhor descrito como um framework "utilitário em primeiro lugar". Os frameworks que priorizam a utilidade são compostos de classes pequenas e simples que podem ser aplicadas a elementos para criar uma interface de usuário ou UI. Na superfície, usar o Tailwind não parece muito diferente de escrever estilos inline. No entanto, o que este framework oferece é a personalização. Em vez de ser restringido pelos componentes pré-fabricados do Bootstrap, você pode essencialmente criar sua própria interface do usuário com o Tailwind para atender às necessidades do seu projeto.

## Exemplo
```html
<section class="flex flex-col">
  <div class="flex flex-col md:flex-row md:space-x-3 items-center space-y-3 md:space-y-0">
    <div class="border border-gray-200 rounded">
      <img src="https://via.placeholder.com/300x200.png" />
      <p class="p-5">This is a card made with Bootstrap</p>
    </div>
  </div>
</section>
```
Um card criado com Tailwind

## Utilitários

A estrutura principal do Tailwind CSS oferece apenas classes utilitárias. Se queremos estilizar um componente HTML, temos que fazê-lo usando apenas as classes utilitárias e aplicando-as aos diferentes elementos HTML. À primeira vista, é muito semelhante ao estilo inline.

    • As classes de utilitários flex e a flex-col podem ser usadas para criar um contêiner flexbox com uma direção flex indo na direção da coluna.
    • A classe de utilitário md:flex-row pode ser usada para alterar a direção do flex de coluna para linha quando o tamanho da tela for médio (768px) ou maior.
    • As classes utilitárias md:space-x-3 e md:space-y-0 podem ser usadas para aumentar ou diminuir o espaço entre os elementos filhos.
    • As classes de utilidade border, border-gray-200 e rounded podem ser usadas juntas para adicionar uma borda cinza arredondada ao redor do elemento.

## Componentes

A estrutura principal do Tailwind CSS não fornece classes de componentes. No entanto, você pode pagar para obter componentes oficiais da interface do usuário diretamente pelo Tailwind ou encontrar alguns componentes criados pela comunidade ou de código aberto gratuitamente. Você também pode criar suas próprias classes de componentes usando a diretiva @apply do Tailwind para extrair padrões de utilitários repetidos em classes CSS personalizadas.

## Exemplos

Simples botão demo
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>DEMO</title>
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss/dist/tailwind.min.css" rel="stylesheet">
</head>
<body>
    <div class="container">
        <button class="button">Buy</button>
        <button class="btn btn-primary">Buy</button>
<!-- Below we have the Tailwind implementation of a simple button  -->
        <button class="bg-purple hover:bg-purple-dark text-white font-bold py-2 px-4 rounded">Buy</button>
    </div>
</body>
</html>
```
No exemplo acima, você pode ver como é fácil implementar um componente de botão com Tailwind CSS.

## Demo de card/cartão simples

O código abaixo é um exemplo simples de um card criado com o framework Tailwind CSS . Se você estiver familiarizado com CSS, talvez já consiga entender algumas das coisas que estão acontecendo com o estilo. Pode ser um pouco complicado memorizar tudo isso no começo, mas uma vez que você tenha alguma familiaridade com a sintaxe, você ficará bem.

O trecho de código abaixo possui um container que possui uma sombra para telas grandes devido à classe shadow-lg e um fundo branco implementado com bg-white. Você também notará as classes px-4 e py-1 - elas são apenas para ajudar no preenchimento/padding dos eixos x e y para o botão de mensagem.
```html
<div class="bg-white mx-auto max-w-sm shadow-lg rounded-lg overflow-hidden"> 
  <div class="sm:flex sm:items-center px-6 py-4"> 
    <img class="block h-16 sm:h-24 rounded-full mx-auto mb-4 sm:mb-0 sm:mr-4 sm:ml-0" src="https://avatars2.githubusercontent.com/u/4323180?s=400&u=4962a4441fae9fba5f0f86456c6c506a21ffca4f&v=4" alt=""> <div class="text-center sm:text-left sm:flex-grow"> 
      <div class="mb-4"> 
        <p class="text-xl leading-tight">Adam Wathan</p> 
        <p class="text-sm leading-tight text-gray-400">Developer at NothingWorks Inc.</p> 
      </div> 
      <div> 
        <button class="text-xs font-semibold rounded-full px-4 py-1 leading-normal bg-white border-2 border-purple-400 text-purple-500 hover:bg-purple-600 hover:text-white">Message</button> 
      </div> 
    </div> 
  </div> 
</div>

Aqui está um CodePen que mostra como é o código acima:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>DEMO</title>
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">
    <!--<link href="https://cdn.jsdelivr.net/npm/tailwindcss/dist/tailwind.min.css" rel="stylesheet">-->
      <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.4/dist/tailwind.min.css" rel="stylesheet">
</head>
<body>
    
<div class="bg-white mx-auto max-w-sm shadow-lg rounded-lg overflow-hidden">
  <div class="sm:flex sm:items-center px-6 py-4">
    <img class="block h-16 sm:h-24 rounded-full mx-auto mb-4 sm:mb-0 sm:mr-4 sm:ml-0" src="https://avatars2.githubusercontent.com/u/4323180?s=400&u=4962a4441fae9fba5f0f86456c6c506a21ffca4f&v=4" alt="">
    <div class="text-center sm:text-left sm:flex-grow">
      <div class="mb-4">
        <p class="text-xl leading-tight">Adam Wathan</p>
        <p class="text-sm leading-tight text-gray-400">Developer at NothingWorks Inc.</p>
      </div>
      <div>
        <button class="text-xs font-semibold rounded-full px-4 py-1 leading-normal border-2 border-purple-400 text-purple hover:bg-purple-400 hover:text-white">Message</button>
      </div>
    </div>
  </div>
</div>
</body>
</html>
```
Tailwind CSS vs. Bootstrap: desempenho

A configuração padrão do Tailwind vem com 36,4 KB reduzidos e compactados em g. Comparado ao Bootstrap de 22,1 KB , o  Tailwind é 14,3 KB mais pesado. Você pode estar pensando: "Esse é realmente o caminho a seguir em termos de desempenho?"

A razão para isso é simples: o Tailwind vem pré-embalado com muitas opções e estilos para os usuários escolherem, e inclui todas essas variações para reduzir a tendência de escrever seu próprio CSS. Felizmente, o Tailwind vem com algumas estratégias que você pode usar para manter seu CSS gerado pequeno e com bom desempenho.

Isso torna possível incluir apenas o código que realmente precisamos nos projetos, ignorando todo o resto  — ao contrário do Bootstrap, no qual há muito código de sobrecarga. Esse recurso de atualização reduz o tempo de compilação de 158 segundos para 8 segundos.

Podemos obter a quantidade exata de variações de cores que precisamos em um projeto, assim:
```js
// ...

module.exports = {
  // ...

  textColors: {
    'black': colors['black'],
    'grey-darker': colors['grey-darker'],
    'grey-dark': colors['grey-dark'],
    'red-dark': colors['red-dark'],
    'red': colors['red'],
    'blue-dark': colors['blue-dark'],
    'blue': colors['blue'],
    // ...
  }
}
```
Remova CSS não utilizado com PurgeCSS

O Tailwind também remove CSS não utilizado com PurgeCSS, uma ferramenta para remover CSS não utilizado do seu projeto. Ele faz isso simplesmente comparando os nomes de classe CSS disponíveis em seu modelo com os nomes de classe usados e, em seguida, removendo o CSS não utilizado.

Escolha o número exato de telas que você precisa

Tailwind CSS permite que você escolha a quantidade exata de tamanhos de tela que você precisa. Veja como definir menos telas afeta a saída:

    • Five screen sizes (default): 36.4KB 
    • Four screen sizes: 29.4KB 
    • Three screen sizes: 22.4KB 
    • Two screen sizes: 15.4KB 
    • One screen size: 8.4KB 

Extraindo padrões de utilitários com @apply

Digamos que você esteja reutilizando um determinado estilo de botão em vários lugares. Redigitar o mesmo tipo de especificação para o mesmo componente torna-se um pouco chato. Não se preocupe: o Tailwind tem uma maneira de reutilizar o estilo com @apply.

Exemplo:
```html
<button class="btn-gray">
  Button 
</button> 

<style> 
.btn-blue { 
  @apply bg-gray text-white font-bold py-2 px-4 rounded; 
} 
.btn-gray:hover { 
  @apply bg-gray-dark; 
} 
</style>
```
Observação: hover:, focus: e {screen}: as variantes do utilitário não podem ser misturadas diretamente.

https://blog.logrocket.com/tailwind-css-vs-bootstrap-ui-kits/ 
```html
<!DOCTYPE html>
<html>
  
<head>
    <!-- Tailwind CSS -->
    <link href=
"https://unpkg.com/tailwindcss@^1.0/dist/tailwind.min.css"
        rel="stylesheet">
    <title>Tailwind CSS</title>
</head>
  
<body style="background-color: gray;">
  
    <!--Card 1-->
    <div class=" w-full lg:max-w-full lg:flex">
        <div class="border-r border-b border-l 
            border-gray-400 lg:border-l-0 
            lg:border-t lg:border-gray-400 bg-white
            \rounded-b lg:rounded-b-none lg:rounded-r
            p-4 leading-normal">
            <p class="text-gray-700 text-base">
                This Card is made using Tailwind CSS.
            </p>
        </div>
    </div>
</body>
  
</html>
```
https://www.geeksforgeeks.org/tailwind-css-vs-bootstrap/

https://www.makeuseof.com/tailwind-css-vs-bootstrap-which-is-a-better-framework/

https://javascript.plainenglish.io/tailwind-vs-bootstrap-which-one-should-you-choose-8186f765e6ab

