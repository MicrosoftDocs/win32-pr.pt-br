---
description: O IP Helper fornece recursos de recuperação de informações que são úteis para a administração de rede do computador local.
ms.assetid: b50b3927-6c74-4282-b79b-c86d72d93ae3
title: Recuperando informações sobre o protocolo de Internet e o protocolo de mensagem de controle da Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b2768ff591b53db79bbbfb38fc2c6c2596ca9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920662"
---
# <a name="retrieving-information-on-the-internet-protocol-and-the-internet-control-message-protocol"></a><span data-ttu-id="d4739-103">Recuperando informações sobre o protocolo de Internet e o protocolo de mensagem de controle da Internet</span><span class="sxs-lookup"><span data-stu-id="d4739-103">Retrieving Information on the Internet Protocol and the Internet Control Message Protocol</span></span>

<span data-ttu-id="d4739-104">O IP Helper fornece recursos de recuperação de informações que são úteis para a administração de rede do computador local.</span><span class="sxs-lookup"><span data-stu-id="d4739-104">IP Helper provides information retrieval capabilities that are useful for the network administration of the local computer.</span></span> <span data-ttu-id="d4739-105">As funções a seguir recuperam estatísticas para o protocolo IP e o protocolo ICMP (Internet Control Message Protocol).</span><span class="sxs-lookup"><span data-stu-id="d4739-105">The following functions retrieve statistics for the Internet Protocol (IP) and the Internet Control Message Protocol (ICMP).</span></span> <span data-ttu-id="d4739-106">Você também pode usar essas funções para definir determinados parâmetros de configuração para o IP.</span><span class="sxs-lookup"><span data-stu-id="d4739-106">You can also use these functions to set certain configuration parameters for IP.</span></span>

<span data-ttu-id="d4739-107">A função [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) recupera as estatísticas de IP atuais para o computador local.</span><span class="sxs-lookup"><span data-stu-id="d4739-107">The [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) function retrieves the current IP statistics for the local computer.</span></span> <span data-ttu-id="d4739-108">Para obter exemplos de código envolvendo **GetIpStatistics** , consulte [recuperando informações usando GetIpStatistics](retrieving-information-using-getipstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="d4739-108">For code samples involving **GetIpStatistics** see [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md).</span></span>

<span data-ttu-id="d4739-109">A função [**GetIcmpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-geticmpstatistics) recupera as estatísticas ICMP atuais.</span><span class="sxs-lookup"><span data-stu-id="d4739-109">The [**GetIcmpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-geticmpstatistics) function retrieves the current ICMP statistics.</span></span>

<span data-ttu-id="d4739-110">Use a função [**SetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatistics) para habilitar ou desabilitar o encaminhamento de IP.</span><span class="sxs-lookup"><span data-stu-id="d4739-110">Use the [**SetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatistics) function to enable or disable IP forwarding.</span></span> <span data-ttu-id="d4739-111">Essa função também possibilita que você defina o TTL (vida útil) padrão para datagramas IP.</span><span class="sxs-lookup"><span data-stu-id="d4739-111">This function also makes it possible for you to set the default time-to-live (TTL) for IP datagrams.</span></span> <span data-ttu-id="d4739-112">Como alternativa, você pode definir o TTL usando a função [**SetIpTTL**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipttl) .</span><span class="sxs-lookup"><span data-stu-id="d4739-112">Alternatively, you can set the TTL by using the [**SetIpTTL**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipttl) function.</span></span>

 

 



