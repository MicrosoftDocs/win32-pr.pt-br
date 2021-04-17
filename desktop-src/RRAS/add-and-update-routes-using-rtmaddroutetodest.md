---
title: Adicionar e atualizar rotas usando RtmAddRouteToDest
description: A função RtmAddRouteToDest é usada para adicionar novas rotas e atualizar as rotas existentes para um destino. Os procedimentos a seguir explicam os dois casos. O código de exemplo a seguir mostra como implementar o primeiro procedimento.
ms.assetid: 17a04511-69f8-4e50-993c-0e558ee72184
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd3594aee054e6815094834bedbc1aae158fc4e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105766356"
---
# <a name="add-and-update-routes-using-rtmaddroutetodest"></a>Adicionar e atualizar rotas usando RtmAddRouteToDest

A função [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) é usada para adicionar novas rotas e atualizar as rotas existentes para um destino. Os procedimentos a seguir explicam os dois casos. O código de exemplo a seguir mostra como implementar o primeiro procedimento.

**Para adicionar uma rota, o cliente deve executar as seguintes etapas**

1.  Se o cliente já armazenou em cache o identificador de próximo salto, vá para a etapa 4.
2.  Crie uma estrutura de [**\_ \_ informações de NEXTHOP do RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) e preencha-a com as informações apropriadas.
3.  Adicione o próximo salto à tabela de roteamento chamando [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop). O Gerenciador de tabela de roteamento retorna um identificador para o próximo salto. Se o próximo salto já existir, a tabela de roteamento não adicionará o próximo salto; em vez disso, ele retorna o identificador para o próximo salto.
4.  Crie uma estrutura de [**\_ \_ informações de rota RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) e preencha-a com as informações apropriadas, incluindo o identificador de próximo salto retornado pelo Gerenciador de tabela de roteamento.
5.  Adicione a rota à tabela de roteamento chamando [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest). O Gerenciador de tabela de roteamento compara a nova rota com as rotas que já estão na tabela de roteamento. Duas rotas serão iguais se todas as seguintes condições forem verdadeiras:

    -   A rota está sendo adicionada ao mesmo destino.
    -   A rota está sendo adicionada pelo mesmo cliente, conforme especificado pelo membro do **proprietário** da estrutura [**de \_ \_ informações da rota RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) .
    -   A rota é anunciada pelo mesmo vizinho conforme especificado pelo membro **vizinho** da estrutura de [**informações de \_ rota \_ RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) .

    Se a rota existir, o Gerenciador de tabela de roteamento retornará o identificador para a rota existente. Caso contrário, o Gerenciador de tabela de roteamento adicionará a rota e retornará o identificador para a nova rota.

    O cliente pode definir o parâmetro de *\_ sinalizadores de alteração* para a \_ alteração de rota RTM \_ \_ nova para instruir o Gerenciador de tabelas de roteamento a adicionar uma nova rota no destino, mesmo que outra rota com os mesmos campos de proprietário e vizinho exista.

    O cliente pode definir o parâmetro de *\_ sinalizadores de alteração* para a \_ rota RTM \_ alterar \_ primeiro para informar ao Gerenciador de tabela de roteamento para atualizar a primeira rota no destino de Propriedade do cliente. Essa atualização pode ser executada se essa rota existir, mesmo se o campo vizinho não corresponder. Esse sinalizador é usado por clientes que mantêm uma rota única por destino.

**Para atualizar uma rota, o cliente deve executar as seguintes etapas**

1.  Chame [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) com a alça para a rota. O identificador é anteriormente armazenado em cache pelo cliente, ou retornado pelo Gerenciador de tabelas de roteamento de uma chamada que retorna um identificador de rota como **RtmGetRouteInfo**.
2.  Faça as alterações na estrutura [**de \_ \_ informações da rota RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) retornada pelo Gerenciador de tabela de roteamento.
3.  Chame [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) com o identificador para a rota e a estrutura [**de \_ \_ informações da rota RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) alterada.

O código de exemplo a seguir mostra como adicionar uma rota a um destino usando o Gerenciador de tabela de roteamento como um intermediário.


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



 

 




