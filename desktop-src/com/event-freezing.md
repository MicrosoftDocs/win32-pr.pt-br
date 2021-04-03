---
title: Congelamento de eventos
description: Congelamento de eventos
ms.assetid: 1e537503-f7e7-42f4-aa3c-3c71715b84fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e403448d53949c263b8e146961690de1200436c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822582"
---
# <a name="event-freezing"></a><span data-ttu-id="bb37d-103">Congelamento de eventos</span><span class="sxs-lookup"><span data-stu-id="bb37d-103">Event Freezing</span></span>

<span data-ttu-id="bb37d-104">Um contêiner pode notificar um controle de que ele não está pronto para responder a eventos chamando [**IOleControl:: FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) com **true**.</span><span class="sxs-lookup"><span data-stu-id="bb37d-104">A container can notify a control that it is not ready to respond to events by calling [**IOleControl::FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **TRUE**.</span></span> <span data-ttu-id="bb37d-105">Ele pode descongelar os eventos chamando **FreezeEvents** com **false**.</span><span class="sxs-lookup"><span data-stu-id="bb37d-105">It can unfreeze the events by calling **FreezeEvents** with **FALSE**.</span></span> <span data-ttu-id="bb37d-106">Quando um contêiner congela eventos, está congelando o processamento de eventos, não o recebimento de eventos; ou seja, um contêiner ainda pode receber eventos enquanto os eventos são congelados.</span><span class="sxs-lookup"><span data-stu-id="bb37d-106">When a container freezes events, it is freezing event processing, not event receiving; that is, a container can still receive events while events are frozen.</span></span> <span data-ttu-id="bb37d-107">Se um contêiner receber uma notificação de eventos enquanto seus eventos estiverem congelados, o contêiner deverá ignorar o evento.</span><span class="sxs-lookup"><span data-stu-id="bb37d-107">If a container receives an event notification while its events are frozen, the container should ignore the event.</span></span> <span data-ttu-id="bb37d-108">Nenhuma outra ação é apropriada.</span><span class="sxs-lookup"><span data-stu-id="bb37d-108">No other action is appropriate.</span></span>

<span data-ttu-id="bb37d-109">Um controle deve anotar a chamada de um contêiner para [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) com **true** se for importante para o controle que um evento não está perdido.</span><span class="sxs-lookup"><span data-stu-id="bb37d-109">A control should take note of a container's call to [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **TRUE** if it is important to the control that an event is not missed.</span></span> <span data-ttu-id="bb37d-110">Enquanto o processamento de eventos de um contêiner é congelado, um controle deve implementar uma das seguintes técnicas:</span><span class="sxs-lookup"><span data-stu-id="bb37d-110">While a container's event processing is frozen, a control should implement one of the following techniques:</span></span>

-   <span data-ttu-id="bb37d-111">Dispare os eventos no conhecimento completo de que o contêiner não executará nenhuma ação.</span><span class="sxs-lookup"><span data-stu-id="bb37d-111">Fire the events in the full knowledge that the container will take no action.</span></span>
-   <span data-ttu-id="bb37d-112">Descartar todos os eventos que o controle teria disparado.</span><span class="sxs-lookup"><span data-stu-id="bb37d-112">Discard all events that the control would have fired.</span></span>
-   <span data-ttu-id="bb37d-113">Enfileirar todos os eventos pendentes e disfire-los depois que o contêiner tiver chamado [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) com **false**.</span><span class="sxs-lookup"><span data-stu-id="bb37d-113">Queue up all pending events and fire them after the container has called [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **FALSE**.</span></span>
-   <span data-ttu-id="bb37d-114">Colocar em fila somente eventos relevantes ou importantes e disfire-los depois que o contêiner tiver chamado [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) com **false**.</span><span class="sxs-lookup"><span data-stu-id="bb37d-114">Queue up only relevant or important events and fire them after the container has called [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **FALSE**.</span></span>

<span data-ttu-id="bb37d-115">Cada técnica é aceitável e apropriada em circunstâncias diferentes.</span><span class="sxs-lookup"><span data-stu-id="bb37d-115">Each technique is acceptable and appropriate in different circumstances.</span></span> <span data-ttu-id="bb37d-116">O desenvolvedor de controle é responsável por determinar e implementar a técnica apropriada para a funcionalidade do controle.</span><span class="sxs-lookup"><span data-stu-id="bb37d-116">The control developer is responsible for determining and implementing the appropriate technique for the control's functionality.</span></span>

 

 




