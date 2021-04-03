---
title: Atualizando rotas usando RtmAddRouteToDest
description: Se o cliente não precisar de eficiência ao adicionar uma rota, ele deverá usar o método de atualização de rotas a seguir.
ms.assetid: bfa914ea-5d54-4ce9-a97c-903c497d135b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c7972b2d5ec0996cafc1dd32a8a4056a6aeb0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916551"
---
# <a name="updating-routes-using-rtmaddroutetodest"></a><span data-ttu-id="2250b-103">Atualizando rotas usando RtmAddRouteToDest</span><span class="sxs-lookup"><span data-stu-id="2250b-103">Updating Routes Using RtmAddRouteToDest</span></span>

<span data-ttu-id="2250b-104">Se o cliente não precisar de eficiência ao adicionar uma rota, ele deverá usar o método de atualização de rotas a seguir.</span><span class="sxs-lookup"><span data-stu-id="2250b-104">If the client does not require efficiency when adding a route, it should use the following method of updating routes.</span></span> <span data-ttu-id="2250b-105">Esse método é menos eficiente, pois requer a obtenção de um identificador para a rota e a passagem da estrutura de [**\_ \_ informações da rota RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) de e para o Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="2250b-105">This method is less efficient since it requires obtaining a handle to the route and passing the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure to and from the routing table manager.</span></span> <span data-ttu-id="2250b-106">Esse método também leva mais tempo.</span><span class="sxs-lookup"><span data-stu-id="2250b-106">This method also takes more time.</span></span> <span data-ttu-id="2250b-107">Como o [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) não manipula a tabela de roteamento diretamente, usar esse método compensa a eficiência para simplificar.</span><span class="sxs-lookup"><span data-stu-id="2250b-107">Since [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) does not manipulate the routing table directly, using this method trades efficiency for simplicity.</span></span>

<span data-ttu-id="2250b-108">Para obter um exemplo de código que mostra como usar essas funções, consulte [Adicionar e atualizar rotas usando o RtmAddRouteToDest](add-and-update-routes-using-rtmaddroutetodest.md).</span><span class="sxs-lookup"><span data-stu-id="2250b-108">For sample code that shows how to use these functions, see [Add and Update Routes Using RtmAddRouteToDest](add-and-update-routes-using-rtmaddroutetodest.md).</span></span>

 

 




