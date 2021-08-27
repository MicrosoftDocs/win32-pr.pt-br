---
title: Estado de pipe assíncrono
description: Esta página descreve o estado de pipe assíncrono para chamadas RPC.
ms.assetid: af937eba-6b70-447a-af76-a8e27f5754e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a35e54d9f86228cb4c957f53411c105e20e2109
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468163"
---
# <a name="asynchronous-pipe-state"></a>Estado de pipe assíncrono

Esta página descreve o estado de pipe assíncrono para chamadas RPC.

## <a name="in-pipe"></a>NO pipe

Comportamento do cliente


| Estado | Nome do Estado | Ação | 
|-------|------------|--------|
| C | Faça a chamada | Tornar o RPC<ul><li>Em ir para o estado de êxito WS</li><li>Na exceção, vá para o fim</li></ul>Para falhar: Vá para pode<br /> | 
| P | Push | Fazer um envio por push<ul><li>Em caso de falha, vá para o fim</li><li>Em caso de sucesso, vá para WS</li></ul>Para falhar: Vá para pode<br /> | 
| WS | Aguardar envio | Aguardar notificação<ul><li>Em caso de falha ao obter uma notificação, acesse pode</li><li>Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de sucesso for recebido e mais dados precisarem ser enviados, vá para P</li><li>Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de sucesso for recebido e mais dados não precisarem ser enviados, vá para NP</li><li>Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> de falha for recebida, acesse comp</li></ul>Para falhar: Vá para pode<br /> | 
| NP | Envio por push nulo | Enviar 0 bytes por push (Push nulo)<ul><li>Em caso de falha, vá para o fim</li><li>Em caso de sucesso, vá para WComp</li></ul>Para falhar: Vá para pode<br /> | 
| Podem | Cancelar a chamada | Chame <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>go to WComp<br /> | 
| WComp | Aguardar a conclusão | Aguarde até que a notificação de notificationCall seja recebida.<br /> Ir para comp<br /> | 
| Às | Completion | Emitir <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>ir para o fim<br /> | 
| End | 




 

Comportamento do servidor


| Estado | Nome do Estado | Ação | 
|-------|------------|--------|
| D | Dispatch | A chamada é expedida pelo tempo de execução RPC, vá para P<br /> Para falhar fatalmente (ao executar no thread RPC): gerar exceção; ir para o fim<br /> Para falhar normalmente: Vá para um<br /> | 
| P | Recepção | Fazer um pull<ul><li>Em caso de falha, vá para o fim</li><li>Em caso de êxito e conclusão síncrona com bytes diferentes de zero lidos, vá para P</li><li>Em caso de êxito e conclusão síncrona com zero bytes lidos (pull nulo), vá para comp</li><li>Em caso de êxito e conclusão assíncrona (ERROR_IO_PENDING é retornado), vá para WP</li></ul>Para falhar: Vá para um<br /> | 
| WP | Aguardar pull | Aguardar notificação<ul><li>Em caso de falha ao obter uma conclusão, vá para um</li><li>Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de falha for recebido, vá para um</li><li>Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de sucesso for recebida com bytes diferentes de zero, leia ir para P</li><li>Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de sucesso for recebida com zero bytes lidos (pull nulo), vá para comp</li><li>Se uma falha for recebida, vá para um</li></ul>Para falhar: Vá para um<br /> | 
| A | Anular a chamada | Chamar <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>ir para o fim<br /> | 
| Às | Completion | Chamar <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>ir para o fim<br /> | 
| End | 




 

## <a name="out-pipe"></a>SAÍDA de pipe

Comportamento do cliente


