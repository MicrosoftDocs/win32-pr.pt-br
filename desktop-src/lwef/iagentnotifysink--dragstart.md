---
title: IAgentNotifySink DragStart
description: IAgentNotifySink DragStart
ms.assetid: b3905b99-69e4-4046-aab9-2322618935aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 031e78319beb0f62ddb0ea340fca0cd7ed88c0a2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292208"
---
# <a name="iagentnotifysinkdragstart"></a>IAgentNotifySink::D ragStart

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT DragStart(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

Notifica um aplicativo cliente quando o usuário começa a arrastar um caractere.

-   Sem valor de retorno.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador do caractere arrastado.

</dd> <dt>

<span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*
</dt> <dd>

Um parâmetro que indica o botão do mouse e o estado de chave do modificador. O parâmetro pode retornar qualquer combinação do seguinte:



|        |                  |
|--------|------------------|
| 0x0001 | Botão esquerdo      |
| 0x0010 | Botão do meio    |
| 0x0002 | Botão direito     |
| 0x0004 | Tecla Shift para baixo   |
| 0x0008 | Tecla de controle para baixo |
| 0x0020 | Tecla Alt para baixo     |



 

</dd> <dt>

<span id="x"></span><span id="X"></span>*w.x.y.*
</dt> <dd>

A coordenada x do ponteiro do mouse em pixels, em relação à origem da tela (superior esquerda).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Iar*
</dt> <dd>

A coordenada y do ponteiro do mouse em pixels, em relação à origem da tela (superior esquerda).

</dd> </dl>

 

 




