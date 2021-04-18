---
description: Os problemas de tamanho do pacote de mídia abordados no tópico sobre o tamanho do pacote de mídia afetam os vários protocolos IPX de PF de \_ forma diferente.
ms.assetid: 7f0643b8-6bb2-4dbb-b306-d9b2e0d0e03c
title: Como o tamanho do pacote afeta os protocolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c778ee6c75cd558d19cdf1cbb76052065e03c427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296350"
---
# <a name="how-packet-size-affects-protocols"></a><span data-ttu-id="74c19-103">Como o tamanho do pacote afeta os protocolos</span><span class="sxs-lookup"><span data-stu-id="74c19-103">How Packet Size Affects Protocols</span></span>

<span data-ttu-id="74c19-104">Os problemas de tamanho do pacote de mídia abordados no tópico [sobre o tamanho do pacote de mídia](about-media-packet-size-2.md)afetam os vários protocolos IPX de PF de \_ forma diferente.</span><span class="sxs-lookup"><span data-stu-id="74c19-104">Media packet size issues discussed in the topic, [About Media Packet Size](about-media-packet-size-2.md), affect the various PF\_IPX protocols differently.</span></span> <span data-ttu-id="74c19-105">Uma estratégia comum para lidar com várias restrições de tamanho de roteador e mídia é usar o tamanho de mídia completo quando o número de rede da estação remota corresponde à estação local e retorna para o tamanho mínimo do pacote, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="74c19-105">A common strategy for handling various router and media size constraints is to use the full media size when the remote station's network number matches the local station, and fall back to the minimum packet size otherwise.</span></span>

## <a name="parameters"></a><span data-ttu-id="74c19-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74c19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74c19-107"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>NSPROTO \_ IPX</span><span class="sxs-lookup"><span data-stu-id="74c19-107"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>NSPROTO\_IPX</span></span>
</dt> <dd>

<span data-ttu-id="74c19-108">Fornece um serviço de datagrama; cada datagrama deve residir no tamanho máximo do pacote.</span><span class="sxs-lookup"><span data-stu-id="74c19-108">Provides a datagram service; each datagram must reside within the maximum packet size.</span></span> <span data-ttu-id="74c19-109">O Winsock define o tamanho máximo do pacote de datagrama para o tamanho do pacote de mídia local menos o cabeçalho IPX.</span><span class="sxs-lookup"><span data-stu-id="74c19-109">Winsock sets the maximum datagram packet size to the local media packet size minus the IPX header.</span></span> <span data-ttu-id="74c19-110">No entanto, tenha em mente que, se o pacote for roteado, ele poderá atingir as restrições do roteador em direção à rota.</span><span class="sxs-lookup"><span data-stu-id="74c19-110">Keep in mind, however, that if the packet is routed, it may hit router restrictions en route.</span></span> <span data-ttu-id="74c19-111">Verifique se seu aplicativo pode retornar a datagramas de 546 bytes.</span><span class="sxs-lookup"><span data-stu-id="74c19-111">Make sure your application can fall back to 546-byte datagrams.</span></span>

</dd> <dt>

<span data-ttu-id="74c19-112"><span id="NSPROTO_SPX"></span><span id="nsproto_spx"></span>NSPROTO \_ SPX</span><span class="sxs-lookup"><span data-stu-id="74c19-112"><span id="NSPROTO_SPX"></span><span id="nsproto_spx"></span>NSPROTO\_SPX</span></span>
</dt> <dd>

<span data-ttu-id="74c19-113">Fornece serviços de fluxo e pacotes sequenciados.</span><span class="sxs-lookup"><span data-stu-id="74c19-113">Provides stream and sequenced-packet services.</span></span> <span data-ttu-id="74c19-114">O Winsock IPX/SPX permite que fluxos de dados e mensagens abranjam vários pacotes, portanto, o tamanho do pacote não limita a quantidade de dados manipulados por [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) e [**recv**](/windows/desktop/api/winsock/nf-winsock-recv).</span><span class="sxs-lookup"><span data-stu-id="74c19-114">Winsock IPX/SPX lets data streams and messages span multiple packets, so packet size does not limit the amount of data handled by [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) and [**recv**](/windows/desktop/api/winsock/nf-winsock-recv).</span></span> <span data-ttu-id="74c19-115">No entanto, o tamanho da mídia subjacente deve ser definido corretamente ou o primeiro pacote grande não será entregue e a conexão será redefinida.</span><span class="sxs-lookup"><span data-stu-id="74c19-115">However, the underlying media size must be set correctly or the first large packet will be undeliverable and the connection will reset.</span></span> <span data-ttu-id="74c19-116">Se a estação de destino estiver na rede local, o Winsock definirá seu tamanho de pacote para o tamanho do pacote de mídia.</span><span class="sxs-lookup"><span data-stu-id="74c19-116">If the target station is on the local network, Winsock sets its packet size to the media packet size.</span></span> <span data-ttu-id="74c19-117">Caso contrário, o padrão é 512 bytes.</span><span class="sxs-lookup"><span data-stu-id="74c19-117">Otherwise, it defaults to 512 bytes.</span></span> <span data-ttu-id="74c19-118">Esse tamanho pode ser alterado imediatamente após a [**conexão**](/windows/desktop/api/Winsock2/nf-winsock2-connect) ou a [**aceitação**](/windows/desktop/api/Winsock2/nf-winsock2-accept) por meio do [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt).</span><span class="sxs-lookup"><span data-stu-id="74c19-118">This size can be changed immediately after [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) or [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) through [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt).</span></span>

