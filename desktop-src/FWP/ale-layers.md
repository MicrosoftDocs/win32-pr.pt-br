---
title: Camadas ALE
description: A ALE (aplicação de camada de aplicativo) consiste em várias camadas de filtragem e muitas camadas de descarte correspondentes.
ms.assetid: 3ac71787-2350-4a60-b0bf-b00b52d30b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a96e3b2ae5092bf8cca014eb3603eea5efe8f71
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293922"
---
# <a name="ale-layers"></a><span data-ttu-id="6cc4e-103">Camadas ALE</span><span class="sxs-lookup"><span data-stu-id="6cc4e-103">ALE Layers</span></span>

<span data-ttu-id="6cc4e-104">A ALE (aplicação da camada de aplicativo) consiste em várias camadas de filtragem e muitas camadas de descarte correspondentes.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-104">The Application Layer Enforcement (ALE) consists of several filtering layers and many matching discard layers.</span></span> <span data-ttu-id="6cc4e-105">Todas as camadas do mecanismo de filtragem da WFP (plataforma de filtragem do Windows), incluindo a EPA, são descritas em [**identificadores de camada**](management-filtering-layer-identifiers-.md)de filtragem.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-105">All the Windows Filtering Platform (WFP) filtering engine layers, including ALE, are described in [**Filtering Layer Identifiers**](management-filtering-layer-identifiers-.md).</span></span> <span data-ttu-id="6cc4e-106">Este tópico contém uma descrição mais detalhada das camadas de filtragem que fazem parte da EPA.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-106">This topic contains a more detailed description of the filtering layers that are part of ALE.</span></span>

## <a name="resource_assignment"></a><span data-ttu-id="6cc4e-107">atribuição de recursos \_</span><span class="sxs-lookup"><span data-stu-id="6cc4e-107">RESOURCE\_ASSIGNMENT</span></span>

<span data-ttu-id="6cc4e-108">Um filtro na camada [**de \_ atribuição de recurso Ale da camada FWPM \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) é correspondido para operações de ligação de rede, explícita ou implícita.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-108">A filter at the [**FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for network bind operations, explicit or implicit.</span></span>

<span data-ttu-id="6cc4e-109">Se um filtro nessa camada for correspondido para autorizar a criação de soquetes brutos, o sinalizador de condição fwp será definido como sinalizador de [**\_ ponto de \_ \_ \_ \_ extremidade bruto**](filtering-condition-flags-.md) .</span><span class="sxs-lookup"><span data-stu-id="6cc4e-109">If a filter at this layer is matched to authorize raw socket creation, the [**FWP\_CONDITION\_FLAG\_IS\_RAW\_ENDPOINT**](filtering-condition-flags-.md) flag will be set.</span></span>

<span data-ttu-id="6cc4e-110">Se um filtro nessa camada for correspondido para autorizar o recebimento do modo promíscuo, o campo de [**\_ \_ \_ \_ modo promíscuo de Ale da condição fwp**](filtering-condition-identifiers-.md) será definido como sio \_ RCVALL.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-110">If a filter at this layer is matched to authorize promiscuous mode receiving, the [**FWP\_CONDITION\_ALE\_PROMISCUOUS\_MODE**](filtering-condition-identifiers-.md) field will be set to SIO\_RCVALL.</span></span> <span data-ttu-id="6cc4e-111">Para obter uma descrição de SIO \_ RCVALL, consulte [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl).</span><span class="sxs-lookup"><span data-stu-id="6cc4e-111">For a description of SIO\_RCVALL, see [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl).</span></span>

> [!Note]  
> <span data-ttu-id="6cc4e-112">Essa é a única camada em que o modo promíscuo pode ser filtrado.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-112">This is the only layer where promiscuous mode can be filtered.</span></span>

 

<span data-ttu-id="6cc4e-113">Se nenhuma porta for especificada durante a **ligação ()**, ou seja, a porta for definida como 0 (zero), a pilha TCP/IP selecionará uma porta do intervalo de portas dinâmicas (19152 – 65535).</span><span class="sxs-lookup"><span data-stu-id="6cc4e-113">If no port is specified during **bind()**, that is, port is set to 0 (zero), then the TCP/IP stack will select a port from the dynamic port range (19152–65535).</span></span> <span data-ttu-id="6cc4e-114">A porta selecionada será classificada nesta camada junto com o [**sinalizador de condição fwp é um sinalizador de \_ \_ \_ \_ \_ ligação curinga**](filtering-condition-flags-.md) .</span><span class="sxs-lookup"><span data-stu-id="6cc4e-114">The selected port will be classified at this layer along with the [**FWP\_CONDITION\_FLAG\_IS\_WILDCARD\_BIND**](filtering-condition-flags-.md) flag.</span></span>

