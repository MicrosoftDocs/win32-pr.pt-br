---
title: Funções de calibragem e caracterização de dispositivo
description: As funções a seguir são úteis para a gravação de ferramentas de calibragem de dispositivo e de caracterização necessárias para instalar e calibrar dispositivos de exibição de cor, como monitores e impressoras.
ms.assetid: e66115cc-b6a9-4df5-b774-38619881bdb0
keywords:
- WCS (sistema de cores do Windows), funções
- WCS (sistema de cores do Windows), funções
- gerenciamento de cores de imagem, funções
- gerenciamento de cores, funções
- cores, funções
- Referência do WCS, funções
- referência para WCS, funções
- WCS (sistema de cores do Windows), calibragem do dispositivo
- WCS (sistema de cores do Windows), calibragem do dispositivo
- gerenciamento de cores de imagem, calibragem de dispositivo
- gerenciamento de cores, calibragem do dispositivo
- cores, calibragem do dispositivo
- Referência do WCS, calibragem do dispositivo
- referência para WCS, calibragem de dispositivo
- WCS (sistema de cores do Windows), caracterização
- WCS (sistema de cores do Windows), caracterização
- gerenciamento de cores de imagem, caracterização
- gerenciamento de cores, caracterização
- cores, caracterização
- Referência do WCS, caracterização
- referência para WCS, caracterization
- calibragem do dispositivo
- calibragem
- caracterização
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3367bbc6385cc21c8dbff3a88bed685616fb3f29
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "105762246"
---
# <a name="device-calibration-and-characterization-functions"></a><span data-ttu-id="a5e9d-127">Funções de calibragem e caracterização de dispositivo</span><span class="sxs-lookup"><span data-stu-id="a5e9d-127">Device Calibration and Characterization Functions</span></span>

<span data-ttu-id="a5e9d-128">As funções a seguir são úteis para a gravação de ferramentas de calibragem de dispositivo e de caracterização necessárias para instalar e calibrar dispositivos de exibição de cor, como monitores e impressoras.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-128">The following functions are useful for writing device calibration and characterization tools needed for installing and calibrating color display devices such as monitors and printers.</span></span>



