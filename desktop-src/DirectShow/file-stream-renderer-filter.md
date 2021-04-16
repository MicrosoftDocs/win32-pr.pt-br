---
description: Filtro de renderizador de fluxo de arquivo
ms.assetid: e26462bb-e67f-4522-bec2-88378c4ff442
title: Filtro de renderizador de fluxo de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64c8d8a0c87dab3aa811c8246be24ded8ee04dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500616"
---
# <a name="file-stream-renderer-filter"></a><span data-ttu-id="52b56-103">Filtro de renderizador de fluxo de arquivo</span><span class="sxs-lookup"><span data-stu-id="52b56-103">File Stream Renderer Filter</span></span>

<span data-ttu-id="52b56-104">O filtro de renderizador de fluxo de arquivo processa nomes de arquivo analisados pelo filtro [analisador de vários arquivos](multi-file-parser-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="52b56-104">The File Stream Renderer filter renders file names that are parsed by the [Multi-File Parser](multi-file-parser-filter.md) filter.</span></span> <span data-ttu-id="52b56-105">Para obter mais informações, consulte a documentação para esse filtro.</span><span class="sxs-lookup"><span data-stu-id="52b56-105">For more information, see the documentation for that filter.</span></span>

<span data-ttu-id="52b56-106">O uso desse filtro foi preterido.</span><span class="sxs-lookup"><span data-stu-id="52b56-106">The use of this filter is deprecated.</span></span> <span data-ttu-id="52b56-107">Para renderizar vários arquivos dentro do mesmo grafo de filtro, o aplicativo deve simplesmente chamar **ProcessFile** ou **AddSourceFilter** várias vezes.</span><span class="sxs-lookup"><span data-stu-id="52b56-107">To render multiple files within the same filter graph, the application should simply call **RenderFile** or **AddSourceFilter** multiple times.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="52b56-108">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="52b56-108">Filter interfaces</span></span></td>
<td><span data-ttu-id="52b56-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="52b56-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52b56-110">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="52b56-110">Input pin media types</span></span></td>
<td><ul>
<li><span data-ttu-id="52b56-111">Tipo principal: MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="52b56-111">Major type: MEDIATYPE_File</span></span></li>
<li><span data-ttu-id="52b56-112">Subtipo: GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="52b56-112">Subtype: GUID_NULL</span></span></li>
<li><span data-ttu-id="52b56-113">Tipo de formato: MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="52b56-113">Format type: MEDIATYPE_File</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52b56-114">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="52b56-114">Input pin interfaces</span></span></td>
<td><span data-ttu-id="52b56-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="52b56-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52b56-116">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="52b56-116">Output pin media types</span></span></td>
<td><span data-ttu-id="52b56-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="52b56-117">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52b56-118">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="52b56-118">Output pin interfaces</span></span></td>
<td><span data-ttu-id="52b56-119"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a></span><span class="sxs-lookup"><span data-stu-id="52b56-119"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52b56-120">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="52b56-120">Filter CLSID</span></span></td>
<td><span data-ttu-id="52b56-121">CLSID_FileRend</span><span class="sxs-lookup"><span data-stu-id="52b56-121">CLSID_FileRend</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52b56-122">Executável</span><span class="sxs-lookup"><span data-stu-id="52b56-122">Executable</span></span></td>
<td><span data-ttu-id="52b56-123">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="52b56-123">Quartz.dll</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52b56-124"><a href="merit.md">Núcleo</a></span><span class="sxs-lookup"><span data-stu-id="52b56-124"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="52b56-125">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="52b56-125">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52b56-126"><a href="filter-categories.md">Categoria do filtro</a></span><span class="sxs-lookup"><span data-stu-id="52b56-126"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="52b56-127">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="52b56-127">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="52b56-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="52b56-128">Remarks</span></span>

<span data-ttu-id="52b56-129">O CLSID do filtro não está definido em UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="52b56-129">The filter's CLSID is not defined in Uuids.h.</span></span> <span data-ttu-id="52b56-130">Use esta macro em seu próprio arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="52b56-130">Use this macro in your own header file:</span></span>


```C++
// {D51BD5A5-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_FileRend,
0xd51bd5A5, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a><span data-ttu-id="52b56-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="52b56-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52b56-132">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="52b56-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



