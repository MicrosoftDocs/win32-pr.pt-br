---
title: IAgentBalloon getVisible
description: IAgentBalloon getVisible
ms.assetid: 328af211-4ea4-482c-8487-42c8e4cd66b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55fd8dbf6792d34b15f82ab6c402e9a0e7eb3ad3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822997"
---
# <a name="iagentballoongetvisible"></a>IAgentBalloon:: getVisible

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for word balloon
);                   // Visible setting
```

Determina se o balão de palavra está visível ou oculto.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

Endereço de uma variável que recebe **true** se a palavra balão estiver visível e **false** se estiver oculta.

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentBalloon:: setVisible**](iagentballoon--setvisible.md)


 

 




