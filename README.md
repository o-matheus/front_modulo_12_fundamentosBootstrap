# Fundamentos do Bootstrap

## Menu
[Aula 1 - Conheça o Bootstrap](#aula-1---conheça-o-bootstrap)  
[Aula 2 - Grids](#aula-2---grids)  
[Aula 3 - Tipografia](#aula-3---tipografia)
[Aula 4 - Tabelas](#aula-4---tabelas)

## Aula 1 - Conheça o Bootstrap

**Framework** → Um framework é uma estrutura reutilizável composta por bibliotecas, padrões e ferramentas que auxiliam desenvolvedores a criar aplicações de forma mais rápida, organizada, padronizada, segura e eficiente.

> "Porções de código que alguém já escreveu, com componentes que podemos reutilizar para construir botões, formulários, campos de alerta e outras coisas."

Para adicionar o Bootstrap ao seu projeto, basta incluir este comando:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css">
```

Entre no site do [Bootstrap](https://getbootstrap.com/) e acesse a documentação para ver a forma mais atualizada de como adicioná-lo ao seu projeto.

## Aula 2 - Grids

O sistema de Grids do Bootstrap é o que o tornou tão popular. Ele trabalha com **12 colunas**.

### Estrutura básica do Grid no Bootstrap:
```html
<div class="container"> <!-- Onde vai ficar o conteúdo -->
    <div class="row"> <!-- As linhas -->
        <div class="col"> <!-- Colunas, o máximo são 12 -->
            
        </div>
    </div>
</div>
```

Se colocarmos um sufixo na classe `col`, como `col-(1 a 12)`, já podemos ir construindo a estrutura do site e definindo como as informações serão apresentadas.

### Breakpoints e responsividade:
O Bootstrap possui categorias com **breakpoints** diferentes, possibilitando criar um CSS responsivo apenas com suas classes.

![Breakpoints](README/image.png)

- `col-lg-8` → Em telas maiores, o conteúdo ocupa 8 colunas das 12.
- `col-sm-12` → Em telas menores, o conteúdo ocupa todas as colunas disponíveis.
- `g-0` → Remove o espaçamento entre as colunas.

### Dica com Emmet:
```emmet
.container>.row>.col*5>img+h3
```
Esse atalho cria rapidamente uma estrutura com 5 colunas, cada uma contendo uma imagem (`<img>`) e um título (`<h3>`).

#### Explicação dos atalhos:
- `.a>.b` → Classe `a` é pai da classe `b`
- `.b>.c*5` → Classe `b` é pai de cinco elementos com a classe `c`
- `.c>img+h3` → Cada `c` conterá uma tag `<img>` e uma `<h3>`

### Resultado final:
```html
<div class="container">
    <div class="row">
        <div class="col">
            <img src="" alt="">
            <h3></h3>
        </div>
        <div class="col">
            <img src="" alt="">
            <h3></h3>
        </div>
        <div class="col">
            <img src="" alt="">
            <h3></h3>
        </div>
        <div class="col">
            <img src="" alt="">
            <h3></h3>
        </div>
        <div class="col">
            <img src="" alt="">
            <h3></h3>
        </div>
    </div>
</div>
```

## Aula 3 - Tipografia

Nesta aula vamos falar de fontes e tipografia no Bootstrap.

O Bootstrap aplica estilos e efeitos tipográficos a diversas tags de texto como `<h1>` a `<h6>`, `<p>`, `<mark>`, entre outras.

### Principais classes:

- `h1` a `h6` → Aplicam estilos de títulos a outros elementos, como parágrafos.
- `display-1` a `display-6` → Aumentam o tamanho da fonte e reduzem o peso do traço, criando títulos de destaque.

## Aula 4 - Tabelas

Aprenderemos sobre tabelas e quais recursos o Bootstrap oferece para estilizar e organizar melhor esses elementos.

### Principais tags de uma tabela:
*(Algumas tags adicionais serão comentadas no código abaixo)*

```html
<table class="table">
    <caption>Tabela de produtos</caption> <!-- Legenda -->
    <thead> <!-- Cabeçalho - Geralmente com os títulos -->
        <tr> <!-- Linha do cabeçalho -->
            <th>Nome do produto</th> <!-- Coluna cabeçalho -->
            <th>Preço original</th>
        </tr>
    </thead>
    <tbody>
        <tr> <!-- Linha onde ficam as células de conteúdo -->
            <td>Iphone 13</td> <!-- Coluna com conteúdo -->
            <td>R$7.000,00</td>
        </tr>
    </tbody>
    <!-- <tfoot>Rodapé da tabela</tfoot> (pode ser utilizado para totais, notas ou sumários) -->
</table>
```

### Classes mais usadas para tabelas no Bootstrap:

- `table` → Define largura 100% e bordas visuais entre as linhas.
- `table-primary` → Estilo com cor primária.
- `table-secondary` → Estilo com cor secundária.
- `table-success` → Estilo com tom de sucesso (verde).
- `table-danger` → Estilo para erros ou dados negativos (vermelho).
- `table-warning` → Estilo para alertas ou atenção (amarelo).
- `table-info` → Estilo com tom informativo (azul claro).
- `table-light` → Estilo claro, acinzentado.
- `table-dark` → Estilo escuro.

### Dica:
Mesmo utilizando o Bootstrap, é importante manter um **arquivo CSS próprio** para ajustes finos no layout e personalização de estilos específicos.

