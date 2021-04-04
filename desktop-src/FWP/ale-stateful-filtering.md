---
title: Filtragem de estado de ALE
description: Os filtros instalados nas camadas de aplicação da camada de aplicativo (EPA) da Windows Filtering Platform (WFP) executam a filtragem de rede com estado.
ms.assetid: d5a3fcad-d55e-4a07-af21-cb40e5e9a9ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30cc1b4a5830efd0fef6dc28c88db85cd9c88cca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007545"
---
# <a name="ale-stateful-filtering"></a><span data-ttu-id="ac480-103">Filtragem de estado de ALE</span><span class="sxs-lookup"><span data-stu-id="ac480-103">ALE Stateful Filtering</span></span>

<span data-ttu-id="ac480-104">Os filtros instalados nas camadas de aplicação da camada de aplicativo (EPA) da Windows Filtering Platform (WFP) executam a filtragem de rede com estado.</span><span class="sxs-lookup"><span data-stu-id="ac480-104">Filters installed at the Application Layer Enforcement (ALE) layers of the Windows Filtering Platform (WFP) perform stateful network filtering.</span></span> <span data-ttu-id="ac480-105">Um *fluxo Ale* é usado como a base para a filtragem de estado da Ale.</span><span class="sxs-lookup"><span data-stu-id="ac480-105">An *ALE flow* is used as the basis for ALE stateful filtering.</span></span>

<span data-ttu-id="ac480-106">Um fluxo ALE é uma maneira de classificar o tráfego de rede agrupando-o com base em um endereço IP de origem, um endereço IP de destino, uma porta de origem, uma porta de destino e um protocolo.</span><span class="sxs-lookup"><span data-stu-id="ac480-106">An ALE flow is a way of classifying network traffic by grouping it based on a Source IP Address, a Destination IP Address, a Source Port, a Destination Port, and a Protocol.</span></span> <span data-ttu-id="ac480-107">Um fluxo ALE poderia ser genérico, ou seja, um ou mais dos descritores poderiam corresponder a tudo (ou curinga \* ).</span><span class="sxs-lookup"><span data-stu-id="ac480-107">An ALE flow could be generic, that is one or more of the descriptors could be matching everything (or wildcard \*).</span></span> <span data-ttu-id="ac480-108">Por exemplo, um fluxo de EPA de UDP genérico seria descrito como endereço IP de origem = \* , endereço IP \* de destino =, porta de origem = \* , porta de destino = \* e protocolo = UDP.</span><span class="sxs-lookup"><span data-stu-id="ac480-108">For example, a generic UDP ALE flow would be described as Source IP Address = \*, Destination IP Address = \*, Source Port = \*, Destination Port = \*, and Protocol = UDP.</span></span>

<span data-ttu-id="ac480-109">Depois que uma conexão é autorizada (as conexões de entrada são autorizadas na camada [**FWPM \_ camada de \_ autenticação Ale de \_ \_ recepção \_ aceitação \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) e conexões de saída na camada **FWPM da \_ autenticação Ale de camadas do \_ \_ \_ \_ AMV {4 \| 6}** ), um fluxo Ale é criado de modo que o bloqueio de uma alteração de política, todos os pacotes, entrada e saída, que pertencem ao mesmo fluxo</span><span class="sxs-lookup"><span data-stu-id="ac480-109">Once a connection is authorized (inbound connections are authorized at the [**FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer and outbound connections at the **FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}** layer), an ALE flow is created such that, barring a policy change, all packets, inbound and outbound, that belong to the same ALE flow are permitted automatically.</span></span> <span data-ttu-id="ac480-110">Como uma alteração de política pode exigir o bloqueio de conexões anteriormente permitidas, os fluxos ALE precisam ser [reautorizados](ale-re-authorization.md) quando ocorre uma alteração de política.</span><span class="sxs-lookup"><span data-stu-id="ac480-110">Because a policy change might require blocking previously allowed connections, ALE flows need to be [reauthorized](ale-re-authorization.md) when a policy change occurs.</span></span>

<span data-ttu-id="ac480-111">A filtragem de estado da ALE reduz drasticamente o número de classificações necessárias classificando apenas o primeiro pacote que pertence a um fluxo ALE.</span><span class="sxs-lookup"><span data-stu-id="ac480-111">ALE stateful filtering reduces drastically the number of required classifications by classifying only the first packet that belongs to an ALE flow.</span></span> <span data-ttu-id="ac480-112">Por comparação, a filtragem sem monitoração de Estado requer a classificação de cada pacote que atravessa a rede.</span><span class="sxs-lookup"><span data-stu-id="ac480-112">By comparison, non-stateful filtering requires classification of every packet that traverse the network.</span></span>

