---
title: Classe MDM_Policy_Result01_Browser02
description: A \_ classe Result01 Browser02 de política de MDM \_ \_ representa as políticas de navegador disponíveis. \_ \_ Result01 de política MDM \_ Browser02 classe representa as políticas de navegador disponíveis.
ms.assetid: 06dc9f68-d9ea-4eec-93cb-1f26e8a6050d
keywords:
- Classe MDM_Policy_Result01_Browser02
- Classe MDM_Policy_Result01_Browser02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Browser02
- MDM_Policy_Result01_Browser02.InstanceID
- MDM_Policy_Result01_Browser02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d132c43b88b242864e248b705a0f6bca02e546
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824188"
---
# <a name="mdm_policy_result01_browser02-class"></a><span data-ttu-id="91447-105">\_Classe MDM \_ Result01 \_ Browser02</span><span class="sxs-lookup"><span data-stu-id="91447-105">MDM\_Policy\_Result01\_Browser02 class</span></span>

<span data-ttu-id="91447-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="91447-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="91447-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="91447-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="91447-108">A **classe \_ \_ Result01 \_ Browser02 de política de MDM** representa as políticas de navegador disponíveis.</span><span class="sxs-lookup"><span data-stu-id="91447-108">The **MDM\_Policy\_Result01\_Browser02** class represents the browser policies available.</span></span>

<span data-ttu-id="91447-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="91447-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="91447-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91447-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Browser02
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

## <a name="members"></a><span data-ttu-id="91447-111">Membros</span><span class="sxs-lookup"><span data-stu-id="91447-111">Members</span></span>

<span data-ttu-id="91447-112">A **classe \_ \_ Result01 \_ Browser02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="91447-112">The **MDM\_Policy\_Result01\_Browser02** class has these types of members:</span></span>

-   [<span data-ttu-id="91447-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="91447-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="91447-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="91447-114">Properties</span></span>

<span data-ttu-id="91447-115">A **classe \_ \_ Result01 \_ Browser02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="91447-115">The **MDM\_Policy\_Result01\_Browser02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="91447-116">AllowAddressBarDropdown</span><span class="sxs-lookup"><span data-stu-id="91447-116">AllowAddressBarDropdown</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowaddressbardropdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-119">AllowAutofill</span><span class="sxs-lookup"><span data-stu-id="91447-119">AllowAutofill</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowautofill)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-122">AllowCookies</span><span class="sxs-lookup"><span data-stu-id="91447-122">AllowCookies</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowcookies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-125">AllowDeveloperTools</span><span class="sxs-lookup"><span data-stu-id="91447-125">AllowDeveloperTools</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowdevelopertools)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-128">AllowDoNotTrack</span><span class="sxs-lookup"><span data-stu-id="91447-128">AllowDoNotTrack</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowdonottrack)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-131">AllowExtensions</span><span class="sxs-lookup"><span data-stu-id="91447-131">AllowExtensions</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-134">AllowFlash</span><span class="sxs-lookup"><span data-stu-id="91447-134">AllowFlash</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-137">AllowFlashClickToRun</span><span class="sxs-lookup"><span data-stu-id="91447-137">AllowFlashClickToRun</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflashclicktorun)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-138">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-140">AllowInPrivate</span><span class="sxs-lookup"><span data-stu-id="91447-140">AllowInPrivate</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowinprivate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-141">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-143">AllowMicrosoftCompatibilityList</span><span class="sxs-lookup"><span data-stu-id="91447-143">AllowMicrosoftCompatibilityList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowmicrosoftcompatibilitylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-144">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-146">AllowPasswordManager</span><span class="sxs-lookup"><span data-stu-id="91447-146">AllowPasswordManager</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpasswordmanager)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-147">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-149">AllowPopups</span><span class="sxs-lookup"><span data-stu-id="91447-149">AllowPopups</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpopups)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-150">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-152">AllowSearchEngineCustomization</span><span class="sxs-lookup"><span data-stu-id="91447-152">AllowSearchEngineCustomization</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchenginecustomization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-153">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-154">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-155">AllowSearchSuggestionsinAddressBar</span><span class="sxs-lookup"><span data-stu-id="91447-155">AllowSearchSuggestionsinAddressBar</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchsuggestionsinaddressbar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-156">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-157">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-158">AllowSmartScreen</span><span class="sxs-lookup"><span data-stu-id="91447-158">AllowSmartScreen</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsmartscreen)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-159">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-160">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-161">AlwaysEnableBooksLibrary</span><span class="sxs-lookup"><span data-stu-id="91447-161">AlwaysEnableBooksLibrary</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-alwaysenablebookslibrary)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-162">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-163">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-164">ClearBrowsingDataOnExit</span><span class="sxs-lookup"><span data-stu-id="91447-164">ClearBrowsingDataOnExit</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-clearbrowsingdataonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-165">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-166">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-167">ConfigureAdditionalSearchEngines</span><span class="sxs-lookup"><span data-stu-id="91447-167">ConfigureAdditionalSearchEngines</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-configureadditionalsearchengines)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="91447-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91447-169">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-170">DisableLockdownOfStartPages</span><span class="sxs-lookup"><span data-stu-id="91447-170">DisableLockdownOfStartPages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-disablelockdownofstartpages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-171">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-172">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-173">EnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="91447-173">EnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="91447-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91447-175">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-176">EnterpriseSiteListServiceUrl</span><span class="sxs-lookup"><span data-stu-id="91447-176">EnterpriseSiteListServiceUrl</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisesitelistserviceurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="91447-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91447-178">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-179">Homepages</span><span class="sxs-lookup"><span data-stu-id="91447-179">Homepages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-homepages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="91447-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91447-181">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="91447-182">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="91447-182">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="91447-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91447-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="91447-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91447-185">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="91447-185">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="91447-186">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="91447-186">Identifies the name of the parent node.</span></span> <span data-ttu-id="91447-187">Para essa classe, a cadeia de caracteres é "browser".</span><span class="sxs-lookup"><span data-stu-id="91447-187">For this class, the string is "Browser".</span></span>

