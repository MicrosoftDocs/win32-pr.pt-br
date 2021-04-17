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
ms.openlocfilehash: 18cedd24b0ddcb8f71373641905228f8252ae4ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779482"
---
# <a name="sample-grabber-filter"></a><span data-ttu-id="aad6c-103">Filtro de apoio de exemplo</span><span class="sxs-lookup"><span data-stu-id="aad6c-103">Sample Grabber Filter</span></span>

> [!Note]  
> <span data-ttu-id="aad6c-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="aad6c-104">\[Deprecated.</span></span> <span data-ttu-id="aad6c-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="aad6c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="aad6c-106">O filtro de apoio de exemplo fornece uma maneira de recuperar amostras à medida que elas passam pelo gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="aad6c-106">The Sample Grabber filter provides a way to retrieve samples as they pass through the filter graph.</span></span> <span data-ttu-id="aad6c-107">É um filtro de transformação com um PIN de entrada e um PIN de saída.</span><span class="sxs-lookup"><span data-stu-id="aad6c-107">It is a transform filter with one input pin and one output pin.</span></span> <span data-ttu-id="aad6c-108">Ele passa todas as amostras downstream inalteradas, para que você possa inseri-la em um grafo de filtro sem alterar o fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="aad6c-108">It passes all samples downstream unchanged, so you can insert it into a filter graph without altering the data stream.</span></span> <span data-ttu-id="aad6c-109">Em seguida, seu aplicativo pode recuperar exemplos individuais do filtro chamando métodos na interface [**ISampleGrabber**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="aad6c-109">Your application can then retrieve individual samples from the filter by calling methods on the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>

<span data-ttu-id="aad6c-110">Se você quiser recuperar amostras sem renderizar os dados, conecte o filtro de apoio de exemplo ao filtro de [**renderizador nulo**](null-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="aad6c-110">If you want to retrieve samples without rendering the data, connect the Sample Grabber filter to the [**Null Renderer**](null-renderer-filter.md) filter.</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aad6c-111">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="aad6c-111">Filter interfaces</span></span>                        | <span data-ttu-id="aad6c-112">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **ISampleGrabber**](isamplegrabber.md)</span><span class="sxs-lookup"><span data-stu-id="aad6c-112">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ISampleGrabber**](isamplegrabber.md)</span></span>                                                                       |
| <span data-ttu-id="aad6c-113">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="aad6c-113">Input pin media types</span></span>                    | <span data-ttu-id="aad6c-114">Qualquer tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="aad6c-114">Any media type.</span></span>                                                                                                                                    |
| <span data-ttu-id="aad6c-115">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="aad6c-115">Input pin interfaces</span></span>                     | <span data-ttu-id="aad6c-116">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="aad6c-116">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="aad6c-117">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="aad6c-117">Output pin media types</span></span>                   | <span data-ttu-id="aad6c-118">Qualquer tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="aad6c-118">Any media type.</span></span> <span data-ttu-id="aad6c-119">Corresponde ao tipo de mídia de entrada.</span><span class="sxs-lookup"><span data-stu-id="aad6c-119">Matches input media type.</span></span>                                                                                                          |
| <span data-ttu-id="aad6c-120">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="aad6c-120">Output pin interfaces</span></span>                    | <span data-ttu-id="aad6c-121">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="aad6c-121">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="aad6c-122">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="aad6c-122">Filter CLSID</span></span>                             | <span data-ttu-id="aad6c-123">\_SAMPLEGRABBER CLSID</span><span class="sxs-lookup"><span data-stu-id="aad6c-123">CLSID\_SampleGrabber</span></span>                                                                                                                               |
| <span data-ttu-id="aad6c-124">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="aad6c-124">Property Page CLSID</span></span>                      | <span data-ttu-id="aad6c-125">Nenhuma página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="aad6c-125">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="aad6c-126">Executável</span><span class="sxs-lookup"><span data-stu-id="aad6c-126">Executable</span></span>                               | <span data-ttu-id="aad6c-127">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="aad6c-127">Qedit.dll</span></span>                                                                                                                                          |
| [<span data-ttu-id="aad6c-128">Núcleo</span><span class="sxs-lookup"><span data-stu-id="aad6c-128">Merit</span></span>](merit.md)                       | <span data-ttu-id="aad6c-129">MÉRITO \_ \_ não \_ use</span><span class="sxs-lookup"><span data-stu-id="aad6c-129">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="aad6c-130">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="aad6c-130">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="aad6c-131">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="aad6c-131">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="aad6c-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="aad6c-132">Remarks</span></span>

<span data-ttu-id="aad6c-133">Para usar esse filtro, adicione-o ao grafo de filtro e chame [**ISampleGrabber:: SetMediaType**](isamplegrabber-setmediatype.md) com o tipo de mídia desejado.</span><span class="sxs-lookup"><span data-stu-id="aad6c-133">To use this filter, add it to the filter graph and call [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) with the desired media type.</span></span> <span data-ttu-id="aad6c-134">Esse método especifica o tipo de mídia para as conexões de entrada e de pino de saída do filtro.</span><span class="sxs-lookup"><span data-stu-id="aad6c-134">This method specifies the media type for the filter's input and output pin connections.</span></span> <span data-ttu-id="aad6c-135">Em seguida, conecte o filtro a outros filtros no grafo.</span><span class="sxs-lookup"><span data-stu-id="aad6c-135">Then connect the filter to other filters in the graph.</span></span>

<span data-ttu-id="aad6c-136">Se você chamar [**ISampleGrabber:: SetBufferSamples**](isamplegrabber-setbuffersamples.md) com o valor **true**, o filtro armazenará em buffer cada exemplo que ele receber antes de passá-lo downstream.</span><span class="sxs-lookup"><span data-stu-id="aad6c-136">If you call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) with the value **TRUE**, the filter buffers each sample that it receives before passing it downstream.</span></span> <span data-ttu-id="aad6c-137">Chame o método [**ISampleGrabber:: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) para recuperar o conteúdo atual do buffer.</span><span class="sxs-lookup"><span data-stu-id="aad6c-137">Call the [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) method to retrieve the current contents of the buffer.</span></span> <span data-ttu-id="aad6c-138">Como alternativa, você pode chamar [**ISampleGrabber:: SetCallback**](isamplegrabber-setcallback.md) para que o filtro invoque uma função de retorno de chamada sempre que receber um exemplo.</span><span class="sxs-lookup"><span data-stu-id="aad6c-138">Alternatively, you can call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) to have the filter invoke a callback function whenever it receives a sample.</span></span>

