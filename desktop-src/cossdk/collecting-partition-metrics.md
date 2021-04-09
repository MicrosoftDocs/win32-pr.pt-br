---
description: Coletando métricas de partição
ms.assetid: 2dc35011-24fa-49df-9cf8-96db2de39efa
title: Coletando métricas de partição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6467dfb9c891e7ae57505c8ec3815bfa99e49d8a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089059"
---
# <a name="collecting-partition-metrics"></a><span data-ttu-id="b483a-103">Coletando métricas de partição</span><span class="sxs-lookup"><span data-stu-id="b483a-103">Collecting Partition Metrics</span></span>

<span data-ttu-id="b483a-104">Em alguns casos, uma organização pode querer coletar informações sobre o uso do aplicativo COM+ para fins de monitoramento, planejamento de capacidade e contabilidade de recursos.</span><span class="sxs-lookup"><span data-stu-id="b483a-104">In some cases, an organization might want to collect information on COM+ application use for the purposes of monitoring, capacity planning, and resource accounting.</span></span>

<span data-ttu-id="b483a-105">Por exemplo, um provedor de serviços de aplicativo (ASP) pode querer cobrar um cliente pelo uso de recursos.</span><span class="sxs-lookup"><span data-stu-id="b483a-105">For example, an application service provider (ASP) might want to charge a customer for its resource usage.</span></span> <span data-ttu-id="b483a-106">Para fazer isso, o COM+ permite coletar informações de eventos e métricas em uma base por partição.</span><span class="sxs-lookup"><span data-stu-id="b483a-106">To do this, COM+ allows you to collect event and metrics information on a per-partition basis.</span></span>

<span data-ttu-id="b483a-107">A maneira de coletar essas informações para uma partição específica é especificando, para cada interface de instrumentação COM+, o membro de ID de partição dentro da estrutura de eventos padrão.</span><span class="sxs-lookup"><span data-stu-id="b483a-107">The way to collect this information for a specific partition is by specifying, for each COM+ instrumentation interface, the partition ID member within the standard event structure.</span></span> <span data-ttu-id="b483a-108">A estrutura de eventos é o primeiro valor de uma interface de instrumentação COM+.</span><span class="sxs-lookup"><span data-stu-id="b483a-108">The event structure is the first value of a COM+ instrumentation interface.</span></span> <span data-ttu-id="b483a-109">Para obter mais informações, consulte [interfaces de instrumentação com+](com--instrumentation-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="b483a-109">For more information, see [COM+ Instrumentation Interfaces](com--instrumentation-interfaces.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b483a-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b483a-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b483a-111">Configurando o cache de partição</span><span class="sxs-lookup"><span data-stu-id="b483a-111">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="b483a-112">Agrupando aplicativos em partições</span><span class="sxs-lookup"><span data-stu-id="b483a-112">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="b483a-113">Gerenciando partições locais</span><span class="sxs-lookup"><span data-stu-id="b483a-113">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="b483a-114">Gerenciando partições no Active Directory</span><span class="sxs-lookup"><span data-stu-id="b483a-114">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="b483a-115">Configurando direitos administrativos para uma partição</span><span class="sxs-lookup"><span data-stu-id="b483a-115">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



