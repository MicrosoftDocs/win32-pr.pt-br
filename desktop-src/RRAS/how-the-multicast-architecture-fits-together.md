---
title: Como a arquitetura de multicast se encaixa
description: Esta seção descreve uma configuração de exemplo e como os principais componentes se encaixam.
ms.assetid: 1fa0b343-0276-402b-8c3d-5ca114ad43cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc82178568bac01e89eb0a4d6ea9222d45e7f5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160057"
---
# <a name="how-the-multicast-architecture-fits-together"></a><span data-ttu-id="c731a-103">Como a arquitetura de multicast se encaixa</span><span class="sxs-lookup"><span data-stu-id="c731a-103">How the Multicast Architecture Fits Together</span></span>

<span data-ttu-id="c731a-104">Esta seção descreve uma configuração de exemplo e como os principais componentes se encaixam.</span><span class="sxs-lookup"><span data-stu-id="c731a-104">This section describes a sample configuration and how the major components fit together.</span></span>

<span data-ttu-id="c731a-105">A ilustração a seguir mostra a relação entre os vários componentes de um roteador.</span><span class="sxs-lookup"><span data-stu-id="c731a-105">The following illustration shows the relationship between the various components of a router.</span></span>

![relação entre componentes do roteador do Windows 2000](images/mrarch1.png)

<span data-ttu-id="c731a-107">O Gerenciador do grupo de multicast faz parte do serviço RRAS que é executado em um servidor que está operando como um roteador.</span><span class="sxs-lookup"><span data-stu-id="c731a-107">The multicast group manager is a part of the RRAS service that runs on a server that is operating as a router.</span></span>

<span data-ttu-id="c731a-108">O roteador mostrado tem três protocolos de roteamento multicast (protocolo 1, protocolo 2, protocolo 3) em execução.</span><span class="sxs-lookup"><span data-stu-id="c731a-108">The router shown has three multicast routing protocols (Protocol 1, Protocol 2, Protocol 3) running on it.</span></span> <span data-ttu-id="c731a-109">Cada protocolo pode possuir uma ou mais interfaces (nesta ilustração, o protocolo 1 possui a interface 1, o protocolo 2 possui a interface 2 e o protocolo 3 possui a interface 3).</span><span class="sxs-lookup"><span data-stu-id="c731a-109">Each protocol can own one or more interfaces (in this illustration, Protocol 1 owns Interface 1, Protocol 2 owns Interface 2, and Protocol 3 owns Interface 3).</span></span> <span data-ttu-id="c731a-110">Cada interface pode pertencer apenas a um protocolo de roteamento (além de IGMP, que é um caso especial).</span><span class="sxs-lookup"><span data-stu-id="c731a-110">Each interface can be owned by only one routing protocol (in addition to IGMP, which is a special case).</span></span>

<span data-ttu-id="c731a-111">O Gerenciador do grupo de multicast é executado no roteador e coordena a distribuição de informações de grupo entre os protocolos de roteamento.</span><span class="sxs-lookup"><span data-stu-id="c731a-111">The multicast group manager runs on the router and coordinates the distribution of group information between the routing protocols.</span></span>

<span data-ttu-id="c731a-112">A ilustração a seguir mostra a relação entre dois roteadores em uma arquitetura de multicast.</span><span class="sxs-lookup"><span data-stu-id="c731a-112">The following illustration shows the relationship between two routers in a multicast architecture.</span></span>

![relação entre dois roteadores na arquitetura de multicast](images/mrarch2.png)

<span data-ttu-id="c731a-114">Na ilustração anterior, o roteador 2 envia uma mensagem de multicast para a rede 2 na interface 3.</span><span class="sxs-lookup"><span data-stu-id="c731a-114">In the previous illustration, Router 2 sends a multicast message to Network 2 on Interface 3.</span></span> <span data-ttu-id="c731a-115">O roteador 1 recebe a mensagem de multicast da rede 2 na interface 3.</span><span class="sxs-lookup"><span data-stu-id="c731a-115">Router 1 receives the multicast message from Network 2 on Interface 3.</span></span> <span data-ttu-id="c731a-116">Em ambos os roteadores, o protocolo 3 possui a respectiva interface 3.</span><span class="sxs-lookup"><span data-stu-id="c731a-116">On both routers, Protocol 3 owns the respective Interface 3.</span></span>

<span data-ttu-id="c731a-117">A ilustração a seguir mostra o caminho em que uma mensagem de uma fonte multicast (para um grupo de multicast) leva para alcançar o host que ingressou no grupo de multicast.</span><span class="sxs-lookup"><span data-stu-id="c731a-117">The following illustration shows the path a message from a multicast source (to a multicast group) takes to reach the host that has joined the multicast group.</span></span> <span data-ttu-id="c731a-118">Os roteadores na ilustração usam a mesma configuração das ilustrações anteriores; no entanto, os detalhes da interface e do protocolo não são mostrados para manter a figura simples.</span><span class="sxs-lookup"><span data-stu-id="c731a-118">The routers in the illustration use the same configuration as previous illustrations; however, the interface and protocol details are not shown in order to keep the figure simple.</span></span>

![caminho da mensagem da origem de multicast para o host de destino](images/mrarch3.png)

