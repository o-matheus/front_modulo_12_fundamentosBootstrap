# Fundamentos do Bootstrap

## Menu
[Aula 1 - Conheça o Bootstrap](#aula-1---conheça-o-bootstrap)
[Aula 1 - Grids](#aula-2---grids)

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

