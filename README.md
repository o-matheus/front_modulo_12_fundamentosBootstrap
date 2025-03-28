# Exércicio módulo 12

## Objetivos 

* Adicionar o Bootstrap em uma página HTML utilizando a CDN
Para adicionar o Bootstrap no HTML é só adicionar o link para o CSS na head e scrip com url no final do body.

* Nesta página HTML, crie um formulário de cadastro que deverá conter os campos: nome, e-mail e telefone, e um botão para o envio

* Aplique as classes do Bootstrap nos elementos do formulário;

* Crie uma branch chamada exercicio_bootstrap no repositório do curso;

* Envie o link através da plataforma. 
 
1. Adicionando bootstrap ao HTML
```HTML
<head>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css">
</head>

<body>
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
```
2. Criação do formulário
```HTML
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
```
No processo de criação do formulário eu fiquei com algumas dúvidas, no primeiro momento comecei fazendo `.row` e `.col`, mas depois percebi que não fazia sentido eu construir a estrutura assim porque esse exéricio só estou construindo o formulário, então meio que é o processo de criação de componente, fui fazer algumas pesquisas com o GPT e acabei descobrindo e relembrando classes do bs bem interessantes.

Um ponto que foi importante nessa construção foi envelopar cada elemento do formulário em uma div separada, descobri que é uma boa prática e ajuda a refatorar e corrigir o projeto no futuro.

Em relação as classes que utilizei vou falar mais a seguir, mas fiquei especialmente animado pela classe `card` pois vai facilitar bastante na construção de elementos, como uma lista de produtos em um site.

3. Criando branch e definindo qual o destino do push.
* Cria e troca para a nova branch  
`git checkout -b exercicio_bootstrap`

* Faz o push inicial e define o upstream  
`git push -u origin exercicio_bootstrap`





## Descobertas | Relembrando
`<div class="container d-flex justify-content-center align-items-center vh-100">`  
Estrutura utilizada para que o container com o formulário ficasse centralizado na págin precisa de todos esses elementos para funcionar corretamente.

`container` -> Centraliza o conteúdo e adiciona espaçamento nas laterais

`card` -> Estilo card, com fundo branco e bordas arredondads.

`d-flex` -> Adiciona o display flex

`justify-content-center` -> Alinha o conteúdo horizontalmente

`align-items-center` -> Alinha o conteúdo verticalmente, quando o elemento tem uma altura definida, por isso que usei o `vh-100` para que pudesse se trabalhar com uma altura em específico e alinhar o conteúdo.

`p-*` -> Adiciona um padding ao elemento é só substituir a * por um número de 1 a 6, quanto maior o número, maior o padding.

`text-center` -> Texto centralizado

`mb-*` -> Margem inferior, número vai de 1 a 6, quanto maior o número, maior a margem.

`form-label` e `form-control` -> Aplicam uma estilização específica para estes campos.

## Referência 
Gabriel Camarate  
app - https://formulario-jquery-bootstrap-responsive.vercel.app/ source - https://github.com/gabrielcamarate/Formulario-Jquery-Bootstrap-Responsive