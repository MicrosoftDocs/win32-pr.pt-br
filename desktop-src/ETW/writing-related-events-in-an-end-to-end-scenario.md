---
description: O ETW fornece uma maneira de agrupar eventos relacionados de mais de um componente.
ms.assetid: 2a85e4af-a1fe-4c28-8ce2-14d15deaa820
title: Gravando eventos relacionados em um cenário de ponta a ponta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d27b3455ffe71c6d657e935e6f93dc2dc39392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967454"
---
# <a name="writing-related-events-in-an-end-to-end-scenario"></a><span data-ttu-id="5770a-103">Gravando eventos relacionados em um cenário de ponta a ponta</span><span class="sxs-lookup"><span data-stu-id="5770a-103">Writing Related Events in an End-to-End Scenario</span></span>

<span data-ttu-id="5770a-104">O ETW fornece uma maneira de agrupar eventos relacionados de mais de um componente.</span><span class="sxs-lookup"><span data-stu-id="5770a-104">ETW provides a way to group related events from more than one component.</span></span> <span data-ttu-id="5770a-105">Por exemplo, se vários componentes (no mesmo computador ou em computadores diferentes) estiverem envolvidos no processamento dos mesmos dados e cada componente registrar eventos para sua parte da atividade, você poderá agrupar todos os eventos relacionados juntos.</span><span class="sxs-lookup"><span data-stu-id="5770a-105">For example, if several components (either on the same computer or on different computers) are involved in processing the same data, and each component logs events for their portion of the activity, you can group all of the related events together.</span></span> <span data-ttu-id="5770a-106">Isso permitirá que um consumidor consuma todos os eventos, desde o início do processo até o fim do processo.</span><span class="sxs-lookup"><span data-stu-id="5770a-106">This will allow a consumer to consume all of the events, from the beginning of the process to the end of the process.</span></span>

<span data-ttu-id="5770a-107">Para gravar eventos relacionados em um provedor [baseado em manifesto](about-event-tracing.md) , consulte [gravando eventos relacionados em um provedor baseado em manifesto](writing-related-events-in-a-manifest-base-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5770a-107">To write related events in a [manifest-based](about-event-tracing.md) provider, see [Writing Related Events in a Manifest-based Provider](writing-related-events-in-a-manifest-base-provider.md).</span></span>

<span data-ttu-id="5770a-108">Para gravar eventos relacionados em um provedor [clássico](about-event-tracing.md) , consulte [gravando eventos relacionados em um provedor clássico](tracing-event-instances.md).</span><span class="sxs-lookup"><span data-stu-id="5770a-108">To write related events in a [classic](about-event-tracing.md) provider, see [Writing Related Events in a Classic Provider](tracing-event-instances.md).</span></span>

 

 