<span data-ttu-id="ac480-113">Um fluxo ALE tem uma direção associada, que é a direção do primeiro pacote do fluxo.</span><span class="sxs-lookup"><span data-stu-id="ac480-113">An ALE flow has an associated direction, which is the direction of the first packet of the flow.</span></span> <span data-ttu-id="ac480-114">Isso permite políticas mais flexíveis, permitindo que conexões iniciadas de entrada tenham políticas diferentes de conexões iniciadas de saída.</span><span class="sxs-lookup"><span data-stu-id="ac480-114">This allows for more flexible policies, by permitting inbound initiated connections to have different policies from outbound initiated connections.</span></span>

## <a name="tcp-ale-flow"></a><span data-ttu-id="ac480-115">Fluxo de ALE TCP</span><span class="sxs-lookup"><span data-stu-id="ac480-115">TCP ALE Flow</span></span>

<span data-ttu-id="ac480-116">Um fluxo ALE para tráfego TCP é identificado por cinco tuplas de TCP/IP (endereço IP de origem, endereço IP de destino, porta de origem, porta de destino e protocolo).</span><span class="sxs-lookup"><span data-stu-id="ac480-116">An ALE flow for TCP traffic is identified by the five-tuple of TCP/IP (Source IP Address, Destination IP Address, Source Port, Destination Port, and Protocol).</span></span>

<span data-ttu-id="ac480-117">Um fluxo ALE TCP tem o mesmo tempo de vida que um soquete TCP conectado.</span><span class="sxs-lookup"><span data-stu-id="ac480-117">A TCP ALE flow has the same lifetime as a connected TCP socket.</span></span> <span data-ttu-id="ac480-118">Um soquete TCP conectado pode ser um soquete criado usando [**Connect ()**](/windows/desktop/api/winsock2/nf-winsock2-connect) ou um soquete criado como resultado de uma chamada [**Accept ()**](/windows/desktop/api/winsock2/nf-winsock2-accept) .</span><span class="sxs-lookup"><span data-stu-id="ac480-118">A connected TCP socket could be either a socket created using [**connect()**](/windows/desktop/api/winsock2/nf-winsock2-connect) or a socket created as a result of an [**accept()**](/windows/desktop/api/winsock2/nf-winsock2-accept) call.</span></span>

<span data-ttu-id="ac480-119">A EPA mantém uma relação um-para-um entre um fluxo de TCP ALE e um bloco de controle TCP (TCB).</span><span class="sxs-lookup"><span data-stu-id="ac480-119">ALE maintains a one-to-one relationship between a TCP ALE flow and a TCP Control Block (TCB).</span></span>

## <a name="udp-ale-flow"></a><span data-ttu-id="ac480-120">Fluxo de ALE UDP</span><span class="sxs-lookup"><span data-stu-id="ac480-120">UDP ALE Flow</span></span>

> [!Note]  
> <span data-ttu-id="ac480-121">Protocolos que não são TCP ou ICMP são tratados como UDP.</span><span class="sxs-lookup"><span data-stu-id="ac480-121">Protocols that are not TCP or ICMP are treated like UDP.</span></span>

 

<span data-ttu-id="ac480-122">Um fluxo ALE para o tráfego UDP é identificado por cinco tuplas de TCP/IP (endereço IP de origem, endereço IP de destino, porta de origem, porta de destino e protocolo).</span><span class="sxs-lookup"><span data-stu-id="ac480-122">An ALE flow for UDP traffic is identified by the five-tuple of TCP/IP (Source IP Address, Destination IP Address, Source Port, Destination Port, and Protocol).</span></span>

<span data-ttu-id="ac480-123">Um fluxo de ALE UDP é criado com base em um soquete UDP e representa o ponto remoto com o qual o aplicativo está se comunicando.</span><span class="sxs-lookup"><span data-stu-id="ac480-123">A UDP ALE flow is created based on a UDP socket and it represents the remote peer that the application is communicating with.</span></span> <span data-ttu-id="ac480-124">Um par remoto é identificado por uma tupla (endereço IP de destino e porta de destino).</span><span class="sxs-lookup"><span data-stu-id="ac480-124">A remote peer is identified by a (Destination IP Address and Destination Port) tuple.</span></span>

<span data-ttu-id="ac480-125">Há uma relação um-para-muitos entre um soquete UDP e os pares remotos aos quais ele se comunica.</span><span class="sxs-lookup"><span data-stu-id="ac480-125">There is a one-to-many relationship between a UDP socket and the remote peers that it talks to.</span></span>

<span data-ttu-id="ac480-126">Quando o soquete UDP local for fechado, todos os fluxos ALE associados a ele serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="ac480-126">When the local UDP socket is closed, all the ALE flows associated with it will be deleted.</span></span>

