---
title: Classe MDM_Policy_Config01_Browser02
description: A \_ classe Config01 Browser02 de política de MDM \_ \_ representa as políticas de navegador disponíveis.
ms.assetid: 296e3be4-3bc1-4e06-9e31-532639a0b912
keywords:
- Classe MDM_Policy_Config01_Browser02
- Classe MDM_Policy_Config01_Browser02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Browser02
- MDM_Policy_Config01_Browser02.InstanceID
- MDM_Policy_Config01_Browser02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba68b4d3f6798a448447e7773dc299977c54434c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009176"
---
# <a name="mdm_policy_config01_browser02-class"></a><span data-ttu-id="45450-105">\_Classe MDM \_ Config01 \_ Browser02</span><span class="sxs-lookup"><span data-stu-id="45450-105">MDM\_Policy\_Config01\_Browser02 class</span></span>

<span data-ttu-id="45450-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="45450-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="45450-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="45450-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="45450-108">A **classe \_ \_ Config01 \_ Browser02 de política de MDM** representa as políticas de navegador disponíveis.</span><span class="sxs-lookup"><span data-stu-id="45450-108">The **MDM\_Policy\_Config01\_Browser02** class represents the browser policies available.</span></span>

<span data-ttu-id="45450-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="45450-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="45450-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45450-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Browser02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAddressBarDropdown;
  sint32 AllowAutofill;
  sint32 AllowCookies;
  sint32 AllowDeveloperTools;
  sint32 AllowInPrivate;
  sint32 AllowMicrosoftCompatibilityList;
  sint32 AllowDoNotTrack;
  sint32 AllowFlashClickToRun;
  sint32 AllowFlash;
  sint32 AllowExtensions;
  sint32 AllowPasswordManager;
  sint32 AllowPopups;
  sint32 AllowSearchEngineCustomization;
  sint32 AllowSearchSuggestionsinAddressBar;
  sint32 AllowSmartScreen;
  sint32 AlwaysEnableBooksLibrary;
  sint32 DisableLockdownOfStartPages;
  string ConfigureAdditionalSearchEngines;
  sint32 ClearBrowsingDataOnExit;
  string EnterpriseModeSiteList;
  string EnterpriseSiteListServiceUrl;
  string Homepages;
  sint32 LockdownFavorites;
  sint32 PreventAccessToAboutFlagsInMicrosoftEdge;
  sint32 PreventLiveTileDataCollection;
  sint32 PreventFirstRunPage;
  sint32 PreventSmartScreenPromptOverride;
  sint32 PreventSmartScreenPromptOverrideForFiles;
  sint32 PreventUsingLocalHostIPAddressForWebRTC;
  string ProvisionFavorites;
  sint32 SendIntranetTraffictoInternetExplorer;
  string SetDefaultSearchEngine;
  sint32 ShowMessageWhenOpeningSitesInInternetExplorer;
  sint32 SyncFavoritesBetweenIEAndMicrosoftEdge;
};
```

## <a name="members"></a><span data-ttu-id="45450-111">Membros</span><span class="sxs-lookup"><span data-stu-id="45450-111">Members</span></span>

<span data-ttu-id="45450-112">A **classe \_ \_ Config01 \_ Browser02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="45450-112">The **MDM\_Policy\_Config01\_Browser02** class has these types of members:</span></span>

-   [<span data-ttu-id="45450-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="45450-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="45450-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="45450-114">Properties</span></span>

<span data-ttu-id="45450-115">A **classe \_ \_ Config01 \_ Browser02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="45450-115">The **MDM\_Policy\_Config01\_Browser02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="45450-116">AllowAddressBarDropdown</span><span class="sxs-lookup"><span data-stu-id="45450-116">AllowAddressBarDropdown</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowaddressbardropdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-119">AllowAutofill</span><span class="sxs-lookup"><span data-stu-id="45450-119">AllowAutofill</span></span>](/windows/client-management/mdm/policy-configuration-service-provider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-122">AllowCookies</span><span class="sxs-lookup"><span data-stu-id="45450-122">AllowCookies</span></span>](/windows/client-management/mdm/policy-configuration-service-provider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-125">AllowDeveloperTools</span><span class="sxs-lookup"><span data-stu-id="45450-125">AllowDeveloperTools</span></span>](/windows/client-management/mdm/policy-configuration-service-provider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-128">AllowDoNotTrack</span><span class="sxs-lookup"><span data-stu-id="45450-128">AllowDoNotTrack</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowdonottrack)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-131">AllowExtensions</span><span class="sxs-lookup"><span data-stu-id="45450-131">AllowExtensions</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-134">AllowFlash</span><span class="sxs-lookup"><span data-stu-id="45450-134">AllowFlash</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-137">AllowFlashClickToRun</span><span class="sxs-lookup"><span data-stu-id="45450-137">AllowFlashClickToRun</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflashclicktorun)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-138">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-140">AllowInPrivate</span><span class="sxs-lookup"><span data-stu-id="45450-140">AllowInPrivate</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowinprivate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-141">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-143">AllowMicrosoftCompatibilityList</span><span class="sxs-lookup"><span data-stu-id="45450-143">AllowMicrosoftCompatibilityList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowmicrosoftcompatibilitylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-144">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-146">AllowPasswordManager</span><span class="sxs-lookup"><span data-stu-id="45450-146">AllowPasswordManager</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpasswordmanager)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-147">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-149">AllowPopups</span><span class="sxs-lookup"><span data-stu-id="45450-149">AllowPopups</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpopups)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-150">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-152">AllowSearchEngineCustomization</span><span class="sxs-lookup"><span data-stu-id="45450-152">AllowSearchEngineCustomization</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchenginecustomization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-153">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-154">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-155">AllowSearchSuggestionsinAddressBar</span><span class="sxs-lookup"><span data-stu-id="45450-155">AllowSearchSuggestionsinAddressBar</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchsuggestionsinaddressbar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-156">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-157">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-158">AllowSmartScreen</span><span class="sxs-lookup"><span data-stu-id="45450-158">AllowSmartScreen</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsmartscreen)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-159">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-160">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-161">AlwaysEnableBooksLibrary</span><span class="sxs-lookup"><span data-stu-id="45450-161">AlwaysEnableBooksLibrary</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-alwaysenablebookslibrary)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-162">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-163">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-164">ClearBrowsingDataOnExit</span><span class="sxs-lookup"><span data-stu-id="45450-164">ClearBrowsingDataOnExit</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-clearbrowsingdataonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-165">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-166">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-167">ConfigureAdditionalSearchEngines</span><span class="sxs-lookup"><span data-stu-id="45450-167">ConfigureAdditionalSearchEngines</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-configureadditionalsearchengines)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="45450-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45450-169">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-170">DisableLockdownOfStartPages</span><span class="sxs-lookup"><span data-stu-id="45450-170">DisableLockdownOfStartPages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-disablelockdownofstartpages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-171">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-172">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-173">EnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="45450-173">EnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="45450-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45450-175">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-176">EnterpriseSiteListServiceUrl</span><span class="sxs-lookup"><span data-stu-id="45450-176">EnterpriseSiteListServiceUrl</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisesitelistserviceurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="45450-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45450-178">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-179">Homepages</span><span class="sxs-lookup"><span data-stu-id="45450-179">Homepages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-homepages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="45450-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45450-181">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="45450-182">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="45450-182">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="45450-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45450-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="45450-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45450-185">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="45450-185">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="45450-186">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="45450-186">Identifies the name of the parent node.</span></span> <span data-ttu-id="45450-187">Para essa classe, a cadeia de caracteres é "browser".</span><span class="sxs-lookup"><span data-stu-id="45450-187">For this class, the string is "Browser".</span></span>

</dd> <dt>

[<span data-ttu-id="45450-188">LockdownFavorites</span><span class="sxs-lookup"><span data-stu-id="45450-188">LockdownFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-lockdownfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-189">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-190">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="45450-191">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="45450-191">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="45450-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45450-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="45450-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45450-194">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="45450-194">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="45450-195">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="45450-195">Describes the full path to the parent node.</span></span> <span data-ttu-id="45450-196">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="45450-196">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="45450-197">PreventAccessToAboutFlagsInMicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="45450-197">PreventAccessToAboutFlagsInMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventaccesstoaboutflagsinmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-198">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-198">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-199">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-200">PreventFirstRunPage</span><span class="sxs-lookup"><span data-stu-id="45450-200">PreventFirstRunPage</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventfirstrunpage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-201">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-201">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-202">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-203">PreventLiveTileDataCollection</span><span class="sxs-lookup"><span data-stu-id="45450-203">PreventLiveTileDataCollection</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventlivetiledatacollection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-204">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-204">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-205">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-206">PreventSmartScreenPromptOverride</span><span class="sxs-lookup"><span data-stu-id="45450-206">PreventSmartScreenPromptOverride</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverride)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-207">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-208">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-209">PreventSmartScreenPromptOverrideForFiles</span><span class="sxs-lookup"><span data-stu-id="45450-209">PreventSmartScreenPromptOverrideForFiles</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverrideforfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-210">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-211">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-212">PreventUsingLocalHostIPAddressForWebRTC</span><span class="sxs-lookup"><span data-stu-id="45450-212">PreventUsingLocalHostIPAddressForWebRTC</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventusinglocalhostipaddressforwebrtc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-213">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-213">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-214">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-215">ProvisionFavorites</span><span class="sxs-lookup"><span data-stu-id="45450-215">ProvisionFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-provisionfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-216">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="45450-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45450-217">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-218">SendIntranetTraffictoInternetExplorer</span><span class="sxs-lookup"><span data-stu-id="45450-218">SendIntranetTraffictoInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-sendintranettraffictointernetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-219">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-220">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-221">SetDefaultSearchEngine</span><span class="sxs-lookup"><span data-stu-id="45450-221">SetDefaultSearchEngine</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-setdefaultsearchengine)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-222">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="45450-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45450-223">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-224">ShowMessageWhenOpeningSitesInInternetExplorer</span><span class="sxs-lookup"><span data-stu-id="45450-224">ShowMessageWhenOpeningSitesInInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-showmessagewhenopeningsitesininternetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-225">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-226">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="45450-227">SyncFavoritesBetweenIEAndMicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="45450-227">SyncFavoritesBetweenIEAndMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-syncfavoritesbetweenieandmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45450-228">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="45450-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45450-229">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="45450-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="45450-230">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45450-230">Requirements</span></span>



| <span data-ttu-id="45450-231">Requisito</span><span class="sxs-lookup"><span data-stu-id="45450-231">Requirement</span></span> | <span data-ttu-id="45450-232">Valor</span><span class="sxs-lookup"><span data-stu-id="45450-232">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45450-233">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45450-233">Minimum supported client</span></span><br/> | <span data-ttu-id="45450-234">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="45450-234">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="45450-235">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45450-235">Minimum supported server</span></span><br/> | <span data-ttu-id="45450-236">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="45450-236">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="45450-237">Namespace</span><span class="sxs-lookup"><span data-stu-id="45450-237">Namespace</span></span><br/>                | <span data-ttu-id="45450-238">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="45450-238">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="45450-239">MOF</span><span class="sxs-lookup"><span data-stu-id="45450-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45450-240"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="45450-240"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="45450-241">DLL</span><span class="sxs-lookup"><span data-stu-id="45450-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45450-242"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45450-242"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45450-243">Confira também</span><span class="sxs-lookup"><span data-stu-id="45450-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45450-244">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="45450-244">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

