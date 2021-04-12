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
# <a name="update-a-route-in-place-using-rtmupdateandunlockroute"></a>Atualizar uma rota no local usando o RtmUpdateAndUnlockRoute

O procedimento a seguir descreve as etapas usadas para atualizar uma rota no local. O código de exemplo a seguir mostra como implementar o procedimento.

**Para atualizar uma rota no local, o cliente deve executar as seguintes etapas**

1.  Bloqueie a rota chamando [**RtmLockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute). Atualmente, essa função realmente bloqueia o destino da rota. O Gerenciador de tabela de roteamento retorna um ponteiro para a rota.
2.  Use o ponteiro para a estrutura de [**\_ \_ informações de rota RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) do Gerenciador de tabela de roteamento, obtida na etapa 1, para fazer as alterações necessárias na rota. Somente determinados membros da estrutura **de \_ \_ informações da rota RTM** podem ser modificados durante a atualização no local. Esses membros são: **vizinho**, **PrefInfo**, **EntitySpecificInfo**, **BelongsToViews** e **NextHopsList**.
    > [!Note]  
    > Se o cliente adicionar informações aos membros **vizinho** ou **NextHopsList** , o cliente deverá chamar [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) para incrementar explicitamente a contagem de referência que o Gerenciador de tabela de roteamento mantém no objeto de próximo salto. Da mesma forma, se o cliente remover informações do membro **NextHopsList** , o cliente deverá chamar [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) para decrementar a contagem de referência.

     

3.  Chame [**RtmUpdateAndUnlockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute) para notificar o Gerenciador de tabela de roteamento de que uma alteração foi feita. O Gerenciador de tabela de roteamento confirma as alterações, atualiza o destino para refletir as novas informações e, em seguida, desbloqueia a rota.

O código de exemplo a seguir mostra como atualizar uma rota diretamente, usando um ponteiro para as informações de rota reais na tabela de roteamento.


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



 

 




