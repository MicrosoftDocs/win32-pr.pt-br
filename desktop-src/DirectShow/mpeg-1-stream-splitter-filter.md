---
description: Filtro de divisor de fluxo MPEG-1
ms.assetid: abadf37f-2876-496d-90e7-77c3475a0064
title: Filtro de divisor de fluxo MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec47e5ad8df16446c588beec2c5d1c2606b9b1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087839"
---
# <a name="mpeg-1-stream-splitter-filter"></a><span data-ttu-id="02bda-103">Filtro de divisor de fluxo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="02bda-103">MPEG-1 Stream Splitter Filter</span></span>

<span data-ttu-id="02bda-104">Esse filtro divide um fluxo do sistema MPEG-1 em seus fluxos de áudio e vídeo do componente.</span><span class="sxs-lookup"><span data-stu-id="02bda-104">This filter splits an MPEG-1 system stream into its component audio and video streams.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="02bda-105">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="02bda-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="02bda-106"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="02bda-106"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02bda-107">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="02bda-107">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="02bda-108">Tipo principal: MEDIATYPE_Stream</span><span class="sxs-lookup"><span data-stu-id="02bda-108">Major type: MEDIATYPE_Stream</span></span><br/> <span data-ttu-id="02bda-109">Subtipos</span><span class="sxs-lookup"><span data-stu-id="02bda-109">Subtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="02bda-110">MEDIASUBTYPE_MPEG1System</span><span class="sxs-lookup"><span data-stu-id="02bda-110">MEDIASUBTYPE_MPEG1System</span></span></li>
<li><span data-ttu-id="02bda-111">MEDIASUBTYPE_MPEG1VideoCD</span><span class="sxs-lookup"><span data-stu-id="02bda-111">MEDIASUBTYPE_MPEG1VideoCD</span></span></li>
<li><span data-ttu-id="02bda-112">MEDIASUBTYPE_Audio</span><span class="sxs-lookup"><span data-stu-id="02bda-112">MEDIASUBTYPE_Audio</span></span></li>
<li><span data-ttu-id="02bda-113">MEDIASUBTYPE_Video</span><span class="sxs-lookup"><span data-stu-id="02bda-113">MEDIASUBTYPE_Video</span></span></li>
</ul>
<span data-ttu-id="02bda-114">Consulte <a href="mpeg-1-media-types.md"> <strong>tipos de mídia MPEG-1</strong></a></span><span class="sxs-lookup"><span data-stu-id="02bda-114">See <a href="mpeg-1-media-types.md"><strong>MPEG-1 Media Types</strong></a></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02bda-115">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="02bda-115">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="02bda-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="02bda-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02bda-117">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="02bda-117">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="02bda-118">Tipo principal: MEDIATYPE_Audio ou MEDIATYPE_Video</span><span class="sxs-lookup"><span data-stu-id="02bda-118">Major type: MEDIATYPE_Audio or MEDIATYPE_Video</span></span><br/> <span data-ttu-id="02bda-119">Subtipo: MEDIASUBTYPE_MPEG1Payload ou MEDIASUBTYPE_MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="02bda-119">Subtype: MEDIASUBTYPE_MPEG1Payload or MEDIASUBTYPE_MPEG1Packet</span></span><br/> <span data-ttu-id="02bda-120">Consulte <a href="mpeg-1-media-types.md"> <strong>tipos de mídia MPEG-1</strong></a></span><span class="sxs-lookup"><span data-stu-id="02bda-120">See <a href="mpeg-1-media-types.md"><strong>MPEG-1 Media Types</strong></a></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02bda-121">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="02bda-121">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="02bda-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="02bda-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02bda-123">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="02bda-123">Filter CLSID</span></span></td>
<td><span data-ttu-id="02bda-124">CLSID_MPEG1Splitter</span><span class="sxs-lookup"><span data-stu-id="02bda-124">CLSID_MPEG1Splitter</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02bda-125">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="02bda-125">Property Page CLSID</span></span></td>
<td><span data-ttu-id="02bda-126">Nenhuma página de propriedades</span><span class="sxs-lookup"><span data-stu-id="02bda-126">No property page</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02bda-127">Executável</span><span class="sxs-lookup"><span data-stu-id="02bda-127">Executable</span></span></td>
<td><span data-ttu-id="02bda-128">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="02bda-128">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02bda-129"><a href="merit.md">Núcleo</a></span><span class="sxs-lookup"><span data-stu-id="02bda-129"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="02bda-130">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="02bda-130">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02bda-131"><a href="filter-categories.md">Categoria do filtro</a></span><span class="sxs-lookup"><span data-stu-id="02bda-131"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="02bda-132">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="02bda-132">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="02bda-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="02bda-133">Remarks</span></span>

