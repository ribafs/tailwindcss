# Adicionar ao Extends do config
```js
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {
        spacing: {
            '580': '580px',
        },
        colors: {
            'minha-cor': '#993355'        
        },
  },
  plugins: [],
}
```

Usando

text-minha-cor
