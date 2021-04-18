---
title: Funções básicas para uso em um contexto de dispositivo
description: As seguintes funções WCS fornecem recursos básicos de mapeamento de cores dentro de contextos de dispositivo. Eles são úteis para todos os aplicativos que precisam implementar o gerenciamento de cores com baixa sobrecarga e intervenção mínima do usuário.
ms.assetid: 199fac5e-daba-4aa3-a631-bb1eb2270b2e
keywords:
- WCS (sistema de cores do Windows), funções
- WCS (sistema de cores do Windows), funções
- gerenciamento de cores de imagem, funções
- gerenciamento de cores, funções
- cores, funções
- Referência do WCS, funções
- referência para WCS, funções
- WCS (sistema de cores do Windows), contextos de dispositivo
- WCS (sistema de cores do Windows), contextos de dispositivo
- gerenciamento de cores de imagem, contextos de dispositivo
- gerenciamento de cores, contextos de dispositivo
- cores, contextos de dispositivo
- Referência do WCS, contextos de dispositivo
- referência para WCS, contextos de dispositivo
- contextos de dispositivo
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde99ed077af108ddc20c73f86e17bedfe1d4a8c
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/03/2021
ms.locfileid: "105808409"
---
# <a name="basic-functions-for-use-within-a-device-context"></a><span data-ttu-id="4e32d-119">Funções básicas para uso em um contexto de dispositivo</span><span class="sxs-lookup"><span data-stu-id="4e32d-119">Basic Functions for Use Within a Device Context</span></span>

<span data-ttu-id="4e32d-120">As seguintes funções WCS fornecem recursos básicos de [mapeamento de cores](c.md) dentro de contextos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e32d-120">The following WCS functions deliver basic [color mapping](c.md) capabilities within device contexts.</span></span> <span data-ttu-id="4e32d-121">Eles são úteis para todos os aplicativos que precisam implementar o gerenciamento de cores com baixa sobrecarga e intervenção mínima do usuário.</span><span class="sxs-lookup"><span data-stu-id="4e32d-121">They are useful to all applications that need to implement color management with low overhead and minimal user intervention.</span></span>



