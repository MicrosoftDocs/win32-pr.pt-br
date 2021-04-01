---
description: Filtro AVI Mux
ms.assetid: 31d30c91-fc6a-45ec-a2e0-34e6a1e902a4
title: Filtro AVI Mux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3755a4d5f63e824ae08eb736a5999dcac3d7ab32
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825990"
---
# <a name="avi-mux-filter"></a><span data-ttu-id="6f9c3-103">Filtro AVI Mux</span><span class="sxs-lookup"><span data-stu-id="6f9c3-103">AVI Mux Filter</span></span>

<span data-ttu-id="6f9c3-104">O filtro AVI Mux aceita vários fluxos de entrada e os intercala no formato AVI.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-104">The AVI Mux filter accepts multiple input streams and interleaves them into AVI format.</span></span> <span data-ttu-id="6f9c3-105">O filtro usa Pins de entrada separados para cada fluxo de entrada e um PIN de saída para o fluxo AVI.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-105">The filter uses separate input pins for each input stream, and one output pin for the AVI stream.</span></span>

<span data-ttu-id="6f9c3-106">Aplicativos de criação ou captura de vídeo podem usar esse filtro para salvar arquivos em disco no formato AVI.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-106">Video capture or authoring applications can use this filter to save files to disk in AVI format.</span></span> <span data-ttu-id="6f9c3-107">O filtro é normalmente conectado ao filtro do [gravador de arquivo](file-writer-filter.md) , mas pode se conectar a qualquer filtro cujo PIN de entrada dê suporte às interfaces IStream e [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="6f9c3-107">The filter is typically connected to the [File Writer](file-writer-filter.md) filter, but it can connect to any filter whose input pin supports the IStream and [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interfaces.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f9c3-108">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="6f9c3-108">Filter Interfaces</span></span></td>
<td><span data-ttu-id="6f9c3-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>IConfigAviMux</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>IConfigInterleaving</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a>, ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="6f9c3-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>IConfigAviMux</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>IConfigInterleaving</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a>, ISpecifyPropertyPages</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f9c3-110">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="6f9c3-110">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="6f9c3-111">Qualquer tipo principal que corresponda a um FOURCC de estilo antigo ou MEDIATYPE_AUXLine21Data.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-111">Any major type that corresponds to an old-style FOURCC, or MEDIATYPE_AUXLine21Data.</span></span> <span data-ttu-id="6f9c3-112">(Para obter mais informações, consulte <a href="fourccmap.md"><strong>classe FOURCCMap</strong></a>.)</span><span class="sxs-lookup"><span data-stu-id="6f9c3-112">(For more information, see <a href="fourccmap.md"><strong>FOURCCMap Class</strong></a>.)</span></span>
<ul>
<li><span data-ttu-id="6f9c3-113">Se o tipo principal for MEDIATYPE_Audio, o formato deverá ser FORMAT_WaveFormatEx.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-113">If the major type is MEDIATYPE_Audio, the format must be FORMAT_WaveFormatEx.</span></span></li>
<li><span data-ttu-id="6f9c3-114">Se o tipo principal for MEDIATYPE_Video, o formato deverá ser FORMAT_VideoInfo ou FORMAT_DvInfo.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-114">If the major type is MEDIATYPE_Video, the format must be FORMAT_VideoInfo or FORMAT_DvInfo.</span></span></li>
<li><span data-ttu-id="6f9c3-115">Se o tipo principal for MEDIATYPE_Interleaved, o formato deverá ser FORMAT_DvInfo.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-115">If the major type is MEDIATYPE_Interleaved, the format must be FORMAT_DvInfo.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f9c3-116">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="6f9c3-116">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="6f9c3-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>IAMStreamControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, IPropertyBag, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f9c3-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>IAMStreamControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, IPropertyBag, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f9c3-118">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="6f9c3-118">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="6f9c3-119">MEDIATYPE_Stream, MEDIASUBTYPE_Avi</span><span class="sxs-lookup"><span data-stu-id="6f9c3-119">MEDIATYPE_Stream, MEDIASUBTYPE_Avi</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f9c3-120">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="6f9c3-120">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="6f9c3-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f9c3-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f9c3-122">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="6f9c3-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="6f9c3-123">CLSID_AviDest</span><span class="sxs-lookup"><span data-stu-id="6f9c3-123">CLSID_AviDest</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f9c3-124">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="6f9c3-124">Property Page CLSID</span></span></td>
<td><span data-ttu-id="6f9c3-125">CLSID_AviMuxProptyPage, CLSID_AviMuxProptyPage1</span><span class="sxs-lookup"><span data-stu-id="6f9c3-125">CLSID_AviMuxProptyPage, CLSID_AviMuxProptyPage1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f9c3-126">Executável</span><span class="sxs-lookup"><span data-stu-id="6f9c3-126">Executable</span></span></td>
<td><span data-ttu-id="6f9c3-127">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="6f9c3-127">qcap.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f9c3-128"><a href="merit.md">Núcleo</a></span><span class="sxs-lookup"><span data-stu-id="6f9c3-128"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="6f9c3-129">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="6f9c3-129">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f9c3-130"><a href="filter-categories.md">Categoria do filtro</a></span><span class="sxs-lookup"><span data-stu-id="6f9c3-130"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="6f9c3-131">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="6f9c3-131">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="remarks"></a><span data-ttu-id="6f9c3-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f9c3-132">Remarks</span></span>

