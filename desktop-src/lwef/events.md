---
title: IAgentNotifySink
description: IAgentNotifySink
ms.assetid: vs|msagent|~\paface_2xet.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb2ccfd4acf4a64c229379aeea5847fbe044b7d5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007470"
---
# <a name="iagentnotifysink"></a>IAgentNotifySink

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O IAgentNotifySink notifica os clientes quando determinadas alterações de estado ocorrem. Essas funções também estão disponíveis em [IAgentNotifySinkEx](iagentnotifysinkex.md).

**Métodos em ordem vtable**



| IAgentNotifySink                                                      | Descrição                                                                              |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**Comando**](command-method.md)                                     | Ocorre quando o servidor processa um comando definido pelo cliente.                               |
| [**ActivateInputState**](iagentnotifysink--activateinputstate.md)    | Ocorre quando um caractere se torna ou deixa de ser inserido-ativo.                            |
| [**BalloonVisibleState**](iagentnotifysink---balloonvisiblestate.md) | Ocorre quando o estado **visível** do caractere é alterado.                                   |
| [**Evento Clicar**](click-event.md)                                    | Ocorre quando um caractere é clicado.                                                      |
| [**Evento DblClick**](dblclick-event.md)                              | Ocorre quando um caractere é clicado duas vezes.                                               |
| [**DragStart**](/windows/desktop/lwef/dragstart-event)                                | Ocorre quando um usuário começa a arrastar um caractere.                                          |
| [**DragComplete**](https://www.bing.com/search?q=**DragComplete**)                          | Ocorre quando um usuário para de arrastar um caractere.                                           |
| [**RequestStart**](iagentnotifysink--requeststart.md)                | Ocorre quando o servidor começa a processar um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .    |
| [**RequestComplete**](iagentnotifysink--requestcomplete.md)          | Ocorre quando o servidor conclui o processamento de um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) . |
| [**Indicador**](iagentnotifysink--bookmark.md)                        | Ocorre quando o servidor processa um indicador.                                             |
| [**Ocioso**](iagentnotifysink--idle.md)                                | Ocorre quando o servidor inicia ou termina o processamento ocioso.                                   |
| [**Mover**](iagentnotifysink--move.md)                                | Ocorre quando um caractere é movido.                                                  |
| [**Tamanho**](iagentnotifysink---size.md)                               | Ocorre quando um caractere é redimensionado.                                                |
| [**BalloonVisibleState**](iagentnotifysink---balloonvisiblestate.md) | Ocorre quando o estado de visibilidade do balão de palavras de um caractere é alterado.                  |



 

Os eventos IAgentNotifySink:: restart e IAgentNotifySink:: Shutdown, com suporte em versões anteriores do Microsoft Agent, agora estão obsoletos. Embora haja suporte para compatibilidade com versões anteriores, o servidor não envia mais esses eventos.

 

 