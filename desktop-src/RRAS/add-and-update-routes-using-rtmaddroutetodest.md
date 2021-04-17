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
# <a name="add-and-update-routes-using-rtmaddroutetodest"></a><span data-ttu-id="36584-105">Adicionar e atualizar rotas usando RtmAddRouteToDest</span><span class="sxs-lookup"><span data-stu-id="36584-105">Add and Update Routes Using RtmAddRouteToDest</span></span>

<span data-ttu-id="36584-106">A função [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) é usada para adicionar novas rotas e atualizar as rotas existentes para um destino.</span><span class="sxs-lookup"><span data-stu-id="36584-106">The function [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) is used to add new routes and update existing routes for a destination.</span></span> <span data-ttu-id="36584-107">Os procedimentos a seguir explicam os dois casos.</span><span class="sxs-lookup"><span data-stu-id="36584-107">The following procedures explain both cases.</span></span> <span data-ttu-id="36584-108">O código de exemplo a seguir mostra como implementar o primeiro procedimento.</span><span class="sxs-lookup"><span data-stu-id="36584-108">The sample code that follows shows how to implement the first procedure.</span></span>

<span data-ttu-id="36584-109">**Para adicionar uma rota, o cliente deve executar as seguintes etapas**</span><span class="sxs-lookup"><span data-stu-id="36584-109">**To add a route, the client should take the following steps**</span></span>

