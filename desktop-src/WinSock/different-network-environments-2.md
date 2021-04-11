---
description: Vários ambientes de rede afetam o comportamento em redes de um aplicativo.
ms.assetid: 4a530a17-5e61-4730-95f5-233261b4ceb0
title: Diferentes ambientes de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63dca7eacd48973a9106e6a1e3a4eb5959afcfef
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104172439"
---
# <a name="different-network-environments"></a><span data-ttu-id="52f80-103">Diferentes ambientes de rede</span><span class="sxs-lookup"><span data-stu-id="52f80-103">Different Network Environments</span></span>

<span data-ttu-id="52f80-104">Vários ambientes de rede afetam o comportamento em redes de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="52f80-104">Several network environments affect the networked behavior of an application.</span></span> <span data-ttu-id="52f80-105">As propriedades que diferenciam os ambientes de rede incluem largura de banda baixa versus alta e RTT baixa versus alta.</span><span class="sxs-lookup"><span data-stu-id="52f80-105">Properties that differentiate network environments include low versus high bandwidth, and low versus high RTT.</span></span> <span data-ttu-id="52f80-106">Os ambientes de rede afetam os aplicativos transacionais e de streaming de maneiras diferentes.</span><span class="sxs-lookup"><span data-stu-id="52f80-106">Network environments affect transactional and streaming applications in different ways.</span></span> <span data-ttu-id="52f80-107">Os aplicativos transacionais são mais sensíveis ao RTT; os aplicativos de streaming são mais sensíveis aos produtos de atraso de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="52f80-107">Transactional applications are more sensitive to RTT; streaming applications are more sensitive to bandwidth-delay products.</span></span>

![Diagrama que mostra como os diferentes ambientes de rede afetam o comportamento do serviço em rede de um aplicativo.](images/hperf-1.png)

<span data-ttu-id="52f80-109">Redes discadas e algumas redes sem fio têm uma variável RTT.</span><span class="sxs-lookup"><span data-stu-id="52f80-109">Dial-up networks and some wireless networks have a variable RTT.</span></span> <span data-ttu-id="52f80-110">Redes satélite geralmente têm uma largura de banda assimétrica entre upstream e downstream.</span><span class="sxs-lookup"><span data-stu-id="52f80-110">Satellite networks generally have an asymmetric bandwidth between upstream and downstream.</span></span> <span data-ttu-id="52f80-111">A LAN sem fio e xDSL são bons exemplos de redes com produtos de atraso de largura de banda semelhantes ao da Fast Ethernet.</span><span class="sxs-lookup"><span data-stu-id="52f80-111">Wireless LAN and xDSL are good examples of networks with bandwidth-delay products similar to that of Fast Ethernet.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52f80-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="52f80-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52f80-113">Aplicativos de alto desempenho do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="52f80-113">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="52f80-114">Dimensões de desempenho</span><span class="sxs-lookup"><span data-stu-id="52f80-114">Performance Dimensions</span></span>](performance-dimensions-2.md)
</dt> </dl>

 

 



