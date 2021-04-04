---
title: Rotas estáticas e auto-estáticas
description: Normalmente, as rotas para redes remotas são obtidas dinamicamente por meio de protocolos de roteamento.
ms.assetid: af2f2039-8131-4ca9-98bf-6aeb7a511034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3faa8931e0fee5c75f598b920b7b97a1e0e829d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916553"
---
# <a name="static-and-autostatic-routes"></a><span data-ttu-id="70ee1-103">Rotas estáticas e auto-estáticas</span><span class="sxs-lookup"><span data-stu-id="70ee1-103">Static and Autostatic Routes</span></span>

<span data-ttu-id="70ee1-104">Normalmente, as rotas para redes remotas são obtidas dinamicamente por meio de protocolos de roteamento.</span><span class="sxs-lookup"><span data-stu-id="70ee1-104">Typically, routes to remote networks are obtained dynamically through routing protocols.</span></span> <span data-ttu-id="70ee1-105">No entanto, o administrador também pode *propagar* a tabela de roteamento fornecendo rotas manualmente.</span><span class="sxs-lookup"><span data-stu-id="70ee1-105">However, the administrator can also *seed* the routing table by providing routes manually.</span></span> <span data-ttu-id="70ee1-106">Essas rotas são conhecidas como *estáticas*.</span><span class="sxs-lookup"><span data-stu-id="70ee1-106">These routes are referred to as *static*.</span></span> <span data-ttu-id="70ee1-107">Uma rota estática é associada a uma interface que representa a rede remota.</span><span class="sxs-lookup"><span data-stu-id="70ee1-107">A static route is associated with an interface that represents the remote network.</span></span> <span data-ttu-id="70ee1-108">Ao contrário das rotas dinâmicas, as rotas estáticas são retidas mesmo se o roteador for reiniciado ou a interface estiver desabilitada.</span><span class="sxs-lookup"><span data-stu-id="70ee1-108">Unlike dynamic routes, static routes are retained even if the router is restarted or the interface is disabled.</span></span>

<span data-ttu-id="70ee1-109">Uma rota *autoestática* é obtida por meio de um protocolo de roteamento, mas uma vez obtida se comporta como uma rota estática.</span><span class="sxs-lookup"><span data-stu-id="70ee1-109">An *autostatic* route is obtained through a routing protocol, but once obtained behaves like a static route.</span></span> <span data-ttu-id="70ee1-110">O processo para obter rotas autoestáticas é o seguinte: o Gerenciador de roteador IP ou IPX emite uma solicitação que um protocolo de roteamento atualiza as informações de roteamento para uma interface específica.</span><span class="sxs-lookup"><span data-stu-id="70ee1-110">The process for obtaining autostatic routes is as follows: The IP or IPX router manager issues a request that a routing protocol update the routing information for a specific interface.</span></span> <span data-ttu-id="70ee1-111">Os resultados da atualização são então convertidos em rotas estáticas.</span><span class="sxs-lookup"><span data-stu-id="70ee1-111">The results of the update are then converted into static routes.</span></span> <span data-ttu-id="70ee1-112">Observe que apenas determinados protocolos de roteamento dão suporte a solicitações para atualizações de rota autoestática.</span><span class="sxs-lookup"><span data-stu-id="70ee1-112">Note that only certain routing protocols support requests for autostatic route updates.</span></span>

 

 




