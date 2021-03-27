---
description: Saiba como estender a faixa de forma do Windows Explorer.
title: Estendendo a faixa de faixas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0C043FF8-3862-4F02-8700-BB556C4F35B8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6a0a3af3ac21e0bac0471bc9a987849536303556
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501412"
---
# <a name="extending-the-ribbon"></a>Estendendo a faixa de faixas

No Windows Explorer, a faixa de faixas ajuda a tornar mais fáceis e mais detectáveis as atividades comuns de gerenciamento de arquivos do usuário final, mas há alterações andamento para desenvolvedores de aplicativos. Por exemplo, a antiga barra de comandos era extensível livremente, mas a faixa de faixas é mais restrita no momento. Além disso, a faixa de opção não é mostrada por padrão para todas as extensões de namespace, portanto, você precisa optar por obter a faixa de opção; caso contrário, você obterá a barra de comandos mais antiga.

As ações disponíveis para os usuários na faixa de faixas se enquadram em três categorias de extensibilidade:

-   A extensibilidade não é necessária. Exemplos: copiar, colar, excluir. O Windows lida com esses verbos para você.
-   A extensibilidade não é permitida no momento: exemplos: zip, sessão de fechamento e outras ações personalizadas. Use o menu de contexto para abordar esses cenários.
-   A extensibilidade é incorporada à própria ação. Exemplos: Pesquisar, enviar por email, imprimir, novo item. Você precisa se registrar para esses verbos para incluir seu aplicativo ou formato de arquivo na faixa de faixas.

Este documento descreve como você pode optar por obter a faixa de opção e como registrá-la para lidar com verbos de faixa de opção específicos.

## <a name="opting-in-to-the-ribbon"></a>Optando pela faixa de faixas

Para aceitar a faixa de opção, sua implementação do [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2) deve especificar a **\_ faixa** de opção do EP em [**IExplorerPaneVisibility:: getpanestate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate) e retornar o EPS **\_ Force** \| **\_ padrão \_ em**.

## <a name="extending-the-ribbon-for-file-extensions"></a>Estendendo a faixa de faixas para extensões de arquivo

Esses botões de faixa de lista são extensíveis com base nas extensões de arquivo:

-    Extrair Tudo
-   \|Gravação de montagem (um ISO)
-   Reproduzir \| reproduzir tudo \| Adicionar à lista de reprodução (verbo: enfileirar)
-   Aberto
-   Editar
-   Propriedades

Quando você se registra para lidar estaticamente com os verbos relevantes para novos tipos de arquivo, a faixa de faixas manipula os verbos adequadamente. Você se registra exatamente como faria para verbos de menu de contexto. Para obter mais informações sobre associações de arquivo e registro para verbos, consulte [verbos e associações de arquivo](fa-verbs.md) e [criando manipuladores de menu de atalho](context-menu-handlers.md).

## <a name="registering-as-a-default-handler-for-actionids"></a>Registrando como um manipulador padrão para ActionIds

Primeiro, Registre seu ProgId na subchave AssocActionId apropriada. Cada subchave AssocActionId representa um verbo ou uma ação que os usuários podem invocar na faixa de faixas. Neste exemplo, o aplicativo registra para o ActionID ZipSelection para estender o botão "extrair tudo" na faixa de faixas.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         Explorer.AssocActionId.ZipSelection
            shell
               open
                  command
                     (Default) = %SystemRoot%\[Your App].exe
      Microsoft
         Windows
            CurrentVersion
               Your App Name
                  Capabilities
                     URL Protocol
                     FriendlyTypeName = @%SystemRoot%\explorer.exe,-1234
```

Depois que o registro for concluído, você deverá se registrar para manipular protocolos da mesma forma como faria normalmente, conforme descrito em [programas padrão](default-programs.md).

 

 



