---
description: Filtro de descompactação de QT
ms.assetid: d013075f-deab-40ef-8438-4fb09820da3e
title: Filtro de descompactação de QT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e586eb9d65ee00509f4a434f3283bd762d535b26
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456563"
---
# <a name="qt-decompressor-filter"></a><span data-ttu-id="fc9cb-103">Filtro de descompactação de QT</span><span class="sxs-lookup"><span data-stu-id="fc9cb-103">QT Decompressor Filter</span></span>

<span data-ttu-id="fc9cb-104">Este componente foi removido do Windows Vista e de sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="fc9cb-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="fc9cb-105">Ele está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fc9cb-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="fc9cb-106">O filtro de descompactação QT descompacta vídeo Apple® QuickTime® 2,0.</span><span class="sxs-lookup"><span data-stu-id="fc9cb-106">The QT Decompressor filter decompresses Apple® QuickTime® 2.0 video.</span></span> <span data-ttu-id="fc9cb-107">Esse formato é normalmente usado em arquivos mais antigos do QuickTime.</span><span class="sxs-lookup"><span data-stu-id="fc9cb-107">This format is typically used in older QuickTime files.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fc9cb-108">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="fc9cb-108">Filter Interfaces</span></span></td>
<td><span data-ttu-id="fc9cb-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc9cb-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc9cb-110">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="fc9cb-110">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="fc9cb-111">MEDIATYPE_Video, FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="fc9cb-111">MEDIATYPE_Video, FORMAT_VideoInfo</span></span><br/> <span data-ttu-id="fc9cb-112">Os seguintes subtipos são válidos:</span><span class="sxs-lookup"><span data-stu-id="fc9cb-112">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="fc9cb-113">MEDIASUBTYPE_QTRpza</span><span class="sxs-lookup"><span data-stu-id="fc9cb-113">MEDIASUBTYPE_QTRpza</span></span></li>
<li><span data-ttu-id="fc9cb-114">MEDIASUBTYPE_QTSmc</span><span class="sxs-lookup"><span data-stu-id="fc9cb-114">MEDIASUBTYPE_QTSmc</span></span></li>
<li><span data-ttu-id="fc9cb-115">MEDIASUBTYPE_QTRle</span><span class="sxs-lookup"><span data-stu-id="fc9cb-115">MEDIASUBTYPE_QTRle</span></span></li>
<li><span data-ttu-id="fc9cb-116">MEDIASUBTYPE_QTJpeg</span><span class="sxs-lookup"><span data-stu-id="fc9cb-116">MEDIASUBTYPE_QTJpeg</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc9cb-117">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="fc9cb-117">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="fc9cb-118"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc9cb-118"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc9cb-119">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="fc9cb-119">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="fc9cb-120">MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="fc9cb-120">MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc9cb-121">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="fc9cb-121">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="fc9cb-122"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc9cb-122"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc9cb-123">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="fc9cb-123">Filter CLSID</span></span></td>
<td><span data-ttu-id="fc9cb-124">CLSID_QTDec</span><span class="sxs-lookup"><span data-stu-id="fc9cb-124">CLSID_QTDec</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc9cb-125">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="fc9cb-125">Property Page CLSID</span></span></td>
<td><span data-ttu-id="fc9cb-126">Nenhuma página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="fc9cb-126">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc9cb-127">Executável</span><span class="sxs-lookup"><span data-stu-id="fc9cb-127">Executable</span></span></td>
<td><span data-ttu-id="fc9cb-128">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="fc9cb-128">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc9cb-129"><a href="merit.md">Núcleo</a></span><span class="sxs-lookup"><span data-stu-id="fc9cb-129"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="fc9cb-130">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="fc9cb-130">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc9cb-131"><a href="filter-categories.md">Categoria do filtro</a></span><span class="sxs-lookup"><span data-stu-id="fc9cb-131"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="fc9cb-132">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="fc9cb-132">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="fc9cb-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc9cb-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc9cb-134">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="fc9cb-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




