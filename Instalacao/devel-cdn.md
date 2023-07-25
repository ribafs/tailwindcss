# Ambiente de desenvolvimento

Usando o CDN ao invés de instalar com node, perdemos o poder das customizações, mas temos as funcionalidades básicas
Nem o auto-complete do VSCode funciona.

Acessar o VSCode

code .

Criar o index.html

index.html, assim
```htmll
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            clifford: '#da373d',
          }
        }
      }
    }
  </script>
</head>
<body>
  <h1 class="text-3xl font-bold underline text-clifford">
    Hello world!
  </h1>
</body>
</html>
```
Agora nosso index.html está pronto para receber código do Tailwind


