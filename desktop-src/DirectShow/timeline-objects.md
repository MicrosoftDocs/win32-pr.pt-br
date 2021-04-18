---
description: Objetos de linha do tempo
ms.assetid: da426964-d5bd-45ca-a914-c19062f3564b
title: Objetos de linha do tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 580286b31afd77f064411dd29d60a62b80bfb51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750873"
---
# <a name="timeline-objects"></a><span data-ttu-id="624e3-103">Objetos de linha do tempo</span><span class="sxs-lookup"><span data-stu-id="624e3-103">Timeline Objects</span></span>

<span data-ttu-id="624e3-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="624e3-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="624e3-105">Cada tipo de objeto na linha do tempo — origem, controle, efeito e assim por diante — é um objeto COM distinto.</span><span class="sxs-lookup"><span data-stu-id="624e3-105">Each type of object in the timeline—source, track, effect, and so forth—is a distinct COM object.</span></span> <span data-ttu-id="624e3-106">No entanto, um aplicativo não os cria usando a função **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="624e3-106">However, an application does not create them using the **CoCreateInstance** function.</span></span> <span data-ttu-id="624e3-107">Em vez disso, ele chama o método [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) .</span><span class="sxs-lookup"><span data-stu-id="624e3-107">Instead, it calls the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span> <span data-ttu-id="624e3-108">Esse método cria um objeto do tipo solicitado, inicializa-o e retorna um ponteiro para o objeto.</span><span class="sxs-lookup"><span data-stu-id="624e3-108">This method creates an object of the requested type, initializes it, and returns a pointer to the object.</span></span> <span data-ttu-id="624e3-109">Para obter detalhes, consulte [construindo uma linha do tempo](constructing-a-timeline.md).</span><span class="sxs-lookup"><span data-stu-id="624e3-109">For details, see [Constructing a Timeline](constructing-a-timeline.md).</span></span>

