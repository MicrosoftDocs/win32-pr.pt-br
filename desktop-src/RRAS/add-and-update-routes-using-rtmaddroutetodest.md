---
title: Adicionar e atualizar rotas usando RtmAddRouteToDest
description: A função RtmAddRouteToDest é usada para adicionar novas rotas e atualizar rotas existentes para um destino. Os procedimentos a seguir explicam os dois casos. O código de exemplo a seguir mostra como implementar o primeiro procedimento.
ms.assetid: 17a04511-69f8-4e50-993c-0e558ee72184
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64032aa5f73019e08bb82405d85ffa5ef85abd0526cf7748ec8881b97ab900e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030596"
---
# <a name="add-and-update-routes-using-rtmaddroutetodest"></a>Adicionar e atualizar rotas usando RtmAddRouteToDest

A função [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) é usada para adicionar novas rotas e atualizar rotas existentes para um destino. Os procedimentos a seguir explicam os dois casos. O código de exemplo a seguir mostra como implementar o primeiro procedimento.

**Para adicionar uma rota, o cliente deve seguir as etapas a seguir**

1.  Se o cliente já tiver armazenado em cache o alça do próximo salto, vá para a etapa 4.
2.  Crie uma [**estrutura \_ RTM NEXTHOP \_ INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) e preencha-a com as informações apropriadas.
3.  Adicione o próximo salto à tabela de roteamento chamando [**RtmAddNextHop.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop) O gerenciador de tabela de roteamento retorna um alça para o próximo salto. Se o próximo salto já existir, a tabela de roteamento não adicionará o próximo salto; em vez disso, ele retorna o alça para o próximo salto.
4.  Crie uma [**estrutura \_ RTM ROUTE \_ INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) e preencha-a com as informações apropriadas, incluindo o alça do próximo salto retornado pelo gerenciador de tabela de roteamento.
5.  Adicione a rota à tabela de roteamento chamando [**RtmAddRouteToDest.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) O gerenciador de tabela de roteamento compara a nova rota com as rotas que já estão na tabela de roteamento. Duas rotas serão iguais se todas as seguintes condições são verdadeiras:

    -   A rota está sendo adicionada ao mesmo destino.
    -   A rota está sendo adicionada pelo mesmo cliente, conforme especificado pelo membro **Proprietário** da estrutura [**RTM \_ ROUTE \_ INFO.**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info)
    -   A rota é anunciada pelo mesmo vizinho, conforme especificado pelo membro **Vizinho** da estrutura [**RTM \_ ROUTE \_ INFO.**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info)

    Se a rota existir, o gerenciador de tabela de roteamento retornará o alçamento para a rota existente. Caso contrário, o gerenciador de tabela de roteamento adiciona a rota e retorna o alça para a nova rota.

    O cliente pode definir o parâmetro *Change \_ Flags* como RTM ROUTE CHANGE NEW para instruir o gerenciador de tabelas de roteamento a adicionar uma nova rota no destino, mesmo que exista outra rota com os mesmos campos proprietário e \_ \_ \_ vizinho.

    O cliente pode definir o parâmetro *Change \_ Flags* como RTM ROUTE CHANGE FIRST para dizer ao gerenciador de tabelas de roteamento para atualizar a primeira rota no destino \_ pertencente ao \_ \_ cliente. Essa atualização poderá ser executada se essa rota existir, mesmo se o campo vizinho não corresponder. Esse sinalizador é usado por clientes que mantêm uma única rota por destino.

**Para atualizar uma rota, o cliente deve seguir as etapas a seguir**

1.  Chame [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) com o alçamento para a rota. O handle é um armazenado anteriormente em cache pelo cliente ou retornado pelo gerenciador de tabela de roteamento de uma chamada que retorna um alça de rota como **RtmGetRouteInfo**.
2.  Faça as alterações na estrutura [**RTM \_ ROUTE \_ INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) retornada pelo gerenciador de tabela de roteamento.
3.  Chame [**RtmAddRouteToDest com**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) o alçamento para a rota e a estrutura de INFORMAÇÕES DE [**ROTA RTM \_ \_ alterada.**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info)

O código de exemplo a seguir mostra como adicionar uma rota a um destino usando o gerenciador de tabela de roteamento como um intermediário.


```C++
// Add a route to a destination given by (addr, masklen)
// using a next hop reachable with an interface

RTM_NEXTHOP_INFO NextHopInfo;

// First, create and add a next hop to the caller's
// next-hop tree (if it does not already exist)

ZeroMemory(&NextHopInfo, sizeof(RTM_NEXTHOP_INFO);

RTM_IPV4_MAKE_NET_ADDRESS(&NextHopInfo.NextHopAddress,
                          nexthop, // Address of the next hop
                          32);

NextHopInfo.InterfaceIndex = interface;

NextHopHandle = NULL;

Status = RtmAddNextHop(RtmRegHandle,
                       &NextHopInfo,
                       &NextHopHandle,
                       &ChangeFlags);

if (Status == NO_ERROR)
{
    // Created a new next hop or found an old one

        // Fill in the route information for the route
    
    ZeroMemory(&RouteInfo, sizeof(RTM_ROUTE_INFO);

    // Fill in the destination network's address and mask values
    RTM_IPV4_MAKE_NET_ADDRESS(&NetAddress, addr, masklen);

    // Assume 'neighbour learnt from' is the first next hop
    RouteInfo.Neighbour = NextHopHandle;

    // Set metric for route; Preference set internally
    RouteInfo.PrefInfo.Metric = metric;

    // Adding a route to both the unicast and multicast views
    RouteInfo.BelongsToViews = RTM_VIEW_MASK_UCAST|RTM_VIEW_MASK_MCAST;

    RouteInfo.NextHopsList.NumNextHops = 1;
    RouteInfo.NextHopsList.NextHops[0] = NextHopHandle;

    // If you want to add a new route, regardless of
    // whether a similar route already exists, use the following 
    //     ChangeFlags = RTM_ROUTE_CHANGE_NEW;

    ChangeFlags = 0;

    Status = RtmAddRouteToDest(RtmRegHandle,
                               &RouteHandle,     // Can be NULL if you do not need handle
                               &NetAddress,
                               &RouteInfo,
                               1000,             // Time out route after 1000 ms
                               RouteListHandle1, // Also add the route to this list
                               0,
                               NULL,
                               &ChangeFlags);

    if (Status == NO_ERROR)
    {
        if (ChangeFlags & RTM_ROUTE_CHANGE_NEW)
        {
        ; // A new route has been created
        }
        else
        {
        ; // An existing route is updated
        }

        if (ChangeFlags & RTM_ROUTE_CHANGE_BEST)
        {
        ; // Best route information has changed
        }

        // Release the route handle if you do not need it
        RtmReleaseRoutes(RtmRegHandle, 1, &RouteHandle);
    }

    // Also release the next hop since it is no longer needed 
    RtmReleaseNextHops(RtmRegHandle, 1, &NextHopHandle);
}
```



 

 