</dd> <dt>

[<span data-ttu-id="91447-188">LockdownFavorites</span><span class="sxs-lookup"><span data-stu-id="91447-188">LockdownFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-lockdownfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-189">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-190">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="91447-191">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="91447-191">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="91447-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91447-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="91447-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91447-194">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="91447-194">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="91447-195">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="91447-195">Describes the full path to the parent node.</span></span> <span data-ttu-id="91447-196">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="91447-196">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="91447-197">PreventAccessToAboutFlagsInMicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="91447-197">PreventAccessToAboutFlagsInMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventaccesstoaboutflagsinmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-198">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-198">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-199">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-200">PreventFirstRunPage</span><span class="sxs-lookup"><span data-stu-id="91447-200">PreventFirstRunPage</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventfirstrunpage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-201">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-201">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-202">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-203">PreventLiveTileDataCollection</span><span class="sxs-lookup"><span data-stu-id="91447-203">PreventLiveTileDataCollection</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventlivetiledatacollection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-204">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-204">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-205">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-206">PreventSmartScreenPromptOverride</span><span class="sxs-lookup"><span data-stu-id="91447-206">PreventSmartScreenPromptOverride</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverride)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-207">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-208">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-209">PreventSmartScreenPromptOverrideForFiles</span><span class="sxs-lookup"><span data-stu-id="91447-209">PreventSmartScreenPromptOverrideForFiles</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverrideforfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-210">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-211">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-212">PreventUsingLocalHostIPAddressForWebRTC</span><span class="sxs-lookup"><span data-stu-id="91447-212">PreventUsingLocalHostIPAddressForWebRTC</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventusinglocalhostipaddressforwebrtc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-213">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-213">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-214">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-215">ProvisionFavorites</span><span class="sxs-lookup"><span data-stu-id="91447-215">ProvisionFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-provisionfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-216">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="91447-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91447-217">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-218">SendIntranetTraffictoInternetExplorer</span><span class="sxs-lookup"><span data-stu-id="91447-218">SendIntranetTraffictoInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-sendintranettraffictointernetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-219">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-220">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-221">SetDefaultSearchEngine</span><span class="sxs-lookup"><span data-stu-id="91447-221">SetDefaultSearchEngine</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-setdefaultsearchengine)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-222">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="91447-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91447-223">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-224">ShowMessageWhenOpeningSitesInInternetExplorer</span><span class="sxs-lookup"><span data-stu-id="91447-224">ShowMessageWhenOpeningSitesInInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-showmessagewhenopeningsitesininternetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-225">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-226">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91447-227">SyncFavoritesBetweenIEAndMicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="91447-227">SyncFavoritesBetweenIEAndMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-syncfavoritesbetweenieandmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91447-228">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91447-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91447-229">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91447-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="91447-230">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91447-230">Requirements</span></span>



| <span data-ttu-id="91447-231">Requisito</span><span class="sxs-lookup"><span data-stu-id="91447-231">Requirement</span></span> | <span data-ttu-id="91447-232">Valor</span><span class="sxs-lookup"><span data-stu-id="91447-232">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91447-233">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91447-233">Minimum supported client</span></span><br/> | <span data-ttu-id="91447-234">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="91447-234">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="91447-235">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91447-235">Minimum supported server</span></span><br/> | <span data-ttu-id="91447-236">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="91447-236">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="91447-237">Namespace</span><span class="sxs-lookup"><span data-stu-id="91447-237">Namespace</span></span><br/>                | <span data-ttu-id="91447-238">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="91447-238">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="91447-239">MOF</span><span class="sxs-lookup"><span data-stu-id="91447-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91447-240"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="91447-240"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="91447-241">DLL</span><span class="sxs-lookup"><span data-stu-id="91447-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91447-242"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91447-242"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91447-243">Confira também</span><span class="sxs-lookup"><span data-stu-id="91447-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91447-244">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="91447-244">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

