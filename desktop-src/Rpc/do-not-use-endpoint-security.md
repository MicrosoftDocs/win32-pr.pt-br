---
title: Não usar a segurança do ponto de extremidade
description: O Endpoint Security é um modelo de segurança no qual um descritor de segurança é fornecido quando um ponto de extremidade é criado com o grupo RpcServerUseProtseq \ de funções RPC.
ms.assetid: 5b8841c4-5b65-417f-b790-e8c2dabb44a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289513810ba7e67e0da625151c3c2975e0eaaf99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635722"
---
# <a name="do-not-use-endpoint-security"></a><span data-ttu-id="18ce7-103">Não usar a segurança do ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="18ce7-103">Do Not Use Endpoint Security</span></span>

<span data-ttu-id="18ce7-104">O Endpoint Security é um modelo de segurança no qual um descritor de segurança é fornecido quando um ponto de extremidade é criado com o grupo [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) \* de funções RPC.</span><span class="sxs-lookup"><span data-stu-id="18ce7-104">Endpoint security is a security model in which a security descriptor is given when an endpoint is created with the [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq)\* group of RPC functions.</span></span> <span data-ttu-id="18ce7-105">Não use esse modelo de segurança.</span><span class="sxs-lookup"><span data-stu-id="18ce7-105">Do not use this security model.</span></span> <span data-ttu-id="18ce7-106">Não forneça descritores de segurança para essas funções.</span><span class="sxs-lookup"><span data-stu-id="18ce7-106">Do not give security descriptors to those functions.</span></span> <span data-ttu-id="18ce7-107">Na melhor das hipóteses, esse método é um desperdício de recursos de CPU.</span><span class="sxs-lookup"><span data-stu-id="18ce7-107">At best, this method is a waste of CPU resources.</span></span> <span data-ttu-id="18ce7-108">Na pior das hipóteses, em muitos ambientes, é possível burlar o descritor de segurança, pois deve [ser cauteloso com outros pontos de extremidade RPC em execução na mesma](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md) seção de processo exemplifica.</span><span class="sxs-lookup"><span data-stu-id="18ce7-108">At worst, in many environments it is possible to circumvent the security descriptor, as the [Be Wary of Other RPC Endpoints Running In the Same Process](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md) section exemplifies.</span></span>

<span data-ttu-id="18ce7-109">A segurança do ponto de extremidade existe somente para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="18ce7-109">Endpoint security exists only for backward compatibility.</span></span>

 

 




