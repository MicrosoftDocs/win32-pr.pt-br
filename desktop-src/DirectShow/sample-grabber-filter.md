---
description: O filtro de apoio de exemplo fornece uma maneira de recuperar amostras à medida que elas passam pelo gráfico de filtro.
ms.assetid: 3c2fb52f-2b44-449a-ae96-3cf35a0a401d
title: Filtro de apoio de exemplo (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Sample
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: f0b0ddffe2bc769b7c2371ef93091d8c1daf379c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909664"
---
# <a name="sample-grabber-filter"></a><span data-ttu-id="b451f-103">Filtro de apoio de exemplo</span><span class="sxs-lookup"><span data-stu-id="b451f-103">Sample Grabber Filter</span></span>

> [!Note]  
> <span data-ttu-id="b451f-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="b451f-104">\[Deprecated.</span></span> <span data-ttu-id="b451f-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b451f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b451f-106">O filtro de apoio de exemplo fornece uma maneira de recuperar amostras à medida que elas passam pelo gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="b451f-106">The Sample Grabber filter provides a way to retrieve samples as they pass through the filter graph.</span></span> <span data-ttu-id="b451f-107">É um filtro de transformação com um PIN de entrada e um PIN de saída.</span><span class="sxs-lookup"><span data-stu-id="b451f-107">It is a transform filter with one input pin and one output pin.</span></span> <span data-ttu-id="b451f-108">Ele passa todas as amostras downstream inalteradas, para que você possa inseri-la em um grafo de filtro sem alterar o fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="b451f-108">It passes all samples downstream unchanged, so you can insert it into a filter graph without altering the data stream.</span></span> <span data-ttu-id="b451f-109">Em seguida, seu aplicativo pode recuperar exemplos individuais do filtro chamando métodos na interface [**ISampleGrabber**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="b451f-109">Your application can then retrieve individual samples from the filter by calling methods on the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>

<span data-ttu-id="b451f-110">Se você quiser recuperar amostras sem renderizar os dados, conecte o filtro de apoio de exemplo ao filtro de [**renderizador nulo**](null-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="b451f-110">If you want to retrieve samples without rendering the data, connect the Sample Grabber filter to the [**Null Renderer**](null-renderer-filter.md) filter.</span></span>



| <span data-ttu-id="b451f-111">Label</span><span class="sxs-lookup"><span data-stu-id="b451f-111">Label</span></span> | <span data-ttu-id="b451f-112">Valor</span><span class="sxs-lookup"><span data-stu-id="b451f-112">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b451f-113">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="b451f-113">Filter interfaces</span></span>                        | <span data-ttu-id="b451f-114">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **ISampleGrabber**](isamplegrabber.md)</span><span class="sxs-lookup"><span data-stu-id="b451f-114">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ISampleGrabber**](isamplegrabber.md)</span></span>                                                                       |
| <span data-ttu-id="b451f-115">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="b451f-115">Input pin media types</span></span>                    | <span data-ttu-id="b451f-116">Qualquer tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="b451f-116">Any media type.</span></span>                                                                                                                                    |
| <span data-ttu-id="b451f-117">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="b451f-117">Input pin interfaces</span></span>                     | <span data-ttu-id="b451f-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="b451f-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="b451f-119">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="b451f-119">Output pin media types</span></span>                   | <span data-ttu-id="b451f-120">Qualquer tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="b451f-120">Any media type.</span></span> <span data-ttu-id="b451f-121">Corresponde ao tipo de mídia de entrada.</span><span class="sxs-lookup"><span data-stu-id="b451f-121">Matches input media type.</span></span>                                                                                                          |
| <span data-ttu-id="b451f-122">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="b451f-122">Output pin interfaces</span></span>                    | <span data-ttu-id="b451f-123">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="b451f-123">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="b451f-124">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="b451f-124">Filter CLSID</span></span>                             | <span data-ttu-id="b451f-125">\_SAMPLEGRABBER CLSID</span><span class="sxs-lookup"><span data-stu-id="b451f-125">CLSID\_SampleGrabber</span></span>                                                                                                                               |
| <span data-ttu-id="b451f-126">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="b451f-126">Property Page CLSID</span></span>                      | <span data-ttu-id="b451f-127">Nenhuma página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="b451f-127">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="b451f-128">Executável</span><span class="sxs-lookup"><span data-stu-id="b451f-128">Executable</span></span>                               | <span data-ttu-id="b451f-129">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="b451f-129">Qedit.dll</span></span>                                                                                                                                          |
| [<span data-ttu-id="b451f-130">Núcleo</span><span class="sxs-lookup"><span data-stu-id="b451f-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="b451f-131">MÉRITO \_ \_ não \_ use</span><span class="sxs-lookup"><span data-stu-id="b451f-131">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="b451f-132">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="b451f-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="b451f-133">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="b451f-133">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="b451f-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="b451f-134">Remarks</span></span>

<span data-ttu-id="b451f-135">Para usar esse filtro, adicione-o ao grafo de filtro e chame [**ISampleGrabber:: SetMediaType**](isamplegrabber-setmediatype.md) com o tipo de mídia desejado.</span><span class="sxs-lookup"><span data-stu-id="b451f-135">To use this filter, add it to the filter graph and call [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) with the desired media type.</span></span> <span data-ttu-id="b451f-136">Esse método especifica o tipo de mídia para as conexões de entrada e de pino de saída do filtro.</span><span class="sxs-lookup"><span data-stu-id="b451f-136">This method specifies the media type for the filter's input and output pin connections.</span></span> <span data-ttu-id="b451f-137">Em seguida, conecte o filtro a outros filtros no grafo.</span><span class="sxs-lookup"><span data-stu-id="b451f-137">Then connect the filter to other filters in the graph.</span></span>

<span data-ttu-id="b451f-138">Se você chamar [**ISampleGrabber:: SetBufferSamples**](isamplegrabber-setbuffersamples.md) com o valor **true**, o filtro armazenará em buffer cada exemplo que ele receber antes de passá-lo downstream.</span><span class="sxs-lookup"><span data-stu-id="b451f-138">If you call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) with the value **TRUE**, the filter buffers each sample that it receives before passing it downstream.</span></span> <span data-ttu-id="b451f-139">Chame o método [**ISampleGrabber:: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) para recuperar o conteúdo atual do buffer.</span><span class="sxs-lookup"><span data-stu-id="b451f-139">Call the [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) method to retrieve the current contents of the buffer.</span></span> <span data-ttu-id="b451f-140">Como alternativa, você pode chamar [**ISampleGrabber:: SetCallback**](isamplegrabber-setcallback.md) para que o filtro invoque uma função de retorno de chamada sempre que receber um exemplo.</span><span class="sxs-lookup"><span data-stu-id="b451f-140">Alternatively, you can call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) to have the filter invoke a callback function whenever it receives a sample.</span></span>

<span data-ttu-id="b451f-141">O filtro tem as seguintes limitações para formatos de vídeo:</span><span class="sxs-lookup"><span data-stu-id="b451f-141">The filter has the following limitations for video formats:</span></span>

-   <span data-ttu-id="b451f-142">Ele não dá suporte a tipos de vídeo com orientação de cima para baixo ( **semialtura** negativa).</span><span class="sxs-lookup"><span data-stu-id="b451f-142">It does not support video types with top-down orientation (negative **biHeight**).</span></span>
-   <span data-ttu-id="b451f-143">Ele não dá suporte à estrutura de formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (tipo de formato igual ao **formato \_ VideoInfo2**).</span><span class="sxs-lookup"><span data-stu-id="b451f-143">It does not support the [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format structure (format type equal to **FORMAT\_VideoInfo2**).</span></span>
-   <span data-ttu-id="b451f-144">Ele rejeita qualquer tipo de vídeo em que o stride da superfície não corresponde à largura do vídeo.</span><span class="sxs-lookup"><span data-stu-id="b451f-144">It rejects any video type where the surface stride does not match the video width.</span></span>

<span data-ttu-id="b451f-145">Como resultado, o exemplo de apoio não se conectará ao VMR (Video mixagem Renderer) para alguns tipos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b451f-145">As a result, the Sample Grabber will not connect to the Video Mixing Renderer (VMR) for some video types.</span></span>

## <a name="requirements"></a><span data-ttu-id="b451f-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b451f-146">Requirements</span></span>



| <span data-ttu-id="b451f-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="b451f-147">Requirement</span></span> | <span data-ttu-id="b451f-148">Valor</span><span class="sxs-lookup"><span data-stu-id="b451f-148">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b451f-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b451f-149">Header</span></span><br/> | <dl> <span data-ttu-id="b451f-150"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b451f-150"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b451f-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="b451f-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b451f-152">Objetos de serviços de edição do DirectShow</span><span class="sxs-lookup"><span data-stu-id="b451f-152">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> <dt>

[<span data-ttu-id="b451f-153">Usando o exemplo de apoio</span><span class="sxs-lookup"><span data-stu-id="b451f-153">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> </dl>

 

 