<span data-ttu-id="aad6c-139">O filtro tem as seguintes limitações para formatos de vídeo:</span><span class="sxs-lookup"><span data-stu-id="aad6c-139">The filter has the following limitations for video formats:</span></span>

-   <span data-ttu-id="aad6c-140">Ele não dá suporte a tipos de vídeo com orientação de cima para baixo ( **semialtura** negativa).</span><span class="sxs-lookup"><span data-stu-id="aad6c-140">It does not support video types with top-down orientation (negative **biHeight**).</span></span>
-   <span data-ttu-id="aad6c-141">Ele não dá suporte à estrutura de formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (tipo de formato igual ao **formato \_ VideoInfo2**).</span><span class="sxs-lookup"><span data-stu-id="aad6c-141">It does not support the [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format structure (format type equal to **FORMAT\_VideoInfo2**).</span></span>
-   <span data-ttu-id="aad6c-142">Ele rejeita qualquer tipo de vídeo em que o stride da superfície não corresponde à largura do vídeo.</span><span class="sxs-lookup"><span data-stu-id="aad6c-142">It rejects any video type where the surface stride does not match the video width.</span></span>

<span data-ttu-id="aad6c-143">Como resultado, o exemplo de apoio não se conectará ao VMR (Video mixagem Renderer) para alguns tipos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="aad6c-143">As a result, the Sample Grabber will not connect to the Video Mixing Renderer (VMR) for some video types.</span></span>

## <a name="requirements"></a><span data-ttu-id="aad6c-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aad6c-144">Requirements</span></span>



| <span data-ttu-id="aad6c-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="aad6c-145">Requirement</span></span> | <span data-ttu-id="aad6c-146">Valor</span><span class="sxs-lookup"><span data-stu-id="aad6c-146">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aad6c-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aad6c-147">Header</span></span><br/> | <dl> <span data-ttu-id="aad6c-148"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="aad6c-148"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aad6c-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="aad6c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aad6c-150">Objetos de serviços de edição do DirectShow</span><span class="sxs-lookup"><span data-stu-id="aad6c-150">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> <dt>

[<span data-ttu-id="aad6c-151">Usando o exemplo de apoio</span><span class="sxs-lookup"><span data-stu-id="aad6c-151">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> </dl>

 

 




