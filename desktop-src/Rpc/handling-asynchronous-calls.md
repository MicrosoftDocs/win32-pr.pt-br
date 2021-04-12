---
title: Manipulando chamadas assíncronas
description: A rotina Manager de uma função assíncrona sempre recebe o identificador assíncrono como o primeiro parâmetro. O servidor deve manter o controle desse identificador e usá-lo para enviar a resposta quando a chamada de procedimento remoto assíncrona for concluída.
ms.assetid: 4f38b68b-0bea-4fa7-8c7e-dd09e7daf8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e04dc7feed0d7bee47f6fa51583cf8de3a8e42f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364111"
---
# <a name="handling-asynchronous-calls"></a><span data-ttu-id="c5902-104">Manipulando chamadas assíncronas</span><span class="sxs-lookup"><span data-stu-id="c5902-104">Handling Asynchronous Calls</span></span>

<span data-ttu-id="c5902-105">A rotina Manager de uma função assíncrona sempre recebe o identificador assíncrono como o primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c5902-105">The manager routine of an asynchronous function always receives the asynchronous handle as the first parameter.</span></span> <span data-ttu-id="c5902-106">O servidor deve manter o controle desse identificador e usá-lo para enviar a resposta quando a chamada de procedimento remoto assíncrona for concluída.</span><span class="sxs-lookup"><span data-stu-id="c5902-106">The server must keep track of this handle and use it to send the reply when the asynchronous remote procedure call finishes.</span></span>

<span data-ttu-id="c5902-107">Se o servidor precisar anular um RPC assíncrono, ele chamará [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall).</span><span class="sxs-lookup"><span data-stu-id="c5902-107">If the server needs to abort an asynchronous RPC, it calls [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall).</span></span> <span data-ttu-id="c5902-108">Essa função executa a mesma limpeza do lado do servidor como [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) e propaga um código de exceção (fornecido pelo aplicativo de servidor) de volta para o cliente, exceto que ele não executa o marshaling dos argumentos de saída.</span><span class="sxs-lookup"><span data-stu-id="c5902-108">This function performs the same server-side cleanup as [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) and propagates an exception code (provided by the server application) back to the client, except that it does not perform marshalling of the out arguments.</span></span>

<span data-ttu-id="c5902-109">Para obter um exemplo de um procedimento assíncrono, consulte [enviando a resposta assíncrona](sending-the-asynchronous-reply.md).</span><span class="sxs-lookup"><span data-stu-id="c5902-109">For an example of an asynchronous procedure, see [Sending the Asynchronous Reply](sending-the-asynchronous-reply.md).</span></span>

 

 




