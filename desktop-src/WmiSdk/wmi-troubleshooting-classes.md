---
description: O WMI fornece um conjunto de classes de solução de problemas que os scripts e aplicativos podem usar para obter informações sobre o estado interno do WMI durante as operações básicas do WMI e do provedor.
ms.assetid: 631e0cce-0e83-42e5-a381-e96b1f70d6f9
ms.tgt_platform: multiple
title: Classes de solução de problemas do WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65b3972ba59c80a1495916ab24a72f6e93bef8e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922776"
---
# <a name="wmi-troubleshooting-classes"></a><span data-ttu-id="f4beb-103">Classes de solução de problemas do WMI</span><span class="sxs-lookup"><span data-stu-id="f4beb-103">WMI Troubleshooting Classes</span></span>

<span data-ttu-id="f4beb-104">O WMI fornece um conjunto de classes de solução de problemas que os scripts e aplicativos podem usar para obter informações sobre o estado interno do WMI durante as operações básicas do WMI e do provedor.</span><span class="sxs-lookup"><span data-stu-id="f4beb-104">WMI supplies a set of troubleshooting classes that scripts and applications can use to get information about WMI internal state during WMI core and provider operations.</span></span> <span data-ttu-id="f4beb-105">Para obter mais informações sobre solução de problemas do WMI, consulte solução de problemas do [WMI](wmi-troubleshooting.md) e [configuração do provedor e classes de solução de problemas](provider-configuration-and-troubleshooting-classes.md).</span><span class="sxs-lookup"><span data-stu-id="f4beb-105">For more information about WMI troubleshooting, see [WMI Troubleshooting](wmi-troubleshooting.md) and [Provider Configuration and Troubleshooting Classes](provider-configuration-and-troubleshooting-classes.md).</span></span>

<span data-ttu-id="f4beb-106">O WMI tem várias classes básicas de solução de problemas para operações de provedor e núcleo do WMI:</span><span class="sxs-lookup"><span data-stu-id="f4beb-106">WMI has several basic troubleshooting classes for WMI core and provider operations:</span></span>

-   [<span data-ttu-id="f4beb-107">**\_Contadores de WmiProvider do MSFT \_**</span><span class="sxs-lookup"><span data-stu-id="f4beb-107">**MSFT\_WmiProvider\_Counters**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-counters)

    <span data-ttu-id="f4beb-108">Apenas uma dessas classes é encontrada em cada sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="f4beb-108">Only one of these classes is found on each computer system.</span></span> <span data-ttu-id="f4beb-109">Ele fornece contagens de vários tipos de operações de provedor nesse sistema.</span><span class="sxs-lookup"><span data-stu-id="f4beb-109">It provides counts of various kind of provider operations on that system.</span></span>

-   [<span data-ttu-id="f4beb-110">**\_WMISELFEVENT MSFT**</span><span class="sxs-lookup"><span data-stu-id="f4beb-110">**MSFT\_WmiSelfEvent**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)

    <span data-ttu-id="f4beb-111">As classes de solução de problemas de evento derivam de [**MSFT \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent).</span><span class="sxs-lookup"><span data-stu-id="f4beb-111">The event troubleshooting classes derive from [**MSFT\_WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent).</span></span> <span data-ttu-id="f4beb-112">As consultas dessa classe retornam instâncias de classes de evento, como [**MSFT \_ WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated) ou [**MSFT \_ WmiProvider \_ CreateInstanceEnumAsyncEvent \_ post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post).</span><span class="sxs-lookup"><span data-stu-id="f4beb-112">Queries of this class return instances of event classes such as [**MSFT\_WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated) or [**MSFT\_WmiProvider\_CreateInstanceEnumAsyncEvent\_Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post).</span></span>

    <span data-ttu-id="f4beb-113">A lista a seguir fornece links para diferentes categorias de classes de evento derivadas de [**MSFT \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent):</span><span class="sxs-lookup"><span data-stu-id="f4beb-113">The following list provides links to different categories of event classes derived from [**MSFT\_WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent):</span></span>

    -   [<span data-ttu-id="f4beb-114">Classes de solução de problemas de eventos do provedor</span><span class="sxs-lookup"><span data-stu-id="f4beb-114">Provider Event Troubleshooting Classes</span></span>](provider-event-troubleshooting-classes.md)
    -   [<span data-ttu-id="f4beb-115">Classes de solução de problemas do consumidorprovider</span><span class="sxs-lookup"><span data-stu-id="f4beb-115">ConsumerProvider Troubleshooting Classes</span></span>](consumerprovider-troubleshooting-classes.md)
    -   [<span data-ttu-id="f4beb-116">Classes de solução de problemas de eventos do serviço WMI</span><span class="sxs-lookup"><span data-stu-id="f4beb-116">WMI Service Event Troubleshooting Classes</span></span>](wmi-service-event-troubleshooting-classes.md)

## <a name="related-topics"></a><span data-ttu-id="f4beb-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f4beb-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4beb-118">Solução de problemas do WMI</span><span class="sxs-lookup"><span data-stu-id="f4beb-118">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="f4beb-119">Recebendo um evento WMI</span><span class="sxs-lookup"><span data-stu-id="f4beb-119">Receiving a WMI Event</span></span>](receiving-a-wmi-event.md)
</dt> </dl>

 

 
