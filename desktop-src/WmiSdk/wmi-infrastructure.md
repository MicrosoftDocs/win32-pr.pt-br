---
description: Na infraestrutura do WMI, o serviço WMI (Winmgmt) é o componente do sistema operacional que atua como o mediador entre os aplicativos de gerenciamento e os provedores de dados WMI. O repositório WMI é uma área de armazenamento para dados estáticos relacionados ao WMI.
ms.assetid: 6ef157be-fb75-4453-bc20-4568a3dc18c0
ms.tgt_platform: multiple
title: Infraestrutura WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4370af9ec062ffa845d54eafda054357a76dc07c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764361"
---
# <a name="wmi-infrastructure"></a><span data-ttu-id="f5447-104">Infraestrutura WMI</span><span class="sxs-lookup"><span data-stu-id="f5447-104">WMI Infrastructure</span></span>

<span data-ttu-id="f5447-105">Na infraestrutura do WMI, o serviço WMI (Winmgmt) é o componente do sistema operacional que atua como o mediador entre os aplicativos de gerenciamento e os [*provedores*](gloss-p.md)de dados WMI.</span><span class="sxs-lookup"><span data-stu-id="f5447-105">In the WMI infrastructure, the WMI service (Winmgmt) is the operating system component that acts as the mediator between management applications and WMI data [*providers*](gloss-p.md).</span></span> <span data-ttu-id="f5447-106">O [*repositório WMI*](gloss-w.md) é uma área de armazenamento para dados estáticos relacionados ao WMI.</span><span class="sxs-lookup"><span data-stu-id="f5447-106">The [*WMI repository*](gloss-w.md) is a storage area for WMI-related static data.</span></span>

