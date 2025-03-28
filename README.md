# Exércicio Módulo 12

## Objetivos

* Adicionar o Bootstrap em uma página HTML utilizando a CDN.  
Para adicionar o Bootstrap no HTML, é só adicionar o link para o CSS na `<head>` e o script com a URL no final do `<body>`.

* Nesta página HTML, criar um formulário de cadastro que deverá conter os campos: nome, e-mail e telefone, e um botão para envio.

* Aplicar as classes do Bootstrap nos elementos do formulário.

* Criar uma branch chamada `exercicio_bootstrap` no repositório do curso.

* Enviar o link através da plataforma.

---

### 1. Adicionando Bootstrap ao HTML

```html
<head>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css">
</head>

<body>
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
```

---

### 2. Criação do formulário

```html
<div class="container d-flex justify-content-center align-items-center vh-100">
  <div class="card p-4">
    <h2 class="text-center">Cadastro</h2>
    <form>
      <div class="mb-3">
        <label class="form-label" for="nome">Seu nome:</label>
        <input class="form-control" id="nome" type="text">
      </div>

      <div class="mb-3">
        <label class="form-label" for="email">Seu e-mail:</label>
        <input class="form-control" id="email" type="email">
      </div>

      <div class="mb-3">
        <label class="form-label" for="telefone">Seu telefone:</label>
        <input class="form-control" id="telefone" type="tel">
      </div>

      <button class="btn btn-success w-100">Enviar</button>
    </form>
  </div>
</div>
```

Durante a criação do formulário, surgiram algumas dúvidas. No primeiro momento, comecei utilizando `.row` e `.col`, mas depois percebi que não fazia sentido construir a estrutura assim, pois neste exercício estou focando apenas na construção do formulário. Isso me levou a encarar esse processo como a criação de um componente.

Fazendo algumas pesquisas, acabei redescobrindo e aprendendo novas classes do Bootstrap. Um ponto importante foi **envelopar cada campo do formulário em uma `div` separada**, algo que descobri ser uma **boa prática** pois facilita a refatoração e manutenção no futuro.

Em relação às classes utilizadas, destaque especial para `card`, que me deixou animado pois vi que pode facilitar bastante a construção de elementos como listas de produtos em sites.

---

### 3. Criando a branch e fazendo o push

* Cria e troca para a nova branch:  
```bash
git checkout -b exercicio_bootstrap
```

* Faz o push inicial e define o upstream:  
```bash
git push -u origin exercicio_bootstrap
```

---

## Descobertas | Relembrando

```html
<div class="container d-flex justify-content-center align-items-center vh-100">
```

Essa estrutura foi usada para centralizar o formulário na tela. Cada classe tem uma função específica:

- `container` → Centraliza o conteúdo e adiciona espaçamento lateral.
- `card` → Cria uma "caixa" com fundo branco e bordas arredondadas.
- `d-flex` → Ativa o Flexbox.
- `justify-content-center` → Centraliza horizontalmente.
- `align-items-center` → Centraliza verticalmente **se houver altura definida**.
- `vh-100` → Define que o container ocupa 100% da altura da tela.
- `p-*` → Padding (espaçamento interno), valores de `1` a `5`.
- `text-center` → Centraliza o texto.
- `mb-*` → Margem inferior, também de `1` a `5`.
- `form-label` e `form-control` → Estiliza os elementos de formulário.

---

## Referência

**Gabriel Camarate**  
App: [https://formulario-jquery-bootstrap-responsive.vercel.app/](https://formulario-jquery-bootstrap-responsive.vercel.app/)  
Repositório: [https://github.com/gabrielcamarate/Formulario-Jquery-Bootstrap-Responsive](https://github.com/gabrielcamarate/Formulario-Jquery-Bootstrap-Responsive)

