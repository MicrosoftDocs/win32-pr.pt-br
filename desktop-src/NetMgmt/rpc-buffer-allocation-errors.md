---
title: Erros de alocação de buffer RPC
description: Como a biblioteca de tempo de execução RPC aloca memória para buffers de envio e recebimento, a função deve esperar erros de alocação RPC.
ms.assetid: be9105df-1183-48d6-8cea-391ca628c8b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbe48c113d644447b5ff7b69988f2534d7de3a9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292152"
---
# <a name="rpc-buffer-allocation-errors"></a><span data-ttu-id="8b716-103">Erros de alocação de buffer RPC</span><span class="sxs-lookup"><span data-stu-id="8b716-103">RPC Buffer Allocation Errors</span></span>

<span data-ttu-id="8b716-104">Como a biblioteca de tempo de execução RPC aloca memória para buffers de envio e recebimento, a função deve esperar erros de alocação RPC.</span><span class="sxs-lookup"><span data-stu-id="8b716-104">Because the RPC run-time library allocates memory for send and receive buffers, the function should expect RPC allocation errors.</span></span> <span data-ttu-id="8b716-105">No caso de um erro de alocação de RPC, um identificador retomável é invalidado.</span><span class="sxs-lookup"><span data-stu-id="8b716-105">In the event of an RPC allocation error, a resumable handle is invalidated.</span></span> <span data-ttu-id="8b716-106">Esse é um requisito porque as funções retomáveis não são rebobinadas.</span><span class="sxs-lookup"><span data-stu-id="8b716-106">This is a requirement because resumable functions are not rewindable.</span></span>

 

 




