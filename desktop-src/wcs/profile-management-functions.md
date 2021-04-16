---
title: Funções de gerenciamento de perfil
description: Funções de gerenciamento de perfil
ms.assetid: 185863b7-0b74-4c65-97c3-3c60b86d37fd
keywords:
- WCS (sistema de cores do Windows), funções
- WCS (sistema de cores do Windows), funções
- gerenciamento de cores de imagem, funções
- gerenciamento de cores, funções
- cores, funções
- Referência do WCS, funções
- referência para WCS, funções
- WCS (sistema de cores do Windows), perfis
- WCS (sistema de cores do Windows), perfis
- gerenciamento de cores de imagem, perfis
- gerenciamento de cores, perfis
- cores, perfis
- Referência do WCS, perfis
- referência para WCS, perfis
- gerenciamento de perfil
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0e80e300532b20148eef6d9dc362438b6714a3
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "105808411"
---
# <a name="profile-management-functions"></a><span data-ttu-id="7f650-118">Funções de gerenciamento de perfil</span><span class="sxs-lookup"><span data-stu-id="7f650-118">Profile Management Functions</span></span>

## <a name="profile-management-functions"></a><span data-ttu-id="7f650-119">Funções de gerenciamento de perfil</span><span class="sxs-lookup"><span data-stu-id="7f650-119">Profile Management Functions</span></span>

<span data-ttu-id="7f650-120">As seguintes funções de API são úteis no gerenciamento de perfil.</span><span class="sxs-lookup"><span data-stu-id="7f650-120">The following API functions are useful in profile management.</span></span>



