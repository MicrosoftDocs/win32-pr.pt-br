---
description: As GUIDs a seguir definem categorias para transformações de Media Foundation (MFTs). Essas categorias são usadas para registrar e enumerar MFTs.
ms.assetid: eca3ae3b-e40a-407d-986c-d0a85b891f52
title: MFT_CATEGORY (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7bc74054ad9f201b1f2ca53b526826d34c510d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827812"
---
# <a name="mft_category"></a><span data-ttu-id="397b2-104">Categoria de MFT \_</span><span class="sxs-lookup"><span data-stu-id="397b2-104">MFT\_CATEGORY</span></span>

<span data-ttu-id="397b2-105">As GUIDs a seguir definem categorias para transformações de Media Foundation (MFTs).</span><span class="sxs-lookup"><span data-stu-id="397b2-105">The following GUIDs define categories for Media Foundation transforms (MFTs).</span></span> <span data-ttu-id="397b2-106">Essas categorias são usadas para registrar e enumerar MFTs.</span><span class="sxs-lookup"><span data-stu-id="397b2-106">These categories are used to register and enumerate MFTs.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="397b2-107">Constante</span><span class="sxs-lookup"><span data-stu-id="397b2-107">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="397b2-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="397b2-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_DECODER"></span><span id="mft_category_audio_decoder"></span><dl> <span data-ttu-id="397b2-109"><dt><strong>MFT_CATEGORY_AUDIO_DECODER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="397b2-109"><dt><strong>MFT_CATEGORY_AUDIO_DECODER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="397b2-110">Decodificadores de áudio.</span><span class="sxs-lookup"><span data-stu-id="397b2-110">Audio decoders.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_EFFECT"></span><span id="mft_category_audio_effect"></span><dl> <span data-ttu-id="397b2-111"><dt><strong>MFT_CATEGORY_AUDIO_EFFECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="397b2-111"><dt><strong>MFT_CATEGORY_AUDIO_EFFECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="397b2-112">Efeitos de áudio.</span><span class="sxs-lookup"><span data-stu-id="397b2-112">Audio effects.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_ENCODER"></span><span id="mft_category_audio_encoder"></span><dl> <span data-ttu-id="397b2-113"><dt><strong>MFT_CATEGORY_AUDIO_ENCODER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="397b2-113"><dt><strong>MFT_CATEGORY_AUDIO_ENCODER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="397b2-114">Codificadores de áudio.</span><span class="sxs-lookup"><span data-stu-id="397b2-114">Audio encoders.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_DEMULTIPLEXER"></span><span id="mft_category_demultiplexer"></span><dl> <span data-ttu-id="397b2-115"><dt><strong>MFT_CATEGORY_DEMULTIPLEXER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="397b2-115"><dt><strong>MFT_CATEGORY_DEMULTIPLEXER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="397b2-116">Demultiplexadores.</span><span class="sxs-lookup"><span data-stu-id="397b2-116">Demultiplexers.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_MULTIPLEXER"></span><span id="mft_category_multiplexer"></span><dl> <span data-ttu-id="397b2-117"><dt><strong>MFT_CATEGORY_MULTIPLEXER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="397b2-117"><dt><strong>MFT_CATEGORY_MULTIPLEXER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="397b2-118">Multiplexadores.</span><span class="sxs-lookup"><span data-stu-id="397b2-118">Multiplexers.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="397b2-119">No Windows Vista, o pipeline Media Foundation não dá suporte a MFTs com mais de uma entrada.</span><span class="sxs-lookup"><span data-stu-id="397b2-119">In Windows Vista, the Media Foundation pipeline does not support MFTs with more than one input.</span></span> <span data-ttu-id="397b2-120">Há suporte para MFTs de várias entradas no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="397b2-120">Multiple-input MFTs are supported in Windows 7.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_OTHER"></span><span id="mft_category_other"></span><dl> <span data-ttu-id="397b2-121"><dt><strong>MFT_CATEGORY_OTHER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="397b2-121"><dt><strong>MFT_CATEGORY_OTHER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="397b2-122">MFTs diversos.</span><span class="sxs-lookup"><span data-stu-id="397b2-122">Miscellaneous MFTs.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_DECODER"></span><span id="mft_category_video_decoder"></span><dl> <span data-ttu-id="397b2-123"><dt><strong>MFT_CATEGORY_VIDEO_DECODER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="397b2-123"><dt><strong>MFT_CATEGORY_VIDEO_DECODER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="397b2-124">Decodificadores de vídeo.</span><span class="sxs-lookup"><span data-stu-id="397b2-124">Video decoders.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_EFFECT"></span><span id="mft_category_video_effect"></span><dl> <span data-ttu-id="397b2-125"><dt><strong>MFT_CATEGORY_VIDEO_EFFECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="397b2-125"><dt><strong>MFT_CATEGORY_VIDEO_EFFECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="397b2-126">Efeitos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="397b2-126">Video effects.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_RENDERER_EFFECT"></span><span id="mft_category_video_renderer_effect"></span><dl> <span data-ttu-id="397b2-127"><dt><strong>MFT_CATEGORY_VIDEO_RENDERER_EFFECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="397b2-127"><dt><strong>MFT_CATEGORY_VIDEO_RENDERER_EFFECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="397b2-128">Efeitos do processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="397b2-128">Video renderer effects.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_ENCODER"></span><span id="mft_category_video_encoder"></span><dl> <span data-ttu-id="397b2-129"><dt><strong>MFT_CATEGORY_VIDEO_ENCODER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="397b2-129"><dt><strong>MFT_CATEGORY_VIDEO_ENCODER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="397b2-130">Codificadores de vídeo.</span><span class="sxs-lookup"><span data-stu-id="397b2-130">Video encoders.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_PROCESSOR"></span><span id="mft_category_video_processor"></span><dl> <span data-ttu-id="397b2-131"><dt><strong>MFT_CATEGORY_VIDEO_PROCESSOR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="397b2-131"><dt><strong>MFT_CATEGORY_VIDEO_PROCESSOR</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="397b2-132">Introduzido no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="397b2-132">Introduced in Windows 7.</span></span>
</blockquote>
<br/> <span data-ttu-id="397b2-133">Processadores de vídeo.</span><span class="sxs-lookup"><span data-stu-id="397b2-133">Video processors.</span></span> <br/> <span data-ttu-id="397b2-134">Essa categoria é limitada a MFTs que executam conversões de formato em vídeo descompactado, incluindo conversões de espaço de cor.</span><span class="sxs-lookup"><span data-stu-id="397b2-134">This category is limited to MFTs that perform format conversions on uncompressed video, including color-space conversions.</span></span> <span data-ttu-id="397b2-135">Para efeitos de vídeo que modificam a aparência da imagem (como um efeito de desfoque ou uma transformação de cor para escala de cinza), use a categoria <strong>MFT_CATEGORY_VIDEO_EFFECT</strong> .</span><span class="sxs-lookup"><span data-stu-id="397b2-135">For video effects that modify the appearance of the image (such as a blur effect or a color-to-grayscale transform), use the <strong>MFT_CATEGORY_VIDEO_EFFECT</strong> category.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="397b2-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="397b2-136">Requirements</span></span>



| <span data-ttu-id="397b2-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="397b2-137">Requirement</span></span> | <span data-ttu-id="397b2-138">Valor</span><span class="sxs-lookup"><span data-stu-id="397b2-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="397b2-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="397b2-139">Minimum supported client</span></span><br/> | <span data-ttu-id="397b2-140">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="397b2-140">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="397b2-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="397b2-141">Minimum supported server</span></span><br/> | <span data-ttu-id="397b2-142">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="397b2-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="397b2-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="397b2-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="397b2-144"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="397b2-144"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="397b2-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="397b2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="397b2-146">Media Foundation constantes</span><span class="sxs-lookup"><span data-stu-id="397b2-146">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> <dt>

[<span data-ttu-id="397b2-147">Transformações de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="397b2-147">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="397b2-148">**MFTEnum**</span><span class="sxs-lookup"><span data-stu-id="397b2-148">**MFTEnum**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftenum)
</dt> <dt>

[<span data-ttu-id="397b2-149">**MFTEnumEx**</span><span class="sxs-lookup"><span data-stu-id="397b2-149">**MFTEnumEx**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> <dt>

[<span data-ttu-id="397b2-150">**MFTRegister**</span><span class="sxs-lookup"><span data-stu-id="397b2-150">**MFTRegister**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftregister)
</dt> </dl>

 

 




