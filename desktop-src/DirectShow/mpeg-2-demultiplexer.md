---
description: Esse filtro desmultiplexa o transporte MPEG-2 e os fluxos de programa que são entregues no modo de push.
ms.assetid: 99bfc55d-6519-4e85-98ce-cad27bd71ffb
title: Demultiplexador MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ea71727dc273bd0dc5d65ac49b28385b4898067
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105759992"
---
# <a name="mpeg-2-demultiplexer"></a><span data-ttu-id="0b6c7-103">Demultiplexador MPEG-2</span><span class="sxs-lookup"><span data-stu-id="0b6c7-103">MPEG-2 Demultiplexer</span></span>

<span data-ttu-id="0b6c7-104">Esse filtro desmultiplexa o transporte MPEG-2 e os fluxos de programa que são entregues no modo de push.</span><span class="sxs-lookup"><span data-stu-id="0b6c7-104">This filter demultiplexes MPEG-2 transport and program streams that are delivered in push-mode.</span></span> <span data-ttu-id="0b6c7-105">A partir do Windows XP, esse filtro também dá suporte a fluxos de programa no modo de pull (reprodução de arquivo).</span><span class="sxs-lookup"><span data-stu-id="0b6c7-105">Starting in Windows XP, this filter also supports program streams in pull mode (file playback).</span></span> <span data-ttu-id="0b6c7-106">Em plataformas anteriores, use o filtro [divisor MPEG-2](mpeg-2-splitter.md) para fluxos de programa no modo de pull.</span><span class="sxs-lookup"><span data-stu-id="0b6c7-106">On earlier platforms, use the [MPEG-2 Splitter](mpeg-2-splitter.md) filter for program streams in pull mode.</span></span> <span data-ttu-id="0b6c7-107">Esse filtro pode ser usado em qualquer tipo de grafo de filtro, incluindo um gráfico de filtro de TV digital BDA.</span><span class="sxs-lookup"><span data-stu-id="0b6c7-107">This filter can be used in any type of filter graph, including a BDA digital TV filter graph.</span></span>

