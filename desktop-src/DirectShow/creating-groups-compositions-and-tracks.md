---
description: Criando composições e faixas de grupos
ms.assetid: c3bef3cd-5e3c-42c5-850f-b4cb00c414bd
title: Criando composições e faixas de grupos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2808c2d096b52ad73da7d518d703bc25103751d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103826020"
---
# <a name="creating-groups-compositions-and-tracks"></a><span data-ttu-id="b26ed-103">Criando composições e faixas de grupos</span><span class="sxs-lookup"><span data-stu-id="b26ed-103">Creating Groups Compositions and Tracks</span></span>

<span data-ttu-id="b26ed-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="b26ed-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="b26ed-105">Grupos, composições e faixas são as camadas intermediárias entre a linha do tempo e os clipes de origem.</span><span class="sxs-lookup"><span data-stu-id="b26ed-105">Groups, compositions, and tracks are the intermediate layers between the timeline and the source clips.</span></span> <span data-ttu-id="b26ed-106">Elas são diferenciadas pelo tipo de objeto que podem conter.</span><span class="sxs-lookup"><span data-stu-id="b26ed-106">They are distinguished by the type of object they can contain.</span></span>

-   <span data-ttu-id="b26ed-107">As faixas contêm objetos de origem.</span><span class="sxs-lookup"><span data-stu-id="b26ed-107">Tracks contain source objects.</span></span>
-   <span data-ttu-id="b26ed-108">As composições contêm faixas e outras composições, mas não objetos de origem.</span><span class="sxs-lookup"><span data-stu-id="b26ed-108">Compositions contain tracks and other compositions, but not source objects.</span></span>
-   <span data-ttu-id="b26ed-109">Os grupos são as composições de nível superior.</span><span class="sxs-lookup"><span data-stu-id="b26ed-109">Groups are top-level compositions.</span></span> <span data-ttu-id="b26ed-110">Os grupos contêm composições e faixas, mas as composições não podem conter grupos.</span><span class="sxs-lookup"><span data-stu-id="b26ed-110">Groups contain compositions and tracks, but compositions cannot contain groups.</span></span>
-   <span data-ttu-id="b26ed-111">Um *controle virtual* é qualquer objeto que possa residir dentro de uma composição ou um grupo.</span><span class="sxs-lookup"><span data-stu-id="b26ed-111">A *virtual track* is any object that can reside inside a composition or a group.</span></span> <span data-ttu-id="b26ed-112">Isso inclui faixas e composições.</span><span class="sxs-lookup"><span data-stu-id="b26ed-112">This includes tracks and compositions.</span></span>

<span data-ttu-id="b26ed-113">Esses objetos expõem as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="b26ed-113">These objects expose the following interfaces:</span></span>



| <span data-ttu-id="b26ed-114">Interface</span><span class="sxs-lookup"><span data-stu-id="b26ed-114">Interface</span></span>                                                  | <span data-ttu-id="b26ed-115">Exposto por</span><span class="sxs-lookup"><span data-stu-id="b26ed-115">Exposed By</span></span>           |
|------------------------------------------------------------|----------------------|
| [<span data-ttu-id="b26ed-116">**IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="b26ed-116">**IAMTimelineTrack**</span></span>](iamtimelinetrack.md)               | <span data-ttu-id="b26ed-117">Faixas</span><span class="sxs-lookup"><span data-stu-id="b26ed-117">Tracks</span></span>               |
| [<span data-ttu-id="b26ed-118">**IAMTimelineVirtualTrack**</span><span class="sxs-lookup"><span data-stu-id="b26ed-118">**IAMTimelineVirtualTrack**</span></span>](iamtimelinevirtualtrack.md) | <span data-ttu-id="b26ed-119">Faixas, composições</span><span class="sxs-lookup"><span data-stu-id="b26ed-119">Tracks, Compositions</span></span> |
| [<span data-ttu-id="b26ed-120">**IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="b26ed-120">**IAMTimelineComp**</span></span>](iamtimelinecomp.md)                 | <span data-ttu-id="b26ed-121">Composições, grupos</span><span class="sxs-lookup"><span data-stu-id="b26ed-121">Compositions, Groups</span></span> |
| [<span data-ttu-id="b26ed-122">**IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="b26ed-122">**IAMTimelineGroup**</span></span>](iamtimelinegroup.md)               | <span data-ttu-id="b26ed-123">Grupos</span><span class="sxs-lookup"><span data-stu-id="b26ed-123">Groups</span></span>               |



 

<span data-ttu-id="b26ed-124">Essas interfaces contêm os métodos para adicionar objetos à linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="b26ed-124">These interfaces contain the methods for adding objects to the timeline.</span></span>

