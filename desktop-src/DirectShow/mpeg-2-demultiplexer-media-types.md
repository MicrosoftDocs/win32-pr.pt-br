---
description: Tipos de mídia de Desmultiplexador MPEG-2
ms.assetid: 240d1753-df8c-45fe-b5a7-9faa96fc5b18
title: Tipos de mídia de Desmultiplexador MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9b5276b975771ba62118976c8e63b4d5faa53d
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909994"
---
# <a name="mpeg-2-demultiplexer-media-types"></a><span data-ttu-id="f90e9-103">Tipos de mídia de Desmultiplexador MPEG-2</span><span class="sxs-lookup"><span data-stu-id="f90e9-103">MPEG-2 Demultiplexer Media Types</span></span>

<span data-ttu-id="f90e9-104">O filtro de [Desmultiplexador MPEG-2](mpeg-2-demultiplexer.md) reconhece os seguintes tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="f90e9-104">The [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) filter recognizes the following media types.</span></span>

### <a name="input-types"></a><span data-ttu-id="f90e9-105">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="f90e9-105">Input Types</span></span>

<span data-ttu-id="f90e9-106">O tipo principal é sempre **\_ fluxo de MediaType**.</span><span class="sxs-lookup"><span data-stu-id="f90e9-106">The major type is always **MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="f90e9-107">O subtipo pode ser qualquer um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="f90e9-107">The subtype can be any of the following.</span></span>



