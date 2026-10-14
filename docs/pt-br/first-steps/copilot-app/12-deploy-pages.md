---
title: "Lição 12 - Publique o site com o GitHub Pages"
description: "Use o aplicativo GitHub Copilot para configurar um workflow do Pages, revisar o pull request e confirmar que o Space Quiz está no ar."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publique o Space Quiz no GitHub Pages para que todos possam acessá-lo. O Copilot pode preparar o workflow e orientar a publicação, mas cabe a você revisar as alterações e confirmar que o site está no ar.

Nesta lição, você vai:

- pedir ao Copilot para configurar a publicação no GitHub Pages.
- revisar o workflow e o pull request antes de fazer o merge.
- acompanhar a publicação e verificar o site publicado.

## Cenário

O Space Quiz já está em um repositório do GitHub, mas as pessoas ainda precisam de uma maneira simples de experimentá-lo. Publicar o site de um único arquivo com o GitHub Pages permite acessá-lo por uma URL pública sem adicionar um servidor ou dependência de runtime.

## Peça ao Copilot para publicar o site

Na sessão do aplicativo Copilot para `space-quiz`, envie este prompt:

```plaintext
Ative o GitHub Pages para este repositório. Crie um workflow do GitHub Actions que compile o site, se necessário, e o publique no GitHub Pages. Se ainda não existir um README, adicione um que descreva o aplicativo e explique como executá-lo localmente. Crie um pull request com essas alterações e faça o merge depois que as verificações obrigatórias forem aprovadas. Acompanhe a publicação até que ela seja concluída e, em seguida, informe a URL final do site no ar. Se você não tiver permissão para ativar o Pages ou fazer o merge, diga exatamente o que preciso aprovar ou fazer; não informe que a publicação foi concluída antes de o site estar no ar.
```

![Diagrama de três etapas: pull request do space-quiz mesclado; execução bem-sucedida do GitHub Actions Deploy website com as etapas Build website, Upload artifact e Deploy to Pages; e Space Quiz disponível em yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este prompt pede ao agente para criar e mesclar um pull request e alterar as configurações do Pages do repositório. Antes de continuar, revise o diff, as permissões de publicação e todas as solicitações de aprovação do GitHub.

## Revise o workflow e verifique a publicação

1. Confirme que o README só foi adicionado se o repositório ainda não tinha um.
2. Revise as alterações do pull request, incluindo as etapas de build e publicação do workflow.
3. Faça o merge somente depois que as verificações obrigatórias do pull request forem aprovadas.
4. Acompanhe a execução de publicação do GitHub Actions até ela ser concluída com sucesso.
5. Abra a URL informada e confirme que o Space Quiz carrega.

Se o agente não puder ativar o Pages ou mesclar o pull request, siga as instruções específicas fornecidas por ele. Não considere a tarefa concluída até que a publicação termine com sucesso e o site esteja no ar.

## Resumo e próximos passos

O Space Quiz está disponível como um site publicado, e você verificou a publicação em vez de confiar apenas no relato do agente. Continue com a [Lição 13: Revisão e próximos passos][next-lesson].

[next-lesson]: ../13-review/
