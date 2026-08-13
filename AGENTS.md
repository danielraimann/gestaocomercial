# Regras permanentes — Gestão Comercial

Este repositório (`danielraimann/gestaocomercial`) contém um aplicativo em produção, publicado pelo GitHub Pages a partir da branch `main` em <https://gestao.dcpf.com.br>. Há usuários e dados reais no Firebase.

## Proibições

- Nunca recriar o aplicativo do zero.
- Nunca criar outro Firebase.
- Nunca apagar, migrar ou resetar o Firestore.
- Nunca alterar UIDs nem apagar usuários.
- Nunca mudar a estrutura de armazenamento existente sem autorização explícita.
- Nunca alterar DNS, CNAME ou `gestao.dcpf.com.br` sem autorização explícita.

## Itens que devem ser preservados integralmente

- Firebase Authentication e Firestore.
- `firebaseConfig` e `projectId` atuais.
- Caminho `painelGestaoUsuarios/{uid}/dados/principal`.
- Todos os dados existentes.
- Favicon e responsividade desktop/mobile.
- F-LOG, produtos ocultos por gerente, Cadastros, Referências, Prioritários, Visão Consolidada e Pontuação POBJ Produção.
- Geração atual de PDFs, salvo quando uma mudança nela for explicitamente solicitada.

## Fluxo obrigatório para qualquer alteração

1. Executar `git fetch`/`git pull` e confirmar que a `main` local corresponde à remota.
2. Ler o código atual antes de modificar.
3. Implementar somente a alteração solicitada.
4. Validar HTML e JavaScript.
5. Testar a funcionalidade alterada.
6. Confirmar que Firebase/Auth/Firestore não sofreram alterações indevidas.
7. Revisar o `git diff`.
8. Criar commit descritivo.
9. Fazer push para `main`.
10. Aguardar a publicação do GitHub Pages.
11. Abrir e validar <https://gestao.dcpf.com.br>.
12. Confirmar que a versão publicada contém o commit.
13. Informar SHA, testes executados, resultado do deploy e validação do domínio.

Uma tarefa só está concluída depois de commit, push, deploy e validação em produção.
