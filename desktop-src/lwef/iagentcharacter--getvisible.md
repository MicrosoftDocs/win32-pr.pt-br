---
title: IAgentCharacter getVisible
description: IAgentCharacter getVisible
ms.assetid: 6e8e3a68-a7bb-4afb-a753-836fe82a0b24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0593b9b3a193b9d5910888b81b4ecba90469b1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084466"
---
# <a name="iagentcharactergetvisible"></a>IAgentCharacter:: getVisible

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for character Visible setting
);
```

Determina se o quadro de animação do caractere está visível no momento.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

Endereço de uma variável que recebe **true** se o quadro do caractere estiver visível e **false** se estiver oculto.

</dd> </dl>

Você pode usar esse método para determinar se o quadro do caractere está visível no momento. Para tornar um caractere visível, use o método [**show**](/windows/desktop/lwef/iagentcharacter--show) . Para ocultar um caractere, use o método [**Hide**](/windows/desktop/lwef/iagentcharacter--hide) .

 

 