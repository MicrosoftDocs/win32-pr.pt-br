---
title: Recebendo a resposta assíncrona
description: Depois de ser notificado de que o servidor enviou uma resposta, o cliente chama RpcAsyncCompleteCall com o identificador assíncrono para que ele possa receber a resposta.
ms.assetid: 48fb3777-d90a-474b-a1fa-9d034b5791e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9143daaf1f276f784086e2ec17efb47dfd1fb6e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366590"
---
# <a name="receiving-the-asynchronous-reply"></a><span data-ttu-id="4afda-103">Recebendo a resposta assíncrona</span><span class="sxs-lookup"><span data-stu-id="4afda-103">Receiving the Asynchronous Reply</span></span>

<span data-ttu-id="4afda-104">Depois de ser notificado de que o servidor enviou uma resposta, o cliente chama [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) com o identificador assíncrono para que ele possa receber a resposta.</span><span class="sxs-lookup"><span data-stu-id="4afda-104">After it is notified that the server has sent a reply, the client calls [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) with the asynchronous handle so that it can receive the reply.</span></span> <span data-ttu-id="4afda-105">Quando **RpcAsyncCompleteCall** for concluído com êxito, o parâmetro de *resposta* apontará para um buffer que contém o valor de retorno da função remota.</span><span class="sxs-lookup"><span data-stu-id="4afda-105">When **RpcAsyncCompleteCall** has completed successfully, the *Reply* parameter points to a buffer that contains the return value of the remote function.</span></span> <span data-ttu-id="4afda-106">Todos os buffers fornecidos pelo programa cliente como \[ [**out**](/windows/desktop/Midl/out-idl) \] ou \[ [**in**](/windows/desktop/Midl/in), parâmetros de **saída** \] para a função remota assíncrona contêm dados válidos.</span><span class="sxs-lookup"><span data-stu-id="4afda-106">Any buffers supplied by the client program as \[[**out**](/windows/desktop/Midl/out-idl)\] or \[[**in**](/windows/desktop/Midl/in), **out**\] parameters to the asynchronous remote function contain valid data.</span></span> <span data-ttu-id="4afda-107">Se o cliente chamar **RpcAsyncCompleteCall** antes que o servidor tenha enviado a resposta, essa chamada falhará e retornará um valor de \_ chamada de RPC S \_ Async \_ \_ pendente.</span><span class="sxs-lookup"><span data-stu-id="4afda-107">If the client calls **RpcAsyncCompleteCall** before the server has sent the reply, that call will fail and return a value of RPC\_S\_ASYNC\_CALL\_PENDING.</span></span>

<span data-ttu-id="4afda-108">Se o programa cliente usar portas de conclusão de e/s ou eventos para notificação, ele deverá chamar [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) para liberar a porta ou o identificador quando ele não precisar mais delas.</span><span class="sxs-lookup"><span data-stu-id="4afda-108">If your client program uses I/O completion ports or events for notification, it must call [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) to release the port or handle when it no longer needs them.</span></span>

 

 