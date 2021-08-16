---
description: A principal responsabilidade de qualquer Painel de Controle item é exibir uma janela que permita que o usuário veja e manipule as configurações.
title: Diretrizes da Experiência do Usuário
ms.topic: article
ms.date: 09/24/2020
ms.assetid: f03a154b-9781-4718-8244-3d57fee0755e
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 15ef54d44a466f3c766075eae771ccac9d74e20c0622d6092530f1015a538425
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857075"
---
# <a name="user-experience-guidelines"></a>Diretrizes da Experiência do Usuário

A principal responsabilidade de qualquer Painel de Controle item é exibir uma janela que permita que o usuário veja e manipule as configurações. Confira as diretrizes de experiência do usuário [(UX)](../uxguide/winenv-ctrl-panels.md) dos Painéis de Controle para o comportamento e o design Painel de Controle itens. As diretrizes discutidas nesse tópico mostram um método de fluxo de tarefas para organizar um Painel de Controle item. Isso coloca as configurações mais importantes em um home page. As configurações usadas com menos frequência são colocadas em páginas spoke ou acessadas de links em um painel lateral.

O Painel de Controle inclui muitos itens que seguem essas diretrizes, como Central de Facilidade de Acesso e Central de Rede e Compartilhamento. Outros Painel de Controle itens usam o formato de folha de propriedades da caixa de diálogo com guias, como nas versões anteriores do Windows. Exemplos incluem o item Mouse e Opções da Internet. O uso do formato de folha de propriedades deve ser descontinuado. Se você criar novos Painel de Controle, siga as diretrizes de fluxo de tarefas.

No passado, Painel de Controle itens eram empacotados como .cpl arquivos. Isso não é mais necessário. Novos Painel de Controle novos itens devem ser implementados como um arquivo .exe autônomo ou como uma opção de sinalizador de linha de comando para o arquivo executável principal do aplicativo.

> [!Note]  
> Em sistemas de 64 bits, os itens Painel de Controle de 32 bits são exibidos no Painel de Controle quando a opção exibir itens Painel de Controle de **32** bits está selecionada. Os itens de 32 bits devem estar localizados na pasta %SystemRoot% \\ SysWOW64 a ser exibida. Eles não exigem nenhum registro posterior.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Painel de Controle itens](control-panel-applications.md)
</dt> <dt>

[Registrando Painel de Controle itens](registering-control-panel-items.md)
</dt> <dt>

[Usando CPLApplet](using-cplapplet.md)
</dt> <dt>

[Painel de Controle processamento de mensagens](message-processing.md)
</dt> <dt>

[Executando Painel de Controle itens](executing-control-panel-items.md)
</dt> <dt>

[Estendendo itens Painel de Controle sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Atribuindo Painel de Controle categorias](assigning-control-panel-categories.md)
</dt> <dt>

[Criando links de tarefa pesquisáveis para um Painel de Controle item](creating-searchable-task-links.md)
</dt> <dt>

[Acessando o Painel de Controle no modo Cofre](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



