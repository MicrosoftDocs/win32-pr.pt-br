---
description: Filtro de decodificador de linha 21
ms.assetid: 48fa5484-1f8c-4133-b2e1-888cb1834402
title: Filtro de decodificador de linha 21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839a6ff8e77f4815b74f5de65b8f0e2a565cdc2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105775556"
---
# <a name="line-21-decoder-filter"></a><span data-ttu-id="048dd-103">Filtro de decodificador de linha 21</span><span class="sxs-lookup"><span data-stu-id="048dd-103">Line 21 Decoder Filter</span></span>

<span data-ttu-id="048dd-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="048dd-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="048dd-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="048dd-105">It may be altered or unavailable in subsequent versions.</span></span>

<span data-ttu-id="048dd-106">Este filtro de decodificador de linha 21 decodifica os dados da linha 21 e desenha o texto da legenda em bitmaps.</span><span class="sxs-lookup"><span data-stu-id="048dd-106">This Line 21 Decoder filter decodes line 21 data and draws the caption text onto bitmaps.</span></span>

<span data-ttu-id="048dd-107">O pino de entrada conecta-se a qualquer linha de 21 provedor de dados, normalmente um decodificador de vídeo DVD ou o filtro de [decodificador de CC](cc-decoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="048dd-107">The input pin connects to any line 21 data provider, typically either a DVD video decoder or the [CC Decoder](cc-decoder-filter.md) filter.</span></span> <span data-ttu-id="048dd-108">O decodificador de CC fornece dados de linha 21 do VBI de um sinal de televisão analógica.</span><span class="sxs-lookup"><span data-stu-id="048dd-108">The CC Decoder provides line 21 data from the VBI of an analog television signal.</span></span> <span data-ttu-id="048dd-109">O pino de saída se conecta a um pin secundário no [mixer de sobreposição](overlay-mixer-filter.md) ou a outro processador de vídeo, como o VMR.</span><span class="sxs-lookup"><span data-stu-id="048dd-109">The output pin connects to a secondary pin on the [Overlay Mixer](overlay-mixer-filter.md) or to another video renderer, such as the VMR.</span></span>

<span data-ttu-id="048dd-110">Esse filtro aceita dados de linha 21 no formato de par de bytes padrão ou, para DVD, como um pacote para todo o grupo de imagens (GOP).</span><span class="sxs-lookup"><span data-stu-id="048dd-110">This filter accepts line 21 data in the standard byte-pair format or, for DVD, as a packet for the whole group of pictures (GOP).</span></span> <span data-ttu-id="048dd-111">Para cada GOP no fluxo de vídeo do DVD, pode haver um pacote de dados do usuário que tenha as informações de cabeçalho de GOP específicas e os dados da linha 21.</span><span class="sxs-lookup"><span data-stu-id="048dd-111">For every GOP in the DVD video stream, there can be a user data packet that has that particular GOP's header information and line 21 data.</span></span> <span data-ttu-id="048dd-112">O formato dos pares de bytes é definido no padrão EIA/CEA-608-B; Veja esse padrão para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="048dd-112">The format of the byte pairs is defined in the EIA/CEA-608-B standard; please refer to that standard for more information.</span></span>

<span data-ttu-id="048dd-113">Duas versões deste filtro estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="048dd-113">Two versions of this filter are available:</span></span>



| <span data-ttu-id="048dd-114">Filtrar</span><span class="sxs-lookup"><span data-stu-id="048dd-114">Filter</span></span>            | <span data-ttu-id="048dd-115">CLSID</span><span class="sxs-lookup"><span data-stu-id="048dd-115">CLSID</span></span>                 |
|-------------------|-----------------------|
| <span data-ttu-id="048dd-116">Decodificador de linha 21</span><span class="sxs-lookup"><span data-stu-id="048dd-116">Line 21 Decoder</span></span>   | <span data-ttu-id="048dd-117">\_LINE21DECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="048dd-117">CLSID\_Line21Decoder</span></span>  |
| <span data-ttu-id="048dd-118">Linha 21 Decoder 2</span><span class="sxs-lookup"><span data-stu-id="048dd-118">Line 21 Decoder 2</span></span> | <span data-ttu-id="048dd-119">\_LINE21DECODER2 CLSID</span><span class="sxs-lookup"><span data-stu-id="048dd-119">CLSID\_Line21Decoder2</span></span> |



 

<span data-ttu-id="048dd-120">O filtro da versão 1 é usado nas plataformas Microsoft® Windows® 95/98/me e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="048dd-120">The version 1 filter is used on Microsoft® Windows® 95/98/Me and Windows 2000 platforms.</span></span> <span data-ttu-id="048dd-121">O filtro versão 2 está disponível no Microsoft Windows XP e versões posteriores e é usado sempre que o processador de mixagem de vídeo estiver no grafo.</span><span class="sxs-lookup"><span data-stu-id="048dd-121">The version 2 filter is available in Microsoft Windows XP and later, and is used whenever the Video Mixing Renderer is in the graph.</span></span>

<span data-ttu-id="048dd-122">As informações na tabela a seguir se aplicam a ambas as versões do filtro:</span><span class="sxs-lookup"><span data-stu-id="048dd-122">The information in the following table applies to both versions of the filter:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="048dd-123">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="048dd-123">Filter Interfaces</span></span></td>
<td><span data-ttu-id="048dd-124"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="048dd-124"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="048dd-125">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="048dd-125">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="048dd-126">Tipo principal: MEDIATYPE_AUXLine21DataSubtype:</span><span class="sxs-lookup"><span data-stu-id="048dd-126">Major Type: MEDIATYPE_AUXLine21DataSubtype:</span></span><br/>
<ul>
<li><span data-ttu-id="048dd-127">MEDIASUBTYPE_Line21_BytePair (linha padrão 21)</span><span class="sxs-lookup"><span data-stu-id="048dd-127">MEDIASUBTYPE_Line21_BytePair (standard line 21)</span></span></li>
<li><span data-ttu-id="048dd-128">MEDIASUBTYPE_Line21_GOPPacket (linha de DVD 21)</span><span class="sxs-lookup"><span data-stu-id="048dd-128">MEDIASUBTYPE_Line21_GOPPacket (DVD line 21)</span></span></li>
</ul>
<span data-ttu-id="048dd-129">Tipo de formato: FORMAT_VideoInfo ou GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="048dd-129">Format Type: FORMAT_VideoInfo or GUID_NULL</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="048dd-130">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="048dd-130">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="048dd-131"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="048dd-131"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="048dd-132">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="048dd-132">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="048dd-133">Tipo principal: MEDIATYPE_VideoSubtype:</span><span class="sxs-lookup"><span data-stu-id="048dd-133">Major type: MEDIATYPE_VideoSubtype:</span></span><br/>
<ul>
<li><span data-ttu-id="048dd-134">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="048dd-134">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="048dd-135">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="048dd-135">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="048dd-136">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="048dd-136">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="048dd-137">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="048dd-137">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="048dd-138">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="048dd-138">MEDIASUBTYPE_RGB32</span></span></li>
</ul>
<span data-ttu-id="048dd-139">Tipo de formato: FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="048dd-139">Format Type: FORMAT_VideoInfo</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="048dd-140">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="048dd-140">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="048dd-141"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="048dd-141"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="048dd-142">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="048dd-142">Filter CLSID</span></span></td>
<td><span data-ttu-id="048dd-143">Consulte a tabela anterior</span><span class="sxs-lookup"><span data-stu-id="048dd-143">See previous table</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="048dd-144">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="048dd-144">Property Page CLSID</span></span></td>
<td><span data-ttu-id="048dd-145">Nenhum</span><span class="sxs-lookup"><span data-stu-id="048dd-145">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="048dd-146">Executável</span><span class="sxs-lookup"><span data-stu-id="048dd-146">Executable</span></span></td>
<td><span data-ttu-id="048dd-147">qdvd.dll</span><span class="sxs-lookup"><span data-stu-id="048dd-147">qdvd.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="048dd-148"><a href="merit.md">Núcleo</a></span><span class="sxs-lookup"><span data-stu-id="048dd-148"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="048dd-149">Decodificador de linha 21: MERIT_NORMALLine 21 Decoder 2: MERIT_NORMAL + 2</span><span class="sxs-lookup"><span data-stu-id="048dd-149">Line 21 Decoder: MERIT_NORMALLine 21 Decoder 2: MERIT_NORMAL + 2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="048dd-150"><a href="filter-categories.md">Categoria do filtro</a></span><span class="sxs-lookup"><span data-stu-id="048dd-150"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="048dd-151">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="048dd-151">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="048dd-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="048dd-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="048dd-153">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="048dd-153">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="048dd-154">Legendas e teletextos codificados</span><span class="sxs-lookup"><span data-stu-id="048dd-154">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)
</dt> <dt>

[<span data-ttu-id="048dd-155">Configuração de grafo de filtro de DVD</span><span class="sxs-lookup"><span data-stu-id="048dd-155">DVD Filter Graph Configuration</span></span>](dvd-filter-graph-configuration.md)
</dt> </dl>

 

 




