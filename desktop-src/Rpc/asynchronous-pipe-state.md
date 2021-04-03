---
title: Estado de pipe assíncrono
description: Esta página descreve o estado de pipe assíncrono para chamadas RPC.
ms.assetid: af937eba-6b70-447a-af76-a8e27f5754e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8396b08c7ef7b8152457d9426883645fab39bdef
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007121"
---
# <a name="asynchronous-pipe-state"></a>Estado de pipe assíncrono

Esta página descreve o estado de pipe assíncrono para chamadas RPC.

## <a name="in-pipe"></a>NO pipe

Comportamento do cliente

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Estado</th>
<th>Nome do Estado</th>
<th>Ação</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>Faça a chamada</td>
<td>Tornar o RPC
<ul>
<li>Em ir para o estado de êxito WS</li>
<li>Na exceção, vá para o fim</li>
</ul>
Para falhar: Vá para pode<br/></td>
</tr>
<tr class="even">
<td>P</td>
<td>Push</td>
<td>Fazer um envio por push
<ul>
<li>Em caso de falha, vá para o fim</li>
<li>Em caso de sucesso, vá para WS</li>
</ul>
Para falhar: Vá para pode<br/></td>
</tr>
<tr class="odd">
<td>WS</td>
<td>Aguardar envio</td>
<td>Aguardar notificação
<ul>
<li>Em caso de falha ao obter uma notificação, acesse pode</li>
<li>Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de sucesso for recebido e mais dados precisarem ser enviados, vá para P</li>
<li>Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de sucesso for recebido e mais dados não precisarem ser enviados, vá para NP</li>
<li>Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> de falha for recebida, acesse comp</li>
</ul>
Para falhar: Vá para pode<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>Envio por push nulo</td>
<td>Enviar 0 bytes por push (Push nulo)
<ul>
<li>Em caso de falha, vá para o fim</li>
<li>Em caso de sucesso, vá para WComp</li>
</ul>
Para falhar: Vá para pode<br/></td>
</tr>
<tr class="odd">
<td>Podem</td>
<td>Cancelar a chamada</td>
<td>Chame <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>go to WComp<br/></td>
</tr>
<tr class="even">
<td>WComp</td>
<td>Aguardar a conclusão</td>
<td>Aguarde até que a notificação de notificationCall seja recebida.<br/> Ir para comp<br/></td>
</tr>
<tr class="odd">
<td>Às</td>
<td>Completion</td>
<td>Emitir <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>ir para o fim<br/></td>
</tr>
<tr class="even">
<td>End</td>


</tr>
</tbody>
</table>



 

Comportamento do servidor

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Estado</th>
<th>Nome do Estado</th>
<th>Ação</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D</td>
<td>Dispatch</td>
<td>A chamada é expedida pelo tempo de execução RPC, vá para P<br/> Para falhar fatalmente (ao executar no thread RPC): gerar exceção; ir para o fim<br/> Para falhar normalmente: Vá para um<br/></td>
</tr>
<tr class="even">
<td>P</td>
<td>Recepção</td>
<td>Fazer um pull
<ul>
<li>Em caso de falha, vá para o fim</li>
<li>Em caso de êxito e conclusão síncrona com bytes diferentes de zero lidos, vá para P</li>
<li>Em caso de êxito e conclusão síncrona com zero bytes lidos (pull nulo), vá para comp</li>
<li>Em caso de êxito e conclusão assíncrona (ERROR_IO_PENDING é retornado), vá para WP</li>
</ul>
Para falhar: Vá para um<br/></td>
</tr>
<tr class="odd">
<td>WP</td>
<td>Aguardar pull</td>
<td>Aguardar notificação
<ul>
<li>Em caso de falha ao obter uma conclusão, vá para um</li>
<li>Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de falha for recebido, vá para um</li>
<li>Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de sucesso for recebida com bytes diferentes de zero, leia ir para P</li>
<li>Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de sucesso for recebida com zero bytes lidos (pull nulo), vá para comp</li>
<li>Se uma falha for recebida, vá para um</li>
</ul>
Para falhar: Vá para um<br/></td>
</tr>
<tr class="even">
<td>Um</td>
<td>Anular a chamada</td>
<td>Chamar <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>ir para o fim<br/></td>
</tr>
<tr class="odd">
<td>Às</td>
<td>Completion</td>
<td>Chamar <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>ir para o fim<br/></td>
</tr>
<tr class="even">
<td>End</td>


</tr>
</tbody>
</table>



 

## <a name="out-pipe"></a>SAÍDA de pipe

