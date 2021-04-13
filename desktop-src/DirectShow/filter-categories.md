---
description: As tabelas a seguir listam os CLSIDs para as categorias de filtro do DirectShow.
ms.assetid: cab4e2c9-eab9-4836-adfc-870490ca5b6b
title: Filtrar categorias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c4ccb9443c405abcbd0b9afbd406d6faf2558a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370071"
---
# <a name="filter-categories"></a><span data-ttu-id="623ad-103">Filtrar categorias</span><span class="sxs-lookup"><span data-stu-id="623ad-103">Filter Categories</span></span>

<span data-ttu-id="623ad-104">As tabelas a seguir listam os CLSIDs para as categorias de filtro do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="623ad-104">The following tables list the CLSIDs for the DirectShow filter categories.</span></span>

-   [<span data-ttu-id="623ad-105">Categorias de filtro do DirectShow</span><span class="sxs-lookup"><span data-stu-id="623ad-105">DirectShow Filter Categories</span></span>](#directshow-filter-categories)
-   [<span data-ttu-id="623ad-106">Outras categorias de filtro</span><span class="sxs-lookup"><span data-stu-id="623ad-106">Other Filter Categories</span></span>](#other-filter-categories)
-   [<span data-ttu-id="623ad-107">Metacategoria de filtro do DirectShow</span><span class="sxs-lookup"><span data-stu-id="623ad-107">DirectShow Filter Meta-Category</span></span>](#directshow-filter-meta-category)
-   [<span data-ttu-id="623ad-108">Categorias de DMO</span><span class="sxs-lookup"><span data-stu-id="623ad-108">DMO Categories</span></span>](#dmo-categories)
-   [<span data-ttu-id="623ad-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="623ad-109">Related topics</span></span>](#related-topics)

## <a name="directshow-filter-categories"></a><span data-ttu-id="623ad-110">Categorias de filtro do DirectShow</span><span class="sxs-lookup"><span data-stu-id="623ad-110">DirectShow Filter Categories</span></span>

<span data-ttu-id="623ad-111">As categorias listadas aqui são enumeradas pelo [mapeador de filtro](filter-mapper.md).</span><span class="sxs-lookup"><span data-stu-id="623ad-111">The categories listed here are enumerated by the [Filter Mapper](filter-mapper.md).</span></span> <span data-ttu-id="623ad-112">Por padrão, no entanto, o mapeador de filtro ignora as categorias com méritos de mérito \_ \_ não \_ usam ou menos.</span><span class="sxs-lookup"><span data-stu-id="623ad-112">By default, however, the Filter Mapper ignores categories with merits of MERIT\_DO\_NOT\_USE or less.</span></span> <span data-ttu-id="623ad-113">Para obter mais informações, consulte [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters).</span><span class="sxs-lookup"><span data-stu-id="623ad-113">For more information, see [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters).</span></span> <span data-ttu-id="623ad-114">Todas as categorias listadas aqui também podem ser enumeradas com o [enumerador de dispositivo do sistema](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="623ad-114">All of the categories listed here can also be enumerated with the [System Device Enumerator](system-device-enumerator.md).</span></span>

<span data-ttu-id="623ad-115">As categorias a seguir são declaradas em UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="623ad-115">The following categories are declared in Uuids.h.</span></span> <span data-ttu-id="623ad-116">Inclua o arquivo de cabeçalho DShow. h.</span><span class="sxs-lookup"><span data-stu-id="623ad-116">Include the header file Dshow.h.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="623ad-117">Nome amigável</span><span class="sxs-lookup"><span data-stu-id="623ad-117">Friendly Name</span></span></th>
<th><span data-ttu-id="623ad-118">CLSID</span><span class="sxs-lookup"><span data-stu-id="623ad-118">CLSID</span></span></th>
<th><span data-ttu-id="623ad-119">Núcleo</span><span class="sxs-lookup"><span data-stu-id="623ad-119">Merit</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="623ad-120">Fontes de captura de áudio</span><span class="sxs-lookup"><span data-stu-id="623ad-120">Audio Capture Sources</span></span></td>
<td><span data-ttu-id="623ad-121"><strong>CLSID_AudioInputDeviceCategory</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-121"><strong>CLSID_AudioInputDeviceCategory</strong></span></span></td>
<td><span data-ttu-id="623ad-122"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-122"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="623ad-123">Compactadores de áudio</span><span class="sxs-lookup"><span data-stu-id="623ad-123">Audio Compressors</span></span></td>
<td><span data-ttu-id="623ad-124"><strong>CLSID_AudioCompressorCategory</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-124"><strong>CLSID_AudioCompressorCategory</strong></span></span></td>
<td><span data-ttu-id="623ad-125"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-125"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="623ad-126">Renderizadores de áudio</span><span class="sxs-lookup"><span data-stu-id="623ad-126">Audio Renderers</span></span></td>
<td><span data-ttu-id="623ad-127"><strong>CLSID_AudioRendererCategory</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-127"><strong>CLSID_AudioRendererCategory</strong></span></span></td>
<td><span data-ttu-id="623ad-128"><strong>MERIT_NORMAL</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-128"><strong>MERIT_NORMAL</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="623ad-129">Filtros de controle de dispositivo</span><span class="sxs-lookup"><span data-stu-id="623ad-129">Device Control Filters</span></span></td>
<td><span data-ttu-id="623ad-130"><strong>CLSID_DeviceControlCategory</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-130"><strong>CLSID_DeviceControlCategory</strong></span></span></td>
<td><span data-ttu-id="623ad-131"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-131"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="623ad-132">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="623ad-132">DirectShow Filters</span></span></td>
<td><span data-ttu-id="623ad-133"><strong>CLSID_LegacyAmFilterCategory</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-133"><strong>CLSID_LegacyAmFilterCategory</strong></span></span></td>
<td><span data-ttu-id="623ad-134"><strong>MERIT_NORMAL</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-134"><strong>MERIT_NORMAL</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="623ad-135">Renderizadores externos</span><span class="sxs-lookup"><span data-stu-id="623ad-135">External Renderers</span></span></td>
<td><span data-ttu-id="623ad-136"><strong>CLSID_TransmitCategory</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-136"><strong>CLSID_TransmitCategory</strong></span></span></td>
<td><span data-ttu-id="623ad-137"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-137"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="623ad-138">Renderizadores Midi</span><span class="sxs-lookup"><span data-stu-id="623ad-138">Midi Renderers</span></span></td>
<td><span data-ttu-id="623ad-139"><strong>CLSID_MidiRendererCategory</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-139"><strong>CLSID_MidiRendererCategory</strong></span></span></td>
<td><span data-ttu-id="623ad-140"><strong>MERIT_NORMAL</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-140"><strong>MERIT_NORMAL</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="623ad-141">Fontes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="623ad-141">Video Capture Sources</span></span></td>
<td><span data-ttu-id="623ad-142"><strong>CLSID_VideoInputDeviceCategory</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-142"><strong>CLSID_VideoInputDeviceCategory</strong></span></span></td>
<td><span data-ttu-id="623ad-143"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-143"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="623ad-144">Compactadores de vídeo</span><span class="sxs-lookup"><span data-stu-id="623ad-144">Video Compressors</span></span></td>
<td><span data-ttu-id="623ad-145"><strong>CLSID_VideoCompressorCategory</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-145"><strong>CLSID_VideoCompressorCategory</strong></span></span></td>
<td><span data-ttu-id="623ad-146"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-146"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="623ad-147">Dispositivos de descompactação de fluxo WDM</span><span class="sxs-lookup"><span data-stu-id="623ad-147">WDM Stream Decompression Devices</span></span></td>
<td><span data-ttu-id="623ad-148"><strong>CLSID_DVDHWDecodersCategory</strong>
</span><span class="sxs-lookup"><span data-stu-id="623ad-148"><strong>CLSID_DVDHWDecodersCategory</strong>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="623ad-149">Esta categoria contém decodificadores de DVD de hardware.</span><span class="sxs-lookup"><span data-stu-id="623ad-149">This category contains hardware DVD decoders.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="623ad-150"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-150"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="623ad-151">Dispositivos de captura de fluxo WDM</span><span class="sxs-lookup"><span data-stu-id="623ad-151">WDM Streaming Capture Devices</span></span></td>
<td><span data-ttu-id="623ad-152"><strong>AM_KSCATEGORY_CAPTURE</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-152"><strong>AM_KSCATEGORY_CAPTURE</strong></span></span></td>
<td><span data-ttu-id="623ad-153"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-153"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="623ad-154">Dispositivos Crossbar de streaming WDM</span><span class="sxs-lookup"><span data-stu-id="623ad-154">WDM Streaming Crossbar Devices</span></span></td>
<td><span data-ttu-id="623ad-155"><strong>AM_KSCATEGORY_CROSSBAR</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-155"><strong>AM_KSCATEGORY_CROSSBAR</strong></span></span></td>
<td><span data-ttu-id="623ad-156"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-156"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="623ad-157">Dispositivos de renderização de streaming WDM</span><span class="sxs-lookup"><span data-stu-id="623ad-157">WDM Streaming Rendering Devices</span></span></td>
<td><span data-ttu-id="623ad-158"><strong>AM_KSCATEGORY_RENDER</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-158"><strong>AM_KSCATEGORY_RENDER</strong></span></span></td>
<td><span data-ttu-id="623ad-159"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-159"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="623ad-160">Dispositivos de divisão/divisor de streaming WDM</span><span class="sxs-lookup"><span data-stu-id="623ad-160">WDM Streaming Tee/Splitter Devices</span></span></td>
<td><span data-ttu-id="623ad-161"><strong>AM_KSCATEGORY_SPLITTER</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-161"><strong>AM_KSCATEGORY_SPLITTER</strong></span></span></td>
<td><span data-ttu-id="623ad-162"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-162"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="623ad-163">Dispositivos de áudio de TV de streaming WDM</span><span class="sxs-lookup"><span data-stu-id="623ad-163">WDM Streaming TV Audio Devices</span></span></td>
<td><span data-ttu-id="623ad-164"><strong>AM_KSCATEGORY_TVAUDIO</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-164"><strong>AM_KSCATEGORY_TVAUDIO</strong></span></span></td>
<td><span data-ttu-id="623ad-165"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-165"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="623ad-166">Dispositivos de sintonização de TV de streaming WDM</span><span class="sxs-lookup"><span data-stu-id="623ad-166">WDM Streaming TV Tuner Devices</span></span></td>
<td><span data-ttu-id="623ad-167"><strong>AM_KSCATEGORY_TVTUNER</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-167"><strong>AM_KSCATEGORY_TVTUNER</strong></span></span></td>
<td><span data-ttu-id="623ad-168"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-168"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="623ad-169">Codecs VBI de streaming WDM</span><span class="sxs-lookup"><span data-stu-id="623ad-169">WDM Streaming VBI Codecs</span></span></td>
<td><span data-ttu-id="623ad-170"><strong>AM_KSCATEGORY_VBICODEC</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-170"><strong>AM_KSCATEGORY_VBICODEC</strong></span></span></td>
<td><span data-ttu-id="623ad-171"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="623ad-171"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="623ad-172">As categorias a seguir são declaradas no arquivo de cabeçalho KS. h.</span><span class="sxs-lookup"><span data-stu-id="623ad-172">The following categories are declared in the header file Ks.h.</span></span>



| <span data-ttu-id="623ad-173">Nome amigável</span><span class="sxs-lookup"><span data-stu-id="623ad-173">Friendly Name</span></span>                          | <span data-ttu-id="623ad-174">CLSID</span><span class="sxs-lookup"><span data-stu-id="623ad-174">CLSID</span></span>                                   | <span data-ttu-id="623ad-175">Núcleo</span><span class="sxs-lookup"><span data-stu-id="623ad-175">Merit</span></span>                   |
|----------------------------------------|-----------------------------------------|-------------------------|
| <span data-ttu-id="623ad-176">Transformações de comunicação de streaming WDM</span><span class="sxs-lookup"><span data-stu-id="623ad-176">WDM Streaming Communication Transforms</span></span> | <span data-ttu-id="623ad-177">**KSCATEGORY \_ COMMUNICATIONSTRANSFORM**</span><span class="sxs-lookup"><span data-stu-id="623ad-177">**KSCATEGORY\_COMMUNICATIONSTRANSFORM**</span></span> | <span data-ttu-id="623ad-178">**MÉRITO \_ \_ não \_ use**</span><span class="sxs-lookup"><span data-stu-id="623ad-178">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="623ad-179">Transformações de dados de streaming WDM</span><span class="sxs-lookup"><span data-stu-id="623ad-179">WDM Streaming Data Transforms</span></span>          | <span data-ttu-id="623ad-180">**KSCATEGORY \_ DATAtransform**</span><span class="sxs-lookup"><span data-stu-id="623ad-180">**KSCATEGORY\_DATATRANSFORM**</span></span>           | <span data-ttu-id="623ad-181">**MÉRITO \_ \_ não \_ use**</span><span class="sxs-lookup"><span data-stu-id="623ad-181">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="623ad-182">Transformações de interface de streaming WDM</span><span class="sxs-lookup"><span data-stu-id="623ad-182">WDM Streaming Interface Transforms</span></span>     | <span data-ttu-id="623ad-183">**KSCATEGORY \_ INTERFACETRANSFORM**</span><span class="sxs-lookup"><span data-stu-id="623ad-183">**KSCATEGORY\_INTERFACETRANSFORM**</span></span>      | <span data-ttu-id="623ad-184">**MÉRITO \_ \_ não \_ use**</span><span class="sxs-lookup"><span data-stu-id="623ad-184">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="623ad-185">Dispositivos de mixer de streaming WDM</span><span class="sxs-lookup"><span data-stu-id="623ad-185">WDM Streaming Mixer Devices</span></span>            | <span data-ttu-id="623ad-186">**MIXER de KSCATEGORY \_**</span><span class="sxs-lookup"><span data-stu-id="623ad-186">**KSCATEGORY\_MIXER**</span></span>                   | <span data-ttu-id="623ad-187">**MÉRITO \_ \_ não \_ use**</span><span class="sxs-lookup"><span data-stu-id="623ad-187">**MERIT\_DO\_NOT\_USE**</span></span> |



 

<span data-ttu-id="623ad-188">As categorias a seguir são declaradas no arquivo de cabeçalho Bdamedia. h.</span><span class="sxs-lookup"><span data-stu-id="623ad-188">The following categories are declared in the header file Bdamedia.h.</span></span> <span data-ttu-id="623ad-189">Inclua os seguintes arquivos de cabeçalho: KS. h, ksmedia. h e bdamedia. h.</span><span class="sxs-lookup"><span data-stu-id="623ad-189">Include the following header files: ks.h, ksmedia.h, and bdamedia.h.</span></span>



| <span data-ttu-id="623ad-190">Nome amigável</span><span class="sxs-lookup"><span data-stu-id="623ad-190">Friendly Name</span></span>                       | <span data-ttu-id="623ad-191">CLSID</span><span class="sxs-lookup"><span data-stu-id="623ad-191">CLSID</span></span>                                       | <span data-ttu-id="623ad-192">Núcleo</span><span class="sxs-lookup"><span data-stu-id="623ad-192">Merit</span></span>                   |
|-------------------------------------|---------------------------------------------|-------------------------|
| <span data-ttu-id="623ad-193">Provedores de rede BDA</span><span class="sxs-lookup"><span data-stu-id="623ad-193">BDA Network Providers</span></span>               | <span data-ttu-id="623ad-194">**\_provedor de \_ rede \_ BDA KSCATEGORY**</span><span class="sxs-lookup"><span data-stu-id="623ad-194">**KSCATEGORY\_BDA\_NETWORK\_PROVIDER**</span></span>      | <span data-ttu-id="623ad-195">**MÉRITO \_ normal**</span><span class="sxs-lookup"><span data-stu-id="623ad-195">**MERIT\_NORMAL**</span></span>       |
| <span data-ttu-id="623ad-196">Componentes do receptor BDA</span><span class="sxs-lookup"><span data-stu-id="623ad-196">BDA Receiver Components</span></span>             | <span data-ttu-id="623ad-197">**\_ \_ componente receptor do KSCATEGORY BDA \_**</span><span class="sxs-lookup"><span data-stu-id="623ad-197">**KSCATEGORY\_BDA\_RECEIVER\_COMPONENT**</span></span>    | <span data-ttu-id="623ad-198">**MÉRITO \_ \_ não \_ use**</span><span class="sxs-lookup"><span data-stu-id="623ad-198">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="623ad-199">Filtros de renderização BDA</span><span class="sxs-lookup"><span data-stu-id="623ad-199">BDA Rendering Filters</span></span>               | <span data-ttu-id="623ad-200">**\_coletor de IP KSCATEGORY \_**</span><span class="sxs-lookup"><span data-stu-id="623ad-200">**KSCATEGORY\_IP\_SINK**</span></span>                    | <span data-ttu-id="623ad-201">**MÉRITO \_ \_ não \_ use**</span><span class="sxs-lookup"><span data-stu-id="623ad-201">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="623ad-202">Filtros de origem BDA</span><span class="sxs-lookup"><span data-stu-id="623ad-202">BDA Source Filters</span></span>                  | <span data-ttu-id="623ad-203">**\_ \_ sintonizador de rede BDA KSCATEGORY \_**</span><span class="sxs-lookup"><span data-stu-id="623ad-203">**KSCATEGORY\_BDA\_NETWORK\_TUNER**</span></span>         | <span data-ttu-id="623ad-204">**MÉRITO \_ \_ não \_ use**</span><span class="sxs-lookup"><span data-stu-id="623ad-204">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="623ad-205">Renderizadores de informações de transporte BDA</span><span class="sxs-lookup"><span data-stu-id="623ad-205">BDA Transport Information Renderers</span></span> | <span data-ttu-id="623ad-206">**\_informações de \_ transporte \_ BDA KSCATEGORY**</span><span class="sxs-lookup"><span data-stu-id="623ad-206">**KSCATEGORY\_BDA\_TRANSPORT\_INFORMATION**</span></span> | <span data-ttu-id="623ad-207">**MÉRITO \_ normal**</span><span class="sxs-lookup"><span data-stu-id="623ad-207">**MERIT\_NORMAL**</span></span>       |



 

> [!Note]  
> <span data-ttu-id="623ad-208">Os decodificadores são registrados na categoria "filtros do DirectShow" (CLSID \_ LegacyAmFilterCategory).</span><span class="sxs-lookup"><span data-stu-id="623ad-208">Decoders are registered under the "DirectShow Filters" category (CLSID\_LegacyAmFilterCategory).</span></span>

 

## <a name="other-filter-categories"></a><span data-ttu-id="623ad-209">Outras categorias de filtro</span><span class="sxs-lookup"><span data-stu-id="623ad-209">Other Filter Categories</span></span>

<span data-ttu-id="623ad-210">As categorias listadas aqui podem ser enumeradas com o enumerador de dispositivo do sistema, mas não são visíveis para o mapeador de filtro e não são usadas pelo [Intelligent Connect](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="623ad-210">The categories listed here can be enumerated with the System Device Enumerator, but are not visible to the Filter Mapper and are not used by [Intelligent Connect](intelligent-connect.md).</span></span>

<span data-ttu-id="623ad-211">As categorias a seguir são declaradas no arquivo de cabeçalho QEdit. h.</span><span class="sxs-lookup"><span data-stu-id="623ad-211">The following categories are declared in the header file Qedit.h.</span></span>



| <span data-ttu-id="623ad-212">Nome amigável</span><span class="sxs-lookup"><span data-stu-id="623ad-212">Friendly Name</span></span>            | <span data-ttu-id="623ad-213">CLID</span><span class="sxs-lookup"><span data-stu-id="623ad-213">CLID</span></span>                             | <span data-ttu-id="623ad-214">Núcleo</span><span class="sxs-lookup"><span data-stu-id="623ad-214">Merit</span></span>                   |
|--------------------------|----------------------------------|-------------------------|
| <span data-ttu-id="623ad-215">Efeitos de vídeo (1 entrada)</span><span class="sxs-lookup"><span data-stu-id="623ad-215">Video Effects (1 input)</span></span>  | <span data-ttu-id="623ad-216">**\_VIDEOEFFECTS1CATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="623ad-216">**CLSID\_VideoEffects1Category**</span></span> | <span data-ttu-id="623ad-217">**MÉRITO \_ \_ não \_ use**</span><span class="sxs-lookup"><span data-stu-id="623ad-217">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="623ad-218">Efeitos de vídeo (2 entradas)</span><span class="sxs-lookup"><span data-stu-id="623ad-218">Video Effects (2 inputs)</span></span> | <span data-ttu-id="623ad-219">**\_VIDEOEFFECTS2CATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="623ad-219">**CLSID\_VideoEffects2Category**</span></span> | <span data-ttu-id="623ad-220">**MÉRITO \_ \_ não \_ use**</span><span class="sxs-lookup"><span data-stu-id="623ad-220">**MERIT\_DO\_NOT\_USE**</span></span> |



 

<span data-ttu-id="623ad-221">Essas categorias contêm efeitos de vídeo e transições para [serviços de edição do DirectShow](directshow-editing-services.md):</span><span class="sxs-lookup"><span data-stu-id="623ad-221">These categories contain video effects and transitions for [DirectShow Editing Services](directshow-editing-services.md):</span></span>

-   <span data-ttu-id="623ad-222">"Efeitos de vídeo (1 entrada)" contém efeitos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="623ad-222">"Video Effects (1 input)" contains video effects.</span></span>
-   <span data-ttu-id="623ad-223">"Efeitos de vídeo (2 entrada)" contém transições de vídeo.</span><span class="sxs-lookup"><span data-stu-id="623ad-223">"Video Effects (2 input)" contains video transitions.</span></span>

<span data-ttu-id="623ad-224">Para obter mais informações, consulte [enumerando efeitos e transições](enumerating-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="623ad-224">For more information, see [Enumerating Effects and Transitions](enumerating-effects-and-transitions.md).</span></span>

<span data-ttu-id="623ad-225">As categorias a seguir são declaradas no arquivo de cabeçalho UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="623ad-225">The following categories are declared in the header file Uuids.h.</span></span> <span data-ttu-id="623ad-226">Inclua o arquivo de cabeçalho DShow. h.</span><span class="sxs-lookup"><span data-stu-id="623ad-226">Include the header file Dshow.h.</span></span>



| <span data-ttu-id="623ad-227">Nome amigável</span><span class="sxs-lookup"><span data-stu-id="623ad-227">Friendly Name</span></span>       | <span data-ttu-id="623ad-228">CLID</span><span class="sxs-lookup"><span data-stu-id="623ad-228">CLID</span></span>                                | <span data-ttu-id="623ad-229">Núcleo</span><span class="sxs-lookup"><span data-stu-id="623ad-229">Merit</span></span>                   |
|---------------------|-------------------------------------|-------------------------|
| <span data-ttu-id="623ad-230">Codificadores do encapi</span><span class="sxs-lookup"><span data-stu-id="623ad-230">EncAPI Encoders</span></span>     | <span data-ttu-id="623ad-231">**\_MEDIAENCODERCATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="623ad-231">**CLSID\_MediaEncoderCategory**</span></span>     | <span data-ttu-id="623ad-232">**MÉRITO \_ \_ não \_ use**</span><span class="sxs-lookup"><span data-stu-id="623ad-232">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="623ad-233">Multiplexadores de encapi</span><span class="sxs-lookup"><span data-stu-id="623ad-233">EncAPI Multiplexers</span></span> | <span data-ttu-id="623ad-234">**\_MEDIAMULTIPLEXERCATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="623ad-234">**CLSID\_MediaMultiplexerCategory**</span></span> | <span data-ttu-id="623ad-235">**MÉRITO \_ \_ não \_ use**</span><span class="sxs-lookup"><span data-stu-id="623ad-235">**MERIT\_DO\_NOT\_USE**</span></span> |



 

## <a name="directshow-filter-meta-category"></a><span data-ttu-id="623ad-236">Filtro do DirectShow Meta-Category</span><span class="sxs-lookup"><span data-stu-id="623ad-236">DirectShow Filter Meta-Category</span></span>



| <span data-ttu-id="623ad-237">Nome amigável</span><span class="sxs-lookup"><span data-stu-id="623ad-237">Friendly Name</span></span>                 | <span data-ttu-id="623ad-238">CLSID</span><span class="sxs-lookup"><span data-stu-id="623ad-238">CLSID</span></span>                            | <span data-ttu-id="623ad-239">Núcleo</span><span class="sxs-lookup"><span data-stu-id="623ad-239">Merit</span></span>          |
|-------------------------------|----------------------------------|----------------|
| <span data-ttu-id="623ad-240">Categorias de filtro do ActiveMovie</span><span class="sxs-lookup"><span data-stu-id="623ad-240">ActiveMovie Filter Categories</span></span> | <span data-ttu-id="623ad-241">**\_ACTIVEMOVIECATEGORIES CLSID**</span><span class="sxs-lookup"><span data-stu-id="623ad-241">**CLSID\_ActiveMovieCategories**</span></span> | <span data-ttu-id="623ad-242">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="623ad-242">Not applicable</span></span> |



 

<span data-ttu-id="623ad-243">Essa meta-categoria contém uma lista de categorias de filtro.</span><span class="sxs-lookup"><span data-stu-id="623ad-243">This meta-category contains a list of filter categories.</span></span> <span data-ttu-id="623ad-244">Se uma categoria de filtro não aparecer nessa lista, o [mapeador de filtro](filter-mapper.md) ignorará a categoria, o que significa que o filtro não está disponível para [conexão inteligente](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="623ad-244">If a filter category does not appear within this list, the [Filter Mapper](filter-mapper.md) ignores the category, which means the filter is not available for [Intelligent Connect](intelligent-connect.md).</span></span>

<span data-ttu-id="623ad-245">Para enumerar a lista de categorias de filtro, chame [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) com o valor CLSID \_ ActiveMovieCategories.</span><span class="sxs-lookup"><span data-stu-id="623ad-245">To enumerate the list of filter categories, call [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) with the value CLSID\_ActiveMovieCategories.</span></span> <span data-ttu-id="623ad-246">Os monikers retornados por esse método dão suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="623ad-246">The monikers returned by this method support the following properties.</span></span>



| <span data-ttu-id="623ad-247">Nome da propriedade</span><span class="sxs-lookup"><span data-stu-id="623ad-247">Property Name</span></span>  | <span data-ttu-id="623ad-248">Descrição</span><span class="sxs-lookup"><span data-stu-id="623ad-248">Description</span></span>                                                                            |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="623ad-249">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="623ad-249">"FriendlyName"</span></span> | <span data-ttu-id="623ad-250">Nome da categoria (VT \_ BSTR).</span><span class="sxs-lookup"><span data-stu-id="623ad-250">Category name (VT\_BSTR).</span></span>                                                              |
| <span data-ttu-id="623ad-251">Núcleo</span><span class="sxs-lookup"><span data-stu-id="623ad-251">"Merit"</span></span>        | <span data-ttu-id="623ad-252">Mérito de categoria (VT \_ i4).</span><span class="sxs-lookup"><span data-stu-id="623ad-252">Category merit (VT\_I4).</span></span> <span data-ttu-id="623ad-253">Se essa propriedade estiver ausente, trate como **mérito \_ não \_ \_ usar**.</span><span class="sxs-lookup"><span data-stu-id="623ad-253">If this property is absent, treat as **MERIT\_DO\_NOT\_USE**.</span></span> |
| <span data-ttu-id="623ad-254">CLSID</span><span class="sxs-lookup"><span data-stu-id="623ad-254">"CLSID"</span></span>        | <span data-ttu-id="623ad-255">CLSID da categoria (VT \_ BSTR).</span><span class="sxs-lookup"><span data-stu-id="623ad-255">Category CLSID (VT\_BSTR).</span></span>                                                             |



 

<span data-ttu-id="623ad-256">Para adicionar uma nova categoria de filtro a essa lista, chame [**IFilterMapper2:: createcategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory).</span><span class="sxs-lookup"><span data-stu-id="623ad-256">To add a new filter category to this list, call [**IFilterMapper2::CreateCategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory).</span></span>

## <a name="dmo-categories"></a><span data-ttu-id="623ad-257">Categorias de DMO</span><span class="sxs-lookup"><span data-stu-id="623ad-257">DMO Categories</span></span>

<span data-ttu-id="623ad-258">Os DMOs (objetos de mídia do DirectX) usam um mecanismo de enumeração diferente dos filtros do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="623ad-258">DirectX Media Objects (DMOs) use a different enumeration mechanism from DirectShow filters.</span></span> <span data-ttu-id="623ad-259">Para obter mais informações, consulte [registrando um DMO](registering-a-dmo.md).</span><span class="sxs-lookup"><span data-stu-id="623ad-259">For more information, see [Registering a DMO](registering-a-dmo.md).</span></span> <span data-ttu-id="623ad-260">No entanto, você pode usar o enumerador de dispositivo do sistema para enumerar categorias DMO.</span><span class="sxs-lookup"><span data-stu-id="623ad-260">However, you can use the System Device Enumerator to enumerate DMO categories.</span></span> <span data-ttu-id="623ad-261">Os monikers são associados ao [filtro de invólucro do DMO](dmo-wrapper-filter.md) e inicializam automaticamente o filtro com o DMO.</span><span class="sxs-lookup"><span data-stu-id="623ad-261">The monikers bind to the [DMO Wrapper Filter](dmo-wrapper-filter.md) and automatically initialize the filter with the DMO.</span></span>

<span data-ttu-id="623ad-262">Além disso, algumas das categorias de DMO são mapeadas para categorias de filtro do DirectShow para fins de conexão inteligente:</span><span class="sxs-lookup"><span data-stu-id="623ad-262">In addition, some of the DMO categories are mapped to DirectShow filter categories for the purposes of intelligent connect:</span></span>



| <span data-ttu-id="623ad-263">Categoria de DMO</span><span class="sxs-lookup"><span data-stu-id="623ad-263">DMO Category</span></span>                    | <span data-ttu-id="623ad-264">Equivalente do DirectShow</span><span class="sxs-lookup"><span data-stu-id="623ad-264">DirectShow Equivalent</span></span>              |
|---------------------------------|------------------------------------|
| <span data-ttu-id="623ad-265">**\_codificador de áudio DMOCATEGORY \_**</span><span class="sxs-lookup"><span data-stu-id="623ad-265">**DMOCATEGORY\_AUDIO\_ENCODER**</span></span> | <span data-ttu-id="623ad-266">**\_AUDIOCOMPRESSORCATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="623ad-266">**CLSID\_AudioCompressorCategory**</span></span> |
| <span data-ttu-id="623ad-267">**\_decodificador de áudio DMOCATEGORY \_**</span><span class="sxs-lookup"><span data-stu-id="623ad-267">**DMOCATEGORY\_AUDIO\_DECODER**</span></span> | <span data-ttu-id="623ad-268">**\_LEGACYAMFILTERCATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="623ad-268">**CLSID\_LegacyAmFilterCategory**</span></span>  |
| <span data-ttu-id="623ad-269">**\_codificador de vídeo DMOCATEGORY \_**</span><span class="sxs-lookup"><span data-stu-id="623ad-269">**DMOCATEGORY\_VIDEO\_ENCODER**</span></span> | <span data-ttu-id="623ad-270">**\_VIDEOCOMPRESSORCATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="623ad-270">**CLSID\_VideoCompressorCategory**</span></span> |
| <span data-ttu-id="623ad-271">**\_decodificador de vídeo DMOCATEGORY \_**</span><span class="sxs-lookup"><span data-stu-id="623ad-271">**DMOCATEGORY\_VIDEO\_DECODER**</span></span> | <span data-ttu-id="623ad-272">**\_LEGACYAMFILTERCATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="623ad-272">**CLSID\_LegacyAmFilterCategory**</span></span>  |



 

<span data-ttu-id="623ad-273">Observe que as categorias de efeito de vídeo e de efeito de áudio não são mapeadas para nenhuma categoria do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="623ad-273">Note that the video effect and audio effect categories are not mapped to any DirectShow categories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="623ad-274">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="623ad-274">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="623ad-275">Constantes e GUIDs</span><span class="sxs-lookup"><span data-stu-id="623ad-275">Constants and GUIDs</span></span>](constants-and-guids.md)
</dt> <dt>

[<span data-ttu-id="623ad-276">Enumerando dispositivos e filtros</span><span class="sxs-lookup"><span data-stu-id="623ad-276">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="623ad-277">Conexão inteligente</span><span class="sxs-lookup"><span data-stu-id="623ad-277">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> <dt>

[<span data-ttu-id="623ad-278">Layout das chaves do registro</span><span class="sxs-lookup"><span data-stu-id="623ad-278">Layout of the Registry Keys</span></span>](layout-of-the-registry-keys.md)
</dt> <dt>

[<span data-ttu-id="623ad-279">Usando o mapeador de filtro</span><span class="sxs-lookup"><span data-stu-id="623ad-279">Using the Filter Mapper</span></span>](using-the-filter-mapper.md)
</dt> <dt>

[<span data-ttu-id="623ad-280">Usando o enumerador de dispositivo do sistema</span><span class="sxs-lookup"><span data-stu-id="623ad-280">Using the System Device Enumerator</span></span>](using-the-system-device-enumerator.md)
</dt> </dl>

 

 




