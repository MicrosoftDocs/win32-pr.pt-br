---
description: Converte um fluxo de vídeo entre formatos de cor.
ms.assetid: 1c15dc2b-0e69-4d16-af02-8056a1eb2c5c
title: Conversor de cores DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a8418d6eeeffcf83a38452b19f18a6baa60bcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457221"
---
# <a name="color-converter-dsp"></a><span data-ttu-id="4c77e-103">DSP de conversor de cores</span><span class="sxs-lookup"><span data-stu-id="4c77e-103">Color Converter DSP</span></span>

<span data-ttu-id="4c77e-104">Converte um fluxo de vídeo entre formatos de cor.</span><span class="sxs-lookup"><span data-stu-id="4c77e-104">Converts a video stream between color formats.</span></span>

## <a name="clsid"></a><span data-ttu-id="4c77e-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="4c77e-105">CLSID</span></span>

<span data-ttu-id="4c77e-106">\_CCOLORCONVERTDMO CLSID</span><span class="sxs-lookup"><span data-stu-id="4c77e-106">CLSID\_CColorConvertDMO</span></span>

## <a name="interfaces"></a><span data-ttu-id="4c77e-107">Interfaces</span><span class="sxs-lookup"><span data-stu-id="4c77e-107">Interfaces</span></span>

