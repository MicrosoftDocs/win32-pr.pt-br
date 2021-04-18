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
ms.openlocfilehash: 7ff6c728276ca3fd69c14e304780b1d70c563265
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761981"
---
# <a name="null-renderer-filter"></a><span data-ttu-id="c1b3e-103">Filtro de renderizador nulo</span><span class="sxs-lookup"><span data-stu-id="c1b3e-103">Null Renderer Filter</span></span>

> [!Note]  
> <span data-ttu-id="c1b3e-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="c1b3e-104">\[Deprecated.</span></span> <span data-ttu-id="c1b3e-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c1b3e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c1b3e-106">O filtro de renderizador nulo é um renderizador que descarta todas as amostras recebidas, sem exibir ou renderizar os dados de exemplo.</span><span class="sxs-lookup"><span data-stu-id="c1b3e-106">The Null Renderer filter is a renderer that discards every sample it receives, without displaying or rendering the sample data.</span></span>



|                                          |                                                                                                                      |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1b3e-107">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="c1b3e-107">Filter interfaces</span></span>                        | <span data-ttu-id="c1b3e-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="c1b3e-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span> |
| <span data-ttu-id="c1b3e-109">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="c1b3e-109">Input pin media types</span></span>                    | <span data-ttu-id="c1b3e-110">Qualquer tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="c1b3e-110">Any media type</span></span>                                                                                                       |
| <span data-ttu-id="c1b3e-111">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="c1b3e-111">Input pin interfaces</span></span>                     | <span data-ttu-id="c1b3e-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="c1b3e-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>               |
| <span data-ttu-id="c1b3e-113">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="c1b3e-113">Output pin media types</span></span>                   | <span data-ttu-id="c1b3e-114">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="c1b3e-114">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="c1b3e-115">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="c1b3e-115">Output pin interfaces</span></span>                    | <span data-ttu-id="c1b3e-116">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="c1b3e-116">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="c1b3e-117">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="c1b3e-117">Filter CLSID</span></span>                             | <span data-ttu-id="c1b3e-118">\_NULLRENDERER CLSID</span><span class="sxs-lookup"><span data-stu-id="c1b3e-118">CLSID\_NullRenderer</span></span>                                                                                                  |
| <span data-ttu-id="c1b3e-119">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="c1b3e-119">Property Page CLSID</span></span>                      | <span data-ttu-id="c1b3e-120">Nenhuma página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c1b3e-120">No property page.</span></span>                                                                                                    |
| <span data-ttu-id="c1b3e-121">Executável</span><span class="sxs-lookup"><span data-stu-id="c1b3e-121">Executable</span></span>                               | <span data-ttu-id="c1b3e-122">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="c1b3e-122">Qedit.dll</span></span>                                                                                                            |
| [<span data-ttu-id="c1b3e-123">Núcleo</span><span class="sxs-lookup"><span data-stu-id="c1b3e-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="c1b3e-124">MÉRITO \_ \_ não \_ use</span><span class="sxs-lookup"><span data-stu-id="c1b3e-124">MERIT\_DO\_NOT\_USE</span></span>                                                                                                  |
| [<span data-ttu-id="c1b3e-125">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="c1b3e-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="c1b3e-126">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="c1b3e-126">CLSID\_LegacyAmFilterCategory</span></span>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="c1b3e-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1b3e-127">Remarks</span></span>

<span data-ttu-id="c1b3e-128">Use esse filtro quando um pino de saída no grafo exigir uma conexão downstream, mas você não quiser renderizar os dados desse PIN.</span><span class="sxs-lookup"><span data-stu-id="c1b3e-128">Use this filter when an output pin in the graph requires a downstream connection, but you do not wish to render the data from that pin.</span></span> <span data-ttu-id="c1b3e-129">Conectando o pino de saída ao renderizador NULL, você conclui a conexão sem renderizar os dados.</span><span class="sxs-lookup"><span data-stu-id="c1b3e-129">By connecting the output pin to the Null Renderer, you complete the connection without rendering the data.</span></span>

<span data-ttu-id="c1b3e-130">Embora esse filtro não processe nenhum exemplo, ele aguarda o tempo de apresentação de cada amostra antes de descartar o exemplo.</span><span class="sxs-lookup"><span data-stu-id="c1b3e-130">Even though this filter does not render any samples, it does wait for each sample's presentation time before discarding the sample.</span></span> <span data-ttu-id="c1b3e-131">Portanto, o grafo será executado com a taxa normal.</span><span class="sxs-lookup"><span data-stu-id="c1b3e-131">Therefore, the graph will run at the normal rate.</span></span> <span data-ttu-id="c1b3e-132">Se você quiser que o grafo seja executado o mais rapidamente possível, defina o relógio de referência como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c1b3e-132">If you want the graph the run as quickly as possible, set the reference clock to **NULL**.</span></span> <span data-ttu-id="c1b3e-133">Para obter mais informações, consulte [definindo o relógio do grafo](setting-the-graph-clock.md).</span><span class="sxs-lookup"><span data-stu-id="c1b3e-133">For more information, see [Setting the Graph Clock](setting-the-graph-clock.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1b3e-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1b3e-134">Requirements</span></span>



| <span data-ttu-id="c1b3e-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1b3e-135">Requirement</span></span> | <span data-ttu-id="c1b3e-136">Valor</span><span class="sxs-lookup"><span data-stu-id="c1b3e-136">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c1b3e-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c1b3e-137">Header</span></span><br/> | <dl> <span data-ttu-id="c1b3e-138"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1b3e-138"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1b3e-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1b3e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1b3e-140">Objetos de serviços de edição do DirectShow</span><span class="sxs-lookup"><span data-stu-id="c1b3e-140">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> </dl>

 

 




