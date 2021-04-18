---
title: Uso do processo de mapeamento de cores com o WCS
description: O mapeamento de cores WCS é baseado em perfis de dispositivo.
ms.assetid: df4d390e-0c9e-40dc-864a-2177934895db
keywords:
- WCS (sistema de cores do Windows), mapeamento de cores
- WCS (sistema de cores do Windows), mapeamento de cores
- gerenciamento de cores de imagem, mapeamento de cores
- gerenciamento de cores, mapeamento de cores
- cores, mapeamento de cores
- mapeamento de cores
- WCS (sistema de cores do Windows), perfis de dispositivo
- WCS (sistema de cores do Windows), perfis de dispositivo
- gerenciamento de cores de imagem, perfis de dispositivo
- gerenciamento de cores, perfis de dispositivo
- cores, perfis de dispositivo
- WCS (sistema de cores do Windows), perfis
- WCS (sistema de cores do Windows), perfis
- gerenciamento de cores de imagem, perfis
- gerenciamento de cores, perfis
- cores, perfis
- perfis de dispositivo
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 428b09749f3781def44e56ff6cea0539259d0464
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "105793777"
---
# <a name="using-the-color-mapping-process-with-wcs"></a><span data-ttu-id="0afbc-120">Uso do processo de mapeamento de cores com o WCS</span><span class="sxs-lookup"><span data-stu-id="0afbc-120">Using The Color Mapping Process with WCS</span></span>

<span data-ttu-id="0afbc-121">O mapeamento de cores WCS é baseado em [perfis de dispositivo](d.md).</span><span class="sxs-lookup"><span data-stu-id="0afbc-121">WCS color mapping is based on [device profiles](d.md).</span></span> <span data-ttu-id="0afbc-122">Eles são fornecidos por fornecedores de dispositivos de hardware de cores e instalados quando um dispositivo é instalado.</span><span class="sxs-lookup"><span data-stu-id="0afbc-122">These are supplied by vendors of color hardware devices and installed when a device is installed.</span></span> <span data-ttu-id="0afbc-123">Quando o mapeamento de cores é usado por um programa de aplicativo, o WCS acessa o perfil de dispositivo da imagem para obter as informações necessárias para converter a imagem nos PCS.</span><span class="sxs-lookup"><span data-stu-id="0afbc-123">When color mapping is used by an application program, WCS accesses the device profile of the image to get the information needed to convert the image to the PCS.</span></span> <span data-ttu-id="0afbc-124">A conversão é feita pelo CMM.</span><span class="sxs-lookup"><span data-stu-id="0afbc-124">The conversion is done by the CMM.</span></span>

<span data-ttu-id="0afbc-125">Um perfil de dispositivo pode ser inserido na própria imagem.</span><span class="sxs-lookup"><span data-stu-id="0afbc-125">A device profile can be embedded into the image itself.</span></span> <span data-ttu-id="0afbc-126">Portanto, o perfil do dispositivo viaja com a imagem, mesmo pela Internet.</span><span class="sxs-lookup"><span data-stu-id="0afbc-126">So the device profile travels with the image, even across the Internet.</span></span> <span data-ttu-id="0afbc-127">Um usuário não precisa do dispositivo de origem para obter um mapeamento de cores preciso.</span><span class="sxs-lookup"><span data-stu-id="0afbc-127">A user does not need the source device to get an accurate color mapping.</span></span> <span data-ttu-id="0afbc-128">Se uma imagem não tiver um perfil de dispositivo, o espaço sRGB será usado como padrão.</span><span class="sxs-lookup"><span data-stu-id="0afbc-128">If an image does not have a device profile, the sRGB space is used as a default.</span></span> <span data-ttu-id="0afbc-129">Para obter mais detalhes, consulte [usando o gerenciamento de cores na Internet](using-color-management-on-the-internet.md).</span><span class="sxs-lookup"><span data-stu-id="0afbc-129">For more details, see [Using Color Management on the Internet](using-color-management-on-the-internet.md).</span></span>

<span data-ttu-id="0afbc-130">Observe que os aplicativos que usam o WCS nunca devem inserir o perfil sRGB em uma imagem.</span><span class="sxs-lookup"><span data-stu-id="0afbc-130">Note that applications which use WCS should never embed the sRGB profile into an image.</span></span> <span data-ttu-id="0afbc-131">O espaço de cores sRGB fornece um espaço de cores padronizado que é portável em todos os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="0afbc-131">The sRGB color space provides a standardized color space that is portable across all devices.</span></span> <span data-ttu-id="0afbc-132">Ele está automaticamente disponível para os usuários do Windows 98 e posterior, bem como Windows 2000 e posterior.</span><span class="sxs-lookup"><span data-stu-id="0afbc-132">It is automatically available to users of Windows 98 and later as well as Windows 2000 and later.</span></span> <span data-ttu-id="0afbc-133">Portanto, ele não precisa viajar com a imagem.</span><span class="sxs-lookup"><span data-stu-id="0afbc-133">Therefore, it does not need to travel with the image.</span></span>