<span data-ttu-id="6f9c3-133">Os comentários a seguir descrevem vários aspectos da funcionalidade do filtro AVI Mux.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-133">The following remarks describe various aspects of the AVI Mux filter's functionality.</span></span>

<span data-ttu-id="6f9c3-134">Pins</span><span class="sxs-lookup"><span data-stu-id="6f9c3-134">Pins</span></span>

<span data-ttu-id="6f9c3-135">Quando o filtro AVI Mux é criado, ele tem um PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-135">When the AVI Mux filter is created, it has one input pin.</span></span> <span data-ttu-id="6f9c3-136">Como cada pino de entrada é conectado, o filtro cria um novo PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-136">As each input pin is connected, the filter creates a new input pin.</span></span>

<span data-ttu-id="6f9c3-137">Propriedades do fluxo</span><span class="sxs-lookup"><span data-stu-id="6f9c3-137">Stream Properties</span></span>

<span data-ttu-id="6f9c3-138">Os Pins de entrada dão suporte à interface IPropertyBag para definir propriedades em fluxos individuais.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-138">The input pins support the IPropertyBag interface for setting properties on individual streams.</span></span> <span data-ttu-id="6f9c3-139">Atualmente, a seguinte propriedade é definida:</span><span class="sxs-lookup"><span data-stu-id="6f9c3-139">Currently, the following property is defined:</span></span>



| <span data-ttu-id="6f9c3-140">Propriedade</span><span class="sxs-lookup"><span data-stu-id="6f9c3-140">Property</span></span> | <span data-ttu-id="6f9c3-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f9c3-141">Description</span></span>                                                           |
|----------|-----------------------------------------------------------------------|
| <span data-ttu-id="6f9c3-142">name</span><span class="sxs-lookup"><span data-stu-id="6f9c3-142">name</span></span>     | <span data-ttu-id="6f9c3-143">O nome do fluxo.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-143">The name of the stream.</span></span> <span data-ttu-id="6f9c3-144">Essa propriedade é gravada como uma `'strn'` parte.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-144">This property is written as a `'strn'` chunk.</span></span> |



 

<span data-ttu-id="6f9c3-145">Se o filtro estiver em execução ou em pausa, o método IPropertyBag:: Write retornará \_ VFW \_ E \_ estado incorreto.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-145">If the filter is running or paused, the IPropertyBag::Write method returns VFW\_E\_WRONG\_STATE.</span></span>

<span data-ttu-id="6f9c3-146">Taxas de quadros</span><span class="sxs-lookup"><span data-stu-id="6f9c3-146">Frame Rates</span></span>

<span data-ttu-id="6f9c3-147">Se o filtro upstream não especificar uma taxa de quadros no membro **AvgTimePerFrame** da estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , o AVI Mux usará os carimbos de data/hora no primeiro quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-147">If the upstream filter does not specify a frame rate in the **AvgTimePerFrame** member of the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure, the AVI Mux uses the time stamps on the first video frame.</span></span> <span data-ttu-id="6f9c3-148">O formato de arquivo AVI não oferece suporte a taxas de quadros variáveis.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-148">The AVI file format does not support variable frame rates.</span></span>

<span data-ttu-id="6f9c3-149">Quadros descartados</span><span class="sxs-lookup"><span data-stu-id="6f9c3-149">Dropped Frames</span></span>

