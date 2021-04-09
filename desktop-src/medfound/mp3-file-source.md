---
description: A fonte de arquivo MP3 analisa os arquivos MP3.
ms.assetid: 37362642-1b8a-4fb3-950d-ed1afe3696e5
title: Origem de arquivo MP3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2241e3b99d5a1918be8ff0182a9eca8939c12ce2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091045"
---
# <a name="mp3-file-source"></a><span data-ttu-id="cc865-103">Origem de arquivo MP3</span><span class="sxs-lookup"><span data-stu-id="cc865-103">MP3 File Source</span></span>

<span data-ttu-id="cc865-104">A fonte de arquivo MP3 analisa os arquivos MP3.</span><span class="sxs-lookup"><span data-stu-id="cc865-104">The MP3 file source parses MP3 files.</span></span>

<span data-ttu-id="cc865-105">A origem do arquivo MP3 gera buffers que contêm quadros de áudio MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="cc865-105">The MP3 file source outputs buffers that contain MPEG-1 audio frames.</span></span> <span data-ttu-id="cc865-106">Ele não decodifica o áudio.</span><span class="sxs-lookup"><span data-stu-id="cc865-106">It does not decode the audio.</span></span>

## <a name="file-extensions-and-mime-types"></a><span data-ttu-id="cc865-107">Extensões de arquivo e tipos MIME</span><span class="sxs-lookup"><span data-stu-id="cc865-107">File Extensions and MIME Types</span></span>

<span data-ttu-id="cc865-108">A origem do arquivo MP3 é a fonte de mídia padrão para a seguinte extensão de nome de arquivo:</span><span class="sxs-lookup"><span data-stu-id="cc865-108">The MP3 file source is the default media source for the following file name extension:</span></span>

-   <span data-ttu-id="cc865-109">.mp3</span><span class="sxs-lookup"><span data-stu-id="cc865-109">.mp3</span></span>

<span data-ttu-id="cc865-110">Também é a fonte de mídia padrão para os tipos MIME a seguir.</span><span class="sxs-lookup"><span data-stu-id="cc865-110">It is also the default media source for the following MIME types.</span></span>

-   <span data-ttu-id="cc865-111">áudio/MPEG</span><span class="sxs-lookup"><span data-stu-id="cc865-111">audio/mpeg</span></span>
-   <span data-ttu-id="cc865-112">áudio/x-mp3</span><span class="sxs-lookup"><span data-stu-id="cc865-112">audio/x-mp3</span></span>
-   <span data-ttu-id="cc865-113">áudio/x-MPEG</span><span class="sxs-lookup"><span data-stu-id="cc865-113">audio/x-mpeg</span></span>

## <a name="media-types"></a><span data-ttu-id="cc865-114">Tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="cc865-114">Media Types</span></span>

<span data-ttu-id="cc865-115">O tipo de mídia oferecido pela origem do arquivo MP3 contém os seguintes atributos.</span><span class="sxs-lookup"><span data-stu-id="cc865-115">The media type offered by the MP3 file source contains the following attributes.</span></span>



