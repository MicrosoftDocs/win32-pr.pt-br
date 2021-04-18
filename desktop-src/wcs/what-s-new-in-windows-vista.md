---
title: Novidades no Windows Vista
description: A versão 1,0 do ICM (Image Color Management) foi fornecida no Microsoft Windows 95 e fornece recursos básicos de gerenciamento de cores em contextos de dispositivo do Windows.
ms.assetid: 3079f84c-0d6c-4f87-a041-de86f5f7d99b
keywords:
- WCS (sistema de cores do Windows), Windows Vista
- WCS (sistema de cores do Windows), Windows Vista
- gerenciamento de cores de imagem, Windows Vista
- gerenciamento de cores, Windows Vista
- cores, Windows Vista
- WCS (sistema de cores do Windows), sistemas operacionais
- WCS (sistema de cores do Windows), sistemas operacionais
- gerenciamento de cores de imagem, sistemas operacionais
- gerenciamento de cores, sistemas operacionais
- cores, sistemas operacionais
- ICM (Gerenciamento de cores de imagem)
- ICM (gerenciamento de cores de imagem)
- Gerenciamento de cores do Windows Vista
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b889dd0ba3b044f0d0f158bd2364f5c3216ec39
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "105814619"
---
# <a name="whats-new-in-windows-vista"></a><span data-ttu-id="836a9-116">Novidades no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="836a9-116">What's New in Windows Vista</span></span>

<span data-ttu-id="836a9-117">A versão 1,0 do ICM (Image Color Management) foi fornecida no Microsoft Windows 95 e fornece recursos básicos de gerenciamento de cores em contextos de dispositivo do Windows.</span><span class="sxs-lookup"><span data-stu-id="836a9-117">Version 1.0 of Image Color Management (ICM) was delivered in Microsoft Windows 95, and provides basic color management capabilities within Windows device contexts.</span></span>

<span data-ttu-id="836a9-118">O ICM versão 2,0 foi fornecido no Windows 98, no Windows Millennium Edition, no Windows 2000 e no WindowsXP e incluía uma variedade de novas funções que implementaram o gerenciamento de cores fora dos contextos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="836a9-118">ICM version 2.0 was delivered in Windows 98, Windows Millennium Edition, Windows 2000, and WindowsXP and included a variety of new functions that implemented color management outside of device contexts.</span></span> <span data-ttu-id="836a9-119">Essas novas funções foram adequadas para requisitos de gerenciamento de cores mais exigentes e forneciam mais controle sobre o processo de gerenciamento de cores.</span><span class="sxs-lookup"><span data-stu-id="836a9-119">These new functions were suitable for more demanding color management requirements, and gave applications greater control over the color-management process.</span></span>

<span data-ttu-id="836a9-120">Com o lançamento do Windows Vista, o ICM 2,0 agora está incluído no WCS (sistema de cores do Windows) 1,0, que adiciona mais funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="836a9-120">With the release of Windows Vista, ICM 2.0 is now included in Windows Color System (WCS) 1.0, which adds more functionality.</span></span> <span data-ttu-id="836a9-121">A tabela a seguir lista as novas interfaces de programação de aplicativo (API) que acompanham o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="836a9-121">The following table lists new application programming interfaces (API) that ship in Windows Vista.</span></span>

## <a name="new-api-shipping-in-windows-vista"></a><span data-ttu-id="836a9-122">Novo envio de API no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="836a9-122">New API Shipping in Windows Vista</span></span>



<span data-ttu-id="836a9-123">Enumerações</span><span class="sxs-lookup"><span data-stu-id="836a9-123">Enumerations</span></span>

<span data-ttu-id="836a9-124">Nome da API</span><span class="sxs-lookup"><span data-stu-id="836a9-124">API Name</span></span>

<span data-ttu-id="836a9-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="836a9-125">Header</span></span>

<span data-ttu-id="836a9-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="836a9-126">Library</span></span>

[<span data-ttu-id="836a9-127">**COLORDATATYPE**</span><span class="sxs-lookup"><span data-stu-id="836a9-127">**COLORDATATYPE**</span></span>](/windows/win32/api/icm/ne-icm-colordatatype)

