---
description: A interface IAMTimelineComp insere ou recupera faixas virtuais em uma composição nos serviços de edição do DirectShow (DES). Uma composição é uma coleção de camadas que atua como uma faixa única e composta.
ms.assetid: b0a47303-9e3c-4b78-ac90-c5d8fce2b727
title: Interface IAMTimelineComp (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 645abbb9c5f61fcfd04e433c3cfc61b926ed403d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775614"
---
# <a name="iamtimelinecomp-interface"></a><span data-ttu-id="0b0a7-103">Interface IAMTimelineComp</span><span class="sxs-lookup"><span data-stu-id="0b0a7-103">IAMTimelineComp interface</span></span>

> [!Note]  
> <span data-ttu-id="0b0a7-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-104">\[Deprecated.</span></span> <span data-ttu-id="0b0a7-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0b0a7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0b0a7-106">A interface **IAMTimelineComp** insere ou recupera faixas virtuais em uma composição nos [serviços de edição do DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="0b0a7-106">The **IAMTimelineComp** interface inserts or retrieves virtual tracks on a composition in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="0b0a7-107">Uma composição é uma coleção de camadas que atua como uma *faixa* única e composta. Por exemplo, uma composição que contém duas faixas com uma transição entre elas atua como uma única faixa com a transição precomposta.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-107">A composition is a collection of layers that acts as a single, composited *track*. For example, a composition that contains two tracks with a transition between them acts as a single track with the transition precomposited.</span></span> <span data-ttu-id="0b0a7-108">Uma composição deve conter mídia de apenas um tipo (como áudio ou vídeo), mas essa limitação não é imposta.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-108">A composition should contain media of only one type (such as audio or video), but this limitation is not enforced.</span></span> <span data-ttu-id="0b0a7-109">Um *controle virtual* é qualquer objeto que possa residir em uma composição, incluindo faixas e outras composições.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-109">A *virtual track* is any object that can reside in a composition, including tracks and other compositions.</span></span>

<span data-ttu-id="0b0a7-110">Os nós mais altos na linha do tempo são *grupos*.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-110">The topmost nodes in the timeline are *groups*.</span></span> <span data-ttu-id="0b0a7-111">Os grupos implementam a `IAMTimelineComp` interface e a interface [**IAMTimelineGroup**](iamtimelinegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="0b0a7-111">Groups implement both the `IAMTimelineComp` interface and the [**IAMTimelineGroup**](iamtimelinegroup.md) interface.</span></span>

<span data-ttu-id="0b0a7-112">Para criar um objeto de composição, chame [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) com o valor linha de tempo \_ Major \_ tipo \_ composto.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-112">To create a composition object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_COMPOSITE.</span></span> <span data-ttu-id="0b0a7-113">Você pode consultar o ponteiro [**IAMTimelineObj**](iamtimelineobj.md) retornado para a `IAMTimelineComp` interface.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-113">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the `IAMTimelineComp` interface.</span></span> <span data-ttu-id="0b0a7-114">Para obter mais informações, consulte [o modelo de linha do tempo](the-timeline-model.md) e [construindo uma linha do tempo](constructing-a-timeline.md).</span><span class="sxs-lookup"><span data-stu-id="0b0a7-114">For more information, see [The Timeline Model](the-timeline-model.md) and [Constructing a Timeline](constructing-a-timeline.md).</span></span>

## <a name="members"></a><span data-ttu-id="0b0a7-115">Membros</span><span class="sxs-lookup"><span data-stu-id="0b0a7-115">Members</span></span>

<span data-ttu-id="0b0a7-116">A interface **IAMTimelineComp** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0b0a7-116">The **IAMTimelineComp** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0b0a7-117">**IAMTimelineComp** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0b0a7-117">**IAMTimelineComp** also has these types of members:</span></span>

-   [<span data-ttu-id="0b0a7-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="0b0a7-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0b0a7-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="0b0a7-119">Methods</span></span>

<span data-ttu-id="0b0a7-120">A interface **IAMTimelineComp** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-120">The **IAMTimelineComp** interface has these methods.</span></span>



| <span data-ttu-id="0b0a7-121">Método</span><span class="sxs-lookup"><span data-stu-id="0b0a7-121">Method</span></span>                                                                       | <span data-ttu-id="0b0a7-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b0a7-122">Description</span></span>                                                                                                                                               |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b0a7-123">**GetCountOfType**</span><span class="sxs-lookup"><span data-stu-id="0b0a7-123">**GetCountOfType**</span></span>](iamtimelinecomp-getcountoftype.md)                     | <span data-ttu-id="0b0a7-124">Recupera o número de objetos de um determinado tipo contido nessa composição e todas as suas faixas virtuais, recursivamente.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-124">Retrieves the number of objects of a given type contained in this composition and all of its virtual tracks, recursively.</span></span><br/>                      |
| [<span data-ttu-id="0b0a7-125">**GetNextVTrack**</span><span class="sxs-lookup"><span data-stu-id="0b0a7-125">**GetNextVTrack**</span></span>](iamtimelinecomp-getnextvtrack.md)                       | <span data-ttu-id="0b0a7-126">Recupera a próxima faixa virtual após uma faixa virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-126">Retrieves the next virtual track after a specified virtual track.</span></span><br/>                                                                              |
| [<span data-ttu-id="0b0a7-127">**GetRecursiveLayerOfType**</span><span class="sxs-lookup"><span data-stu-id="0b0a7-127">**GetRecursiveLayerOfType**</span></span>](iamtimelinecomp-getrecursivelayeroftype.md)   | <span data-ttu-id="0b0a7-128">Executa uma ordenação de profundidade das faixas virtuais contidas nessa composição e recupera a *n* º de faixa virtual dessa ordem.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-128">Performs a depth-first ordering of the virtual tracks contained in this composition, and retrieves the *n* th virtual track from that ordering.</span></span><br/> |
| [<span data-ttu-id="0b0a7-129">**GetRecursiveLayerOfTypeI**</span><span class="sxs-lookup"><span data-stu-id="0b0a7-129">**GetRecursiveLayerOfTypeI**</span></span>](iamtimelinecomp-getrecursivelayeroftypei.md) | <span data-ttu-id="0b0a7-130">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-130">Not supported.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="0b0a7-131">**GetVTrack**</span><span class="sxs-lookup"><span data-stu-id="0b0a7-131">**GetVTrack**</span></span>](iamtimelinecomp-getvtrack.md)                               | <span data-ttu-id="0b0a7-132">Recupera a faixa virtual na prioridade especificada.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-132">Retrieves the virtual track at the specified priority.</span></span><br/>                                                                                         |
| [<span data-ttu-id="0b0a7-133">**VTrackGetCount**</span><span class="sxs-lookup"><span data-stu-id="0b0a7-133">**VTrackGetCount**</span></span>](iamtimelinecomp-vtrackgetcount.md)                     | <span data-ttu-id="0b0a7-134">Recupera o número de faixas virtuais contidas na composição.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-134">Retrieves the number of virtual tracks contained in the composition.</span></span><br/>                                                                           |
| [<span data-ttu-id="0b0a7-135">**VTrackInsBefore**</span><span class="sxs-lookup"><span data-stu-id="0b0a7-135">**VTrackInsBefore**</span></span>](iamtimelinecomp-vtrackinsbefore.md)                   | <span data-ttu-id="0b0a7-136">Insere uma faixa virtual na composição na prioridade especificada.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-136">Inserts a virtual track into the composition at the specified priority.</span></span><br/>                                                                        |
| [<span data-ttu-id="0b0a7-137">**VTrackSwapPriorities**</span><span class="sxs-lookup"><span data-stu-id="0b0a7-137">**VTrackSwapPriorities**</span></span>](iamtimelinecomp-vtrackswappriorities.md)         | <span data-ttu-id="0b0a7-138">Alterna os níveis de prioridade de duas faixas.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-138">Switches the priority levels of two tracks.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="0b0a7-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b0a7-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0b0a7-140">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-140">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0b0a7-141">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0b0a7-141">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0b0a7-142">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-142">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0b0a7-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b0a7-143">Requirements</span></span>



| <span data-ttu-id="0b0a7-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b0a7-144">Requirement</span></span> | <span data-ttu-id="0b0a7-145">Valor</span><span class="sxs-lookup"><span data-stu-id="0b0a7-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b0a7-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b0a7-146">Header</span></span><br/>  | <dl> <span data-ttu-id="0b0a7-147"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b0a7-147"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0b0a7-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0b0a7-148">Library</span></span><br/> | <dl> <span data-ttu-id="0b0a7-149"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b0a7-149"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
