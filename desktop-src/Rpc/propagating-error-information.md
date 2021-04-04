---
title: Propagando informações de erro
description: A propagação de informações de erro estendidas permite que os servidores que recebem um \_ erro RPC S \_ ou qualquer outro código de erro, para permitir que o tempo de execução de RPC propaguem as informações recebidas para seus chamadores.
ms.assetid: f0395f19-ceb1-4249-892e-9b688464d0d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd20575cee304c0a1693ae4bc6442de4837caa0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822894"
---
# <a name="propagating-error-information"></a><span data-ttu-id="be048-103">Propagando informações de erro</span><span class="sxs-lookup"><span data-stu-id="be048-103">Propagating Error Information</span></span>

<span data-ttu-id="be048-104">A propagação de informações de erro estendidas permite que os servidores que recebem um erro de RPC \_ S \_ \* ou qualquer outro código de erro, para permitir que o tempo de execução de RPC propaguem as informações recebidas para seus chamadores.</span><span class="sxs-lookup"><span data-stu-id="be048-104">Propagating extended error information allows servers that receive an RPC\_S\_\* error, or any other error code for that matter, to allow the RPC run time to propagate the information it received to its callers.</span></span> <span data-ttu-id="be048-105">Tudo o que o servidor deve fazer é chamar [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) ou [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) após encontrar um erro fatal.</span><span class="sxs-lookup"><span data-stu-id="be048-105">All the server must do is call the [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) or [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) upon encountering a fatal error.</span></span> <span data-ttu-id="be048-106">O tempo de execução do RPC se encarrega de encadear as informações de erro estendidas, se houver, fazendo com que o erro fatal relate o erro fatal em si, desde que o código de erro fornecido a **RpcRaiseException** ou **RpcAsyncAbortCall** seja o mesmo que o código de erro causando o erro fatal.</span><span class="sxs-lookup"><span data-stu-id="be048-106">The RPC run time takes care of chaining the extended error information, if any, causing the fatal error to report the fatal error itself, as long as the error code given to **RpcRaiseException** or **RpcAsyncAbortCall** is the same as the error code causing the fatal error.</span></span>

 

 