<span data-ttu-id="836a9-128">ICM. h</span><span class="sxs-lookup"><span data-stu-id="836a9-128">icm.h</span></span>

<span data-ttu-id="836a9-129">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="836a9-129">mscms.lib</span></span>

[<span data-ttu-id="836a9-130">**COLORPROFILESUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="836a9-130">**COLORPROFILESUBTYPE**</span></span>](/windows/win32/api/icm/ne-icm-colorprofilesubtype)

<span data-ttu-id="836a9-131">ICM. h</span><span class="sxs-lookup"><span data-stu-id="836a9-131">icm.h</span></span>

<span data-ttu-id="836a9-132">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="836a9-132">mscms.lib</span></span>

[<span data-ttu-id="836a9-133">**COLORPROFILETYPE**</span><span class="sxs-lookup"><span data-stu-id="836a9-133">**COLORPROFILETYPE**</span></span>](/windows/win32/api/icm/ne-icm-colorprofiletype)

<span data-ttu-id="836a9-134">ICM. h</span><span class="sxs-lookup"><span data-stu-id="836a9-134">icm.h</span></span>

<span data-ttu-id="836a9-135">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="836a9-135">mscms.lib</span></span>

[<span data-ttu-id="836a9-136">**\_escopo de \_ Gerenciamento de perfil do WCS \_**</span><span class="sxs-lookup"><span data-stu-id="836a9-136">**WCS\_PROFILE\_MANAGEMENT\_SCOPE**</span></span>](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope)

<span data-ttu-id="836a9-137">ICM. h</span><span class="sxs-lookup"><span data-stu-id="836a9-137">icm.h</span></span>

<span data-ttu-id="836a9-138">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="836a9-138">mscms.lib</span></span>



 



<span data-ttu-id="836a9-139">Funções</span><span class="sxs-lookup"><span data-stu-id="836a9-139">Functions</span></span>

<span data-ttu-id="836a9-140">Nome da API</span><span class="sxs-lookup"><span data-stu-id="836a9-140">API Name</span></span>

<span data-ttu-id="836a9-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="836a9-141">Header</span></span>

<span data-ttu-id="836a9-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="836a9-142">Library</span></span>

