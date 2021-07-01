---
title: IAgentNotifySink DblClick
description: IAgentNotifySink DblClick
ms.assetid: 7e86cc9b-8bc3-405e-9bbf-764cec9c3130
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88193f228f94d24384e6bf2b874e9208d67f3e9c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120919"
---
# <a name="iagentnotifysinkdblclick"></a>IAgentNotifySink::D blClick

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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

Um parâmetro que indica o botão do mouse e o estado da chave modificadora. O parâmetro pode retornar qualquer combinação do seguinte:



| Valor  | Descrição                               |
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

 

 




