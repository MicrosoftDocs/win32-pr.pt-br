---
description: Saiba como estender a faixa de opções Windows Explorer.
title: Estendendo a faixa de opções
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0C043FF8-3862-4F02-8700-BB556C4F35B8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 635698461f897a08248ea99bf68d534ea8ad24763f926460d2e9ce64181ba2a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860847"
---
# <a name="extending-the-ribbon"></a>Estendendo a faixa de opções

No Windows Explorer, a Faixa de Opções ajuda a tornar as atividades comuns de gerenciamento de arquivos do usuário final mais fáceis e mais descobertas, mas há alterações em andamento para desenvolvedores de aplicativos. Por exemplo, a barra de comandos antiga era extensível livremente, mas a Faixa de Opções é mais restrita no momento. Além disso, a Faixa de Opções não é mostrada por padrão para todas as extensões de namespace, portanto, você precisa optar por obter a Faixa de Opções; caso contrário, você obterá a barra de comandos mais antiga.

As ações disponíveis para usuários na Faixa de Opções se enquadram em três categorias de extensibilidade:

-   A extensibilidade não é necessária. Exemplos: Copiar, Colar, Excluir. Windows trata esses verbos para você.
-   Atualmente, a extensibilidade não é permitida: Exemplos: Zip, Fechar Sessão e outras ações personalizadas. Use o menu de contexto para abranger esses cenários.
-   A extensibilidade é integrada à própria ação. Exemplos: Pesquisar, Email, Imprimir, Novo Item. Você precisa se registrar para esses verbos para incluir seu aplicativo ou formato de arquivo na Faixa de Opções .

Este documento descreve como você pode optar por obter a Faixa de Opções e como se registrar para lidar com verbos da Faixa de Opções específicos.

## <a name="opting-in-to-the-ribbon"></a>Opting in to the Ribbon

Para optar pela Faixa de Opções, sua implementação [**de IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2) deve especificar a Faixa de Opções do **EP \_** [**em IExplorerPaneVisibility::GetPaneState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate) e retornar **EPS \_ FORCE** \| **EPS \_ DEFAULT \_ ON**.

## <a name="extending-the-ribbon-for-file-extensions"></a>Estendendo a faixa de opções para extensões de arquivo

Esses botões da Faixa de Opções são extensíveis com base em extensões de arquivo:

-    Extrair Tudo
-   Montagem \| de burn (um ISO)
-   Reproduzir \| Reproduzir Tudo Adicionar à Playlist \| (verbo: Enqueue)
-   Aberto
-   Editar
-   Propriedades

Quando você se registra para manipular estaticamente os verbos relevantes para novos tipos de arquivo, a Faixa de Opções trata os verbos adequadamente. Registre-se exatamente como faria para verbos de menu de contexto. Para obter mais informações sobre associações de arquivo e registro de verbos, consulte [Verbos e](fa-verbs.md) associações de arquivo e [Criando manipuladores de menu de atalho](context-menu-handlers.md).

## <a name="registering-as-a-default-handler-for-actionids"></a>Registrando como um manipulador padrão para ActionIds

Primeiro, registre sua ProgId na sub-chave AssocActionId apropriada. Cada subkey AssocActionId representa um verbo ou ação que os usuários podem invocar na Faixa de Opções. Neste exemplo, o aplicativo se registra para o ZipSelection ActionID para estender o botão "Extrair Tudo" na Faixa de Opções.

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

Depois que o registro for concluído, você deverá se registrar para lidar com protocolos da mesma forma que faria normalmente, conforme descrito em [Programas Padrão](default-programs.md).

 

 



