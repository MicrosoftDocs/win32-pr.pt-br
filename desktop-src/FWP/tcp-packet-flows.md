---
title: Fluxos de pacotes TCP
description: A ordem na qual as camadas do mecanismo de filtro da WFP (Windows Filtering Platform) são percorridas durante uma sessão TCP típica.
ms.assetid: 75319c91-f77b-4dec-b94f-36772f1f1d53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2203ccb4b2793983bd5b1052d53c2700d3033a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916443"
---
# <a name="tcp-packet-flows"></a><span data-ttu-id="ac1ae-103">Fluxos de pacotes TCP</span><span class="sxs-lookup"><span data-stu-id="ac1ae-103">TCP Packet Flows</span></span>

<span data-ttu-id="ac1ae-104">Esta seção descreve a ordem na qual as camadas do mecanismo de filtro da WFP (Windows Filtering Platform) são percorridas durante uma sessão TCP típica.</span><span class="sxs-lookup"><span data-stu-id="ac1ae-104">This section describes the order in which the layers of the Windows Filtering Platform (WFP) filter engine are traversed during a typical TCP session.</span></span>

> [!Note]  
> <span data-ttu-id="ac1ae-105">Os fluxos de pacotes TCP para IPv6 seguem o mesmo padrão que para IPv4.</span><span class="sxs-lookup"><span data-stu-id="ac1ae-105">TCP packet flows for IPv6 follow the same pattern as for IPv4.</span></span>

 

> [!Note]  
> <span data-ttu-id="ac1ae-106">Os fluxos de pacotes não TCP seguem o mesmo padrão que os [fluxos de pacotes UDP](udp-packet-flows.md).</span><span class="sxs-lookup"><span data-stu-id="ac1ae-106">Non-TCP packet flows follow the same pattern as [UDP packet flows](udp-packet-flows.md).</span></span>

 

## <a name="tcp-connection-establishment"></a><span data-ttu-id="ac1ae-107">Estabelecimento de conexão TCP</span><span class="sxs-lookup"><span data-stu-id="ac1ae-107">TCP Connection Establishment</span></span>

<dl> <span data-ttu-id="ac1ae-108">O servidor (receptor) executa a abertura passiva</span><span class="sxs-lookup"><span data-stu-id="ac1ae-108">Server (receiver) performs Passive Open</span></span>