[<span data-ttu-id="836a9-143">**WcsAssociateColorProfileWithDevice**</span><span class="sxs-lookup"><span data-stu-id="836a9-143">**WcsAssociateColorProfileWithDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

<span data-ttu-id="836a9-144">ICM. h</span><span class="sxs-lookup"><span data-stu-id="836a9-144">icm.h</span></span>

<span data-ttu-id="836a9-145">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="836a9-145">mscms.lib</span></span>

[<span data-ttu-id="836a9-146">**WcsCheckColors**</span><span class="sxs-lookup"><span data-stu-id="836a9-146">**WcsCheckColors**</span></span>](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

<span data-ttu-id="836a9-147">ICM. h</span><span class="sxs-lookup"><span data-stu-id="836a9-147">icm.h</span></span>

<span data-ttu-id="836a9-148">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="836a9-148">mscms.lib</span></span>

[<span data-ttu-id="836a9-149">**WcsCreateIccProfile**</span><span class="sxs-lookup"><span data-stu-id="836a9-149">**WcsCreateIccProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)

<span data-ttu-id="836a9-150">ICM. h</span><span class="sxs-lookup"><span data-stu-id="836a9-150">icm.h</span></span>

<span data-ttu-id="836a9-151">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="836a9-151">mscms.lib</span></span>

[<span data-ttu-id="836a9-152">**WcsDisassociateColorProfileFromDevice**</span><span class="sxs-lookup"><span data-stu-id="836a9-152">**WcsDisassociateColorProfileFromDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice)

<span data-ttu-id="836a9-153">ICM. h</span><span class="sxs-lookup"><span data-stu-id="836a9-153">icm.h</span></span>

<span data-ttu-id="836a9-154">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="836a9-154">mscms.lib</span></span>

[<span data-ttu-id="836a9-155">**WcsEnumColorProfiles**</span><span class="sxs-lookup"><span data-stu-id="836a9-155">**WcsEnumColorProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)

<span data-ttu-id="836a9-156">ICM. h</span><span class="sxs-lookup"><span data-stu-id="836a9-156">icm.h</span></span>

<span data-ttu-id="836a9-157">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="836a9-157">mscms.lib</span></span>

[<span data-ttu-id="836a9-158">**WcsEnumColorProfilesSize**</span><span class="sxs-lookup"><span data-stu-id="836a9-158">**WcsEnumColorProfilesSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)

<span data-ttu-id="836a9-159">ICM. h</span><span class="sxs-lookup"><span data-stu-id="836a9-159">icm.h</span></span>

<span data-ttu-id="836a9-160">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="836a9-160">mscms.lib</span></span>

[<span data-ttu-id="836a9-161">**WcsGetDefaultColorProfile**</span><span class="sxs-lookup"><span data-stu-id="836a9-161">**WcsGetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)

<span data-ttu-id="836a9-162">ICM. h</span><span class="sxs-lookup"><span data-stu-id="836a9-162">icm.h</span></span>

<span data-ttu-id="836a9-163">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="836a9-163">mscms.lib</span></span>

[<span data-ttu-id="836a9-164">**WcsGetDefaultColorProfileSize**</span><span class="sxs-lookup"><span data-stu-id="836a9-164">**WcsGetDefaultColorProfileSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize)

<span data-ttu-id="836a9-165">ICM. h</span><span class="sxs-lookup"><span data-stu-id="836a9-165">icm.h</span></span>

<span data-ttu-id="836a9-166">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="836a9-166">mscms.lib</span></span>

[<span data-ttu-id="836a9-167">**WcsGetDefaultRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="836a9-167">**WcsGetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

<span data-ttu-id="836a9-168">ICM. h</span><span class="sxs-lookup"><span data-stu-id="836a9-168">icm.h</span></span>

<span data-ttu-id="836a9-169">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="836a9-169">mscms.lib</span></span>

[<span data-ttu-id="836a9-170">**WcsGetUsePerUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="836a9-170">**WcsGetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

<span data-ttu-id="836a9-171">ICM. h</span><span class="sxs-lookup"><span data-stu-id="836a9-171">icm.h</span></span>

<span data-ttu-id="836a9-172">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="836a9-172">mscms.lib</span></span>

[<span data-ttu-id="836a9-173">**WcsOpenColorProfileW**</span><span class="sxs-lookup"><span data-stu-id="836a9-173">**WcsOpenColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew)

<span data-ttu-id="836a9-174">ICM. h</span><span class="sxs-lookup"><span data-stu-id="836a9-174">icm.h</span></span>

<span data-ttu-id="836a9-175">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="836a9-175">mscms.lib</span></span>

[<span data-ttu-id="836a9-176">**WcsSetDefaultColorProfile**</span><span class="sxs-lookup"><span data-stu-id="836a9-176">**WcsSetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile)

<span data-ttu-id="836a9-177">ICM. h</span><span class="sxs-lookup"><span data-stu-id="836a9-177">icm.h</span></span>

<span data-ttu-id="836a9-178">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="836a9-178">mscms.lib</span></span>

[<span data-ttu-id="836a9-179">**WcsSetDefaultRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="836a9-179">**WcsSetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent)

<span data-ttu-id="836a9-180">ICM. h</span><span class="sxs-lookup"><span data-stu-id="836a9-180">icm.h</span></span>

<span data-ttu-id="836a9-181">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="836a9-181">mscms.lib</span></span>

[<span data-ttu-id="836a9-182">**WcsSetUsePerUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="836a9-182">**WcsSetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)

<span data-ttu-id="836a9-183">ICM. h</span><span class="sxs-lookup"><span data-stu-id="836a9-183">icm.h</span></span>

<span data-ttu-id="836a9-184">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="836a9-184">mscms.lib</span></span>

[<span data-ttu-id="836a9-185">**WcsTranslateColors**</span><span class="sxs-lookup"><span data-stu-id="836a9-185">**WcsTranslateColors**</span></span>](/windows/win32/api/icm/nf-icm-wcstranslatecolors)

<span data-ttu-id="836a9-186">ICM. h</span><span class="sxs-lookup"><span data-stu-id="836a9-186">icm.h</span></span>

<span data-ttu-id="836a9-187">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="836a9-187">mscms.lib</span></span>



 



<span data-ttu-id="836a9-188">Interfaces e suas funções</span><span class="sxs-lookup"><span data-stu-id="836a9-188">Interfaces and Their Functions</span></span>

<span data-ttu-id="836a9-189">Nome da API</span><span class="sxs-lookup"><span data-stu-id="836a9-189">API Name</span></span>

<span data-ttu-id="836a9-190">parâmetro</span><span class="sxs-lookup"><span data-stu-id="836a9-190">Header</span></span>

<span data-ttu-id="836a9-191">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="836a9-191">Library</span></span>

[<span data-ttu-id="836a9-192">**IDeviceModelPlugin**</span><span class="sxs-lookup"><span data-stu-id="836a9-192">**IDeviceModelPlugin**</span></span>](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin)

<span data-ttu-id="836a9-193">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="836a9-193">WcsPlugIn.h</span></span>

<span data-ttu-id="836a9-194">N/D</span><span class="sxs-lookup"><span data-stu-id="836a9-194">N/A</span></span>

[<span data-ttu-id="836a9-195">**IDeviceModelPlugin::ColorimetricToDeviceColors**</span><span class="sxs-lookup"><span data-stu-id="836a9-195">**IDeviceModelPlugin::ColorimetricToDeviceColors**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolors)

<span data-ttu-id="836a9-196">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="836a9-196">WcsPlugIn.h</span></span>

<span data-ttu-id="836a9-197">N/D</span><span class="sxs-lookup"><span data-stu-id="836a9-197">N/A</span></span>

[<span data-ttu-id="836a9-198">**IDeviceModelPlugin::ColorimetricToDeviceColorsWithBlack**</span><span class="sxs-lookup"><span data-stu-id="836a9-198">**IDeviceModelPlugin::ColorimetricToDeviceColorsWithBlack**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolorswithblack)

<span data-ttu-id="836a9-199">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="836a9-199">WcsPlugIn.h</span></span>

<span data-ttu-id="836a9-200">N/D</span><span class="sxs-lookup"><span data-stu-id="836a9-200">N/A</span></span>

[<span data-ttu-id="836a9-201">**IDeviceModelPlugin::D eviceToColorimetricColors**</span><span class="sxs-lookup"><span data-stu-id="836a9-201">**IDeviceModelPlugin::DeviceToColorimetricColors**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-devicetocolorimetriccolors)

<span data-ttu-id="836a9-202">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="836a9-202">WcsPlugIn.h</span></span>

<span data-ttu-id="836a9-203">N/D</span><span class="sxs-lookup"><span data-stu-id="836a9-203">N/A</span></span>

[<span data-ttu-id="836a9-204">**IDeviceModelPlugin::GetGamutBoundaryMesh**</span><span class="sxs-lookup"><span data-stu-id="836a9-204">**IDeviceModelPlugin::GetGamutBoundaryMesh**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymesh)

<span data-ttu-id="836a9-205">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="836a9-205">WcsPlugIn.h</span></span>

<span data-ttu-id="836a9-206">N/D</span><span class="sxs-lookup"><span data-stu-id="836a9-206">N/A</span></span>

[<span data-ttu-id="836a9-207">**IDeviceModelPlugin::GetGamutBoundaryMeshSize**</span><span class="sxs-lookup"><span data-stu-id="836a9-207">**IDeviceModelPlugin::GetGamutBoundaryMeshSize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymeshsize)

<span data-ttu-id="836a9-208">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="836a9-208">WcsPlugIn.h</span></span>

<span data-ttu-id="836a9-209">N/D</span><span class="sxs-lookup"><span data-stu-id="836a9-209">N/A</span></span>

[<span data-ttu-id="836a9-210">**IDeviceModelPlugin::GetNeutralAxis**</span><span class="sxs-lookup"><span data-stu-id="836a9-210">**IDeviceModelPlugin::GetNeutralAxis**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxis)

<span data-ttu-id="836a9-211">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="836a9-211">WcsPlugIn.h</span></span>

<span data-ttu-id="836a9-212">N/D</span><span class="sxs-lookup"><span data-stu-id="836a9-212">N/A</span></span>

[<span data-ttu-id="836a9-213">**IDeviceModelPlugin::GetNeutralAxisSize**</span><span class="sxs-lookup"><span data-stu-id="836a9-213">**IDeviceModelPlugin::GetNeutralAxisSize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxissize)

<span data-ttu-id="836a9-214">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="836a9-214">WcsPlugIn.h</span></span>

<span data-ttu-id="836a9-215">N/D</span><span class="sxs-lookup"><span data-stu-id="836a9-215">N/A</span></span>

[<span data-ttu-id="836a9-216">**IDeviceModelPlugin::GetNumChannels**</span><span class="sxs-lookup"><span data-stu-id="836a9-216">**IDeviceModelPlugin::GetNumChannels**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getnumchannels)

<span data-ttu-id="836a9-217">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="836a9-217">WcsPlugIn.h</span></span>

<span data-ttu-id="836a9-218">N/D</span><span class="sxs-lookup"><span data-stu-id="836a9-218">N/A</span></span>

[<span data-ttu-id="836a9-219">**IDeviceModelPlugin::GetPrimarySamples**</span><span class="sxs-lookup"><span data-stu-id="836a9-219">**IDeviceModelPlugin::GetPrimarySamples**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getprimarysamples)

<span data-ttu-id="836a9-220">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="836a9-220">WcsPlugIn.h</span></span>

<span data-ttu-id="836a9-221">N/D</span><span class="sxs-lookup"><span data-stu-id="836a9-221">N/A</span></span>

[<span data-ttu-id="836a9-222">**IDeviceModelPlugin:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="836a9-222">**IDeviceModelPlugin::Initialize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-initialize)

<span data-ttu-id="836a9-223">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="836a9-223">WcsPlugIn.h</span></span>

<span data-ttu-id="836a9-224">N/D</span><span class="sxs-lookup"><span data-stu-id="836a9-224">N/A</span></span>

[<span data-ttu-id="836a9-225">**IDeviceModelPlugin::SetTransformDeviceModelInfo**</span><span class="sxs-lookup"><span data-stu-id="836a9-225">**IDeviceModelPlugin::SetTransformDeviceModelInfo**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-settransformdevicemodelinfo)

<span data-ttu-id="836a9-226">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="836a9-226">WcsPlugIn.h</span></span>

<span data-ttu-id="836a9-227">N/D</span><span class="sxs-lookup"><span data-stu-id="836a9-227">N/A</span></span>

[<span data-ttu-id="836a9-228">**IGamutMapModelPlugin**</span><span class="sxs-lookup"><span data-stu-id="836a9-228">**IGamutMapModelPlugin**</span></span>](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-igamutmapmodelplugin)

<span data-ttu-id="836a9-229">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="836a9-229">WcsPlugIn.h</span></span>

<span data-ttu-id="836a9-230">N/D</span><span class="sxs-lookup"><span data-stu-id="836a9-230">N/A</span></span>

[<span data-ttu-id="836a9-231">**IGamutMapModelPlugin:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="836a9-231">**IGamutMapModelPlugin::Initialize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-initialize)

<span data-ttu-id="836a9-232">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="836a9-232">WcsPlugIn.h</span></span>

<span data-ttu-id="836a9-233">N/D</span><span class="sxs-lookup"><span data-stu-id="836a9-233">N/A</span></span>

[<span data-ttu-id="836a9-234">**IGamutMapModelPlugin::SourceToDestinationAppearanceColors**</span><span class="sxs-lookup"><span data-stu-id="836a9-234">**IGamutMapModelPlugin::SourceToDestinationAppearanceColors**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-sourcetodestinationappearancecolors)

<span data-ttu-id="836a9-235">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="836a9-235">WcsPlugIn.h</span></span>

<span data-ttu-id="836a9-236">N/D</span><span class="sxs-lookup"><span data-stu-id="836a9-236">N/A</span></span>



 



<span data-ttu-id="836a9-237">Estruturas</span><span class="sxs-lookup"><span data-stu-id="836a9-237">Structures</span></span>

<span data-ttu-id="836a9-238">Nome da API</span><span class="sxs-lookup"><span data-stu-id="836a9-238">API Name</span></span>

<span data-ttu-id="836a9-239">parâmetro</span><span class="sxs-lookup"><span data-stu-id="836a9-239">Header</span></span>

<span data-ttu-id="836a9-240">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="836a9-240">Library</span></span>

[<span data-ttu-id="836a9-241">**BlackInformation**</span><span class="sxs-lookup"><span data-stu-id="836a9-241">**BlackInformation**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_blackinformation)

<span data-ttu-id="836a9-242">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="836a9-242">WcsPlugIn.h</span></span>

<span data-ttu-id="836a9-243">N/D</span><span class="sxs-lookup"><span data-stu-id="836a9-243">N/A</span></span>

[<span data-ttu-id="836a9-244">**GamutBoundaryDescription**</span><span class="sxs-lookup"><span data-stu-id="836a9-244">**GamutBoundaryDescription**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutboundarydescription)

<span data-ttu-id="836a9-245">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="836a9-245">WcsPlugIn.h</span></span>

<span data-ttu-id="836a9-246">N/D</span><span class="sxs-lookup"><span data-stu-id="836a9-246">N/A</span></span>

[<span data-ttu-id="836a9-247">**XYZColorF**</span><span class="sxs-lookup"><span data-stu-id="836a9-247">**XYZColorF**</span></span>](https://www.bing.com/search?q=**XYZColorF**)

<span data-ttu-id="836a9-248">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="836a9-248">WcsPlugIn.h</span></span>

<span data-ttu-id="836a9-249">N/D</span><span class="sxs-lookup"><span data-stu-id="836a9-249">N/A</span></span>

[<span data-ttu-id="836a9-250">**JChColorF**</span><span class="sxs-lookup"><span data-stu-id="836a9-250">**JChColorF**</span></span>](https://www.bing.com/search?q=**JChColorF**)

<span data-ttu-id="836a9-251">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="836a9-251">WcsPlugIn.h</span></span>

<span data-ttu-id="836a9-252">N/D</span><span class="sxs-lookup"><span data-stu-id="836a9-252">N/A</span></span>

[<span data-ttu-id="836a9-253">**JabColorF**</span><span class="sxs-lookup"><span data-stu-id="836a9-253">**JabColorF**</span></span>](https://www.bing.com/search?q=**JabColorF**)

<span data-ttu-id="836a9-254">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="836a9-254">WcsPlugIn.h</span></span>

<span data-ttu-id="836a9-255">N/D</span><span class="sxs-lookup"><span data-stu-id="836a9-255">N/A</span></span>

[<span data-ttu-id="836a9-256">**GamutShell**</span><span class="sxs-lookup"><span data-stu-id="836a9-256">**GamutShell**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshell)

<span data-ttu-id="836a9-257">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="836a9-257">WcsPlugIn.h</span></span>

<span data-ttu-id="836a9-258">N/D</span><span class="sxs-lookup"><span data-stu-id="836a9-258">N/A</span></span>

[<span data-ttu-id="836a9-259">**GamutShellTriangle**</span><span class="sxs-lookup"><span data-stu-id="836a9-259">**GamutShellTriangle**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshelltriangle)

<span data-ttu-id="836a9-260">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="836a9-260">WcsPlugIn.h</span></span>

<span data-ttu-id="836a9-261">N/D</span><span class="sxs-lookup"><span data-stu-id="836a9-261">N/A</span></span>

[<span data-ttu-id="836a9-262">**PrimaryJabColors**</span><span class="sxs-lookup"><span data-stu-id="836a9-262">**PrimaryJabColors**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryjabcolors)

<span data-ttu-id="836a9-263">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="836a9-263">WcsPlugIn.h</span></span>

<span data-ttu-id="836a9-264">N/D</span><span class="sxs-lookup"><span data-stu-id="836a9-264">N/A</span></span>

[<span data-ttu-id="836a9-265">**PrimaryXYZColors**</span><span class="sxs-lookup"><span data-stu-id="836a9-265">**PrimaryXYZColors**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryxyzcolors)

<span data-ttu-id="836a9-266">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="836a9-266">WcsPlugIn.h</span></span>

<span data-ttu-id="836a9-267">N/D</span><span class="sxs-lookup"><span data-stu-id="836a9-267">N/A</span></span>



 

 

 