| <span data-ttu-id="a5e9d-129">Função</span><span class="sxs-lookup"><span data-stu-id="a5e9d-129">Function</span></span> | <span data-ttu-id="a5e9d-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="a5e9d-130">Description</span></span> |
|-|-|
| [<span data-ttu-id="a5e9d-131">**CloseColorProfile**</span><span class="sxs-lookup"><span data-stu-id="a5e9d-131">**CloseColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-closecolorprofile) | <span data-ttu-id="a5e9d-132">Fecha um identificador de perfil aberto.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-132">Closes an open profile handle.</span></span> |
| [<span data-ttu-id="a5e9d-133">**CreateDeviceLinkProfile**</span><span class="sxs-lookup"><span data-stu-id="a5e9d-133">**CreateDeviceLinkProfile**</span></span>](/windows/win32/api/icm/nf-icm-createdevicelinkprofile) | <span data-ttu-id="a5e9d-134">Cria um *perfil de link de dispositivo* do consórcio de cor internacional (ICC) a partir de um conjunto de perfis de cor, usando as tentativas especificadas.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-134">Creates an International Color Consortium (ICC) *device link profile* from a set of color profiles, using the specified intents.</span></span> |
| [<span data-ttu-id="a5e9d-135">**GetColorProfileElement**</span><span class="sxs-lookup"><span data-stu-id="a5e9d-135">**GetColorProfileElement**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | <span data-ttu-id="a5e9d-136">Copia dados de um elemento de perfil marcado especificado de um perfil de cor especificado em um buffer.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-136">Copies data from a specified tagged profile element of a specified color profile into a buffer.</span></span> |
| [<span data-ttu-id="a5e9d-137">**GetColorProfileElementTag**</span><span class="sxs-lookup"><span data-stu-id="a5e9d-137">**GetColorProfileElementTag**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | <span data-ttu-id="a5e9d-138">Recupera o nome de marca especificado por *dwIndex* na tabela de marcas de um perfil de cor ICC (International Color Consortium) específico, em que *dwIndex* é um índice de base um para essa tabela.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-138">Retrieves the tag name specified by *dwIndex* in the tag table of a given International Color Consortium (ICC) color profile, where *dwIndex* is a one-based index into that table.</span></span> |
| [<span data-ttu-id="a5e9d-139">**GetColorProfileFromHandle**</span><span class="sxs-lookup"><span data-stu-id="a5e9d-139">**GetColorProfileFromHandle**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofilefromhandle)| <span data-ttu-id="a5e9d-140">Recupera o conteúdo do perfil de cor dado um identificador para um perfil de cor aberta.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-140">Retrieves the color profile contents given a handle to an open color profile.</span></span>     |
| [<span data-ttu-id="a5e9d-141">**GetColorProfileHeader**</span><span class="sxs-lookup"><span data-stu-id="a5e9d-141">**GetColorProfileHeader**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | <span data-ttu-id="a5e9d-142">Recupera ou deriva a estrutura de cabeçalho ICC do perfil de cor ICC ou do perfil XML WCS.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-142">Retrieves or derives ICC header structure from either ICC color profile or WCS XML profile.</span></span> <span data-ttu-id="a5e9d-143">Os drivers e os aplicativos devem assumir que retornar **true** apenas indica que um cabeçalho estruturado corretamente é retornado.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-143">Drivers and applications should assume returning **TRUE** only indicates that a properly structured header is returned.</span></span> <span data-ttu-id="a5e9d-144">Cada marca ainda precisará ser validada de forma independente, usando APIs ICM2 herdadas ou APIs de esquema XML.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-144">Each tag will still need to be validated independently using either legacy ICM2 APIs or XML schema APIs.</span></span> |
| [<span data-ttu-id="a5e9d-145">**GetCountColorProfileElements**</span><span class="sxs-lookup"><span data-stu-id="a5e9d-145">**GetCountColorProfileElements**</span></span>](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | <span data-ttu-id="a5e9d-146">Recupera o número de elementos marcados em um determinado perfil de cor.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-146">Retrieves the number of tagged elements in a given color profile.</span></span> |
| [<span data-ttu-id="a5e9d-147">**GetPS2ColorRenderingDictionary**</span><span class="sxs-lookup"><span data-stu-id="a5e9d-147">**GetPS2ColorRenderingDictionary**</span></span>](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | <span data-ttu-id="a5e9d-148">Recupera o dicionário de renderização de cor PostScript Nível 2 do perfil de cor ICC especificado.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-148">Retrieves the PostScript Level 2 color rendering dictionary from the specified ICC color profile.</span></span> |
| [<span data-ttu-id="a5e9d-149">**GetPS2ColorRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="a5e9d-149">**GetPS2ColorRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | <span data-ttu-id="a5e9d-150">Recupera a [tentativa de renderização](r.md) de cor PostScript Nível 2 de um perfil de cor ICC.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-150">Retrieves the PostScript Level 2 color [rendering intent](r.md) from an ICC color profile.</span></span> |
| [<span data-ttu-id="a5e9d-151">**GetPS2ColorSpaceArray**</span><span class="sxs-lookup"><span data-stu-id="a5e9d-151">**GetPS2ColorSpaceArray**</span></span>](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | <span data-ttu-id="a5e9d-152">Recupera a matriz de espaço de [cores](c.md) de nível 2 PostScript de um perfil de cor ICC.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-152">Retrieves the PostScript Level 2 [color space](c.md) array from an ICC color profile.</span></span> |
| [<span data-ttu-id="a5e9d-153">**IsColorProfileTagPresent**</span><span class="sxs-lookup"><span data-stu-id="a5e9d-153">**IsColorProfileTagPresent**</span></span>](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | <span data-ttu-id="a5e9d-154">Relata se uma marca especificada do consórcio de cor internacional (ICC) está presente no perfil de cor especificado.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-154">Reports whether a specified International Color Consortium (ICC) tag is present in the specified color profile.</span></span> |
| [<span data-ttu-id="a5e9d-155">**IsColorProfileValid**</span><span class="sxs-lookup"><span data-stu-id="a5e9d-155">**IsColorProfileValid**</span></span>](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | <span data-ttu-id="a5e9d-156">Permite que você determine se o perfil especificado é um perfil ICC (International Color Consortium) válido ou um identificador de perfil válido do WCS (sistema de cores do Windows) que pode ser usado para o gerenciamento de cores.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-156">Allows you to determine whether the specified profile is a valid International Color Consortium (ICC) profile, or a valid Windows Color System (WCS) profile handle that can be used for color management.</span></span> |
| [<span data-ttu-id="a5e9d-157">**OpenColorProfileW**</span><span class="sxs-lookup"><span data-stu-id="a5e9d-157">**OpenColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-opencolorprofilew) | <span data-ttu-id="a5e9d-158">Cria um identificador para um perfil de cor especificado.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-158">Creates a handle to a specified color profile.</span></span> <span data-ttu-id="a5e9d-159">O identificador pode então ser usado em outras funções de gerenciamento de perfil.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-159">The handle can then be used in other profile management functions.</span></span> |
| [<span data-ttu-id="a5e9d-160">**SetColorProfileElement**</span><span class="sxs-lookup"><span data-stu-id="a5e9d-160">**SetColorProfileElement**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | <span data-ttu-id="a5e9d-161">Define os dados do elemento para um elemento de perfil marcado em um perfil de cor ICC.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-161">Sets the element data for a tagged profile element in an ICC color profile.</span></span> |
| [<span data-ttu-id="a5e9d-162">**SetColorProfileElementReference**</span><span class="sxs-lookup"><span data-stu-id="a5e9d-162">**SetColorProfileElementReference**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | <span data-ttu-id="a5e9d-163">Cria em um perfil de cor ICC especificado uma nova marca que faz referência aos mesmos dados de uma marca existente.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-163">Creates in a specified ICC color profile a new tag that references the same data as an existing tag.</span></span> |
| [<span data-ttu-id="a5e9d-164">**SetColorProfileElementSize**</span><span class="sxs-lookup"><span data-stu-id="a5e9d-164">**SetColorProfileElementSize**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | <span data-ttu-id="a5e9d-165">Define o tamanho de um elemento marcado em um perfil de cor ICC.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-165">Sets the size of a tagged element in an ICC color profile.</span></span> |
| [<span data-ttu-id="a5e9d-166">**SetColorProfileHeader**</span><span class="sxs-lookup"><span data-stu-id="a5e9d-166">**SetColorProfileHeader**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | <span data-ttu-id="a5e9d-167">Define os dados de cabeçalho em um perfil de cor ICC especificado.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-167">Sets the header data in a specified ICC color profile.</span></span> |
| [<span data-ttu-id="a5e9d-168">**WcsGetCalibrationManagementState**</span><span class="sxs-lookup"><span data-stu-id="a5e9d-168">**WcsGetCalibrationManagementState**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | <span data-ttu-id="a5e9d-169">Determina se o gerenciamento do sistema do estado de calibragem de exibição está habilitado.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-169">Determines whether system management of the display calibration state is enabled.</span></span> |
| [<span data-ttu-id="a5e9d-170">**WcsSetCalibrationManagementState**</span><span class="sxs-lookup"><span data-stu-id="a5e9d-170">**WcsSetCalibrationManagementState**</span></span>](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | <span data-ttu-id="a5e9d-171">Determina se o gerenciamento do sistema do estado de calibragem de exibição está habilitado.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-171">Determines whether system management of the display calibration state is enabled.</span></span> |



 

 

 