Comportamento do cliente

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Estado</th>
<th>Nome do Estado</th>
<th>Ação</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>Faça a chamada</td>
<td>Tornar o RPC
<ul>
<li>Em caso de sucesso, vá para P</li>
<li>Em caso de falha, vá para comp</li>
</ul>
Para falhar: Vá para pode<br/></td>
</tr>
<tr class="even">
<td>P</td>
<td>Recepção</td>
<td>Fazer um pull
<ul>
<li>Em caso de falha, vá para o fim</li>
<li>Em caso de êxito e conclusão síncrona com bytes diferentes de zero lidos, vá para P</li>
<li>Em caso de êxito e conclusão síncrona com zero bytes lidos (pull nulo), vá para WComp</li>
<li>Em caso de êxito e conclusão assíncrona (ERROR_IO_PENDING é retornado), vá para WP</li>
</ul>
Para falhar: Vá para pode<br/></td>
</tr>
<tr class="odd">
<td>WP</td>
<td>Aguardar pull</td>
<td>Aguardar notificação
<ul>
<li>Em caso de falha ao obter uma conclusão, vá para pode</li>
<li>Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de falha for recebida, vá para Can</li>
<li>Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de sucesso for recebida com bytes diferentes de zero, leia ir para P</li>
<li>Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de sucesso for recebida com zero bytes lidos (pull nulo), vá para comp</li>
<li>Se uma falha for recebida, vá pode</li>
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
<td>Aguarde a notificação. A notificação de conclusão de chamada deve ser recebida.<br/> Ir para comp<br/></td>
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



 

Comportamento do servidor

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Estado</th>
<th>Nome do Estado</th>
<th>Ação</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D</td>
<td>Dispatch</td>
<td>A chamada é expedida pelo tempo de execução RPC, vá para P<br/> Para falhar fatalmente (ao executar no thread RPC): gerar exceção; ir para o fim<br/> Para falhar normalmente: Vá para um<br/></td>
</tr>
<tr class="even">
<td>P</td>
<td>Push</td>
<td>Fazer um envio por push
<ul>
<li>Em caso de sucesso, vá para WP</li>
<li>Em caso de falha, vá para o fim</li>
</ul>
Para falhar: Vá para um<br/></td>
</tr>
<tr class="odd">
<td>WP</td>
<td>Aguardar envio por push</td>
<td>Aguardar notificação
<ul>
<li>Em caso de falha ao obter uma conclusão, vá para um</li>
<li>Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de sucesso for recebido e mais dados precisarem ser enviados, vá para P</li>
<li>Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de sucesso for recebido e mais dados não precisarem ser enviados, vá para NP</li>
<li>Se uma falha for recebida, go comp</li>
</ul>
Para falhar: Vá para um<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>Envio por push nulo</td>
<td>Enviar 0 bytes por push
<ul>
<li>em caso de sucesso, vá para o WNP</li>
<li>em caso de falha, vá para comp</li>
</ul>
Para falhar: Vá para um<br/></td>
</tr>
<tr class="odd">
<td>WNP</td>
<td>Aguardar envio por push nulo</td>
<td>Aguardar notificação
<ul>
<li>Em caso de falha ao obter uma conclusão, vá para um</li>
<li>Se uma falha for recebida, go comp</li>
<li>Se um sucesso for recebido, acesse comp</li>
</ul></td>
</tr>
<tr class="even">
<td>Um</td>
<td>Anular a chamada</td>
<td>Chamar <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; ir para o fim</td>
</tr>
<tr class="odd">
<td>Às</td>
<td>Completion</td>
<td>Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; ir para o fim</td>
</tr>
<tr class="even">
<td>End</td>


</tr>
</tbody>
</table>



 

## <a name="in-out-pipe"></a>Pipe de saída

