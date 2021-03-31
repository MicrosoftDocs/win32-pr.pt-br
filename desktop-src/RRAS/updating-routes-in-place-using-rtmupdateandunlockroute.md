---
title: Atualizando rotas no local usando RtmUpdateAndUnlockRoute
description: A atualização in-loco geralmente é mais eficiente do que atualizar a tabela de roteamento com um método indireto, como o usado pela função RtmAddRouteToDest.
ms.assetid: d4b0b14e-957a-43d5-bacc-8eee4512e2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d76d2af5d60172b890eefa1041a08d47a5221b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005677"
---
# <a name="updating-routes-in-place-using-rtmupdateandunlockroute"></a><span data-ttu-id="d38e7-103">Atualizando rotas no local usando RtmUpdateAndUnlockRoute</span><span class="sxs-lookup"><span data-stu-id="d38e7-103">Updating Routes In Place Using RtmUpdateAndUnlockRoute</span></span>

<span data-ttu-id="d38e7-104">A atualização in-loco geralmente é mais eficiente do que atualizar a tabela de roteamento com um método indireto, como o usado pela função [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) .</span><span class="sxs-lookup"><span data-stu-id="d38e7-104">Updating in place is generally more efficient than updating the routing table with an indirect method such as that used by the [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) function.</span></span> <span data-ttu-id="d38e7-105">Esse método é mais eficiente, pois o cliente não precisa obter um identificador nem passar a estrutura de [**informações da \_ rota \_ RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) de e para o Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="d38e7-105">This method is more efficient because the client is not required to obtain a handle, nor to pass the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure to and from the routing table manager.</span></span> <span data-ttu-id="d38e7-106">Esse método também leva menos tempo.</span><span class="sxs-lookup"><span data-stu-id="d38e7-106">This method also takes less time.</span></span> <span data-ttu-id="d38e7-107">No entanto, a atualização direta da tabela de roteamento pode ser arriscada, pois o Gerenciador da tabela de roteamento não está funcionando como um intermediário.</span><span class="sxs-lookup"><span data-stu-id="d38e7-107">However, directly updating the routing table can be risky, since the routing table manager is not functioning as an intermediary.</span></span>

<span data-ttu-id="d38e7-108">Para obter um exemplo de código que mostra como usar essas funções, consulte [atualizar uma rota no local usando RtmUpdateAndUnlockRoute](update-a-route-in-place-using-rtmupdateandunlockroute.md).</span><span class="sxs-lookup"><span data-stu-id="d38e7-108">For sample code that shows how to use these functions, see [Update a Route In Place Using RtmUpdateAndUnlockRoute](update-a-route-in-place-using-rtmupdateandunlockroute.md).</span></span>

 

 




