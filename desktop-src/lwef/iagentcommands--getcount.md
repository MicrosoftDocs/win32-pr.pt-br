---
title: GetCount IAgentCommands
description: GetCount IAgentCommands
ms.assetid: 17140eda-17b0-49c2-8d50-5a38a553191a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ece3e007b644b370ee721cef2d273fa50d43ce
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365837"
---
# <a name="iagentcommandsgetcount"></a>IAgentCommands:: GetCount

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of count of commands
);                    
```

Recupera o número de objetos de [**comando**](/windows/desktop/lwef/the-command-object) em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*
</dt> <dd>

Endereço de uma variável que recebe o número de [**comandos**](/windows/desktop/lwef/the-command-object) em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

*pdwCount* inclui apenas o número de [**comandos**](/windows/desktop/lwef/the-command-object) que você define em sua coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . O servidor ou outras entradas de cliente não estão incluídas.

 

 