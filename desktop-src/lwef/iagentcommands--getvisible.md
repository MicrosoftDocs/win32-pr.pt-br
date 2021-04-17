---
title: IAgentCommands getVisible
description: IAgentCommands getVisible
ms.assetid: 229a02c8-f0a1-4ee5-9bae-961b63792038
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 853a47f6136779415a08adc3c891d9b5cc95dcca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105763504"
---
# <a name="iagentcommandsgetvisible"></a>IAgentCommands:: getVisible

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of Visible setting for Commands collection
);
```

Recupera o valor da propriedade [**Visible**](visible-property.md) para uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

O endereço de uma variável que recebe o valor da propriedade [**Visible**](visible-property.md) para uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentCommands:: setvisível**](iagentcommands--setvisible.md), [ **IAgentCommands:: SetCaption**](iagentcommands--setcaption.md)


 

 