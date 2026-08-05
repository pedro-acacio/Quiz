# Quiz

Protótipo de um jogo de perguntas e respostas em [p5.js](https://p5js.org/), com integração planejada com o Firebase Realtime Database. O projeto está incompleto: hoje existe apenas uma pergunta fixa (uma charada) renderizada na tela e os campos de nome/resposta, mas o botão "Enviar" não processa a resposta (a lógica está comentada no código) e a classe `Contestant` ainda está vazia.

## Tecnologias

- p5.js e p5.dom (via CDN) para desenho e elementos de UI
- p5.play.js incluído no repositório
- Firebase (app + realtime-database, via CDN) configurado em `index.html`, mas com a inicialização parcialmente comentada

## Estrutura

- `sketch.js` — `setup()`/`draw()` do p5.js, cria o canvas e instancia `Quiz`
- `js/Quiz.js` — classe que inicia a exibição da pergunta
- `js/Question.js` — cria os elementos DOM da pergunta, opções e formulário de resposta
- `js/Contestant.js` — classe vazia (esqueleto ainda não implementado)
- `p5.play.js` — biblioteca de sprites do p5

## Como rodar

Abra `index.html` diretamente no navegador ou sirva a pasta com um servidor estático (ex: `npx serve .`). Não há build nem `package.json` — todas as dependências são carregadas via `<script>` no HTML.
