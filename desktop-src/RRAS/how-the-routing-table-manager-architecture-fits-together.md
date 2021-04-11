---
title: Como a arquitetura do Gerenciador de tabela de roteamento se encaixa
description: A ilustração a seguir mostra a relação entre os diferentes componentes de um roteador.
ms.assetid: 862566ce-47c4-424a-84c2-99f4c92efcc0
keywords:
- RTM, arquitetura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc36c339ac89f01d5ba14c00857b3ced9c29414c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292877"
---
# <a name="how-the-routing-table-manager-architecture-fits-together"></a><span data-ttu-id="3ede1-104">Como a arquitetura do Gerenciador de tabela de roteamento se encaixa</span><span class="sxs-lookup"><span data-stu-id="3ede1-104">How the Routing Table Manager Architecture Fits Together</span></span>

<span data-ttu-id="3ede1-105">A ilustração a seguir mostra a relação entre os diferentes componentes de um roteador.</span><span class="sxs-lookup"><span data-stu-id="3ede1-105">The following illustration shows the relationship between the different components of a router.</span></span>

![relação entre os componentes do roteador](images/rtsrvarch.png)

<span data-ttu-id="3ede1-107">Quando o roteador é inicializado, o serviço Gerenciador de roteadores é iniciado, bem como um ou mais protocolos de roteamento.</span><span class="sxs-lookup"><span data-stu-id="3ede1-107">When the router is bootstrapped, the router manager service is started, as well as one or more routing protocols.</span></span> <span data-ttu-id="3ede1-108">Os protocolos de roteamento são associados às várias interfaces no roteador.</span><span class="sxs-lookup"><span data-stu-id="3ede1-108">Routing protocols are associated with the various interfaces on the router.</span></span> <span data-ttu-id="3ede1-109">O Gerenciador de roteador também inicia o Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="3ede1-109">The router manager also starts the routing table manager.</span></span>

<span data-ttu-id="3ede1-110">A ilustração a seguir mostra a relação entre clientes e os diferentes componentes do Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="3ede1-110">The following illustration shows the relationship between clients and the different components of the routing table manager.</span></span>

![relação entre clientes e componentes do Gerenciador de tabela de roteamento](images/rtmentrel.png)

<span data-ttu-id="3ede1-112">O Gerenciador de roteadores inicia uma ou mais instâncias do Gerenciador de tabelas de roteamento.</span><span class="sxs-lookup"><span data-stu-id="3ede1-112">The router manager starts one or more instances of the routing table manager.</span></span> <span data-ttu-id="3ede1-113">Quando várias instâncias do Gerenciador de tabela de roteamento são iniciadas, o roteador foi configurado para atuar como um ou mais roteadores virtuais.</span><span class="sxs-lookup"><span data-stu-id="3ede1-113">When multiple instances of the routing table manager are started, the router has been configured to act as one or more virtual routers.</span></span> <span data-ttu-id="3ede1-114">Cada instância do Gerenciador de tabela de roteamento possui uma ou mais interfaces; cada interface só pode pertencer a uma instância do Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="3ede1-114">Each instance of the routing table manager owns one or more interfaces; each interface can only be owned by one instance of the routing table manager.</span></span>

<span data-ttu-id="3ede1-115">Cada instância do Gerenciador de tabela de roteamento é independente das outras; nenhuma informação é trocada entre as instâncias.</span><span class="sxs-lookup"><span data-stu-id="3ede1-115">Each instance of the routing table manager is independent from the others; no information is exchanged between the instances.</span></span>

<span data-ttu-id="3ede1-116">Cada instância do Gerenciador de tabela de roteamento contém uma ou mais tabelas de roteamento.</span><span class="sxs-lookup"><span data-stu-id="3ede1-116">Each instance of the routing table manager contains one or more routing tables.</span></span> <span data-ttu-id="3ede1-117">Cada tabela de roteamento é associada a uma família de endereços.</span><span class="sxs-lookup"><span data-stu-id="3ede1-117">Each routing table is associated with an address family.</span></span>

