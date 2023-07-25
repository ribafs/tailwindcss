# Adicionar ao Extends do config
```js
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {
        colors: {
            'minha-cor': '#993355'        
        },
  },
  plugins: [],
}
```

Exemplo de uso

class="text-minha-cor"