</dd> <dt>

<span data-ttu-id="74c19-119"><span id="NSPROTO_SPXII"></span><span id="nsproto_spxii"></span>NSPROTO \_ SPXII</span><span class="sxs-lookup"><span data-stu-id="74c19-119"><span id="NSPROTO_SPXII"></span><span id="nsproto_spxii"></span>NSPROTO\_SPXII</span></span>
</dt> <dd>

<span data-ttu-id="74c19-120">O SPXII apresenta uma grande negociação de pacotes da Internet para manter um melhor ajuste para pacotes e não requer intervenção do programador.</span><span class="sxs-lookup"><span data-stu-id="74c19-120">SPXII features large Internet packet negotiation to maintain a best-fit size for packets and does not require programmer intervention.</span></span> <span data-ttu-id="74c19-121">No entanto, se a estação remota não oferecer suporte a SPXII e negociar para o SPX Standard, as regras do NSPROTO \_ SPX estarão em vigor.</span><span class="sxs-lookup"><span data-stu-id="74c19-121">However, if the remote station does not support SPXII and negotiates down to standard SPX, the NSPROTO\_SPX rules are in effect.</span></span>



| <span data-ttu-id="74c19-122">Protocolo</span><span class="sxs-lookup"><span data-stu-id="74c19-122">Protocol</span></span>     | <span data-ttu-id="74c19-123">Mídia</span><span class="sxs-lookup"><span data-stu-id="74c19-123">Media</span></span>      | <span data-ttu-id="74c19-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="74c19-124">Type</span></span>        | <span data-ttu-id="74c19-125">Tamanho do pacote de dados</span><span class="sxs-lookup"><span data-stu-id="74c19-125">Data packet size</span></span> |
|--------------|------------|-------------|------------------|
| <span data-ttu-id="74c19-126">NSPROTO \_ IPX</span><span class="sxs-lookup"><span data-stu-id="74c19-126">NSPROTO\_IPX</span></span> | <span data-ttu-id="74c19-127">Ethernet</span><span class="sxs-lookup"><span data-stu-id="74c19-127">Ethernet</span></span>   | <span data-ttu-id="74c19-128">Ethernet II</span><span class="sxs-lookup"><span data-stu-id="74c19-128">Ethernet II</span></span> |                  |
|              |            | <span data-ttu-id="74c19-129">802.3</span><span class="sxs-lookup"><span data-stu-id="74c19-129">802.3</span></span>       |                  |
|              |            | <span data-ttu-id="74c19-130">802.2</span><span class="sxs-lookup"><span data-stu-id="74c19-130">802.2</span></span>       | <span data-ttu-id="74c19-131">1466</span><span class="sxs-lookup"><span data-stu-id="74c19-131">1466</span></span>             |
|              |            | <span data-ttu-id="74c19-132">ALINHA</span><span class="sxs-lookup"><span data-stu-id="74c19-132">SNAP</span></span>        |                  |
|              | <span data-ttu-id="74c19-133">Anel de token</span><span class="sxs-lookup"><span data-stu-id="74c19-133">Token Ring</span></span> | <span data-ttu-id="74c19-134">4 megabits</span><span class="sxs-lookup"><span data-stu-id="74c19-134">4 megabit</span></span>   |                  |
|              |            | <span data-ttu-id="74c19-135">16 megabits</span><span class="sxs-lookup"><span data-stu-id="74c19-135">16 megabit</span></span>  |                  |
| <span data-ttu-id="74c19-136">NSPROTO \_ SPX</span><span class="sxs-lookup"><span data-stu-id="74c19-136">NSPROTO\_SPX</span></span> | <span data-ttu-id="74c19-137">Ethernet</span><span class="sxs-lookup"><span data-stu-id="74c19-137">Ethernet</span></span>   | <span data-ttu-id="74c19-138">Ethernet II</span><span class="sxs-lookup"><span data-stu-id="74c19-138">Ethernet II</span></span> |                  |
|              |            | <span data-ttu-id="74c19-139">802.3</span><span class="sxs-lookup"><span data-stu-id="74c19-139">802.3</span></span>       |                  |
|              |            | <span data-ttu-id="74c19-140">802.2</span><span class="sxs-lookup"><span data-stu-id="74c19-140">802.2</span></span>       | <span data-ttu-id="74c19-141">1454</span><span class="sxs-lookup"><span data-stu-id="74c19-141">1454</span></span>             |
|              |            | <span data-ttu-id="74c19-142">ALINHA</span><span class="sxs-lookup"><span data-stu-id="74c19-142">SNAP</span></span>        |                  |
|              | <span data-ttu-id="74c19-143">Anel de token</span><span class="sxs-lookup"><span data-stu-id="74c19-143">Token Ring</span></span> | <span data-ttu-id="74c19-144">4 megabits</span><span class="sxs-lookup"><span data-stu-id="74c19-144">4 megabit</span></span>   |                  |
|              |            | <span data-ttu-id="74c19-145">16 megabits</span><span class="sxs-lookup"><span data-stu-id="74c19-145">16 megabit</span></span>  |                  |



 

</dd> </dl>

 

 