-   <span data-ttu-id="ac1ae-109">bind: \_ \_ \_ \_ redirecionamento de associação Ale de camada FWPM \_ (somente windows 7/Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="ac1ae-109">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="ac1ae-110">Associação: \_ v4 de \_ \_ atribuição de \_ recursos \_ da camada FWPM</span><span class="sxs-lookup"><span data-stu-id="ac1ae-110">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>
-   <span data-ttu-id="ac1ae-111">escutar: FWPM \_ da \_ autenticação Ale de camada de conexão \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-111">listen: FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V4</span></span>

  
<span data-ttu-id="ac1ae-112">Cliente (remetente) executa active open</span><span class="sxs-lookup"><span data-stu-id="ac1ae-112">Client (sender) performs Active Open</span></span>

-   <span data-ttu-id="ac1ae-113">bind: \_ \_ \_ \_ redirecionamento de associação Ale de camada FWPM \_ (somente windows 7/Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="ac1ae-113">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="ac1ae-114">Associação: \_ v4 de \_ \_ atribuição de \_ recursos \_ da camada FWPM</span><span class="sxs-lookup"><span data-stu-id="ac1ae-114">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>
-   <span data-ttu-id="ac1ae-115">Connect: \_ \_ redirecionamento da camada Ale do FWPM layer para \_ \_ \_ V4 (somente windows 7/Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="ac1ae-115">connect: FWPM\_LAYER\_ALE\_CONNECT\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="ac1ae-116">conectar: \_ conexão de \_ autenticação Ale de camada FWPM \_ \_ Connect \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-116">connect: FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V4</span></span>
-   <span data-ttu-id="ac1ae-117">SYN: transporte de saída da camada do FWPM \_ \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-117">SYN: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="ac1ae-118">SYN: \_ IPPACKET de saída da camada FWPM \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-118">SYN: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="ac1ae-119">Servidor</span><span class="sxs-lookup"><span data-stu-id="ac1ae-119">Server</span></span>

-   <span data-ttu-id="ac1ae-120">SYN: \_ IPPACKET de entrada da camada FWPM \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-120">SYN: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="ac1ae-121">SYN: transporte de entrada da camada do FWPM \_ \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-121">SYN: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="ac1ae-122">SYN: \_ aceitação de \_ recepção de autenticação Ale de camada de FWPM \_ \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-122">SYN: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="ac1ae-123">SYN-ACK: \_ transporte de saída de camada FWPM \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-123">SYN-ACK: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="ac1ae-124">SYN-ACK: \_ IPPACKET de saída da camada FWPM \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-124">SYN-ACK: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="ac1ae-125">Cliente</span><span class="sxs-lookup"><span data-stu-id="ac1ae-125">Client</span></span>

-   <span data-ttu-id="ac1ae-126">SYN-ACK: \_ entrada da camada FWPM \_ \_ IPPACKET \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-126">SYN-ACK: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="ac1ae-127">SYN-ACK: FWPM \_ de \_ transporte de entrada da camada \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-127">SYN-ACK: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="ac1ae-128">O \_ fluxo de Ale de camada de FWPM \_ \_ \_ estabeleceu \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-128">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="ac1ae-129">ACK: \_ transporte de saída da camada FWPM \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-129">ACK: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="ac1ae-130">ACK: FWPM \_ IPPACKET de saída da camada \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-130">ACK: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="ac1ae-131">Servidor</span><span class="sxs-lookup"><span data-stu-id="ac1ae-131">Server</span></span>

-   <span data-ttu-id="ac1ae-132">ACK: \_ \_ \_ IPPACKET v4 de entrada na camada FWPM \_</span><span class="sxs-lookup"><span data-stu-id="ac1ae-132">ACK: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="ac1ae-133">ACK: \_ transporte de entrada da camada FWPM \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-133">ACK: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="ac1ae-134">O \_ fluxo de Ale de camada de FWPM \_ \_ \_ estabeleceu \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-134">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="ac1ae-135">A escuta é concluída.</span><span class="sxs-lookup"><span data-stu-id="ac1ae-135">Listen completes.</span></span> <span data-ttu-id="ac1ae-136">O servidor pode executar uma aceitação.</span><span class="sxs-lookup"><span data-stu-id="ac1ae-136">Server can perform an accept.</span></span>

  
</dl>

## <a name="tcp-syn-received-with-no-one-listening-on-the-port-or-protocol"></a><span data-ttu-id="ac1ae-137">TCP SYN recebido sem escuta na porta ou no protocolo</span><span class="sxs-lookup"><span data-stu-id="ac1ae-137">TCP SYN Received with No One Listening on the Port or Protocol</span></span>

<span data-ttu-id="ac1ae-138">Servidor (receptor)</span><span class="sxs-lookup"><span data-stu-id="ac1ae-138">Server (receiver)</span></span>

-   <span data-ttu-id="ac1ae-139">SYN: \_ IPPACKET de entrada da camada FWPM \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-139">SYN: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="ac1ae-140">SYN: \_ \_ \_ \_ descarte v4 de transporte de entrada da camada FWPM \_</span><span class="sxs-lookup"><span data-stu-id="ac1ae-140">SYN: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4\_DISCARD</span></span>
-   <span data-ttu-id="ac1ae-141">RST: \_ transporte de saída de camada FWPM \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-141">RST: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="ac1ae-142">RST: \_ IPPACKET de saída da camada FWPM \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-142">RST: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

> [!Note]  
> <span data-ttu-id="ac1ae-143">O TCP SYN sem nenhum ponto de extremidade é indicado em descarte de transporte com uma condição de erro específica.</span><span class="sxs-lookup"><span data-stu-id="ac1ae-143">TCP SYN with no endpoint is indicated at TRANSPORT discard with a specific error condition.</span></span> <span data-ttu-id="ac1ae-144">Bloquear este pacote no descarte de transporte para fazer com que a pilha não envie o evento correspondente (RST).</span><span class="sxs-lookup"><span data-stu-id="ac1ae-144">Block this packet at TRANSPORT discard to cause the stack not to send the corresponding event (RST).</span></span> <span data-ttu-id="ac1ae-145">Para obter um exemplo de filtragem de modo furtivo, consulte [impedindo a verificação de porta](preventing-port-scanning.md).</span><span class="sxs-lookup"><span data-stu-id="ac1ae-145">For an example of stealth-mode filtering, see [Preventing Port Scanning](preventing-port-scanning.md).</span></span>

 

## <a name="data-transmitted-over-a-tcp-connection"></a><span data-ttu-id="ac1ae-146">Dados transmitidos por uma conexão TCP</span><span class="sxs-lookup"><span data-stu-id="ac1ae-146">Data Transmitted Over a TCP Connection</span></span>

<dl> <span data-ttu-id="ac1ae-147">Cliente (remetente)</span><span class="sxs-lookup"><span data-stu-id="ac1ae-147">Client (sender)</span></span>

-   <span data-ttu-id="ac1ae-148">Enviar</span><span class="sxs-lookup"><span data-stu-id="ac1ae-148">send</span></span>
-   <span data-ttu-id="ac1ae-149">dados: \_ fluxo de camada FWPM \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-149">data: FWPM\_LAYER\_STREAM\_V4</span></span>
-   <span data-ttu-id="ac1ae-150">Segmentos TCP: \_ v4 de \_ transporte de saída da camada FWPM \_ \_</span><span class="sxs-lookup"><span data-stu-id="ac1ae-150">TCP segments: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="ac1ae-151">Datagramas IP: \_ \_ \_ IPPACKET v4 de saída da camada FWPM \_</span><span class="sxs-lookup"><span data-stu-id="ac1ae-151">IP datagrams: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="ac1ae-152">Servidor (receptor)</span><span class="sxs-lookup"><span data-stu-id="ac1ae-152">Server (receiver)</span></span>

-   <span data-ttu-id="ac1ae-153">Datagramas IP: \_ \_ \_ IPPACKET v4 de entrada da camada FWPM \_</span><span class="sxs-lookup"><span data-stu-id="ac1ae-153">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="ac1ae-154">Segmentos TCP: \_ transporte de entrada da camada FWPM \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-154">TCP segments: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="ac1ae-155">dados: \_ fluxo de camada FWPM \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-155">data: FWPM\_LAYER\_STREAM\_V4</span></span>
-   <span data-ttu-id="ac1ae-156">Os dados estão disponíveis para leitura.</span><span class="sxs-lookup"><span data-stu-id="ac1ae-156">Data is available to read.</span></span>

  
</dl>

## <a name="successful-reauthorization-of-a-tcp-packet"></a><span data-ttu-id="ac1ae-157">Reautorização bem-sucedida de um pacote TCP</span><span class="sxs-lookup"><span data-stu-id="ac1ae-157">Successful Reauthorization of a TCP Packet</span></span>

<span data-ttu-id="ac1ae-158">Servidor (receptor)</span><span class="sxs-lookup"><span data-stu-id="ac1ae-158">Server (receiver)</span></span>

-   <span data-ttu-id="ac1ae-159">Datagramas IP: \_ \_ \_ IPPACKET v4 de entrada da camada FWPM \_</span><span class="sxs-lookup"><span data-stu-id="ac1ae-159">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="ac1ae-160">Segmento TCP: \_ transporte de entrada da camada FWPM \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-160">TCP segment: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="ac1ae-161">Segmento TCP: \_ aceitação de \_ recepção de autenticação Ale de camada de FWPM \_ \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-161">TCP segment: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="ac1ae-162">dados: \_ \_ fluxo de camada FWPM \_ V4 (entrada)</span><span class="sxs-lookup"><span data-stu-id="ac1ae-162">data: FWPM\_LAYER\_STREAM\_V4(INBOUND)</span></span>

## <a name="failed-reauthorization-of-a-tcp-packet"></a><span data-ttu-id="ac1ae-163">Falha na Reautorização de um pacote TCP</span><span class="sxs-lookup"><span data-stu-id="ac1ae-163">Failed Reauthorization of a TCP Packet</span></span>

<span data-ttu-id="ac1ae-164">Servidor (receptor)</span><span class="sxs-lookup"><span data-stu-id="ac1ae-164">Server (receiver)</span></span>

-   <span data-ttu-id="ac1ae-165">Datagramas IP: \_ \_ \_ IPPACKET v4 de entrada da camada FWPM \_</span><span class="sxs-lookup"><span data-stu-id="ac1ae-165">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="ac1ae-166">Segmento TCP: \_ transporte de entrada da camada FWPM \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-166">TCP segment: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="ac1ae-167">Segmento TCP: \_ aceitação de \_ recepção de autenticação Ale de camada de FWPM \_ \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ac1ae-167">TCP segment: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="ac1ae-168">Segmento TCP: FWPM \_ camada \_ de \_ autenticação \_ Ale \_ aceitar aceitação \_ v4 \_ descartar</span><span class="sxs-lookup"><span data-stu-id="ac1ae-168">TCP segment: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4\_DISCARD</span></span>

## <a name="tcp-connection-termination"></a><span data-ttu-id="ac1ae-169">Término da conexão TCP</span><span class="sxs-lookup"><span data-stu-id="ac1ae-169">TCP Connection Termination</span></span>

<span data-ttu-id="ac1ae-170">A terminação de conexão TCP não é indicada em nenhuma camada WFP.</span><span class="sxs-lookup"><span data-stu-id="ac1ae-170">TCP connection termination is not indicated at any WFP layer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac1ae-171">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ac1ae-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac1ae-172">Reautorização de ALE</span><span class="sxs-lookup"><span data-stu-id="ac1ae-172">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="ac1ae-173">**Filtrando identificadores de camada**</span><span class="sxs-lookup"><span data-stu-id="ac1ae-173">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




