---
description: Filtro do analisador de vários arquivos
ms.assetid: 8ef06f49-fda4-49e2-9b07-70453a2e897c
title: Filtro do analisador de vários arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44fc83a56bb12c307b85be875a3a2e7e73b744d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105779324"
---
# <a name="multi-file-parser-filter"></a><span data-ttu-id="a2823-103">Filtro do analisador de vários arquivos</span><span class="sxs-lookup"><span data-stu-id="a2823-103">Multi-File Parser Filter</span></span>

<span data-ttu-id="a2823-104">O filtro analisador de vários arquivos analisa um formato de arquivo simples que permite que vários nomes de arquivo sejam especificados como se fossem um arquivo.</span><span class="sxs-lookup"><span data-stu-id="a2823-104">The Multi-File Parser filter parses a simple file format that enables multiple file names to be specified as though they were one file.</span></span> <span data-ttu-id="a2823-105">Esses arquivos têm o formato mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="a2823-105">These files have the format shown in the following example:</span></span>


```C++
;MULTI
https://server/share/video.mpg
https://server/share/captions.smi
```



<span data-ttu-id="a2823-106">O uso desse filtro foi preterido.</span><span class="sxs-lookup"><span data-stu-id="a2823-106">The use of this filter is deprecated.</span></span> <span data-ttu-id="a2823-107">Para renderizar vários arquivos dentro do mesmo grafo de filtro, o aplicativo deve simplesmente chamar **ProcessFile** ou **AddSourceFilter** várias vezes.</span><span class="sxs-lookup"><span data-stu-id="a2823-107">To render multiple files within the same filter graph, the application should simply call **RenderFile** or **AddSourceFilter** multiple times.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a2823-108">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="a2823-108">Filter interfaces</span></span></td>
<td><span data-ttu-id="a2823-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="a2823-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a2823-110">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="a2823-110">Input pin media types</span></span></td>
<td><ul>
<li><span data-ttu-id="a2823-111">Tipo principal: MEDIATYPE_Stream</span><span class="sxs-lookup"><span data-stu-id="a2823-111">Major type: MEDIATYPE_Stream</span></span></li>
<li><span data-ttu-id="a2823-112">Subtipo: CLSID_MultFile</span><span class="sxs-lookup"><span data-stu-id="a2823-112">Subtype: CLSID_MultFile</span></span></li>
<li><span data-ttu-id="a2823-113">Tipo de formato: GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="a2823-113">Format type: GUID_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a2823-114">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="a2823-114">Input pin interfaces</span></span></td>
<td><span data-ttu-id="a2823-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="a2823-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a2823-116">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="a2823-116">Output pin media types</span></span></td>
<td><ul>
<li><span data-ttu-id="a2823-117">Tipo principal: MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="a2823-117">Major type: MEDIATYPE_File</span></span></li>
<li><span data-ttu-id="a2823-118">Subtipo: GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="a2823-118">Subtype: GUID_NULL</span></span></li>
<li><span data-ttu-id="a2823-119">Tipo de formato: MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="a2823-119">Format type: MEDIATYPE_File</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a2823-120">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="a2823-120">Output pin interfaces</span></span></td>
<td><span data-ttu-id="a2823-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="a2823-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a2823-122">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="a2823-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="a2823-123">CLSID_MultFile</span><span class="sxs-lookup"><span data-stu-id="a2823-123">CLSID_MultFile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a2823-124">Executável</span><span class="sxs-lookup"><span data-stu-id="a2823-124">Executable</span></span></td>
<td><span data-ttu-id="a2823-125">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="a2823-125">Quartz.dll</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a2823-126"><a href="merit.md">Núcleo</a></span><span class="sxs-lookup"><span data-stu-id="a2823-126"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="a2823-127">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="a2823-127">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a2823-128"><a href="filter-categories.md">Categoria do filtro</a></span><span class="sxs-lookup"><span data-stu-id="a2823-128"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="a2823-129">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="a2823-129">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="a2823-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2823-130">Remarks</span></span>

<span data-ttu-id="a2823-131">O filtro cria um PIN de saída para cada arquivo listado no arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="a2823-131">The filter creates one output pin for each file listed in the source file.</span></span> <span data-ttu-id="a2823-132">O tipo de saída é \_ arquivo de MediaType e o bloco de formato para o tipo de saída é uma cadeia de caracteres largos que contém o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="a2823-132">The output type is MEDIATYPE\_File, and the format block for the output type is a wide-character string that contains the file name.</span></span> <span data-ttu-id="a2823-133">Cada PIN se conecta a uma instância do filtro de [renderizador de fluxo de arquivo](file-stream-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="a2823-133">Each pin connects to an instance of the [File Stream Renderer](file-stream-renderer-filter.md) filter.</span></span> <span data-ttu-id="a2823-134">O filtro de renderizador de fluxo de arquivo cria um PIN de saída, que expõe a interface [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) .</span><span class="sxs-lookup"><span data-stu-id="a2823-134">The File Stream Renderer filter creates one output pin, which exposes the [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) interface.</span></span> <span data-ttu-id="a2823-135">O PIN de saída renderiza o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="a2823-135">The output pin renders the specified file.</span></span> <span data-ttu-id="a2823-136">Nenhum dado de mídia é transmitido entre o analisador de vários arquivos e o renderizador de fluxo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="a2823-136">No media data travels between the Multi-File Parser and the File Stream Renderer.</span></span>

<span data-ttu-id="a2823-137">O CLSID do filtro não está definido em UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="a2823-137">The filter's CLSID is not defined in Uuids.h.</span></span> <span data-ttu-id="a2823-138">Use esta macro em seu próprio arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a2823-138">Use this macro in your own header file:</span></span>


```C++
// {D51BD5A3-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_MultFile,
0xd51bd5a3, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a><span data-ttu-id="a2823-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a2823-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2823-140">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="a2823-140">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



