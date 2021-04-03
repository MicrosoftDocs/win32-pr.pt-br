---
title: IAgentNotifySink mover
description: IAgentNotifySink mover
ms.assetid: d1809fdb-df4b-4884-b9e8-2877a814dc9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52563ff3838348b7bf8e6a2bcdfdf20a51c79723
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916576"
---
# <a name="iagentnotifysinkmove"></a>IAgentNotifySink:: mover

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Move(
   long dwCharID,  // character ID
   long x,         // x-coordinate of new location
   long y,         // y-coordinate of new location
   long dwCause    // cause of move state
);                          
```

Notifica um aplicativo cliente quando o caractere é movido.

-   Sem valor de retorno.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador do caractere que foi movido.

</dd> <dt>

<span id="x"></span><span id="X"></span>*w.x.y.*
</dt> <dd>

A coordenada x da nova posição em pixels, relativa à origem da tela (superior esquerda). O local de um caractere é baseado no canto superior esquerdo de seu quadro de animação.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Iar*
</dt> <dd>

A coordenada y da nova posição em pixels, em relação à origem da tela (superior esquerda). O local de um caractere é baseado no canto superior esquerdo de seu quadro de animação.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

A causa da movimentação de caracteres. O parâmetro pode ser um dos seguintes:



| Valor                                                          | Descrição                                                                          |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const NeverMoved curto não assinado** **= 0;**<br/>        | O caractere não foi movido.                                                        |
| **const não assinada curto-** **movida = 1;**<br/>         | O usuário arrastou o caractere.                                                          |
| **const ProgramMoved curto não assinado** **= 2;**<br/>      | Seu aplicativo moveu o caractere.                                                |
| **const OtherProgramMoved curto não assinado** **= 3;**<br/> | Outro aplicativo moveu o caractere.                                             |
| **const SystemMoved curto sem sinal** **= 4**<br/>        | O servidor moveu o caractere para mantê-lo na tela após uma alteração de resolução de tela. |



 

</dd> </dl>

Esse evento é enviado a todos os clientes do caractere.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter:: GetMoveCause**](iagentcharacter--getmovecause.md), [ **IAgentCharacter:: MoveTo**](iagentcharacter--moveto.md)


 

 





