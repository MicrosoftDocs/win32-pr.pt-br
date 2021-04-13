---
description: Filtro de navegador de DVD
ms.assetid: 3b2c01a2-d52c-4497-8fc9-d1113e8507e8
title: Filtro de navegador de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53bb1c6f46e3dd846ffccda32fece2c2f04c8992
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456658"
---
# <a name="dvd-navigator-filter"></a><span data-ttu-id="5d09b-103">Filtro de navegador de DVD</span><span class="sxs-lookup"><span data-stu-id="5d09b-103">DVD Navigator Filter</span></span>

<span data-ttu-id="5d09b-104">O filtro de navegador de DVD é o filtro de origem para um DVD-Video grafo de filtro de reprodução.</span><span class="sxs-lookup"><span data-stu-id="5d09b-104">The DVD Navigator filter is the source filter for a DVD-Video playback filter graph.</span></span> <span data-ttu-id="5d09b-105">Ele abre todos os arquivos necessários em um volume DVD-Video, navega pelos arquivos lineares DVD-Video. VOB e analisa o fluxo de programa MPEG-2 resultante, dividindo o fluxo em três (vídeo, áudio, subimagem) Pins de saída.</span><span class="sxs-lookup"><span data-stu-id="5d09b-105">It opens all necessary files in a DVD-Video volume, navigates through the linear DVD-Video .vob files, and parses the resulting MPEG-2 program stream, splitting the stream into three (video, audio, subpicture) output pins.</span></span>

<span data-ttu-id="5d09b-106">O filtro navegador de DVD também implementa as interfaces [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) e [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) que permitem que um aplicativo de reprodução de DVD controle DVD-Video reprodução.</span><span class="sxs-lookup"><span data-stu-id="5d09b-106">The DVD Navigator filter also implements the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) and [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) interfaces that enable a DVD playback application to control DVD-Video playback.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5d09b-107">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="5d09b-107">Filter Interfaces</span></span></td>
<td><span data-ttu-id="5d09b-108"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>IFileSourceFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="5d09b-108"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>IFileSourceFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d09b-109">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="5d09b-109">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="5d09b-110">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</span><span class="sxs-lookup"><span data-stu-id="5d09b-110">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d09b-111">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="5d09b-111">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="5d09b-112">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="5d09b-112">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d09b-113">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="5d09b-113">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="5d09b-114">Tipos de base:</span><span class="sxs-lookup"><span data-stu-id="5d09b-114">Base types:</span></span><br/>
<ul>
<li><span data-ttu-id="5d09b-115">Vídeo: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="5d09b-115">Video: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
<li><span data-ttu-id="5d09b-116">Áudio: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="5d09b-116">Audio: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
<li><span data-ttu-id="5d09b-117">Subimagem: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="5d09b-117">Subpicture: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
</ul>
<span data-ttu-id="5d09b-118">Tipos estendidos:</span><span class="sxs-lookup"><span data-stu-id="5d09b-118">Extended types:</span></span><br/> <span data-ttu-id="5d09b-119">Vídeo:</span><span class="sxs-lookup"><span data-stu-id="5d09b-119">Video:</span></span><br/>
<ul>
<li><span data-ttu-id="5d09b-120"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="5d09b-120"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
<li><span data-ttu-id="5d09b-121"><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="5d09b-121"><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
<li><span data-ttu-id="5d09b-122"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="5d09b-122"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
</ul>
<span data-ttu-id="5d09b-123">Áudio:</span><span class="sxs-lookup"><span data-stu-id="5d09b-123">Audio:</span></span><br/>
<ul>
<li><span data-ttu-id="5d09b-124"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="5d09b-124"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
<li><span data-ttu-id="5d09b-125"><strong>MEDIATYPE_Audio</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="5d09b-125"><strong>MEDIATYPE_Audio</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
<li><span data-ttu-id="5d09b-126"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="5d09b-126"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
</ul>
<span data-ttu-id="5d09b-127">Subimagem</span><span class="sxs-lookup"><span data-stu-id="5d09b-127">Subpicture:</span></span><br/>
<ul>
<li><span data-ttu-id="5d09b-128"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="5d09b-128"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
<li><span data-ttu-id="5d09b-129"><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="5d09b-129"><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
<li><span data-ttu-id="5d09b-130"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="5d09b-130"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
</ul>
<span data-ttu-id="5d09b-131">Para habilitar os tipos estendidos, chame <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>IDvdControl2:: SetOption</strong></a> e defina o</span><span class="sxs-lookup"><span data-stu-id="5d09b-131">To enable the extended types, call <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>IDvdControl2::SetOption</strong></a> and set the</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d09b-132">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="5d09b-132">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="5d09b-133"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d09b-133"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d09b-134">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="5d09b-134">Filter CLSID</span></span></td>
<td><span data-ttu-id="5d09b-135">CLSID_DVDNavigator</span><span class="sxs-lookup"><span data-stu-id="5d09b-135">CLSID_DVDNavigator</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d09b-136">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="5d09b-136">Property Page CLSID</span></span></td>
<td><span data-ttu-id="5d09b-137">Nenhuma página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="5d09b-137">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d09b-138">Executável</span><span class="sxs-lookup"><span data-stu-id="5d09b-138">Executable</span></span></td>
<td><span data-ttu-id="5d09b-139">qdvd.dll</span><span class="sxs-lookup"><span data-stu-id="5d09b-139">qdvd.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d09b-140"><a href="merit.md">Núcleo</a></span><span class="sxs-lookup"><span data-stu-id="5d09b-140"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="5d09b-141">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="5d09b-141">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d09b-142"><a href="filter-categories.md">Categoria do filtro</a></span><span class="sxs-lookup"><span data-stu-id="5d09b-142"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="5d09b-143">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="5d09b-143">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="5d09b-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5d09b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d09b-145">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="5d09b-145">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="5d09b-146">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="5d09b-146">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 




