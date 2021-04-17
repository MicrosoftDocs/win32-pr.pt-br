---
description: Para aprimorar a segurança do wmiprvse.exe processo de host do provedor compartilhado Instrumentação de Gerenciamento do Windows (WMI), foram feitas alterações nas plataformas do Windows que protegem o processo de host do provedor com um SID (identificador de segurança do serviço).
ms.assetid: f93ac155-512c-4efa-8168-ca2d56fe6f01
ms.tgt_platform: multiple
title: Chaves e valores do registro para controlar a segurança do provedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2c7dd990c1a9ebbc1242af5ce4601ce6eb22a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782646"
---
# <a name="registry-keys-and-values-for-controlling-provider-security"></a><span data-ttu-id="efb15-103">Chaves e valores do registro para controlar a segurança do provedor</span><span class="sxs-lookup"><span data-stu-id="efb15-103">Registry Keys and Values for Controlling Provider Security</span></span>

<span data-ttu-id="efb15-104">Para aprimorar a segurança do wmiprvse.exe processo de host do provedor compartilhado Instrumentação de Gerenciamento do Windows (WMI), foram feitas alterações nas plataformas do Windows que protegem o processo de host do provedor com um [*Sid (identificador de segurança do serviço)*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="efb15-104">To enhance the security of the Windows Management Instrumentation (WMI) shared provider host process (wmiprvse.exe), changes were made to Windows platforms that secure the provider host process with a [*service security identifier (SID)*](gloss-s.md).</span></span> <span data-ttu-id="efb15-105">Essas alterações apresentam os seguintes modos de execução para o host compartilhado do WMI: seguro e compatível.</span><span class="sxs-lookup"><span data-stu-id="efb15-105">These changes introduce the following running modes for the WMI shared host: secure and compatible.</span></span>

<span data-ttu-id="efb15-106">As seções a seguir são abordadas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="efb15-106">The following sections are covered in this topic:</span></span>

-   [<span data-ttu-id="efb15-107">Modos seguros e compatíveis</span><span class="sxs-lookup"><span data-stu-id="efb15-107">Secure and Compatible Modes</span></span>](#secure-and-compatible-modes)
-   [<span data-ttu-id="efb15-108">Chaves e valores do registro</span><span class="sxs-lookup"><span data-stu-id="efb15-108">Registry Keys and Values</span></span>](#registry-keys-and-values)
-   [<span data-ttu-id="efb15-109">Configurando um provedor para ser executado no modo seguro ou compatível</span><span class="sxs-lookup"><span data-stu-id="efb15-109">Configuring a Provider to Run in Secure or Compatible Mode</span></span>](#configuring-a-provider-to-run-in-secure-or-compatible-mode)

## <a name="secure-and-compatible-modes"></a><span data-ttu-id="efb15-110">Modos seguros e compatíveis</span><span class="sxs-lookup"><span data-stu-id="efb15-110">Secure and Compatible Modes</span></span>

<span data-ttu-id="efb15-111">A partir do Windows 7, os dois modos de execução a seguir para o processo de host compartilhado WMI foram adicionados:</span><span class="sxs-lookup"><span data-stu-id="efb15-111">Starting in Windows 7, the following two running modes for the WMI shared host process were added:</span></span>

<dl> <dt>

<span data-ttu-id="efb15-112"><span id="Secure_mode"></span><span id="secure_mode"></span><span id="SECURE_MODE"></span>Modo de segurança</span><span class="sxs-lookup"><span data-stu-id="efb15-112"><span id="Secure_mode"></span><span id="secure_mode"></span><span id="SECURE_MODE"></span>Secure mode</span></span>
</dt> <dd>

<span data-ttu-id="efb15-113">Os recursos de processo do host do provedor WMI são protegidos com um [*Sid de serviço*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="efb15-113">WMI provider host process resources are secured with a [*service SID*](gloss-s.md).</span></span> <span data-ttu-id="efb15-114">Somente o *SID do serviço* tem permissões para esses recursos.</span><span class="sxs-lookup"><span data-stu-id="efb15-114">Only the *service SID* has permissions for these resources.</span></span>

</dd> <dt>

<span data-ttu-id="efb15-115"><span id="Compatible_mode"></span><span id="compatible_mode"></span><span id="COMPATIBLE_MODE"></span>Modo compatível</span><span class="sxs-lookup"><span data-stu-id="efb15-115"><span id="Compatible_mode"></span><span id="compatible_mode"></span><span id="COMPATIBLE_MODE"></span>Compatible mode</span></span>
</dt> <dd>

<span data-ttu-id="efb15-116">O processo de host do provedor compartilhado WMI não está protegido com um [*Sid de serviço*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="efb15-116">The WMI shared provider host process is not secured with a [*service SID*](gloss-s.md).</span></span> <span data-ttu-id="efb15-117">O processo host do provedor permite acesso às contas NetworkService ou LocalService, dependendo do modelo de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="efb15-117">The provider host process allows access to the NetworkService or LocalService accounts depending on the hosting model.</span></span> <span data-ttu-id="efb15-118">Para obter mais informações sobre modelos de hospedagem, consulte [provedor de hospedagem e segurança](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="efb15-118">For more information about hosting models, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

</dd> </dl>

<span data-ttu-id="efb15-119">**Windows Vista e Windows Server 2008:** Para acessar as chaves e os valores do registro para controlar modos seguros e compatíveis para o processo de host do provedor, você deve instalar a atualização de segurança em [KB 959454](https://support.microsoft.com/kb/959454).</span><span class="sxs-lookup"><span data-stu-id="efb15-119">**Windows Vista and Windows Server 2008:** To access the registry keys and values for controlling secure and compatible modes for the provider host process, you must install the security update in [KB 959454](https://support.microsoft.com/kb/959454).</span></span> <span data-ttu-id="efb15-120">Para obter mais informações, consulte o [Boletim de segurança da Microsoft MS09-012](https://www.microsoft.com/technet/security/bulletin/ms09-012.mspx).</span><span class="sxs-lookup"><span data-stu-id="efb15-120">For more information, see the [Microsoft Security Bulletin MS09-012](https://www.microsoft.com/technet/security/bulletin/ms09-012.mspx).</span></span>

## <a name="registry-keys-and-values"></a><span data-ttu-id="efb15-121">Chaves e valores do registro</span><span class="sxs-lookup"><span data-stu-id="efb15-121">Registry Keys and Values</span></span>

<span data-ttu-id="efb15-122">As configurações do modo seguro e compatível são especificadas por meio de chaves do registro.</span><span class="sxs-lookup"><span data-stu-id="efb15-122">The secure and compatible mode settings are specified through registry keys.</span></span> <span data-ttu-id="efb15-123">As chaves do registro para WMI estão localizadas no registro em **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .</span><span class="sxs-lookup"><span data-stu-id="efb15-123">The registry keys for WMI are located in the registry at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\.</span></span>

<span data-ttu-id="efb15-124">As seguintes chaves do registro e o valor **DWORD** descritos na lista a seguir foram adicionados para controlar o comportamento dos provedores WMI.</span><span class="sxs-lookup"><span data-stu-id="efb15-124">The following registry keys and **DWORD** value described in the following list were added to control the behavior of WMI providers.</span></span>

<dl> <dt>

<span data-ttu-id="efb15-125"><span id="SecuredHostProviders"></span><span id="securedhostproviders"></span><span id="SECUREDHOSTPROVIDERS"></span>**SecuredHostProviders**</span><span class="sxs-lookup"><span data-stu-id="efb15-125"><span id="SecuredHostProviders"></span><span id="securedhostproviders"></span><span id="SECUREDHOSTPROVIDERS"></span>**SecuredHostProviders**</span></span>
</dt> <dd>

<span data-ttu-id="efb15-126">Essa chave controla o comportamento de provedores individuais.</span><span class="sxs-lookup"><span data-stu-id="efb15-126">This key controls the behavior of individual providers.</span></span> <span data-ttu-id="efb15-127">Todos os provedores listados nessa chave sempre são executados no modo de segurança.</span><span class="sxs-lookup"><span data-stu-id="efb15-127">All of the providers that are listed in this key always run in secure mode.</span></span> <span data-ttu-id="efb15-128">Todos os provedores de caixa de entrada fornecidos com o Windows são listados sob essa chave e são executados no modo de segurança por padrão.</span><span class="sxs-lookup"><span data-stu-id="efb15-128">All inbox providers that are shipped with Windows are listed under this key, and are run in secure mode by default.</span></span>

<span data-ttu-id="efb15-129">Essa chave tem precedência sobre os provedores listados na chave **CompatibleHostProviders** .</span><span class="sxs-lookup"><span data-stu-id="efb15-129">This key takes precedence over providers listed in the **CompatibleHostProviders** key.</span></span>

</dd> <dt>

<span data-ttu-id="efb15-130"><span id="CompatibleHostProviders"></span><span id="compatiblehostproviders"></span><span id="COMPATIBLEHOSTPROVIDERS"></span>**CompatibleHostProviders**</span><span class="sxs-lookup"><span data-stu-id="efb15-130"><span id="CompatibleHostProviders"></span><span id="compatiblehostproviders"></span><span id="COMPATIBLEHOSTPROVIDERS"></span>**CompatibleHostProviders**</span></span>
</dt> <dd>

<span data-ttu-id="efb15-131">Essa chave controla o comportamento de provedores individuais.</span><span class="sxs-lookup"><span data-stu-id="efb15-131">This key controls the behavior of individual providers.</span></span> <span data-ttu-id="efb15-132">Todos os provedores listados nessa chave sempre são executados no modo compatível.</span><span class="sxs-lookup"><span data-stu-id="efb15-132">All providers that are listed in this key always run in compatible mode.</span></span> <span data-ttu-id="efb15-133">Essa chave está vazia por padrão.</span><span class="sxs-lookup"><span data-stu-id="efb15-133">This key is empty by default.</span></span>

<span data-ttu-id="efb15-134">Se um provedor estiver listado na chave **SecuredHostProviders** e na chave **CompatibleHostProviders** , o provedor será executado no modo de segurança.</span><span class="sxs-lookup"><span data-stu-id="efb15-134">If a provider is listed both in the **SecuredHostProviders** key and in the **CompatibleHostProviders** key, the provider is run in secure mode.</span></span>

> [!Note]  
> <span data-ttu-id="efb15-135">A chave **CompatibleHostProviders** fornece compatibilidade de aplicativos para aplicativos de terceiros se a chave **DefaultSecuredHost** estiver definida como 1 e o provedor não funcionar no modo de segurança.</span><span class="sxs-lookup"><span data-stu-id="efb15-135">The **CompatibleHostProviders** key provides application compatibility for third-party applications if the **DefaultSecuredHost** key is set to 1 and the provider is known to not function in secure mode.</span></span>

 

</dd> <dt>

<span data-ttu-id="efb15-136"><span id="DefaultSecuredHost"></span><span id="defaultsecuredhost"></span><span id="DEFAULTSECUREDHOST"></span>**DefaultSecuredHost**</span><span class="sxs-lookup"><span data-stu-id="efb15-136"><span id="DefaultSecuredHost"></span><span id="defaultsecuredhost"></span><span id="DEFAULTSECUREDHOST"></span>**DefaultSecuredHost**</span></span>
</dt> <dd>

<span data-ttu-id="efb15-137">Um valor **DWORD** do registro global que determina se todos os provedores, que não estão listados nas chaves **SecuredHostProviders** ou **CompatibleHostProviders** , são executados no modo seguro ou compatível.</span><span class="sxs-lookup"><span data-stu-id="efb15-137">A global registry **DWORD** value that determines whether all of the providers, which are not listed in the **SecuredHostProviders** or **CompatibleHostProviders** keys, are run in the secure or compatible mode.</span></span> <span data-ttu-id="efb15-138">Esse valor **DWORD** permite que o administrador decida em qual modo um provedor de terceiros deve ser executado.</span><span class="sxs-lookup"><span data-stu-id="efb15-138">This **DWORD** value lets the administrator decide under which mode a third-party provider must run.</span></span> <span data-ttu-id="efb15-139">Por padrão, esse valor é definido como zero e todos os provedores de terceiros são executados no modo compatível.</span><span class="sxs-lookup"><span data-stu-id="efb15-139">By default, this value is set to zero and all third-party providers are run in compatible mode.</span></span> <span data-ttu-id="efb15-140">Os administradores podem tornar seu computador mais seguro por padrão, definindo o valor **DefaultSecuredHost** como 1.</span><span class="sxs-lookup"><span data-stu-id="efb15-140">Administrators can make their computer more secure by default by setting the **DefaultSecuredHost** value to 1.</span></span>

> [!Note]  
> <span data-ttu-id="efb15-141">O valor de **DefaultSecuredHost** não afeta as outras chaves do registro.</span><span class="sxs-lookup"><span data-stu-id="efb15-141">The **DefaultSecuredHost** value does not affect the other registry keys.</span></span> <span data-ttu-id="efb15-142">Os provedores listados na chave **SecuredHostProviders** permanecem no modo de segurança, e aqueles listados na chave **CompatibleHostProviders** permanecem no modo compatível.</span><span class="sxs-lookup"><span data-stu-id="efb15-142">The providers that are listed in the **SecuredHostProviders** key remain in secure mode, and the ones that are listed in the **CompatibleHostProviders** key remain in compatible mode.</span></span>

 

<span data-ttu-id="efb15-143">As seguintes configurações são possíveis:</span><span class="sxs-lookup"><span data-stu-id="efb15-143">The following settings are possible:</span></span>

<dl> <dt>

<span data-ttu-id="efb15-144"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="efb15-144"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="efb15-145">Especifica que os provedores são executados no modo compatível.</span><span class="sxs-lookup"><span data-stu-id="efb15-145">Specifies that providers run in compatible mode.</span></span>

</dd> <dt>

<span data-ttu-id="efb15-146"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="efb15-146"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="efb15-147">Especifica que os provedores são executados no modo de segurança.</span><span class="sxs-lookup"><span data-stu-id="efb15-147">Specifies that providers run in secure mode.</span></span>

</dd> </dl> </dd> </dl>

<span data-ttu-id="efb15-148">A lista a seguir lista as configurações de registro possíveis e os modos de execução associados para um provedor.</span><span class="sxs-lookup"><span data-stu-id="efb15-148">The following list lists the possible registry settings and the associated running modes for a provider.</span></span>



| <span data-ttu-id="efb15-149">Listado em SecuredHostProviders</span><span class="sxs-lookup"><span data-stu-id="efb15-149">Listed under SecuredHostProviders</span></span> | <span data-ttu-id="efb15-150">Listado em CompatibleHostProviders</span><span class="sxs-lookup"><span data-stu-id="efb15-150">Listed under CompatibleHostProviders</span></span> | <span data-ttu-id="efb15-151">Configuração de DefaultSecuredHost</span><span class="sxs-lookup"><span data-stu-id="efb15-151">DefaultSecuredHost Setting</span></span> | <span data-ttu-id="efb15-152">Mode</span><span class="sxs-lookup"><span data-stu-id="efb15-152">Mode</span></span>       |
|-----------------------------------|--------------------------------------|----------------------------|------------|
| <span data-ttu-id="efb15-153">Não</span><span class="sxs-lookup"><span data-stu-id="efb15-153">No</span></span>                                | <span data-ttu-id="efb15-154">Não</span><span class="sxs-lookup"><span data-stu-id="efb15-154">No</span></span>                                   | <span data-ttu-id="efb15-155">0</span><span class="sxs-lookup"><span data-stu-id="efb15-155">0</span></span>                          | <span data-ttu-id="efb15-156">Compatível</span><span class="sxs-lookup"><span data-stu-id="efb15-156">Compatible</span></span> |
| <span data-ttu-id="efb15-157">Não</span><span class="sxs-lookup"><span data-stu-id="efb15-157">No</span></span>                                | <span data-ttu-id="efb15-158">Sim</span><span class="sxs-lookup"><span data-stu-id="efb15-158">Yes</span></span>                                  | <span data-ttu-id="efb15-159">0</span><span class="sxs-lookup"><span data-stu-id="efb15-159">0</span></span>                          | <span data-ttu-id="efb15-160">Compatível</span><span class="sxs-lookup"><span data-stu-id="efb15-160">Compatible</span></span> |
| <span data-ttu-id="efb15-161">Sim</span><span class="sxs-lookup"><span data-stu-id="efb15-161">Yes</span></span>                               | <span data-ttu-id="efb15-162">Não</span><span class="sxs-lookup"><span data-stu-id="efb15-162">No</span></span>                                   | <span data-ttu-id="efb15-163">0</span><span class="sxs-lookup"><span data-stu-id="efb15-163">0</span></span>                          | <span data-ttu-id="efb15-164">Seguro</span><span class="sxs-lookup"><span data-stu-id="efb15-164">Secure</span></span>     |
| <span data-ttu-id="efb15-165">Sim</span><span class="sxs-lookup"><span data-stu-id="efb15-165">Yes</span></span>                               | <span data-ttu-id="efb15-166">Sim</span><span class="sxs-lookup"><span data-stu-id="efb15-166">Yes</span></span>                                  | <span data-ttu-id="efb15-167">0</span><span class="sxs-lookup"><span data-stu-id="efb15-167">0</span></span>                          | <span data-ttu-id="efb15-168">Seguro</span><span class="sxs-lookup"><span data-stu-id="efb15-168">Secure</span></span>     |
| <span data-ttu-id="efb15-169">Não</span><span class="sxs-lookup"><span data-stu-id="efb15-169">No</span></span>                                | <span data-ttu-id="efb15-170">Não</span><span class="sxs-lookup"><span data-stu-id="efb15-170">No</span></span>                                   | <span data-ttu-id="efb15-171">1</span><span class="sxs-lookup"><span data-stu-id="efb15-171">1</span></span>                          | <span data-ttu-id="efb15-172">Seguro</span><span class="sxs-lookup"><span data-stu-id="efb15-172">Secure</span></span>     |
| <span data-ttu-id="efb15-173">Não</span><span class="sxs-lookup"><span data-stu-id="efb15-173">No</span></span>                                | <span data-ttu-id="efb15-174">Sim</span><span class="sxs-lookup"><span data-stu-id="efb15-174">Yes</span></span>                                  | <span data-ttu-id="efb15-175">1</span><span class="sxs-lookup"><span data-stu-id="efb15-175">1</span></span>                          | <span data-ttu-id="efb15-176">Compatível</span><span class="sxs-lookup"><span data-stu-id="efb15-176">Compatible</span></span> |
| <span data-ttu-id="efb15-177">Sim</span><span class="sxs-lookup"><span data-stu-id="efb15-177">Yes</span></span>                               | <span data-ttu-id="efb15-178">Não</span><span class="sxs-lookup"><span data-stu-id="efb15-178">No</span></span>                                   | <span data-ttu-id="efb15-179">1</span><span class="sxs-lookup"><span data-stu-id="efb15-179">1</span></span>                          | <span data-ttu-id="efb15-180">Seguro</span><span class="sxs-lookup"><span data-stu-id="efb15-180">Secure</span></span>     |
| <span data-ttu-id="efb15-181">Sim</span><span class="sxs-lookup"><span data-stu-id="efb15-181">Yes</span></span>                               | <span data-ttu-id="efb15-182">Sim</span><span class="sxs-lookup"><span data-stu-id="efb15-182">Yes</span></span>                                  | <span data-ttu-id="efb15-183">1</span><span class="sxs-lookup"><span data-stu-id="efb15-183">1</span></span>                          | <span data-ttu-id="efb15-184">Seguro</span><span class="sxs-lookup"><span data-stu-id="efb15-184">Secure</span></span>     |



 

## <a name="configuring-a-provider-to-run-in-secure-or-compatible-mode"></a><span data-ttu-id="efb15-185">Configurando um provedor para ser executado no modo seguro ou compatível</span><span class="sxs-lookup"><span data-stu-id="efb15-185">Configuring a Provider to Run in Secure or Compatible Mode</span></span>

<span data-ttu-id="efb15-186">As chaves do registro podem ser modificadas usando o Console de Gerenciamento de Política de Grupo (GPMC).</span><span class="sxs-lookup"><span data-stu-id="efb15-186">The registry keys can be modified using the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="efb15-187">Para obter mais informações, consulte [console de gerenciamento de política de grupo](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span><span class="sxs-lookup"><span data-stu-id="efb15-187">For more information, see [Group Policy Management Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span></span>

<span data-ttu-id="efb15-188">Os procedimentos a seguir ilustram como gerenciar configurações de modo seguro e compatível usando as preferências de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="efb15-188">The following procedures illustrate how to manage secure and compatible mode settings by using group policy preferences.</span></span> <span data-ttu-id="efb15-189">Para obter mais informações sobre as preferências de política de grupo, consulte a [visão geral de preferências de política de grupo](/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn581922(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="efb15-189">For more information about group policy preferences, see the [Group Policy Preferences Overview](/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn581922(v=ws.11)).</span></span>

<span data-ttu-id="efb15-190">**Para adicionar um provedor ao modo seguro ou compatível usando Política de Grupo**</span><span class="sxs-lookup"><span data-stu-id="efb15-190">**To add a provider to either the secure or compatible mode by using Group Policy**</span></span>

1.  <span data-ttu-id="efb15-191">Abra o GPMC.</span><span class="sxs-lookup"><span data-stu-id="efb15-191">Open the GPMC.</span></span>
2.  <span data-ttu-id="efb15-192">Crie um objeto de Política de Grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="efb15-192">Create a Group Policy Object (GPO).</span></span>
3.  <span data-ttu-id="efb15-193">Edite o GPO.</span><span class="sxs-lookup"><span data-stu-id="efb15-193">Edit the GPO.</span></span>
4.  <span data-ttu-id="efb15-194">Navegue até preferências/configurações do Windows/registro.</span><span class="sxs-lookup"><span data-stu-id="efb15-194">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="efb15-195">Clique com o botão direito do mouse e selecione **novo... Registro**.</span><span class="sxs-lookup"><span data-stu-id="efb15-195">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="efb15-196">Essa ação apresenta uma interface do usuário na qual você pode inserir informações do registro.</span><span class="sxs-lookup"><span data-stu-id="efb15-196">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="efb15-197">Selecione o comando **criar** .</span><span class="sxs-lookup"><span data-stu-id="efb15-197">Select the **Create** command.</span></span>
7.  <span data-ttu-id="efb15-198">Selecione o seguinte caminho de chave do registro:</span><span class="sxs-lookup"><span data-stu-id="efb15-198">Select the following registry key path:</span></span>

    <span data-ttu-id="efb15-199">**Modo de segurança: hKey \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **SecuredHostProviders**</span><span class="sxs-lookup"><span data-stu-id="efb15-199">**Secure Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**SecuredHostProviders**</span></span>

    <span data-ttu-id="efb15-200">**Modo compatível: hKey \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **CompatibleHostProviders**</span><span class="sxs-lookup"><span data-stu-id="efb15-200">**Compatible Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**CompatibleHostProviders**</span></span>

8.  <span data-ttu-id="efb15-201">No campo **nome** , insira o nome do provedor que você deseja adicionar a essa chave.</span><span class="sxs-lookup"><span data-stu-id="efb15-201">In the **name** field, enter the name of the provider you want to add to this key.</span></span> <span data-ttu-id="efb15-202">O nome do provedor deve estar no seguinte formato: <namespace> : <\_ \_ RelPath>.</span><span class="sxs-lookup"><span data-stu-id="efb15-202">The provider name must be in the following format: <namespace>:<\_\_RELPATH>.</span></span> <span data-ttu-id="efb15-203">Por exemplo, raiz \\ cimv2: \_ \_ Win32Provider. nome = "myfornecedor".</span><span class="sxs-lookup"><span data-stu-id="efb15-203">For example, root\\cimv2:\_\_win32provider.name="MyProvider".</span></span>
9.  <span data-ttu-id="efb15-204">No campo de **dados** , digite 0.</span><span class="sxs-lookup"><span data-stu-id="efb15-204">In the **data** field, enter 0.</span></span>
10. <span data-ttu-id="efb15-205">Clique em OK.</span><span class="sxs-lookup"><span data-stu-id="efb15-205">Click OK.</span></span>

<span data-ttu-id="efb15-206">**Para remover um provedor do modo seguro ou compatível usando Política de Grupo**</span><span class="sxs-lookup"><span data-stu-id="efb15-206">**To remove a provider from either the secure or compatible mode by using Group Policy**</span></span>

1.  <span data-ttu-id="efb15-207">Abra o GPMC.</span><span class="sxs-lookup"><span data-stu-id="efb15-207">Open the GPMC.</span></span>
2.  <span data-ttu-id="efb15-208">Crie um GPO.</span><span class="sxs-lookup"><span data-stu-id="efb15-208">Create a GPO.</span></span>
3.  <span data-ttu-id="efb15-209">Edite o GPO.</span><span class="sxs-lookup"><span data-stu-id="efb15-209">Edit the GPO.</span></span>
4.  <span data-ttu-id="efb15-210">Navegue até preferências/configurações do Windows/registro.</span><span class="sxs-lookup"><span data-stu-id="efb15-210">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="efb15-211">Clique com o botão direito do mouse e selecione **novo... Registro**.</span><span class="sxs-lookup"><span data-stu-id="efb15-211">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="efb15-212">Essa ação apresenta uma interface do usuário na qual você pode inserir informações do registro.</span><span class="sxs-lookup"><span data-stu-id="efb15-212">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="efb15-213">Selecione o comando **remover** .</span><span class="sxs-lookup"><span data-stu-id="efb15-213">Select the **Remove** command.</span></span>
7.  <span data-ttu-id="efb15-214">Selecione o seguinte caminho de chave do registro:</span><span class="sxs-lookup"><span data-stu-id="efb15-214">Select the following registry key path:</span></span>

    <span data-ttu-id="efb15-215">**Modo de segurança: hKey \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **SecuredHostProviders**</span><span class="sxs-lookup"><span data-stu-id="efb15-215">**Secure Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**SecuredHostProviders**</span></span>

    <span data-ttu-id="efb15-216">**Modo compatível: hKey \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **CompatibleHostProviders**</span><span class="sxs-lookup"><span data-stu-id="efb15-216">**Compatible Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**CompatibleHostProviders**</span></span>

8.  <span data-ttu-id="efb15-217">No campo **nome** , insira o nome do provedor que você deseja remover dessa chave.</span><span class="sxs-lookup"><span data-stu-id="efb15-217">In the **name** field, enter the name of the provider you want to remove from this key.</span></span>
9.  <span data-ttu-id="efb15-218">No campo de **dados** , digite 0.</span><span class="sxs-lookup"><span data-stu-id="efb15-218">In the **data** field, enter 0.</span></span>
10. <span data-ttu-id="efb15-219">Clique em OK.</span><span class="sxs-lookup"><span data-stu-id="efb15-219">Click OK.</span></span>

<span data-ttu-id="efb15-220">O procedimento a seguir fornece detalhes sobre como modificar o comportamento de provedores que não estão listados nas chaves **SecuredHostProviders** ou **CompatibleHostProviders** .</span><span class="sxs-lookup"><span data-stu-id="efb15-220">The following procedure provides details about how to modify the behavior of providers that are not listed in either the **SecuredHostProviders** or **CompatibleHostProviders** keys.</span></span>

<span data-ttu-id="efb15-221">**Para alterar o valor padrão da chave DefaultSecuredHost usando Política de Grupo**</span><span class="sxs-lookup"><span data-stu-id="efb15-221">**To change the default value of the DefaultSecuredHost key by using Group Policy**</span></span>

1.  <span data-ttu-id="efb15-222">Abra o GPMC.</span><span class="sxs-lookup"><span data-stu-id="efb15-222">Open the GPMC.</span></span>
2.  <span data-ttu-id="efb15-223">Crie um GPO.</span><span class="sxs-lookup"><span data-stu-id="efb15-223">Create a GPO.</span></span>
3.  <span data-ttu-id="efb15-224">Edite o GPO.</span><span class="sxs-lookup"><span data-stu-id="efb15-224">Edit the GPO.</span></span>
4.  <span data-ttu-id="efb15-225">Navegue até preferências/configurações do Windows/registro.</span><span class="sxs-lookup"><span data-stu-id="efb15-225">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="efb15-226">Clique com o botão direito do mouse e selecione **novo... Registro**.</span><span class="sxs-lookup"><span data-stu-id="efb15-226">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="efb15-227">Essa ação apresenta uma interface do usuário na qual você pode inserir informações do registro.</span><span class="sxs-lookup"><span data-stu-id="efb15-227">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="efb15-228">Selecione o comando **Atualizar** .</span><span class="sxs-lookup"><span data-stu-id="efb15-228">Select the **Update** command.</span></span>
7.  <span data-ttu-id="efb15-229">Selecione o seguinte caminho de chave do registro: **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM**.</span><span class="sxs-lookup"><span data-stu-id="efb15-229">Select the following registry key path: **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**.</span></span>
8.  <span data-ttu-id="efb15-230">No campo **nome** , insira **DefaultSecuredHost**.</span><span class="sxs-lookup"><span data-stu-id="efb15-230">In the **name** field, enter **DefaultSecuredHost**.</span></span>
9.  <span data-ttu-id="efb15-231">No campo de **dados** , digite 0 para modo compatível ou 1 para modo de segurança.</span><span class="sxs-lookup"><span data-stu-id="efb15-231">In the **data** field, enter 0 for compatible mode or 1 for secure mode.</span></span>
10. <span data-ttu-id="efb15-232">Clique em OK.</span><span class="sxs-lookup"><span data-stu-id="efb15-232">Click OK.</span></span>

 

 