<span data-ttu-id="02bda-134">Este arquivo dá suporte ao modo de pull somente por meio de [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) ; Ele não dá suporte ao modo de push.</span><span class="sxs-lookup"><span data-stu-id="02bda-134">This file supports pull mode via [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) only; it does not support push mode.</span></span>

<span data-ttu-id="02bda-135">Como o conteúdo MPEG-1 não é indexado, a busca pode ser muito aproximada.</span><span class="sxs-lookup"><span data-stu-id="02bda-135">Because MPEG-1 content is not indexed, seeking can be very approximate.</span></span> <span data-ttu-id="02bda-136">Geralmente é bom para um fluxo de sistema de taxa de bits MPEG-1 fixo (que geralmente é gerado pelo hardware para o CD de vídeo).</span><span class="sxs-lookup"><span data-stu-id="02bda-136">It is usually good for a fixed bitrate MPEG-1 system stream (which is usually hardware generated for video CD).</span></span>

<span data-ttu-id="02bda-137">O filtro dá suporte à interface [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) para recuperar metadados ID3.</span><span class="sxs-lookup"><span data-stu-id="02bda-137">The filter supports the [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) interface for retrieving ID3 metadata.</span></span>

<span data-ttu-id="02bda-138">Nem todas as amostras MPEG têm carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="02bda-138">Not all MPEG samples have time stamps.</span></span> <span data-ttu-id="02bda-139">A falta de um carimbo de data/hora em um exemplo de MPEG não é um erro.</span><span class="sxs-lookup"><span data-stu-id="02bda-139">The lack of a time stamp on an MPEG sample is not an error.</span></span> <span data-ttu-id="02bda-140">Para os desenvolvedores de filtro, isso significa que você não deve retornar um código de erro do método **Receive** do PIN de entrada se [**IMediaSample:: getTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) falhar.</span><span class="sxs-lookup"><span data-stu-id="02bda-140">For filter developers, this means that you should not return an error code from your input pin's **Receive** method if [**IMediaSample::GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) fails.</span></span> <span data-ttu-id="02bda-141">Se **Receive** retornar qualquer valor diferente de S \_ OK, isso fará com que o divisor pare de enviar amostras.</span><span class="sxs-lookup"><span data-stu-id="02bda-141">If **Receive** returns any value other than S\_OK, it will cause the splitter to stop sending samples.</span></span>

<span data-ttu-id="02bda-142">Se o arquivo contiver um fluxo de vídeo, o divisor de fluxo MPEG-1 dará suporte à busca por número de quadro.</span><span class="sxs-lookup"><span data-stu-id="02bda-142">If the file contains a video stream, the MPEG-1 Stream Splitter supports seeking by frame number.</span></span> <span data-ttu-id="02bda-143">Para habilitar a busca baseada em quadros, chame [**IMediaSeeking:: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) no [Gerenciador de gráficos de filtro](filter-graph-manager.md) com o **\_ \_ quadro formato de tempo** de valor.</span><span class="sxs-lookup"><span data-stu-id="02bda-143">To enable frame-based seeking, call [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the [Filter Graph Manager](filter-graph-manager.md) with the value **TIME\_FORMAT\_FRAME**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02bda-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="02bda-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02bda-145">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="02bda-145">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




