---
title: Conversão de cores e correspondência de cores
description: O processo de converter cores de um espaço de cor para outro é chamado de conversão de cores.
ms.assetid: 52f68779-d4d6-4f1e-88a4-f872e9e90054
keywords:
- WCS (sistema de cores do Windows), conversão de cores
- WCS (sistema de cores do Windows), conversão de cores
- gerenciamento de cores de imagem, conversão de cores
- gerenciamento de cores, conversão de cores
- cores, conversão de cores
- conversão de cores
- WCS (sistema de cores do Windows), correspondência de cores
- WCS (sistema de cores do Windows), correspondência de cores
- gerenciamento de cores de imagem, correspondência de cores
- gerenciamento de cores, correspondência de cores
- cores, correspondência de cores
- correspondência de cores
- WCS (sistema de cores do Windows), mapeamento de cores
- WCS (sistema de cores do Windows), mapeamento de cores
- gerenciamento de cores de imagem, mapeamento de cores
- gerenciamento de cores, mapeamento de cores
- cores, mapeamento de cores
- mapeamento de cores
- ponto branco
- colorants
- correção gama
- gama
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b74de95238472f58d49c5033a601c6d5458773c8
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "105816060"
---
# <a name="color-conversion-and-color-matching"></a><span data-ttu-id="2e7fa-125">Conversão de cores e correspondência de cores</span><span class="sxs-lookup"><span data-stu-id="2e7fa-125">Color Conversion and Color Matching</span></span>

<span data-ttu-id="2e7fa-126">O processo de converter cores de um [espaço de cor](c.md) para outro é chamado de *conversão de cores*.</span><span class="sxs-lookup"><span data-stu-id="2e7fa-126">The process of converting colors from one [color space](c.md) to another is called *color conversion*.</span></span> <span data-ttu-id="2e7fa-127">Todas as cores em um espaço de cores são fixas em relação ao [ponto branco](w.md)do espaço de cores.</span><span class="sxs-lookup"><span data-stu-id="2e7fa-127">All colors in a color space are fixed relative to the color space's [white point](w.md).</span></span> <span data-ttu-id="2e7fa-128">Como o ponto branco de um espaço de cor varia de dispositivo para dispositivo, uma cor convertida deve ser correspondida à sua cor mais próxima no espaço de cores de destino.</span><span class="sxs-lookup"><span data-stu-id="2e7fa-128">Since the white point of a color space varies from device to device, a converted color must then be matched to its visually closest color in the destination color space.</span></span> <span data-ttu-id="2e7fa-129">Esse processo é chamado de *mapeamento de cores*.</span><span class="sxs-lookup"><span data-stu-id="2e7fa-129">This process is called *color mapping*.</span></span>

<span data-ttu-id="2e7fa-130">Por exemplo, se você tiver uma imagem digital que você criou na exibição, ela poderá estar em um espaço de cores RGB dependente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2e7fa-130">For example, if you have a digital image that you created on your display, it may be in a device-dependent RGB color space.</span></span> <span data-ttu-id="2e7fa-131">Se você quiser imprimi-lo em uma impressora, ele deverá ser convertido no espaço de cores da impressora.</span><span class="sxs-lookup"><span data-stu-id="2e7fa-131">If you want to print it on a printer, it must be converted to the printer's color space.</span></span> <span data-ttu-id="2e7fa-132">Como a impressora provavelmente usa um espaço de cores CMYK dependente de dispositivo, todos os valores RGB devem ser convertidos em CYMK.</span><span class="sxs-lookup"><span data-stu-id="2e7fa-132">Since the printer probably uses a device-dependent CMYK color space, all RGB values must be converted to CYMK.</span></span> <span data-ttu-id="2e7fa-133">Esta é a [conversão de cores](c.md).</span><span class="sxs-lookup"><span data-stu-id="2e7fa-133">This is [color conversion](c.md).</span></span> <span data-ttu-id="2e7fa-134">Depois que os valores são especificados em termos do espaço CYMK, eles precisam corresponder à cor mais próxima que a impressora pode produzir.</span><span class="sxs-lookup"><span data-stu-id="2e7fa-134">Once the values are specified in terms of the CYMK space, they need to be matched to the closest color that the printer can produce.</span></span> <span data-ttu-id="2e7fa-135">Isso é chamado de mapeamento de cores ou [correspondência de cores](c.md).</span><span class="sxs-lookup"><span data-stu-id="2e7fa-135">This is called color mapping or [color matching](c.md).</span></span>