> [!Note]  
> <span data-ttu-id="0b6c7-108">O demultiplexador MPEG-2 não dá suporte à busca com precisão de quadro.</span><span class="sxs-lookup"><span data-stu-id="0b6c7-108">The MPEG-2 Demultiplexer does not support frame-accurate seeking.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0b6c7-109">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="0b6c7-109">Filter Interfaces</span></span></td>
<td><span data-ttu-id="0b6c7-110">Todos os modos:</span><span class="sxs-lookup"><span data-stu-id="0b6c7-110">All modes:</span></span><br/>
<ul>
<li><span data-ttu-id="0b6c7-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="0b6c7-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="0b6c7-112"><strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="0b6c7-112"><strong>ISpecifyPropertyPages</strong></span></span></li>
</ul>
<span data-ttu-id="0b6c7-113">Somente modo de push:</span><span class="sxs-lookup"><span data-stu-id="0b6c7-113">Push mode only:</span></span><br/>
<ul>
<li><span data-ttu-id="0b6c7-114"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span><span class="sxs-lookup"><span data-stu-id="0b6c7-114"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span></span></li>
<li><span data-ttu-id="0b6c7-115"><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></span><span class="sxs-lookup"><span data-stu-id="0b6c7-115"><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></span></span></li>
<li><span data-ttu-id="0b6c7-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span><span class="sxs-lookup"><span data-stu-id="0b6c7-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b6c7-117">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="0b6c7-117">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="0b6c7-118">Tipo principal: MEDIATYPE_STREAM</span><span class="sxs-lookup"><span data-stu-id="0b6c7-118">Major type: MEDIATYPE_STREAM</span></span><br/> <span data-ttu-id="0b6c7-119">Subtipo</span><span class="sxs-lookup"><span data-stu-id="0b6c7-119">Subtype:</span></span><br/>
<ul>
<li><span data-ttu-id="0b6c7-120">KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</span><span class="sxs-lookup"><span data-stu-id="0b6c7-120">KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</span></span></li>
<li><span data-ttu-id="0b6c7-121">MEDIASUBTYPE_MPEG2_PROGRAM</span><span class="sxs-lookup"><span data-stu-id="0b6c7-121">MEDIASUBTYPE_MPEG2_PROGRAM</span></span></li>
<li><span data-ttu-id="0b6c7-122">MEDIASUBTYPE_MPEG2_TRANSPORT</span><span class="sxs-lookup"><span data-stu-id="0b6c7-122">MEDIASUBTYPE_MPEG2_TRANSPORT</span></span></li>
<li><span data-ttu-id="0b6c7-123">MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</span><span class="sxs-lookup"><span data-stu-id="0b6c7-123">MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</span></span></li>
</ul>
<span data-ttu-id="0b6c7-124">Para obter mais informações, consulte <a href="mpeg-2-demultiplexer-media-types.md"><strong>tipos de mídia do demultiplexador MPEG-2</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0b6c7-124">For more information, see <a href="mpeg-2-demultiplexer-media-types.md"><strong>MPEG-2 Demultiplexer Media Types</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0b6c7-125">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="0b6c7-125">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="0b6c7-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="0b6c7-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b6c7-127">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="0b6c7-127">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="0b6c7-128">Os fluxos elementares de áudio e vídeo devem ter um tipo principal de MEDIATYPE_Audio ou MEDIATYPE_Video.</span><span class="sxs-lookup"><span data-stu-id="0b6c7-128">Audio and video elementary streams must have a major type of MEDIATYPE_Audio or MEDIATYPE_Video.</span></span><br/> <span data-ttu-id="0b6c7-129">Para obter mais informações, consulte <a href="mpeg-2-demultiplexer-media-types.md"><strong>tipos de mídia do demultiplexador MPEG-2</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0b6c7-129">For more information, see <a href="mpeg-2-demultiplexer-media-types.md"><strong>MPEG-2 Demultiplexer Media Types</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0b6c7-130">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="0b6c7-130">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="0b6c7-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>somente modo push: <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>IAMPushSource</strong></a>, <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a></span><span class="sxs-lookup"><span data-stu-id="0b6c7-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>Push mode only: <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>IAMPushSource</strong></a>, <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a></span></span><br/> <span data-ttu-id="0b6c7-132">Somente modo de pull: <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="0b6c7-132">Pull mode only: <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b6c7-133">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="0b6c7-133">Filter CLSID</span></span></td>
<td><span data-ttu-id="0b6c7-134">CLSID_MPEG2Demultiplexer</span><span class="sxs-lookup"><span data-stu-id="0b6c7-134">CLSID_MPEG2Demultiplexer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0b6c7-135">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="0b6c7-135">Property Page CLSID</span></span></td>
<td><span data-ttu-id="0b6c7-136">Disponível somente para teste.</span><span class="sxs-lookup"><span data-stu-id="0b6c7-136">Available for testing only.</span></span> <span data-ttu-id="0b6c7-137">Usar a interface <strong>ISpecifyPropertyPages</strong> para acessar as páginas de propriedades</span><span class="sxs-lookup"><span data-stu-id="0b6c7-137">Use the <strong>ISpecifyPropertyPages</strong> interface to access the property pages</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b6c7-138">Executável</span><span class="sxs-lookup"><span data-stu-id="0b6c7-138">Executable</span></span></td>
<td><span data-ttu-id="0b6c7-139">mpg2splt.ax</span><span class="sxs-lookup"><span data-stu-id="0b6c7-139">mpg2splt.ax</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0b6c7-140"><a href="merit.md">Núcleo</a></span><span class="sxs-lookup"><span data-stu-id="0b6c7-140"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="0b6c7-141">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="0b6c7-141">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b6c7-142"><a href="filter-categories.md">Categoria do filtro</a></span><span class="sxs-lookup"><span data-stu-id="0b6c7-142"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="0b6c7-143">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="0b6c7-143">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="0b6c7-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b6c7-144">Remarks</span></span>

<span data-ttu-id="0b6c7-145">Para gerar fluxos de áudio e vídeo elementares, o Demux deve receber os fluxos de PCR e SCR.</span><span class="sxs-lookup"><span data-stu-id="0b6c7-145">To output audio and video elementary streams, the demux must receive the PCR and SCR streams.</span></span> <span data-ttu-id="0b6c7-146">No lado da entrada, isso significa que um fluxo de transporte deve conter as tabelas PAT e PGTO que definem o PID para o fluxo de PCR; e fluxos de programa devem conter pelo menos um cabeçalho de pacote.</span><span class="sxs-lookup"><span data-stu-id="0b6c7-146">On the input side, this means a transport stream must contain the PAT and PMT tables that define the PID for the PCR stream; and program streams must contain at least one pack header.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b6c7-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b6c7-147">Requirements</span></span>



| <span data-ttu-id="0b6c7-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b6c7-148">Requirement</span></span> | <span data-ttu-id="0b6c7-149">Valor</span><span class="sxs-lookup"><span data-stu-id="0b6c7-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0b6c7-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b6c7-150">Minimum supported client</span></span><br/> | <span data-ttu-id="0b6c7-151">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0b6c7-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0b6c7-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b6c7-152">Minimum supported server</span></span><br/> | <span data-ttu-id="0b6c7-153">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0b6c7-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0b6c7-154">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="0b6c7-154">End of server support</span></span><br/>    | <span data-ttu-id="0b6c7-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0b6c7-155">Windows Server 2003 R2</span></span><br/>                          |



## <a name="see-also"></a><span data-ttu-id="0b6c7-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b6c7-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b6c7-157">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="0b6c7-157">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="0b6c7-158">Usando o demultiplexador MPEG-2</span><span class="sxs-lookup"><span data-stu-id="0b6c7-158">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 




