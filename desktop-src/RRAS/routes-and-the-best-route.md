---
title: Rotas e a melhor rota
description: Uma rota é um caminho de rede \ 0034; \ 0034; para um destino que tem um determinado custo associado a ele. O custo é representado por sua preferência administrativa e sua métrica específica de protocolo. As rotas com custos mais baixos são preferenciais em todas as outras rotas.
ms.assetid: c5a75308-42da-4ef9-a712-9987c87eef84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd55ec1188383f4cdef55511aae7a9c2cf59303
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105775656"
---
# <a name="routes-and-the-best-route"></a><span data-ttu-id="02e20-105">Rotas e a melhor rota</span><span class="sxs-lookup"><span data-stu-id="02e20-105">Routes and the Best Route</span></span>

<span data-ttu-id="02e20-106">Uma rota é um "caminho de rede" para um destino que tem um determinado custo associado a ele.</span><span class="sxs-lookup"><span data-stu-id="02e20-106">A route is a "network path" to a destination that has a certain cost associated with it.</span></span> <span data-ttu-id="02e20-107">O custo é representado por sua preferência administrativa e sua métrica específica de protocolo.</span><span class="sxs-lookup"><span data-stu-id="02e20-107">The cost is represented by its administrative preference and its protocol-specific metric.</span></span> <span data-ttu-id="02e20-108">As rotas com custos mais baixos são preferenciais em todas as outras rotas.</span><span class="sxs-lookup"><span data-stu-id="02e20-108">Routes with lower costs are preferred over all other routes.</span></span>

<span data-ttu-id="02e20-109">Uma entrada de rota na tabela de roteamento inclui:</span><span class="sxs-lookup"><span data-stu-id="02e20-109">A route entry in the routing table includes:</span></span>

-   <span data-ttu-id="02e20-110">Um identificador para o destino</span><span class="sxs-lookup"><span data-stu-id="02e20-110">A handle to the destination</span></span>
-   <span data-ttu-id="02e20-111">O proprietário desta rota</span><span class="sxs-lookup"><span data-stu-id="02e20-111">The owner of this route</span></span>
-   <span data-ttu-id="02e20-112">O vizinho (par) que forneceu as informações de rota</span><span class="sxs-lookup"><span data-stu-id="02e20-112">The neighbor (peer) that provided the route information</span></span>
-   <span data-ttu-id="02e20-113">Sinalizadores associados ao estado da rota</span><span class="sxs-lookup"><span data-stu-id="02e20-113">Flags associated with the state of the route</span></span>
-   <span data-ttu-id="02e20-114">Sinalizadores associados à rota</span><span class="sxs-lookup"><span data-stu-id="02e20-114">Flags associated with the route</span></span>
-   <span data-ttu-id="02e20-115">A preferência e a métrica para a rota</span><span class="sxs-lookup"><span data-stu-id="02e20-115">The preference and metric for the route</span></span>
-   <span data-ttu-id="02e20-116">A lista de exibições às quais a rota pertence</span><span class="sxs-lookup"><span data-stu-id="02e20-116">The list of views to which the route belongs</span></span>
-   <span data-ttu-id="02e20-117">Informações que são privadas para o proprietário da rota</span><span class="sxs-lookup"><span data-stu-id="02e20-117">Information that is private to the owner of the route</span></span>
-   <span data-ttu-id="02e20-118">Uma lista de próximos saltos usados para alcançar o destino</span><span class="sxs-lookup"><span data-stu-id="02e20-118">A list of next hops used to reach the destination</span></span>

<span data-ttu-id="02e20-119">Os valores a seguir, em conjunto, identificam exclusivamente uma rota na tabela de roteamento:</span><span class="sxs-lookup"><span data-stu-id="02e20-119">The following values, taken together, uniquely identify a route in the routing table:</span></span>

-   <span data-ttu-id="02e20-120">A rede de destino</span><span class="sxs-lookup"><span data-stu-id="02e20-120">The destination network</span></span>
-   <span data-ttu-id="02e20-121">O proprietário da rota</span><span class="sxs-lookup"><span data-stu-id="02e20-121">The owner of the route</span></span>
-   <span data-ttu-id="02e20-122">O vizinho que forneceu a rota</span><span class="sxs-lookup"><span data-stu-id="02e20-122">The neighbor who supplied the route</span></span>

## <a name="metrics-and-preference"></a><span data-ttu-id="02e20-123">Métricas e preferência</span><span class="sxs-lookup"><span data-stu-id="02e20-123">Metrics and Preference</span></span>

<span data-ttu-id="02e20-124">Cada rota tem uma preferência administrativa (especificada pela política de roteamento) e uma métrica dependente do cliente.</span><span class="sxs-lookup"><span data-stu-id="02e20-124">Each route has an administrative preference (specified by the routing policy), and a client-dependent metric.</span></span> <span data-ttu-id="02e20-125">O Gerenciador de tabela de roteamento usa essas informações para determinar qual rota é a melhor rota para um destino.</span><span class="sxs-lookup"><span data-stu-id="02e20-125">The routing table manager uses this information to determine which route is the better route to a destination.</span></span> <span data-ttu-id="02e20-126">Rotas com preferência mais baixa são rotas melhores (uma sendo a mais baixa e, portanto, melhor).</span><span class="sxs-lookup"><span data-stu-id="02e20-126">Routes with lower preference are better routes (one being lowest, and therefore best).</span></span> <span data-ttu-id="02e20-127">Se duas rotas tiverem a mesma preferência, a rota com a métrica mais baixa será a melhor rota.</span><span class="sxs-lookup"><span data-stu-id="02e20-127">If two routes have the same preference, the route with the lower metric is the better route.</span></span>

<span data-ttu-id="02e20-128">Normalmente, a preferência de uma rota é determinada pela preferência do cliente que adicionou a rota.</span><span class="sxs-lookup"><span data-stu-id="02e20-128">Normally, the preference of a route is determined by the preference of the client that added the route.</span></span> <span data-ttu-id="02e20-129">No entanto, para todas as rotas adicionadas usando a ferramenta de gerenciamento de Netsh.exe, um valor de preferência pode ser especificado por rota.</span><span class="sxs-lookup"><span data-stu-id="02e20-129">However, for any routes added using the Netsh.exe management tool, a preference value can be specified on a per-route basis.</span></span>

<span data-ttu-id="02e20-130">A preferência é normalmente usada para indicar a prioridade entre os clientes.</span><span class="sxs-lookup"><span data-stu-id="02e20-130">Preference is normally used to indicate priority between clients.</span></span> <span data-ttu-id="02e20-131">Por exemplo, um administrador pode atribuir ao OSPF uma preferência mais baixa (melhor) do que o RIP.</span><span class="sxs-lookup"><span data-stu-id="02e20-131">For example, an administrator can assign OSPF a lower (better) preference than RIP.</span></span> <span data-ttu-id="02e20-132">Nesse caso, as rotas OSPF são preferíveis para rotas RIP.</span><span class="sxs-lookup"><span data-stu-id="02e20-132">In this case, OSPF routes are preferable to RIP routes.</span></span>

 

 




