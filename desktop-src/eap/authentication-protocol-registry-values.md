---
title: Valores do registro do protocolo de autenticação
description: O software de instalação para a DLL EAP pode criar os seguintes valores de registro abaixo de eaptypeid.
ms.assetid: a5f6674d-77c8-4b88-af0e-bb62f84d8a2b
keywords:
- RAS_EAP_VALUENAME_PATH
- RAS_EAP_VALUENAME_FRIENDLY_NAME
- RAS_EAP_VALUENAME_CONFIGUI
- RAS_EAP_VALUENAME_DEFAULT_DATA
- RAS_EAP_VALUENAME_REQUIRE_CONFIGUI
- RAS_EAP_VALUENAME_CONFIG_CLSID
- RAS_EAP_VALUENAME_IDENTITY
- RAS_EAP_VALUENAME_INTERACTIVEUI
- RAS_EAP_VALUENAME_INVOKE_NAMEDLG
- RAS_EAP_VALUENAME_INVOKE_PWDDLG
- RAS_EAP_VALUENAME_ENCRYPTION
- RAS_EAP_VALUENAME_STANDALONE_SUPPORTED
- RAS_EAP_VALUENAME_ROLES_SUPPORTED
- RAS_EAP_VALUENAME_PER_POLICY_CONFIG
- RAS_EAP_VALUENAME_ISTUNNEL_METHOD
- RAS_EAP_VALUENAME_FILTER_INNERMETHODS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8091197c7b0d5c5a208bf3658bbc15284a29ac9e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104006958"
---
# <a name="authentication-protocol-registry-values"></a><span data-ttu-id="d6f1e-119">Valores do registro do protocolo de autenticação</span><span class="sxs-lookup"><span data-stu-id="d6f1e-119">Authentication Protocol Registry Values</span></span>

<span data-ttu-id="d6f1e-120">O software de instalação para a DLL EAP pode criar os seguintes valores de registro abaixo de **&lt; eaptypeid &gt;**.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-120">The setup software for the EAP DLL may create the following registry values below **&lt;eaptypeid&gt;**.</span></span> <span data-ttu-id="d6f1e-121">Esses valores de registro são definidos no arquivo de cabeçalho Raseapif. h.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-121">These registry values are defined in the Raseapif.h header file.</span></span> <span data-ttu-id="d6f1e-122">Os valores de **RAS_EAP_VALUENAME_PATH** e **RAS_EAP_VALUENAME_FRIENDLY_NAME** são obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-122">The **RAS_EAP_VALUENAME_PATH** and **RAS_EAP_VALUENAME_FRIENDLY_NAME** values are required.</span></span> <span data-ttu-id="d6f1e-123">O software de instalação também pode criar outras chaves e valores.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-123">The setup software may create other keys and values as well.</span></span> <span data-ttu-id="d6f1e-124">Eles podem ser usados pelo próprio protocolo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-124">These could be used by the authentication protocol itself.</span></span> <span data-ttu-id="d6f1e-125">Para obter mais informações e um exemplo de configuração de registro, consulte [exemplo de valores de registro](registry-values-example.md).</span><span class="sxs-lookup"><span data-stu-id="d6f1e-125">For more information and an example of registry configuration, see [Registry Values Example](registry-values-example.md).</span></span>

