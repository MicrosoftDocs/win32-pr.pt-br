---
title: IAgentCommands GetCount
description: IAgentCommands GetCount
ms.assetid: 17140eda-17b0-49c2-8d50-5a38a553191a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 810f9fc268bc13558e4e51a3b64dd6f5b1d54caa5a055d9c90b6a8d11c48b3c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749820"
---
# <a name="iagentcommandsgetcount"></a>IAgentCommands::GetCount

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of count of commands
);                    
```

Recupera o número de objetos [**Command**](/windows/desktop/lwef/the-command-object) em uma [**coleção De**](/windows/desktop/lwef/the-commands-collection-object) comandos.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*
</dt> <dd>

Endereço de uma variável que recebe o número de [**Comandos em**](/windows/desktop/lwef/the-command-object) uma coleção [**de Comandos.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> </dl>

*pdwCount* inclui apenas o número de [**Comandos**](/windows/desktop/lwef/the-command-object) que você define na coleção [**Comandos.**](/windows/desktop/lwef/the-commands-collection-object) O servidor ou outras entradas de cliente não estão incluídos.

 

 