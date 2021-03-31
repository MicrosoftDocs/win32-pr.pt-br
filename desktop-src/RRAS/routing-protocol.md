---
title: Protocolo de roteamento
description: Um protocolo de roteamento é um tipo de cliente que registra com o Gerenciador de tabela de roteamento. Os roteadores usam protocolos de roteamento para trocar informações relacionadas a rotas para um destino.
ms.assetid: 957ec896-94e3-4bdb-801a-12b861460fff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e64d12912494d0d6c20f484eba588b47670a808
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005423"
---
# <a name="routing-protocol"></a><span data-ttu-id="c532c-104">Protocolo de roteamento</span><span class="sxs-lookup"><span data-stu-id="c532c-104">Routing Protocol</span></span>

<span data-ttu-id="c532c-105">Um protocolo de roteamento é um tipo de cliente que registra com o Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="c532c-105">A routing protocol is a type of client that registers with the routing table manager.</span></span> <span data-ttu-id="c532c-106">Os roteadores usam protocolos de roteamento para trocar informações relacionadas a rotas para um destino.</span><span class="sxs-lookup"><span data-stu-id="c532c-106">Routers use routing protocols to exchange information regarding routes to a destination.</span></span>

<span data-ttu-id="c532c-107">Os protocolos de roteamento são unicast ou multicast.</span><span class="sxs-lookup"><span data-stu-id="c532c-107">Routing protocols are either unicast or multicast.</span></span> <span data-ttu-id="c532c-108">Os protocolos de roteamento anunciam rotas para um destino.</span><span class="sxs-lookup"><span data-stu-id="c532c-108">Routing protocols advertise routes to a destination.</span></span>

<span data-ttu-id="c532c-109">Uma rota unicast para um destino é usada por um protocolo de Roteamento unicast para encaminhar dados unicast para esse destino.</span><span class="sxs-lookup"><span data-stu-id="c532c-109">A unicast route to a destination is used by a unicast routing protocol to forward unicast data to that destination.</span></span> <span data-ttu-id="c532c-110">Os exemplos de protocolos de Roteamento unicast incluem: RIP (Routing Information Protocol), Open Shortest Path First (OSPF) e Border Gateway Protocol (BGP).</span><span class="sxs-lookup"><span data-stu-id="c532c-110">Examples of unicast routing protocols include: Routing Information Protocol (RIP), Open Shortest Path First (OSPF), and Border Gateway Protocol (BGP).</span></span>

<span data-ttu-id="c532c-111">Uma rota de multicast para um destino é usada por alguns protocolos de roteamento multicast para criar as informações que são usadas para encaminhar dados multicast de hosts na rede de destino da rota (conhecida como encaminhamento de caminho reverso). Exemplos de protocolos de roteamento multicast incluem: MOSPF (multicast Open Shortest Path First), DVMRP (protocolo de roteamento multicast de vetor de distância) e PIM (multicast independente de protocolo).</span><span class="sxs-lookup"><span data-stu-id="c532c-111">A multicast route to a destination is used by some multicast routing protocols to create the information that is used to forward multicast data from hosts on the destination network of the route (known as reverse path forwarding).Examples of multicast routing protocols include: Multicast Open Shortest Path First (MOSPF), Distance Vector Multicast Routing Protocol (DVMRP), and Protocol Independent Multicast (PIM).</span></span>

<span data-ttu-id="c532c-112">O Gerenciador de tabela de roteamento dá suporte a várias instâncias do mesmo protocolo (como a implementação da Microsoft do OSPF e de um OSPF de terceiros) em execução no roteador.</span><span class="sxs-lookup"><span data-stu-id="c532c-112">The routing table manager supports multiple instances of the same protocol (such as Microsoft's implementation of OSPF and a third-party OSPF) running on the router.</span></span> <span data-ttu-id="c532c-113">Isso permite que os roteadores usem os diferentes recursos de cada versão.</span><span class="sxs-lookup"><span data-stu-id="c532c-113">This allows routers to use the different capabilities of each version.</span></span> <span data-ttu-id="c532c-114">Esses protocolos têm identificadores de protocolo diferentes.</span><span class="sxs-lookup"><span data-stu-id="c532c-114">These protocols have different protocol identifiers.</span></span>

<span data-ttu-id="c532c-115">Os identificadores de protocolo são compostos por um identificador de fornecedor e um identificador específico de protocolo.</span><span class="sxs-lookup"><span data-stu-id="c532c-115">Protocol identifiers are comprised of a vendor identifier and a protocol-specific identifier.</span></span> <span data-ttu-id="c532c-116">O identificador específico do protocolo é o mesmo para diferentes implementações do protocolo, como a implementação da Microsoft do OSPF e uma implementação de terceiros do OSPF.</span><span class="sxs-lookup"><span data-stu-id="c532c-116">The protocol-specific identifier is the same for different implementations of the protocol, such as Microsoft's implementation of OSPF and a third-party implementation of OSPF.</span></span> <span data-ttu-id="c532c-117">Somente quando os identificadores específicos do fornecedor e do protocolo são combinados há um identificador exclusivo para um protocolo de roteamento.</span><span class="sxs-lookup"><span data-stu-id="c532c-117">Only when the vendor and protocol-specific identifiers are combined is there a unique identifier for a routing protocol.</span></span>

<span data-ttu-id="c532c-118">Um protocolo com o mesmo identificador de protocolo (ou seja, o mesmo identificador de fornecedor e de protocolo específico) pode se registrar com o Gerenciador de tabela de roteamento várias vezes.</span><span class="sxs-lookup"><span data-stu-id="c532c-118">A protocol with the same protocol identifier (that is, the same vendor identifier and protocol-specific identifier) can register with the routing table manager multiple times.</span></span> <span data-ttu-id="c532c-119">A cada vez, o protocolo registra usando um identificador de instância de protocolo diferente.</span><span class="sxs-lookup"><span data-stu-id="c532c-119">Each time, the protocol registers using a different protocol instance identifier.</span></span> <span data-ttu-id="c532c-120">Por exemplo, uma implementação do OSPF de um determinado fornecedor pode se registrar como fornecedor-OSPF-1 e fornecedor-OSPF-2.</span><span class="sxs-lookup"><span data-stu-id="c532c-120">For example, an implementation of OSPF from a particular vendor can register as Vendor-OSPF-1 and Vendor-OSPF-2.</span></span> <span data-ttu-id="c532c-121">Isso permite que uma implementação de protocolo específica particione as informações que ele mantém na tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="c532c-121">This enables a specific protocol implementation to partition the information that it keeps in the routing table.</span></span>

 

 