<span data-ttu-id="f5447-107">O serviço WMI é implementado como um processo de serviço dentro de um processo de host de serviço compartilhado (SVCHOST).</span><span class="sxs-lookup"><span data-stu-id="f5447-107">The WMI service is implemented as a service process within a shared service host process (SVCHOST).</span></span> <span data-ttu-id="f5447-108">Para obter mais informações, consulte [provedor de hospedagem e segurança](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="f5447-108">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

<span data-ttu-id="f5447-109">O serviço WMI é iniciado quando o primeiro aplicativo de gerenciamento ou script faz uma chamada para conectar-se a um namespace WMI.</span><span class="sxs-lookup"><span data-stu-id="f5447-109">The WMI service starts when the first management application or script makes a call to connect to a WMI namespace.</span></span> <span data-ttu-id="f5447-110">Dependendo da configuração, o serviço WMI pode desligar ou entrar em um perfil de memória insuficiente quando não está sendo chamado por um aplicativo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="f5447-110">Depending on the setup, the WMI service may shut down or go into a low memory profile when not being called by a management application.</span></span>

<span data-ttu-id="f5447-111">O serviço WMI interage com aplicativos de gerenciamento por meio da interface COM.</span><span class="sxs-lookup"><span data-stu-id="f5447-111">The WMI service interacts with management applications through the COM interface.</span></span> <span data-ttu-id="f5447-112">Quando um aplicativo faz uma solicitação por meio da interface, o WMI determina se a solicitação é para dados estáticos ou dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="f5447-112">When an application makes a request through the interface, WMI determines whether the request is for static or dynamic data.</span></span> <span data-ttu-id="f5447-113">Se a solicitação envolver dados estáticos, como o nome de um objeto gerenciado, o WMI recuperará os dados do repositório.</span><span class="sxs-lookup"><span data-stu-id="f5447-113">If the request involves static data, such as the name of a managed object, WMI retrieves the data from the repository.</span></span> <span data-ttu-id="f5447-114">Se a solicitação envolver dados dinâmicos, como a quantidade de memória que um objeto gerenciado está usando no momento, o WMI passará a solicitação para um provedor.</span><span class="sxs-lookup"><span data-stu-id="f5447-114">If the request involves dynamic data, such as the amount of memory a managed object is currently using, WMI passes the request on to a provider.</span></span>

<span data-ttu-id="f5447-115">Os provedores registram seu local com o serviço WMI, que permite ao WMI rotear solicitações de dados.</span><span class="sxs-lookup"><span data-stu-id="f5447-115">Providers register their location with the WMI service, which allows WMI to route data requests.</span></span> <span data-ttu-id="f5447-116">Um provedor também registra o suporte para operações específicas, como recuperação de dados, modificação, exclusão, enumeração ou processamento de consulta.</span><span class="sxs-lookup"><span data-stu-id="f5447-116">A provider also registers support for particular operations, such as data retrieval, modification, deletion, enumeration, or query processing.</span></span> <span data-ttu-id="f5447-117">O serviço WMI usa as informações de registro do provedor para corresponder às solicitações do aplicativo com o provedor apropriado.</span><span class="sxs-lookup"><span data-stu-id="f5447-117">The WMI service uses the provider registration information to match application requests with the appropriate provider.</span></span> <span data-ttu-id="f5447-118">O WMI também usa as informações de registro para carregar e descarregar provedores, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="f5447-118">WMI also uses the registration information to load and unload providers, as necessary.</span></span> <span data-ttu-id="f5447-119">Quando um provedor termina de processar uma solicitação, o provedor retorna o resultado para o serviço WMI.</span><span class="sxs-lookup"><span data-stu-id="f5447-119">When a provider finishes processing a request, the provider returns the result back to the WMI service.</span></span> <span data-ttu-id="f5447-120">Em seguida, o WMI encaminha o resultado para o aplicativo por meio da interface COM.</span><span class="sxs-lookup"><span data-stu-id="f5447-120">WMI then forwards the result on to the application through the COM interface.</span></span> <span data-ttu-id="f5447-121">Para obter mais informações, consulte [fornecendo dados ao WMI](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="f5447-121">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="f5447-122">O WMI usa o ETW ( [rastreamento de eventos](/windows/desktop/ETW/event-tracing-portal) ) para registrar a atividade do serviço WMI.</span><span class="sxs-lookup"><span data-stu-id="f5447-122">WMI uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) to record WMI service activity.</span></span>

<span data-ttu-id="f5447-123">Como a infraestrutura manipula todo o tráfego entre os provedores e os aplicativos de gerenciamento, a infraestrutura fornece os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="f5447-123">Because the infrastructure handles all traffic between the providers and the management applications, the infrastructure provides the following features:</span></span>

-   <span data-ttu-id="f5447-124">Suporte à notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="f5447-124">Event Notification Support</span></span>

    <span data-ttu-id="f5447-125">Para obter mais informações, consulte [monitorando eventos](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="f5447-125">For more information, see [Monitoring Events](monitoring-events.md).</span></span>

-   <span data-ttu-id="f5447-126">Suporte à linguagem de consulta</span><span class="sxs-lookup"><span data-stu-id="f5447-126">Query Language Support</span></span>

    <span data-ttu-id="f5447-127">Para obter mais informações, consulte [consultando com WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="f5447-127">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>

-   <span data-ttu-id="f5447-128">Suporte de segurança</span><span class="sxs-lookup"><span data-stu-id="f5447-128">Security Support</span></span>

    <span data-ttu-id="f5447-129">Para obter mais informações, consulte [mantendo a segurança do WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="f5447-129">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

-   <span data-ttu-id="f5447-130">Script de acesso a dados do contador de desempenho</span><span class="sxs-lookup"><span data-stu-id="f5447-130">Scripting Access to Performance Counter Data</span></span>

    <span data-ttu-id="f5447-131">Para obter mais informações, consulte [monitorando dados de desempenho](monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="f5447-131">For more information, see [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5447-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5447-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5447-133">Arquitetura do WMI</span><span class="sxs-lookup"><span data-stu-id="f5447-133">WMI Architecture</span></span>](wmi-architecture.md)
</dt> </dl>

 

 
