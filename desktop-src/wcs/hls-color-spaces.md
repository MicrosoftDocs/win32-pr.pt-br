---
title: Espaços de Cores HLS
description: Os espaços de cores HLS também são amplamente usados por artistas. Seus componentes de cor são matiz, claridade e saturação (croma).
ms.assetid: 8c80d200-c4d0-4233-8f53-a9637dff9ab2
keywords:
- WCS (sistema de cores do Windows), espaços de cores HLS
- WCS (sistema de cores do Windows), espaços de cores HLS
- gerenciamento de cores de imagem, espaços de cores HLS
- gerenciamento de cores, espaços de cores HLS
- cores, HLS espaços de cores
- espaços de cores, HLS
- HLS espaços de cores
- Hue
- saturação
- tonalidades
- Saturação zero
- saturação de luminosidade de matiz (HLS)
- HLS (saturação de luminosidade de matiz)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613a62d4a998b51f9bfb22bd7431dd8645a72f3e
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "105814188"
---
# <a name="hls-color-spaces"></a><span data-ttu-id="19f1f-117">Espaços de Cores HLS</span><span class="sxs-lookup"><span data-stu-id="19f1f-117">HLS Color Spaces</span></span>

<span data-ttu-id="19f1f-118">Os [espaços de cores](c.md) HLS também são amplamente usados por artistas.</span><span class="sxs-lookup"><span data-stu-id="19f1f-118">HLS [color spaces](c.md) are also widely used by artists.</span></span> <span data-ttu-id="19f1f-119">Seus componentes de cor são matiz, claridade e saturação (croma).</span><span class="sxs-lookup"><span data-stu-id="19f1f-119">Its color components are hue, lightness, and saturation (chroma).</span></span>

<span data-ttu-id="19f1f-120">O matiz tem o mesmo significado que o modelo HSV, exceto que um ângulo de matiz de 0 corresponde a azul nesse modelo.</span><span class="sxs-lookup"><span data-stu-id="19f1f-120">Hue has the same meaning as the HSV model, except that a hue angle of 0 corresponds to blue in this model.</span></span> <span data-ttu-id="19f1f-121">O magenta está em 60, o vermelho está em 120.</span><span class="sxs-lookup"><span data-stu-id="19f1f-121">Magenta is at 60, red is at 120.</span></span> <span data-ttu-id="19f1f-122">Assim como acontece com o modelo HSV, as cores complementares são de diferença de 180.</span><span class="sxs-lookup"><span data-stu-id="19f1f-122">As with the HSV model, complementary colors are 180 apart.</span></span>

<span data-ttu-id="19f1f-123">A claridade é a quantidade de preto ou branco em uma cor.</span><span class="sxs-lookup"><span data-stu-id="19f1f-123">Lightness is the amount of black or white in a color.</span></span> <span data-ttu-id="19f1f-124">Aumentar a claridade adiciona branco ao matiz.</span><span class="sxs-lookup"><span data-stu-id="19f1f-124">Increasing lightness adds white to the hue.</span></span> <span data-ttu-id="19f1f-125">Diminuir a claridade adiciona preto ao matiz.</span><span class="sxs-lookup"><span data-stu-id="19f1f-125">Decreasing lightness adds black to the hue.</span></span>

<span data-ttu-id="19f1f-126">A [saturação](s.md) no modelo HLS é uma medida da "pureza" de um matiz.</span><span class="sxs-lookup"><span data-stu-id="19f1f-126">[Saturation](s.md) in the HLS model is a measure of the "purity" of a hue.</span></span> <span data-ttu-id="19f1f-127">À medida que a saturação é diminuída, o matiz se torna mais cinza.</span><span class="sxs-lookup"><span data-stu-id="19f1f-127">As saturation is decreased, the hue becomes more gray.</span></span> <span data-ttu-id="19f1f-128">Um valor de saturação igual a zero resulta em um valor de escala cinza.</span><span class="sxs-lookup"><span data-stu-id="19f1f-128">A saturation value of zero results in a gray-scale value.</span></span>

<span data-ttu-id="19f1f-129">A figura a seguir é um desenho de linha de espaço HLS, que é um hexcone duplo.</span><span class="sxs-lookup"><span data-stu-id="19f1f-129">The following figure is a line drawing of HLS space, which is a double hexcone.</span></span> <span data-ttu-id="19f1f-130">Qualquer seção cruzada horizontal do espaço de cores HLS é um hexágono.</span><span class="sxs-lookup"><span data-stu-id="19f1f-130">Any horizontal cross section of the HLS color space is a hexagon.</span></span> <span data-ttu-id="19f1f-131">HLS é um espaço de cores normalizado.</span><span class="sxs-lookup"><span data-stu-id="19f1f-131">HLS is a normalized color space.</span></span> <span data-ttu-id="19f1f-132">Ou seja, os valores de luminosidade e saturação variam de 0,0 a 1,0, inclusive.</span><span class="sxs-lookup"><span data-stu-id="19f1f-132">That is, the lightness and saturation values range from 0.0 to 1.0 inclusive.</span></span> <span data-ttu-id="19f1f-133">O matiz varia de 0 a 360, inclusive.</span><span class="sxs-lookup"><span data-stu-id="19f1f-133">Hue varies from 0 to 360 inclusive.</span></span>

![espaço de cores HLS](images/hlsline.png)

<span data-ttu-id="19f1f-135">Os espaços de cores HLS podem ser dependentes de dispositivo ou independentes de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19f1f-135">HLS color spaces can be device dependent or device independent.</span></span>

 

 




