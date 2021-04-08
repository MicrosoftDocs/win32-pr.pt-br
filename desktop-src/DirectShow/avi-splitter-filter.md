---
description: Filtro de Splitter AVI
ms.assetid: df3c7d11-7ecc-499a-af36-b74437e21999
title: Filtro de Splitter AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e61b9a60c4c42aafa875c166ae08ccdf337793c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087872"
---
# <a name="avi-splitter-filter"></a><span data-ttu-id="c846c-103">Filtro de Splitter AVI</span><span class="sxs-lookup"><span data-stu-id="c846c-103">AVI Splitter Filter</span></span>

<span data-ttu-id="c846c-104">O filtro de Splitter AVI é usado para reprodução de arquivos AVI.</span><span class="sxs-lookup"><span data-stu-id="c846c-104">The AVI Splitter Filter is used for playback of AVI files.</span></span> <span data-ttu-id="c846c-105">Ele aceita dados no formato AVI e os divide em seus fluxos constituintes para processamento e/ou renderização adicionais.</span><span class="sxs-lookup"><span data-stu-id="c846c-105">It accepts data in AVI format and splits it into its constituent streams for further processing and/or rendering.</span></span>



|                                          |                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c846c-106">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="c846c-106">Filter Interfaces</span></span>                        | <span data-ttu-id="c846c-107">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span><span class="sxs-lookup"><span data-stu-id="c846c-107">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span></span>                        |
| <span data-ttu-id="c846c-108">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="c846c-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="c846c-109">\_Fluxo de MediaType, MEDIASUBTYPE \_ avi</span><span class="sxs-lookup"><span data-stu-id="c846c-109">MEDIATYPE\_Stream, MEDIASUBTYPE\_Avi</span></span>                                                                                                                                |
| <span data-ttu-id="c846c-110">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="c846c-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="c846c-111">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="c846c-111">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                    |
| <span data-ttu-id="c846c-112">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="c846c-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="c846c-113">Normalmente **, \_ vídeo de MediaType** ou **\_ áudio de MediaType**.</span><span class="sxs-lookup"><span data-stu-id="c846c-113">Typically **MEDIATYPE\_Video** or **MEDIATYPE\_Audio**.</span></span> <span data-ttu-id="c846c-114">O tipo exato depende do conteúdo do arquivo, se o arquivo está compactado e qual codec foi usado.</span><span class="sxs-lookup"><span data-stu-id="c846c-114">The exact type depends on the content of the file, whether the file is compressed, and what codec was used.</span></span> |
| <span data-ttu-id="c846c-115">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="c846c-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="c846c-116">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="c846c-116">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>    |
| <span data-ttu-id="c846c-117">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="c846c-117">Filter CLSID</span></span>                             | <span data-ttu-id="c846c-118">\_AVISPLITTER CLSID</span><span class="sxs-lookup"><span data-stu-id="c846c-118">CLSID\_AviSplitter</span></span>                                                                                                                                                  |
| <span data-ttu-id="c846c-119">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="c846c-119">Property Page CLSID</span></span>                      | <span data-ttu-id="c846c-120">Nenhuma página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c846c-120">No property page.</span></span>                                                                                                                                                   |
| <span data-ttu-id="c846c-121">Executável</span><span class="sxs-lookup"><span data-stu-id="c846c-121">Executable</span></span>                               | <span data-ttu-id="c846c-122">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="c846c-122">quartz.dll</span></span>                                                                                                                                                          |
| [<span data-ttu-id="c846c-123">Núcleo</span><span class="sxs-lookup"><span data-stu-id="c846c-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="c846c-124">MÉRITO \_ normal</span><span class="sxs-lookup"><span data-stu-id="c846c-124">MERIT\_NORMAL</span></span>                                                                                                                                                       |
| [<span data-ttu-id="c846c-125">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="c846c-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="c846c-126">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="c846c-126">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="c846c-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="c846c-127">Remarks</span></span>

<span data-ttu-id="c846c-128">Esse filtro é normalmente conectado ao filtro de [origem de arquivo assíncrono](file-source--async--filter.md) em seu pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="c846c-128">This filter is typically connected to the [Async File Source](file-source--async--filter.md) filter on its input pin.</span></span> <span data-ttu-id="c846c-129">Ele pode se conectar a qualquer filtro cujo PIN de saída dê suporte a [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) e oferece o tipo de mídia correto para o pino de entrada do filtro AVI Splitter.</span><span class="sxs-lookup"><span data-stu-id="c846c-129">It can connect to any filter whose output pin supports [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) and offers the correct media type to the AVI Splitter filter's input pin.</span></span>

<span data-ttu-id="c846c-130">Os Pins de saída no divisor AVI dão suporte ao método IPropertyBag:: Read para a leitura de propriedades de fluxos individuais.</span><span class="sxs-lookup"><span data-stu-id="c846c-130">The output pins on the AVI Splitter support the IPropertyBag::Read method for reading properties from individual streams.</span></span> <span data-ttu-id="c846c-131">Atualmente, a propriedade a seguir é definida.</span><span class="sxs-lookup"><span data-stu-id="c846c-131">Currently, the following property is defined.</span></span>



| <span data-ttu-id="c846c-132">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c846c-132">Property</span></span> | <span data-ttu-id="c846c-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="c846c-133">Description</span></span>                                                                                                                                    |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c846c-134">name</span><span class="sxs-lookup"><span data-stu-id="c846c-134">name</span></span>     | <span data-ttu-id="c846c-135">Retorna o nome do fluxo, extraído da `'strn'` parte no arquivo avi.</span><span class="sxs-lookup"><span data-stu-id="c846c-135">Returns the name of the stream, taken from the `'strn'` chunk in the AVI file.</span></span> <span data-ttu-id="c846c-136">Se essa parte estiver ausente, o método Read retornará E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="c846c-136">If this chunk is absent, the Read method returns E\_INVALIDARG.</span></span> |



 

<span data-ttu-id="c846c-137">O método IPropertyBag:: Write retorna E \_ falha.</span><span class="sxs-lookup"><span data-stu-id="c846c-137">The IPropertyBag::Write method returns E\_FAIL.</span></span> <span data-ttu-id="c846c-138">O filtro [AVI Mux](avi-mux-filter.md) dá suporte a IPropertyBag:: Write para salvar propriedades de fluxo em um arquivo avi.</span><span class="sxs-lookup"><span data-stu-id="c846c-138">The [AVI Mux](avi-mux-filter.md) filter supports IPropertyBag::Write for saving stream properties into an AVI file.</span></span>

<span data-ttu-id="c846c-139">O divisor AVI não permite que filtros downstream usem seu próprio alocador.</span><span class="sxs-lookup"><span data-stu-id="c846c-139">The AVI Splitter does not allow downstream filters to use their own allocator.</span></span>

<span data-ttu-id="c846c-140">A duração de intercalação no arquivo determina a quantidade de memória que o divisor AVI alocará para processá-lo.</span><span class="sxs-lookup"><span data-stu-id="c846c-140">The interleaving duration in the file determines how much memory the AVI Splitter will allocate to process it.</span></span> <span data-ttu-id="c846c-141">Um arquivo Intercalado em uma segunda parte exigirá muito mais memória para ser processado do que um arquivo cuja duração da intercalação seja definida como um ou dois quadros.</span><span class="sxs-lookup"><span data-stu-id="c846c-141">A file that is interleaved in one second chunks will require much more memory to process than a file whose interleave duration is set to one or two frames.</span></span> <span data-ttu-id="c846c-142">Em computadores modernos, isso geralmente não é um problema, a menos que você esteja executando várias instâncias do divisor AVI simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="c846c-142">On modern computers, this is generally not an issue unless you are running multiple instances of the AVI Splitter simultaneously.</span></span>

### <a name="seeking"></a><span data-ttu-id="c846c-143">Atingir</span><span class="sxs-lookup"><span data-stu-id="c846c-143">Seeking</span></span>

<span data-ttu-id="c846c-144">Se o arquivo contiver um fluxo de vídeo, o divisor AVI oferecerá suporte à busca por número de quadro.</span><span class="sxs-lookup"><span data-stu-id="c846c-144">If the file contains a video stream, the AVI Splitter supports seeking by frame number.</span></span> <span data-ttu-id="c846c-145">Para habilitar a busca baseada em quadros, chame [**IMediaSeeking:: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) no [Gerenciador de gráficos de filtro](filter-graph-manager.md) com o **\_ \_ quadro formato de tempo** de valor.</span><span class="sxs-lookup"><span data-stu-id="c846c-145">To enable frame-based seeking, call [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the [Filter Graph Manager](filter-graph-manager.md) with the value **TIME\_FORMAT\_FRAME**.</span></span>

<span data-ttu-id="c846c-146">Se o arquivo contiver um fluxo de áudio, o divisor AVI oferecerá suporte à busca por número de exemplo.</span><span class="sxs-lookup"><span data-stu-id="c846c-146">If the file contains an audio stream, the AVI Splitter supports seeking by sample number.</span></span> <span data-ttu-id="c846c-147">Para habilitar a busca com base em amostra, chame [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) no Gerenciador do grafo de filtro com o valor de **formato de tempo \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="c846c-147">To enable sample-based seeking, call [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the Filter Graph Manager with the value **TIME\_FORMAT\_SAMPLE**.</span></span>

<span data-ttu-id="c846c-148">Em ambos os casos, o pino de saída para esse fluxo deve ser conectado a um filtro de renderizador.</span><span class="sxs-lookup"><span data-stu-id="c846c-148">In both cases, the output pin for that stream must be connected to a renderer filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c846c-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c846c-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c846c-150">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="c846c-150">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



