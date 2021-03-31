---
title: Transições de imagem de vídeo
description: Transições de imagem de vídeo
ms.assetid: 201ddbfb-567b-4893-b754-569f1e7d8466
keywords:
- SDK do Windows Media Format, transições de imagem de vídeo
- ASF (Advanced Systems Format), transições de imagem de vídeo
- ASF (formato de sistemas avançados), transições de imagem de vídeo
- transições de imagem de vídeo
- Codec do Windows Media Video 9 Image v2
- codecs, imagem do Windows Media Video 9 Image v2
- fluxos de vídeo, Windows Media Video 9 Image v2 codec
- fluxos de vídeo, transições de imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbfd02628a78196a73750c2c0ff6b9e9c3d6729c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005326"
---
# <a name="video-image-transitions"></a><span data-ttu-id="65994-111">Transições de imagem de vídeo</span><span class="sxs-lookup"><span data-stu-id="65994-111">Video Image Transitions</span></span>

<span data-ttu-id="65994-112">O codec Windows Media Video 9 Image v2 anima uma série de imagens, resultando em um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="65994-112">The Windows Media Video 9 Image v2 codec animates a series of images, resulting in a video stream.</span></span> <span data-ttu-id="65994-113">O codec pode manipular duas imagens ao mesmo tempo, reuni-las e criar uma transição de uma para a outra de acordo com a configuração que você fornece.</span><span class="sxs-lookup"><span data-stu-id="65994-113">The codec can manipulate two images at once, blending them together and creating a transition from one to the other according to the configuration you supply.</span></span> <span data-ttu-id="65994-114">Esta seção descreve as transições com suporte e os parâmetros necessários.</span><span class="sxs-lookup"><span data-stu-id="65994-114">This section describes the supported transitions and the parameters they require.</span></span>

<span data-ttu-id="65994-115">As transições são listadas na tabela a seguir por seus identificadores globais.</span><span class="sxs-lookup"><span data-stu-id="65994-115">The transitions are listed in the following table by their global identifiers.</span></span>