<span data-ttu-id="3ede1-118">Cada tabela de roteamento contém uma ou mais exibições.</span><span class="sxs-lookup"><span data-stu-id="3ede1-118">Each routing table contains one or more views.</span></span> <span data-ttu-id="3ede1-119">Neste exemplo, a tabela de roteamento é mostrada com uma exibição unicast e multicast.</span><span class="sxs-lookup"><span data-stu-id="3ede1-119">In this example, the routing table is shown with a unicast and multicast view.</span></span> <span data-ttu-id="3ede1-120">Cada exibição é um subconjunto da tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="3ede1-120">Each view is a subset of the routing table.</span></span>

<span data-ttu-id="3ede1-121">A ilustração a seguir mostra a relação entre clientes e várias instâncias do Gerenciador de tabela de roteamento, tabelas de roteamento e exibições.</span><span class="sxs-lookup"><span data-stu-id="3ede1-121">The following illustration shows the relationship between clients and multiple instances of the routing table manager, routing tables, and views.</span></span>

![clientes de relações, Gerenciador de tabelas de roteamento, tabelas de roteamento, exibições](images/multrtabrel.png)

<span data-ttu-id="3ede1-123">Uma instância do cliente pode ser registrada várias vezes com uma instância do Gerenciador de tabelas de roteamento — uma vez por família de endereços.</span><span class="sxs-lookup"><span data-stu-id="3ede1-123">An instance of the client can register multiple times with an instance of the routing table manager — once per address family.</span></span> <span data-ttu-id="3ede1-124">Um cliente pode se registrar em cada instância do Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="3ede1-124">A client can register with each instance of the routing table manager.</span></span>

<span data-ttu-id="3ede1-125">A ilustração a seguir mostra como as entradas da tabela de roteamento estão relacionadas.</span><span class="sxs-lookup"><span data-stu-id="3ede1-125">The following illustration shows how the routing table entries are related.</span></span> <span data-ttu-id="3ede1-126">Para obter mais informações sobre as entradas da tabela de roteamento, consulte [entradas da tabela de roteamento](routing-table-entries.md).</span><span class="sxs-lookup"><span data-stu-id="3ede1-126">For more information on routing table entries, see [Routing Table Entries](routing-table-entries.md).</span></span>

![relação entre entradas da tabela de roteamento](images/nexthop.png)

<span data-ttu-id="3ede1-128">A tabela de roteamento contém destinos.</span><span class="sxs-lookup"><span data-stu-id="3ede1-128">The routing table contains destinations.</span></span> <span data-ttu-id="3ede1-129">Cada destino está relacionado a uma ou mais rotas.</span><span class="sxs-lookup"><span data-stu-id="3ede1-129">Each destination is related to one or more routes.</span></span> <span data-ttu-id="3ede1-130">Cada rota tem zero, um ou mais ponteiros para os próximos saltos associados à rota.</span><span class="sxs-lookup"><span data-stu-id="3ede1-130">Each route has zero, one, or more pointers to next hops that are associated with the route.</span></span> <span data-ttu-id="3ede1-131">Cada ponteiro refere-se ao próximo salto real na lista de próximos saltos.</span><span class="sxs-lookup"><span data-stu-id="3ede1-131">Each pointer refers to the actual next hop in the list of next hops.</span></span> <span data-ttu-id="3ede1-132">Cada cliente que se registra com o Gerenciador de tabela de roteamento cria uma lista dos próximos saltos que o cliente possui.</span><span class="sxs-lookup"><span data-stu-id="3ede1-132">Each client that registers with the routing table manager creates a list of next hops that the client owns.</span></span>

<span data-ttu-id="3ede1-133">As rotas só podem conter ponteiros para a lista de próximo salto associada ao cliente que possui a rota.</span><span class="sxs-lookup"><span data-stu-id="3ede1-133">Routes can only contain pointers to the next-hop list associated with the client that owns the route.</span></span>

 

 




