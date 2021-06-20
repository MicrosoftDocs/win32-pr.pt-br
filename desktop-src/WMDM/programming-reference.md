---
title: Referência do WMDM
description: O SDK do Windows Media Gerenciador de Dispositivos consiste em uma coleção de interfaces, estruturas, enumerações e constantes. Use estes artigos de referência.
ms.assetid: 1d2260a8-bc9f-41b3-a3b0-0176b45fff1f
keywords:
- Windows Media Gerenciador de Dispositivos, referência de programação
- Gerenciador de Dispositivos, referência de programação
- Windows Media Gerenciador de Dispositivos, aplicativos da área de trabalho
- Gerenciador de Dispositivos aplicativos da área de trabalho
- Windows Media Gerenciador de Dispositivos, provedores de serviços
- Gerenciador de Dispositivos, provedores de serviços
- aplicativos da área de trabalho, referência de programação
- provedores de serviços, referência de programação
- referência de programação, aplicativos da área de trabalho
- referência de programação, provedores de serviços
- referência de programação, windows media Gerenciador de Dispositivos
- referência para o Windows Media Gerenciador de Dispositivos, sobre
- referência para o Windows Media Gerenciador de Dispositivos,aplicativos da área de trabalho
- referência para o Windows Media Gerenciador de Dispositivos, provedores de serviços
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e624bbc445d5d5e376cad926248ae4ee4db17a6e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406519"
---
# <a name="wmdm-reference"></a><span data-ttu-id="535ac-118">Referência do WMDM</span><span class="sxs-lookup"><span data-stu-id="535ac-118">WMDM reference</span></span>

<span data-ttu-id="535ac-119">O SDK do Windows Media Gerenciador de Dispositivos consiste em uma coleção de interfaces, estruturas, enumerações e constantes.</span><span class="sxs-lookup"><span data-stu-id="535ac-119">The Windows Media Device Manager SDK consists of a collection of interfaces, structures, enumerations, and constants.</span></span> <span data-ttu-id="535ac-120">A seção de referência divide as interfaces em grupos de acordo com o tipo de objeto que as usa.</span><span class="sxs-lookup"><span data-stu-id="535ac-120">The reference section divides the interfaces into groups according to the type of object that uses them.</span></span>



| <span data-ttu-id="535ac-121">Seção</span><span class="sxs-lookup"><span data-stu-id="535ac-121">Section</span></span>                                                                                                    | <span data-ttu-id="535ac-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="535ac-122">Description</span></span>                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="535ac-123">Interfaces para aplicativos</span><span class="sxs-lookup"><span data-stu-id="535ac-123">Interfaces for Applications</span></span>](interfaces-for-applications.md)                                             | <span data-ttu-id="535ac-124">Descreve interfaces que são usadas ou implementadas somente por aplicativos da área de trabalho, Windows Media Player plug-ins ou objetos COM que precisam de acesso de alto nível a um dispositivo portátil.</span><span class="sxs-lookup"><span data-stu-id="535ac-124">Describes interfaces that are used or implemented only by desktop applications, Windows Media Player plug-ins, or COM objects that need high-level access to a portable device.</span></span>                     |
| [<span data-ttu-id="535ac-125">Interfaces para provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="535ac-125">Interfaces for Service Providers</span></span>](interfaces-for-service-providers.md)                                   | <span data-ttu-id="535ac-126">Descreve interfaces que são usadas ou implementadas somente por provedores de serviços, que lidam com a comunicação real de baixo nível com um dispositivo portátil.</span><span class="sxs-lookup"><span data-stu-id="535ac-126">Describes interfaces that are used or implemented only by service providers, which handle the actual low-level communication with a portable device.</span></span>                                                |
| [<span data-ttu-id="535ac-127">Interfaces de DRM-Implemented mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="535ac-127">Windows Media DRM-Implemented Interfaces</span></span>](windows-media-drm-implemented-interfaces.md)                   | <span data-ttu-id="535ac-128">Descreve as interfaces que não se destinam a serem implementadas por provedores de serviços de terceiros, mas que são implementadas e chamadas internamente pelo DRM de Mídia do Windows e pelo Windows Media Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="535ac-128">Describes interfaces that are not intended to be implemented by third-party service providers, but are implemented and called internally by the Windows Media DRM and Windows Media Device Manager.</span></span> |
| [<span data-ttu-id="535ac-129">Interfaces para provedores de serviços e aplicativos</span><span class="sxs-lookup"><span data-stu-id="535ac-129">Interfaces for Service Providers and Applications</span></span>](interfaces-for-service-providers-and-applications.md) | <span data-ttu-id="535ac-130">Descreve interfaces que podem ser usadas por aplicativos ou por provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="535ac-130">Describes interfaces that can be used either by applications or by service providers.</span></span>                                                                                                               |
| [<span data-ttu-id="535ac-131">Interfaces para provedores de conteúdo seguros</span><span class="sxs-lookup"><span data-stu-id="535ac-131">Interfaces for Secure Content Providers</span></span>](interfaces-for-secure-content-providers.md)                     | <span data-ttu-id="535ac-132">Descreve as interfaces que devem ser implementadas por um dispositivo ou aplicativo que usará conteúdo protegido por DRM.</span><span class="sxs-lookup"><span data-stu-id="535ac-132">Describes interfaces that must be implemented by a device or application that will use DRM-protected content.</span></span>                                                                                       |
| [<span data-ttu-id="535ac-133">Estruturas</span><span class="sxs-lookup"><span data-stu-id="535ac-133">Structures</span></span>](structures.md)                                                                               | <span data-ttu-id="535ac-134">Descreve estruturas usadas para métodos de Gerenciador de Dispositivos Windows Media.</span><span class="sxs-lookup"><span data-stu-id="535ac-134">Describes structures used for Windows Media Device Manager methods.</span></span>                                                                                                                                 |
| [<span data-ttu-id="535ac-135">Tipos de enumeração</span><span class="sxs-lookup"><span data-stu-id="535ac-135">Enumeration Types</span></span>](enumeration-types.md)                                                                 | <span data-ttu-id="535ac-136">Descreve enumerações usadas para métodos de Gerenciador de Dispositivos Windows Media.</span><span class="sxs-lookup"><span data-stu-id="535ac-136">Describes enumerations used for Windows Media Device Manager methods.</span></span>                                                                                                                               |
| [<span data-ttu-id="535ac-137">Constantes de metadados</span><span class="sxs-lookup"><span data-stu-id="535ac-137">Metadata Constants</span></span>](metadata-constants.md)                                                               | <span data-ttu-id="535ac-138">Descreve as constantes definidas pelo SDK do Windows Media Gerenciador de Dispositivos para definir ou recuperar várias propriedades de metadados para um dispositivo ou objeto no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="535ac-138">Describes the constants defined by the Windows Media Device Manager SDK for setting or retrieving various metadata properties for a device or object on the device.</span></span>                                 |
| [<span data-ttu-id="535ac-139">Códigos de Erro</span><span class="sxs-lookup"><span data-stu-id="535ac-139">Error Codes</span></span>](error-codes.md)                                                                             | <span data-ttu-id="535ac-140">Descreve os códigos de erro que podem ser retornados pelos métodos do SDK do Windows Media Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="535ac-140">Describes the error codes that can be returned by Windows Media Device Manager SDK methods.</span></span>                                                                                                         |



 

 

 