<span data-ttu-id="0afbc-134">Depois que as cores da imagem estiverem nos [PCs](p.md), o WCS acessará o perfil do dispositivo do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="0afbc-134">After the image colors are in the [PCS](p.md), WCS accesses the device profile of the destination device.</span></span> <span data-ttu-id="0afbc-135">Ele obtém o CMM para converter as cores da imagem dos PCS para a gama do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="0afbc-135">It gets the CMM to convert the image colors from PCS to the gamut of the destination device.</span></span>

<span data-ttu-id="0afbc-136">O mapeamento de cores mais complexo também pode ser feito com o WCS.</span><span class="sxs-lookup"><span data-stu-id="0afbc-136">More complex color mapping can also be done with WCS.</span></span> <span data-ttu-id="0afbc-137">Por exemplo, ele pode ser usado para ter uma ideia da aparência de uma imagem criada em uma exibição de vídeo quando impressa em uma impressora laser de alta resolução.</span><span class="sxs-lookup"><span data-stu-id="0afbc-137">For example, it can be used to get an idea of what an image created on a video display would look like when printed on a high resolution laser printer.</span></span> <span data-ttu-id="0afbc-138">O exemplo se torna mais complexo se houver apenas uma impressora jato de radiostandard na qual seja possível visualizá-la.</span><span class="sxs-lookup"><span data-stu-id="0afbc-138">The example gets more complex if there is only a standard inkjet printer on which to preview it.</span></span> <span data-ttu-id="0afbc-139">A imagem pode ser convertida da gama da tela, na gama da impressora da jato de radiográfica.</span><span class="sxs-lookup"><span data-stu-id="0afbc-139">The image can be converted from the gamut of the display, into the gamut of the inkjet printer.</span></span> <span data-ttu-id="0afbc-140">A partir daí, ele pode ser convertido na gama da impressora laser.</span><span class="sxs-lookup"><span data-stu-id="0afbc-140">From there it can converted into the gamut of the laser printer.</span></span> <span data-ttu-id="0afbc-141">A imagem resultante pode ser impressa na impressora jato de radiográfica.</span><span class="sxs-lookup"><span data-stu-id="0afbc-141">The resulting image can be printed on the inkjet printer.</span></span> <span data-ttu-id="0afbc-142">É claro que a imagem estaria em uma resolução mais alta quando impressa na impressora laser colorida.</span><span class="sxs-lookup"><span data-stu-id="0afbc-142">Of course the image would be at a higher resolution when printed on the color laser printer.</span></span> <span data-ttu-id="0afbc-143">No entanto, as cores da imagem de prova impressa na impressora jato de radiográfica seriam uma correspondência próxima às cores que a impressora laser imprimiria.</span><span class="sxs-lookup"><span data-stu-id="0afbc-143">However, the colors of the proofing image printed on the inkjet printer would be a close match to the colors that the laser printer would print.</span></span>

<span data-ttu-id="0afbc-144">A maneira como as conversões no exemplo são realizadas é converter as cores da imagem da gama do vídeo nos PCS.</span><span class="sxs-lookup"><span data-stu-id="0afbc-144">The way the conversions in the example are accomplished is to convert the image colors from the display's gamut into the PCS.</span></span> <span data-ttu-id="0afbc-145">Depois que as cores da imagem forem convertidas nos PCS, o perfil do dispositivo da impressora jato de radiográfica será usado para transformá-las na gama da impressora da jato de radiográfica.</span><span class="sxs-lookup"><span data-stu-id="0afbc-145">After the image colors are converted into the PCS, the device profile of the inkjet printer would be used to transform them into the gamut of the inkjet printer.</span></span> <span data-ttu-id="0afbc-146">Em seguida, a transformação de gama para PCS seria usada para mover as cores de volta para os PCS.</span><span class="sxs-lookup"><span data-stu-id="0afbc-146">Next, the gamut to PCS transform would be used to move the colors back to the PCS.</span></span> <span data-ttu-id="0afbc-147">A partir daí, o perfil de dispositivo da impressora laser é usado para converter as cores dos PCS na gama da impressora laser.</span><span class="sxs-lookup"><span data-stu-id="0afbc-147">From there, the laser printer's device profile is used to convert the colors from PCS into the gamut of the laser printer.</span></span>

<span data-ttu-id="0afbc-148">A capacidade de transformar facilmente as cores de uma gama de dispositivos nos PCS e voltar novamente permite que as cores de imagem pretendidas para um dispositivo de saída de cor sejam provadas em praticamente qualquer outro.</span><span class="sxs-lookup"><span data-stu-id="0afbc-148">The ability to easily transform colors from a device gamut to the PCS and back again enables image colors intended for one color output device to be proofed on almost any other.</span></span>

<span data-ttu-id="0afbc-149">No exemplo anterior, a descrição varia do procedimento real um pouco para maior clareza.</span><span class="sxs-lookup"><span data-stu-id="0afbc-149">In the preceding example, the description varies from the actual procedure somewhat for clarity.</span></span> <span data-ttu-id="0afbc-150">Na realidade, todas as transformações mencionadas no parágrafo anterior seriam concatenadas em uma única transformação.</span><span class="sxs-lookup"><span data-stu-id="0afbc-150">In reality, all of the transformations mentioned in the preceding paragraph would be concatenated into a single transformation.</span></span>

 

 




