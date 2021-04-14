---
description: Filtro de processador de comandos de script interno
ms.assetid: 264cc7c3-987c-4832-85a2-087278a4d024
title: Filtro de processador de comandos de script interno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b241643d991e9348015dc51ea5b2f1c4875f079d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500436"
---
# <a name="internal-script-command-renderer-filter"></a><span data-ttu-id="450f6-103">Filtro de processador de comandos de script interno</span><span class="sxs-lookup"><span data-stu-id="450f6-103">Internal Script Command Renderer Filter</span></span>

<span data-ttu-id="450f6-104">Recebe comandos de script e os envia para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="450f6-104">Receives script commands and dispatches them to the application.</span></span>

<span data-ttu-id="450f6-105">Esse filtro aceita comandos de script em um dos dois formatos:</span><span class="sxs-lookup"><span data-stu-id="450f6-105">This filter accepts script commands in one of two formats:</span></span>

-   <span data-ttu-id="450f6-106">Texto de MEDIATYPE \_ : cada amostra de mídia contém uma cadeia de caracteres de texto ANSI.</span><span class="sxs-lookup"><span data-stu-id="450f6-106">MEDIATYPE\_Text: Each media sample contains an ANSI text string.</span></span>
-   <span data-ttu-id="450f6-107">MEDIATYPE \_ ScriptCommand: cada amostra de mídia contém duas cadeias de caracteres Unicode terminadas em nulo, concatenadas juntas.</span><span class="sxs-lookup"><span data-stu-id="450f6-107">MEDIATYPE\_ScriptCommand: Each media sample contains two NULL-terminated Unicode strings, concatenated together.</span></span> <span data-ttu-id="450f6-108">A primeira cadeia de caracteres descreve o tipo de comando e a segunda cadeia de caracteres é o comando de script.</span><span class="sxs-lookup"><span data-stu-id="450f6-108">The first string describes the command type and the second string is the script command.</span></span>

    <span data-ttu-id="450f6-109">Quando o filtro recebe um exemplo, ele envia uma notificação de evento de [**\_ \_ evento OLE do EC**](ec-ole-event.md) .</span><span class="sxs-lookup"><span data-stu-id="450f6-109">When the filter receives a sample, it sends an [**EC\_OLE\_EVENT**](ec-ole-event.md) event notification.</span></span> <span data-ttu-id="450f6-110">O primeiro parâmetro de evento é um **BSTR** com o tipo de comando, ou `Text` se o formato for texto de MediaType \_ .</span><span class="sxs-lookup"><span data-stu-id="450f6-110">The first event parameter is a **BSTR** with the command type, or `Text` if the format is MEDIATYPE\_Text.</span></span> <span data-ttu-id="450f6-111">O segundo parâmetro de evento é um **BSTR** com o comando de script.</span><span class="sxs-lookup"><span data-stu-id="450f6-111">The second event parameter is a **BSTR** with the script command.</span></span> <span data-ttu-id="450f6-112">O aplicativo pode recuperar o evento e responder ao comando de script.</span><span class="sxs-lookup"><span data-stu-id="450f6-112">The application can retrieve the event and respond to the script command.</span></span>

<span data-ttu-id="450f6-113">Para obter um exemplo de como usar esse filtro, consulte [Sami (CC) Parser](sami--cc--parser-filter.md).</span><span class="sxs-lookup"><span data-stu-id="450f6-113">For an example of how to use this filter, see [SAMI (CC) Parser](sami--cc--parser-filter.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="450f6-114">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="450f6-114">Filter Interfaces</span></span></td>
<td><span data-ttu-id="450f6-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="450f6-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="450f6-116">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="450f6-116">Input Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="450f6-117">MEDIATYPE_ScriptCommand, MEDIASUBTYPE_NULL</span><span class="sxs-lookup"><span data-stu-id="450f6-117">MEDIATYPE_ScriptCommand, MEDIASUBTYPE_NULL</span></span></li>
<li><span data-ttu-id="450f6-118">MEDIATYPE_Text, MEDIASUBTYPE_NULL</span><span class="sxs-lookup"><span data-stu-id="450f6-118">MEDIATYPE_Text, MEDIASUBTYPE_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="450f6-119">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="450f6-119">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="450f6-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="450f6-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="450f6-121">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="450f6-121">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="450f6-122">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="450f6-122">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="450f6-123">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="450f6-123">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="450f6-124">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="450f6-124">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="450f6-125">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="450f6-125">Filter CLSID</span></span></td>
<td><span data-ttu-id="450f6-126">{48025243-2D39-11CE-875D-00608CB78066}</span><span class="sxs-lookup"><span data-stu-id="450f6-126">{48025243-2D39-11CE-875D-00608CB78066}</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="450f6-127">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="450f6-127">Property Page CLSID</span></span></td>
<td><span data-ttu-id="450f6-128">Nenhuma página de propriedades</span><span class="sxs-lookup"><span data-stu-id="450f6-128">No property page</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="450f6-129">Executável</span><span class="sxs-lookup"><span data-stu-id="450f6-129">Executable</span></span></td>
<td><span data-ttu-id="450f6-130">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="450f6-130">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="450f6-131"><a href="merit.md">Núcleo</a></span><span class="sxs-lookup"><span data-stu-id="450f6-131"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="450f6-132">MERIT_PREFERRED + 1</span><span class="sxs-lookup"><span data-stu-id="450f6-132">MERIT_PREFERRED + 1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="450f6-133"><a href="filter-categories.md">Categoria do filtro</a></span><span class="sxs-lookup"><span data-stu-id="450f6-133"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="450f6-134">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="450f6-134">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="450f6-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="450f6-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="450f6-136">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="450f6-136">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



