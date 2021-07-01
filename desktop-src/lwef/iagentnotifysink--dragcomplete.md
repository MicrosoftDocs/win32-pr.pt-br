---
title: IAgentNotifySink DragComplete
description: IAgentNotifySink DragComplete
ms.assetid: b2d9b9c2-709e-4988-aa92-f129e3836fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb93fbc7bae1ac43d534962659b850561bd50a6d
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120801"
---
# <a name="iagentnotifysinkdragcomplete"></a>IAgentNotifySink::D ragComplete

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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

 

 