[<span data-ttu-id="d6f1e-126">RAS_EAP_VALUENAME_PATH</span><span class="sxs-lookup"><span data-stu-id="d6f1e-126">RAS_EAP_VALUENAME_PATH</span></span>](#ras_eap_valuename_path)

[<span data-ttu-id="d6f1e-127">RAS_EAP_VALUENAME_FRIENDLY_NAME</span><span class="sxs-lookup"><span data-stu-id="d6f1e-127">RAS_EAP_VALUENAME_FRIENDLY_NAME</span></span>](#ras_eap_valuename_friendly_name)

[<span data-ttu-id="d6f1e-128">RAS_EAP_VALUENAME_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="d6f1e-128">RAS_EAP_VALUENAME_CONFIGUI</span></span>](#ras_eap_valuename_configui)

[<span data-ttu-id="d6f1e-129">RAS_EAP_VALUENAME_DEFAULT_DATA</span><span class="sxs-lookup"><span data-stu-id="d6f1e-129">RAS_EAP_VALUENAME_DEFAULT_DATA</span></span>](#ras_eap_valuename_default_data)

[<span data-ttu-id="d6f1e-130">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="d6f1e-130">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span></span>](#ras_eap_valuename_require_configui)

[<span data-ttu-id="d6f1e-131">RAS_EAP_VALUENAME_CONFIG_CLSID</span><span class="sxs-lookup"><span data-stu-id="d6f1e-131">RAS_EAP_VALUENAME_CONFIG_CLSID</span></span>](#ras_eap_valuename_config_clsid)

[<span data-ttu-id="d6f1e-132">RAS_EAP_VALUENAME_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="d6f1e-132">RAS_EAP_VALUENAME_IDENTITY</span></span>](#ras_eap_valuename_identity)

<span data-ttu-id="d6f1e-133">[RAS_EAP_VALUENAME_INTERACTIVEUI](#ras_eap_valuename_interactiveui) Encontrei</span><span class="sxs-lookup"><span data-stu-id="d6f1e-133">[RAS_EAP_VALUENAME_INTERACTIVEUI](#ras_eap_valuename_interactiveui)I</span></span>

[<span data-ttu-id="d6f1e-134">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span><span class="sxs-lookup"><span data-stu-id="d6f1e-134">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span></span>](#ras_eap_valuename_invoke_namedlg)

[<span data-ttu-id="d6f1e-135">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span><span class="sxs-lookup"><span data-stu-id="d6f1e-135">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span></span>](#ras_eap_valuename_invoke_pwddlg)

[<span data-ttu-id="d6f1e-136">RAS_EAP_VALUENAME_ENCRYPTION</span><span class="sxs-lookup"><span data-stu-id="d6f1e-136">RAS_EAP_VALUENAME_ENCRYPTION</span></span>](#ras_eap_valuename_encryption)

[<span data-ttu-id="d6f1e-137">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="d6f1e-137">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span></span>](#ras_eap_valuename_standalone_supported)

[<span data-ttu-id="d6f1e-138">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="d6f1e-138">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span></span>](#ras_eap_valuename_roles_supported)

[<span data-ttu-id="d6f1e-139">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="d6f1e-139">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span></span>](#ras_eap_valuename_per_policy_config)

[<span data-ttu-id="d6f1e-140">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span><span class="sxs-lookup"><span data-stu-id="d6f1e-140">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span></span>](#ras_eap_valuename_istunnel_method)

[<span data-ttu-id="d6f1e-141">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span><span class="sxs-lookup"><span data-stu-id="d6f1e-141">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span></span>](#ras_eap_valuename_filter_innermethods)

## <a name="ras_eap_valuename_path"></a><span data-ttu-id="d6f1e-142">RAS_EAP_VALUENAME_PATH</span><span class="sxs-lookup"><span data-stu-id="d6f1e-142">RAS_EAP_VALUENAME_PATH</span></span>

| <span data-ttu-id="d6f1e-143">Valor constante</span><span class="sxs-lookup"><span data-stu-id="d6f1e-143">Constant value</span></span> | <span data-ttu-id="d6f1e-144">Caminho</span><span class="sxs-lookup"><span data-stu-id="d6f1e-144">Path</span></span>                               |
|----------------|------------------------------------|
| <span data-ttu-id="d6f1e-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6f1e-145">Type</span></span>           | <span data-ttu-id="d6f1e-146">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="d6f1e-146">REG_EXPAND_SZ</span></span>                    |
| <span data-ttu-id="d6f1e-147">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6f1e-147">Description</span></span>    | <span data-ttu-id="d6f1e-148">Especifica o caminho para a DLL de EAP.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-148">Specifies the path to the EAP DLL.</span></span> |

## <a name="ras_eap_valuename_friendly_name"></a><span data-ttu-id="d6f1e-149">RAS_EAP_VALUENAME_FRIENDLY_NAME</span><span class="sxs-lookup"><span data-stu-id="d6f1e-149">RAS_EAP_VALUENAME_FRIENDLY_NAME</span></span>

| <span data-ttu-id="d6f1e-150">Valor constante</span><span class="sxs-lookup"><span data-stu-id="d6f1e-150">Constant value</span></span> | <span data-ttu-id="d6f1e-151">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d6f1e-151">FriendlyName</span></span>                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f1e-152">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6f1e-152">Type</span></span>           | <span data-ttu-id="d6f1e-153">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="d6f1e-153">REG_SZ</span></span>                                                                                                                                                           |
| <span data-ttu-id="d6f1e-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6f1e-154">Description</span></span>    | <span data-ttu-id="d6f1e-155">Especifica um nome amigável para o protocolo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-155">Specifies a friendly name for the authentication protocol.</span></span> <span data-ttu-id="d6f1e-156">Esse nome aparece na interface do usuário do aplicativo EAP para implementações discadas e sem fio.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-156">This name appears in the EAP application user interface for both dial-up and wireless implementations.</span></span> |

## <a name="ras_eap_valuename_configui"></a><span data-ttu-id="d6f1e-157">RAS_EAP_VALUENAME_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="d6f1e-157">RAS_EAP_VALUENAME_CONFIGUI</span></span>

| <span data-ttu-id="d6f1e-158">Valor constante</span><span class="sxs-lookup"><span data-stu-id="d6f1e-158">Constant value</span></span> | <span data-ttu-id="d6f1e-159">ConfigUIPath</span><span class="sxs-lookup"><span data-stu-id="d6f1e-159">ConfigUIPath</span></span>                                                                                                                      |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f1e-160">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6f1e-160">Type</span></span>           | <span data-ttu-id="d6f1e-161">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="d6f1e-161">REG_EXPAND_SZ</span></span>                                                                                                                   |
| <span data-ttu-id="d6f1e-162">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6f1e-162">Description</span></span>    | <span data-ttu-id="d6f1e-163">Especifica o caminho para a DLL que implementa a interface do usuário de configuração no cliente, porque essa interface do usuário é apenas para o cliente.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-163">Specifies the path to the DLL that implements the configuration user interface on the client, because this UI is for client only.</span></span> |

## <a name="ras_eap_valuename_default_data"></a><span data-ttu-id="d6f1e-164">RAS_EAP_VALUENAME_DEFAULT_DATA</span><span class="sxs-lookup"><span data-stu-id="d6f1e-164">RAS_EAP_VALUENAME_DEFAULT_DATA</span></span>

| <span data-ttu-id="d6f1e-165">Valor constante</span><span class="sxs-lookup"><span data-stu-id="d6f1e-165">Constant value</span></span> | <span data-ttu-id="d6f1e-166">ConfigData</span><span class="sxs-lookup"><span data-stu-id="d6f1e-166">ConfigData</span></span>                                                            |
|----------------|-----------------------------------------------------------------------|
| <span data-ttu-id="d6f1e-167">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6f1e-167">Type</span></span>           | <span data-ttu-id="d6f1e-168">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="d6f1e-168">REG_BINARY</span></span>                                                           |
| <span data-ttu-id="d6f1e-169">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6f1e-169">Description</span></span>    | <span data-ttu-id="d6f1e-170">Especifica os dados de configuração padrão para o protocolo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-170">Specifies default configuration data for the authentication protocol.</span></span> |

## <a name="ras_eap_valuename_require_configui"></a><span data-ttu-id="d6f1e-171">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="d6f1e-171">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span></span>

| <span data-ttu-id="d6f1e-172">Valor constante</span><span class="sxs-lookup"><span data-stu-id="d6f1e-172">Constant value</span></span> | <span data-ttu-id="d6f1e-173">RequireConfigUI</span><span class="sxs-lookup"><span data-stu-id="d6f1e-173">RequireConfigUI</span></span>                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f1e-174">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6f1e-174">Type</span></span>           | <span data-ttu-id="d6f1e-175">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="d6f1e-175">REG_DWORD</span></span>                                                                                                                                                                                                                                               |
| <span data-ttu-id="d6f1e-176">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6f1e-176">Description</span></span>    | <span data-ttu-id="d6f1e-177">Especifica se o usuário deve fornecer dados de configuração na interface do usuário do aplicativo de cliente EAP.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-177">Specifies whether the user must provide configuration data in the EAP client application user interface.</span></span> <span data-ttu-id="d6f1e-178">Se esse valor for 1, o usuário não poderá sair da interface do usuário do aplicativo do cliente EAP sem fornecer dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-178">If this value is 1, the user is not allowed to exit the EAP client application UI without providing configuration data.</span></span> <span data-ttu-id="d6f1e-179">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-179">The default value is 0.</span></span> |

## <a name="ras_eap_valuename_config_clsid"></a><span data-ttu-id="d6f1e-180">RAS_EAP_VALUENAME_CONFIG_CLSID</span><span class="sxs-lookup"><span data-stu-id="d6f1e-180">RAS_EAP_VALUENAME_CONFIG_CLSID</span></span>

| <span data-ttu-id="d6f1e-181">Valor constante</span><span class="sxs-lookup"><span data-stu-id="d6f1e-181">Constant value</span></span> | <span data-ttu-id="d6f1e-182">ConfigCLSID</span><span class="sxs-lookup"><span data-stu-id="d6f1e-182">ConfigCLSID</span></span>                                                   |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="d6f1e-183">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6f1e-183">Type</span></span>           | <span data-ttu-id="d6f1e-184">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="d6f1e-184">REG_SZ</span></span>                                                       |
| <span data-ttu-id="d6f1e-185">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6f1e-185">Description</span></span>    | <span data-ttu-id="d6f1e-186">Especifica a ID de classe da interface do usuário de configuração no servidor.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-186">Specifies the class ID of the configuration UI on the server.</span></span> |

## <a name="ras_eap_valuename_identity"></a><span data-ttu-id="d6f1e-187">RAS_EAP_VALUENAME_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="d6f1e-187">RAS_EAP_VALUENAME_IDENTITY</span></span>

| <span data-ttu-id="d6f1e-188">Valor constante</span><span class="sxs-lookup"><span data-stu-id="d6f1e-188">Constant value</span></span> | <span data-ttu-id="d6f1e-189">IdentityPath</span><span class="sxs-lookup"><span data-stu-id="d6f1e-189">IdentityPath</span></span>                                                                                                                           |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f1e-190">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6f1e-190">Type</span></span>           | <span data-ttu-id="d6f1e-191">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="d6f1e-191">REG_EXPAND_SZ</span></span>                                                                                                                        |
| <span data-ttu-id="d6f1e-192">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6f1e-192">Description</span></span>    | <span data-ttu-id="d6f1e-193">Especifica o caminho para a DLL que implementa as funções para obter a identidade do usuário no cliente, porque essa interface do usuário é apenas para o cliente.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-193">Specifies the path to the DLL that implements functions to obtain the user identity on the client, because this UI is for client only.</span></span> |

## <a name="ras_eap_valuename_interactiveui"></a><span data-ttu-id="d6f1e-194">RAS_EAP_VALUENAME_INTERACTIVEUI</span><span class="sxs-lookup"><span data-stu-id="d6f1e-194">RAS_EAP_VALUENAME_INTERACTIVEUI</span></span>

| <span data-ttu-id="d6f1e-195">Valor constante</span><span class="sxs-lookup"><span data-stu-id="d6f1e-195">Constant value</span></span> | <span data-ttu-id="d6f1e-196">InteractiveUIPath</span><span class="sxs-lookup"><span data-stu-id="d6f1e-196">InteractiveUIPath</span></span>                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f1e-197">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6f1e-197">Type</span></span>           | <span data-ttu-id="d6f1e-198">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="d6f1e-198">REG_EXPAND_SZ</span></span>                                                                                                                 |
| <span data-ttu-id="d6f1e-199">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6f1e-199">Description</span></span>    | <span data-ttu-id="d6f1e-200">Especifica o caminho para a DLL que implementa a interface do usuário interativa no cliente, pois essa interface do usuário é apenas para o cliente.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-200">Specifies the path to the DLL that implements the interactive user interface on the client, because this UI is for client only.</span></span> |

## <a name="ras_eap_valuename_invoke_namedlg"></a><span data-ttu-id="d6f1e-201">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span><span class="sxs-lookup"><span data-stu-id="d6f1e-201">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span></span>

| <span data-ttu-id="d6f1e-202">Valor constante</span><span class="sxs-lookup"><span data-stu-id="d6f1e-202">Constant value</span></span> | <span data-ttu-id="d6f1e-203">InvokeUsernameDialog</span><span class="sxs-lookup"><span data-stu-id="d6f1e-203">InvokeUsernameDialog</span></span>                                                                                                                                                                                   |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f1e-204">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6f1e-204">Type</span></span>           | <span data-ttu-id="d6f1e-205">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="d6f1e-205">REG_DWORD</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="d6f1e-206">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6f1e-206">Description</span></span>    | <span data-ttu-id="d6f1e-207">Especifica se o RAS deve exibir a caixa de diálogo padrão de nome de usuário do Windows NT/Windows 2000 (valor de 1) ou invocar [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) (valor de 0).</span><span class="sxs-lookup"><span data-stu-id="d6f1e-207">Specifies whether RAS should display the standard Windows NT/Windows 2000 user name dialog (value of 1) or invoke [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) (value of 0).</span></span> <span data-ttu-id="d6f1e-208">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-208">The default value is 1.</span></span> |

## <a name="ras_eap_valuename_invoke_pwddlg"></a><span data-ttu-id="d6f1e-209">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span><span class="sxs-lookup"><span data-stu-id="d6f1e-209">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span></span>

| <span data-ttu-id="d6f1e-210">Valor constante</span><span class="sxs-lookup"><span data-stu-id="d6f1e-210">Constant value</span></span> | <span data-ttu-id="d6f1e-211">InvokePasswordDialog</span><span class="sxs-lookup"><span data-stu-id="d6f1e-211">InvokePasswordDialog</span></span>                                                                                                                                                                        |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f1e-212">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6f1e-212">Type</span></span>           | <span data-ttu-id="d6f1e-213">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="d6f1e-213">REG_DWORD</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="d6f1e-214">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6f1e-214">Description</span></span>    | <span data-ttu-id="d6f1e-215">Especifica se o RAS deve exibir a caixa de diálogo de senha padrão do Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-215">Specifies whether RAS should display the standard Windows NT/Windows 2000 password dialog.</span></span> <span data-ttu-id="d6f1e-216">Se esse valor existir e for 0, o RAS não exibirá a caixa de diálogo de senha.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-216">If this value exists and is 0, RAS will not display the password dialog.</span></span> <span data-ttu-id="d6f1e-217">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-217">The default value is 1.</span></span> |


## <a name="ras_eap_valuename_encryption"></a><span data-ttu-id="d6f1e-218">RAS_EAP_VALUENAME_ENCRYPTION</span><span class="sxs-lookup"><span data-stu-id="d6f1e-218">RAS_EAP_VALUENAME_ENCRYPTION</span></span>

| <span data-ttu-id="d6f1e-219">Valor constante</span><span class="sxs-lookup"><span data-stu-id="d6f1e-219">Constant value</span></span> | <span data-ttu-id="d6f1e-220">MPPEEncryptionSupported</span><span class="sxs-lookup"><span data-stu-id="d6f1e-220">MPPEEncryptionSupported</span></span>                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f1e-221">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6f1e-221">Type</span></span>           | <span data-ttu-id="d6f1e-222">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="d6f1e-222">REG_DWORD</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="d6f1e-223">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6f1e-223">Description</span></span>    | <span data-ttu-id="d6f1e-224">Se esse valor for 1, o protocolo de autenticação poderá gerar chaves para o estilo de criptografia MPPE (criptografia ponto a ponto) da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-224">If this value is 1, the authentication protocol can generate keys for the Microsoft Point-to-Point Encryption (MPPE) style of encryption.</span></span> <span data-ttu-id="d6f1e-225">Os valores possíveis são 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-225">Possible values are 0 or 1.</span></span> <span data-ttu-id="d6f1e-226">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-226">The default value is 0.</span></span> |

## <a name="ras_eap_valuename_standalone_supported"></a><span data-ttu-id="d6f1e-227">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="d6f1e-227">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span></span>

| <span data-ttu-id="d6f1e-228">Valor constante</span><span class="sxs-lookup"><span data-stu-id="d6f1e-228">Constant value</span></span> | <span data-ttu-id="d6f1e-229">StandaloneSupported</span><span class="sxs-lookup"><span data-stu-id="d6f1e-229">StandaloneSupported</span></span>                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f1e-230">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6f1e-230">Type</span></span>           | <span data-ttu-id="d6f1e-231">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="d6f1e-231">REG_DWORD</span></span>                                                                                                                                                                     |
| <span data-ttu-id="d6f1e-232">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6f1e-232">Description</span></span>    | <span data-ttu-id="d6f1e-233">Especifica se esse protocolo de autenticação tem suporte em um servidor Windows 2000 autônomo.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-233">Specifies whether this authentication protocol is supported on a standalone Windows 2000 Server.</span></span> <span data-ttu-id="d6f1e-234">Um valor de 0 indica que não há suporte para o EAP.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-234">A value of 0 indicates that the EAP is not supported.</span></span> <span data-ttu-id="d6f1e-235">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-235">The default value is 1.</span></span> |

## <a name="ras_eap_valuename_roles_supported"></a><span data-ttu-id="d6f1e-236">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="d6f1e-236">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span></span>

| <span data-ttu-id="d6f1e-237">Valor Constante</span><span class="sxs-lookup"><span data-stu-id="d6f1e-237">Constant Value</span></span> | <span data-ttu-id="d6f1e-238">RolesSupported</span><span class="sxs-lookup"><span data-stu-id="d6f1e-238">RolesSupported</span></span>                                                                                                                                                                                                                             |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f1e-239">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6f1e-239">Type</span></span>           | <span data-ttu-id="d6f1e-240">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="d6f1e-240">REG_DWORD</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="d6f1e-241">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6f1e-241">Description</span></span>    | <span data-ttu-id="d6f1e-242">Especifica as várias funções às quais o EAP dá suporte.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-242">Specifies the various roles the EAP supports.</span></span> <span data-ttu-id="d6f1e-243">Isso indica se ele pode ser usado em um servidor ou em um cliente, se há suporte para conexões RAS (VPN) ou PEAP.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-243">This indicates whether it can be used on a server or a client, whether it is supported for RAS connections (VPN) or PEAP.</span></span> <span data-ttu-id="d6f1e-244">O comportamento padrão é mostrar o método EAP no PEAP e no EAP.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-244">The default behavior is to show the EAP method in PEAP and in EAP.</span></span> |

## <a name="ras_eap_valuename_per_policy_config"></a><span data-ttu-id="d6f1e-245">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="d6f1e-245">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span></span>

| <span data-ttu-id="d6f1e-246">Valor Constante</span><span class="sxs-lookup"><span data-stu-id="d6f1e-246">Constant Value</span></span> | <span data-ttu-id="d6f1e-247">PerPolicyConfig</span><span class="sxs-lookup"><span data-stu-id="d6f1e-247">PerPolicyConfig</span></span> |
|----------------|-----------------|
| <span data-ttu-id="d6f1e-248">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6f1e-248">Type</span></span>           | <span data-ttu-id="d6f1e-249">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="d6f1e-249">REG_DWORD</span></span>      |
| <span data-ttu-id="d6f1e-250">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6f1e-250">Description</span></span>    |                 |

## <a name="ras_eap_valuename_istunnel_method"></a><span data-ttu-id="d6f1e-251">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span><span class="sxs-lookup"><span data-stu-id="d6f1e-251">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span></span>

<span data-ttu-id="d6f1e-252">Esse valor de registro não está em uso.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-252">This registry value is not in use.</span></span>

## <a name="ras_eap_valuename_filter_innermethods"></a><span data-ttu-id="d6f1e-253">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span><span class="sxs-lookup"><span data-stu-id="d6f1e-253">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span></span>

<span data-ttu-id="d6f1e-254">Esse valor de registro não está em uso.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-254">This registry value is not in use.</span></span>

