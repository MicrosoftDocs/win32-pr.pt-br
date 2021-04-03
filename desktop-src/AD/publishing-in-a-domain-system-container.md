---
title: Publicando em um contêiner do sistema de domínio
description: O contêiner do sistema de uma partição de domínio contém informações operacionais por domínio.
ms.assetid: 18bb3409-774e-42d9-8f27-6c582d74ca86
ms.tgt_platform: multiple
keywords:
- Publicando em um contêiner do sistema de domínio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf7d1febd91e3540c7bc2002a36d33346820344
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822255"
---
# <a name="publishing-in-a-domain-system-container"></a><span data-ttu-id="af0f1-104">Publicando em um contêiner do sistema de domínio</span><span class="sxs-lookup"><span data-stu-id="af0f1-104">Publishing in a Domain System Container</span></span>

<span data-ttu-id="af0f1-105">O contêiner do sistema de uma partição de domínio contém informações operacionais por domínio.</span><span class="sxs-lookup"><span data-stu-id="af0f1-105">The System container of a domain partition holds per-domain operational information.</span></span> <span data-ttu-id="af0f1-106">Isso inclui a política de segurança local padrão, rastreamento de link de arquivo, reuniões de rede e contêineres para pontos de conexão de RnR (registro e resolução do Windows Sockets) e serviço de nome RPC (RpcNs).</span><span class="sxs-lookup"><span data-stu-id="af0f1-106">This includes the default local security policy, file link tracking, network meetings, and containers for Windows Sockets registration and resolution (RnR) and RPC name service (RpcNs) connection points.</span></span> <span data-ttu-id="af0f1-107">O contêiner do sistema está oculto, por padrão, e fornece um local conveniente para armazenar objetos de interesse para os administradores, mas não para os usuários finais.</span><span class="sxs-lookup"><span data-stu-id="af0f1-107">The system container is hidden, by default, and provides a convenient place for storing objects that are of interest to administrators, but not to end users.</span></span>

<span data-ttu-id="af0f1-108">Os serviços que não estão vinculados a um único host podem querer criar seus SCPs no contêiner do sistema de uma partição de domínio.</span><span class="sxs-lookup"><span data-stu-id="af0f1-108">Services that are not tied to a single host may want to create their SCPs under the System container of a domain partition.</span></span> <span data-ttu-id="af0f1-109">Essa alternativa pode ser útil para serviços com réplicas instaladas em vários hosts, cada réplica fornecendo serviços idênticos aos clientes em todo o domínio.</span><span class="sxs-lookup"><span data-stu-id="af0f1-109">This alternative can be useful for services with replicas installed on multiple hosts, each replica providing identical services to clients throughout the domain.</span></span> <span data-ttu-id="af0f1-110">Ele permite agrupar todos os objetos para o serviço replicado em um único contêiner.</span><span class="sxs-lookup"><span data-stu-id="af0f1-110">It enables you to group all the objects for the replicated service under a single container.</span></span>

<span data-ttu-id="af0f1-111">Os serviços que criam objetos específicos do serviço no contêiner do sistema devem fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="af0f1-111">Services that create service-specific objects in the System container must do the following:</span></span>

1.  <span data-ttu-id="af0f1-112">Crie um subcontêiner do **contêiner** da classe de objeto como um filho imediato do contêiner do sistema.</span><span class="sxs-lookup"><span data-stu-id="af0f1-112">Create a sub-container of object class **container** as an immediate child of the System container.</span></span> <span data-ttu-id="af0f1-113">Dê a esse subcontêiner um nome que o identifique claramente como pertencente ao serviço.</span><span class="sxs-lookup"><span data-stu-id="af0f1-113">Give this sub-container a name that clearly identifies it as pertaining to the service.</span></span>
2.  <span data-ttu-id="af0f1-114">Crie os objetos relacionados ao serviço nesse subcontêiner.</span><span class="sxs-lookup"><span data-stu-id="af0f1-114">Create the service-related objects in this sub-container.</span></span> <span data-ttu-id="af0f1-115">Por exemplo, o NetMeeting usa o contêiner de reuniões para publicar objetos de reunião de rede.</span><span class="sxs-lookup"><span data-stu-id="af0f1-115">For example, NetMeeting uses the Meetings container to publish network meeting objects.</span></span>

<span data-ttu-id="af0f1-116">Um fornecedor com vários produtos pode usar uma estratégia semelhante para agrupar objetos relacionados ao serviço para todos os seus produtos.</span><span class="sxs-lookup"><span data-stu-id="af0f1-116">A vendor with multiple products can use a similar strategy to group service-related objects for all of its products.</span></span> <span data-ttu-id="af0f1-117">Nesse caso, você pode criar um objeto de **contêiner** com um nome que identifique claramente o fornecedor; em seguida, crie objetos de **contêiner** para cada serviço como filhos do contêiner do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="af0f1-117">In this case, you could create a **container** object with a name that clearly identifies the vendor; then create **container** objects for each service as children of the vendor container.</span></span> <span data-ttu-id="af0f1-118">Crie o contêiner específico do fornecedor como um filho do contêiner do sistema.</span><span class="sxs-lookup"><span data-stu-id="af0f1-118">Create the vendor-specific container as a child of the System container.</span></span>

 

 