-   [<span data-ttu-id="4c77e-108">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="4c77e-108">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [<span data-ttu-id="4c77e-109">**IMFRealTimeClient**</span><span class="sxs-lookup"><span data-stu-id="4c77e-109">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="4c77e-110">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="4c77e-110">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="4c77e-111">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="4c77e-111">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [<span data-ttu-id="4c77e-112">IWMColorConvProps</span><span class="sxs-lookup"><span data-stu-id="4c77e-112">IWMColorConvProps</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcolorconvprops)

## <a name="input-formats"></a><span data-ttu-id="4c77e-113">Formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="4c77e-113">Input Formats</span></span>

-   <span data-ttu-id="4c77e-114">RGB 24</span><span class="sxs-lookup"><span data-stu-id="4c77e-114">RGB 24</span></span>
-   <span data-ttu-id="4c77e-115">RGB 32</span><span class="sxs-lookup"><span data-stu-id="4c77e-115">RGB 32</span></span>
-   <span data-ttu-id="4c77e-116">RGB 555</span><span class="sxs-lookup"><span data-stu-id="4c77e-116">RGB 555</span></span>
-   <span data-ttu-id="4c77e-117">RGB 565</span><span class="sxs-lookup"><span data-stu-id="4c77e-117">RGB 565</span></span>
-   <span data-ttu-id="4c77e-118">RGB 8</span><span class="sxs-lookup"><span data-stu-id="4c77e-118">RGB 8</span></span>
-   <span data-ttu-id="4c77e-119">AYUV</span><span class="sxs-lookup"><span data-stu-id="4c77e-119">AYUV</span></span>
-   <span data-ttu-id="4c77e-120">I420</span><span class="sxs-lookup"><span data-stu-id="4c77e-120">I420</span></span>
-   <span data-ttu-id="4c77e-121">IYUV</span><span class="sxs-lookup"><span data-stu-id="4c77e-121">IYUV</span></span>
-   <span data-ttu-id="4c77e-122">NV11</span><span class="sxs-lookup"><span data-stu-id="4c77e-122">NV11</span></span>
-   <span data-ttu-id="4c77e-123">NV12</span><span class="sxs-lookup"><span data-stu-id="4c77e-123">NV12</span></span>
-   <span data-ttu-id="4c77e-124">UYVY</span><span class="sxs-lookup"><span data-stu-id="4c77e-124">UYVY</span></span>
-   <span data-ttu-id="4c77e-125">V216</span><span class="sxs-lookup"><span data-stu-id="4c77e-125">V216</span></span>
-   <span data-ttu-id="4c77e-126">V410</span><span class="sxs-lookup"><span data-stu-id="4c77e-126">V410</span></span>
-   <span data-ttu-id="4c77e-127">Y41P</span><span class="sxs-lookup"><span data-stu-id="4c77e-127">Y41P</span></span>
-   <span data-ttu-id="4c77e-128">Y41T</span><span class="sxs-lookup"><span data-stu-id="4c77e-128">Y41T</span></span>
-   <span data-ttu-id="4c77e-129">Y42T</span><span class="sxs-lookup"><span data-stu-id="4c77e-129">Y42T</span></span>
-   <span data-ttu-id="4c77e-130">YUY2</span><span class="sxs-lookup"><span data-stu-id="4c77e-130">YUY2</span></span>
-   <span data-ttu-id="4c77e-131">YV12</span><span class="sxs-lookup"><span data-stu-id="4c77e-131">YV12</span></span>
-   <span data-ttu-id="4c77e-132">YVU9</span><span class="sxs-lookup"><span data-stu-id="4c77e-132">YVU9</span></span>
-   <span data-ttu-id="4c77e-133">YVYU</span><span class="sxs-lookup"><span data-stu-id="4c77e-133">YVYU</span></span>

## <a name="output-formats"></a><span data-ttu-id="4c77e-134">Formatos de saída</span><span class="sxs-lookup"><span data-stu-id="4c77e-134">Output Formats</span></span>

-   <span data-ttu-id="4c77e-135">RGB 24</span><span class="sxs-lookup"><span data-stu-id="4c77e-135">RGB 24</span></span>
-   <span data-ttu-id="4c77e-136">RGB 32</span><span class="sxs-lookup"><span data-stu-id="4c77e-136">RGB 32</span></span>
-   <span data-ttu-id="4c77e-137">RGB 555</span><span class="sxs-lookup"><span data-stu-id="4c77e-137">RGB 555</span></span>
-   <span data-ttu-id="4c77e-138">RGB 565</span><span class="sxs-lookup"><span data-stu-id="4c77e-138">RGB 565</span></span>
-   <span data-ttu-id="4c77e-139">RGB 8</span><span class="sxs-lookup"><span data-stu-id="4c77e-139">RGB 8</span></span>
-   <span data-ttu-id="4c77e-140">AYUV</span><span class="sxs-lookup"><span data-stu-id="4c77e-140">AYUV</span></span>
-   <span data-ttu-id="4c77e-141">I420</span><span class="sxs-lookup"><span data-stu-id="4c77e-141">I420</span></span>
-   <span data-ttu-id="4c77e-142">IYUV</span><span class="sxs-lookup"><span data-stu-id="4c77e-142">IYUV</span></span>
-   <span data-ttu-id="4c77e-143">NV11</span><span class="sxs-lookup"><span data-stu-id="4c77e-143">NV11</span></span>
-   <span data-ttu-id="4c77e-144">NV12</span><span class="sxs-lookup"><span data-stu-id="4c77e-144">NV12</span></span>
-   <span data-ttu-id="4c77e-145">UYVY</span><span class="sxs-lookup"><span data-stu-id="4c77e-145">UYVY</span></span>
-   <span data-ttu-id="4c77e-146">V216</span><span class="sxs-lookup"><span data-stu-id="4c77e-146">V216</span></span>
-   <span data-ttu-id="4c77e-147">V410</span><span class="sxs-lookup"><span data-stu-id="4c77e-147">V410</span></span>
-   <span data-ttu-id="4c77e-148">YUY2</span><span class="sxs-lookup"><span data-stu-id="4c77e-148">YUY2</span></span>
-   <span data-ttu-id="4c77e-149">YV12</span><span class="sxs-lookup"><span data-stu-id="4c77e-149">YV12</span></span>
-   <span data-ttu-id="4c77e-150">YVYU</span><span class="sxs-lookup"><span data-stu-id="4c77e-150">YVYU</span></span>

## <a name="properties"></a><span data-ttu-id="4c77e-151">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4c77e-151">Properties</span></span>

-   [<span data-ttu-id="4c77e-152">MFPKEY \_ COLORCONV \_ SRCLEFT</span><span class="sxs-lookup"><span data-stu-id="4c77e-152">MFPKEY\_COLORCONV\_SRCLEFT</span></span>](mfpkey-colorconv-srcleft.md)
-   [<span data-ttu-id="4c77e-153">MFPKEY \_ COLORCONV \_ SRCTOP</span><span class="sxs-lookup"><span data-stu-id="4c77e-153">MFPKEY\_COLORCONV\_SRCTOP</span></span>](mfpkey-colorconv-srctop.md)
-   [<span data-ttu-id="4c77e-154">MFPKEY \_ COLORCONV \_ DSTLEFT</span><span class="sxs-lookup"><span data-stu-id="4c77e-154">MFPKEY\_COLORCONV\_DSTLEFT</span></span>](mfpkey-colorconv-dstleft.md)
-   [<span data-ttu-id="4c77e-155">MFPKEY \_ COLORCONV \_ DSTTOP</span><span class="sxs-lookup"><span data-stu-id="4c77e-155">MFPKEY\_COLORCONV\_DSTTOP</span></span>](mfpkey-colorconv-dsttop.md)
-   [<span data-ttu-id="4c77e-156">\_largura de COLORCONV MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="4c77e-156">MFPKEY\_COLORCONV\_WIDTH</span></span>](mfpkey-colorconv-width.md)
-   [<span data-ttu-id="4c77e-157">\_altura de COLORCONV MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="4c77e-157">MFPKEY\_COLORCONV\_HEIGHT</span></span>](mfpkey-colorconv-height.md)
-   [<span data-ttu-id="4c77e-158">\_modo de COLORCONV MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="4c77e-158">MFPKEY\_COLORCONV\_MODE</span></span>](mfpkey-colorconv-mode.md)

## <a name="remarks"></a><span data-ttu-id="4c77e-159">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c77e-159">Remarks</span></span>

<span data-ttu-id="4c77e-160">O DSP do conversor de cores é implementado como um objeto COM que pode atuar como um objeto DirectXMedia (DMO) ou uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="4c77e-160">The Color Converter DSP is implemented as a COM object that can act as a DirectXMedia Object (DMO) or a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="4c77e-161">O objeto tem um único identificador de classe (CLSID), independentemente de agir como um DMO ou uma MFT.</span><span class="sxs-lookup"><span data-stu-id="4c77e-161">The object has a single class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span> <span data-ttu-id="4c77e-162">Para obter informações sobre quando um DSP atua como um DMO ou uma MFT, consulte [processadores de sinais digitais](windowsmediadigitalsignalprocessors.md).</span><span class="sxs-lookup"><span data-stu-id="4c77e-162">For information about when a DSP acts as a DMO or an MFT, see [Digital Signal Processors](windowsmediadigitalsignalprocessors.md).</span></span>

<span data-ttu-id="4c77e-163">Os identificadores globalmente exclusivos (GUIDs) para subtipos de mídia RGB diferem dependendo se um DSP está agindo como um DMO ou uma MFT.</span><span class="sxs-lookup"><span data-stu-id="4c77e-163">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="4c77e-164">Os GUIDs para subtipos de mídia não RGB são os mesmos, independentemente de um DSP estar agindo como um DMO ou um MFT.</span><span class="sxs-lookup"><span data-stu-id="4c77e-164">The GUIDs for non-RGB media subtypes are the same, regardless of whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="4c77e-165">Para obter informações sobre os GUIDs que representam subtipos de mídia, consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="4c77e-165">For information about the GUIDs that represent media subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="4c77e-166">Por padrão, esse DSP copia a imagem de origem inteira para o buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="4c77e-166">By default, this DSP copies the entire source image to the output buffer.</span></span> <span data-ttu-id="4c77e-167">Opcionalmente, você pode especificar retângulos de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="4c77e-167">Optionally, you can specify source and destination rectangles.</span></span> <span data-ttu-id="4c77e-168">O DSP copia a parte da imagem de origem definida pelo retângulo de origem e a grava no retângulo de destino no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="4c77e-168">The DSP copies the portion of the source image defined by source rectangle, and writes it into the destination rectangle on the output buffer.</span></span> <span data-ttu-id="4c77e-169">O DSP não executa nenhum dimensionamento; os retângulos de origem e de destino devem ter o mesmo tamanho.</span><span class="sxs-lookup"><span data-stu-id="4c77e-169">The DSP does not perform any scaling; the source and destination rectangles must be the same size.</span></span> <span data-ttu-id="4c77e-170">Os retângulos de origem e de destino não podem exceder os limites do quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4c77e-170">The source and destination rectangles cannot exceed the boundaries of the video frame.</span></span>

<span data-ttu-id="4c77e-171">Todas as propriedades, exceto [**o \_ \_ modo MFPKEY COLORCONV**](mfpkey-colorconv-mode.md) , devem ser definidas em um grupo.</span><span class="sxs-lookup"><span data-stu-id="4c77e-171">All of the properties except [**MFPKEY\_COLORCONV\_MODE**](mfpkey-colorconv-mode.md) must be set in a group.</span></span> <span data-ttu-id="4c77e-172">Se você definir qualquer uma dessas propriedades, deverá definir todas as outras.</span><span class="sxs-lookup"><span data-stu-id="4c77e-172">If you set any of these properties, you must set all of the others.</span></span> <span data-ttu-id="4c77e-173">Caso contrário, os retângulos de origem e de destino podem ser inválidos. nesse caso, os métodos [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) e [**IMediaObject::P Rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) retornarão **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="4c77e-173">Otherwise, the source and destination rectangles might be invalid, in which case both the [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) and [**IMediaObject::ProcessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) methods will return **E\_INVALIDARG**.</span></span>

<span data-ttu-id="4c77e-174">O conversor de cores não oferece suporte a todas as combinações de formato de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="4c77e-174">The color converter does not support every combination of input format and output format.</span></span> <span data-ttu-id="4c77e-175">Normalmente, você deve definir o formato de mídia que você conhece, entrada ou saída e, em seguida, enumerar os formatos disponíveis no fluxo oposto.</span><span class="sxs-lookup"><span data-stu-id="4c77e-175">Usually, you should set the media format that you know, either input or output, and then enumerate the available formats on the opposite stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c77e-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c77e-176">Requirements</span></span>



| <span data-ttu-id="4c77e-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c77e-177">Requirement</span></span> | <span data-ttu-id="4c77e-178">Valor</span><span class="sxs-lookup"><span data-stu-id="4c77e-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c77e-179">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c77e-179">Minimum supported client</span></span><br/> | <span data-ttu-id="4c77e-180">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4c77e-180">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4c77e-181">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c77e-181">Minimum supported server</span></span><br/> | <span data-ttu-id="4c77e-182">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4c77e-182">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4c77e-183">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4c77e-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c77e-184"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c77e-184"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="4c77e-185">DLL</span><span class="sxs-lookup"><span data-stu-id="4c77e-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c77e-186"><dt>Colorcnv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c77e-186"><dt>Colorcnv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c77e-187">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c77e-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c77e-188">Processadores de sinais digitais</span><span class="sxs-lookup"><span data-stu-id="4c77e-188">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