| <span data-ttu-id="7f650-121">Função</span><span class="sxs-lookup"><span data-stu-id="7f650-121">Function</span></span>                                                                               | <span data-ttu-id="7f650-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f650-122">Description</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f650-123">**AssociateColorProfileWithDeviceW**</span><span class="sxs-lookup"><span data-stu-id="7f650-123">**AssociateColorProfileWithDeviceW**</span></span>](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)             | <span data-ttu-id="7f650-124">Associa um perfil de cor especificado a um dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="7f650-124">Associates a specified color profile with a specified device.</span></span>                                                              |
| <span data-ttu-id="7f650-125">[**CreateProfileFromLogColorSpaceW**] ((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew)</span><span class="sxs-lookup"><span data-stu-id="7f650-125">[**CreateProfileFromLogColorSpaceW**]((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew)</span></span> | <span data-ttu-id="7f650-126">Converte um [espaço de cor](c.md) lógico em um [perfil de dispositivo](d.md).</span><span class="sxs-lookup"><span data-stu-id="7f650-126">Converts a logical [color space](c.md) to a [device profile](d.md).</span></span> |
| [<span data-ttu-id="7f650-127">**DisassociateColorProfileFromDeviceW**</span><span class="sxs-lookup"><span data-stu-id="7f650-127">**DisassociateColorProfileFromDeviceW**</span></span>](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew) | <span data-ttu-id="7f650-128">Desassocia um perfil de cor especificado a um dispositivo especificado em um computador especificado.</span><span class="sxs-lookup"><span data-stu-id="7f650-128">Disassociates a specified color profile with a specified device on a specified computer.</span></span> |
| [<span data-ttu-id="7f650-129">**EnumColorProfilesW**</span><span class="sxs-lookup"><span data-stu-id="7f650-129">**EnumColorProfilesW**</span></span>](/windows/win32/api/icm/nf-icm-enumcolorprofilesw) | <span data-ttu-id="7f650-130">Enumera todos os perfis que atendem aos critérios de enumeração fornecidos.</span><span class="sxs-lookup"><span data-stu-id="7f650-130">Enumerates all the profiles satisfying the given enumeration criteria.</span></span> |
| [<span data-ttu-id="7f650-131">**GetColorDirectoryW**</span><span class="sxs-lookup"><span data-stu-id="7f650-131">**GetColorDirectoryW**</span></span>](/windows/win32/api/icm/nf-icm-getcolordirectoryw) | <span data-ttu-id="7f650-132">Recupera o caminho do diretório de cores do Windows em um computador especificado.</span><span class="sxs-lookup"><span data-stu-id="7f650-132">Retrieves the path of the Windows COLOR directory on a specified machine.</span></span> |
| [<span data-ttu-id="7f650-133">**GetDeviceGammaRamp**</span><span class="sxs-lookup"><span data-stu-id="7f650-133">**GetDeviceGammaRamp**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getdevicegammaramp)                                       | <span data-ttu-id="7f650-134">Obtém a rampa de gama de placas de exibição de cor direta.</span><span class="sxs-lookup"><span data-stu-id="7f650-134">Gets the gamma ramp from direct color display boards.</span></span>                                                                                                |
| [<span data-ttu-id="7f650-135">**GetStandardColorSpaceProfileW**</span><span class="sxs-lookup"><span data-stu-id="7f650-135">**GetStandardColorSpaceProfileW**</span></span>](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) | <span data-ttu-id="7f650-136">Recupera o perfil de cor registrado para o [espaço de cores](c.md)padrão especificado.</span><span class="sxs-lookup"><span data-stu-id="7f650-136">Retrieves the color profile registered for the specified standard [color space](c.md).</span></span> |
| [<span data-ttu-id="7f650-137">**InstallColorProfileW**</span><span class="sxs-lookup"><span data-stu-id="7f650-137">**InstallColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-installcolorprofilew) | <span data-ttu-id="7f650-138">Instala um determinado perfil para uso em um computador especificado.</span><span class="sxs-lookup"><span data-stu-id="7f650-138">Installs a given profile for use on a specified machine.</span></span> <span data-ttu-id="7f650-139">O perfil também é copiado para o diretório de cores.</span><span class="sxs-lookup"><span data-stu-id="7f650-139">The profile is also copied to the COLOR directory.</span></span> |
| [<span data-ttu-id="7f650-140">**RegisterCMMW**</span><span class="sxs-lookup"><span data-stu-id="7f650-140">**RegisterCMMW**</span></span>](/windows/win32/api/icm/nf-icm-registercmmw) | <span data-ttu-id="7f650-141">Associa um valor de identificação especificado com a DLL do CMM (Dynamic Link Library) do módulo de gerenciamento de cores especificado.</span><span class="sxs-lookup"><span data-stu-id="7f650-141">Associates a specified identification value with the specified color management module dynamic link library (CMM DLL).</span></span> <span data-ttu-id="7f650-142">Quando essa ID aparece em um perfil de cor, o Windows pode localizar o CMM correspondente para criar uma transformação.</span><span class="sxs-lookup"><span data-stu-id="7f650-142">When this ID appears in a color profile, Windows can then locate the corresponding CMM so as to create a transform.</span></span> |
| [<span data-ttu-id="7f650-143">**SetDeviceGammaRamp**</span><span class="sxs-lookup"><span data-stu-id="7f650-143">**SetDeviceGammaRamp**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdevicegammaramp)                                       | <span data-ttu-id="7f650-144">Define a rampa de gama em placas de exibição de cor direta.</span><span class="sxs-lookup"><span data-stu-id="7f650-144">Sets the gamma ramp on direct color display boards.</span></span>                                                                                                  |
| [<span data-ttu-id="7f650-145">**SetStandardColorSpaceProfileW**</span><span class="sxs-lookup"><span data-stu-id="7f650-145">**SetStandardColorSpaceProfileW**</span></span>](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew) | <span data-ttu-id="7f650-146">Registra um perfil especificado para um espaço de [cores](c.md)padrão específico.</span><span class="sxs-lookup"><span data-stu-id="7f650-146">Registers a specified profile for a given standard [color space](c.md).</span></span> <span data-ttu-id="7f650-147">O perfil pode ser consultado usando [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew).</span><span class="sxs-lookup"><span data-stu-id="7f650-147">The profile can be queried using [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew).</span></span> |
| [<span data-ttu-id="7f650-148">**UninstallColorProfileW**</span><span class="sxs-lookup"><span data-stu-id="7f650-148">**UninstallColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-uninstallcolorprofilew) | <span data-ttu-id="7f650-149">Remove um perfil de cor especificado de um computador especificado.</span><span class="sxs-lookup"><span data-stu-id="7f650-149">Removes a specified color profile from a specified computer.</span></span> <span data-ttu-id="7f650-150">Os arquivos associados são excluídos opcionalmente do sistema.</span><span class="sxs-lookup"><span data-stu-id="7f650-150">Associated files are optionally deleted from the system.</span></span> |
| [<span data-ttu-id="7f650-151">**UnregisterCMMW**</span><span class="sxs-lookup"><span data-stu-id="7f650-151">**UnregisterCMMW**</span></span>](/windows/win32/api/icm/nf-icm-unregistercmmw) | <span data-ttu-id="7f650-152">Dissocia um valor de ID especificado de uma determinada biblioteca de vínculo dinâmico (DLL do CMM) do módulo de gerenciamento de cores.</span><span class="sxs-lookup"><span data-stu-id="7f650-152">Dissociates a specified ID value from a given color management module dynamic-link library (CMM DLL).</span></span> |
| [<span data-ttu-id="7f650-153">**WcsAssociateColorProfileWithDevice**</span><span class="sxs-lookup"><span data-stu-id="7f650-153">**WcsAssociateColorProfileWithDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)       | <span data-ttu-id="7f650-154">Associa um perfil de cor WCS especificado a um dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="7f650-154">Associates a specified WCS color profile with a specified device.</span></span>                                                                                    |
| [<span data-ttu-id="7f650-155">**WcsCreateIccProfile**</span><span class="sxs-lookup"><span data-stu-id="7f650-155">**WcsCreateIccProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)                                     | <span data-ttu-id="7f650-156">Converte um perfil WCS em um perfil ICC.</span><span class="sxs-lookup"><span data-stu-id="7f650-156">Converts a WCS profile into an ICC profile.</span></span>                                                                                                          |
| [<span data-ttu-id="7f650-157">**WcsDisassociateColorProfileFromDevice**</span><span class="sxs-lookup"><span data-stu-id="7f650-157">**WcsDisassociateColorProfileFromDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice) | <span data-ttu-id="7f650-158">Desassocia um perfil de cor WCS especificado com um dispositivo especificado em um computador especificado.</span><span class="sxs-lookup"><span data-stu-id="7f650-158">Disassociates a specified WCS color profile with a specified device on a specified computer.</span></span>                                                         |
| [<span data-ttu-id="7f650-159">**WcsEnumColorProfiles**</span><span class="sxs-lookup"><span data-stu-id="7f650-159">**WcsEnumColorProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)                                   | <span data-ttu-id="7f650-160">Enumera todos os perfis de cor que atendem aos critérios de enumeração no escopo de gerenciamento de perfil especificado.</span><span class="sxs-lookup"><span data-stu-id="7f650-160">Enumerates all color profiles that satisfy the enumeration criteria in the specified profile management scope.</span></span>                                       |
| [<span data-ttu-id="7f650-161">**WcsEnumColorProfilesSize**</span><span class="sxs-lookup"><span data-stu-id="7f650-161">**WcsEnumColorProfilesSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)                           | <span data-ttu-id="7f650-162">Retorna o tamanho, em bytes, do buffer exigido pela função [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) para enumerar perfis de cor.</span><span class="sxs-lookup"><span data-stu-id="7f650-162">Returns the size, in bytes, of the buffer required by the [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) function to enumerate color profiles.</span></span> |
| [<span data-ttu-id="7f650-163">**WcsGetDefaultColorProfile**</span><span class="sxs-lookup"><span data-stu-id="7f650-163">**WcsGetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)                         | <span data-ttu-id="7f650-164">Recupera o perfil de cor padrão para um dispositivo ou o padrão independente do dispositivo, se o dispositivo não for especificado.</span><span class="sxs-lookup"><span data-stu-id="7f650-164">Retrieves the default color profile for a device, or the device-independent default if the device is not specified.</span></span>                                  |
| [<span data-ttu-id="7f650-165">**WcsGetDefaultColorProfileSize**</span><span class="sxs-lookup"><span data-stu-id="7f650-165">**WcsGetDefaultColorProfileSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) | <span data-ttu-id="7f650-166">Retorna o tamanho, em bytes, do nome do perfil de cor padrão para um dispositivo, incluindo o terminador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="7f650-166">Returns the size, in bytes, of the default color profile name for a device, including the **NULL** terminator.</span></span>                                       |
| [<span data-ttu-id="7f650-167">**WcsGetDefaultRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="7f650-167">**WcsGetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | <span data-ttu-id="7f650-168">Recupera a tentativa de renderização padrão no escopo de gerenciamento de perfil especificado.</span><span class="sxs-lookup"><span data-stu-id="7f650-168">Retrieves the default rendering intent in the specified profile management scope.</span></span>                                                                    |
| [<span data-ttu-id="7f650-169">**WcsGetUsePerUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="7f650-169">**WcsGetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | <span data-ttu-id="7f650-170">Determina se o usuário optou por usar uma lista de associação de perfil por usuário para o dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="7f650-170">Determines whether the user has chosen to use a per-user profile association list for the specified device.</span></span>                                          |
| [<span data-ttu-id="7f650-171">**WcsOpenColorProfileW**</span><span class="sxs-lookup"><span data-stu-id="7f650-171">**WcsOpenColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew) | <span data-ttu-id="7f650-172">Cria um identificador para um perfil de cor especificado.</span><span class="sxs-lookup"><span data-stu-id="7f650-172">Creates a handle to a specified color profile.</span></span>                                                                                                       |
| [<span data-ttu-id="7f650-173">**WcsSetDefaultColorProfile**</span><span class="sxs-lookup"><span data-stu-id="7f650-173">**WcsSetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile) | <span data-ttu-id="7f650-174">Define o nome do perfil de cor padrão do tipo de perfil especificado no escopo de gerenciamento de perfil especificado.</span><span class="sxs-lookup"><span data-stu-id="7f650-174">Sets the default color profile name of the specified profile type in the specified profile management scope.</span></span>                                         |
| [<span data-ttu-id="7f650-175">**WcsSetDefaultRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="7f650-175">**WcsSetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent) | <span data-ttu-id="7f650-176">Define a tentativa de renderização padrão no escopo de gerenciamento de perfil especificado.</span><span class="sxs-lookup"><span data-stu-id="7f650-176">Sets the default rendering intent in the specified profile management scope.</span></span>                                                                         |
| [<span data-ttu-id="7f650-177">**WcsSetUsePerUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="7f650-177">**WcsSetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)                           | <span data-ttu-id="7f650-178">Permite que o usuário especifique se deseja usar uma lista de associação de perfil por usuário para o dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="7f650-178">Allows the user to specify whether to use a per-user profile association list for the specified device.</span></span>                                              |



 

## <a name="profile-consumption-functions"></a><span data-ttu-id="7f650-179">Funções de consumo de perfil</span><span class="sxs-lookup"><span data-stu-id="7f650-179">Profile Consumption Functions</span></span>

<span data-ttu-id="7f650-180">As APIs de consumo de perfil são aquelas em ICM2 que usam perfis de XML ICC ou WCS, identificadores de perfil ou tentativas de renderização como parâmetros e um conjunto de novas APIs para suporte de perfil WCS para o código de gerenciamento de cores do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7f650-180">The profile consumption APIs are those APIs in ICM2 that take ICC or WCS XML profiles, profile handles, or rendering intents as parameters, and a set of new APIs for WCS profile support for application color management code.</span></span>

 

## <a name="profiles-and-profile-management-functions"></a><span data-ttu-id="7f650-181">Perfis e funções de gerenciamento de perfil</span><span class="sxs-lookup"><span data-stu-id="7f650-181">Profiles and Profile Management Functions</span></span>

<span data-ttu-id="7f650-182">O fluxo de trabalho de gerenciamento de perfil é baseado em APIs ICM2 existentes que são aumentadas para fornecer funcionalidade adicional para a revisão do código do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7f650-182">The profile management workflow is based on existing ICM2 APIs that are augmented to provide additional functionality for revising application code.</span></span>

<span data-ttu-id="7f650-183">Os perfis contêm informações usadas por algoritmos de processamento de cores para converter a cor entre espaços de cores diferentes.</span><span class="sxs-lookup"><span data-stu-id="7f650-183">Profiles contain information used by color processing algorithms to translate color between different color spaces.</span></span> <span data-ttu-id="7f650-184">O gerenciamento de perfil fornece uma maneira de consultar e especificar quais perfis são usados em diferentes estágios pelo modelo de processamento de cores para gerenciar a saída de cores de vários dispositivos periféricos com características de cores diversas.</span><span class="sxs-lookup"><span data-stu-id="7f650-184">Profile management provides a way to query and specify which profiles get used at different stages by the color processing model to manage color output of various peripheral devices with diverse color characteristics.</span></span>

<span data-ttu-id="7f650-185">O gerenciamento de perfil fornece o seguinte conjunto de funcionalidades:</span><span class="sxs-lookup"><span data-stu-id="7f650-185">Profile management provides the following set of functionalities:</span></span>

 

1. <span data-ttu-id="7f650-186">Instalando perfis de cor para uso no sistema.</span><span class="sxs-lookup"><span data-stu-id="7f650-186">Installing color profiles for use in the system.</span></span>

 

2. <span data-ttu-id="7f650-187">Associação de um ou mais perfis de cor instalados a qualquer dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="7f650-187">Associating one or more installed color profiles with any particular device.</span></span>

 

3. <span data-ttu-id="7f650-188">Escolher um perfil de cor padrão de um tipo específico entre os perfis disponíveis para uso em um estágio específico de processamento de cores.</span><span class="sxs-lookup"><span data-stu-id="7f650-188">Choosing a default color profile of a particular type among the profiles available for use in a particular stage of color processing.</span></span> <span data-ttu-id="7f650-189">Isso pode ser para um dispositivo entre os perfis associados a ele, ou entre os perfis instalados no sistema e não específico ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7f650-189">This could be for a device among the profiles associated with it, or among the profiles installed in the system and not device specific.</span></span>

 

4. <span data-ttu-id="7f650-190">Enumerar perfis de cor que satisfaçam critérios específicos entre os perfis instalados no sistema.</span><span class="sxs-lookup"><span data-stu-id="7f650-190">Enumerating color profiles that satisfy particular criteria among the profiles installed in the system.</span></span>

<span data-ttu-id="7f650-191">As extensões de nome de arquivo do perfil WCS são ". CDMP" para DMPs, ". Camp" para acampamentos e ". gmmp" para GMMPs.</span><span class="sxs-lookup"><span data-stu-id="7f650-191">The WCS profile filename extensions are ".cdmp" for DMPs, ".camp" for CAMPs, and ".gmmp" for GMMPs.</span></span>

 

<span data-ttu-id="7f650-192">**Gerenciamento de perfil por usuário e habilitação da execução no contexto LUA**</span><span class="sxs-lookup"><span data-stu-id="7f650-192">**Per-user profile management and enabling execution in LUA context**</span></span>

<span data-ttu-id="7f650-193">A meta do design descrito no documento atual é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="7f650-193">The goal of the design described in the current document is as follows:</span></span>

 

1. <span data-ttu-id="7f650-194">A implementação de ICM2 herdada não oferece suporte para o gerenciamento de perfil por usuário.</span><span class="sxs-lookup"><span data-stu-id="7f650-194">Legacy ICM2 implementation does not provide support for per-user profile management.</span></span> <span data-ttu-id="7f650-195">Usuários diferentes não podem ter suas próprias configurações de perfil.</span><span class="sxs-lookup"><span data-stu-id="7f650-195">Different users cannot have their own profile settings.</span></span> <span data-ttu-id="7f650-196">No Vista, a infraestrutura de gerenciamento do perfil WCS permite que os usuários definam configurações de perfil individuais para a maioria das funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="7f650-196">In Vista, the WCS profile management infrastructure enables users to configure individual profile settings for most functionalities.</span></span>

 

2. <span data-ttu-id="7f650-197">Todas as APIs de gerenciamento de perfil ICM2 herdadas modificam configurações de todo o sistema e exigem privilégios administrativos.</span><span class="sxs-lookup"><span data-stu-id="7f650-197">All legacy ICM2 profile management APIs modify settings system-wide and require administrative privileges.</span></span> <span data-ttu-id="7f650-198">No Windows Vista, todos os usuários são executados em configurações de LUA (conta de usuário com privilégios mínimos) na maioria das vezes, e os administradores podem elevar o privilégio de forma seletiva para executar aplicativos que modificam as configurações de todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="7f650-198">In Windows Vista, all users run in Least-privileged User Account (LUA) settings most of the time, and administrators can elevate privilege selectively to run applications that modify system-wide settings.</span></span> <span data-ttu-id="7f650-199">No gerenciamento de perfil WCS, todas as configurações de perfil por usuário são configuráveis no contexto LUA.</span><span class="sxs-lookup"><span data-stu-id="7f650-199">In WCS profile management, all per-user profile settings are configurable in LUA context.</span></span> <span data-ttu-id="7f650-200">Os aplicativos de gerenciamento de perfil podem ser executados como configurações de LUA, aumentando seu escopo de uso e garantindo que a segurança do sistema não seja comprometida.</span><span class="sxs-lookup"><span data-stu-id="7f650-200">Profile management applications can run as LUA settings, increasing their scope of use and ensuring that security of the system is not compromised.</span></span>

<span data-ttu-id="7f650-201">O gerenciamento de perfil no Vista fornece os seguintes aprimoramentos em relação à infraestrutura de ICM2 herdada:</span><span class="sxs-lookup"><span data-stu-id="7f650-201">Profile management in Vista provides the following enhancements over legacy ICM2 infrastructure:</span></span>

 

1. <span data-ttu-id="7f650-202">Ele habilita a associação de perfil com dispositivos, configurações de perfil padrão e enumeração de perfis no escopo de todo o usuário e do sistema.</span><span class="sxs-lookup"><span data-stu-id="7f650-202">It enables profile association with devices, default profile settings, and enumeration of profiles in both per-user and system-wide scope.</span></span>

 

2. <span data-ttu-id="7f650-203">A instalação de um perfil permanece em todo o sistema e requer privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="7f650-203">Installing a profile remains system wide and requires administrator privileges.</span></span> <span data-ttu-id="7f650-204">Isso é consistente com a instalação do perfil durante a instalação do dispositivo porque a instalação do dispositivo é de todo o sistema e requer privilégios administrativos.</span><span class="sxs-lookup"><span data-stu-id="7f650-204">This is consistent with profile installation during device installation because device installation is system wide and requires administrative privileges.</span></span>

 

<span data-ttu-id="7f650-205">Se os dispositivos podem ser instalados do contexto LUA é específico ao que tem suporte para essa classe de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7f650-205">Whether devices can be installed from LUA context is particular to what is supported for that class of device.</span></span> <span data-ttu-id="7f650-206">Por exemplo, no Vista, é possível fazer a instalação da impressora do contexto LUA se o usuário tiver concedido direitos para copiar arquivos no repositório de drivers por um administrador de domínio usando políticas de repositório de driver.</span><span class="sxs-lookup"><span data-stu-id="7f650-206">For example, in Vista, it is possible to do printer installation from LUA context if the user has been granted rights to copy files into the driver store by a domain administrator using driver store policies.</span></span> <span data-ttu-id="7f650-207">A infraestrutura de gerenciamento do perfil de cores não precisa fazer nada de especial nesse sentido, já que a instalação ocorre no contexto do spooler.</span><span class="sxs-lookup"><span data-stu-id="7f650-207">Color profile management infrastructure doesn't need to do anything special in this regard since the installation happens in spooler context.</span></span>

 

3. <span data-ttu-id="7f650-208">A modificação das configurações de perfil no escopo por usuário pode ser feita no contexto LUA; modificações em todo o sistema exigem privilégios administrativos.</span><span class="sxs-lookup"><span data-stu-id="7f650-208">Modifying profile settings in per-user scope can be done in LUA context; system-wide modifications required administrative privileges.</span></span> <span data-ttu-id="7f650-209">As operações de gerenciamento de perfil que exigem a leitura de informações de configuração podem ser feitas no contexto de LUA para as configurações por usuário e para todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="7f650-209">Profile management operations that require reading configuration information can be done in LUA context for both per-user and system-wide settings.</span></span>

<span data-ttu-id="7f650-210">Escopo de gerenciamento de perfil indica o escopo das operações executadas; por usuário ou por todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="7f650-210">Profile management scope indicates the scope of the operations performed; either per-user or system wide.</span></span>

<span data-ttu-id="7f650-211">Para cada operação, é indicado se pode ser feito a partir do contexto LUA.</span><span class="sxs-lookup"><span data-stu-id="7f650-211">For each operation, it is indicated whether it can be done from LUA context.</span></span> <span data-ttu-id="7f650-212">Se uma operação não puder ser executada no contexto LUA, a API de gerenciamento de perfil correspondente retornará uma falha com acesso negado.</span><span class="sxs-lookup"><span data-stu-id="7f650-212">If an operation cannot be performed in LUA context, the corresponding profile management API returns failure with access denied.</span></span> <span data-ttu-id="7f650-213">Os aplicativos que usam a API, como o painel de controle de gerenciamento de cores, podem permitir que o usuário eleve o contexto administrativo (usando OTS ou a interface do usuário de consentimento) e, em seguida, chame a API do contexto elevado para que a operação seja realizada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="7f650-213">Applications using the API, such as Color Management Control Panel, can enable the user to elevate to administrative context (using OTS or Consent UI), and then call the API from the elevated context so that the operation will succeed.</span></span>



<span data-ttu-id="7f650-214">Operação</span><span class="sxs-lookup"><span data-stu-id="7f650-214">Operation</span></span>

<span data-ttu-id="7f650-215">Escopo de gerenciamento de perfil</span><span class="sxs-lookup"><span data-stu-id="7f650-215">Profile Management Scope</span></span>

<span data-ttu-id="7f650-216">Pré-condição</span><span class="sxs-lookup"><span data-stu-id="7f650-216">Pre-condition</span></span>

<span data-ttu-id="7f650-217">Pós-condição</span><span class="sxs-lookup"><span data-stu-id="7f650-217">Post-condition</span></span>

<span data-ttu-id="7f650-218">Executável no contexto LUA</span><span class="sxs-lookup"><span data-stu-id="7f650-218">Executable in LUA context</span></span>

<span data-ttu-id="7f650-219">$ {ROWSPAN2} $Install do perfil $ {remover} $</span><span class="sxs-lookup"><span data-stu-id="7f650-219">${ROWSPAN2}$Install profile${REMOVE}$</span></span>  

<span data-ttu-id="7f650-220">Todo o sistema</span><span class="sxs-lookup"><span data-stu-id="7f650-220">System wide</span></span>

<span data-ttu-id="7f650-221">Perfil copiado, instalado no sistema e disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="7f650-221">Profile copied, installed into the system, and available for use.</span></span> <span data-ttu-id="7f650-222">O perfil é enumerável em todo o sistema e no escopo do usuário atual para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="7f650-222">Profile is enumerable in system-wide and current-user scope for all users.</span></span>

<span data-ttu-id="7f650-223">Durante a instalação do driver de dispositivo, governada pelas políticas de instalação do driver.</span><span class="sxs-lookup"><span data-stu-id="7f650-223">During device driver installation, governed by driver installation policies.</span></span> <span data-ttu-id="7f650-224">Não, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="7f650-224">No, otherwise.</span></span>

<span data-ttu-id="7f650-225">Usuário atual</span><span class="sxs-lookup"><span data-stu-id="7f650-225">Current user</span></span>

<span data-ttu-id="7f650-226">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="7f650-226">Not supported</span></span>

<span data-ttu-id="7f650-227">$ {ROWSPAN2} $Uninstall do perfil $ {remover} $</span><span class="sxs-lookup"><span data-stu-id="7f650-227">${ROWSPAN2}$Uninstall profile${REMOVE}$</span></span>  

<span data-ttu-id="7f650-228">Todo o sistema</span><span class="sxs-lookup"><span data-stu-id="7f650-228">System wide</span></span>

<span data-ttu-id="7f650-229">O perfil está instalado no sistema</span><span class="sxs-lookup"><span data-stu-id="7f650-229">Profile is installed in the system</span></span>

<span data-ttu-id="7f650-230">Perfil desinstalado do sistema e, opcionalmente, excluído do repositório de perfis.</span><span class="sxs-lookup"><span data-stu-id="7f650-230">Profile uninstalled from the system and optionally deleted from the profile store.</span></span> <span data-ttu-id="7f650-231">O perfil não está mais disponível para uso e não é enumerável em nenhum escopo.</span><span class="sxs-lookup"><span data-stu-id="7f650-231">Profile is no longer available for use and is not enumerable in any scope.</span></span>

<span data-ttu-id="7f650-232">No</span><span class="sxs-lookup"><span data-stu-id="7f650-232">No</span></span>

<span data-ttu-id="7f650-233">Usuário atual</span><span class="sxs-lookup"><span data-stu-id="7f650-233">Current user</span></span>

<span data-ttu-id="7f650-234">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="7f650-234">Not supported</span></span>

<span data-ttu-id="7f650-235">$ {ROWSPAN2} $Associate o perfil com o dispositivo $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7f650-235">${ROWSPAN2}$Associate profile with device${REMOVE}$</span></span>  

<span data-ttu-id="7f650-236">Todo o sistema</span><span class="sxs-lookup"><span data-stu-id="7f650-236">System wide</span></span>

<span data-ttu-id="7f650-237">O perfil está instalado e é do tipo ICC ou CDMP</span><span class="sxs-lookup"><span data-stu-id="7f650-237">Profile is installed and is of type ICC or CDMP</span></span>

<span data-ttu-id="7f650-238">O perfil está disponível para uso com o dispositivo por todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="7f650-238">Profile is available for use with the device by all users.</span></span> <span data-ttu-id="7f650-239">Ele é enumerável, no escopo de todo o sistema e também no escopo do usuário atual para todos os usuários, como associado ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7f650-239">It is enumerable, in system-wide scope and also current-user scope for all users, as associated with the device.</span></span>

<span data-ttu-id="7f650-240">No</span><span class="sxs-lookup"><span data-stu-id="7f650-240">No</span></span>

<span data-ttu-id="7f650-241">Usuário atual</span><span class="sxs-lookup"><span data-stu-id="7f650-241">Current user</span></span>

<span data-ttu-id="7f650-242">O perfil está instalado.</span><span class="sxs-lookup"><span data-stu-id="7f650-242">Profile is installed.</span></span> <span data-ttu-id="7f650-243">Não importa se o perfil já está associado ao dispositivo no escopo de todo o sistema e é do tipo ICC ou CDMP.</span><span class="sxs-lookup"><span data-stu-id="7f650-243">It does not matter whether the profile is already associated to the device in system-wide scope and is of type ICC or CDMP.</span></span>

<span data-ttu-id="7f650-244">O perfil está disponível para uso com o dispositivo pelo usuário atual.</span><span class="sxs-lookup"><span data-stu-id="7f650-244">Profile is available for use with the device by current user.</span></span> <span data-ttu-id="7f650-245">Ele é enumerável somente no escopo do usuário atual (a menos que também haja uma associação em todo o sistema) como associado ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7f650-245">It is enumerable only in current-user scope (unless there is a system-wide association as well) as associated with the device.</span></span>

<span data-ttu-id="7f650-246">Yes</span><span class="sxs-lookup"><span data-stu-id="7f650-246">Yes</span></span>

<span data-ttu-id="7f650-247">$ {ROWSPAN2} $Disassociate o perfil do dispositivo $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7f650-247">${ROWSPAN2}$Disassociate profile from device${REMOVE}$</span></span>  

<span data-ttu-id="7f650-248">Todo o sistema</span><span class="sxs-lookup"><span data-stu-id="7f650-248">System wide</span></span>

<span data-ttu-id="7f650-249">O perfil está associado ao dispositivo no escopo de todo o sistema e é do tipo ICC ou CDMP</span><span class="sxs-lookup"><span data-stu-id="7f650-249">Profile is associated with the device in system-wide scope and is of type ICC or CDMP</span></span>

<span data-ttu-id="7f650-250">O perfil não está mais disponível para uso (exceto para usuários que têm essa associação em seu escopo de usuário atual também).</span><span class="sxs-lookup"><span data-stu-id="7f650-250">Profile is no longer available for use (except for users who have this association in their current-user scope as well).</span></span> <span data-ttu-id="7f650-251">Não é enumerável no escopo de todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="7f650-251">It is not enumerable in system-wide scope.</span></span> <span data-ttu-id="7f650-252">No entanto, pode ser enumerável no escopo do usuário atual, para um usuário que tenha essa associação em seu escopo.</span><span class="sxs-lookup"><span data-stu-id="7f650-252">It could be enumerable in current-user scope though, for a user who has this association in its scope.</span></span>

<span data-ttu-id="7f650-253">No</span><span class="sxs-lookup"><span data-stu-id="7f650-253">No</span></span>

<span data-ttu-id="7f650-254">Usuário atual</span><span class="sxs-lookup"><span data-stu-id="7f650-254">Current user</span></span>

<span data-ttu-id="7f650-255">O perfil está associado ao dispositivo no escopo do usuário atual (independentemente de estar associado no escopo de todo o sistema) e é do tipo ICC ou CDMP.</span><span class="sxs-lookup"><span data-stu-id="7f650-255">Profile is associated with the device in current-user scope (irrespective of whether it is associated in system-wide scope) and is of type ICC or CDMP.</span></span>

<span data-ttu-id="7f650-256">O perfil não está mais disponível para uso ou enumerável como associado ao dispositivo, pelo usuário atual (a menos que ele também esteja associado no escopo de todo o sistema ao dispositivo).</span><span class="sxs-lookup"><span data-stu-id="7f650-256">Profile is no longer available for use, or enumerable as associated to the device, by current user (unless it is also associated in system-wide scope to the device).</span></span>

<span data-ttu-id="7f650-257">Yes</span><span class="sxs-lookup"><span data-stu-id="7f650-257">Yes</span></span>

<span data-ttu-id="7f650-258">$ {ROWSPAN2} $Set o perfil para um tipo (DMP ou ICC) como padrão para um dispositivo $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7f650-258">${ROWSPAN2}$Set profile for a type (DMP or ICC) as default for a device${REMOVE}$</span></span>  

<span data-ttu-id="7f650-259">Todo o sistema</span><span class="sxs-lookup"><span data-stu-id="7f650-259">System wide</span></span>

<span data-ttu-id="7f650-260">O perfil é do tipo ICC ou CDMP</span><span class="sxs-lookup"><span data-stu-id="7f650-260">Profile is of type ICC or CDMP</span></span>

<span data-ttu-id="7f650-261">O perfil é usado por padrão para o tipo específico com o dispositivo, para todos os usuários, exceto aqueles que substituíram essa configuração em seu escopo de usuário atual.</span><span class="sxs-lookup"><span data-stu-id="7f650-261">The profile is used by default, for the particular type with the device, for all users except for those who have overridden this setting in their current-user scope.</span></span> <span data-ttu-id="7f650-262">(O perfil é instalado e associado ao sistema de dispositivos em todo, se esse ainda não for o caso.)</span><span class="sxs-lookup"><span data-stu-id="7f650-262">(The profile is installed and associated to the device system wide, if that is not already the case.)</span></span>

<span data-ttu-id="7f650-263">No</span><span class="sxs-lookup"><span data-stu-id="7f650-263">No</span></span>

<span data-ttu-id="7f650-264">Usuário atual</span><span class="sxs-lookup"><span data-stu-id="7f650-264">Current user</span></span>

<span data-ttu-id="7f650-265">O perfil é do tipo ICC ou CDMP</span><span class="sxs-lookup"><span data-stu-id="7f650-265">Profile is of type ICC or CDMP</span></span>

<span data-ttu-id="7f650-266">O perfil é usado por padrão para o tipo específico com o dispositivo no caso do usuário atual, independentemente do padrão de todo o sistema para isso.</span><span class="sxs-lookup"><span data-stu-id="7f650-266">The profile is used by default for the particular type with the device in case of current user, irrespective of the system-wide default for this.</span></span> <span data-ttu-id="7f650-267">(O perfil é instalado e associado ao dispositivo para o usuário atual, se esse ainda não for o caso.)</span><span class="sxs-lookup"><span data-stu-id="7f650-267">(The profile is installed and associated to the device for current user, if that is not already the case.)</span></span>

<span data-ttu-id="7f650-268">Sim, se o perfil já estiver instalado</span><span class="sxs-lookup"><span data-stu-id="7f650-268">Yes, if the profile is already installed</span></span>

<span data-ttu-id="7f650-269">$ {ROWSPAN2} $Set o perfil para um tipo (ICC, DMP, CAMP, GMMP) e a combinação de subtipo como padrão global $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7f650-269">${ROWSPAN2}$Set profile for a type (ICC, DMP, CAMP, GMMP) and subtype combination as global default${REMOVE}$</span></span>  

<span data-ttu-id="7f650-270">Todo o sistema</span><span class="sxs-lookup"><span data-stu-id="7f650-270">System wide</span></span>

<span data-ttu-id="7f650-271">Somente perfis ICC e CDMP podem ser associados a dispositivos.</span><span class="sxs-lookup"><span data-stu-id="7f650-271">Only ICC and CDMP profiles can be associated with devices.</span></span>

<span data-ttu-id="7f650-272">O perfil é usado por padrão para o tipo específico.</span><span class="sxs-lookup"><span data-stu-id="7f650-272">The profile is used by default for the particular type.</span></span> <span data-ttu-id="7f650-273">Os usuários podem substituir essa configuração no escopo do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="7f650-273">Users can override this setting in the current-user scope.</span></span> <span data-ttu-id="7f650-274">(O perfil é instalado, se esse ainda não for o caso.)</span><span class="sxs-lookup"><span data-stu-id="7f650-274">(The profile is installed, if that is not already the case.)</span></span>

<span data-ttu-id="7f650-275">No</span><span class="sxs-lookup"><span data-stu-id="7f650-275">No</span></span>

<span data-ttu-id="7f650-276">Usuário atual</span><span class="sxs-lookup"><span data-stu-id="7f650-276">Current user</span></span>

<span data-ttu-id="7f650-277">Somente perfis ICC e CDMP podem ser associados a dispositivos.</span><span class="sxs-lookup"><span data-stu-id="7f650-277">Only ICC and CDMP profiles can be associated with devices.</span></span>

<span data-ttu-id="7f650-278">O perfil é usado por padrão para o tipo específico para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="7f650-278">The profile is used by default for the particular type for current user.</span></span> <span data-ttu-id="7f650-279">(O perfil é instalado, se esse ainda não for o caso.)</span><span class="sxs-lookup"><span data-stu-id="7f650-279">(The profile is installed, if that is not already the case.)</span></span>

<span data-ttu-id="7f650-280">Sim, se o perfil já estiver instalado.</span><span class="sxs-lookup"><span data-stu-id="7f650-280">Yes, if the profile is already installed.</span></span>

<span data-ttu-id="7f650-281">$ {ROWSPAN2} $Erase a substituição do usuário atual para uma configuração de perfil padrão específica, para que o padrão do sistema sempre seja usado (como fallback) mesmo para o escopo do usuário atual. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7f650-281">${ROWSPAN2}$Erase the current-user override for a particular default profile setting, so that the system default always gets used (as fallback) even for current-user scope.${REMOVE}$</span></span>  

<span data-ttu-id="7f650-282">Todo o sistema</span><span class="sxs-lookup"><span data-stu-id="7f650-282">System wide</span></span>

<span data-ttu-id="7f650-283">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="7f650-283">Not applicable</span></span>

<span data-ttu-id="7f650-284">Usuário atual</span><span class="sxs-lookup"><span data-stu-id="7f650-284">Current user</span></span>

<span data-ttu-id="7f650-285">Mesmo para consultas de usuário atual em configurações de perfil padrão, as configurações de todo o sistema são retornadas para uso.</span><span class="sxs-lookup"><span data-stu-id="7f650-285">Even for current-user queries on default profile settings, system-wide settings are returned for use.</span></span>

<span data-ttu-id="7f650-286">Yes</span><span class="sxs-lookup"><span data-stu-id="7f650-286">Yes</span></span>

<span data-ttu-id="7f650-287">$ {ROWSPAN2} $Enumerate perfis instalados que atendem a critérios específicos (como classe de dispositivo, classe de perfil, etc.) $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="7f650-287">${ROWSPAN2}$Enumerate installed profiles satisfying particular criteria (like device class, profile class, etc.)${REMOVE}$</span></span>  

<span data-ttu-id="7f650-288">Todo o sistema</span><span class="sxs-lookup"><span data-stu-id="7f650-288">System wide</span></span>

<span data-ttu-id="7f650-289">Somente perfis ICC e CDMP podem ser associados e enumerados para dispositivos.</span><span class="sxs-lookup"><span data-stu-id="7f650-289">Only ICC and CDMP profiles can be associated with and enumerated for devices.</span></span>

<span data-ttu-id="7f650-290">Os perfis que estão instalados e atendem aos critérios especificados no escopo de todo o sistema são enumerados.</span><span class="sxs-lookup"><span data-stu-id="7f650-290">Profiles that are installed and satisfy the specified criteria in system-wide scope are enumerated.</span></span>

<span data-ttu-id="7f650-291">Yes</span><span class="sxs-lookup"><span data-stu-id="7f650-291">Yes</span></span>

<span data-ttu-id="7f650-292">Usuário atual</span><span class="sxs-lookup"><span data-stu-id="7f650-292">Current user</span></span>

<span data-ttu-id="7f650-293">Somente perfis ICC e CDMP podem ser associados a dispositivos e, portanto, enumerados para dispositivos.</span><span class="sxs-lookup"><span data-stu-id="7f650-293">Only ICC and CDMP profiles can be associated with devices and thus enumerated for devices.</span></span>

<span data-ttu-id="7f650-294">Os perfis que estão instalados e atendem aos critérios especificados no escopo de todo o sistema são enumerados.</span><span class="sxs-lookup"><span data-stu-id="7f650-294">Profiles which are installed and satisfy the specified criteria in system-wide scope are enumerated.</span></span>

<span data-ttu-id="7f650-295">Yes</span><span class="sxs-lookup"><span data-stu-id="7f650-295">Yes</span></span>

<span data-ttu-id="7f650-296">$ {ROWSPAN2} $Enumerate perfis associados a um dispositivo específico que atendem a critérios específicos, como classe de dispositivo e classe de perfil $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7f650-296">${ROWSPAN2}$Enumerate profiles associated with a particular device satisfying particular criteria, such as device class, and profile class${REMOVE}$</span></span>  

<span data-ttu-id="7f650-297">Todo o sistema</span><span class="sxs-lookup"><span data-stu-id="7f650-297">System wide</span></span>

<span data-ttu-id="7f650-298">Somente perfis ICC e CDMP podem ser associados e enumerados para dispositivos.</span><span class="sxs-lookup"><span data-stu-id="7f650-298">Only ICC and CDMP profiles can be associated with and enumerated for devices.</span></span>

<span data-ttu-id="7f650-299">Os perfis associados ao dispositivo no escopo de todo o sistema e atendem aos critérios especificados no escopo de todo o sistema são enumerados.</span><span class="sxs-lookup"><span data-stu-id="7f650-299">Profiles that are associated with the device in system-wide scope and satisfies the specified criteria in system-wide scope are enumerated.</span></span>

<span data-ttu-id="7f650-300">Yes</span><span class="sxs-lookup"><span data-stu-id="7f650-300">Yes</span></span>

<span data-ttu-id="7f650-301">Usuário atual</span><span class="sxs-lookup"><span data-stu-id="7f650-301">Current user</span></span>

<span data-ttu-id="7f650-302">Somente perfis ICC e CDMP podem ser associados e enumerados para dispositivos.</span><span class="sxs-lookup"><span data-stu-id="7f650-302">Only ICC and CDMP profiles can be associated with and enumerated for devices.</span></span>

<span data-ttu-id="7f650-303">Os perfis que estão disponíveis como associados ao dispositivo no escopo do usuário atual, que inclui as associações de todo o sistema e atendem aos critérios especificados no escopo do usuário atual são enumerados.</span><span class="sxs-lookup"><span data-stu-id="7f650-303">Profiles that are available as associated with the device in current-user scope, which includes the system-wide associations and satisfies the specified criteria in current-user scope are enumerated.</span></span>

<span data-ttu-id="7f650-304">Yes</span><span class="sxs-lookup"><span data-stu-id="7f650-304">Yes</span></span>



 

<span data-ttu-id="7f650-305">Os tipos de perfil de cor válidos são fornecidos pela enumeração COLORPROFILETYPE.</span><span class="sxs-lookup"><span data-stu-id="7f650-305">The valid color profile types are provided by the COLORPROFILETYPE enumeration.</span></span>

<span data-ttu-id="7f650-306">Os subtipos de perfil de cor válidos são fornecidos pela enumeração COLORPROFILESUBTYPE.</span><span class="sxs-lookup"><span data-stu-id="7f650-306">The valid color profile subtypes are provided by the COLORPROFILESUBTYPE enumeration.</span></span>

<span data-ttu-id="7f650-307">As combinações de tipo/subtipo de perfil válidas são mostradas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7f650-307">The valid profile type/subtype combinations are shown in the following table.</span></span>



<span data-ttu-id="7f650-308">COLORPROFILETYPE </span><span class="sxs-lookup"><span data-stu-id="7f650-308">COLORPROFILETYPE</span></span>

<span data-ttu-id="7f650-309">COLORPROFILESUBTYPE válido</span><span class="sxs-lookup"><span data-stu-id="7f650-309">Valid COLORPROFILESUBTYPE</span></span>

<span data-ttu-id="7f650-310">Observações</span><span class="sxs-lookup"><span data-stu-id="7f650-310">Notes</span></span>

<span data-ttu-id="7f650-311">Padrão do dispositivo</span><span class="sxs-lookup"><span data-stu-id="7f650-311">Device Default</span></span>

<span data-ttu-id="7f650-312">Padrão global</span><span class="sxs-lookup"><span data-stu-id="7f650-312">Global Default</span></span>

<span data-ttu-id="7f650-313">Uso pretendido</span><span class="sxs-lookup"><span data-stu-id="7f650-313">Intended Use</span></span>

<span data-ttu-id="7f650-314">Uso pretendido</span><span class="sxs-lookup"><span data-stu-id="7f650-314">Intended Use</span></span>

<span data-ttu-id="7f650-315">\_ICC CPT</span><span class="sxs-lookup"><span data-stu-id="7f650-315">CPT\_ICC</span></span>

<span data-ttu-id="7f650-316">CPST \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="7f650-316">CPST\_NONE</span></span>

<span data-ttu-id="7f650-317">Obter/definir perfil ICC padrão associado a um dispositivo</span><span class="sxs-lookup"><span data-stu-id="7f650-317">Get/Set default ICC profile associated with a device</span></span>

<span data-ttu-id="7f650-318">CPST \_ RGBWorkingSpace ou CPST \_ CustomWorkingSpace</span><span class="sxs-lookup"><span data-stu-id="7f650-318">CPST\_RGBWorkingSpace or CPST\_CustomWorkingSpace</span></span>

<span data-ttu-id="7f650-319">Obter/definir perfil ICC como global RGB ou perfil de espaço de trabalho personalizado.</span><span class="sxs-lookup"><span data-stu-id="7f650-319">Get/Set ICC profile as global RGB or custom working space profile.</span></span> <span data-ttu-id="7f650-320">Consulte a observação.</span><span class="sxs-lookup"><span data-stu-id="7f650-320">See Note.</span></span>

<span data-ttu-id="7f650-321">O COLORPROFILETYPE CPT \_ ICC e o CPT \_ DMP são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="7f650-321">The COLORPROFILETYPE CPT\_ICC and CPT\_DMP are mutually exclusive.</span></span> <span data-ttu-id="7f650-322">O perfil de cor padrão definido para um determinado espaço de trabalho (RGB ou personalizado) pode ser um perfil ICC ou um perfil DMP, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="7f650-322">The default color profile you set for a given working space (RGB or Custom) can be either an ICC profile or a DMP profile, but not both.</span></span>

<span data-ttu-id="7f650-323">CPT \_ DMP</span><span class="sxs-lookup"><span data-stu-id="7f650-323">CPT\_DMP</span></span>

<span data-ttu-id="7f650-324">CPST \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="7f650-324">CPST\_NONE</span></span>

<span data-ttu-id="7f650-325">Obter/definir perfil DMP padrão associado a um dispositivo</span><span class="sxs-lookup"><span data-stu-id="7f650-325">Get/Set default DMP profile associated with a device</span></span>

<span data-ttu-id="7f650-326">CPST \_ RGBWorkingSpace ou CPST \_ CustomWorkingSpace</span><span class="sxs-lookup"><span data-stu-id="7f650-326">CPST\_RGBWorkingSpace or CPST\_CustomWorkingSpace</span></span>

<span data-ttu-id="7f650-327">Obter/definir perfil DMP como global RGB ou perfil de espaço de trabalho personalizado.</span><span class="sxs-lookup"><span data-stu-id="7f650-327">Get/Set DMP profile as global RGB or custom working space profile.</span></span> <span data-ttu-id="7f650-328">Consulte a observação.</span><span class="sxs-lookup"><span data-stu-id="7f650-328">See Note.</span></span>

<span data-ttu-id="7f650-329">O COLORPROFILETYPE CPT \_ ICC e o CPT \_ DMP são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="7f650-329">The COLORPROFILETYPE CPT\_ICC and CPT\_DMP are mutually exclusive.</span></span> <span data-ttu-id="7f650-330">O perfil de cor padrão definido para um determinado espaço de trabalho (RGB ou personalizado) pode ser um perfil ICC ou um perfil DMP, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="7f650-330">The default color profile you set for a given working space (RGB or Custom) can be either an ICC profile or a DMP profile, but not both.</span></span>



 

> [!Note]  
> <span data-ttu-id="7f650-331">Quando WcsSetDefaultColorProfile é chamado para definir um perfil DMP como o perfil padrão para o espaço de trabalho RGB ou um espaço de trabalho personalizado, somente um perfil DMP que é do tipo RGBVirtualDevice, LCD ou CRT é válido.</span><span class="sxs-lookup"><span data-stu-id="7f650-331">When WcsSetDefaultColorProfile is called to set a DMP profile as the default profile for the RGB working space or a custom working space, only a DMP profile that is of type RGBVirtualDevice, LCD, or CRT is valid.</span></span>
>
>  
>
> <span data-ttu-id="7f650-332">Quando WcsSetDefaultColorProfile é chamado para definir um perfil ICC como o perfil padrão para o espaço de trabalho RGB ou um espaço de trabalho personalizado, somente um perfil ICC cuja classe é "spac" ou "Disp" e cujo espaço de cores é "RGB" é válido.</span><span class="sxs-lookup"><span data-stu-id="7f650-332">When WcsSetDefaultColorProfile is called to set an ICC profile as the default profile for the RGB working space or a custom working space, only an ICC profile whose class is "spac" or "disp," and whose color space is "RGB" is valid.</span></span>

 

<span data-ttu-id="7f650-333">A arquitetura é projetada de acordo com os requisitos das operações, conforme mencionado nas enumerações e tabelas acima.</span><span class="sxs-lookup"><span data-stu-id="7f650-333">The architecture is designed according to the requirements of the operations as mentioned in the enumerations and tables above.</span></span>

### <a name="profile-management-public-api-layer"></a><span data-ttu-id="7f650-334">Camada de API pública de gerenciamento de perfil</span><span class="sxs-lookup"><span data-stu-id="7f650-334">Profile management public API layer</span></span>

<span data-ttu-id="7f650-335">Como o escopo de gerenciamento de perfil não é suportado por APIs ICM2 herdadas, um novo conjunto de APIs de gerenciamento de perfil WCS é necessário que define o escopo de gerenciamento de perfil como usuário de todo o sistema ou atual.</span><span class="sxs-lookup"><span data-stu-id="7f650-335">Because profile management scope is not supported by legacy ICM2 APIs, a new set of WCS profile management APIs is required that defines profile management scope as system wide or current user.</span></span> <span data-ttu-id="7f650-336">?</span><span class="sxs-lookup"><span data-stu-id="7f650-336">?</span></span> <span data-ttu-id="7f650-337">As APIs de ICM2 herdadas continuam com suporte para compatibilidade com versões anteriores e funcionam no escopo de gerenciamento de perfil que é implícito para a chamada.</span><span class="sxs-lookup"><span data-stu-id="7f650-337">Legacy ICM2 APIs continue to be supported for backward compatibility, and work on profile management scope that is implicit for the call.</span></span> <span data-ttu-id="7f650-338">o ICM2 APIs que funcionam no escopo do usuário atual?</span><span class="sxs-lookup"><span data-stu-id="7f650-338">o ICM2 APIs that work on current-user scope ?</span></span> <span data-ttu-id="7f650-339">Isso é para operações que têm suporte para o escopo do usuário em todo e no momento no gerenciamento do perfil do WCS.</span><span class="sxs-lookup"><span data-stu-id="7f650-339">This is for operations that are supported for both system wide and current-user scope in WCS profile management.</span></span> <span data-ttu-id="7f650-340">As APIs herdadas do ICM2 chamam novas APIs do WCS com o escopo de gerenciamento de perfis como usuário atual.</span><span class="sxs-lookup"><span data-stu-id="7f650-340">Legacy ICM2 APIs call on new WCS APIs with profile management scope as current user.</span></span> <span data-ttu-id="7f650-341">Isso faz sentido da perspectiva do usuário porque isso permite configurações por usuário de aplicativos herdados e também a execução da maioria das operações no contexto de LUA.</span><span class="sxs-lookup"><span data-stu-id="7f650-341">This makes sense from user perspective because this enables per-user settings from legacy applications and also executing most of the operations in LUA context.</span></span> <span data-ttu-id="7f650-342">o ICM2 APIs que funcionam no escopo de todo o sistema?</span><span class="sxs-lookup"><span data-stu-id="7f650-342">o ICM2 APIs that work on system-wide scope ?</span></span> <span data-ttu-id="7f650-343">Isso é para operações (perfis de instalação e perfis de desinstalação) que dão suporte apenas ao escopo de todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="7f650-343">This is for operations (install profiles and uninstall profiles) that support only system-wide scope.</span></span> <span data-ttu-id="7f650-344">Nenhuma nova API de gerenciamento de perfil WCS é criada e APIs existentes podem ser modificadas.</span><span class="sxs-lookup"><span data-stu-id="7f650-344">No new WCS profile management APIs are created and existing APIs can be modified.</span></span>

<span data-ttu-id="7f650-345">As implementações subjacentes das operações de gerenciamento de perfil funcionam nas seguintes entidades de dados de configuração para criar o contexto para algoritmos de processamento de cores para fornecer funcionalidades de gerenciamento de cores.</span><span class="sxs-lookup"><span data-stu-id="7f650-345">The underlying implementations of the profile management operations work on the following configuration data entities to create the context for color processing algorithms to provide color management functionalities.</span></span> <span data-ttu-id="7f650-346">Eles são configurações específicas de dispositivo ou globais (independentes de dispositivo).</span><span class="sxs-lookup"><span data-stu-id="7f650-346">They are either device specific or global (device independent) settings.</span></span> <span data-ttu-id="7f650-347">dados de configuração específicos do dispositivo:?</span><span class="sxs-lookup"><span data-stu-id="7f650-347">o Device specific configuration data: ?</span></span> <span data-ttu-id="7f650-348">Lista de perfis associados a um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="7f650-348">List of profiles associated with a particular device.</span></span> <span data-ttu-id="7f650-349">?</span><span class="sxs-lookup"><span data-stu-id="7f650-349">?</span></span> <span data-ttu-id="7f650-350">Perfil padrão para tipos de perfil diferentes associados a um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7f650-350">Default profile for different profile types associated with a device.</span></span> <span data-ttu-id="7f650-351">?</span><span class="sxs-lookup"><span data-stu-id="7f650-351">?</span></span> <span data-ttu-id="7f650-352">Modo de correspondência de perfis usados para enumeração.</span><span class="sxs-lookup"><span data-stu-id="7f650-352">Matching mode of profiles used for enumeration.</span></span> <span data-ttu-id="7f650-353">o dados de configuração global:?</span><span class="sxs-lookup"><span data-stu-id="7f650-353">o Global configuration data: ?</span></span> <span data-ttu-id="7f650-354">Lista de perfis instalados no sistema.</span><span class="sxs-lookup"><span data-stu-id="7f650-354">List of profiles installed in the system.</span></span> <span data-ttu-id="7f650-355">?</span><span class="sxs-lookup"><span data-stu-id="7f650-355">?</span></span> <span data-ttu-id="7f650-356">Perfil padrão global para tipos de perfil diferentes.</span><span class="sxs-lookup"><span data-stu-id="7f650-356">Global default profile for different profile types.</span></span> <span data-ttu-id="7f650-357">?</span><span class="sxs-lookup"><span data-stu-id="7f650-357">?</span></span> <span data-ttu-id="7f650-358">As implementações subjacentes do armazenamento de dados de configuração assumem o escopo de armazenamento para dados de configuração (dispositivo independente ou específico de dispositivo), que pode ser o usuário de todo o sistema ou o atual.</span><span class="sxs-lookup"><span data-stu-id="7f650-358">The underlying implementations of configuration data storage take in storage scope for configuration data (either device independent or device specific), which can be either system wide or current user.</span></span> <span data-ttu-id="7f650-359">Isso é diferente do escopo de gerenciamento de perfil.</span><span class="sxs-lookup"><span data-stu-id="7f650-359">This is different from profile management scope.</span></span> <span data-ttu-id="7f650-360">Uma operação com o escopo de gerenciamento de perfil de usuário atual pode causar uma leitura de um escopo de armazenamento em todo o sistema se a configuração de usuário atual para essa operação não estiver presente.</span><span class="sxs-lookup"><span data-stu-id="7f650-360">An operation with current-user profile management scope can cause a read from a system-wide storage scope if the current-user setting for that operation is not present.</span></span> <span data-ttu-id="7f650-361">?</span><span class="sxs-lookup"><span data-stu-id="7f650-361">?</span></span> <span data-ttu-id="7f650-362">A camada de API ICM2/WCS chama essa camada de armazenamento para obter e definir dados com o escopo de armazenamento apropriado.</span><span class="sxs-lookup"><span data-stu-id="7f650-362">The ICM2/WCS API layer calls in this storage layer for getting and setting data with appropriate storage scope.</span></span> <span data-ttu-id="7f650-363">A camada de armazenamento é transparente para o escopo de gerenciamento de perfil.</span><span class="sxs-lookup"><span data-stu-id="7f650-363">The storage layer is transparent to profile management scope.</span></span> <span data-ttu-id="7f650-364">A lógica para combinar dados de escopos de armazenamento de usuário atual e de todo o sistema para criar ou atualizar uma configuração de acordo com o escopo de gerenciamento de perfil especificado pelo chamador da API.</span><span class="sxs-lookup"><span data-stu-id="7f650-364">The logic for combining data from current-user and system-wide storage scopes to create or update a configuration according to the profile management scope specified by the API caller.</span></span> <span data-ttu-id="7f650-365">Essa lógica está presente na camada de API ICM2/WCS.</span><span class="sxs-lookup"><span data-stu-id="7f650-365">This logic is present in the ICM2/WCS API layer.</span></span>

### <a name="device-specific-storage-layer"></a><span data-ttu-id="7f650-366">Camada de armazenamento específica do dispositivo</span><span class="sxs-lookup"><span data-stu-id="7f650-366">Device-specific storage layer</span></span>

<span data-ttu-id="7f650-367">O armazenamento para diferentes classes de dispositivos, como impressão, captura ou exibição, pode ser diferente entre si.</span><span class="sxs-lookup"><span data-stu-id="7f650-367">The storage for different classes of devices like print, capture or display could be different from each other.</span></span> <span data-ttu-id="7f650-368">Por exemplo, os dados de configuração para um dispositivo de impressão devem ser armazenados usando APIs de impressão padrão, como SetPrinterDataEx e GetPrinterDataEx, para permitir que os perfis sejam copiados e as configurações sejam transferidas para um computador cliente durante a conexão de apontar e imprimir.</span><span class="sxs-lookup"><span data-stu-id="7f650-368">For example, configuration data for a print device must be stored using standard print APIs, such as SetPrinterDataEx and GetPrinterDataEx, to enable the profiles to be copied and settings to be transferred to a client machine during Point-and-Print connection.</span></span> <span data-ttu-id="7f650-369">?</span><span class="sxs-lookup"><span data-stu-id="7f650-369">?</span></span> <span data-ttu-id="7f650-370">Essa camada exporta a funcionalidade para abrir armazenamento, obter dados, definir dados e fechar a loja usando interfaces predefinidas comuns para que a camada de armazenamento de configuração de gerenciamento de perfil possa chamá-las enquanto são transparentes para o modo como os dados são armazenados para esse dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7f650-370">This layer exports functionality to open store, get data, set data and close store using common pre-defined interfaces so that the profile management configuration storage layer can call into them while being transparent to the way the data gets stored for that device.</span></span>

<span data-ttu-id="7f650-371">O diagrama a seguir ilustra essa arquitetura.</span><span class="sxs-lookup"><span data-stu-id="7f650-371">The following diagram illustrates this architecture.</span></span>



<span data-ttu-id="7f650-372">Camada de API pública de gerenciamento de perfil</span><span class="sxs-lookup"><span data-stu-id="7f650-372">Profile Management Public API Layer</span></span>

<span data-ttu-id="7f650-373">$ {ROWSPAN2} $Legacy APIs ICM2 para operações que dão suporte apenas ao escopo de gerenciamento de perfil em todo o sistema no Vista (instalar, desinstalar e obter o diretório de cores).</span><span class="sxs-lookup"><span data-stu-id="7f650-373">${ROWSPAN2}$Legacy ICM2 APIs for operations that support only system-wide profile management scope in Vista (install, uninstall, and get color directory).</span></span> <span data-ttu-id="7f650-374">Eles chamam a camada de armazenamento de configuração com o escopo de armazenamento apropriado. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7f650-374">They call the configuration storage layer with appropriate storage scope.${REMOVE}$</span></span>  

<span data-ttu-id="7f650-375">API ICM2 herdada para operações que dão suporte a escopo de gerenciamento de perfil de usuário atual e de todo o sistema no Vista (todas as operações diferentes de instalar, desinstalar e obter o diretório de cores).</span><span class="sxs-lookup"><span data-stu-id="7f650-375">Legacy ICM2 API for operations that support both system-wide and current-user profile management scope in Vista (all operations other than install, uninstall, and get color directory).</span></span> <span data-ttu-id="7f650-376">Eles trabalham implicitamente no escopo do usuário atual e chamam a nova API do WCS com o escopo de gerenciamento de perfil como usuário atual.</span><span class="sxs-lookup"><span data-stu-id="7f650-376">They implicitly work on current-user scope, and call into new WCS API with profile management scope as current user.</span></span>

<span data-ttu-id="7f650-377">Nova API WCS com suporte a escopo de gerenciamento de perfil de usuário atual e de todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="7f650-377">New WCS API with system-wide and current-user profile management scope support.</span></span> <span data-ttu-id="7f650-378">Eles chamam a camada de armazenamento de configuração com o escopo de armazenamento apropriado.</span><span class="sxs-lookup"><span data-stu-id="7f650-378">They call the configuration storage layer with appropriate storage scope.</span></span>



 



<span data-ttu-id="7f650-379">Camada de armazenamento de configuração de gerenciamento de perfil</span><span class="sxs-lookup"><span data-stu-id="7f650-379">Profile Management Configuration Storage Layer</span></span>

<span data-ttu-id="7f650-380">Rotinas de configuração global independentes de dispositivo</span><span class="sxs-lookup"><span data-stu-id="7f650-380">Device-independent global configuration routines</span></span>

<span data-ttu-id="7f650-381">Rotinas de configuração específicas do dispositivo</span><span class="sxs-lookup"><span data-stu-id="7f650-381">Device-specific configuration routines</span></span>

<span data-ttu-id="7f650-382">$ {ROWSPAN3} $Profile a instalação e o gerenciamento de configurações de perfil padrão independente de dispositivo, com suporte no escopo de armazenamento de todo o sistema e do usuário atual. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7f650-382">${ROWSPAN3}$Profile installation and device-independent default profile settings management, supported in system-wide and current-user storage scope.${REMOVE}$</span></span>  

<span data-ttu-id="7f650-383">Associação de dispositivo e gerenciamento de configurações de perfil padrão específicas do dispositivo, com suporte no escopo de armazenamento de todo o sistema e do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="7f650-383">Device association and device-specific default profile settings management, supported in system-wide and current-user storage scope.</span></span>

<span data-ttu-id="7f650-384">Device-Specific camada de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7f650-384">Device-Specific Storage layer</span></span>

<span data-ttu-id="7f650-385">Imprimir armazenamento específico</span><span class="sxs-lookup"><span data-stu-id="7f650-385">Print specific storage</span></span>

<span data-ttu-id="7f650-386">Exibir armazenamento específico</span><span class="sxs-lookup"><span data-stu-id="7f650-386">Display specific storage</span></span>

<span data-ttu-id="7f650-387">Capturar armazenamento específico</span><span class="sxs-lookup"><span data-stu-id="7f650-387">Capture specific storage</span></span>



 

<span data-ttu-id="7f650-388">APIs ICM2 herdadas para operações que dão suporte apenas ao escopo de gerenciamento de perfil em todo o sistema no Vista não têm alterações no comportamento.</span><span class="sxs-lookup"><span data-stu-id="7f650-388">Legacy ICM2 APIs for operations that support only system-wide profile management scope in Vista have no changes in behavior.</span></span> <span data-ttu-id="7f650-389">As operações de instalação e desinstalação caem nesta categoria.</span><span class="sxs-lookup"><span data-stu-id="7f650-389">Install and uninstall operations fall in this category.</span></span>

<span data-ttu-id="7f650-390">APIs ICM2 herdadas para operações que dão suporte a escopo de gerenciamento de perfil de usuário atual e de todo o sistema têm seu comportamento alterado para consultar e definir as configurações do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="7f650-390">Legacy ICM2 APIs for operations that support both system-wide and current-user profile management scope have their behavior changed to query and configure current-user settings.</span></span> <span data-ttu-id="7f650-391">Todas as operações que não sejam instalar e desinstalar se enquadram nesta categoria.</span><span class="sxs-lookup"><span data-stu-id="7f650-391">All operations other than install and uninstall fall in this category.</span></span>

 

 




