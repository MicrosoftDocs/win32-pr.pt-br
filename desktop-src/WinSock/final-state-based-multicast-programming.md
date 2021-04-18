---
description: Esta seção descreve a programação de multicast com base no estado final usando IOCTLs, em vez de opções de soquete. Para obter uma visão geral de como a programação de multicast baseada em estado final difere da programação de multicast baseada em alteração, consulte programação de multicast.
ms.assetid: 71c05393-3f8c-42c0-9060-e0df9b5e2578
title: Programação de multicast com base no estado final
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6abfebfc7efe27f1c5a6d63312c376bd659dce57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789343"
---
# <a name="final-state-based-multicast-programming"></a><span data-ttu-id="12302-104">Programação de multicast com base no estado final</span><span class="sxs-lookup"><span data-stu-id="12302-104">Final-State-Based Multicast Programming</span></span>

<span data-ttu-id="12302-105">Esta seção descreve a programação de multicast com base no estado final usando IOCTLs, em vez de opções de soquete.</span><span class="sxs-lookup"><span data-stu-id="12302-105">This section describes final-state-based multicast programming using IOCTLs instead of socket options.</span></span> <span data-ttu-id="12302-106">Para obter uma visão geral de como a programação de multicast baseada em estado final difere da programação de multicast baseada em alteração, consulte [programação de multicast](multicast-programming.md).</span><span class="sxs-lookup"><span data-stu-id="12302-106">For an overview of how final-state-based multicast programming differs from change-based multicast programming, see [Multicast Programming](multicast-programming.md).</span></span>

<span data-ttu-id="12302-107">A tabela a seguir descreve os IOCTLs do Windows Sockets usados para programação de multicast no Windows.</span><span class="sxs-lookup"><span data-stu-id="12302-107">The following table describes the Windows Sockets IOCTLs used for multicast programming on Windows.</span></span> 

| <span data-ttu-id="12302-108">IOCTL</span><span class="sxs-lookup"><span data-stu-id="12302-108">IOCTL</span></span>                       | <span data-ttu-id="12302-109">Tipo de argumento</span><span class="sxs-lookup"><span data-stu-id="12302-109">Argument type</span></span>                                   |
|-----------------------------|-------------------------------------------------|
| <span data-ttu-id="12302-110">SIOCSMSFILTER</span><span class="sxs-lookup"><span data-stu-id="12302-110">SIOCSMSFILTER</span></span>               | <span data-ttu-id="12302-111">[**Grupo \_**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) Estrutura do filtro</span><span class="sxs-lookup"><span data-stu-id="12302-111">[**GROUP\_FILTER**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) structure</span></span> |
| <span data-ttu-id="12302-112">SIOCGMSFILTER</span><span class="sxs-lookup"><span data-stu-id="12302-112">SIOCGMSFILTER</span></span>               | <span data-ttu-id="12302-113">[**Grupo \_**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) Estrutura do filtro</span><span class="sxs-lookup"><span data-stu-id="12302-113">[**GROUP\_FILTER**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) structure</span></span> |
| <span data-ttu-id="12302-114">SIO \_ obter \_ \_ filtro multicast</span><span class="sxs-lookup"><span data-stu-id="12302-114">SIO\_GET\_MULTICAST\_FILTER</span></span> | <span data-ttu-id="12302-115">estrutura de [**\_ MsFilter IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)</span><span class="sxs-lookup"><span data-stu-id="12302-115">[**ip\_msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) structure</span></span>   |
| <span data-ttu-id="12302-116">SIO \_ definir \_ filtro de multicast \_</span><span class="sxs-lookup"><span data-stu-id="12302-116">SIO\_SET\_MULTICAST\_FILTER</span></span> | <span data-ttu-id="12302-117">estrutura de [**\_ MsFilter IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)</span><span class="sxs-lookup"><span data-stu-id="12302-117">[**ip\_msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) structure</span></span>   |



 

<span data-ttu-id="12302-118">Observe que os IOCTLs **SIOCSMSFILTER** e **SIOCGMSFILTER** estão disponíveis no Windows Vista e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="12302-118">Note that the **SIOCSMSFILTER** and **SIOCGMSFILTER** IOCTLS are available on Windows Vista and later.</span></span>

<span data-ttu-id="12302-119">O uso desses IOCTLs para a programação de multicast tem benefícios de desempenho ao trabalhar com listas de origem grandes.</span><span class="sxs-lookup"><span data-stu-id="12302-119">Using these IOCTLs for multicast programming has performance benefits when working with large source lists.</span></span> <span data-ttu-id="12302-120">Para obter mais informações sobre os parâmetros e configurações associados ao uso do SIO \_ obter \_ \_ filtro de multicast ou \_ \_ o filtro de multicast definido por Sio \_ , consulte a página de referência de [**\_ filtro de grupo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) .</span><span class="sxs-lookup"><span data-stu-id="12302-120">For more information about the parameters and settings associated with using SIO\_GET\_MULTICAST\_FILTER or SIO\_SET\_MULTICAST\_FILTER, consult the [**GROUP\_FILTER**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) reference page.</span></span> <span data-ttu-id="12302-121">Para obter mais informações sobre os parâmetros e as configurações associadas ao uso do SIO \_ obter \_ \_ filtro multicast ou \_ o sio definir \_ \_ filtro de multicast, consulte a página de referência de [**\_ MsFilter de IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) .</span><span class="sxs-lookup"><span data-stu-id="12302-121">For more information about the parameters and settings associated with using SIO\_GET\_MULTICAST\_FILTER or SIO\_SET\_MULTICAST\_FILTER, consult the [**ip\_msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) reference page.</span></span>

 

 



