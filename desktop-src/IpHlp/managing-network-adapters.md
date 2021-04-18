---
description: O IP Helper fornece recursos para gerenciar adaptadores de rede. Há uma correspondência um-para-um entre as interfaces e os adaptadores em um determinado computador. Uma interface é uma abstração de nível de IP, enquanto que um adaptador é uma abstração no nível de vínculo de datalink.
ms.assetid: fbb32941-2add-4f74-90c4-1dc1bfebd64c
title: Gerenciando adaptadores de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaa8f42cf1499ee7873d13334d0edbc9f954794f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501602"
---
# <a name="managing-network-adapters"></a><span data-ttu-id="2b9f5-105">Gerenciando adaptadores de rede</span><span class="sxs-lookup"><span data-stu-id="2b9f5-105">Managing Network Adapters</span></span>

<span data-ttu-id="2b9f5-106">O IP Helper fornece recursos para gerenciar adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="2b9f5-106">IP Helper provides capabilities for managing network adapters.</span></span> <span data-ttu-id="2b9f5-107">Há uma correspondência um-para-um entre as interfaces e os adaptadores em um determinado computador.</span><span class="sxs-lookup"><span data-stu-id="2b9f5-107">There is a one-to-one correspondence between the interfaces and adapters on a given computer.</span></span> <span data-ttu-id="2b9f5-108">Uma interface é uma abstração de nível de IP, enquanto que um adaptador é uma abstração no nível de vínculo de datalink.</span><span class="sxs-lookup"><span data-stu-id="2b9f5-108">An interface is an IP-level abstraction, whereas an adapter is a datalink-level abstraction.</span></span>

<span data-ttu-id="2b9f5-109">Use as funções descritas nos parágrafos a seguir para recuperar informações sobre os adaptadores de rede no computador local.</span><span class="sxs-lookup"><span data-stu-id="2b9f5-109">Use the functions described in the following paragraphs to retrieve information about the network adapters in the local computer.</span></span>

<span data-ttu-id="2b9f5-110">A função [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) retorna uma matriz de estruturas de [**\_ \_ informações do adaptador IP**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) , uma para cada adaptador no computador local.</span><span class="sxs-lookup"><span data-stu-id="2b9f5-110">The [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function returns an array of [**IP\_ADAPTER\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) structures, one for each adapter in the local computer.</span></span> <span data-ttu-id="2b9f5-111">A função [**GetPerAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getperadapterinfo) retorna informações adicionais sobre um adaptador específico.</span><span class="sxs-lookup"><span data-stu-id="2b9f5-111">The [**GetPerAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getperadapterinfo) function returns additional information about a specific adapter.</span></span> <span data-ttu-id="2b9f5-112">A função **GetPerAdapterInfo** requer que o chamador especifique o índice do adaptador.</span><span class="sxs-lookup"><span data-stu-id="2b9f5-112">The **GetPerAdapterInfo** function requires the caller to specify the index of the adapter.</span></span> <span data-ttu-id="2b9f5-113">Para obter o índice de adaptador do nome do adaptador, use a função [**GetAdapterIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadapterindex) .</span><span class="sxs-lookup"><span data-stu-id="2b9f5-113">To obtain the adapter index from the adapter name, use the [**GetAdapterIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadapterindex) function.</span></span>

<span data-ttu-id="2b9f5-114">Alguns aplicativos usam adaptadores que recebem datagrams, mas não podem transmiti-los.</span><span class="sxs-lookup"><span data-stu-id="2b9f5-114">Some applications use adapters that receive datagrams, but cannot transmit them.</span></span> <span data-ttu-id="2b9f5-115">Para obter informações sobre esses adaptadores, use a função [**GetUniDirectionalAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo) .</span><span class="sxs-lookup"><span data-stu-id="2b9f5-115">To obtain information about these adapters, use the [**GetUniDirectionalAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo) function.</span></span>

<span data-ttu-id="2b9f5-116">A função [**GetAdaptersAddresses**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses) permite que você recupere os endereços IP associados a um adaptador específico.</span><span class="sxs-lookup"><span data-stu-id="2b9f5-116">The [**GetAdaptersAddresses**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses) function enables you to retrieve the IP addresses associated with a particular adapter.</span></span> <span data-ttu-id="2b9f5-117">Essa função dá suporte ao endereçamento IPv4 e IPv6.</span><span class="sxs-lookup"><span data-stu-id="2b9f5-117">This function supports both IPv4 and IPv6 addressing.</span></span>

-   <span data-ttu-id="2b9f5-118">Para obter exemplos de código envolvendo [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) , consulte [Managing Network adapters using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).</span><span class="sxs-lookup"><span data-stu-id="2b9f5-118">For code samples involving [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) see [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).</span></span>

 

 