-   <span data-ttu-id="b26ed-125">[**IAMTimeline:: addgroup**](iamtimeline-addgroup.md): insere um grupo na linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="b26ed-125">[**IAMTimeline::AddGroup**](iamtimeline-addgroup.md): Inserts a group into the timeline.</span></span>
-   <span data-ttu-id="b26ed-126">[**IAMTimelineComp:: VTrackInsBefore**](iamtimelinecomp-vtrackinsbefore.md): insere uma faixa virtual em uma composição ou grupo.</span><span class="sxs-lookup"><span data-stu-id="b26ed-126">[**IAMTimelineComp::VTrackInsBefore**](iamtimelinecomp-vtrackinsbefore.md): Inserts a virtual track into a composition or group.</span></span>
-   <span data-ttu-id="b26ed-127">[**IAMTimelineTrack:: SrcAdd**](iamtimelinetrack-srcadd.md): insere uma fonte em um controle.</span><span class="sxs-lookup"><span data-stu-id="b26ed-127">[**IAMTimelineTrack::SrcAdd**](iamtimelinetrack-srcadd.md): Inserts a source into a track.</span></span>

<span data-ttu-id="b26ed-128">Por exemplo, o código a seguir insere uma nova faixa em um grupo.</span><span class="sxs-lookup"><span data-stu-id="b26ed-128">For example, the following code inserts a new track into a group.</span></span> <span data-ttu-id="b26ed-129">Conforme mostrado na tabela anterior, um grupo é considerado um tipo de composição, e uma faixa é um tipo de faixa virtual. Portanto, para inserir a faixa no grupo, você deve consultar o grupo para sua interface **IAMTimelineComp** e chamar o método **IAMTimelineComp:: VTrackInsBefore** .</span><span class="sxs-lookup"><span data-stu-id="b26ed-129">As shown in the previous table, a group is considered a kind of composition, and a track is a kind of virtual track. Therefore, to insert the track into the group, you must query the group for its **IAMTimelineComp** interface and call the **IAMTimelineComp::VTrackInsBefore** method.</span></span>


```C++
IAMTimelineGroup    *pGroup;
// Create a new group (not shown). 

IAMTimelineComp     *pComp = NULL;
IAMTimelineObj      *pTrackObj = NULL;

pTL->CreateEmptyNode(&pTrackObj, TIMELINE_MAJOR_TYPE_TRACK);
pGroup->QueryInterface(IID_IAMTimelineComp, (void **)&pComp);
pComp->VTrackInsBefore(pTrackObj, 0);
```



<span data-ttu-id="b26ed-130">O segundo parâmetro para **VTrackInsBefore** especifica a prioridade da faixa virtual. Os níveis de prioridade começam em zero.</span><span class="sxs-lookup"><span data-stu-id="b26ed-130">The second parameter to **VTrackInsBefore** specifies the priority of the virtual track. Priority levels start at zero.</span></span> <span data-ttu-id="b26ed-131">Se você especificar o valor – 1, a faixa virtual será inserida no final da lista de prioridades.</span><span class="sxs-lookup"><span data-stu-id="b26ed-131">If you specify the value –1, the virtual track is inserted at the end of the priority list.</span></span> <span data-ttu-id="b26ed-132">Se você especificar um valor onde já exista uma faixa virtual, tudo desse ponto em será movido para baixo na lista por um nível de prioridade.</span><span class="sxs-lookup"><span data-stu-id="b26ed-132">If you specify a value where there is already a virtual track, everything from that point on moves down the list by one priority level.</span></span> <span data-ttu-id="b26ed-133">Não insira uma faixa virtual em uma prioridade maior que o número de faixas virtuais, pois isso causará um comportamento indefinido.</span><span class="sxs-lookup"><span data-stu-id="b26ed-133">Do not insert a virtual track at a priority greater than the number of virtual tracks, because it will cause undefined behavior.</span></span>

<span data-ttu-id="b26ed-134">Para excluir um objeto permanentemente da linha do tempo, chame [**IAMTimelineObj:: RemoveAll**](iamtimelineobj-removeall.md) no objeto.</span><span class="sxs-lookup"><span data-stu-id="b26ed-134">To delete an object permanently from the timeline, call [**IAMTimelineObj::RemoveAll**](iamtimelineobj-removeall.md) on the object.</span></span> <span data-ttu-id="b26ed-135">Esse método remove o objeto e todos os seus filhos.</span><span class="sxs-lookup"><span data-stu-id="b26ed-135">This method removes the object and all its children.</span></span> <span data-ttu-id="b26ed-136">Para remover um objeto com a finalidade de reinseri-lo em outro lugar na linha do tempo, chame [**IAMTimelineObj:: Remove**](iamtimelineobj-remove.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="b26ed-136">To remove an object for the purpose of reinserting it elsewhere in the timeline, call [**IAMTimelineObj::Remove**](iamtimelineobj-remove.md) instead.</span></span> <span data-ttu-id="b26ed-137">Ao contrário de **RemoveAll**, esse método não exclui os filhos do objeto.</span><span class="sxs-lookup"><span data-stu-id="b26ed-137">Unlike **RemoveAll**, this method does not delete the object's children.</span></span> <span data-ttu-id="b26ed-138">Para remover tudo da linha do tempo, chame [**IAMTimeline:: ClearAllGroups**](iamtimeline-clearallgroups.md).</span><span class="sxs-lookup"><span data-stu-id="b26ed-138">To remove everything from the timeline, call [**IAMTimeline::ClearAllGroups**](iamtimeline-clearallgroups.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b26ed-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b26ed-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b26ed-140">Construindo uma linha do tempo</span><span class="sxs-lookup"><span data-stu-id="b26ed-140">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



