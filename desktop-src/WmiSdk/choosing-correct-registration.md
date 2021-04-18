---
description: O WMI dá suporte a modelos de Threading diferentes, dependendo de como o provedor é hospedado e do tipo de funcionalidade do provedor, como classe ou propriedade.
ms.assetid: cce3faf5-7bfe-46fe-9205-57398ab9dae9
ms.tgt_platform: multiple
title: Escolhendo o registro correto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49b66ec0266b5482dcff13a7de05a5bd1414312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771420"
---
# <a name="choosing-correct-registration"></a><span data-ttu-id="bc067-103">Escolhendo o registro correto</span><span class="sxs-lookup"><span data-stu-id="bc067-103">Choosing Correct Registration</span></span>

<span data-ttu-id="bc067-104">O WMI dá suporte a modelos de Threading diferentes, dependendo de como o provedor é hospedado e do tipo de funcionalidade do provedor, como [classe](writing-a-class-provider.md) ou [Propriedade](writing-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="bc067-104">WMI supports different threading models depending on how the provider is hosted and the type of provider functionality, such as [Class](writing-a-class-provider.md) or [Property](writing-a-property-provider.md).</span></span> <span data-ttu-id="bc067-105">Por exemplo, os [*provedores dissociados*](gloss-d.md) não oferecem suporte a todos os tipos de funcionalidade do provedor.</span><span class="sxs-lookup"><span data-stu-id="bc067-105">For example, [*decoupled providers*](gloss-d.md) do not support all the types of provider functionality.</span></span> <span data-ttu-id="bc067-106">Para obter mais informações sobre modelos de hospedagem diferentes e como configurá-los, consulte [provedor de hospedagem e segurança](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="bc067-106">For more information about different hosting models and how to configure them, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

## <a name="in-process-providers"></a><span data-ttu-id="bc067-107">Provedores de In-Process</span><span class="sxs-lookup"><span data-stu-id="bc067-107">In-Process Providers</span></span>

<span data-ttu-id="bc067-108">Os provedores em processo são executados em um processo de host compartilhado, Wmiprvse.exe.</span><span class="sxs-lookup"><span data-stu-id="bc067-108">In-process providers run in a shared host process, Wmiprvse.exe.</span></span> <span data-ttu-id="bc067-109">A maioria dos tipos de provedor em processo usa o modelo de MTA (multithreaded apartment).</span><span class="sxs-lookup"><span data-stu-id="bc067-109">Most in-process provider types use the multithreaded apartment (MTA) model.</span></span>

<span data-ttu-id="bc067-110">O modelo MTA tem suporte para os seguintes tipos de funcionalidade de provedor:</span><span class="sxs-lookup"><span data-stu-id="bc067-110">The MTA model is supported for the following types of provider functionality:</span></span>

-   [<span data-ttu-id="bc067-111">Provedor de classe</span><span class="sxs-lookup"><span data-stu-id="bc067-111">Class Provider</span></span>](writing-a-class-provider.md)
-   [<span data-ttu-id="bc067-112">Provedor de instância</span><span class="sxs-lookup"><span data-stu-id="bc067-112">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="bc067-113">Provedor de método</span><span class="sxs-lookup"><span data-stu-id="bc067-113">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="bc067-114">Provedor de propriedades</span><span class="sxs-lookup"><span data-stu-id="bc067-114">Property Provider</span></span>](writing-a-property-provider.md)
-   [<span data-ttu-id="bc067-115">Provedor de eventos</span><span class="sxs-lookup"><span data-stu-id="bc067-115">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="bc067-116">Provedor de consumidor de eventos</span><span class="sxs-lookup"><span data-stu-id="bc067-116">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

<span data-ttu-id="bc067-117">O modelo STA (single-threaded apartment) tem suporte para alguns tipos de funcionalidade de provedor:</span><span class="sxs-lookup"><span data-stu-id="bc067-117">The single-threaded apartment (STA) model is supported for some types of provider functionality:</span></span>

-   [<span data-ttu-id="bc067-118">Provedor de instância</span><span class="sxs-lookup"><span data-stu-id="bc067-118">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="bc067-119">Provedor de método</span><span class="sxs-lookup"><span data-stu-id="bc067-119">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="bc067-120">Provedor de eventos</span><span class="sxs-lookup"><span data-stu-id="bc067-120">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="bc067-121">Provedor de consumidor de eventos</span><span class="sxs-lookup"><span data-stu-id="bc067-121">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

## <a name="out-of-process-providers"></a><span data-ttu-id="bc067-122">Provedores fora do processo</span><span class="sxs-lookup"><span data-stu-id="bc067-122">Out-of-Process Providers</span></span>

<span data-ttu-id="bc067-123">Provedores que são hospedados em um host de serviço compartilhado diferente dão suporte à seguinte funcionalidade de provedor:</span><span class="sxs-lookup"><span data-stu-id="bc067-123">Providers that are hosted in a different shared service host support the following provider functionality:</span></span>

-   [<span data-ttu-id="bc067-124">Provedor de classe</span><span class="sxs-lookup"><span data-stu-id="bc067-124">Class Provider</span></span>](writing-a-class-provider.md)
-   [<span data-ttu-id="bc067-125">Provedor de instância</span><span class="sxs-lookup"><span data-stu-id="bc067-125">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="bc067-126">Provedor de método</span><span class="sxs-lookup"><span data-stu-id="bc067-126">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="bc067-127">Provedor de propriedades</span><span class="sxs-lookup"><span data-stu-id="bc067-127">Property Provider</span></span>](writing-a-property-provider.md)
-   [<span data-ttu-id="bc067-128">Provedor de eventos</span><span class="sxs-lookup"><span data-stu-id="bc067-128">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="bc067-129">Provedor de consumidor de eventos</span><span class="sxs-lookup"><span data-stu-id="bc067-129">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

<span data-ttu-id="bc067-130">Para obter mais informações sobre hosts de serviço compartilhado, consulte [Hospedagem de provedor e segurança](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="bc067-130">For more information about shared service hosts, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

## <a name="decoupled-providers"></a><span data-ttu-id="bc067-131">Provedores dissociados</span><span class="sxs-lookup"><span data-stu-id="bc067-131">Decoupled Providers</span></span>

<span data-ttu-id="bc067-132">Os provedores dissociados são hospedados em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bc067-132">Decoupled providers are hosted in an application.</span></span> <span data-ttu-id="bc067-133">Para obter mais informações, consulte [incorporando um provedor em um aplicativo](incorporating-a-provider-in-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="bc067-133">For more information, see [Incorporating a Provider in an Application](incorporating-a-provider-in-an-application.md).</span></span> <span data-ttu-id="bc067-134">Os provedores criados usando o WMI no .NET Framework são separados.</span><span class="sxs-lookup"><span data-stu-id="bc067-134">Providers created using WMI in the .NET Framework are decoupled.</span></span> <span data-ttu-id="bc067-135">Os provedores dissociados oferecem suporte à seguinte funcionalidade de provedor:</span><span class="sxs-lookup"><span data-stu-id="bc067-135">Decoupled providers support the following provider functionality:</span></span>

-   [<span data-ttu-id="bc067-136">Provedor de instância</span><span class="sxs-lookup"><span data-stu-id="bc067-136">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="bc067-137">Provedor de método</span><span class="sxs-lookup"><span data-stu-id="bc067-137">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="bc067-138">Provedor de eventos</span><span class="sxs-lookup"><span data-stu-id="bc067-138">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="bc067-139">Provedor de consumidor de eventos</span><span class="sxs-lookup"><span data-stu-id="bc067-139">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

## <a name="related-topics"></a><span data-ttu-id="bc067-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bc067-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc067-141">Desenvolvendo um provedor WMI</span><span class="sxs-lookup"><span data-stu-id="bc067-141">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="bc067-142">Hospedagem e segurança de provedor</span><span class="sxs-lookup"><span data-stu-id="bc067-142">Provider Hosting and Security</span></span>](provider-hosting-and-security.md)
</dt> </dl>

 

 