| <span data-ttu-id="f90e9-108">GUID</span><span class="sxs-lookup"><span data-stu-id="f90e9-108">GUID</span></span>                                             | <span data-ttu-id="f90e9-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f90e9-109">Description</span></span>                                                                                                                                                                                               |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f90e9-110">**\_Transporte do KSDATAFORMAT \_ \_ MPEG2 BDA do subtipo \_**</span><span class="sxs-lookup"><span data-stu-id="f90e9-110">**KSDATAFORMAT\_SUBTYPE\_BDA\_MPEG2\_TRANSPORT**</span></span> | <span data-ttu-id="f90e9-111">Fluxo de transporte de um filtro de dispositivo da arquitetura de driver de difusão (BDA).</span><span class="sxs-lookup"><span data-stu-id="f90e9-111">Transport stream from a Broadcast Driver Architecture (BDA) device filter.</span></span> <span data-ttu-id="f90e9-112">O demultiplexador MPEG-2 trata esse subtipo de forma idêntica **ao \_ \_ transporte MEDIASUBTYPE MPEG2**.</span><span class="sxs-lookup"><span data-stu-id="f90e9-112">The MPEG-2 demultiplexer treats this subtype identically to **MEDIASUBTYPE\_MPEG2\_TRANSPORT**.</span></span>                                |
| <span data-ttu-id="f90e9-113">**\_Programa MEDIASUBTYPE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="f90e9-113">**MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span>                 | <span data-ttu-id="f90e9-114">Fluxo do programa</span><span class="sxs-lookup"><span data-stu-id="f90e9-114">Program stream</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="f90e9-115">**\_Transporte MEDIASUBTYPE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="f90e9-115">**MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span>               | <span data-ttu-id="f90e9-116">Fluxo de transporte (TS), com pacotes de 188 bytes</span><span class="sxs-lookup"><span data-stu-id="f90e9-116">Transport stream (TS), with 188-byte packets</span></span>                                                                                                                                                              |
| <span data-ttu-id="f90e9-117">**\_Stride de \_ transporte MEDIASUBTYPE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="f90e9-117">**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**</span></span>       | <span data-ttu-id="f90e9-118">Fluxo de transporte com pacotes "enrided".</span><span class="sxs-lookup"><span data-stu-id="f90e9-118">Transport stream with "strided" packets.</span></span> <span data-ttu-id="f90e9-119">Esse subtipo indica que os pacotes TS podem ser preenchidos com bytes extras.</span><span class="sxs-lookup"><span data-stu-id="f90e9-119">This subtype indicates that the TS packets may be padded with extra bytes.</span></span> <span data-ttu-id="f90e9-120">Para obter mais informações, consulte [**MPEG2 \_ Transport \_ Stride**](mpeg2-transport-stride.md).</span><span class="sxs-lookup"><span data-stu-id="f90e9-120">For more information, see [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> |



 

<span data-ttu-id="f90e9-121">Para pacotes de transporte (STRIDE de **\_ transporte MEDIASUBTYPE \_ MPEG2 \_**), cada amostra de mídia deve conter um número integral de pacotes de transporte, conforme descrito no [**\_ \_ Stride de transporte MPEG2**](mpeg2-transport-stride.md).</span><span class="sxs-lookup"><span data-stu-id="f90e9-121">For strided transport packets (**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**), each media sample must contain an integral number of transport packets, as described in [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> <span data-ttu-id="f90e9-122">Para todos os outros tipos de entrada, não há restrições sobre os limites de amostra; pacotes individuais podem abranger limites de amostra.</span><span class="sxs-lookup"><span data-stu-id="f90e9-122">For all other input types, there are no restrictions on sample boundaries; individual packets can span sample boundaries.</span></span>

### <a name="output-types"></a><span data-ttu-id="f90e9-123">Tipos de saída</span><span class="sxs-lookup"><span data-stu-id="f90e9-123">Output Types</span></span>

<span data-ttu-id="f90e9-124">O demultiplexador MPEG-2 não valida tipos de saída; o filtro downstream é responsável por analisar os dados que recebe do demultiplexador.</span><span class="sxs-lookup"><span data-stu-id="f90e9-124">The MPEG-2 Demultiplexer does not validate output types; the downstream filter is responsible for parsing the data it receives from the demultiplexer.</span></span> <span data-ttu-id="f90e9-125">No entanto, os seguintes tipos são normalmente aceitos por filtros downstream como saída do demultiplexador.</span><span class="sxs-lookup"><span data-stu-id="f90e9-125">However, the following types are commonly accepted by downstream filters as output from the demultiplexer.</span></span>

### <a name="mpeg-2-sections"></a><span data-ttu-id="f90e9-126">Seções MPEG-2</span><span class="sxs-lookup"><span data-stu-id="f90e9-126">MPEG-2 Sections</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f90e9-127">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="f90e9-127">Major Type</span></span></td>
<td><span data-ttu-id="f90e9-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span><span class="sxs-lookup"><span data-stu-id="f90e9-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f90e9-129">Subtype</span><span class="sxs-lookup"><span data-stu-id="f90e9-129">Subtype</span></span></td>
<td><span data-ttu-id="f90e9-130">Um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="f90e9-130">Any of the following:</span></span><br/>
<ul>
<li><span data-ttu-id="f90e9-131"><strong>MEDIASUBTYPE_ATSC_SI</strong>: informações do serviço ATSC.</span><span class="sxs-lookup"><span data-stu-id="f90e9-131"><strong>MEDIASUBTYPE_ATSC_SI</strong>: ATSC Service Information.</span></span></li>
<li><span data-ttu-id="f90e9-132"><strong>MEDIASUBTYPE_DVB_SI</strong>: informações de serviço DVB.</span><span class="sxs-lookup"><span data-stu-id="f90e9-132"><strong>MEDIASUBTYPE_DVB_SI</strong>: DVB Service Information.</span></span></li>
<li><span data-ttu-id="f90e9-133"><strong>MEDIASUBTYPE_ISDB_SI</strong>: informações de serviço de difusão digital de serviços integrados (ISDB).</span><span class="sxs-lookup"><span data-stu-id="f90e9-133"><strong>MEDIASUBTYPE_ISDB_SI</strong>: Integrated Services Digital Broadcasting (ISDB) Service Information.</span></span></li>
<li><span data-ttu-id="f90e9-134"><strong>MEDIASUBTYPE_MPEG2DATA</strong>: dados da seção MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="f90e9-134"><strong>MEDIASUBTYPE_MPEG2DATA</strong>: MPEG-2 section data.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f90e9-135">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="f90e9-135">Format Type</span></span></td>
<td><span data-ttu-id="f90e9-136">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f90e9-136">None</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="mpeg-2-video"></a><span data-ttu-id="f90e9-137">Vídeo MPEG-2</span><span class="sxs-lookup"><span data-stu-id="f90e9-137">MPEG-2 Video</span></span>



| <span data-ttu-id="f90e9-138">Label</span><span class="sxs-lookup"><span data-stu-id="f90e9-138">Label</span></span> | <span data-ttu-id="f90e9-139">Valor</span><span class="sxs-lookup"><span data-stu-id="f90e9-139">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="f90e9-140">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="f90e9-140">Major type</span></span>       | <span data-ttu-id="f90e9-141">**Vídeo de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="f90e9-141">**MEDIATYPE\_Video**</span></span>                     |
| <span data-ttu-id="f90e9-142">Subtype</span><span class="sxs-lookup"><span data-stu-id="f90e9-142">Subtype</span></span>          | <span data-ttu-id="f90e9-143">**Vídeo do MEDIASUBTYPE \_ MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="f90e9-143">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           |
| <span data-ttu-id="f90e9-144">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="f90e9-144">Format Type</span></span>      | <span data-ttu-id="f90e9-145">**MPEG2Video de formato \_**</span><span class="sxs-lookup"><span data-stu-id="f90e9-145">**FORMAT\_MPEG2Video**</span></span>                   |
| <span data-ttu-id="f90e9-146">Estrutura de formato</span><span class="sxs-lookup"><span data-stu-id="f90e9-146">Format Structure</span></span> | [<span data-ttu-id="f90e9-147">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="f90e9-147">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) |



 

### <a name="mpeg-2-audio"></a><span data-ttu-id="f90e9-148">Áudio MPEG-2</span><span class="sxs-lookup"><span data-stu-id="f90e9-148">MPEG-2 Audio</span></span>



| <span data-ttu-id="f90e9-149">Label</span><span class="sxs-lookup"><span data-stu-id="f90e9-149">Label</span></span> | <span data-ttu-id="f90e9-150">Valor</span><span class="sxs-lookup"><span data-stu-id="f90e9-150">Value</span></span> |
|------------------|--------------------------------------|
| <span data-ttu-id="f90e9-151">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="f90e9-151">Major type</span></span>       | <span data-ttu-id="f90e9-152">**Áudio de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="f90e9-152">**MEDIATYPE\_Audio**</span></span>                 |
| <span data-ttu-id="f90e9-153">Subtype</span><span class="sxs-lookup"><span data-stu-id="f90e9-153">Subtype</span></span>          | <span data-ttu-id="f90e9-154">**\_Áudio MEDIASUBTYPE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="f90e9-154">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>       |
| <span data-ttu-id="f90e9-155">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="f90e9-155">Format Type</span></span>      | <span data-ttu-id="f90e9-156">**WaveFormatEx de formato \_**</span><span class="sxs-lookup"><span data-stu-id="f90e9-156">**FORMAT\_WaveFormatEx**</span></span>             |
| <span data-ttu-id="f90e9-157">Estrutura de formato</span><span class="sxs-lookup"><span data-stu-id="f90e9-157">Format Structure</span></span> | <span data-ttu-id="f90e9-158">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f90e9-158">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f90e9-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f90e9-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f90e9-160">Tipos de mídia MPEG-2</span><span class="sxs-lookup"><span data-stu-id="f90e9-160">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
