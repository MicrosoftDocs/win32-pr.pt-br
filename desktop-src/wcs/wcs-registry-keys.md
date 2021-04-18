---
title: Chaves do Registro do WCS
description: O WCS usa chaves do registro para sinalizar que determinados eventos de perfil de cor ocorreram. Os aplicativos devem consultar essas chaves do registro para o estado atualizado do perfil de cor do sistema.
ms.assetid: e728efa0-e547-45b9-af85-1312766d2fe7
keywords:
- WCS (sistema de cores do Windows), chaves do registro
- WCS (sistema de cores do Windows), chaves do registro
- gerenciamento de cores de imagem, chaves do registro
- gerenciamento de cores, chaves do registro
- cores, chaves do registro
- Referência do WCS, chaves do registro
- referência para WCS, chaves do registro
- WCS (sistema de cores do Windows), registro
- WCS (sistema de cores do Windows), registro
- gerenciamento de cores de imagem, registro
- gerenciamento de cores, registro
- cores, registro
- Referência do WCS, registro
- referência para WCS, registro
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a1c0072d9a00fe0cff4a4dbe57af839f65731b
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "105766588"
---
# <a name="wcs-registry-keys"></a><span data-ttu-id="deb52-118">Chaves do Registro do WCS</span><span class="sxs-lookup"><span data-stu-id="deb52-118">WCS Registry Keys</span></span>

<span data-ttu-id="deb52-119">O WCS usa chaves do registro para sinalizar que determinados eventos de perfil de cor ocorreram.</span><span class="sxs-lookup"><span data-stu-id="deb52-119">WCS uses registry keys to signal that certain color profile events have occurred.</span></span> <span data-ttu-id="deb52-120">Os aplicativos devem consultar essas chaves do registro para o estado atualizado do perfil de cor do sistema.</span><span class="sxs-lookup"><span data-stu-id="deb52-120">Apps should query these registry keys for updated system color profile state.</span></span>

## <a name="active-color-profile-changed"></a><span data-ttu-id="deb52-121">Perfil de cor ativo alterado</span><span class="sxs-lookup"><span data-stu-id="deb52-121">Active color profile changed</span></span>

<span data-ttu-id="deb52-122">Os aplicativos podem querer responder a eventos de alteração de perfil de cor para um dispositivo monitor; Isso garante que eles sempre tenham informações de cores precisas para seu destino, mesmo que o usuário ou outro aplicativo tenha alterado o perfil ativo para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="deb52-122">Apps may want to respond to color profile change events for a monitor device; this ensures that they always have accurate color information for their target, even if the user or another app has changed the active profile for the device.</span></span>

### <a name="desktop-applications"></a><span data-ttu-id="deb52-123">Aplicativos da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="deb52-123">Desktop applications</span></span>

<span data-ttu-id="deb52-124">Os aplicativos da área de trabalho devem escutar alterações no registro para determinar quando uma associação de perfil de cor foi alterada usando [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue).</span><span class="sxs-lookup"><span data-stu-id="deb52-124">Desktop apps should listen for changes to the registry to determine when a color profile associations has changed using [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue).</span></span> <span data-ttu-id="deb52-125">Um aplicativo deve ser registrado para alterações de associação de perfil por usuário e para alterações em todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="deb52-125">An app should register both for per-user profile association changes, and for system-wide changes.</span></span>

<span data-ttu-id="deb52-126">[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) deve ser inicializado com um HKEY fornecido por [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa).</span><span class="sxs-lookup"><span data-stu-id="deb52-126">[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) should be initialized with an HKEY provided by [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa).</span></span> <span data-ttu-id="deb52-127">**RegOpenKeyEx** deve ser inicializado usando os seguintes locais de árvore do registro:</span><span class="sxs-lookup"><span data-stu-id="deb52-127">**RegOpenKeyEx** should be initialized using the following registry tree locations:</span></span>



