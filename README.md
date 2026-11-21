# Revise — Cartões de estudo

Uma app para alunos estudarem com cartões (flashcards) a partir dos seus apontamentos.
Funciona em português e inglês, com modo claro e escuro.

## O que faz

- **Disciplinas e pastas** — cada disciplina tem uma cor; as pastas (e subpastas) organizam os temas.
- **Apontamentos** — escrever, colar ou carregar ficheiros de texto, Markdown, PDF ou Word (.docx).
- **Cartões** — feitos a partir dos apontamentos, editáveis à mão.
- **Escolha múltipla** — cada cartão tem a resposta certa e 3 erradas; o aluno escolhe e só depois vê se acertou.
- **Virar cartões** — modo alternativo: pensa na resposta, vira o cartão e avalia (Outra vez / Difícil / Bem / Fácil).
- **Repetição espaçada** — os cartões que o aluno sabe voltam mais tarde; os que erra voltam mais cedo.
- **Ficha de revisão** — um resumo dos apontamentos para a última revisão.
- **Simulador de teste** — teste de uma pasta ou disciplina, com número de perguntas e tempo limite à escolha; nota de 0 a 20, resultado por tema, correção de cada pergunta e histórico dos testes. Dentro do Claude, pode incluir perguntas de desenvolvimento escritas e corrigidas pela IA.

## Como usar

É um único ficheiro: `index.html`. Abre-o num navegador ou publica-o com o GitHub Pages:

1. Cria um repositório no GitHub e carrega o `index.html` (e este `README.md`).
2. No repositório, vai a **Settings → Pages**.
3. Em **Source**, escolhe **Deploy from a branch**, branch `main`, pasta `/ (root)`, e carrega em **Save**.
4. Passado um minuto, a app fica em `https://<o-teu-utilizador>.github.io/<nome-do-repositório>/`.

## Fora do Claude: o que muda

A versão completa corre dentro do Claude, que lhe dá a IA e a conta onde os dados ficam guardados.
Fora do Claude (GitHub Pages ou o ficheiro aberto no computador), a app funciona assim:

| | Dentro do Claude | Fora do Claude |
|---|---|---|
| Onde ficam os dados | Na conta do aluno, em qualquer dispositivo | Só naquele navegador (apagar o histórico apaga os cartões) |
| Fazer cartões | A IA lê os apontamentos e escreve as perguntas | Só a partir de linhas no formato `Termo: definição` |
| Respostas erradas da escolha múltipla | Escritas pela IA | Escritas à mão no editor do cartão (✎) |
| Ler fotografias de apontamentos | Sim | Não |
| Ficha de revisão | Sim | Não |
| Ler PDF e Word | Sim | Sim |

Exemplo de apontamentos que funcionam sem IA:

```
Núcleo: controla a célula e contém o ADN.
Mitocôndrias: libertam energia da glicose pela respiração aeróbia.
Ribossomas: onde se fazem as proteínas.
```

## Tecnologia

HTML, CSS e JavaScript num só ficheiro, sem instalação. Bibliotecas carregadas só quando são precisas:
[pdf.js](https://mozilla.github.io/pdf.js/) para PDF e [mammoth.js](https://github.com/mwilliamson/mammoth.js) para Word.
Letras: Nunito e Kalam (Google Fonts).
