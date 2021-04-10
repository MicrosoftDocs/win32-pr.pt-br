---
title: Fluxos de pacotes UDP
description: A ordem na qual as camadas do mecanismo de filtro da WFP (Windows Filtering Platform) são percorridas durante uma sessão UDP típica.
ms.assetid: ab618c1f-3e7c-4f4b-b4ff-9e396d3258d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 790de49e971d5506c1732b9c4d30b88643c7af0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292516"
---
# <a name="udp-packet-flows"></a><span data-ttu-id="65cc1-103">Fluxos de pacotes UDP</span><span class="sxs-lookup"><span data-stu-id="65cc1-103">UDP Packet Flows</span></span>

<span data-ttu-id="65cc1-104">Esta seção descreve a ordem na qual as camadas do mecanismo de filtro da WFP (Windows Filtering Platform) são percorridas durante uma sessão UDP típica.</span><span class="sxs-lookup"><span data-stu-id="65cc1-104">This section describes the order in which the layers of the Windows Filtering Platform (WFP) filter engine are traversed during a typical UDP session.</span></span>

> [!Note]  
> <span data-ttu-id="65cc1-105">Os fluxos de pacotes UDP para IPv6 seguem o mesmo padrão que para IPv4.</span><span class="sxs-lookup"><span data-stu-id="65cc1-105">UDP packet flows for IPv6 follow the same pattern as for IPv4.</span></span>

 

> [!Note]  
> <span data-ttu-id="65cc1-106">Todos os fluxos de pacotes não TCP seguem o mesmo padrão que os fluxos de pacotes UDP.</span><span class="sxs-lookup"><span data-stu-id="65cc1-106">All non-TCP packet flows follow the same pattern as UDP packet flows.</span></span>

 

## <a name="udp-connection-establishment"></a><span data-ttu-id="65cc1-107">Estabelecimento de conexão UDP</span><span class="sxs-lookup"><span data-stu-id="65cc1-107">UDP Connection Establishment</span></span>

<dl> <span data-ttu-id="65cc1-108">O servidor (receptor) executa a abertura passiva</span><span class="sxs-lookup"><span data-stu-id="65cc1-108">Server (receiver) performs Passive Open</span></span>

