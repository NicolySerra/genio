# 🔮 Genius — Bola de Cristal

Um pequeno projeto interativo desenvolvido para praticar **HTML, CSS e JavaScript**, simulando uma bola de cristal capaz de responder perguntas aleatoriamente.

O usuário digita uma pergunta, clica em **"Fazer Pergunta"** e recebe uma resposta selecionada aleatoriamente a partir de uma lista predefinida.

> 🔮 Um projeto simples, divertido e criado para colocar JavaScript em prática.

 
## 🎯 Sobre o projeto

A ideia surgiu como um exercício de introdução à programação web e interação com o usuário.

O projeto possui uma interface simples contendo:

* 🔮 Uma imagem de bola de cristal
* ✏️ Campo para digitar uma pergunta
* 🔘 Botão para enviar a pergunta
* 💬 Área para exibir a resposta

Ao realizar uma pergunta, o JavaScript escolhe uma resposta aleatória e a apresenta na tela.

---

## ⚙️ Como funciona

O fluxo da aplicação é simples:

```text
Usuário
   ↓
Digita uma pergunta
   ↓
Clica em "Fazer Pergunta"
   ↓
JavaScript verifica se o campo foi preenchido
   ↓
Escolhe uma resposta aleatória
   ↓
Exibe pergunta + resposta
   ↓
Aguarda 3 segundos
   ↓
Esconde a resposta
```

---

## 🛠️ Tecnologias utilizadas

* **HTML5** — estrutura da página
* **CSS3** — estilização e layout
* **JavaScript** — lógica e interação
* **DOM** — manipulação dos elementos da página

---

## 🧠 Conceitos praticados

### 📦 Arrays

As possíveis respostas ficam armazenadas em um array:

```javascript
const respostas = [
    "Certeza!",
    "Não tenho tanta certeza.",
    "É decididamente assim.",
    "Não conte com isso.",
    "Sem dúvidas!",
    "Pergunte novamente mais tarde."
]
```

Isso permite adicionar ou remover respostas facilmente.

---

### 🎲 Geração de números aleatórios

Para escolher uma resposta diferente a cada pergunta, foi utilizado:

```javascript
const numeroAleatorio =
    Math.floor(Math.random() * totalRespostas)
```

O número gerado é utilizado como índice do array:

```javascript
respostas[numeroAleatorio]
```

Dessa forma, qualquer resposta disponível pode ser selecionada.

---

### 🔎 Validação de entrada

Antes de processar a pergunta, o programa verifica se o usuário realmente digitou alguma coisa:

```javascript
if (inputPergunta.value == "") {
    alert("Digite sua pergunta")
    return
}
```

Isso evita executar a lógica quando o campo está vazio.

---

### 🌐 Manipulação do DOM

O JavaScript acessa elementos do HTML através de:

```javascript
document.querySelector()
```

Por exemplo:

```javascript
const inputPergunta =
    document.querySelector("#inputPergunta")
```

Isso permite que o JavaScript leia o que o usuário digitou e altere o conteúdo da página.

---

### ⏱️ Temporização

Depois de mostrar a resposta, o projeto utiliza `setTimeout()` para escondê-la após três segundos:

```javascript
setTimeout(function() {
    elementoResposta.style.opacity = 0;
    buttonPerguntar.removeAttribute("disabled")
}, 3000)
```

Além de controlar a interface, isso também impede que o usuário faça várias perguntas simultaneamente durante o processo.

---

## 📂 Estrutura

Como o projeto foi criado originalmente em um único arquivo:

```text
Genius/
│
└── index.html
```

O HTML contém:

* Estrutura da interface
* CSS dentro da tag `<style>`
* JavaScript dentro da tag `<script>`

---

## 🚀 Possíveis melhorias

Este projeto foi criado como exercício, mas existem várias possibilidades de evolução:

* [ ] Separar HTML, CSS e JavaScript em arquivos diferentes
* [ ] Adicionar animação à bola de cristal
* [ ] Criar respostas com diferentes efeitos visuais
* [ ] Permitir pressionar `Enter` para fazer a pergunta
* [ ] Adicionar histórico das perguntas
* [ ] Melhorar a responsividade
* [ ] Substituir `alert()` por mensagens na própria interface
* [ ] Adicionar acessibilidade ao formulário
* [ ] Criar uma interface mais moderna
* [ ] Adicionar modo escuro e efeitos visuais

---

## 🧪 O que aprendi

Este projeto foi importante para praticar a transição entre uma página **estática** e uma página **interativa**.

Além de construir a interface, foi possível trabalhar com:

```text
HTML
 ↓
Estrutura

CSS
 ↓
Visual

JavaScript
 ↓
Lógica + Interação
```

O projeto representa uma das primeiras experiências com **manipulação do DOM e lógica executada diretamente no navegador**.

---

## 🎮 Experimente

Digite qualquer pergunta e descubra o que a bola de cristal tem a dizer. 🔮

---

## 📌 Observação

Este é um projeto experimental desenvolvido durante meus estudos de desenvolvimento web.

A aplicação não possui qualquer finalidade de previsão real — as respostas são escolhidas **aleatoriamente** a partir de uma lista predefinida.

---

### 👩🏻‍💻 Desenvolvido por Nicoly Serra

[GitHub](https://github.com/NicolySerra)
