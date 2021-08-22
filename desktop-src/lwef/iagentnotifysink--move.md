---
title: IAgentNotifySink mover
description: IAgentNotifySink mover
ms.assetid: d1809fdb-df4b-4884-b9e8-2877a814dc9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16f32df3058a5b5c8e0a4e02a98f9a97afdbff56f349a63fceb5d70a9001391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105163"
---
# <a name="iagentnotifysinkmove"></a>IAgentNotifySink:: mover

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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


 

 