1.  <span data-ttu-id="36584-110">Se o cliente já armazenou em cache o identificador de próximo salto, vá para a etapa 4.</span><span class="sxs-lookup"><span data-stu-id="36584-110">If the client has already cached the next-hop handle, go to step 4.</span></span>
2.  <span data-ttu-id="36584-111">Crie uma estrutura de [**\_ \_ informações de NEXTHOP do RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) e preencha-a com as informações apropriadas.</span><span class="sxs-lookup"><span data-stu-id="36584-111">Create an [**RTM\_NEXTHOP\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) structure and fill it with the appropriate information.</span></span>
3.  <span data-ttu-id="36584-112">Adicione o próximo salto à tabela de roteamento chamando [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop).</span><span class="sxs-lookup"><span data-stu-id="36584-112">Add the next hop to the routing table by calling [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop).</span></span> <span data-ttu-id="36584-113">O Gerenciador de tabela de roteamento retorna um identificador para o próximo salto.</span><span class="sxs-lookup"><span data-stu-id="36584-113">The routing table manager returns a handle to the next hop.</span></span> <span data-ttu-id="36584-114">Se o próximo salto já existir, a tabela de roteamento não adicionará o próximo salto; em vez disso, ele retorna o identificador para o próximo salto.</span><span class="sxs-lookup"><span data-stu-id="36584-114">If the next hop already exists, the routing table does not add the next hop; instead it returns the handle to the next hop.</span></span>
4.  <span data-ttu-id="36584-115">Crie uma estrutura de [**\_ \_ informações de rota RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) e preencha-a com as informações apropriadas, incluindo o identificador de próximo salto retornado pelo Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="36584-115">Create an [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure and fill it with the appropriate information, including the next-hop handle returned by the routing table manager.</span></span>
5.  <span data-ttu-id="36584-116">Adicione a rota à tabela de roteamento chamando [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest).</span><span class="sxs-lookup"><span data-stu-id="36584-116">Add the route to the routing table by calling [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest).</span></span> <span data-ttu-id="36584-117">O Gerenciador de tabela de roteamento compara a nova rota com as rotas que já estão na tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="36584-117">The routing table manager compares the new route to the routes that are already in the routing table.</span></span> <span data-ttu-id="36584-118">Duas rotas serão iguais se todas as seguintes condições forem verdadeiras:</span><span class="sxs-lookup"><span data-stu-id="36584-118">Two routes are equal if all of the following conditions are true:</span></span>

    -   <span data-ttu-id="36584-119">A rota está sendo adicionada ao mesmo destino.</span><span class="sxs-lookup"><span data-stu-id="36584-119">The route is being added to the same destination.</span></span>
    -   <span data-ttu-id="36584-120">A rota está sendo adicionada pelo mesmo cliente, conforme especificado pelo membro do **proprietário** da estrutura [**de \_ \_ informações da rota RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) .</span><span class="sxs-lookup"><span data-stu-id="36584-120">The route is being added by the same client as specified by the **Owner** member of the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure.</span></span>
    -   <span data-ttu-id="36584-121">A rota é anunciada pelo mesmo vizinho conforme especificado pelo membro **vizinho** da estrutura de [**informações de \_ rota \_ RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) .</span><span class="sxs-lookup"><span data-stu-id="36584-121">The route is advertised by the same neighbor as specified by the **Neighbor** member of the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure.</span></span>

    <span data-ttu-id="36584-122">Se a rota existir, o Gerenciador de tabela de roteamento retornará o identificador para a rota existente.</span><span class="sxs-lookup"><span data-stu-id="36584-122">If the route exists, the routing table manager returns the handle to the existing route.</span></span> <span data-ttu-id="36584-123">Caso contrário, o Gerenciador de tabela de roteamento adicionará a rota e retornará o identificador para a nova rota.</span><span class="sxs-lookup"><span data-stu-id="36584-123">Otherwise, the routing table manager adds the route and returns the handle to the new route.</span></span>

    <span data-ttu-id="36584-124">O cliente pode definir o parâmetro de *\_ sinalizadores de alteração* para a \_ alteração de rota RTM \_ \_ nova para instruir o Gerenciador de tabelas de roteamento a adicionar uma nova rota no destino, mesmo que outra rota com os mesmos campos de proprietário e vizinho exista.</span><span class="sxs-lookup"><span data-stu-id="36584-124">The client can set the *Change\_Flags* parameter to RTM\_ROUTE\_CHANGE\_NEW to instruct the routing table manager to add a new route on the destination, even if another route with the same owner and neighbor fields exists.</span></span>

    <span data-ttu-id="36584-125">O cliente pode definir o parâmetro de *\_ sinalizadores de alteração* para a \_ rota RTM \_ alterar \_ primeiro para informar ao Gerenciador de tabela de roteamento para atualizar a primeira rota no destino de Propriedade do cliente.</span><span class="sxs-lookup"><span data-stu-id="36584-125">The client can set the *Change\_Flags* parameter to RTM\_ROUTE\_CHANGE\_FIRST to tell the routing table manager to update the first route on the destination owned by the client.</span></span> <span data-ttu-id="36584-126">Essa atualização pode ser executada se essa rota existir, mesmo se o campo vizinho não corresponder.</span><span class="sxs-lookup"><span data-stu-id="36584-126">This update can be performed if such a route exists, even if the neighbor field does not match.</span></span> <span data-ttu-id="36584-127">Esse sinalizador é usado por clientes que mantêm uma rota única por destino.</span><span class="sxs-lookup"><span data-stu-id="36584-127">This flag is used by clients that maintain a single route per destination.</span></span>

<span data-ttu-id="36584-128">**Para atualizar uma rota, o cliente deve executar as seguintes etapas**</span><span class="sxs-lookup"><span data-stu-id="36584-128">**To update a route, the client should take the following steps**</span></span>

1.  <span data-ttu-id="36584-129">Chame [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) com a alça para a rota.</span><span class="sxs-lookup"><span data-stu-id="36584-129">Call [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) with the handle to the route.</span></span> <span data-ttu-id="36584-130">O identificador é anteriormente armazenado em cache pelo cliente, ou retornado pelo Gerenciador de tabelas de roteamento de uma chamada que retorna um identificador de rota como **RtmGetRouteInfo**.</span><span class="sxs-lookup"><span data-stu-id="36584-130">The handle is either one previously cached by the client, or returned by the routing table manager from a call that returns a route handle such as **RtmGetRouteInfo**.</span></span>
2.  <span data-ttu-id="36584-131">Faça as alterações na estrutura [**de \_ \_ informações da rota RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) retornada pelo Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="36584-131">Make the changes to the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure that is returned by the routing table manager.</span></span>
3.  <span data-ttu-id="36584-132">Chame [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) com o identificador para a rota e a estrutura [**de \_ \_ informações da rota RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) alterada.</span><span class="sxs-lookup"><span data-stu-id="36584-132">Call [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) with the handle to the route and the changed [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure.</span></span>

<span data-ttu-id="36584-133">O código de exemplo a seguir mostra como adicionar uma rota a um destino usando o Gerenciador de tabela de roteamento como um intermediário.</span><span class="sxs-lookup"><span data-stu-id="36584-133">The following sample code shows how to add a route to a destination using the routing table manager as an intermediary.</span></span>


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



 

 