| Estado | Nome do Estado | Ação | 
|-------|------------|--------|
| C | Faça a chamada | Tornar o RPC<ul><li>Em caso de sucesso, vá para P</li><li>Em caso de falha, vá para comp</li></ul>Para falhar: Vá para pode<br /> | 
| P | Recepção | Fazer um pull<ul><li>Em caso de falha, vá para o fim</li><li>Em caso de êxito e conclusão síncrona com bytes diferentes de zero lidos, vá para P</li><li>Em caso de êxito e conclusão síncrona com zero bytes lidos (pull nulo), vá para WComp</li><li>Em caso de êxito e conclusão assíncrona (ERROR_IO_PENDING é retornado), vá para WP</li></ul>Para falhar: Vá para pode<br /> | 
| WP | Aguardar pull | Aguardar a notificação<ul><li>Em caso de falha ao obter uma conclusão, acesse Pode</li><li>Se uma falha <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> for recebida, acesse Pode</li><li>Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> bem-sucedido for recebido com bytes não zero lidos, vá para P</li><li>Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> bem-sucedido for recebido com zero bytes lidos (pull nulo) vá para Comp</li><li>Se uma falha for recebida, acesse Pode</li></ul>Para falhar: acesse Pode<br /> | 
| Cna | Cancelar a chamada | Chamar <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go para WComp<br /> | 
| WComp | Aguardar a conclusão | Aguarde a notificação. A notificação de conclusão da chamada deve ser recebida.<br /> Vá para Comp<br /> | 
| Comp | Completion | Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End<br /> | 
| End | 




 

Comportamento do servidor


| Estado | Nome do Estado | Ação | 
|-------|------------|--------|
| D | Dispatch | A chamada é expedida pelo runtime RPC Ir para P<br /> Para falhar fatalmente (durante a execução no thread RPC): aumentar exceção; ir para Fim<br /> Para falhar normalmente: vá para A<br /> | 
| P | Push | Fazer um push<ul><li>Em caso de êxito, acesse WP</li><li>Em caso de falha, vá para Fim</li></ul>Para falhar: vá para A<br /> | 
| WP | Aguardar push | Aguardar a notificação<ul><li>Em caso de falha ao obter uma conclusão, vá para A</li><li>Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete bem-sucedido</strong></a> for recebido e mais dados precisarem ser enviados, vá para P</li><li>Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete bem-sucedido</strong></a> for recebido e mais dados não precisarem ser enviados, vá para NP</li><li>Se uma falha for recebida, acesse Comp</li></ul>Para falhar: vá para A<br /> | 
| NP | Push nulo | Push 0 bytes<ul><li>em caso de sucesso, vá para WNP</li><li>em caso de falha, vá para Comp</li></ul>Para falhar: vá para A<br /> | 
| WNP | Aguardar push nulo | Aguardar a notificação<ul><li>Em caso de falha ao obter uma conclusão, vá para A</li><li>Se uma falha for recebida, acesse Comp</li><li>Se um sucesso for recebido, acesse Comp</li></ul> | 
| A | Anular a chamada | Chame <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; ir para Fim | 
| Comp | Completion | Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; ir para Fim | 
| End | 




 

## <a name="in-out-pipe"></a>IN-OUT Pipe

Comportamento do cliente


