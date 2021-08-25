---
title: IAgentCommands GetVisible
description: IAgentCommands GetVisible
ms.assetid: 229a02c8-f0a1-4ee5-9bae-961b63792038
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d63ef62a0e57539d633d595901c6cfde1a252ac9ef369f9f56bc3ddaaeea0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961906"
---
# <a name="iagentcommandsgetvisible"></a>IAgentCommands::GetVisible

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of Visible setting for Commands collection
);
```

Recupera o valor da propriedade [**Visible**](visible-property.md) para uma coleção [**de Comandos.**](/windows/desktop/lwef/the-commands-collection-object)

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

O endereço de uma variável que recebe o valor da propriedade [**Visible**](visible-property.md) para uma [**coleção commands.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentCommands::SetVisible**](iagentcommands--setvisible.md), [ **IAgentCommands::SetCaption**](iagentcommands--setcaption.md)


 

 