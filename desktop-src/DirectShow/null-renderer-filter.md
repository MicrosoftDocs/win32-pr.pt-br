---
description: O filtro de renderizador nulo é um renderizador que descarta todas as amostras recebidas, sem exibir ou renderizar os dados de exemplo.
ms.assetid: 2954762d-2ae6-4e38-ac88-5390a081897e
title: Filtro de renderizador nulo (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Null Renderer Filter
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 64647cbcbcc836c400890fb173a29c76f8723029
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908804"
---
# <a name="null-renderer-filter"></a><span data-ttu-id="5128d-103">Filtro de renderizador nulo</span><span class="sxs-lookup"><span data-stu-id="5128d-103">Null Renderer Filter</span></span>

> [!Note]  
> <span data-ttu-id="5128d-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="5128d-104">\[Deprecated.</span></span> <span data-ttu-id="5128d-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5128d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5128d-106">O filtro de renderizador nulo é um renderizador que descarta todas as amostras recebidas, sem exibir ou renderizar os dados de exemplo.</span><span class="sxs-lookup"><span data-stu-id="5128d-106">The Null Renderer filter is a renderer that discards every sample it receives, without displaying or rendering the sample data.</span></span>



| <span data-ttu-id="5128d-107">Label</span><span class="sxs-lookup"><span data-stu-id="5128d-107">Label</span></span> | <span data-ttu-id="5128d-108">Valor</span><span class="sxs-lookup"><span data-stu-id="5128d-108">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5128d-109">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="5128d-109">Filter interfaces</span></span>                        | <span data-ttu-id="5128d-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="5128d-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span> |
| <span data-ttu-id="5128d-111">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="5128d-111">Input pin media types</span></span>                    | <span data-ttu-id="5128d-112">Qualquer tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="5128d-112">Any media type</span></span>                                                                                                       |
| <span data-ttu-id="5128d-113">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="5128d-113">Input pin interfaces</span></span>                     | <span data-ttu-id="5128d-114">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="5128d-114">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>               |
| <span data-ttu-id="5128d-115">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="5128d-115">Output pin media types</span></span>                   | <span data-ttu-id="5128d-116">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="5128d-116">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="5128d-117">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="5128d-117">Output pin interfaces</span></span>                    | <span data-ttu-id="5128d-118">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="5128d-118">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="5128d-119">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="5128d-119">Filter CLSID</span></span>                             | <span data-ttu-id="5128d-120">\_NULLRENDERER CLSID</span><span class="sxs-lookup"><span data-stu-id="5128d-120">CLSID\_NullRenderer</span></span>                                                                                                  |
| <span data-ttu-id="5128d-121">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="5128d-121">Property Page CLSID</span></span>                      | <span data-ttu-id="5128d-122">Nenhuma página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="5128d-122">No property page.</span></span>                                                                                                    |
| <span data-ttu-id="5128d-123">Executável</span><span class="sxs-lookup"><span data-stu-id="5128d-123">Executable</span></span>                               | <span data-ttu-id="5128d-124">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="5128d-124">Qedit.dll</span></span>                                                                                                            |
| [<span data-ttu-id="5128d-125">Núcleo</span><span class="sxs-lookup"><span data-stu-id="5128d-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="5128d-126">MÉRITO \_ \_ não \_ use</span><span class="sxs-lookup"><span data-stu-id="5128d-126">MERIT\_DO\_NOT\_USE</span></span>                                                                                                  |
| [<span data-ttu-id="5128d-127">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="5128d-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="5128d-128">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="5128d-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="5128d-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="5128d-129">Remarks</span></span>

<span data-ttu-id="5128d-130">Use esse filtro quando um pino de saída no grafo exigir uma conexão downstream, mas você não quiser renderizar os dados desse PIN.</span><span class="sxs-lookup"><span data-stu-id="5128d-130">Use this filter when an output pin in the graph requires a downstream connection, but you do not wish to render the data from that pin.</span></span> <span data-ttu-id="5128d-131">Conectando o pino de saída ao renderizador NULL, você conclui a conexão sem renderizar os dados.</span><span class="sxs-lookup"><span data-stu-id="5128d-131">By connecting the output pin to the Null Renderer, you complete the connection without rendering the data.</span></span>

<span data-ttu-id="5128d-132">Embora esse filtro não processe nenhum exemplo, ele aguarda o tempo de apresentação de cada amostra antes de descartar o exemplo.</span><span class="sxs-lookup"><span data-stu-id="5128d-132">Even though this filter does not render any samples, it does wait for each sample's presentation time before discarding the sample.</span></span> <span data-ttu-id="5128d-133">Portanto, o grafo será executado com a taxa normal.</span><span class="sxs-lookup"><span data-stu-id="5128d-133">Therefore, the graph will run at the normal rate.</span></span> <span data-ttu-id="5128d-134">Se você quiser que o grafo seja executado o mais rapidamente possível, defina o relógio de referência como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="5128d-134">If you want the graph the run as quickly as possible, set the reference clock to **NULL**.</span></span> <span data-ttu-id="5128d-135">Para obter mais informações, consulte [definindo o relógio do grafo](setting-the-graph-clock.md).</span><span class="sxs-lookup"><span data-stu-id="5128d-135">For more information, see [Setting the Graph Clock](setting-the-graph-clock.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5128d-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5128d-136">Requirements</span></span>



| <span data-ttu-id="5128d-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="5128d-137">Requirement</span></span> | <span data-ttu-id="5128d-138">Valor</span><span class="sxs-lookup"><span data-stu-id="5128d-138">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5128d-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5128d-139">Header</span></span><br/> | <dl> <span data-ttu-id="5128d-140"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5128d-140"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5128d-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="5128d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5128d-142">Objetos de serviços de edição do DirectShow</span><span class="sxs-lookup"><span data-stu-id="5128d-142">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> </dl>

 

 