| Estado | Nome do Estado | Ação | 
|-------|------------|--------|
| C | Fazer a chamada | Tornar o RPC<ul><li>Em caso de sucesso, vá para WS</li><li>Na exceção, vá para Fim</li></ul>Para falhar: acesse Pode<br /> | 
| PS | Push | Fazer um push<ul><li>Em caso de falha, vá para Fim</li><li>Em caso de sucesso, vá para WS</li></ul>Para falhar: acesse Pode<br /> | 
| WS | Aguardar o envio | Aguardar a notificação<ul><li>Em caso de falha ao receber uma notificação, acesse Pode</li><li>Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete bem-sucedido</strong></a> for recebido e mais dados precisarem ser enviados, vá para PS</li><li>Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete bem-sucedido</strong></a> for recebido e mais dados não precisarem ser enviados, vá para NP</li><li>Se uma falha <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> for recebida, acesse Comp</li></ul>Para falhar: acesse Pode<br /> | 
| NP | Push nulo | Push 0 bytes (push nulo)<ul><li>Em caso de falha, vá para Fim</li><li>Em caso de sucesso, acesse PL</li></ul>Para falhar: acesse Pode<br /> | 
| PL | Recepção | Fazer um pull<ul><li>Em caso de falha, vá para Fim</li><li>Em caso de êxito e conclusão síncrona com bytes não zero lidos, acesse PL</li><li>Em caso de êxito e conclusão síncrona com zero bytes lidos (pull nulo) vá para WComp</li><li>Em caso de êxito e conclusão assíncrona (ERROR_IO_PENDING retornado) vá para WPL</li></ul>Para falhar: acesse Pode<br /> | 
| WPL | Aguardar pull | Aguardar notificação<ul><li>Em caso de falha ao obter uma conclusão, vá para pode</li><li>Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de falha for recebida, vá para Can</li><li>Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de sucesso for recebida com bytes diferentes de zero, leia ir para pl</li><li>Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de sucesso for recebida com zero bytes lido, vá para comp</li><li>Se uma falha for recebida, vá pode</li></ul>Para falhar: Vá para pode<br /> | 
| Podem | Cancelar a chamada | Chame <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>go to WComp<br /> | 
| WComp | Aguardar a conclusão | Aguarde a notificação. A notificação de CallComplete deve ser recebida.<br /> Ir para comp<br /> | 
| Às | Completion | Emitir <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>ir para o fim<br /> | 
| End | 




 

Comportamento do servidor


| Estado | Nome do Estado | Ação | 
|-------|------------|--------|
| D | Dispatch | A chamada é expedida pelo RPC runtimeGo para PL<br /> Para falhar fatalmente (ao executar no thread RPC): gerar exceção; ir para o fim<br /> Para falhar normalmente: Vá para um<br /> | 
| PL | Recepção | Fazer um pull<ul><li>Em caso de falha, vá para o fim</li><li>Em caso de êxito e conclusão síncrona com bytes diferentes de zero lidos, acesse PL</li><li>Em caso de êxito e conclusão síncrona com zero bytes lidos (pull nulo), vá para PS</li><li>Em caso de êxito e conclusão assíncrona (ERROR_IO_PENDING é retornado), vá para WPL</li></ul>Para falhar: Vá para um<br /> | 
| WPL | Aguardar pull | Aguardar notificação<ul><li>Em caso de falha ao obter uma conclusão, vá para um</li><li>Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de falha for recebido, vá para um</li><li>Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de sucesso for recebida com bytes diferentes de zero, leia ir para pl</li><li>Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de sucesso for recebida com zero bytes lido, vá para PS</li><li>Se uma falha for recebida, vá para</li></ul>Para falhar: Vá para um<br /> | 
| PS | Push | Fazer um envio por push<ul><li>Em caso de sucesso, vá para WPS</li><li>Em caso de falha, vá para o fim</li></ul>Para falhar: Vá para um<br /> | 
| WPS | Aguardar envio por push | Aguardar notificação<ul><li>Em caso de falha ao obter uma conclusão, vá para um</li><li>Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de sucesso for recebido e mais dados precisarem ser enviados, vá para PS</li><li>Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de sucesso for recebido e mais dados não precisarem ser enviados, vá para NP</li><li>Se uma falha for recebida, go comp</li></ul>Para falhar: Vá para um<br /> | 
| NP | Envio por push nulo | Enviar 0 bytes por push<ul><li>em caso de sucesso, vá para o WNP</li><li>em caso de falha, vá para comp</li></ul>Para falhar: Vá para um<br /> | 
| WNP | Aguardar envio por push nulo | Aguardar notificação<ul><li>Em caso de falha ao obter uma conclusão, vá para um</li><li>Se uma falha for recebida, go comp</li><li>Se um sucesso for recebido, acesse comp</li></ul><br /> | 
| A | Anular a chamada | Chamar <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; ir para o fim | 
| Às | Completion | Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; ir para o fim | 
| End | 




 

 

 





