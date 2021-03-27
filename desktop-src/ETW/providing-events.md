---
description: Provedores são aplicativos que contêm a instrumentação de rastreamento de eventos.
ms.assetid: b522f16d-8d61-4db3-9194-d965b6d859ec
title: Fornecendo eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc53daa602662dfabd163560e8e9d69a888be610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967421"
---
# <a name="providing-events"></a><span data-ttu-id="e3e95-103">Fornecendo eventos</span><span class="sxs-lookup"><span data-stu-id="e3e95-103">Providing Events</span></span>

<span data-ttu-id="e3e95-104">Provedores são aplicativos que contêm a instrumentação de rastreamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="e3e95-104">Providers are applications that contain event tracing instrumentation.</span></span> <span data-ttu-id="e3e95-105">Depois que um provedor se registra, um controlador pode habilitar ou desabilitar o rastreamento de eventos no provedor.</span><span class="sxs-lookup"><span data-stu-id="e3e95-105">After a provider registers itself, a controller can then enable or disable event tracing in the provider.</span></span> <span data-ttu-id="e3e95-106">O provedor define sua interpretação de ser habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="e3e95-106">The provider defines its interpretation of being enabled or disabled.</span></span> <span data-ttu-id="e3e95-107">Geralmente, um provedor habilitado gera eventos e um provedor desabilitado não.</span><span class="sxs-lookup"><span data-stu-id="e3e95-107">Generally, an enabled provider generates events, and a disabled provider does not.</span></span> <span data-ttu-id="e3e95-108">Isso permite que você adicione o rastreamento de eventos ao seu aplicativo sem exigir que ele gere eventos o tempo todo.</span><span class="sxs-lookup"><span data-stu-id="e3e95-108">This lets you add event tracing to your application without requiring that it generate events all the time.</span></span>

<span data-ttu-id="e3e95-109">Esta seção mostra como:</span><span class="sxs-lookup"><span data-stu-id="e3e95-109">This section shows you how to:</span></span>

-   [<span data-ttu-id="e3e95-110">Eventos de gravação</span><span class="sxs-lookup"><span data-stu-id="e3e95-110">Write events</span></span>](writing-events.md)
-   [<span data-ttu-id="e3e95-111">Gravar eventos relacionados</span><span class="sxs-lookup"><span data-stu-id="e3e95-111">Write related events</span></span>](writing-related-events-in-an-end-to-end-scenario.md)
-   [<span data-ttu-id="e3e95-112">Publicar seu esquema de eventos para compartilhar com consumidores</span><span class="sxs-lookup"><span data-stu-id="e3e95-112">Publish your event schema to share with consumers</span></span>](publishing-your-event-schema.md)

<span data-ttu-id="e3e95-113">Para obter informações sobre como controlar sessões de rastreamento de eventos, consulte [controlando sessões de rastreamento de eventos](controlling-event-tracing-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="e3e95-113">For information about controlling event tracing sessions, see [Controlling Event Tracing Sessions](controlling-event-tracing-sessions.md).</span></span> <span data-ttu-id="e3e95-114">Para obter informações sobre como consumir eventos de um provedor de rastreamento de eventos, consulte [consumindo eventos](consuming-events.md).</span><span class="sxs-lookup"><span data-stu-id="e3e95-114">For information about consuming events from an event trace provider, see [Consuming Events](consuming-events.md).</span></span>

 

 



