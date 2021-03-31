---
title: IAgentCommands remover
description: IAgentCommands remover
ms.assetid: 1f41aa2d-e50b-48a8-87fc-fda4730b035a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d0c3321de3d06b5e2ebea873a4bace91482d8c5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104162001"
---
# <a name="iagentcommandsremove"></a>IAgentCommands:: Remove

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Remove(
   long dwID  // Command ID
);
```

Remove o [**comando**](/windows/desktop/lwef/the-command-object) especificado de uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*
</dt> <dd>

A ID de um [**comando**](/windows/desktop/lwef/the-command-object) a ser removido da coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

A remoção de um [**comando**](/windows/desktop/lwef/the-command-object) de uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) também o Remove do menu pop-up e da **janela de comandos de voz** quando seu aplicativo está em entrada-ativo.

## <a name="see-also"></a>Consulte Também

[**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md), [**IAgentCommands:: RemoveAll**](iagentcommands--removeall.md)


 

 