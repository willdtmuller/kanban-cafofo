# kanban-cafofo

Quadro kanban compartilhado para organizar as tarefas da casa nova. 🐈‍⬛

## Como acessar

O quadro está publicado via GitHub Pages em:
**https://willdtmuller.github.io/kanban-cafofo/**

Qualquer pessoa com esse link consegue ver e editar o quadro (os dados são salvos em um armazenamento compartilhado no [JSONBin](https://jsonbin.io)). Não há login — é um link "quem tem, acessa".

## Como funciona

- Todo o app está em um único arquivo: `index.html` (HTML + CSS + JS puro, sem build step).
- Os dados do quadro (cards, colunas, responsáveis) ficam salvos em um "bin" no JSONBin.
- Ao abrir a página, ela carrega automaticamente o estado mais recente.
- Ao editar (mover card, adicionar, marcar responsável, etc.), ela salva automaticamente no JSONBin.
- O botão de atualizar no topo busca manualmente a versão mais recente (útil se duas pessoas estiverem editando ao mesmo tempo em abas diferentes).

## Como editar o código

1. Clone o repositório:
   ```bash
   git clone https://github.com/willdtmuller/kanban-cafofo.git
   ```
2. Edite `index.html` normalmente (é só HTML/CSS/JS, sem dependências, sem build).
3. Abra o arquivo direto no navegador pra testar localmente.
4. Commite e dê push:
   ```bash
   git add index.html
   git commit -m "descrição da mudança"
   git push
   ```
5. O GitHub Pages atualiza automaticamente em 1-2 minutos após o push na branch `main`.

## Configuração do armazenamento (JSONBin)

As credenciais do JSONBin (Bin ID e Access Key) estão no topo do `<script>` em `index.html`. A Access Key usada está restrita (permissão de leitura/atualização apenas neste bin específico, sem permissão de exclusão), então mesmo estando em um arquivo público não dá acesso à conta inteira do JSONBin.

Se precisar trocar de bin ou gerar uma nova chave, acesse [jsonbin.io](https://jsonbin.io) e atualize as constantes `JSONBIN_BIN_ID` e `JSONBIN_ACCESS_KEY` no início do script.

## Aviso de privacidade

Este repositório é **privado**, mas a página publicada via GitHub Pages é **pública para quem tiver o link** (limitação do GitHub Pages em contas free). Não é indexada pelo Google, mas não é protegida por senha.
