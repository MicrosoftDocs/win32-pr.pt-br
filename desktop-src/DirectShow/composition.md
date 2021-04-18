---
description: Composição
ms.assetid: b5f607b2-9cca-4eef-9c63-d2015bd10469
title: Composição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e030e02ab77ec54e1e340d72db7210665d649bfb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105757695"
---
# <a name="composition"></a><span data-ttu-id="80e42-103">Composição</span><span class="sxs-lookup"><span data-stu-id="80e42-103">Composition</span></span>

> [!Note]  
> <span data-ttu-id="80e42-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="80e42-104">\[Deprecated.</span></span> <span data-ttu-id="80e42-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="80e42-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="80e42-106">O objeto de composição é um contêiner para faixas.</span><span class="sxs-lookup"><span data-stu-id="80e42-106">The composition object is a container for tracks.</span></span> <span data-ttu-id="80e42-107">Ele também pode conter outras composições (para aninhamento de faixas), efeitos e transições.</span><span class="sxs-lookup"><span data-stu-id="80e42-107">It can also hold other compositions (for nesting of tracks), effects, and transitions.</span></span> <span data-ttu-id="80e42-108">Para criar esse objeto, chame o método [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) .</span><span class="sxs-lookup"><span data-stu-id="80e42-108">To create this object, call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span>

<span data-ttu-id="80e42-109">O objeto de composição expõe as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="80e42-109">The composition object exposes the following interfaces:</span></span>

-   [<span data-ttu-id="80e42-110">**IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="80e42-110">**IAMTimelineComp**</span></span>](iamtimelinecomp.md)
-   [<span data-ttu-id="80e42-111">**IAMTimelineEffectable**</span><span class="sxs-lookup"><span data-stu-id="80e42-111">**IAMTimelineEffectable**</span></span>](iamtimelineeffectable.md)
-   [<span data-ttu-id="80e42-112">**IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="80e42-112">**IAMTimelineObj**</span></span>](iamtimelineobj.md)
-   [<span data-ttu-id="80e42-113">**IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="80e42-113">**IAMTimelineTransable**</span></span>](iamtimelinetransable.md)
-   [<span data-ttu-id="80e42-114">**IAMTimelineVirtualTrack**</span><span class="sxs-lookup"><span data-stu-id="80e42-114">**IAMTimelineVirtualTrack**</span></span>](iamtimelinevirtualtrack.md)

## <a name="related-topics"></a><span data-ttu-id="80e42-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="80e42-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80e42-116">O modelo de linha do tempo</span><span class="sxs-lookup"><span data-stu-id="80e42-116">The Timeline Model</span></span>](the-timeline-model.md)
</dt> <dt>

[<span data-ttu-id="80e42-117">Construindo uma linha do tempo</span><span class="sxs-lookup"><span data-stu-id="80e42-117">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



