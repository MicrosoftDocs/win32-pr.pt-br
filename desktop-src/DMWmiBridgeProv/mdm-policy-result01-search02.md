---
title: Classe MDM_Policy_Result01_Search02
description: A \_ classe Result01 Search02 de política de MDM \_ \_ representa as políticas de pesquisa disponíveis.
ms.assetid: 3025753f-a3cc-430c-bc73-438085ef5c51
keywords:
- Classe MDM_Policy_Result01_Search02
- Classe MDM_Policy_Result01_Search02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Search02
- MDM_Policy_Result01_Search02.InstanceID
- MDM_Policy_Result01_Search02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94a0e25e7f5aa47abcc2b39d9a30a764c5dc9c34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009066"
---
# <a name="mdm_policy_result01_search02-class"></a><span data-ttu-id="1decc-105">\_Classe MDM \_ Result01 \_ Search02</span><span class="sxs-lookup"><span data-stu-id="1decc-105">MDM\_Policy\_Result01\_Search02 class</span></span>

<span data-ttu-id="1decc-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="1decc-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1decc-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="1decc-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1decc-108">A **classe \_ \_ Result01 \_ Search02 de política de MDM** representa as políticas de pesquisa disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1decc-108">The **MDM\_Policy\_Result01\_Search02** class represents the search policies available.</span></span>

<span data-ttu-id="1decc-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1decc-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1decc-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1decc-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Search02
{
  string InstanceID;
  string ParentID;
  sint32 AllowCloudSearch;
  sint32 AllowSearchToUseLocation;
  sint32 AllowStoringImagesFromVisionSearch;
  sint32 AlwaysUseAutoLangDetection;
  sint32 PreventRemoteQueries;
  sint32 PreventIndexingLowDiskSpaceMB;
  sint32 DisableRemovableDriveIndexing;
  sint32 DisableBackoff;
  sint32 AllowUsingDiacritics;
  sint32 AllowWindowsIndexer;
  sint32 AllowIndexingEncryptedStoresOrItems;
};
```

## <a name="members"></a><span data-ttu-id="1decc-111">Membros</span><span class="sxs-lookup"><span data-stu-id="1decc-111">Members</span></span>

<span data-ttu-id="1decc-112">A **classe \_ \_ Result01 \_ Search02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1decc-112">The **MDM\_Policy\_Result01\_Search02** class has these types of members:</span></span>

-   [<span data-ttu-id="1decc-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1decc-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1decc-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1decc-114">Properties</span></span>

<span data-ttu-id="1decc-115">A **classe \_ \_ Result01 \_ Search02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1decc-115">The **MDM\_Policy\_Result01\_Search02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1decc-116">AllowCloudSearch</span><span class="sxs-lookup"><span data-stu-id="1decc-116">AllowCloudSearch</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowcloudsearch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1decc-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1decc-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1decc-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1decc-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1decc-119">AllowIndexingEncryptedStoresOrItems</span><span class="sxs-lookup"><span data-stu-id="1decc-119">AllowIndexingEncryptedStoresOrItems</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowindexingencryptedstoresoritems)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1decc-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1decc-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1decc-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1decc-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1decc-122">AllowSearchToUseLocation</span><span class="sxs-lookup"><span data-stu-id="1decc-122">AllowSearchToUseLocation</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowsearchtouselocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1decc-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1decc-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1decc-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1decc-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1decc-125">AllowStoringImagesFromVisionSearch</span><span class="sxs-lookup"><span data-stu-id="1decc-125">AllowStoringImagesFromVisionSearch</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowstoringimagesfromvisionsearch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1decc-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1decc-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1decc-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1decc-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1decc-128">AllowUsingDiacritics</span><span class="sxs-lookup"><span data-stu-id="1decc-128">AllowUsingDiacritics</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowusingdiacritics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1decc-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1decc-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1decc-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1decc-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1decc-131">AllowWindowsIndexer</span><span class="sxs-lookup"><span data-stu-id="1decc-131">AllowWindowsIndexer</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowwindowsindexer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1decc-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1decc-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1decc-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1decc-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1decc-134">AlwaysUseAutoLangDetection</span><span class="sxs-lookup"><span data-stu-id="1decc-134">AlwaysUseAutoLangDetection</span></span>](/windows/client-management/mdm/policy-csp-search#search-alwaysuseautolangdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1decc-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1decc-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1decc-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1decc-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1decc-137">DisableBackoff</span><span class="sxs-lookup"><span data-stu-id="1decc-137">DisableBackoff</span></span>](/windows/client-management/mdm/policy-csp-search#search-disablebackoff)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1decc-138">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1decc-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1decc-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1decc-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1decc-140">DisableRemovableDriveIndexing</span><span class="sxs-lookup"><span data-stu-id="1decc-140">DisableRemovableDriveIndexing</span></span>](/windows/client-management/mdm/policy-csp-search#search-disableremovabledriveindexing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1decc-141">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1decc-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1decc-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1decc-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1decc-143">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1decc-143">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1decc-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1decc-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1decc-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1decc-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1decc-146">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1decc-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1decc-147">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="1decc-147">Identifies the name of the parent node.</span></span> <span data-ttu-id="1decc-148">Para essa classe, a cadeia de caracteres é "Search".</span><span class="sxs-lookup"><span data-stu-id="1decc-148">For this class, the string is "Search".</span></span>

</dd> <dt>

<span data-ttu-id="1decc-149">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1decc-149">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1decc-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1decc-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1decc-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1decc-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1decc-152">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1decc-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1decc-153">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="1decc-153">Describes the full path to the parent node.</span></span> <span data-ttu-id="1decc-154">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="1decc-154">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="1decc-155">PreventIndexingLowDiskSpaceMB</span><span class="sxs-lookup"><span data-stu-id="1decc-155">PreventIndexingLowDiskSpaceMB</span></span>](/windows/client-management/mdm/policy-csp-search#search-preventindexinglowdiskspacemb)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1decc-156">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1decc-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1decc-157">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1decc-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1decc-158">PreventRemoteQueries</span><span class="sxs-lookup"><span data-stu-id="1decc-158">PreventRemoteQueries</span></span>](/windows/client-management/mdm/policy-csp-search#search-preventremotequeries)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1decc-159">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1decc-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1decc-160">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1decc-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1decc-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1decc-161">Requirements</span></span>



| <span data-ttu-id="1decc-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="1decc-162">Requirement</span></span> | <span data-ttu-id="1decc-163">Valor</span><span class="sxs-lookup"><span data-stu-id="1decc-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1decc-164">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1decc-164">Minimum supported client</span></span><br/> | <span data-ttu-id="1decc-165">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1decc-165">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1decc-166">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1decc-166">Minimum supported server</span></span><br/> | <span data-ttu-id="1decc-167">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1decc-167">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1decc-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="1decc-168">Namespace</span></span><br/>                | <span data-ttu-id="1decc-169">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="1decc-169">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="1decc-170">MOF</span><span class="sxs-lookup"><span data-stu-id="1decc-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1decc-171"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1decc-171"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1decc-172">DLL</span><span class="sxs-lookup"><span data-stu-id="1decc-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1decc-173"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1decc-173"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1decc-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="1decc-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1decc-175">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="1decc-175">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

