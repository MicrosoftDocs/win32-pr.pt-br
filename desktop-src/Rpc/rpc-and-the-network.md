---
title: RPC e a rede
description: Esta seção discute como lidar com a não confiabilidade de rede ao usar o RPC e explica como as APIs de nível de RPC se convertem em atividade de rede. A seção refere-se somente às \_ \_ sequências de protocolo http TCP e ncacn de IP ncacn \_ .
ms.assetid: af7c67ea-32af-40b0-b74b-0a339e5088c4
keywords:
- RPC de chamada de procedimento remoto, práticas recomendadas, RPC e rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c0373bb81d9da0bf20eed1fb9f80863604b040
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084771"
---
# <a name="rpc-and-the-network"></a><span data-ttu-id="c137d-105">RPC e a rede</span><span class="sxs-lookup"><span data-stu-id="c137d-105">RPC and the Network</span></span>

<span data-ttu-id="c137d-106">Esta seção discute como lidar com a não confiabilidade de rede ao usar o RPC e explica como as APIs de nível de RPC se convertem em atividade de rede.</span><span class="sxs-lookup"><span data-stu-id="c137d-106">This section discusses how to deal with network unreliability when using RPC, and explains how RPC-level APIs translate into network activity.</span></span> <span data-ttu-id="c137d-107">A seção refere-se somente às sequências de [**protocolo \_ http**](/windows/desktop/Midl/ncacn-http) TCP e ncacn de [**\_ \_ IP ncacn**](/windows/desktop/Midl/ncacn-ip-tcp) .</span><span class="sxs-lookup"><span data-stu-id="c137d-107">The section refers only to the [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp) and [**ncacn\_http**](/windows/desktop/Midl/ncacn-http) protocol sequences.</span></span>

<span data-ttu-id="c137d-108">Esta seção é dividida nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="c137d-108">This section is divided into the following topics:</span></span>

-   [<span data-ttu-id="c137d-109">Desenvolvimento versus implantação na rede</span><span class="sxs-lookup"><span data-stu-id="c137d-109">Development Versus Deployment in the Network</span></span>](development-versus-deployment-in-the-network.md)
-   [<span data-ttu-id="c137d-110">Evitar travamentos de Client-Side</span><span class="sxs-lookup"><span data-stu-id="c137d-110">Preventing Client-Side Hangs</span></span>](preventing-client-side-hangs.md)
-   [<span data-ttu-id="c137d-111">Gerenciando conjuntos de conexões de rede (associações)</span><span class="sxs-lookup"><span data-stu-id="c137d-111">Managing Network Connection Sets (Associations)</span></span>](managing-network-connection-sets-associations-.md)
-   [<span data-ttu-id="c137d-112">Limpeza de conexão ociosa</span><span class="sxs-lookup"><span data-stu-id="c137d-112">Idle Connection Cleanup</span></span>](idle-connection-cleanup.md)
-   [<span data-ttu-id="c137d-113">Lidando com a perda de conectividade</span><span class="sxs-lookup"><span data-stu-id="c137d-113">Dealing with Loss of Connectivity</span></span>](dealing-with-loss-of-connectivity.md)
-   [<span data-ttu-id="c137d-114">Limpeza do lado do servidor</span><span class="sxs-lookup"><span data-stu-id="c137d-114">Server Side Cleanup</span></span>](server-side-cleanup.md)

 

 