<span data-ttu-id="2e7fa-136">A conversão de cores e o mapeamento de cores devem levar em consideração uma série de fatores específicos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2e7fa-136">Both color conversion and color mapping must take into account a number of device-specific factors.</span></span> <span data-ttu-id="2e7fa-137">Por exemplo, os blocos de construção de imagens de tela são pixels.</span><span class="sxs-lookup"><span data-stu-id="2e7fa-137">For instance, the building blocks of screen images are pixels.</span></span> <span data-ttu-id="2e7fa-138">Cada pixel tem um número definido de bits para armazenar seu valor de índice de cor ou cor.</span><span class="sxs-lookup"><span data-stu-id="2e7fa-138">Each pixel has a set number of bits to store its color or color index value.</span></span> <span data-ttu-id="2e7fa-139">O número de bits por pixel depende do tipo de adaptador de vídeo e exibição que está sendo usado e do modo ao qual o adaptador está definido.</span><span class="sxs-lookup"><span data-stu-id="2e7fa-139">The number of bits per pixel depends on the type of display and display adapter being used, and the mode to which that the adapter is set.</span></span> <span data-ttu-id="2e7fa-140">A maioria dos tipos de impressora usa diferentes [colorants](c.md) e imprime em resoluções específicas.</span><span class="sxs-lookup"><span data-stu-id="2e7fa-140">Most every printer type uses different [colorants](c.md) and prints at particular resolutions.</span></span>

<span data-ttu-id="2e7fa-141">Além disso, as características de Tom físico de um dispositivo geralmente são diferentes em dispositivos diferentes.</span><span class="sxs-lookup"><span data-stu-id="2e7fa-141">In addition, the physical tone characteristics of a device are often different on different devices.</span></span> <span data-ttu-id="2e7fa-142">Por exemplo, quando as cores são produzidas por monitores de computador, elas podem parecer diferentes do que se fossem produzidas em uma prensa de impressão.</span><span class="sxs-lookup"><span data-stu-id="2e7fa-142">For instance, when colors are produced by computer monitors, they can appear different than they would if they were produced on a printing press.</span></span> <span data-ttu-id="2e7fa-143">Um fator de correção, chamado de *correção gama*, é frequentemente usado para compensar essas diferenças.</span><span class="sxs-lookup"><span data-stu-id="2e7fa-143">A correction factor, called *gamma correction*, is frequently used to compensate for such differences.</span></span>

<span data-ttu-id="2e7fa-144">O resultado desses fatores dependentes de dispositivo é que cada dispositivo de cores tem um conjunto específico de cores que ele pode produzir.</span><span class="sxs-lookup"><span data-stu-id="2e7fa-144">The result of these device-dependent factors is that each color device has a particular set of colors that it can produce.</span></span> <span data-ttu-id="2e7fa-145">Esse conjunto de cores é conhecido como sua *gama*.</span><span class="sxs-lookup"><span data-stu-id="2e7fa-145">This color set is known as its *gamut*.</span></span> <span data-ttu-id="2e7fa-146">Para executar a conversão de cores e o mapeamento de cores, as cores em uma imagem devem ser convertidas do espaço de cores e da gama do dispositivo de origem no espaço de cores do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="2e7fa-146">To perform color conversion and color mapping, the colors in an image must be converted from the color space and gamut of the source device into the color space of the destination device.</span></span> <span data-ttu-id="2e7fa-147">Em seguida, eles são combinados na gama do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="2e7fa-147">They are then matched into the gamut of the destination device.</span></span>

 

 