<span data-ttu-id="c731a-120">O cenário a seguir descreve os eventos que ocorrem quando um host ingressa em um grupo de multicast.</span><span class="sxs-lookup"><span data-stu-id="c731a-120">The following scenario describes the events that take place when a host joins a multicast group.</span></span> <span data-ttu-id="c731a-121">Consulte a ilustração anterior para obter relações entre as várias entidades.</span><span class="sxs-lookup"><span data-stu-id="c731a-121">Refer to the previous illustration for relationships between the various entities.</span></span>

1.  <span data-ttu-id="c731a-122">O host 1 une o grupo de multicast G na rede 3.</span><span class="sxs-lookup"><span data-stu-id="c731a-122">Host 1 joins the multicast group G on Network 3.</span></span>
2.  <span data-ttu-id="c731a-123">O roteador 3 aprende sobre o G via IGMP.</span><span class="sxs-lookup"><span data-stu-id="c731a-123">Router 3 learns about G via IGMP.</span></span>
3.  <span data-ttu-id="c731a-124">O Gerenciador de grupo de multicast no roteador 3 notifica o protocolo 3 no roteador 3 de que há novos destinatários para G.</span><span class="sxs-lookup"><span data-stu-id="c731a-124">The multicast group manager on Router 3 notifies Protocol 3 on Router 3 that there are new receivers for G.</span></span>
4.  <span data-ttu-id="c731a-125">O protocolo 3 no roteador 3 notifica o protocolo 3 no roteador 1 sobre G.</span><span class="sxs-lookup"><span data-stu-id="c731a-125">Protocol 3 on Router 3 then notifies Protocol 3 on Router 1 about G.</span></span>
5.  <span data-ttu-id="c731a-126">Por sua vez, o protocolo 3 no roteador 1 notifica o Gerenciador de grupo de multicast no roteador 1 sobre G.</span><span class="sxs-lookup"><span data-stu-id="c731a-126">In turn, Protocol 3 on Router 1 notifies the multicast group manager on Router 1 about G.</span></span>
6.  <span data-ttu-id="c731a-127">O Gerenciador de grupo de multicast no roteador 1 notifica o protocolo 1 e o protocolo 2 sobre G.</span><span class="sxs-lookup"><span data-stu-id="c731a-127">The multicast group manager on Router 1 then notifies Protocol 1 and Protocol 2 about G.</span></span>
7.  <span data-ttu-id="c731a-128">O protocolo 2 pode informar ao roteador 2 sobre G, se o protocolo for projetado para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="c731a-128">Protocol 2 may inform Router 2 about G, if the protocol is designed to do so.</span></span>

<span data-ttu-id="c731a-129">O cenário a seguir descreve os eventos que ocorrem quando uma mensagem é enviada a um grupo de multicast.</span><span class="sxs-lookup"><span data-stu-id="c731a-129">The following scenario describes the events that take place when a message is sent to a multicast group.</span></span> <span data-ttu-id="c731a-130">Consulte a ilustração anterior para obter as relações entre as várias entidades.</span><span class="sxs-lookup"><span data-stu-id="c731a-130">Refer to the previous illustration for the relationships between the various entities.</span></span>

1.  <span data-ttu-id="c731a-131">Uma fonte na rede 1 envia uma mensagem para o Grupo G.</span><span class="sxs-lookup"><span data-stu-id="c731a-131">A source on Network 1 sends a message to Group G.</span></span>
2.  <span data-ttu-id="c731a-132">A mensagem enviada dos S de origem é primeiro para o roteador 2, que, em seguida, a encaminha para o roteador 1 usando a interface 2 (já que o roteador 2 foi informado pelo protocolo 2 que os receptores estão presentes no downstream).</span><span class="sxs-lookup"><span data-stu-id="c731a-132">The message sent from Source S goes first to Router 2, which then forwards it to Router 1 using Interface 2 (since Router 2 has been informed by Protocol 2 that receivers are present downstream).</span></span>
3.  <span data-ttu-id="c731a-133">O roteador 1 encaminha a mensagem para o roteador 3 (uma vez que o roteador 1 foi informado pelo protocolo 2 que os receptores estão presentes no downstream).</span><span class="sxs-lookup"><span data-stu-id="c731a-133">Router 1 forwards the message to Router 3 (since Router 1 has been informed by Protocol 2 that receivers are present downstream).</span></span>
4.  <span data-ttu-id="c731a-134">O roteador 3 encaminha a mensagem para a rede 3 e, portanto, chega no host 1.</span><span class="sxs-lookup"><span data-stu-id="c731a-134">Router 3 forwards the message to Network 3, and therefore it arrives at Host 1.</span></span>

<span data-ttu-id="c731a-135">Para obter mais informações sobre a interação do protocolo de roteamento de multicast, consulte [RFC 2715](routing-protocols-request-for-comments.md), regras de interoperabilidade para protocolos de roteamento de multicast.</span><span class="sxs-lookup"><span data-stu-id="c731a-135">For further information on multicast routing protocol interaction, see [RFC 2715](routing-protocols-request-for-comments.md), Interoperability Rules for Multicast Routing Protocols.</span></span>

 

 