<span data-ttu-id="624e3-110">Cada objeto Timeline expõe a interface [**IAMTimelineObj**](iamtimelineobj.md) .</span><span class="sxs-lookup"><span data-stu-id="624e3-110">Every timeline object exposes the [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span> <span data-ttu-id="624e3-111">Além disso, os vários tipos de objeto dão suporte a suas próprias interfaces especializadas:</span><span class="sxs-lookup"><span data-stu-id="624e3-111">In addition, the various object types support their own specialized interfaces:</span></span>

-   <span data-ttu-id="624e3-112">Origem: [ **IAMTimelineSrc**](iamtimelinesrc.md)</span><span class="sxs-lookup"><span data-stu-id="624e3-112">Source: [**IAMTimelineSrc**](iamtimelinesrc.md)</span></span>
-   <span data-ttu-id="624e3-113">Controle: [ **IAMTimelineTrack**](iamtimelinetrack.md)</span><span class="sxs-lookup"><span data-stu-id="624e3-113">Track: [**IAMTimelineTrack**](iamtimelinetrack.md)</span></span>
-   <span data-ttu-id="624e3-114">Composição: [ **IAMTimelineComp**](iamtimelinecomp.md)</span><span class="sxs-lookup"><span data-stu-id="624e3-114">Composition: [**IAMTimelineComp**](iamtimelinecomp.md)</span></span>
-   <span data-ttu-id="624e3-115">Grupo: [**IAMTimelineComp**](iamtimelinecomp.md), [**IAMTimelineGroup**](iamtimelinegroup.md)</span><span class="sxs-lookup"><span data-stu-id="624e3-115">Group: [**IAMTimelineComp**](iamtimelinecomp.md), [**IAMTimelineGroup**](iamtimelinegroup.md)</span></span>
-   <span data-ttu-id="624e3-116">Efeito: [ **IAMTimelineEffect**](iamtimelineeffect.md)</span><span class="sxs-lookup"><span data-stu-id="624e3-116">Effect: [**IAMTimelineEffect**](iamtimelineeffect.md)</span></span>
-   <span data-ttu-id="624e3-117">Transição: [ **IAMTimelineTrans**](iamtimelinetrans.md)</span><span class="sxs-lookup"><span data-stu-id="624e3-117">Transition: [**IAMTimelineTrans**](iamtimelinetrans.md)</span></span>

<span data-ttu-id="624e3-118">Observe que os grupos são um tipo de composição, portanto, dão suporte a [**IAMTimelineComp**](iamtimelinecomp.md), bem como sua própria interface [**IAMTimelineGroup**](iamtimelinegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="624e3-118">Note that groups are a type of composition, so they support [**IAMTimelineComp**](iamtimelinecomp.md), as well as their own [**IAMTimelineGroup**](iamtimelinegroup.md) interface.</span></span>

<span data-ttu-id="624e3-119">Além das interfaces listadas anteriormente, os objetos de linha do tempo expõem outras interfaces secundárias.</span><span class="sxs-lookup"><span data-stu-id="624e3-119">In addition to the interfaces listed previously, timeline objects expose other, secondary interfaces.</span></span> <span data-ttu-id="624e3-120">Essas interfaces determinam as relações entre os tipos de objeto.</span><span class="sxs-lookup"><span data-stu-id="624e3-120">These interfaces determine the relationships between the object types.</span></span>



| <span data-ttu-id="624e3-121">Interface</span><span class="sxs-lookup"><span data-stu-id="624e3-121">Interface</span></span>                                                  | <span data-ttu-id="624e3-122">Significado</span><span class="sxs-lookup"><span data-stu-id="624e3-122">Meaning</span></span>                                                                                                       | <span data-ttu-id="624e3-123">Exposto por</span><span class="sxs-lookup"><span data-stu-id="624e3-123">Exposed By</span></span>                        |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [<span data-ttu-id="624e3-124">**IAMTimelineVirtualTrack**</span><span class="sxs-lookup"><span data-stu-id="624e3-124">**IAMTimelineVirtualTrack**</span></span>](iamtimelinevirtualtrack.md) | <span data-ttu-id="624e3-125">O objeto é uma faixa virtual. As faixas virtuais podem residir em composições e conter outros objetos de linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="624e3-125">The object is a virtual track. Virtual tracks can reside inside compositions and hold other timeline objects.</span></span> | <span data-ttu-id="624e3-126">Composição, faixa</span><span class="sxs-lookup"><span data-stu-id="624e3-126">Composition, Track</span></span>                |
| [<span data-ttu-id="624e3-127">**IAMTimelineEffectable**</span><span class="sxs-lookup"><span data-stu-id="624e3-127">**IAMTimelineEffectable**</span></span>](iamtimelineeffectable.md)     | <span data-ttu-id="624e3-128">O objeto pode ter efeitos.</span><span class="sxs-lookup"><span data-stu-id="624e3-128">The object can have effects.</span></span>                                                                                  | <span data-ttu-id="624e3-129">Composição, faixa, origem</span><span class="sxs-lookup"><span data-stu-id="624e3-129">Composition, Track, Source</span></span>        |
| [<span data-ttu-id="624e3-130">**IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="624e3-130">**IAMTimelineTransable**</span></span>](iamtimelinetransable.md)       | <span data-ttu-id="624e3-131">O objeto pode ter transições.</span><span class="sxs-lookup"><span data-stu-id="624e3-131">The object can have transitions.</span></span>                                                                              | <span data-ttu-id="624e3-132">Composição, faixa</span><span class="sxs-lookup"><span data-stu-id="624e3-132">Composition, Track</span></span>                |
| [<span data-ttu-id="624e3-133">**IAMTimelineSplittable**</span><span class="sxs-lookup"><span data-stu-id="624e3-133">**IAMTimelineSplittable**</span></span>](iamtimelinesplittable.md)     | <span data-ttu-id="624e3-134">O objeto pode ser dividido em dois objetos.</span><span class="sxs-lookup"><span data-stu-id="624e3-134">The object can be split into two objects.</span></span>                                                                     | <span data-ttu-id="624e3-135">Rastrear, origem, efeito, transição</span><span class="sxs-lookup"><span data-stu-id="624e3-135">Track, Source, Effect, Transition</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="624e3-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="624e3-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="624e3-137">Visão geral dos componentes da linha do tempo</span><span class="sxs-lookup"><span data-stu-id="624e3-137">Overview of the Timeline Components</span></span>](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



