---
title: Clique em IAgentNotifySink
description: Clique em IAgentNotifySink
ms.assetid: 6587fed8-4651-4c5c-b257-6e3f991cd3a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 154b35d85b86d1bd835275e93e6ea4c397b01240910066debd826c3570f806fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477072"
---
# <a name="iagentnotifysinkclick"></a>IAgentNotifySink::Click

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Click(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

Notifica um aplicativo cliente quando o usuário clica no ícone de barra de tarefas de um caractere ou caractere.

-   Sem valor de retorno.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador do caractere clicado.

</dd> <dt>

<span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*
</dt> <dd>

Um parâmetro que indica o botão do mouse e o estado da chave modificadora. O parâmetro pode retornar qualquer combinação do seguinte:



| Valor  | Descrição                                    |
|--------|------------------------------------------------|
| 0x0001 | Botão Esquerdo                                    |
| 0x0010 | Botão Central                                  |
| 0x0002 | Botão Direito                                   |
| 0x0004 | Tecla shift para baixo                                 |
| 0x0008 | Tecla de controle para baixo                               |
| 0x0020 | Tecla Alt para baixo                                   |
| 0x1000 | Evento ocorrido no ícone da barra de tarefas do caractere |



 

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

A coordenada X do ponteiro do mouse em pixels, em relação à origem da tela (superior esquerdo).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

A coordenada Y do ponteiro do mouse em pixels, em relação à origem da tela (superior esquerdo).

</dd> </dl>

Esse evento é enviado para o cliente ativo de entrada do caractere. Se nenhum dos clientes do caractere estiver ativo de entrada, o servidor notifica o cliente ativo do caractere. Se o caractere estiver visível, o servidor também torna esse cliente ativo de entrada e envia [**o IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md). Se o caractere estiver oculto, o caractere também será mostrado automaticamente.

 

 




