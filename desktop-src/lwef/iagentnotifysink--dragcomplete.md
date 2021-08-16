---
title: IAgentNotifySink DragComplete
description: IAgentNotifySink DragComplete
ms.assetid: b2d9b9c2-709e-4988-aa92-f129e3836fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b63c24abd41f0509293ba2fafeb055f195a4d13ad354662e8d32d0fb1715e1fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477024"
---
# <a name="iagentnotifysinkdragcomplete"></a>IAgentNotifySink::D ragComplete

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT DragComplete(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

Notifica um aplicativo cliente quando o usuário para de arrastar um caractere.

-   Sem valor de retorno.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador do caractere arrastado.

</dd> <dt>

<span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*
</dt> <dd>

Um parâmetro que indica o botão do mouse e o estado da chave modificadora. O parâmetro pode retornar qualquer combinação do seguinte:



| Valor  | Descrição      |
|--------|------------------|
| 0x0001 | Botão Esquerdo      |
| 0x0010 | Botão Central    |
| 0x0002 | Botão Direito     |
| 0x0004 | Tecla shift para baixo   |
| 0x0008 | Tecla de controle para baixo |
| 0x0020 | Tecla Alt para baixo     |



 

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

A coordenada X do ponteiro do mouse em pixels, em relação à origem da tela (superior esquerdo).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

A coordenada Y do ponteiro do mouse em pixels, em relação à origem da tela (superior esquerdo).

</dd> </dl>

 

 




