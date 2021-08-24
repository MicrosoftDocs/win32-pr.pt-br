---
title: IAgentCommands remover
description: IAgentCommands remover
ms.assetid: 1f41aa2d-e50b-48a8-87fc-fda4730b035a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5875d1377aecc7e28554bac6aae1ccb2b4f515f730a6ab1b0b3a83cec7573418
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477189"
---
# <a name="iagentcommandsremove"></a>IAgentCommands:: Remove

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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


 

 