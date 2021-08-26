---
title: IAgentNotifySink DblClick
description: IAgentNotifySink DblClick
ms.assetid: 7e86cc9b-8bc3-405e-9bbf-764cec9c3130
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 317e11b52d9ab01eb3ecf145925601cee3bf4b4245039390427a7370a7362d32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961516"
---
# <a name="iagentnotifysinkdblclick"></a>IAgentNotifySink::D blClick

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT DblClick(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

Notifica um aplicativo cliente quando o usuário clica duas vezes em um caractere.

-   Sem valor de retorno.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador do caractere clicado duas vezes.

</dd> <dt>

<span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*
</dt> <dd>

Um parâmetro que indica o botão do mouse e o estado de chave do modificador. O parâmetro pode retornar qualquer combinação do seguinte:



| Valor  | Descrição                               |
|--------|------------------------------------------------|
| 0x0001 | Botão esquerdo                                    |
| 0x0010 | Botão do meio                                  |
| 0x0002 | Botão direito                                   |
| 0x0004 | Tecla Shift para baixo                                 |
| 0x0008 | Tecla de controle para baixo                               |
| 0x0020 | Tecla Alt para baixo                                   |
| 0x1000 | Ocorreu um evento no ícone da barra de tarefas do caractere |



 

</dd> <dt>

<span id="x"></span><span id="X"></span>*w.x.y.*
</dt> <dd>

A coordenada x do ponteiro do mouse em pixels, em relação à origem da tela (superior esquerda).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Iar*
</dt> <dd>

A coordenada y do ponteiro do mouse em pixels, em relação à origem da tela (superior esquerda).

</dd> </dl>

Esse evento é enviado para o cliente de entrada-ativo do caractere. Se nenhum dos clientes do caractere for entrada-ativo, o servidor notificará o cliente ativo do caractere. Se o caractere estiver visível, o servidor também tornará a entrada do cliente ativa e enviará o [**IAgentNotifySink:: ActivateInputState**](iagentnotifysink--activateinputstate.md). Se o caractere estiver oculto, o caractere também será mostrado automaticamente.

 

 




