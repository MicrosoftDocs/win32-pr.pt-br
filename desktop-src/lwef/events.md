---
title: IAgentNotifySink
description: IAgentNotifySink
ms.assetid: vs|msagent|~\paface_2xet.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b43a092ddd9c50ff7aacb0254c4773a43005759ab23b6682aaf6484d5aef4839
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725776"
---
# <a name="iagentnotifysink"></a>IAgentNotifySink

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

IAgentNotifySink notifica os clientes quando determinadas alterações de estado ocorrem. Essas funções também estão disponíveis em [IAgentNotifySinkEx.](iagentnotifysinkex.md)

**Métodos em ordem Vtable**



| IAgentNotifySink                                                      | Descrição                                                                              |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**Comando**](command-method.md)                                     | Ocorre quando o servidor processa um comando definido pelo cliente.                               |
| [**ActivateInputState**](iagentnotifysink--activateinputstate.md)    | Ocorre quando um caractere se torna ou deixa de ser ativo de entrada.                            |
| [**BalloonVisibleState**](iagentnotifysink---balloonvisiblestate.md) | Ocorre quando o estado Visível **do** caractere muda.                                   |
| [**Evento Clicar**](click-event.md)                                    | Ocorre quando um caractere é clicado.                                                      |
| [**Evento DblClick**](dblclick-event.md)                              | Ocorre quando um caractere é clicado duas vezes.                                               |
| [**DragStart**](/windows/desktop/lwef/dragstart-event)                                | Ocorre quando um usuário começa a arrastar um caractere.                                          |
| [**DragComplete**](https://www.bing.com/search?q=**DragComplete**)                          | Ocorre quando um usuário para de arrastar um caractere.                                           |
| [**RequestStart**](iagentnotifysink--requeststart.md)                | Ocorre quando o servidor começa a processar um [**objeto Request.**](/windows/desktop/lwef/the-request-object)    |
| [**RequestComplete**](iagentnotifysink--requestcomplete.md)          | Ocorre quando o servidor conclui o processamento de um [**objeto Request.**](/windows/desktop/lwef/the-request-object) |
| [**Indicador**](iagentnotifysink--bookmark.md)                        | Ocorre quando o servidor processa um indicador.                                             |
| [**Ocioso**](iagentnotifysink--idle.md)                                | Ocorre quando o servidor inicia ou termina o processamento ocioso.                                   |
| [**Mover**](iagentnotifysink--move.md)                                | Ocorre quando um caractere foi movido.                                                  |
| [**Tamanho**](iagentnotifysink---size.md)                               | Ocorre quando um caractere foi ressado.                                                |
| [**BalloonVisibleState**](iagentnotifysink---balloonvisiblestate.md) | Ocorre quando o estado de visibilidade do balão de palavra de um caractere muda.                  |



 

Os eventos IAgentNotifySink::Restart e IAgentNotifySink::Shutdown, com suporte em versões anteriores do Microsoft Agent, agora estão obsoletos. Embora seja compatível com compatibilidade com backward, o servidor não envia mais esses eventos.

 

 