|                                  |                                                                                                                                                    |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="deb52-128">Associações de perfil por usuário</span><span class="sxs-lookup"><span data-stu-id="deb52-128">Per-user profile associations</span></span>    | <span data-ttu-id="deb52-129">**HKEY \_ Current \_ User Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ ICM \\ ProfileAssociations \\ Display \\ {4d36e96e-E325-11CE-BFC1-08002BE10318}**</span><span class="sxs-lookup"><span data-stu-id="deb52-129">**HKEY\_CURRENT\_USER SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\ICM\\ProfileAssociations\\Display\\{4d36e96e-e325-11ce-bfc1-08002be10318}**</span></span> |
| <span data-ttu-id="deb52-130">Associações de perfil em todo o sistema</span><span class="sxs-lookup"><span data-stu-id="deb52-130">System-wide profile associations</span></span> | <span data-ttu-id="deb52-131">**HKEY \_ \_ computador local \\ System sistema de \\ \\ controle CurrentControlSet \\ classe \\ {4d36e96e-E325-11CE-BFC1-08002BE10318}**</span><span class="sxs-lookup"><span data-stu-id="deb52-131">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Class\\{4d36e96e-e325-11ce-bfc1-08002be10318}**</span></span>                                        |



 

<span data-ttu-id="deb52-132">Quando o aplicativo é notificado sobre uma alteração na chave do registro, ele deve primeiro consultar se as associações por usuário ou para todo o sistema estão sendo usadas chamando [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent).</span><span class="sxs-lookup"><span data-stu-id="deb52-132">When the app is notified of a registry key change, it should first query whether per-user or system-wide associations are being used by calling [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent).</span></span> <span data-ttu-id="deb52-133">Em seguida, ele deve chamar [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) com o valor de escopo direito de gerenciamento de perfil de WCS para obter o novo perfil de cor ativo para o monitor. [**\_ \_ \_**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope)</span><span class="sxs-lookup"><span data-stu-id="deb52-133">It should then call [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) with the right [**WCS\_PROFILE\_MANAGEMENT\_SCOPE**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) value to obtain the new active color profile for the monitor.</span></span> <span data-ttu-id="deb52-134">Observe que nem todas as alterações da chave do registro corresponderão a uma alteração real no perfil de cor atualmente ativo; o aplicativo visualiza verifica se o perfil retornado por **WcsGetDefaultColorProfile** foi realmente alterado.</span><span class="sxs-lookup"><span data-stu-id="deb52-134">Note that not all registry key changes will correspond to an actual change in the currently active color profile; the app mush check whether the profile returned by **WcsGetDefaultColorProfile** has actually changed.</span></span>

### <a name="universal-windows-uwp-apps"></a><span data-ttu-id="deb52-135">Aplicativos do Windows universal (UWP)</span><span class="sxs-lookup"><span data-stu-id="deb52-135">Universal Windows (UWP) apps</span></span>

<span data-ttu-id="deb52-136">Os aplicativos universais do Windows não têm acesso às chaves do registro acima.</span><span class="sxs-lookup"><span data-stu-id="deb52-136">Universal Windows Apps do not have access to the above registry keys.</span></span> <span data-ttu-id="deb52-137">Em vez disso, eles devem registrar um manipulador para o evento [**DisplayInformation. ColorProfileChanged**](/uwp/api/Windows.Graphics.Display.DisplayInformation) .</span><span class="sxs-lookup"><span data-stu-id="deb52-137">Instead, they should register a handler for the [**DisplayInformation.ColorProfileChanged**](/uwp/api/Windows.Graphics.Display.DisplayInformation) event.</span></span> <span data-ttu-id="deb52-138">Esse evento é acionado sempre que o perfil de cor ativo do monitor no qual o aplicativo está sendo executado foi alterado.</span><span class="sxs-lookup"><span data-stu-id="deb52-138">This event fires whenever the active color profile for the monitor on which the application is running has changed.</span></span> <span data-ttu-id="deb52-139">ColorProfileChanged leva em conta se as associações de perfil por usuário ou todo o sistema estão sendo usadas; essas informações são extraídas de aplicativos UWP.</span><span class="sxs-lookup"><span data-stu-id="deb52-139">ColorProfileChanged takes into account whether per-user or system-wide profile associations are being used; this information is abstracted from UWP apps.</span></span>

<span data-ttu-id="deb52-140">Ao responder ao evento ColorProfileChanged, o aplicativo deve consultar o perfil ativo no momento usando [**DisplayInformation. GetColorProfileAsync**](/uwp/api/Windows.Graphics.Display.DisplayInformation).</span><span class="sxs-lookup"><span data-stu-id="deb52-140">When responding to the ColorProfileChanged event, the app should query the currently active profile using [**DisplayInformation.GetColorProfileAsync**](/uwp/api/Windows.Graphics.Display.DisplayInformation).</span></span>

 

 