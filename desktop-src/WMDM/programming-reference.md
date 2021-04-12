---
title: Referência de WMDM
description: Referência de programação
ms.assetid: 1d2260a8-bc9f-41b3-a3b0-0176b45fff1f
keywords:
- Gerenciador de Dispositivos de mídia do Windows, referência de programação
- Gerenciador de Dispositivos, referência de programação
- Windows Media Gerenciador de Dispositivos, aplicativos de área de trabalho
- Gerenciador de Dispositivos, aplicativos de área de trabalho
- Windows Media Gerenciador de Dispositivos, provedores de serviços
- Gerenciador de Dispositivos, provedores de serviços
- aplicativos de área de trabalho, referência de programação
- provedores de serviços, referência de programação
- referência de programação, aplicativos de área de trabalho
- referência de programação, provedores de serviço
- referência de programação, Windows Media Gerenciador de Dispositivos
- referência para Windows Media Gerenciador de Dispositivos, sobre
- referência para Windows Media Gerenciador de Dispositivos, aplicativos de área de trabalho
- referência para Windows Media Gerenciador de Dispositivos, provedores de serviços
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1498d42e65de99abc1d32895f3628d93502c70f
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104365319"
---
# <a name="wmdm-reference"></a><span data-ttu-id="8d3b9-117">Referência de WMDM</span><span class="sxs-lookup"><span data-stu-id="8d3b9-117">WMDM reference</span></span>

<span data-ttu-id="8d3b9-118">O SDK do Windows Media Gerenciador de Dispositivos consiste em uma coleção de interfaces, estruturas, enumerações e constantes.</span><span class="sxs-lookup"><span data-stu-id="8d3b9-118">The Windows Media Device Manager SDK consists of a collection of interfaces, structures, enumerations, and constants.</span></span> <span data-ttu-id="8d3b9-119">A seção de referência divide as interfaces em grupos de acordo com o tipo de objeto que as utiliza.</span><span class="sxs-lookup"><span data-stu-id="8d3b9-119">The reference section divides the interfaces into groups according to the type of object that uses them.</span></span>



| <span data-ttu-id="8d3b9-120">Seção</span><span class="sxs-lookup"><span data-stu-id="8d3b9-120">Section</span></span>                                                                                                    | <span data-ttu-id="8d3b9-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d3b9-121">Description</span></span>                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d3b9-122">Interfaces para aplicativos</span><span class="sxs-lookup"><span data-stu-id="8d3b9-122">Interfaces for Applications</span></span>](interfaces-for-applications.md)                                             | <span data-ttu-id="8d3b9-123">Descreve as interfaces que são usadas ou implementadas somente por aplicativos de área de trabalho, plug-ins do Windows Media Player ou objetos COM que precisam de acesso de alto nível a um dispositivo portátil.</span><span class="sxs-lookup"><span data-stu-id="8d3b9-123">Describes interfaces that are used or implemented only by desktop applications, Windows Media Player plug-ins, or COM objects that need high-level access to a portable device.</span></span>                     |
| [<span data-ttu-id="8d3b9-124">Interfaces para provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="8d3b9-124">Interfaces for Service Providers</span></span>](interfaces-for-service-providers.md)                                   | <span data-ttu-id="8d3b9-125">Descreve as interfaces que são usadas ou implementadas somente por provedores de serviço, que lidam com a comunicação de baixo nível real com um dispositivo portátil.</span><span class="sxs-lookup"><span data-stu-id="8d3b9-125">Describes interfaces that are used or implemented only by service providers, which handle the actual low-level communication with a portable device.</span></span>                                                |
| [<span data-ttu-id="8d3b9-126">Interfaces de DRM-Implemented de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="8d3b9-126">Windows Media DRM-Implemented Interfaces</span></span>](windows-media-drm-implemented-interfaces.md)                   | <span data-ttu-id="8d3b9-127">Descreve as interfaces que não devem ser implementadas por provedores de serviço de terceiros, mas são implementadas e chamadas internamente pela Windows Media DRM e Windows Media Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="8d3b9-127">Describes interfaces that are not intended to be implemented by third-party service providers, but are implemented and called internally by the Windows Media DRM and Windows Media Device Manager.</span></span> |
| [<span data-ttu-id="8d3b9-128">Interfaces para provedores de serviços e aplicativos</span><span class="sxs-lookup"><span data-stu-id="8d3b9-128">Interfaces for Service Providers and Applications</span></span>](interfaces-for-service-providers-and-applications.md) | <span data-ttu-id="8d3b9-129">Descreve as interfaces que podem ser usadas por aplicativos ou por provedores de serviço.</span><span class="sxs-lookup"><span data-stu-id="8d3b9-129">Describes interfaces that can be used either by applications or by service providers.</span></span>                                                                                                               |
| [<span data-ttu-id="8d3b9-130">Interfaces para provedores de conteúdo seguro</span><span class="sxs-lookup"><span data-stu-id="8d3b9-130">Interfaces for Secure Content Providers</span></span>](interfaces-for-secure-content-providers.md)                     | <span data-ttu-id="8d3b9-131">Descreve as interfaces que devem ser implementadas por um dispositivo ou aplicativo que usará conteúdo protegido por DRM.</span><span class="sxs-lookup"><span data-stu-id="8d3b9-131">Describes interfaces that must be implemented by a device or application that will use DRM-protected content.</span></span>                                                                                       |
| [<span data-ttu-id="8d3b9-132">Estruturas</span><span class="sxs-lookup"><span data-stu-id="8d3b9-132">Structures</span></span>](structures.md)                                                                               | <span data-ttu-id="8d3b9-133">Descreve estruturas usadas para os métodos de Gerenciador de Dispositivos de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="8d3b9-133">Describes structures used for Windows Media Device Manager methods.</span></span>                                                                                                                                 |
| [<span data-ttu-id="8d3b9-134">Tipos de enumeração</span><span class="sxs-lookup"><span data-stu-id="8d3b9-134">Enumeration Types</span></span>](enumeration-types.md)                                                                 | <span data-ttu-id="8d3b9-135">Descreve as enumerações usadas para os métodos de Gerenciador de Dispositivos de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="8d3b9-135">Describes enumerations used for Windows Media Device Manager methods.</span></span>                                                                                                                               |
| [<span data-ttu-id="8d3b9-136">Constantes de metadados</span><span class="sxs-lookup"><span data-stu-id="8d3b9-136">Metadata Constants</span></span>](metadata-constants.md)                                                               | <span data-ttu-id="8d3b9-137">Descreve as constantes definidas pelo SDK do Windows Media Gerenciador de Dispositivos para configurar ou recuperar várias propriedades de metadados para um dispositivo ou objeto no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d3b9-137">Describes the constants defined by the Windows Media Device Manager SDK for setting or retrieving various metadata properties for a device or object on the device.</span></span>                                 |
| [<span data-ttu-id="8d3b9-138">Códigos de Erro</span><span class="sxs-lookup"><span data-stu-id="8d3b9-138">Error Codes</span></span>](error-codes.md)                                                                             | <span data-ttu-id="8d3b9-139">Descreve os códigos de erro que podem ser retornados pelos métodos do SDK do Windows Media Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="8d3b9-139">Describes the error codes that can be returned by Windows Media Device Manager SDK methods.</span></span>                                                                                                         |



 

 

 




