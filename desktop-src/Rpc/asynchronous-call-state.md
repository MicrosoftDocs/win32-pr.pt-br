---
title: Estado de chamada assíncrona
description: Esta página descreve o estado de chamada assíncrona para chamadas RPC.
ms.assetid: 4a594dad-a8a1-44e9-8648-ddc2539c234c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96331a18b267b2e44072840727c8fd06afd11d6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823045"
---
# <a name="asynchronous-call-state"></a>Estado de chamada assíncrona

Esta página descreve o estado de chamada assíncrona para chamadas RPC.

## <a name="client-behavior"></a>Comportamento do cliente



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Estado</th>
<th>Nome do estado</th>
<th>Ação</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>Faça a chamada</td>
<td>Tornar o RPC
<ul>
<li>Em caso de sucesso, vá para o estado WComp</li>
<li>Na exceção, vá para o fim</li>
</ul>
Para falhar: Vá para pode<br/></td>
</tr>
<tr class="even">
<td>Podem</td>
<td>Cancelar a chamada</td>
<td>Chame <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>go to WComp<br/></td>
</tr>
<tr class="odd">
<td>WComp</td>
<td>Aguardar a conclusão</td>
<td>Aguarde até que a notificação de notificationCall seja recebida<br/> Ir para comp<br/></td>
</tr>
<tr class="even">
<td>Às</td>
<td>Completion</td>
<td>Emitir <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>ir para o fim<br/></td>
</tr>
<tr class="odd">
<td>End</td>


</tr>
</tbody>
</table>



 

## <a name="server-behavior"></a>Comportamento do servidor



| Estado | Nome do estado     | Ação                                                                                                                                                                                                              |
|-------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D     | Dispatch       | A chamada é expedida pelo runtimeProcess RPC<br/> Ir para comp<br/> Para falhar fatalmente (ao executar no thread RPC): gerar exceção; ir para o fim<br/> Para falhar normalmente: Vá para um<br/> |
| Um     | Anular a chamada | Chamar [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)ir para o fim<br/>                                                                                                                                             |
| Às  | Completion     | Emitir [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)ir para o fim<br/>                                                                                                                                      |
| End   |                |                                                                                                                                                                                                                     |



 

 

 