<span data-ttu-id="ac480-127">Na ausência de fechamentos de soquete, os fluxos ALE de unicast UDP têm um tempo limite de ociosidade [configurável](ale-flow-customization.md) que usa por padrão 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="ac480-127">In the absence of socket closures, UDP unicast ALE flows have a [configurable](ale-flow-customization.md) idle timeout that defaults to 60 seconds.</span></span> <span data-ttu-id="ac480-128">Se nenhum pacote for enviado ou recebido nessa janela, o fluxo ALE será excluído.</span><span class="sxs-lookup"><span data-stu-id="ac480-128">If no packets are sent or received within this window, the ALE flow will be deleted.</span></span> <span data-ttu-id="ac480-129">Esse tempo limite padrão é progressivamente reduzido quando o número de fluxos ALE em todo o sistema atinge um determinado limite.</span><span class="sxs-lookup"><span data-stu-id="ac480-129">This default timeout is progressively shortened when the number of ALE flows system-wide reaches a certain threshold.</span></span>

## <a name="icmp-ale-flow"></a><span data-ttu-id="ac480-130">Fluxo de ALE ICMP</span><span class="sxs-lookup"><span data-stu-id="ac480-130">ICMP ALE Flow</span></span>

<span data-ttu-id="ac480-131">Um fluxo ALE para tráfego ICMP é identificado por seis tuplas (endereço IP de origem, endereço IP de destino, tipo de ICMP, código ICMP, protocolo e ID de ICMP).</span><span class="sxs-lookup"><span data-stu-id="ac480-131">An ALE flow for ICMP traffic is identified by the six-tuple (Source IP Address, Destination IP Address, ICMP type, ICMP code, Protocol, and ICMP ID).</span></span> <span data-ttu-id="ac480-132">A ID de ICMP faz parte do fluxo de ALE somente para o tráfego de eco/resposta ICMP.</span><span class="sxs-lookup"><span data-stu-id="ac480-132">The ICMP ID is part of the ALE flow only for ICMP echo/reply traffic.</span></span>

<span data-ttu-id="ac480-133">Na ausência de fechamentos de soquete, os fluxos ALE de unicast ICMP têm um tempo limite de ociosidade [configurável](ale-flow-customization.md) cujo padrão é de 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="ac480-133">In the absence of socket closures, ICMP unicast ALE flows have a [configurable](ale-flow-customization.md) idle timeout that defaults to 60 seconds.</span></span> <span data-ttu-id="ac480-134">Se nenhum pacote for enviado ou recebido nessa janela, o fluxo ALE será excluído.</span><span class="sxs-lookup"><span data-stu-id="ac480-134">If no packets are sent or received within this window, the ALE flow will be deleted.</span></span> <span data-ttu-id="ac480-135">Esse tempo limite padrão é progressivamente reduzido quando o número de fluxos ALE em todo o sistema atinge um determinado limite.</span><span class="sxs-lookup"><span data-stu-id="ac480-135">This default timeout is progressively shortened when the number of ALE flows system-wide reaches a certain threshold.</span></span>

<span data-ttu-id="ac480-136">Somente as mensagens ICMP que não são de erro são indicadas para camadas ALE.</span><span class="sxs-lookup"><span data-stu-id="ac480-136">Only ICMP non-error messages are indicated to ALE layers.</span></span> <span data-ttu-id="ac480-137">Mensagens de erro ICMP podem ser inspecionadas em \_ camadas de erro ICMP.</span><span class="sxs-lookup"><span data-stu-id="ac480-137">ICMP error messages can be inspected at ICMP\_ERROR layers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac480-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ac480-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac480-139">Aplicação da camada de aplicativo (EPA)</span><span class="sxs-lookup"><span data-stu-id="ac480-139">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="ac480-140">Camadas ALE</span><span class="sxs-lookup"><span data-stu-id="ac480-140">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="ac480-141">Tráfego de difusão/multicast ALE</span><span class="sxs-lookup"><span data-stu-id="ac480-141">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="ac480-142">Reautorização de ALE</span><span class="sxs-lookup"><span data-stu-id="ac480-142">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="ac480-143">Personalização de fluxo ALE</span><span class="sxs-lookup"><span data-stu-id="ac480-143">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> <dt>

[<span data-ttu-id="ac480-144">Fluxos de pacotes TCP</span><span class="sxs-lookup"><span data-stu-id="ac480-144">TCP Packet Flows</span></span>](tcp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="ac480-145">Fluxos de pacotes UDP</span><span class="sxs-lookup"><span data-stu-id="ac480-145">UDP Packet Flows</span></span>](udp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="ac480-146">Funções do Winsock</span><span class="sxs-lookup"><span data-stu-id="ac480-146">Winsock Functions</span></span>](/windows/desktop/WinSock/winsock-functions)
</dt> </dl>

 

 