| <span data-ttu-id="4e32d-122">Função</span><span class="sxs-lookup"><span data-stu-id="4e32d-122">Function</span></span>                                                           | <span data-ttu-id="4e32d-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e32d-123">Description</span></span>                                                                                                                                         |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e32d-124">**CheckColorsInGamut**</span><span class="sxs-lookup"><span data-stu-id="4e32d-124">**CheckColorsInGamut**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-checkcolorsingamut)                   | <span data-ttu-id="4e32d-125">Verifica se as cores determinadas estão na gama de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e32d-125">Checks if given colors are in a device's gamut.</span></span>                                                                                                     |
| [<span data-ttu-id="4e32d-126">**ColorCorrectPalette**</span><span class="sxs-lookup"><span data-stu-id="4e32d-126">**ColorCorrectPalette**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-colorcorrectpalette)                 | <span data-ttu-id="4e32d-127">Corrige as entradas em uma paleta para um contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e32d-127">Corrects the entries in a palette for a device context.</span></span>                                                                                             |
| [<span data-ttu-id="4e32d-128">**ColorMatchToTarget**</span><span class="sxs-lookup"><span data-stu-id="4e32d-128">**ColorMatchToTarget**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-colormatchtotarget)                   | <span data-ttu-id="4e32d-129">Executa o mapeamento de cores para fins de visualização.</span><span class="sxs-lookup"><span data-stu-id="4e32d-129">Performs color mapping for preview purposes.</span></span>                                                                                                        |
| [<span data-ttu-id="4e32d-130">**CreateColorSpace**</span><span class="sxs-lookup"><span data-stu-id="4e32d-130">**CreateColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createcolorspacea)                       | <span data-ttu-id="4e32d-131">Cria um espaço de cores.</span><span class="sxs-lookup"><span data-stu-id="4e32d-131">Creates a color space.</span></span>                                                                                                                              |
| [<span data-ttu-id="4e32d-132">**DeleteColorSpace**</span><span class="sxs-lookup"><span data-stu-id="4e32d-132">**DeleteColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-deletecolorspace)                       | <span data-ttu-id="4e32d-133">Exclui um espaço de cores.</span><span class="sxs-lookup"><span data-stu-id="4e32d-133">Deletes a color space.</span></span>                                                                                                                              |
| [<span data-ttu-id="4e32d-134">**EnumICMProfiles**</span><span class="sxs-lookup"><span data-stu-id="4e32d-134">**EnumICMProfiles**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)                         | <span data-ttu-id="4e32d-135">Enumera os perfis de cor de saída disponíveis para um determinado contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e32d-135">Enumerates output color profiles available for a given device context.</span></span>                                                                              |
| [<span data-ttu-id="4e32d-136">**EnumICMProfilesProcCallback**</span><span class="sxs-lookup"><span data-stu-id="4e32d-136">**EnumICMProfilesProcCallback**</span></span>](/windows/desktop/api/Wingdi/) | <span data-ttu-id="4e32d-137">Função de retorno de chamada definida pelo aplicativo para [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa).</span><span class="sxs-lookup"><span data-stu-id="4e32d-137">Application-defined callback function for [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa).</span></span> <span data-ttu-id="4e32d-138">O nome dessa função também é definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4e32d-138">The name of this function is also defined by the application.</span></span> |
| [<span data-ttu-id="4e32d-139">**GetColorSpace**</span><span class="sxs-lookup"><span data-stu-id="4e32d-139">**GetColorSpace**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getcolorspace) | <span data-ttu-id="4e32d-140">Obtém o espaço de cor de entrada atual em um contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e32d-140">Gets the current input color space in a device context.</span></span> |
| [<span data-ttu-id="4e32d-141">**GetICMProfile**</span><span class="sxs-lookup"><span data-stu-id="4e32d-141">**GetICMProfile**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)                             | <span data-ttu-id="4e32d-142">Obtém o perfil de cor de saída atual de um contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e32d-142">Gets the current output color profile of a device context.</span></span>                                                                                          |
| [<span data-ttu-id="4e32d-143">**GetLogColorSpace**</span><span class="sxs-lookup"><span data-stu-id="4e32d-143">**GetLogColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getlogcolorspacea)                       | <span data-ttu-id="4e32d-144">Obtém a estrutura [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) de um contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e32d-144">Gets the [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) structure of a device context.</span></span>                                                                      |
| [<span data-ttu-id="4e32d-145">**SetColorSpace**</span><span class="sxs-lookup"><span data-stu-id="4e32d-145">**SetColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setcolorspace)                             | <span data-ttu-id="4e32d-146">Define o espaço de cores de entrada de um contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e32d-146">Sets a device context's input color space.</span></span>                                                                                                          |
| [<span data-ttu-id="4e32d-147">**SetICMMode**</span><span class="sxs-lookup"><span data-stu-id="4e32d-147">**SetICMMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)                                   | <span data-ttu-id="4e32d-148">Ativa ou desativa o gerenciamento de cores em um contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e32d-148">Turns color management on or off in a device context.</span></span>                                                                                               |
| [<span data-ttu-id="4e32d-149">**SetICMProfile**</span><span class="sxs-lookup"><span data-stu-id="4e32d-149">**SetICMProfile**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-seticmprofilea)                             | <span data-ttu-id="4e32d-150">Define o perfil de cor de saída para um determinado contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e32d-150">Sets the output color profile for a given device context.</span></span>                                                                                           |
| [<span data-ttu-id="4e32d-151">**WcsEnumColorProfiles**</span><span class="sxs-lookup"><span data-stu-id="4e32d-151">**WcsEnumColorProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)               | <span data-ttu-id="4e32d-152">Enumera todos os perfis de cor que atendem aos critérios de enumeração no escopo de gerenciamento de perfil especificado.</span><span class="sxs-lookup"><span data-stu-id="4e32d-152">Enumerates all color profiles that satisfy the enumeration criteria in the specified profile management scope.</span></span>                                      |



 

 

 