-   <span data-ttu-id="65cc1-109">bind: \_ \_ \_ \_ redirecionamento de associação Ale de camada FWPM \_ (somente windows 7/Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="65cc1-109">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="65cc1-110">Associação: \_ v4 de \_ \_ atribuição de \_ recursos \_ da camada FWPM</span><span class="sxs-lookup"><span data-stu-id="65cc1-110">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>

  
<span data-ttu-id="65cc1-111">Cliente (remetente) executa active open</span><span class="sxs-lookup"><span data-stu-id="65cc1-111">Client (sender) performs Active Open</span></span>

-   <span data-ttu-id="65cc1-112">bind: \_ \_ \_ \_ redirecionamento de associação Ale de camada FWPM \_ (somente windows 7/Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="65cc1-112">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="65cc1-113">Associação: \_ v4 de \_ \_ atribuição de \_ recursos \_ da camada FWPM</span><span class="sxs-lookup"><span data-stu-id="65cc1-113">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>
-   <span data-ttu-id="65cc1-114">SendTo: \_ \_ \_ redirecionamento do FWPM da camada Ale Connect \_ \_ V4 (somente windows 7/Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="65cc1-114">sendto: FWPM\_LAYER\_ALE\_CONNECT\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="65cc1-115">SendTo: \_ conexão de \_ autenticação Ale de camada FWPM \_ \_ Connect \_ v4</span><span class="sxs-lookup"><span data-stu-id="65cc1-115">sendto: FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V4</span></span>
-   <span data-ttu-id="65cc1-116">O \_ fluxo de Ale de camada de FWPM \_ \_ \_ estabeleceu \_ v4</span><span class="sxs-lookup"><span data-stu-id="65cc1-116">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="65cc1-117">dados: \_ dados de \_ datagramas da camada FWPM \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="65cc1-117">data: FWPM\_LAYER\_DATAGRAM\_DATA\_V4</span></span>
-   <span data-ttu-id="65cc1-118">Mensagem UDP: \_ transporte de saída da camada FWPM \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="65cc1-118">UDP message: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="65cc1-119">Datagramas IP: \_ \_ \_ IPPACKET v4 de saída da camada FWPM \_</span><span class="sxs-lookup"><span data-stu-id="65cc1-119">IP datagrams: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="65cc1-120">Servidor</span><span class="sxs-lookup"><span data-stu-id="65cc1-120">Server</span></span>

-   <span data-ttu-id="65cc1-121">Datagramas IP: \_ \_ \_ IPPACKET v4 de entrada da camada FWPM \_</span><span class="sxs-lookup"><span data-stu-id="65cc1-121">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="65cc1-122">Mensagem UDP: \_ transporte de entrada da camada FWPM \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="65cc1-122">UDP message: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="65cc1-123">Mensagem UDP: \_ aceitação de \_ recepção de autenticação Ale de camada de FWPM \_ \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="65cc1-123">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="65cc1-124">O \_ fluxo de Ale de camada de FWPM \_ \_ \_ estabeleceu \_ v4</span><span class="sxs-lookup"><span data-stu-id="65cc1-124">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="65cc1-125">dados: \_ dados de \_ datagramas da camada FWPM \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="65cc1-125">data: FWPM\_LAYER\_DATAGRAM\_DATA\_V4</span></span>

  
</dl>

## <a name="udp-message-received-with-no-one-listening-on-the-port-or-protocol"></a><span data-ttu-id="65cc1-126">Mensagem UDP recebida sem escuta na porta ou no protocolo</span><span class="sxs-lookup"><span data-stu-id="65cc1-126">UDP Message Received with No One Listening on the Port or Protocol</span></span>

<span data-ttu-id="65cc1-127">Servidor (receptor)</span><span class="sxs-lookup"><span data-stu-id="65cc1-127">Server (receiver)</span></span>

-   <span data-ttu-id="65cc1-128">Datagramas IP: \_ \_ \_ IPPACKET v4 de entrada da camada FWPM \_</span><span class="sxs-lookup"><span data-stu-id="65cc1-128">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="65cc1-129">Datagramas IP: \_ \_ \_ descarte de IPPACKET \_ v4 \_ de entrada na camada FWPM</span><span class="sxs-lookup"><span data-stu-id="65cc1-129">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4\_DISCARD</span></span>
-   <span data-ttu-id="65cc1-130">Destino ICMP inacessível: erro de \_ ICMP de saída de camada FWPM \_ \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="65cc1-130">ICMP Dest Unreachable: FWPM\_LAYER\_OUTBOUND\_ICMP\_ERROR\_V4</span></span>
-   <span data-ttu-id="65cc1-131">Destino ICMP inacessível: transporte de \_ saída de camada FWPM \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="65cc1-131">ICMP Dest Unreachable: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="65cc1-132">Destino ICMP inacessível: IPPACKET de \_ saída da camada FWPM \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="65cc1-132">ICMP Dest Unreachable: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

> [!Note]  
> <span data-ttu-id="65cc1-133">O UDP sem nenhum ponto de extremidade é indicado em descartar IPPACKET com uma condição de erro específica.</span><span class="sxs-lookup"><span data-stu-id="65cc1-133">UDP with no endpoint is indicated at IPPACKET discard with a specific error condition.</span></span> <span data-ttu-id="65cc1-134">Bloqueie esse pacote em IPPACKET descarte para fazer com que a pilha não envie o evento correspondente (erro de ICMP).</span><span class="sxs-lookup"><span data-stu-id="65cc1-134">Block this packet at IPPACKET discard to cause the stack not to send the corresponding event (ICMP error).</span></span>

 

## <a name="successful-reauthorization-of-a-udp-packet"></a><span data-ttu-id="65cc1-135">Reautorização bem-sucedida de um pacote UDP</span><span class="sxs-lookup"><span data-stu-id="65cc1-135">Successful Reauthorization of a UDP Packet</span></span>

<span data-ttu-id="65cc1-136">Servidor (receptor)</span><span class="sxs-lookup"><span data-stu-id="65cc1-136">Server (receiver)</span></span>

-   <span data-ttu-id="65cc1-137">Datagramas IP: \_ \_ \_ IPPACKET v4 de entrada da camada FWPM \_</span><span class="sxs-lookup"><span data-stu-id="65cc1-137">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="65cc1-138">Mensagem UDP: \_ transporte de entrada da camada FWPM \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="65cc1-138">UDP message: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="65cc1-139">Mensagem UDP: \_ aceitação de \_ recepção de autenticação Ale de camada de FWPM \_ \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="65cc1-139">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="65cc1-140">Mensagem UDP: \_ \_ datagrama de camada de FWPM \_ Data \_ V4 (entrada)</span><span class="sxs-lookup"><span data-stu-id="65cc1-140">UDP message: FWPM\_LAYER\_DATAGRAM\_DATA\_V4(INBOUND)</span></span>

## <a name="failed-reauthorization-of-a-udp-packet"></a><span data-ttu-id="65cc1-141">Falha na Reautorização de um pacote UDP</span><span class="sxs-lookup"><span data-stu-id="65cc1-141">Failed Reauthorization of a UDP Packet</span></span>

<span data-ttu-id="65cc1-142">Servidor (receptor)</span><span class="sxs-lookup"><span data-stu-id="65cc1-142">Server (receiver)</span></span>

-   <span data-ttu-id="65cc1-143">Datagramas IP: \_ \_ \_ IPPACKET v4 de entrada da camada FWPM \_</span><span class="sxs-lookup"><span data-stu-id="65cc1-143">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="65cc1-144">Mensagem UDP: \_ transporte de entrada da camada FWPM \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="65cc1-144">UDP message: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="65cc1-145">Mensagem UDP: \_ aceitação de \_ recepção de autenticação Ale de camada de FWPM \_ \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="65cc1-145">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="65cc1-146">Mensagem UDP: FWPM \_ camada \_ de \_ autenticação Ale AUT \_ \_ aceitar \_ \_ descarta v4</span><span class="sxs-lookup"><span data-stu-id="65cc1-146">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4\_DISCARD</span></span>

## <a name="udp-connection-termination"></a><span data-ttu-id="65cc1-147">Terminação de conexão UDP</span><span class="sxs-lookup"><span data-stu-id="65cc1-147">UDP Connection Termination</span></span>

<span data-ttu-id="65cc1-148">A terminação de conexão UDP não é indicada em nenhuma camada WFP.</span><span class="sxs-lookup"><span data-stu-id="65cc1-148">UDP connection termination is not indicated at any WFP layer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65cc1-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="65cc1-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65cc1-150">Reautorização de ALE</span><span class="sxs-lookup"><span data-stu-id="65cc1-150">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="65cc1-151">**Filtrando identificadores de camada**</span><span class="sxs-lookup"><span data-stu-id="65cc1-151">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