Comportamento do cliente

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Estado</th>
<th>Nome do Estado</th>
<th>Ação</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>Faça a chamada</td>
<td>Tornar o RPC
<ul>
<li>Em caso de sucesso, vá para WS</li>
<li>Na exceção, vá para o fim</li>
</ul>
Para falhar: Vá para pode<br/></td>
</tr>
<tr class="even">
<td>PS</td>
<td>Push</td>
<td>Fazer um envio por push
<ul>
<li>Em caso de falha, vá para o fim</li>
<li>Em caso de sucesso, vá para WS</li>
</ul>
Para falhar: Vá para pode<br/></td>
</tr>
<tr class="odd">
<td>WS</td>
<td>Aguardar envio</td>
<td>Aguardar notificação
<ul>
<li>Em caso de falha ao obter uma notificação, acesse pode</li>
<li>Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de sucesso for recebido e mais dados precisarem ser enviados, vá para PS</li>
<li>Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de sucesso for recebido e mais dados não precisarem ser enviados, vá para NP</li>
<li>Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> de falha for recebida, acesse comp</li>
</ul>
Para falhar: Vá para pode<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>Envio por push nulo</td>
<td>Enviar 0 bytes por push (Push nulo)
<ul>
<li>Em caso de falha, vá para o fim</li>
<li>Em caso de sucesso, vá para PL</li>
</ul>
Para falhar: Vá para pode<br/></td>
</tr>
<tr class="odd">
<td>PL</td>
<td>Recepção</td>
<td>Fazer um pull
<ul>
<li>Em caso de falha, vá para o fim</li>
<li>Em caso de êxito e conclusão síncrona com bytes diferentes de zero lidos, acesse PL</li>
<li>Em caso de êxito e conclusão síncrona com zero bytes lidos (pull nulo), vá para WComp</li>
<li>Em caso de êxito e conclusão assíncrona (ERROR_IO_PENDING é retornado), vá para WPL</li>
</ul>
Para falhar: Vá para pode<br/></td>
</tr>
<tr class="even">
<td>WPL</td>
<td>Aguardar pull</td>
<td>Aguardar notificação
<ul>
<li>Em caso de falha ao obter uma conclusão, vá para pode</li>
<li>Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de falha for recebida, vá para Can</li>
<li>Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de sucesso for recebida com bytes diferentes de zero, leia ir para pl</li>
<li>Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de sucesso for recebida com zero bytes lido, vá para comp</li>
<li>Se uma falha for recebida, vá pode</li>
</ul>
Para falhar: Vá para pode<br/></td>
</tr>
<tr class="odd">
<td>Podem</td>
<td>Cancelar a chamada</td>
<td>Chame <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>go to WComp<br/></td>
</tr>
<tr class="even">
<td>WComp</td>
<td>Aguardar a conclusão</td>
<td>Aguarde a notificação. A notificação de CallComplete deve ser recebida.<br/> Ir para comp<br/></td>
</tr>
<tr class="odd">
<td>Às</td>
<td>Completion</td>
<td>Emitir <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>ir para o fim<br/></td>
</tr>
<tr class="even">
<td>End</td>


</tr>
</tbody>
</table>



 

Comportamento do servidor

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Estado</th>
<th>Nome do Estado</th>
<th>Ação</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D</td>
<td>Dispatch</td>
<td>A chamada é expedida pelo RPC runtimeGo para PL<br/> Para falhar fatalmente (ao executar no thread RPC): gerar exceção; ir para o fim<br/> Para falhar normalmente: Vá para um<br/></td>
</tr>
<tr class="even">
<td>PL</td>
<td>Recepção</td>
<td>Fazer um pull
<ul>
<li>Em caso de falha, vá para o fim</li>
<li>Em caso de êxito e conclusão síncrona com bytes diferentes de zero lidos, acesse PL</li>
<li>Em caso de êxito e conclusão síncrona com zero bytes lidos (pull nulo), vá para PS</li>
<li>Em caso de êxito e conclusão assíncrona (ERROR_IO_PENDING é retornado), vá para WPL</li>
</ul>
Para falhar: Vá para um<br/></td>
</tr>
<tr class="odd">
<td>WPL</td>
<td>Aguardar pull</td>
<td>Aguardar notificação
<ul>
<li>Em caso de falha ao obter uma conclusão, vá para um</li>
<li>Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de falha for recebido, vá para um</li>
<li>Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de sucesso for recebida com bytes diferentes de zero, leia ir para pl</li>
<li>Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de sucesso for recebida com zero bytes lido, vá para PS</li>
<li>Se uma falha for recebida, vá para</li>
</ul>
Para falhar: Vá para um<br/></td>
</tr>
<tr class="even">
<td>PS</td>
<td>Push</td>
<td>Fazer um envio por push
<ul>
<li>Em caso de sucesso, vá para WPS</li>
<li>Em caso de falha, vá para o fim</li>
</ul>
Para falhar: Vá para um<br/></td>
</tr>
<tr class="odd">
<td>WPS</td>
<td>Aguardar envio por push</td>
<td>Aguardar notificação
<ul>
<li>Em caso de falha ao obter uma conclusão, vá para um</li>
<li>Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de sucesso for recebido e mais dados precisarem ser enviados, vá para PS</li>
<li>Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de sucesso for recebido e mais dados não precisarem ser enviados, vá para NP</li>
<li>Se uma falha for recebida, go comp</li>
</ul>
Para falhar: Vá para um<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>Envio por push nulo</td>
<td>Enviar 0 bytes por push
<ul>
<li>em caso de sucesso, vá para o WNP</li>
<li>em caso de falha, vá para comp</li>
</ul>
Para falhar: Vá para um<br/></td>
</tr>
<tr class="odd">
<td>WNP</td>
<td>Aguardar envio por push nulo</td>
<td>Aguardar notificação
<ul>
<li>Em caso de falha ao obter uma conclusão, vá para um</li>
<li>Se uma falha for recebida, go comp</li>
<li>Se um sucesso for recebido, acesse comp</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Um</td>
<td>Anular a chamada</td>
<td>Chamar <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; ir para o fim</td>
</tr>
<tr class="odd">
<td>Às</td>
<td>Completion</td>
<td>Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; ir para o fim</td>
</tr>
<tr class="even">
<td>End</td>


</tr>
</tbody>
</table>



 

 

 





