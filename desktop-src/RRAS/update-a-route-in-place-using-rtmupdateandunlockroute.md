---
title: Atualizar uma rota no local usando o RtmUpdateAndUnlockRoute
description: O procedimento a seguir descreve as etapas usadas para atualizar uma rota no local. O código de exemplo a seguir mostra como implementar o procedimento.
ms.assetid: 3598a28f-8ade-4b3f-9d31-4f2c84df2dd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb79b86645d77f0ee44ffd06b8ef6f403dbd8ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364167"
---
# <a name="update-a-route-in-place-using-rtmupdateandunlockroute"></a><span data-ttu-id="3bbf4-104">Atualizar uma rota no local usando o RtmUpdateAndUnlockRoute</span><span class="sxs-lookup"><span data-stu-id="3bbf4-104">Update a Route In Place Using RtmUpdateAndUnlockRoute</span></span>

<span data-ttu-id="3bbf4-105">O procedimento a seguir descreve as etapas usadas para atualizar uma rota no local.</span><span class="sxs-lookup"><span data-stu-id="3bbf4-105">The following procedure outlines the steps used to update a route in place.</span></span> <span data-ttu-id="3bbf4-106">O código de exemplo a seguir mostra como implementar o procedimento.</span><span class="sxs-lookup"><span data-stu-id="3bbf4-106">The sample code that follows shows how to implement the procedure.</span></span>

<span data-ttu-id="3bbf4-107">**Para atualizar uma rota no local, o cliente deve executar as seguintes etapas**</span><span class="sxs-lookup"><span data-stu-id="3bbf4-107">**To update a route in place, the client should take the following steps**</span></span>

1.  <span data-ttu-id="3bbf4-108">Bloqueie a rota chamando [**RtmLockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute).</span><span class="sxs-lookup"><span data-stu-id="3bbf4-108">Lock the route by calling [**RtmLockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute).</span></span> <span data-ttu-id="3bbf4-109">Atualmente, essa função realmente bloqueia o destino da rota.</span><span class="sxs-lookup"><span data-stu-id="3bbf4-109">Currently, this function actually locks the route's destination.</span></span> <span data-ttu-id="3bbf4-110">O Gerenciador de tabela de roteamento retorna um ponteiro para a rota.</span><span class="sxs-lookup"><span data-stu-id="3bbf4-110">The routing table manager returns a pointer to the route.</span></span>
2.  <span data-ttu-id="3bbf4-111">Use o ponteiro para a estrutura de [**\_ \_ informações de rota RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) do Gerenciador de tabela de roteamento, obtida na etapa 1, para fazer as alterações necessárias na rota.</span><span class="sxs-lookup"><span data-stu-id="3bbf4-111">Use the pointer to the routing table manager's [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure, obtained in step 1, to make the necessary changes to the route.</span></span> <span data-ttu-id="3bbf4-112">Somente determinados membros da estrutura **de \_ \_ informações da rota RTM** podem ser modificados durante a atualização no local.</span><span class="sxs-lookup"><span data-stu-id="3bbf4-112">Only certain members of the **RTM\_ROUTE\_INFO** structure can be modified when updating in place.</span></span> <span data-ttu-id="3bbf4-113">Esses membros são: **vizinho**, **PrefInfo**, **EntitySpecificInfo**, **BelongsToViews** e **NextHopsList**.</span><span class="sxs-lookup"><span data-stu-id="3bbf4-113">These members are: **Neighbour**, **PrefInfo**, **EntitySpecificInfo**, **BelongsToViews**, and **NextHopsList**.</span></span>
    > [!Note]  
    > <span data-ttu-id="3bbf4-114">Se o cliente adicionar informações aos membros **vizinho** ou **NextHopsList** , o cliente deverá chamar [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) para incrementar explicitamente a contagem de referência que o Gerenciador de tabela de roteamento mantém no objeto de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="3bbf4-114">If the client adds information to either the **Neighbour** or **NextHopsList** members, the client must call [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) to explicitly increment the reference count that the routing table manager keeps on the next-hop object.</span></span> <span data-ttu-id="3bbf4-115">Da mesma forma, se o cliente remover informações do membro **NextHopsList** , o cliente deverá chamar [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) para decrementar a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="3bbf4-115">Similarly, if the client removes information from the **NextHopsList** member, the client must call [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) to decrement the reference count.</span></span>

     

3.  <span data-ttu-id="3bbf4-116">Chame [**RtmUpdateAndUnlockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute) para notificar o Gerenciador de tabela de roteamento de que uma alteração foi feita.</span><span class="sxs-lookup"><span data-stu-id="3bbf4-116">Call [**RtmUpdateAndUnlockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute) to notify the routing table manager that a change has taken place.</span></span> <span data-ttu-id="3bbf4-117">O Gerenciador de tabela de roteamento confirma as alterações, atualiza o destino para refletir as novas informações e, em seguida, desbloqueia a rota.</span><span class="sxs-lookup"><span data-stu-id="3bbf4-117">The routing table manager commits the changes, updates the destination to reflect the new information, and then unlocks the route.</span></span>

<span data-ttu-id="3bbf4-118">O código de exemplo a seguir mostra como atualizar uma rota diretamente, usando um ponteiro para as informações de rota reais na tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="3bbf4-118">The following sample code shows how to update a route directly, using a pointer to the actual route information in the routing table.</span></span>


```C++
Status = RtmLockRoute(RtmRegHandle,
                      RouteHandle,
                      TRUE,
                      TRUE,
                      &RoutePointer);

if (Status == NO_ERROR)
{
        // Update route parameters in place (i.e., directly on 
// the routing table manager's copy)
    
    // Update the metric and views of the route
    RoutePointer->PrefInfo.Metric = 16;

    // Change the views so that the route belongs to only the multicast view
    RoutePointer->BelongsToViews = RTM_VIEW_MASK_MCAST;

    // Set the entity-specific information to X
    RoutePointer->EntitySpecificInfo = X;

    // Note that the following manipulation of
    // next-hop references is not needed when
    // using RtmAddRouteToDest, as it is done
    // by the routing table manager automatically
    
    // Change next hop from NextHop1 to NextHop2
    NextHop1 = RoutePointer->NextHopsList.NextHop[0];

    // Explicitly dereference the old next hop
    RtmReleaseNextHops(RtmRegHandle, 1, &NextHop1);

    RoutePointer->NextHopsList.NextHop[0] = NextHop2;

    // Explicitly reference next hop being added
    RtmReferenceHandles(RtmRegHandle, 1, &NextHop2);

    // Call the routing table manager to indicate that route information
    // has changed, and that its position might
    // have to be rearranged and the corresponding destination
    // needs to be updated to reflect this change.
    
    Status = RtmUpdateAndUnlockRoute(RtmRegHandle,
                                     RouteHandle,
                                     INFINITE, // Keep forever
                                     NULL,
                                     0,
                                     NULL,
                                     &ChangeFlags);
    ASSERT(Status == NO_ERROR);
}
```



 

 




