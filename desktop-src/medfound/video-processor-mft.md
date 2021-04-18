---
description: O MFT do processador de vídeo é uma Microsoft Media Foundation de transformação (MFT) que executa conversão de colorspace, redimensionamento de vídeo, desentrelaçamento, conversão de taxa de quadros, rotação, corte, desempacotamento de exibição à esquerda e à direita e espelhamento.
ms.assetid: 1476995A-9692-4B08-8EF7-7DB6321BEC24
title: MFT do processador de vídeo (Camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53783b42073414e4dc440546698bf295b404dcc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791604"
---
# <a name="video-processor-mft"></a><span data-ttu-id="ae1cc-103">MFT do processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ae1cc-103">Video Processor MFT</span></span>

<span data-ttu-id="ae1cc-104">O MFT do processador de vídeo é uma Microsoft Media Foundation de transformação (MFT) que executa conversão de colorspace, redimensionamento de vídeo, desentrelaçamento, conversão de taxa de quadros, rotação, corte, desempacotamento de exibição à esquerda e à direita e espelhamento.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-104">The video processor MFT is a Microsoft Media Foundation transform (MFT) that performs colorspace conversion, video resizing, deinterlacing, frame rate conversion, rotation, cropping, spatial left and right view unpacking, and mirroring.</span></span>

## <a name="clsid"></a><span data-ttu-id="ae1cc-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="ae1cc-105">CLSID</span></span>

<span data-ttu-id="ae1cc-106">\_VIDEOPROCESSORMFT CLSID</span><span class="sxs-lookup"><span data-stu-id="ae1cc-106">CLSID\_VideoProcessorMFT</span></span>

## <a name="interfaces"></a><span data-ttu-id="ae1cc-107">Interfaces</span><span class="sxs-lookup"><span data-stu-id="ae1cc-107">Interfaces</span></span>

-   [<span data-ttu-id="ae1cc-108">**IMFRealTimeClientEx**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-108">**IMFRealTimeClientEx**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)
-   [<span data-ttu-id="ae1cc-109">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-109">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="ae1cc-110">**IMFVideoProcessorControl**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-110">**IMFVideoProcessorControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol)

## <a name="input-formats"></a><span data-ttu-id="ae1cc-111">Formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="ae1cc-111">Input Formats</span></span>

-   <span data-ttu-id="ae1cc-112">**MFVideoFormat \_ ARGB32**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-112">**MFVideoFormat\_ARGB32**</span></span>
-   <span data-ttu-id="ae1cc-113">**MFVideoFormat \_ AYUV**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-113">**MFVideoFormat\_AYUV**</span></span>
-   <span data-ttu-id="ae1cc-114">**MFVideoFormat \_ I420**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-114">**MFVideoFormat\_I420**</span></span>
-   <span data-ttu-id="ae1cc-115">**MFVideoFormat \_ IYUV**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-115">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="ae1cc-116">**MFVideoFormat \_ NV11**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-116">**MFVideoFormat\_NV11**</span></span>
-   <span data-ttu-id="ae1cc-117">**MFVideoFormat \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-117">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="ae1cc-118">**MFVideoFormat \_ RGB24**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-118">**MFVideoFormat\_RGB24**</span></span>
-   <span data-ttu-id="ae1cc-119">**MFVideoFormat \_ RGB32**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-119">**MFVideoFormat\_RGB32**</span></span>
-   <span data-ttu-id="ae1cc-120">**MFVideoFormat \_ RGB555**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-120">**MFVideoFormat\_RGB555**</span></span>
-   <span data-ttu-id="ae1cc-121">**MFVideoFormat \_ RGB565**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-121">**MFVideoFormat\_RGB565**</span></span>
-   <span data-ttu-id="ae1cc-122">**MFVideoFormat \_ RGB8**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-122">**MFVideoFormat\_RGB8**</span></span>
-   <span data-ttu-id="ae1cc-123">**MFVideoFormat \_ UYVY**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-123">**MFVideoFormat\_UYVY**</span></span>
-   <span data-ttu-id="ae1cc-124">**MFVideoFormat \_ v410**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-124">**MFVideoFormat\_v410**</span></span>
-   <span data-ttu-id="ae1cc-125">**MFVideoFormat \_ Y216**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-125">**MFVideoFormat\_Y216**</span></span>
-   <span data-ttu-id="ae1cc-126">**MFVideoFormat \_ Y41P**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-126">**MFVideoFormat\_Y41P**</span></span>
-   <span data-ttu-id="ae1cc-127">**MFVideoFormat \_ Y41T**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-127">**MFVideoFormat\_Y41T**</span></span>
-   <span data-ttu-id="ae1cc-128">**MFVideoFormat \_ Y42T**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-128">**MFVideoFormat\_Y42T**</span></span>
-   <span data-ttu-id="ae1cc-129">**MFVideoFormat \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-129">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="ae1cc-130">**MFVideoFormat \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-130">**MFVideoFormat\_YV12**</span></span>
-   <span data-ttu-id="ae1cc-131">**MFVideoFormat \_ YVYU**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-131">**MFVideoFormat\_YVYU**</span></span>

## <a name="output-formats"></a><span data-ttu-id="ae1cc-132">Formatos de saída</span><span class="sxs-lookup"><span data-stu-id="ae1cc-132">Output Formats</span></span>

-   <span data-ttu-id="ae1cc-133">**MFVideoFormat \_ ARGB32**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-133">**MFVideoFormat\_ARGB32**</span></span>
-   <span data-ttu-id="ae1cc-134">**MFVideoFormat \_ AYUV**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-134">**MFVideoFormat\_AYUV**</span></span>
-   <span data-ttu-id="ae1cc-135">**MFVideoFormat \_ I420**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-135">**MFVideoFormat\_I420**</span></span>
-   <span data-ttu-id="ae1cc-136">**MFVideoFormat \_ IYUV**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-136">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="ae1cc-137">**MFVideoFormat \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-137">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="ae1cc-138">**MFVideoFormat \_ RGB24**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-138">**MFVideoFormat\_RGB24**</span></span>
-   <span data-ttu-id="ae1cc-139">**MFVideoFormat \_ RGB32**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-139">**MFVideoFormat\_RGB32**</span></span>
-   <span data-ttu-id="ae1cc-140">**MFVideoFormat \_ RGB555**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-140">**MFVideoFormat\_RGB555**</span></span>
-   <span data-ttu-id="ae1cc-141">**MFVideoFormat \_ RGB565**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-141">**MFVideoFormat\_RGB565**</span></span>
-   <span data-ttu-id="ae1cc-142">**MFVideoFormat \_ UYVY**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-142">**MFVideoFormat\_UYVY**</span></span>
-   <span data-ttu-id="ae1cc-143">**MFVideoFormat \_ Y216**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-143">**MFVideoFormat\_Y216**</span></span>
-   <span data-ttu-id="ae1cc-144">**MFVideoFormat \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-144">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="ae1cc-145">**MFVideoFormat \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="ae1cc-145">**MFVideoFormat\_YV12**</span></span>

<span data-ttu-id="ae1cc-146">Nem todas as combinações de formatos de entrada e saída têm suporte.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-146">Not every combination of input and output formats is supported.</span></span> <span data-ttu-id="ae1cc-147">Para testar se há suporte para uma conversão, defina o tipo de entrada e, em seguida, chame [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span><span class="sxs-lookup"><span data-stu-id="ae1cc-147">To test whether a conversion is supported, set the input type and then call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span></span>

<span data-ttu-id="ae1cc-148">Para obter mais informações sobre esses formatos, consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="ae1cc-148">For more information about these formats, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ae1cc-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae1cc-149">Remarks</span></span>

<span data-ttu-id="ae1cc-150">Uma instância do processador de vídeo pode ser criada de uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="ae1cc-150">An instance of the video processor can be created in one of the following ways:</span></span>

-   <span data-ttu-id="ae1cc-151">Chamando [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="ae1cc-151">By calling [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span> <span data-ttu-id="ae1cc-152">O processador de vídeo é registrado sob a categoria **MFT do \_ \_ \_ processador de vídeo** categoria.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-152">The video processor is registered under the **MFT\_CATEGORY\_VIDEO\_PROCESSOR** category.</span></span>
-   <span data-ttu-id="ae1cc-153">Chamando a função COM **CoCreateInstance** passando-a para o CLSID **CLSID \_ VideoProcessorMFT**.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-153">By calling the COM function **CoCreateInstance** passing it the CLSID **CLSID\_VideoProcessorMFT**.</span></span>

<span data-ttu-id="ae1cc-154">Os comentários a seguir pertencem ao trabalho com retângulos de origem e retângulos de destino na **MFT do processador de vídeo**.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-154">The following remarks pertain to working with source rectangles and destination rectangles in the **Video Processor MFT**.</span></span> <span data-ttu-id="ae1cc-155">Os retângulos de origem e de destino são definidos com [**IMFVideoProcessorControl:: SetDestinationRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setdestinationrectangle) e [**SetSourceRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setsourcerectangle) e algumas vezes com [**IMFMediaEngineEx:: UpdateVideoStream**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-updatevideostream).</span><span class="sxs-lookup"><span data-stu-id="ae1cc-155">Source and destination rectangles are set with [**IMFVideoProcessorControl::SetDestinationRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setdestinationrectangle) and [**SetSourceRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setsourcerectangle) and some times with [**IMFMediaEngineEx::UpdateVideoStream**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-updatevideostream).</span></span>

-   <span data-ttu-id="ae1cc-156">O retângulo de origem deve ser alinhado e arredondado para corresponder aos requisitos do formato de cor do quadro inserido no processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-156">The source rectangle should be aligned and rounded to match the requirements of the color format of the frame inputted to the video processor.</span></span> <span data-ttu-id="ae1cc-157">Isso é importante porque formatos como 420 e 422 têm requisitos sobre as dimensões e os deslocamentos que podem ser criados e acessados.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-157">This is important because formats like 420 and 422 have requirements about the dimensions and offsets that can be created and accessed.</span></span> <span data-ttu-id="ae1cc-158">Por exemplo, um retângulo de origem de {1, 0, 319, 240} (esquerda, superior, direita, inferior) será arredondado para {2, 0, 320, 240} quando o formato de entrada for 420.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-158">For example, a source rectangle of {1, 0, 319, 240} (left, top, right, bottom) will be rounded to {2, 0, 320, 240} when the input format is 420.</span></span>
-   <span data-ttu-id="ae1cc-159">O destino e o retângulo de origem sempre serão clamped para caber dentro de seus respectivos quadros — o retângulo de origem para o quadro de origem e o retângulo de destino para o quadro de destino.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-159">Both the destination and source rectangle will always be clamped to fit inside their respective frames—the source rectangle to the source frame and the destination rectangle to the destination frame.</span></span> <span data-ttu-id="ae1cc-160">Isso significa que valores negativos não são significativos — eles serão sempre clamped para 0.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-160">This means that negative values are not meaningful—they will be always clamped to 0.</span></span>
-   <span data-ttu-id="ae1cc-161">O retângulo de origem está no sistema de coordenadas do quadro de destino, menos qualquer retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-161">The source rectangle is in the destination frame's coordinate system, minus any destination rectangle.</span></span> <span data-ttu-id="ae1cc-162">Isso significa que as transformações como a rotação são "desfeitas" no retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-162">This means that transformations like rotation are "undone" on the source rectangle.</span></span> <span data-ttu-id="ae1cc-163">Portanto, você não precisa saber se o vídeo foi girado ou 3D desempacotado.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-163">Therefore, you do not need to know if the video was rotated or 3D unpacked.</span></span> <span data-ttu-id="ae1cc-164">Por exemplo, você pode desenhar um retângulo sobre a marca de vídeo, pegar as coordenadas relativas (em relação à marca de vídeo), Normalize-las (intervalo de 0 a 1) e passá-las como o retângulo de origem e elas devem funcionar conforme o esperado, mesmo se o vídeo estiver sendo girado.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-164">For example, you could draw a rectangle on top of the video tag, take the relative coordinates (relative to the video tag), normalize them (range 0 to 1) and pass them down as the source rectangle and they should work as expected, even if the video is being rotated.</span></span>

<span data-ttu-id="ae1cc-165">O processador de vídeo dá suporte ao processamento de vídeo acelerado por GPU, usando o Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-165">The video processor supports GPU-accelerated video processing, using Microsoft Direct3D 11.</span></span> <span data-ttu-id="ae1cc-166">Para obter mais informações, consulte [MF \_ SA \_ D3D11 \_ Aware](mf-sa-d3d11-aware.md).</span><span class="sxs-lookup"><span data-stu-id="ae1cc-166">For more information, see [MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md).</span></span>

### <a name="stereoscopic-video"></a><span data-ttu-id="ae1cc-167">Vídeo do estereoscópico</span><span class="sxs-lookup"><span data-stu-id="ae1cc-167">Stereoscopic Video</span></span>

<span data-ttu-id="ae1cc-168">O processador de vídeo dá suporte à operação exibir desempacotamento em quadros de vídeo 3D:</span><span class="sxs-lookup"><span data-stu-id="ae1cc-168">The video processor supports the view unpacking operation on 3D video frames:</span></span>

<span data-ttu-id="ae1cc-169">Se o quadro de entrada contiver dois modos de exibição compactados no mesmo quadro, o processador de vídeo poderá dividir as exibições em buffers separados ou extrair a exibição de base e descartar a segunda exibição.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-169">If the input frame contains two views packed in the same frame, the video processor can split the views into separate buffers, or extract the base view and discard the second view.</span></span> <span data-ttu-id="ae1cc-170">Para habilitar o desempacotamento de View, defina o atributo de [ \_ \_ \_ saída MF Enable 3DVIDEO](mf-enable-3dvideo-output.md) para **MF3DVideoOutputType \_ estéreo** ou **MF3DVideoOutputType \_ BaseView**.</span><span class="sxs-lookup"><span data-stu-id="ae1cc-170">To enable view unpacking, set the [MF\_ENABLE\_3DVIDEO\_OUTPUT](mf-enable-3dvideo-output.md) attribute to **MF3DVideoOutputType\_Stereo** or **MF3DVideoOutputType\_BaseView**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae1cc-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae1cc-171">Requirements</span></span>



| <span data-ttu-id="ae1cc-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae1cc-172">Requirement</span></span> | <span data-ttu-id="ae1cc-173">Valor</span><span class="sxs-lookup"><span data-stu-id="ae1cc-173">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae1cc-174">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ae1cc-174">Header</span></span><br/> | <dl> <span data-ttu-id="ae1cc-175"><dt>Camerauicontrol. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae1cc-175"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae1cc-176">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae1cc-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae1cc-177">Processadores de sinais digitais</span><span class="sxs-lookup"><span data-stu-id="ae1cc-177">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




