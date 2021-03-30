---
title: Marcando rotas para o estado de Hold-Down
description: Alguns clientes, como protocolos de vetor de distância, como RIP e DVMRP, exigem que os destinos sejam anunciados como inacessíveis por um determinado tempo após a última rota para o destino ser excluída.
ms.assetid: 2a86c092-d8a6-4fd4-8b2e-451c160f743f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af10832452a3a0b9ca851c209d240c97998ef519
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916365"
---
# <a name="marking-routes-for-the-hold-down-state"></a><span data-ttu-id="d49f6-103">Marcando rotas para o estado de Hold-Down</span><span class="sxs-lookup"><span data-stu-id="d49f6-103">Marking Routes for the Hold-Down State</span></span>

<span data-ttu-id="d49f6-104">Alguns clientes, como protocolos de vetor de distância, como RIP e DVMRP, exigem que os destinos sejam anunciados como inacessíveis por um determinado tempo após a última rota para o destino ser excluída.</span><span class="sxs-lookup"><span data-stu-id="d49f6-104">Some clients, such as distance vector protocols like RIP and DVMRP, require that destinations be advertised as unreachable for a certain time after the last route to the destination is deleted.</span></span> <span data-ttu-id="d49f6-105">A última rota que é excluída deve ser anunciada como inacessível, mesmo que as rotas mais novas cheguem enquanto isso.</span><span class="sxs-lookup"><span data-stu-id="d49f6-105">The last route that is deleted must be advertised as unreachable even if newer routes arrive in the meantime.</span></span> <span data-ttu-id="d49f6-106">A última rota excluída está marcada como estando em um *estado de espera*.</span><span class="sxs-lookup"><span data-stu-id="d49f6-106">The last route deleted is marked as being in a *hold-down state*.</span></span> <span data-ttu-id="d49f6-107">O processo de suspensão impede a formação de loops de roteamento.</span><span class="sxs-lookup"><span data-stu-id="d49f6-107">The hold-down process prevents the formation of routing loops.</span></span> <span data-ttu-id="d49f6-108">Os loops de roteamento são causados quando um protocolo de roteamento anuncia informações de roteamento obsoletas.</span><span class="sxs-lookup"><span data-stu-id="d49f6-108">Routing loops are caused when a routing protocol advertises obsolete routing information.</span></span> <span data-ttu-id="d49f6-109">Quando a suspensão expira, esses protocolos retomam seu anúncio com a nova rota recomendada.</span><span class="sxs-lookup"><span data-stu-id="d49f6-109">When the hold-down expires, these protocols resume their advertisement with the new best route.</span></span>

<span data-ttu-id="d49f6-110">Um protocolo que implementa os Estados de espera indica que um destino está em um estado suspenso usando a função [**RtmHoldDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination) .</span><span class="sxs-lookup"><span data-stu-id="d49f6-110">A protocol that implements hold-down states indicates that a destination is in a hold-down state by using the [**RtmHoldDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination) function.</span></span> <span data-ttu-id="d49f6-111">O cliente chama essa função quando anuncia a melhor rota para esse destino.</span><span class="sxs-lookup"><span data-stu-id="d49f6-111">The client calls this function when it advertises the best route to this destination.</span></span> <span data-ttu-id="d49f6-112">Se todas as rotas para esse destino forem excluídas posteriormente, a última rota excluída será mantida em um estado de espera para o período de tempo especificado na chamada anterior para **RtmHoldDestination**.</span><span class="sxs-lookup"><span data-stu-id="d49f6-112">If all routes to this destination are later deleted, the last route that is deleted is kept in a hold-down state for the period of time specified in the earlier call to **RtmHoldDestination**.</span></span>

<span data-ttu-id="d49f6-113">Quando um protocolo anuncia um destino, as informações de rota que são usadas dependem de o protocolo usar os Estados suspensos e se uma rota no estado suspenso existe para o destino.</span><span class="sxs-lookup"><span data-stu-id="d49f6-113">When a protocol advertises a destination, the route information that is used depends on whether the protocol uses hold-down states and if a route in the hold-down state exists for the destination.</span></span>

<span data-ttu-id="d49f6-114">Os protocolos que não usam os Estados suspensos podem ignorar informações de rota relacionadas aos Estados de espera de um destino e sempre anunciar a melhor rota.</span><span class="sxs-lookup"><span data-stu-id="d49f6-114">Protocols that do not use hold-down states can ignore route information that relates to hold-down states for a destination, and always advertise the best route.</span></span>

<span data-ttu-id="d49f6-115">Para obter um exemplo de código que mostra como usar essas funções, consulte [usar o estado de Hold-Down de rota](use-the-route-hold-down-state.md).</span><span class="sxs-lookup"><span data-stu-id="d49f6-115">For sample code that shows how to use these functions, see [Use the Route Hold-Down State](use-the-route-hold-down-state.md).</span></span>

 

 