| <span data-ttu-id="cc865-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="cc865-116">Attribute</span></span>                                                                                    | <span data-ttu-id="cc865-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc865-117">Description</span></span>                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc865-118">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="cc865-118">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="cc865-119">Igual a **MFMediaType \_ Audio**.</span><span class="sxs-lookup"><span data-stu-id="cc865-119">Equal to **MFMediaType\_Audio**.</span></span>                                                                                                                   |
| [<span data-ttu-id="cc865-120">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="cc865-120">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="cc865-121">Igual a **MFAudioFormat \_ mp3** ou **MFAudioFormat \_ MPEG**.</span><span class="sxs-lookup"><span data-stu-id="cc865-121">Equal to **MFAudioFormat\_MP3** or **MFAudioFormat\_MPEG**.</span></span>                                                                                        |
| [<span data-ttu-id="cc865-122">**áudio do MF \_ MT \_ média de \_ \_ bytes \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="cc865-122">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="cc865-123">Número médio de bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="cc865-123">Average number of bytes per second.</span></span>                                                                                                                |
| [<span data-ttu-id="cc865-124">**\_alinhamento de \_ bloco de áudio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cc865-124">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="cc865-125">Igual a 1.</span><span class="sxs-lookup"><span data-stu-id="cc865-125">Equal to 1.</span></span>                                                                                                                                        |
| [<span data-ttu-id="cc865-126">**\_canais de \_ número de áudio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cc865-126">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="cc865-127">Número de canais de áudio.</span><span class="sxs-lookup"><span data-stu-id="cc865-127">Number of audio channels.</span></span>                                                                                                                          |
| [<span data-ttu-id="cc865-128">**\_amostras de áudio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="cc865-128">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="cc865-129">Número de amostras de áudio por segundo.</span><span class="sxs-lookup"><span data-stu-id="cc865-129">Number of audio samples per second.</span></span>                                                                                                                |
| [<span data-ttu-id="cc865-130">**dados de usuário do MF \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cc865-130">**MF\_MT\_USER\_DATA**</span></span>](mf-mt-user-data-attribute.md)                                      | <span data-ttu-id="cc865-131">Contém a parte de uma estrutura [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) que aparece após o membro **WFX** da estrutura.</span><span class="sxs-lookup"><span data-stu-id="cc865-131">Contains the portion of a [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) structure that appears after the **wfx** member of the structure.</span></span> |



 

## <a name="interfaces"></a><span data-ttu-id="cc865-132">Interfaces</span><span class="sxs-lookup"><span data-stu-id="cc865-132">Interfaces</span></span>

<span data-ttu-id="cc865-133">A origem do arquivo MP3 expõe as seguintes interfaces por meio de [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):</span><span class="sxs-lookup"><span data-stu-id="cc865-133">The MP3 file source exposes the following interfaces through [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):</span></span>

-   [<span data-ttu-id="cc865-134">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="cc865-134">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="cc865-135">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="cc865-135">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [<span data-ttu-id="cc865-136">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="cc865-136">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)

<span data-ttu-id="cc865-137">Além disso, ele expõe as seguintes interfaces por meio de [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice):</span><span class="sxs-lookup"><span data-stu-id="cc865-137">In addition, it exposes the following interfaces through [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cc865-138">GUID de Serviço</span><span class="sxs-lookup"><span data-stu-id="cc865-138">Service GUID</span></span></th>
<th><span data-ttu-id="cc865-139">Interface</span><span class="sxs-lookup"><span data-stu-id="cc865-139">Interface</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc865-140"><strong>MF_METADATA_PROVIDER_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="cc865-140"><strong>MF_METADATA_PROVIDER_SERVICE</strong></span></span></td>
<td><span data-ttu-id="cc865-141"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc865-141"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc865-142"><strong>MF_PROPERTY_HANDLER_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="cc865-142"><strong>MF_PROPERTY_HANDLER_SERVICE</strong></span></span></td>
<td><span data-ttu-id="cc865-143"><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="cc865-143"><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="cc865-144">Consulte <a href="shell-metadata-providers.md">provedores de metadados do Shell</a>.</span><span class="sxs-lookup"><span data-stu-id="cc865-144">See <a href="shell-metadata-providers.md">Shell Metadata Providers</a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc865-145"><strong>MF_RATE_CONTROL_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="cc865-145"><strong>MF_RATE_CONTROL_SERVICE</strong></span></span></td>
<td><span data-ttu-id="cc865-146"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>IMFRateControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc865-146"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>IMFRateControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc865-147"><strong>MF_RATE_CONTROL_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="cc865-147"><strong>MF_RATE_CONTROL_SERVICE</strong></span></span></td>
<td><span data-ttu-id="cc865-148"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>IMFRateSupport</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc865-148"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>IMFRateSupport</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="cc865-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc865-149">Requirements</span></span>



| <span data-ttu-id="cc865-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc865-150">Requirement</span></span> | <span data-ttu-id="cc865-151">Valor</span><span class="sxs-lookup"><span data-stu-id="cc865-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="cc865-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc865-152">Minimum supported client</span></span><br/> | <span data-ttu-id="cc865-153">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cc865-153">Windows 7 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cc865-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc865-154">Minimum supported server</span></span><br/> | <span data-ttu-id="cc865-155">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="cc865-155">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cc865-156">DLL</span><span class="sxs-lookup"><span data-stu-id="cc865-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc865-157"><dt>Mf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc865-157"><dt>Mf.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc865-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc865-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc865-159">Fontes de mídia e coletores</span><span class="sxs-lookup"><span data-stu-id="cc865-159">Media Sources and Sinks</span></span>](media-sources-and-sinks.md)
</dt> <dt>

[<span data-ttu-id="cc865-160">Fontes de mídia</span><span class="sxs-lookup"><span data-stu-id="cc865-160">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="cc865-161">Resolvedor de origem</span><span class="sxs-lookup"><span data-stu-id="cc865-161">Source Resolver</span></span>](source-resolver.md)
</dt> <dt>

[<span data-ttu-id="cc865-162">Formatos de mídia compatíveis com o Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cc865-162">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