<span data-ttu-id="6cc4e-115">Se o endereço local não for especificado na chamada [**BIND ()**](/windows/desktop/api/winsock/nf-winsock-bind) , o campo endereço local será definido como [**fwp \_ vazio**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span><span class="sxs-lookup"><span data-stu-id="6cc4e-115">If the local address is not specified in the [**bind()**](/windows/desktop/api/winsock/nf-winsock-bind) call, the local address field is set to [**FWP\_EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span>

## <a name="auth_listen"></a><span data-ttu-id="6cc4e-116">Escuta de autenticação \_</span><span class="sxs-lookup"><span data-stu-id="6cc4e-116">AUTH\_LISTEN</span></span>

<span data-ttu-id="6cc4e-117">Um filtro na camada [**\_ \_ \_ \_ \_ V {4 \| 6} da autenticação Ale da camada FWPM**](management-filtering-layer-identifiers-.md) é correspondido para chamadas TCP [**() de escuta**](/windows/desktop/api/winsock2/nf-winsock2-listen) .</span><span class="sxs-lookup"><span data-stu-id="6cc4e-117">A filter at the [**FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for TCP [**listen()**](/windows/desktop/api/winsock2/nf-winsock2-listen) calls.</span></span>

## <a name="auth_recv_accept"></a><span data-ttu-id="6cc4e-118">\_aceitação de recv de autenticação \_</span><span class="sxs-lookup"><span data-stu-id="6cc4e-118">AUTH\_RECV\_ACCEPT</span></span>

<span data-ttu-id="6cc4e-119">Um filtro na camada de [**FWPM de \_ autenticação Ale de camada de \_ \_ \_ recepção \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) é correspondido para chamadas de [**aceitação TCP ()**](/windows/desktop/api/winsock2/nf-winsock2-accept) , para os primeiros pacotes UDP (unicast) de uma tupla de endereço/porta remoto exclusiva e para as primeiras mensagens ICMP de não erro de entrada (unicast) com um tipo de ICMP, código e ID exclusivos.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-119">A filter at the [**FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for TCP [**accept()**](/windows/desktop/api/winsock2/nf-winsock2-accept) calls, for first UDP packets (unicast) from a unique remote address/port tuple, and for first inbound non-error ICMP messages (unicast) with a unique ICMP type, code, and ID.</span></span>

> [!Note]  
> <span data-ttu-id="6cc4e-120">Protocolos que não são TCP ou ICMP são tratados como UDP.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-120">Protocols that are not TCP or ICMP are treated like UDP.</span></span>

 

<span data-ttu-id="6cc4e-121">Os pacotes TCP recebidos por soquetes brutos são tratados de forma semelhante ao tráfego UDP.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-121">TCP packets received by raw sockets are handled similarly to UDP traffic.</span></span> <span data-ttu-id="6cc4e-122">Ou seja, somente o primeiro TCP [**Send ()**](/windows/desktop/api/winsock2/nf-winsock2-send) e o primeiro TCP [**recv ()**](/windows/desktop/api/winsock/nf-winsock-recv) sobre soquetes brutos serão filtrados.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-122">That is, only the first TCP [**send()**](/windows/desktop/api/winsock2/nf-winsock2-send) and the first TCP [**recv()**](/windows/desktop/api/winsock/nf-winsock-recv) over raw sockets will be filtered.</span></span>

## <a name="auth_connect"></a><span data-ttu-id="6cc4e-123">conexão de autenticação \_</span><span class="sxs-lookup"><span data-stu-id="6cc4e-123">AUTH\_CONNECT</span></span>

<span data-ttu-id="6cc4e-124">Um filtro na camada [**\_ \_ \_ \_ \_ V {4 \| 6} da autenticação Ale da camada FWPM**](management-filtering-layer-identifiers-.md) é correspondido para chamadas de [**conexão TCP ()**](/windows/desktop/api/winsock2/nf-winsock2-connect) , para os primeiros pacotes UDP enviados a uma tupla de porta e um endereço remoto exclusivo, e para as primeiras mensagens ICMP de não erro de saída com um tipo ICMP, código e ID exclusivos.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-124">A filter at the [**FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for TCP [**connect()**](/windows/desktop/api/winsock2/nf-winsock2-connect) calls, for first UDP packets sent to a unique remote address and port tuple, and for first outbound non-error ICMP messages with a unique ICMP type, code, and ID.</span></span>

> [!Note]  
> <span data-ttu-id="6cc4e-125">Protocolos que não são TCP ou ICMP são tratados como UDP.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-125">Protocols that are not TCP or ICMP are treated like UDP.</span></span>

 

<span data-ttu-id="6cc4e-126">Os pacotes TCP enviados por soquetes brutos são tratados de forma semelhante ao tráfego UDP.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-126">TCP packets sent by raw sockets are handled similarly to UDP traffic.</span></span> <span data-ttu-id="6cc4e-127">Ou seja, somente o primeiro TCP [**Send ()**](/windows/desktop/api/winsock2/nf-winsock2-send) e o primeiro TCP [**recv ()**](/windows/desktop/api/winsock/nf-winsock-recv) sobre soquetes brutos serão filtrados.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-127">That is, only the first TCP [**send()**](/windows/desktop/api/winsock2/nf-winsock2-send) and the first TCP [**recv()**](/windows/desktop/api/winsock/nf-winsock-recv) over raw sockets will be filtered.</span></span>

## <a name="flow_established"></a><span data-ttu-id="6cc4e-128">FLUXO \_ estabelecido</span><span class="sxs-lookup"><span data-stu-id="6cc4e-128">FLOW\_ESTABLISHED</span></span>

<span data-ttu-id="6cc4e-129">Um filtro no [**\_ fluxo Ale da camada de FWPM \_ estabeleceu uma camada \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) correspondente depois que um handshake de três vias TCP for concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-129">A filter at the [**FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched after a TCP three-way handshake has successfully completed.</span></span> <span data-ttu-id="6cc4e-130">Para o tráfego não TCP, o filtro é correspondido imediatamente após os filtros das camadas de **\_ \_ aceitação de recv de autenticação** ou de **\_ conexão de autenticação** serem correspondidos.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-130">For non-TCP traffic, the filter is matched immediately after filters from **AUTH\_RECV\_ACCEPT** or **AUTH\_CONNECT** layers are matched.</span></span>

<span data-ttu-id="6cc4e-131">Um filtro nesta camada não deve retornar o bloco ou a permissão.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-131">A filter at this layer should not return Block or Permit.</span></span>

<span data-ttu-id="6cc4e-132">Essa camada é usada por drivers de texto explicativo para acompanhar o estado de conexão, descrito em detalhes na documentação do [Kit de driver do Windows](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) .</span><span class="sxs-lookup"><span data-stu-id="6cc4e-132">This layer is used by callout drivers to track connection state, described in detail in the [Windows Driver Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) documentation.</span></span>

## <a name="resource_release"></a><span data-ttu-id="6cc4e-133">versão do recurso \_</span><span class="sxs-lookup"><span data-stu-id="6cc4e-133">RESOURCE\_RELEASE</span></span>

<span data-ttu-id="6cc4e-134">Um filtro na camada [**do \_ recurso Ale da camada FWPM da \_ \_ \_ versão \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) é correspondido depois que os recursos alocados por meio da **\_ atribuição de recursos** foram liberados.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-134">A filter at the [**FWPM\_LAYER\_ALE\_RESOURCE\_RELEASE\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched after resources that were allocated via **RESOURCE\_ASSIGNMENT** have been freed.</span></span>

## <a name="endpoint_closure"></a><span data-ttu-id="6cc4e-135">encerramento do ponto de extremidade \_</span><span class="sxs-lookup"><span data-stu-id="6cc4e-135">ENDPOINT\_CLOSURE</span></span>

<span data-ttu-id="6cc4e-136">Um filtro na camada de [**fechamento de ponto de extremidade da camada FWPM do \_ \_ \_ \_ encerramento \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) é correspondido quando um fluxo TCP conectado ou um ponto de extremidade de soquetes UDP é fechado.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-136">A filter at the [**FWPM\_LAYER\_ALE\_ENDPOINT\_CLOSURE\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched when a connected TCP flow or UDP sockets endpoint is closed.</span></span>

## <a name="connect_redirect"></a><span data-ttu-id="6cc4e-137">redirecionamento de conexão \_</span><span class="sxs-lookup"><span data-stu-id="6cc4e-137">CONNECT\_REDIRECT</span></span>

<span data-ttu-id="6cc4e-138">Um filtro na camada [**\_ \_ \_ \_ redirecionamento Ale Connect \_ V {4 \| 6} da camada FWPM**](management-filtering-layer-identifiers-.md) permite a modificação de endereços e portas remotos.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-138">A filter at the [**FWPM\_LAYER\_ALE\_CONNECT\_REDIRECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer allows for modification of remote addresses and ports.</span></span> <span data-ttu-id="6cc4e-139">A conexão de saída será redirecionada pela duração dessa conexão.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-139">The outbound connection will be redirected for the duration of that connection.</span></span>

## <a name="bind_redirect"></a><span data-ttu-id="6cc4e-140">redirecionamento de associação \_</span><span class="sxs-lookup"><span data-stu-id="6cc4e-140">BIND\_REDIRECT</span></span>

<span data-ttu-id="6cc4e-141">Um filtro na camada [**\_ \_ \_ \_ redirecionamento Ale BIND \_ V {4 \| 6} da camada FWPM**](management-filtering-layer-identifiers-.md) permite a modificação do endereço local e das portas do soquete subjacente.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-141">A filter at the [**FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer allows for modification of the underlying socket's local address and ports.</span></span> <span data-ttu-id="6cc4e-142">O soquete local será redirecionado durante o tempo de vida do soquete</span><span class="sxs-lookup"><span data-stu-id="6cc4e-142">The local socket will be redirected for the lifetime of the socket</span></span>

## <a name="ale-discard-layers"></a><span data-ttu-id="6cc4e-143">Camadas de descarte ALE</span><span class="sxs-lookup"><span data-stu-id="6cc4e-143">ALE DISCARD Layers</span></span>

<span data-ttu-id="6cc4e-144">Para cada uma das camadas ALE descritas acima, o mecanismo de filtragem contém uma camada de descarte correspondente.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-144">For each of the ALE layers described above the filtering engine contains a matching discard layer.</span></span> <span data-ttu-id="6cc4e-145">As camadas de descarte ALE são usadas por textos explicativos para fins de log.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-145">The ALE discard layers are used by callouts for logging purposes.</span></span> <span data-ttu-id="6cc4e-146">Os pacotes e as indicações que foram descartadas em uma das camadas de filtragem ALE são indicados para a camada de descarte ALE correspondente.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-146">Packets and indications that have been discarded at one of the ALE filtering layers are indicated to the matching ALE discard layer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6cc4e-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6cc4e-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cc4e-148">Aplicação da camada de aplicativo (EPA)</span><span class="sxs-lookup"><span data-stu-id="6cc4e-148">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="6cc4e-149">Filtragem de estado de ALE</span><span class="sxs-lookup"><span data-stu-id="6cc4e-149">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="6cc4e-150">Tráfego de difusão/multicast ALE</span><span class="sxs-lookup"><span data-stu-id="6cc4e-150">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="6cc4e-151">Reautorização de ALE</span><span class="sxs-lookup"><span data-stu-id="6cc4e-151">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="6cc4e-152">Personalização de fluxo ALE</span><span class="sxs-lookup"><span data-stu-id="6cc4e-152">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> <dt>

[<span data-ttu-id="6cc4e-153">Fluxos de pacotes TCP</span><span class="sxs-lookup"><span data-stu-id="6cc4e-153">TCP Packet Flows</span></span>](tcp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="6cc4e-154">Fluxos de pacotes UDP</span><span class="sxs-lookup"><span data-stu-id="6cc4e-154">UDP Packet Flows</span></span>](udp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="6cc4e-155">Funções do Winsock</span><span class="sxs-lookup"><span data-stu-id="6cc4e-155">Winsock Functions</span></span>](/windows/desktop/WinSock/winsock-functions)
</dt> <dt>

[<span data-ttu-id="6cc4e-156">**Filtrando sinalizadores de condição**</span><span class="sxs-lookup"><span data-stu-id="6cc4e-156">**Filtering Condition Flags**</span></span>](filtering-condition-flags-.md)
</dt> <dt>

[<span data-ttu-id="6cc4e-157">**Condições de filtragem disponíveis em cada camada de filtragem**</span><span class="sxs-lookup"><span data-stu-id="6cc4e-157">**Filtering Conditions Available At Each Filtering Layer**</span></span>](filtering-conditions-available-at-each-filtering-layer.md)
</dt> </dl>

 

 