<span data-ttu-id="6f9c3-150">O filtro AVI Mux calcula os quadros descartados com base nos tempos de mídia de cada amostra, se disponíveis ou os carimbos de data/hora do exemplo.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-150">The AVI Mux filter calculates dropped frames based on each sample's media times, if available, or else the sample's time stamps.</span></span> <span data-ttu-id="6f9c3-151">Ele grava uma entrada de índice de comprimento zero para cada quadro Descartado.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-151">It writes a zero-length index entry for every dropped frame.</span></span>

<span data-ttu-id="6f9c3-152">IMediaSeeking</span><span class="sxs-lookup"><span data-stu-id="6f9c3-152">IMediaSeeking</span></span>

<span data-ttu-id="6f9c3-153">O filtro AVI Mux implementa a interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6f9c3-153">The AVI Mux filter implements the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface as follows:</span></span>

-   <span data-ttu-id="6f9c3-154">O método [**getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) retorna o progresso atual da multiplexação.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-154">The [**GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method returns the current progress of the multiplexing.</span></span> <span data-ttu-id="6f9c3-155">Se você estiver transcodificando um arquivo (mais lento do que o tempo real), esse valor será mais preciso do que o valor retornado pelo Gerenciador do gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-155">If you are transcoding a file (slower than real time), this value is more accurate than the value returned by the Filter Graph Manager.</span></span> <span data-ttu-id="6f9c3-156">Para obter mais informações, consulte a seção comentários da página de referência do GetCurrentPosition.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-156">For more information, see the Remarks section of the GetCurrentPosition reference page.</span></span>
-   <span data-ttu-id="6f9c3-157">O método [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) consulta cada filtro upstream e retorna a duração do fluxo mais longo.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-157">The [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method queries each upstream filter and returns the duration of the longest stream.</span></span> <span data-ttu-id="6f9c3-158">Se qualquer um desses filtros falhar na chamada getDuration (ou não oferecer suporte a IMediaSeeking), o AVI Mux retornará um código de falha e preencherá o parâmetro *pDuration* com a duração mais longa encontrada.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-158">If any of these filters fails the GetDuration call (or does not support IMediaSeeking), the AVI Mux returns a failure code and fills in the *pDuration* parameter with the longest duration found.</span></span> <span data-ttu-id="6f9c3-159">No entanto, o valor de *pDuration* nesse caso não é necessariamente o comprimento do fluxo de entrada mais longo.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-159">However, the value of *pDuration* in this case is not necessarily the length of the longest input stream.</span></span>
-   <span data-ttu-id="6f9c3-160">O AVI Mux não implementa os métodos GetStopPosition, GetPositions, GetAvailable, GetRate ou GetPreroll; Nem implementa nenhum \* método definido para busca.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-160">The AVI Mux does not implement the GetStopPosition, GetPositions, GetAvailable, GetRate, or GetPreroll methods; nor does it implement any Set\* methods for seeking.</span></span>

<span data-ttu-id="6f9c3-161">Extensões de formato de arquivo AVI 2,0</span><span class="sxs-lookup"><span data-stu-id="6f9c3-161">AVI 2.0 File Format Extensions</span></span>

<span data-ttu-id="6f9c3-162">Atualmente, o DirectShow dá suporte às seguintes extensões de formato de arquivo AVI 2,0:</span><span class="sxs-lookup"><span data-stu-id="6f9c3-162">DirectShow currently supports the following AVI 2.0 file format extensions:</span></span>

-   <span data-ttu-id="6f9c3-163">Maior tamanho de arquivo AVI (maior que 1 GB)</span><span class="sxs-lookup"><span data-stu-id="6f9c3-163">Increased AVI file size (greater than 1 GB)</span></span>
-   <span data-ttu-id="6f9c3-164">Indexação hierárquica</span><span class="sxs-lookup"><span data-stu-id="6f9c3-164">Hierarchical indexing</span></span>

<span data-ttu-id="6f9c3-165">Para obter mais informações, consulte a versão 1, 2 do "OpenDML AVI File Format Extensions" publicado pelo Subcomitê OpenDML AVI M-JPEG File Format.</span><span class="sxs-lookup"><span data-stu-id="6f9c3-165">For more information, see version 1.02 of the "OpenDML AVI File Format Extensions" published by the OpenDML AVI M-JPEG File Format Subcommittee.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f9c3-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6f9c3-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f9c3-167">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="6f9c3-167">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



