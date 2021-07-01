---
title: IAgentNotifySink DragStart
description: IAgentNotifySink DragStart
ms.assetid: b3905b99-69e4-4046-aab9-2322618935aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33ae89f9e24c6c7b0ec69fba1a98b3a64a18620
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120820"
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



| Valor  | Descrição      |
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

 

 




