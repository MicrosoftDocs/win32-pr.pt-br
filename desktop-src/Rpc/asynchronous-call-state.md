---
title: Estado de chamada assíncrona
description: Esta página descreve o estado de chamada assíncrona para chamadas RPC.
ms.assetid: 4a594dad-a8a1-44e9-8648-ddc2539c234c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7ab00104b305ac87fa87883031d2425f229ce5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478622"
---
# <a name="asynchronous-call-state"></a>Estado de chamada assíncrona

Esta página descreve o estado de chamada assíncrona para chamadas RPC.

## <a name="client-behavior"></a>Comportamento do cliente




| Estado | Nome do estado | Ação | 
|-------|------------|--------|
| C | Faça a chamada | Tornar o RPC<ul><li>Em caso de sucesso, vá para o estado WComp</li><li>Na exceção, vá para o fim</li></ul>Para falhar: Vá para pode<br /> | 
| Podem | Cancelar a chamada | Chame <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>go to WComp<br /> | 
| WComp | Aguardar a conclusão | Aguarde até que a notificação de notificationCall seja recebida<br /> Ir para comp<br /> | 
| Às | Completion | Emitir <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>ir para o fim<br /> | 
| End | 




 

## <a name="server-behavior"></a>Comportamento do servidor



| Estado | Nome do estado     | Ação                                                                                                                                                                                                              |
|-------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D     | Dispatch       | A chamada é expedida pelo runtimeProcess RPC<br/> Ir para comp<br/> Para falhar fatalmente (ao executar no thread RPC): gerar exceção; ir para o fim<br/> Para falhar normalmente: Vá para um<br/> |
| A     | Anular a chamada | Chamar [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)ir para o fim<br/>                                                                                                                                             |
| Às  | Completion     | Emitir [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)ir para o fim<br/>                                                                                                                                      |
| End   |                |                                                                                                                                                                                                                     |



 

 

 





