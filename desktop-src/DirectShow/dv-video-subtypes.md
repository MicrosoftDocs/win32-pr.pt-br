---
description: Vários subtipos são definidos para vídeo DV. Cada um tem um código FOURCC e um valor GUID correspondente. Nem todos esses formatos têm suporte; consulte a seção comentários para obter mais informações.
ms.assetid: d8390bd4-0339-4955-992c-92b8c9f6bf88
title: Subtipos de vídeo DV (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbacb15f5801d959fbc5150546cff04dea687753
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770080"
---
# <a name="dv-video-subtypes"></a><span data-ttu-id="b59a3-105">Subtipos de vídeo DV</span><span class="sxs-lookup"><span data-stu-id="b59a3-105">DV Video Subtypes</span></span>

<span data-ttu-id="b59a3-106">Vários subtipos são definidos para vídeo DV.</span><span class="sxs-lookup"><span data-stu-id="b59a3-106">A number of subtypes are defined for DV video.</span></span> <span data-ttu-id="b59a3-107">Cada um tem um código FOURCC e um valor GUID correspondente.</span><span class="sxs-lookup"><span data-stu-id="b59a3-107">Each has a FOURCC code and a corresponding GUID value.</span></span> <span data-ttu-id="b59a3-108">Nem todos esses formatos têm suporte; consulte a seção comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b59a3-108">Not all of these formats are supported; see the Remarks section for more information.</span></span>

## <a name="consumer-formats"></a><span data-ttu-id="b59a3-109">Formatos de consumidor</span><span class="sxs-lookup"><span data-stu-id="b59a3-109">Consumer Formats</span></span>



| <span data-ttu-id="b59a3-110">FOURCC</span><span class="sxs-lookup"><span data-stu-id="b59a3-110">FOURCC</span></span> | <span data-ttu-id="b59a3-111">GUID</span><span class="sxs-lookup"><span data-stu-id="b59a3-111">GUID</span></span>               | <span data-ttu-id="b59a3-112">Taxa de dados</span><span class="sxs-lookup"><span data-stu-id="b59a3-112">Data Rate</span></span> | <span data-ttu-id="b59a3-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="b59a3-113">Description</span></span>                  |
|--------|--------------------|-----------|------------------------------|
| <span data-ttu-id="b59a3-114">'dvsl'</span><span class="sxs-lookup"><span data-stu-id="b59a3-114">'dvsl'</span></span> | <span data-ttu-id="b59a3-115">MEDIASUBTYPE \_ dvsl</span><span class="sxs-lookup"><span data-stu-id="b59a3-115">MEDIASUBTYPE\_dvsl</span></span> | <span data-ttu-id="b59a3-116">12,5 Mbps</span><span class="sxs-lookup"><span data-stu-id="b59a3-116">12.5 Mbps</span></span> | <span data-ttu-id="b59a3-117">SD-DVCR (525-60 ou 625-50)</span><span class="sxs-lookup"><span data-stu-id="b59a3-117">SD-DVCR (525-60 or 625-50)</span></span>   |
| <span data-ttu-id="b59a3-118">'dvsd'</span><span class="sxs-lookup"><span data-stu-id="b59a3-118">'dvsd'</span></span> | <span data-ttu-id="b59a3-119">MEDIASUBTYPE \_ dvsd</span><span class="sxs-lookup"><span data-stu-id="b59a3-119">MEDIASUBTYPE\_dvsd</span></span> | <span data-ttu-id="b59a3-120">25 Mbps</span><span class="sxs-lookup"><span data-stu-id="b59a3-120">25 Mbps</span></span>   | <span data-ttu-id="b59a3-121">SDL-DVCR (525-60 ou 625-50)</span><span class="sxs-lookup"><span data-stu-id="b59a3-121">SDL-DVCR (525-60 or 625-50)</span></span>  |
| <span data-ttu-id="b59a3-122">'dvhd'</span><span class="sxs-lookup"><span data-stu-id="b59a3-122">'dvhd'</span></span> | <span data-ttu-id="b59a3-123">MEDIASUBTYPE \_ dvhd</span><span class="sxs-lookup"><span data-stu-id="b59a3-123">MEDIASUBTYPE\_dvhd</span></span> | <span data-ttu-id="b59a3-124">50 Mbps</span><span class="sxs-lookup"><span data-stu-id="b59a3-124">50 Mbps</span></span>   | <span data-ttu-id="b59a3-125">HD-DVCR (1125-60 ou 1250-50)</span><span class="sxs-lookup"><span data-stu-id="b59a3-125">HD-DVCR (1125-60 or 1250-50)</span></span> |



 

<span data-ttu-id="b59a3-126">Consulte IEC-61834 para obter mais informações sobre esses formatos.</span><span class="sxs-lookup"><span data-stu-id="b59a3-126">Refer to IEC-61834 for more information about these formats.</span></span>

## <a name="professional-formats"></a><span data-ttu-id="b59a3-127">Formatos profissionais</span><span class="sxs-lookup"><span data-stu-id="b59a3-127">Professional Formats</span></span>



| <span data-ttu-id="b59a3-128">FOURCC</span><span class="sxs-lookup"><span data-stu-id="b59a3-128">FOURCC</span></span> | <span data-ttu-id="b59a3-129">GUID</span><span class="sxs-lookup"><span data-stu-id="b59a3-129">GUID</span></span>               | <span data-ttu-id="b59a3-130">Taxa de dados</span><span class="sxs-lookup"><span data-stu-id="b59a3-130">Data Rate</span></span> | <span data-ttu-id="b59a3-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="b59a3-131">Description</span></span>                                 |
|--------|--------------------|-----------|---------------------------------------------|
| <span data-ttu-id="b59a3-132">'dv25'</span><span class="sxs-lookup"><span data-stu-id="b59a3-132">'dv25'</span></span> | <span data-ttu-id="b59a3-133">MEDIASUBTYPE \_ DV25</span><span class="sxs-lookup"><span data-stu-id="b59a3-133">MEDIASUBTYPE\_dv25</span></span> | <span data-ttu-id="b59a3-134">25 Mbps</span><span class="sxs-lookup"><span data-stu-id="b59a3-134">25 Mbps</span></span>   | <span data-ttu-id="b59a3-135">DVCPRO 25 (525-60 ou 625-50).</span><span class="sxs-lookup"><span data-stu-id="b59a3-135">DVCPRO 25 (525-60 or 625-50).</span></span>               |
| <span data-ttu-id="b59a3-136">'dv50'</span><span class="sxs-lookup"><span data-stu-id="b59a3-136">'dv50'</span></span> | <span data-ttu-id="b59a3-137">MEDIASUBTYPE \_ DV50</span><span class="sxs-lookup"><span data-stu-id="b59a3-137">MEDIASUBTYPE\_dv50</span></span> | <span data-ttu-id="b59a3-138">50 Mbps</span><span class="sxs-lookup"><span data-stu-id="b59a3-138">50 Mbps</span></span>   | <span data-ttu-id="b59a3-139">DVCPRO 50 (525-60 ou 625-50)</span><span class="sxs-lookup"><span data-stu-id="b59a3-139">DVCPRO 50 (525-60 or 625-50)</span></span>                |
| <span data-ttu-id="b59a3-140">'dvh1'</span><span class="sxs-lookup"><span data-stu-id="b59a3-140">'dvh1'</span></span> | <span data-ttu-id="b59a3-141">MEDIASUBTYPE \_ dvh1</span><span class="sxs-lookup"><span data-stu-id="b59a3-141">MEDIASUBTYPE\_dvh1</span></span> | <span data-ttu-id="b59a3-142">100 Mbps</span><span class="sxs-lookup"><span data-stu-id="b59a3-142">100 Mbps</span></span>  | <span data-ttu-id="b59a3-143">DVCPRO 100 (1080/60i, 1080/50i ou 720/60P)</span><span class="sxs-lookup"><span data-stu-id="b59a3-143">DVCPRO 100 (1080/60i, 1080/50i, or 720/60P)</span></span> |



 

<span data-ttu-id="b59a3-144">Consulte o SMPTE 314M para obter mais informações sobre DV25 e DV50 e SMPTE 370M para obter mais informações sobre dvh1.</span><span class="sxs-lookup"><span data-stu-id="b59a3-144">Refer to SMPTE 314M for more information about dv25 and dv50, and SMPTE 370M for more information about dvh1.</span></span>

## <a name="miscellaneous"></a><span data-ttu-id="b59a3-145">Diversos</span><span class="sxs-lookup"><span data-stu-id="b59a3-145">Miscellaneous</span></span>

<span data-ttu-id="b59a3-146">Dois subtipos de DV adicionais são definidos no arquivo de cabeçalho UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="b59a3-146">Two additional DV subtypes are defined in the header file Uuids.h.</span></span> <span data-ttu-id="b59a3-147">Eles correspondem a códigos FOURCC que são produzidos por determinados codecs de DV; Eles não correspondem a nenhum padrão de DV definido.</span><span class="sxs-lookup"><span data-stu-id="b59a3-147">These correspond to FOURCC codes that are produced by certain DV codecs; they do not correspond to any defined DV standards.</span></span> <span data-ttu-id="b59a3-148">Esses subtipos são obsoletos e não devem ser usados.</span><span class="sxs-lookup"><span data-stu-id="b59a3-148">These subtypes are obsolete and should not be used.</span></span>



| <span data-ttu-id="b59a3-149">FOURCC</span><span class="sxs-lookup"><span data-stu-id="b59a3-149">FOURCC</span></span> | <span data-ttu-id="b59a3-150">GUID</span><span class="sxs-lookup"><span data-stu-id="b59a3-150">GUID</span></span>               |
|--------|--------------------|
| <span data-ttu-id="b59a3-151">DVCS</span><span class="sxs-lookup"><span data-stu-id="b59a3-151">'DVCS'</span></span> | <span data-ttu-id="b59a3-152">MEDIASUBTYPE \_ DVCS</span><span class="sxs-lookup"><span data-stu-id="b59a3-152">MEDIASUBTYPE\_DVCS</span></span> |
| <span data-ttu-id="b59a3-153">'DVSD'</span><span class="sxs-lookup"><span data-stu-id="b59a3-153">'DVSD'</span></span> | <span data-ttu-id="b59a3-154">MEDIASUBTYPE \_ DVSD</span><span class="sxs-lookup"><span data-stu-id="b59a3-154">MEDIASUBTYPE\_DVSD</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b59a3-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="b59a3-155">Remarks</span></span>

<span data-ttu-id="b59a3-156">A tabela a seguir mostra as taxas de dados com suporte, em megabits por segundo (Mbps), para os drivers MSDV e UVC.</span><span class="sxs-lookup"><span data-stu-id="b59a3-156">The following table shows the supported data rates, in megabits per second (Mbps), for the MSDV and UVC drivers.</span></span>



| <span data-ttu-id="b59a3-157">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="b59a3-157">Operating System</span></span>                                                                 | <span data-ttu-id="b59a3-158">Driver MSDV (IEEE 1394)</span><span class="sxs-lookup"><span data-stu-id="b59a3-158">MSDV (IEEE 1394) Driver</span></span> | <span data-ttu-id="b59a3-159">Driver UVC</span><span class="sxs-lookup"><span data-stu-id="b59a3-159">UVC Driver</span></span>    |
|----------------------------------------------------------------------------------|-------------------------|---------------|
| <span data-ttu-id="b59a3-160">Windows XP Service Pack 1 ou anterior</span><span class="sxs-lookup"><span data-stu-id="b59a3-160">Windows XP Service Pack 1 or earlier</span></span>                                             | <span data-ttu-id="b59a3-161">12,5, 25</span><span class="sxs-lookup"><span data-stu-id="b59a3-161">12.5, 25</span></span>                | <span data-ttu-id="b59a3-162">Não disponível</span><span class="sxs-lookup"><span data-stu-id="b59a3-162">Not available</span></span> |
| <span data-ttu-id="b59a3-163">Windows XP Service Pack 2 ou posterior, Windows Server 2003 Service Pack 1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="b59a3-163">Windows XP Service Pack 2 or later, Windows Server 2003 Service Pack 1 or later.</span></span> | <span data-ttu-id="b59a3-164">12,5, 25, 50, 100</span><span class="sxs-lookup"><span data-stu-id="b59a3-164">12.5, 25, 50, 100</span></span>       | <span data-ttu-id="b59a3-165">12,5, 25</span><span class="sxs-lookup"><span data-stu-id="b59a3-165">12.5, 25</span></span>      |



 

<span data-ttu-id="b59a3-166">Para fluxos de 25 Mbps, o comportamento do driver MSDV foi alterado no Windows Vista antes do Windows Vista, o driver MSDV sempre definiu o tipo de mídia como MEDIASUBTYPE \_ dvsd para fluxos de 25 Mbps, independentemente de a origem ser o SDL-DVCR ou DVCPRO 25.</span><span class="sxs-lookup"><span data-stu-id="b59a3-166">For 25-Mbps streams, the behavior of the MSDV driver has changed in Windows Vista Prior to Windows Vista, the MSDV driver always set the media type to MEDIASUBTYPE\_dvsd for 25-Mbps streams, regardless of whether the source was SDL-DVCR or DVCPRO 25.</span></span> <span data-ttu-id="b59a3-167">O tipo de mídia ' DV25 ' não foi usado.</span><span class="sxs-lookup"><span data-stu-id="b59a3-167">The 'dv25' media type was not used.</span></span> <span data-ttu-id="b59a3-168">A partir do Windows Vista, o driver MSDV agora distingue entre esses dois formatos.</span><span class="sxs-lookup"><span data-stu-id="b59a3-168">Starting with Windows Vista, the MSDV driver now distinguishes between these two formats.</span></span> <span data-ttu-id="b59a3-169">Para o SDL-DVCR, ele continua a usar o subtipo ' dvsd '.</span><span class="sxs-lookup"><span data-stu-id="b59a3-169">For SDL-DVCR, it continues to use the 'dvsd' subtype.</span></span> <span data-ttu-id="b59a3-170">Para o DVCPRO 25, ele agora usa o subtipo ' DV25 '.</span><span class="sxs-lookup"><span data-stu-id="b59a3-170">For DVCPRO 25, it now uses the 'dv25' subtype.</span></span>

<span data-ttu-id="b59a3-171">Os filtros de [revisor](dv-splitter-filter.md) de vídeo do DirectShow e do [codificador DV Video](dv-video-decoder-filter.md) dão suporte apenas aos formatos SDL-DVCR.</span><span class="sxs-lookup"><span data-stu-id="b59a3-171">The DirectShow [DV Splitter](dv-splitter-filter.md) and [DV Video Decoder](dv-video-decoder-filter.md) filters support SDL-DVCR formats only.</span></span> <span data-ttu-id="b59a3-172">Os dados podem ser PAL ou NTSC.</span><span class="sxs-lookup"><span data-stu-id="b59a3-172">The data can be PAL or NTSC.</span></span> <span data-ttu-id="b59a3-173">Filtros ou codecs de terceiros podem estar disponíveis e podem analisar outros formatos de DV, desde que a taxa de dados seja suportada pelo driver MSDV ou UVC.</span><span class="sxs-lookup"><span data-stu-id="b59a3-173">Third-party filters or codecs may be available that can parse other DV formats, as long as the data rate is supported by the MSDV or UVC driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="b59a3-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b59a3-174">Requirements</span></span>



| <span data-ttu-id="b59a3-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="b59a3-175">Requirement</span></span> | <span data-ttu-id="b59a3-176">Valor</span><span class="sxs-lookup"><span data-stu-id="b59a3-176">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b59a3-177">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b59a3-177">Header</span></span><br/> | <dl> <span data-ttu-id="b59a3-178"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="b59a3-178"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b59a3-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="b59a3-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b59a3-180">Vídeo digital no DirectShow</span><span class="sxs-lookup"><span data-stu-id="b59a3-180">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="b59a3-181">Driver MSDV</span><span class="sxs-lookup"><span data-stu-id="b59a3-181">MSDV Driver</span></span>](msdv-driver.md)
</dt> <dt>

[<span data-ttu-id="b59a3-182">Subtipos de vídeo</span><span class="sxs-lookup"><span data-stu-id="b59a3-182">Video Subtypes</span></span>](video-subtypes.md)
</dt> </dl>

 

 