| <span data-ttu-id="65994-116">Identificador de transição</span><span class="sxs-lookup"><span data-stu-id="65994-116">Transition identifier</span></span>                                                                           | <span data-ttu-id="65994-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="65994-117">Description</span></span>                                                                                                                                  |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65994-118">**gravata WMT de \_ transição de VIDEOIMAGE \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="65994-118">**WMT\_VIDEOIMAGE\_TRANSITION\_BOW\_TIE**</span></span>](wmt-videoimage-transition-bow-tie.md)              | <span data-ttu-id="65994-119">A nova imagem é revelada em um conjunto de triângulos nos lados opostos do quadro.</span><span class="sxs-lookup"><span data-stu-id="65994-119">New image is revealed in a set of triangles on opposite sides of the frame.</span></span>                                                                  |
| [<span data-ttu-id="65994-120">**\_círculo de \_ transição de VIDEOIMAGE WMT \_**</span><span class="sxs-lookup"><span data-stu-id="65994-120">**WMT\_VIDEOIMAGE\_TRANSITION\_CIRCLE**</span></span>](wmt-videoimage-transition-circle.md)                 | <span data-ttu-id="65994-121">A nova imagem é revelada em um círculo.</span><span class="sxs-lookup"><span data-stu-id="65994-121">New image is revealed in a circle.</span></span>                                                                                                           |
| [<span data-ttu-id="65994-122">**\_ \_ \_ esmaecimento cruzado de transição WMT VIDEOIMAGE \_**</span><span class="sxs-lookup"><span data-stu-id="65994-122">**WMT\_VIDEOIMAGE\_TRANSITION\_CROSS\_FADE**</span></span>](wmt-videoimage-transition-cross-fade.md)        | <span data-ttu-id="65994-123">Sem transição especial, os coeficientes de Blend das duas imagens determinam o esmaecimento cruzado (dissolução).</span><span class="sxs-lookup"><span data-stu-id="65994-123">No special transition, the blend coefficients of the two images determine the cross-fade (dissolve).</span></span>                                         |
| [<span data-ttu-id="65994-124">**\_diagonal de \_ transição WMT VIDEOIMAGE \_**</span><span class="sxs-lookup"><span data-stu-id="65994-124">**WMT\_VIDEOIMAGE\_TRANSITION\_DIAGONAL**</span></span>](wmt-videoimage-transition-diagonal.md)             | <span data-ttu-id="65994-125">A nova imagem é revelada ao longo de uma linha diagonal originada em um canto do quadro.</span><span class="sxs-lookup"><span data-stu-id="65994-125">New image is revealed along a diagonal line originating in one corner of the frame.</span></span>                                                          |
| [<span data-ttu-id="65994-126">**\_diamante de \_ transição WMT VIDEOIMAGE \_**</span><span class="sxs-lookup"><span data-stu-id="65994-126">**WMT\_VIDEOIMAGE\_TRANSITION\_DIAMOND**</span></span>](wmt-videoimage-transition-diamond.md)               | <span data-ttu-id="65994-127">A nova imagem é revelada em um losango.</span><span class="sxs-lookup"><span data-stu-id="65994-127">New image is revealed in a diamond.</span></span>                                                                                                          |
| [<span data-ttu-id="65994-128">**WMT \_ \_ transição \_ de VIDEOIMAGE esmaecer \_ para \_ cor**</span><span class="sxs-lookup"><span data-stu-id="65994-128">**WMT\_VIDEOIMAGE\_TRANSITION\_FADE\_TO\_COLOR**</span></span>](wmt-videoimage-transition-fade-to-color.md) | <span data-ttu-id="65994-129">Desresolve da imagem para um quadro de cor sólida.</span><span class="sxs-lookup"><span data-stu-id="65994-129">Dissolves from the image to a frame of solid color.</span></span>                                                                                          |
| [<span data-ttu-id="65994-130">**transição de WMT \_ VIDEOIMAGE \_ \_ preenchida \_**</span><span class="sxs-lookup"><span data-stu-id="65994-130">**WMT\_VIDEOIMAGE\_TRANSITION\_FILLED\_V**</span></span>](wmt-videoimage-transition-filled-v.md)            | <span data-ttu-id="65994-131">A nova imagem é revelada em um triângulo proveniente de um lado do quadro.</span><span class="sxs-lookup"><span data-stu-id="65994-131">New image is revealed in a triangle originating from one side of the frame.</span></span>                                                                  |
| [<span data-ttu-id="65994-132">**Inverter WMT de \_ \_ transição VIDEOIMAGE \_**</span><span class="sxs-lookup"><span data-stu-id="65994-132">**WMT\_VIDEOIMAGE\_TRANSITION\_FLIP**</span></span>](wmt-videoimage-transition-flip.md)                     | <span data-ttu-id="65994-133">A imagem antiga é girada em um eixo y no centro do quadro.</span><span class="sxs-lookup"><span data-stu-id="65994-133">Old image is rotated on a y-axis through the center of the frame.</span></span> <span data-ttu-id="65994-134">A nova imagem é revelada como a parte traseira da imagem antiga.</span><span class="sxs-lookup"><span data-stu-id="65994-134">The new image is revealed as the back of the old image.</span></span>                    |
| [<span data-ttu-id="65994-135">**\_inserção de \_ transição WMT VIDEOIMAGE \_**</span><span class="sxs-lookup"><span data-stu-id="65994-135">**WMT\_VIDEOIMAGE\_TRANSITION\_INSET**</span></span>](wmt-videoimage-transition-inset.md)                   | <span data-ttu-id="65994-136">A nova imagem é revelada por um retângulo proveniente de um canto do quadro.</span><span class="sxs-lookup"><span data-stu-id="65994-136">New image is revealed by a rectangle originating from one corner of the frame.</span></span>                                                               |
| [<span data-ttu-id="65994-137">**\_íris de \_ transição WMT VIDEOIMAGE \_**</span><span class="sxs-lookup"><span data-stu-id="65994-137">**WMT\_VIDEOIMAGE\_TRANSITION\_IRIS**</span></span>](wmt-videoimage-transition-iris.md)                     | <span data-ttu-id="65994-138">A nova imagem é revelada ao longo de um eixo x e um eixo y.</span><span class="sxs-lookup"><span data-stu-id="65994-138">New image is revealed along an x-axis and a y-axis.</span></span>                                                                                          |
| [<span data-ttu-id="65994-139">**Roll WMT de \_ \_ página de transição VIDEOIMAGE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="65994-139">**WMT\_VIDEOIMAGE\_TRANSITION\_PAGE\_ROLL**</span></span>](wmt-videoimage-transition-page-roll.md)          | <span data-ttu-id="65994-140">A imagem antiga é transformada em um efeito de inversão de página, revelando a nova imagem abaixo.</span><span class="sxs-lookup"><span data-stu-id="65994-140">Old image is transformed in a page-flipping effect, revealing the new image underneath.</span></span>                                                      |
| [<span data-ttu-id="65994-141">**\_retângulo de \_ transição WMT VIDEOIMAGE \_**</span><span class="sxs-lookup"><span data-stu-id="65994-141">**WMT\_VIDEOIMAGE\_TRANSITION\_RECTANGLE**</span></span>](wmt-videoimage-transition-rectangle.md)           | <span data-ttu-id="65994-142">A nova imagem é revelada por um retângulo dentro do quadro.</span><span class="sxs-lookup"><span data-stu-id="65994-142">New image is revealed by a rectangle within the frame.</span></span>                                                                                       |
| [<span data-ttu-id="65994-143">**WMT \_ de \_ transição VIDEOIMAGE \_ revela**</span><span class="sxs-lookup"><span data-stu-id="65994-143">**WMT\_VIDEOIMAGE\_TRANSITION\_REVEAL**</span></span>](wmt-videoimage-transition-reveal.md)                 | <span data-ttu-id="65994-144">A nova imagem é revelada ao longo de uma linha reta originada de um lado do quadro.</span><span class="sxs-lookup"><span data-stu-id="65994-144">New image is revealed along a straight line originating from one side of the frame.</span></span>                                                          |
| [<span data-ttu-id="65994-145">**SLIDE de transição do WMT \_ VIDEOIMAGE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="65994-145">**WMT\_VIDEOIMAGE\_TRANSITION\_SLIDE**</span></span>](wmt-videoimage-transition-slide.md)                   | <span data-ttu-id="65994-146">Imagem antiga fora do quadro, revelando a nova imagem abaixo.</span><span class="sxs-lookup"><span data-stu-id="65994-146">Old image slides out of the frame, revealing the new image underneath.</span></span>                                                                       |
| [<span data-ttu-id="65994-147">**\_divisão de \_ transição WMT VIDEOIMAGE \_**</span><span class="sxs-lookup"><span data-stu-id="65994-147">**WMT\_VIDEOIMAGE\_TRANSITION\_SPLIT**</span></span>](wmt-videoimage-transition-split.md)                   | <span data-ttu-id="65994-148">A nova imagem é revelada por uma divisão horizontal ou vertical na imagem antiga.</span><span class="sxs-lookup"><span data-stu-id="65994-148">New image is revealed by a horizontal or vertical split in the old image.</span></span> <span data-ttu-id="65994-149">A divisão aparece ao longo de uma linha reta começando dentro do quadro.</span><span class="sxs-lookup"><span data-stu-id="65994-149">The split appears along a straight line starting inside the frame.</span></span> |
| [<span data-ttu-id="65994-150">**\_estrela de \_ transição WMT VIDEOIMAGE \_**</span><span class="sxs-lookup"><span data-stu-id="65994-150">**WMT\_VIDEOIMAGE\_TRANSITION\_STAR**</span></span>](wmt-videoimage-transition-star.md)                     | <span data-ttu-id="65994-151">A nova imagem é revelada por uma estrela de cinco pontas dentro do quadro.</span><span class="sxs-lookup"><span data-stu-id="65994-151">New image is revealed by a five-pointed star inside the frame.</span></span>                                                                               |
| [<span data-ttu-id="65994-152">**\_roda de \_ transição WMT VIDEOIMAGE \_**</span><span class="sxs-lookup"><span data-stu-id="65994-152">**WMT\_VIDEOIMAGE\_TRANSITION\_WHEEL**</span></span>](wmt-videoimage-transition-wheel.md)                   | <span data-ttu-id="65994-153">A nova imagem é revelada por quatro spokes giratórias com um ponto dinâmico comum.</span><span class="sxs-lookup"><span data-stu-id="65994-153">New image is revealed by four rotating spokes with a common pivot point.</span></span>                                                                     |



 

<span data-ttu-id="65994-154">Cada transição é totalmente descrita em seu próprio tópico.</span><span class="sxs-lookup"><span data-stu-id="65994-154">Each transition is fully described in its own topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65994-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="65994-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65994-156">**Referência de programação**</span><span class="sxs-lookup"><span data-stu-id="65994-156">**Programming Reference**</span></span>](programming-reference.md)
</dt> <dt>

[<span data-ttu-id="65994-157">**WMT \_ VIDEOIMAGE \_ SAMPLE2**</span><span class="sxs-lookup"><span data-stu-id="65994-157">**WMT\_VIDEOIMAGE\_SAMPLE2**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2)
</dt> </dl>

 

 




