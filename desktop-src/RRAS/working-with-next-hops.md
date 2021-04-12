---
title: Trabalhando com próximos saltos
description: A API RTMv2 permite que os clientes trabalhem com a lista de próximos saltos associados a rotas e destinos.
ms.assetid: ef474091-48fe-48e5-b476-73d77dbcbec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d20a812fd272afafd2cd8eb1d6fb93d97530a2a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364370"
---
# <a name="working-with-next-hops"></a><span data-ttu-id="36fb3-103">Trabalhando com próximos saltos</span><span class="sxs-lookup"><span data-stu-id="36fb3-103">Working with Next Hops</span></span>

<span data-ttu-id="36fb3-104">A API RTMv2 permite que os clientes trabalhem com a lista de próximos saltos associados a rotas e destinos.</span><span class="sxs-lookup"><span data-stu-id="36fb3-104">The RTMv2 API allows clients to work with the list of next hops that are associated with routes and destinations.</span></span> <span data-ttu-id="36fb3-105">Os clientes podem adicionar ou atualizar um próximo salto chamando [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop).</span><span class="sxs-lookup"><span data-stu-id="36fb3-105">Clients can add or update a next hop by calling [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop).</span></span> <span data-ttu-id="36fb3-106">Os clientes podem excluir um próximo salto usando [**RtmDeleteNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop).</span><span class="sxs-lookup"><span data-stu-id="36fb3-106">Clients can delete a next hop using [**RtmDeleteNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop).</span></span> <span data-ttu-id="36fb3-107">Os clientes podem pesquisar os próximos saltos chamando [**RtmFindNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop).</span><span class="sxs-lookup"><span data-stu-id="36fb3-107">Clients can search for next hops by calling [**RtmFindNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop).</span></span>

<span data-ttu-id="36fb3-108">Os clientes também podem atualizar o próximo salto diretamente.</span><span class="sxs-lookup"><span data-stu-id="36fb3-108">Clients can also update the next hop directly.</span></span> <span data-ttu-id="36fb3-109">Para fazer isso, o cliente deve primeiro bloquear o próximo salto com a função [**RtmLockNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop) .</span><span class="sxs-lookup"><span data-stu-id="36fb3-109">To do so, the client must first lock the next hop with the [**RtmLockNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop) function.</span></span> <span data-ttu-id="36fb3-110">Em seguida, o cliente pode usar o ponteiro direto para a estrutura de [**\_ \_ informações de NEXTHOP**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) do Gerenciador de tabela de roteamento para fazer as modificações necessárias.</span><span class="sxs-lookup"><span data-stu-id="36fb3-110">Then the client can use the direct pointer to the routing table manager's [**RTM\_NEXTHOP\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) structure to make necessary modifications.</span></span> <span data-ttu-id="36fb3-111">Por fim, o cliente pode desbloquear o próximo salto.</span><span class="sxs-lookup"><span data-stu-id="36fb3-111">Finally, the client can unlock the next hop.</span></span>

> [!Note]  
> <span data-ttu-id="36fb3-112">Os campos de endereço de próximo salto e índice de interface no próximo salto identificam exclusivamente o próximo salto e não devem ser modificados.</span><span class="sxs-lookup"><span data-stu-id="36fb3-112">The next-hop address and interface index fields in the next hop uniquely identify the next hop and should not be modified.</span></span>

 

 

 




