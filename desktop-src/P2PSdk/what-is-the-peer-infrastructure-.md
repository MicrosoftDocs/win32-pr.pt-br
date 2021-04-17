---
description: A infraestrutura de pares é um conjunto de várias APIs que são poderosas e flexíveis.
ms.assetid: aed7585a-88e5-4ca3-a8c3-e2ccfe13d35d
title: O que é a infraestrutura de pares?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873717b3f90497fe9ab9f50bb9c18e6f0692a4e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811304"
---
# <a name="what-is-the-peer-infrastructure"></a><span data-ttu-id="b137d-103">O que é a infraestrutura de pares?</span><span class="sxs-lookup"><span data-stu-id="b137d-103">What is the Peer Infrastructure?</span></span>

<span data-ttu-id="b137d-104">A infraestrutura de pares é um conjunto de várias APIs que são poderosas e flexíveis.</span><span class="sxs-lookup"><span data-stu-id="b137d-104">The Peer Infrastructure is a set of several APIs that are powerful and flexible.</span></span> <span data-ttu-id="b137d-105">Os principais componentes incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b137d-105">The major components include the following:</span></span>

-   [<span data-ttu-id="b137d-106">API de grafo de pares</span><span class="sxs-lookup"><span data-stu-id="b137d-106">Peer Graphing API</span></span>](#peer-graphing-api)
-   [<span data-ttu-id="b137d-107">API de agrupamento de pares</span><span class="sxs-lookup"><span data-stu-id="b137d-107">Peer Grouping API</span></span>](#peer-grouping-api)
-   [<span data-ttu-id="b137d-108">API do Gerenciador de identidade do par</span><span class="sxs-lookup"><span data-stu-id="b137d-108">Peer Identity Manager API</span></span>](#peer-identity-manager-api)
-   [<span data-ttu-id="b137d-109">API do provedor de Namespace PNRP</span><span class="sxs-lookup"><span data-stu-id="b137d-109">PNRP Namespace Provider API</span></span>](#pnrp-namespace-provider-api)

## <a name="peer-graphing-api"></a><span data-ttu-id="b137d-110">API de grafo de pares</span><span class="sxs-lookup"><span data-stu-id="b137d-110">Peer Graphing API</span></span>

<span data-ttu-id="b137d-111">A infraestrutura de pares fornece uma tecnologia de gráfico que pode passar informações de forma eficiente e confiável entre os pares de um grafo de mesmo nível.</span><span class="sxs-lookup"><span data-stu-id="b137d-111">The Peer Infrastructure provides a graphing technology that can pass information efficiently and reliably between peers in a peer graph.</span></span> <span data-ttu-id="b137d-112">A [API de grafo de pares](graphing-api.md) garante que cada nó tenha uma exibição consistente dos dados em um grafo.</span><span class="sxs-lookup"><span data-stu-id="b137d-112">The [Peer Graphing API](graphing-api.md) ensures that each node has a consistent view of the data in a graph.</span></span>

<span data-ttu-id="b137d-113">Você pode usar a [API de grafo de pares](graphing-api.md) para fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b137d-113">You can use the [Peer Graphing API](graphing-api.md) to do the following:</span></span>

-   <span data-ttu-id="b137d-114">Criar e gerenciar grafos de pares</span><span class="sxs-lookup"><span data-stu-id="b137d-114">Create and manage peer graphs</span></span>
-   <span data-ttu-id="b137d-115">Enumerar e interagir com outros pares em um grafo de mesmo nível</span><span class="sxs-lookup"><span data-stu-id="b137d-115">Enumerate and interact with other peers in a peer graph</span></span>
-   <span data-ttu-id="b137d-116">Enviar dados na forma de um [registro](records.md) para cada nó em um grafo de mesmo nível</span><span class="sxs-lookup"><span data-stu-id="b137d-116">Send data in the form of a [record](records.md) to each node in a peer graph</span></span>

## <a name="peer-grouping-api"></a><span data-ttu-id="b137d-117">API de agrupamento de pares</span><span class="sxs-lookup"><span data-stu-id="b137d-117">Peer Grouping API</span></span>

<span data-ttu-id="b137d-118">A [API de agrupamento de pares](grouping-api.md) combina e aprimora as APIs par de [PNRP](#pnrp-namespace-provider-api) e de [grafo](#peer-graphing-api) e adiciona os dois componentes a seguir:</span><span class="sxs-lookup"><span data-stu-id="b137d-118">The [Peer Grouping API](grouping-api.md) combines and enhances the Peer [PNRP](#pnrp-namespace-provider-api) and [Graphing](#peer-graphing-api) APIs, and adds the following two components:</span></span>

-   <span data-ttu-id="b137d-119">Uma camada de multiplexação que permite que vários aplicativos em execução em uma entidade de mesmo nível se conectem a um grupo</span><span class="sxs-lookup"><span data-stu-id="b137d-119">A multiplexing layer that allows multiple applications running on one peer entity to connect to a group</span></span>
-   <span data-ttu-id="b137d-120">Um modelo de segurança específico que garante que somente os colegas convidados para um grupo possam se conectar ao grupo por meio do tempo de vida do grupo</span><span class="sxs-lookup"><span data-stu-id="b137d-120">A specific security model that ensures only peers invited to a group can connect to the group through the lifetime of the group</span></span>

<span data-ttu-id="b137d-121">Você pode usar a API de agrupamento de pares para fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b137d-121">You can use the Peer Grouping API to do the following:</span></span>

-   <span data-ttu-id="b137d-122">Criar e gerenciar grupos de pares seguros</span><span class="sxs-lookup"><span data-stu-id="b137d-122">Create and manage secure peer groups</span></span>
-   <span data-ttu-id="b137d-123">Enumerar e interagir com outros pares em um grupo</span><span class="sxs-lookup"><span data-stu-id="b137d-123">Enumerate and interact with other peers in a group</span></span>
-   <span data-ttu-id="b137d-124">Enviar dados na forma de um [registro](records.md) para cada nó em um grupo de pares</span><span class="sxs-lookup"><span data-stu-id="b137d-124">Send data in the form of a [record](records.md) to each node in a peer group</span></span>

## <a name="peer-identity-manager-api"></a><span data-ttu-id="b137d-125">API do Gerenciador de identidade do par</span><span class="sxs-lookup"><span data-stu-id="b137d-125">Peer Identity Manager API</span></span>

<span data-ttu-id="b137d-126">Usando a [API do Gerenciador de identidade do par](identity-manager-api.md) , você pode criar nomes de [pares](peer-names.md) seguros que o PNRP pode usar para garantir que uma pessoa que está publicando um nome oficialmente é o nome.</span><span class="sxs-lookup"><span data-stu-id="b137d-126">By using the [Peer Identity Manager API](identity-manager-api.md) you can create secure [peer names](peer-names.md) that PNRP can use to ensure that a person publishing a name officially owns the name.</span></span> <span data-ttu-id="b137d-127">Os nomes de pares também são chamados de identidades e são usados na API de agrupamento de pares para identificar os indivíduos em um grupo.</span><span class="sxs-lookup"><span data-stu-id="b137d-127">Peer names are also called identities, and they are used in the Peer Grouping API to identify the individuals in a group.</span></span>

<span data-ttu-id="b137d-128">Você pode usar a [API do Gerenciador de identidade do par](identity-manager-api.md) para fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b137d-128">You can use the [Peer Identity Manager API](identity-manager-api.md) to do the following:</span></span>

-   <span data-ttu-id="b137d-129">Crie, enumere e gerencie identidades pares.</span><span class="sxs-lookup"><span data-stu-id="b137d-129">Create, enumerate, and manage peer identities.</span></span>

## <a name="pnrp-namespace-provider-api"></a><span data-ttu-id="b137d-130">API do provedor de Namespace PNRP</span><span class="sxs-lookup"><span data-stu-id="b137d-130">PNRP Namespace Provider API</span></span>

<span data-ttu-id="b137d-131">A infraestrutura de pares fornece uma tecnologia de resolução de nomes sem servidor chamada [API do provedor de namespace do PNRP](pnrp-namespace-provider-api.md).</span><span class="sxs-lookup"><span data-stu-id="b137d-131">The Peer Infrastructure provides a serverless name resolution technology called the [PNRP Namespace Provider API](pnrp-namespace-provider-api.md).</span></span> <span data-ttu-id="b137d-132">Usando a API do provedor de namespace do Winsock 2 PNRP, um ponto de extremidade, serviço, dispositivo de computação e ponto de extremidade do grupo de pontos pode gerenciar, registrar, cancelar o registro e resolver outro ponto de extremidade em uma [nuvem](clouds.md)PNRP.</span><span class="sxs-lookup"><span data-stu-id="b137d-132">By using the Winsock 2 PNRP Namespace Provider API, a peer, service, computing device, and peer group endpoint can manage, register, unregister, and resolve another endpoint in a PNRP [cloud](clouds.md).</span></span>

> [!Note]  
> <span data-ttu-id="b137d-133">O PNRP é um acrônimo para o **protocolo de resolução de nomes de pares**.</span><span class="sxs-lookup"><span data-stu-id="b137d-133">PNRP is an acronym for **peer name resolution protocol**.</span></span>

 

 

 



