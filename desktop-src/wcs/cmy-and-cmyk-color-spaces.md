---
title: Espaços de cores CMY e CMYK
description: Os espaços de cores CMY e CMYK geralmente são usados na impressão em cores. Um espaço de cores CMY usa o CMY (ciano, magenta e amarelo) como suas cores primárias. Vermelho, verde e azul são as cores secundárias.
ms.assetid: e135b5ef-fa5c-49b7-8537-5dc31cde2418
keywords:
- WCS (sistema de cores do Windows), espaços de cores CMY
- WCS (sistema de cores do Windows), espaços de cores CMY
- gerenciamento de cores de imagem, espaços de cores CMY
- gerenciamento de cores, espaços de cores CMY
- cores, espaços de cores CMY
- espaços de cores, CMY
- Espaços de cores CMY
- WCS (sistema de cores do Windows), espaços de cores CMYK
- WCS (sistema de cores do Windows), espaços de cores CMYK
- gerenciamento de cores de imagem, espaços de cores CMYK
- gerenciamento de cores, espaços CMYKcolors
- cores, espaços de cores CMYK
- espaços de cores, CMYK
- Espaços de cores CMYK
- cyan
- magenta
- yellow
- amarelo magenta ciano (CMY)
- CMY (ciano magenta amarelo)
- preto-magenta amarelo ciano (CMYK)
- CMYK (ciano magenta amarelo preto)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52622c929222eb9027b6272137a8b897210697b6
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "105816058"
---
# <a name="cmy-and-cmyk-color-spaces"></a><span data-ttu-id="1bed6-126">Espaços de cores CMY e CMYK</span><span class="sxs-lookup"><span data-stu-id="1bed6-126">CMY and CMYK Color Spaces</span></span>

<span data-ttu-id="1bed6-127">Os [espaços de cores](c.md) CMY e CMYK geralmente são usados na impressão em cores.</span><span class="sxs-lookup"><span data-stu-id="1bed6-127">The CMY and CMYK [color spaces](c.md) are often used in color printing.</span></span> <span data-ttu-id="1bed6-128">Um espaço de cores CMY usa o CMY (ciano, magenta e amarelo) como suas [cores primárias](p.md).</span><span class="sxs-lookup"><span data-stu-id="1bed6-128">A CMY color space uses cyan, magenta, and yellow (CMY) as its [primary colors](p.md).</span></span> <span data-ttu-id="1bed6-129">Vermelho, verde e azul são as cores secundárias.</span><span class="sxs-lookup"><span data-stu-id="1bed6-129">Red, green, and blue are the secondary colors.</span></span>

<span data-ttu-id="1bed6-130">As figuras a seguir são representações de cor do espaço de cores CMY.</span><span class="sxs-lookup"><span data-stu-id="1bed6-130">The following figures are color representations of the CMY color space.</span></span> <span data-ttu-id="1bed6-131">O espaço de cores CMY é normalizado.</span><span class="sxs-lookup"><span data-stu-id="1bed6-131">The CMY color space is normalized.</span></span>

![cubo de espaço de cores CMY em valores máximos](images/cmyclrs1.png)

![cubo de espaço de cores CMY em valores mínimos](images/cmyclrs2.png)

<span data-ttu-id="1bed6-134">O espaço de cores CMY é subtraíl.</span><span class="sxs-lookup"><span data-stu-id="1bed6-134">The CMY color space is subtractive.</span></span> <span data-ttu-id="1bed6-135">Portanto, o branco está em (0,0, 0,0, 0,0) e o preto está em (1,0, 1,0, 1,0).</span><span class="sxs-lookup"><span data-stu-id="1bed6-135">Therefore, white is at (0.0, 0.0, 0.0) and black is at (1.0, 1.0, 1.0).</span></span> <span data-ttu-id="1bed6-136">Se você começar com branco e subtrair sem cores, você terá branco.</span><span class="sxs-lookup"><span data-stu-id="1bed6-136">If you start with white and subtract no colors, you get white.</span></span> <span data-ttu-id="1bed6-137">Se você começar com branco e subtrair todas as cores igualmente, você terá preto.</span><span class="sxs-lookup"><span data-stu-id="1bed6-137">If you start with white and subtract all colors equally, you get black.</span></span>

<span data-ttu-id="1bed6-138">O espaço de cores CMYK é uma variação no modelo CMY.</span><span class="sxs-lookup"><span data-stu-id="1bed6-138">The CMYK color space is a variation on the CMY model.</span></span> <span data-ttu-id="1bed6-139">Ele adiciona preto (ciano, magenta, amarelo e preto).</span><span class="sxs-lookup"><span data-stu-id="1bed6-139">It adds black (Cyan, Magenta, Yellow, and blacK).</span></span> <span data-ttu-id="1bed6-140">O espaço de cores CMYK fecha a lacuna entre teoria e prática.</span><span class="sxs-lookup"><span data-stu-id="1bed6-140">The CMYK color space closes the gap between theory and practice.</span></span> <span data-ttu-id="1bed6-141">Teoricamente, o componente preto extra não é necessário.</span><span class="sxs-lookup"><span data-stu-id="1bed6-141">In theory, the extra black component is not needed.</span></span> <span data-ttu-id="1bed6-142">No entanto, a experiência com vários tipos de tintas e documentos mostrou que, quando os componentes iguais de tintas ciano, magenta e amarelo são misturados, o resultado é geralmente um marrom escuro, e não preto.</span><span class="sxs-lookup"><span data-stu-id="1bed6-142">However, experience with various types of inks and papers has shown that when equal components of cyan, magenta, and yellow inks are mixed, the result is usually a dark brown, not black.</span></span> <span data-ttu-id="1bed6-143">A adição de tinta preta à combinação resolve esse problema.</span><span class="sxs-lookup"><span data-stu-id="1bed6-143">Adding black ink to the mix solves this problem.</span></span>

<span data-ttu-id="1bed6-144">Os espaços de cores CMY e CMYK podem ser independentes de dispositivo, mas geralmente são usados em referência a um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="1bed6-144">The CMY and CMYK colors spaces can be device independent, but most often they are used in reference to a specific device.</span></span>

 

 




