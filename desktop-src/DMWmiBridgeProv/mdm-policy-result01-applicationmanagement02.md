---
title: Classe MDM_Policy_Result01_ApplicationManagement02
description: A \_ classe MDM Policy \_ Result01 \_ ApplicationManagement02 representa as políticas de gerenciamento de aplicativos disponíveis. \_Result01 política \_ \_ de MDM ApplicationManagement02 classe representa as políticas de gerenciamento de aplicativos disponíveis.
ms.assetid: 141614e4-b2b1-49d9-879c-f6f86bee070c
keywords:
- Classe MDM_Policy_Result01_ApplicationManagement02
- Classe MDM_Policy_Result01_ApplicationManagement02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_ApplicationManagement02
- MDM_Policy_Result01_ApplicationManagement02.InstanceID
- MDM_Policy_Result01_ApplicationManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 477e4e58216c912aa14ec17b8e5879643e3de83f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085622"
---
# <a name="mdm_policy_result01_applicationmanagement02-class"></a><span data-ttu-id="f5cc8-105">\_Classe MDM \_ Result01 \_ ApplicationManagement02</span><span class="sxs-lookup"><span data-stu-id="f5cc8-105">MDM\_Policy\_Result01\_ApplicationManagement02 class</span></span>

<span data-ttu-id="f5cc8-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="f5cc8-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f5cc8-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="f5cc8-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f5cc8-108">A classe **MDM \_ Policy \_ Result01 \_ ApplicationManagement02** representa as políticas de gerenciamento de aplicativos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f5cc8-108">The **MDM\_Policy\_Result01\_ApplicationManagement02** class represents the application management policies available.</span></span>

<span data-ttu-id="f5cc8-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f5cc8-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5cc8-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5cc8-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_ApplicationManagement02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAllTrustedApps;
  sint32 AllowAppStoreAutoUpdate;
  sint32 AllowDeveloperUnlock;
  sint32 AllowGameDVR;
  sint32 AllowSharedUserAppData;
  sint32 DisableStoreOriginatedApps;
  sint32 RestrictAppDataToSystemVolume;
  sint32 RestrictAppToSystemVolume;
};
```

## <a name="members"></a><span data-ttu-id="f5cc8-111">Membros</span><span class="sxs-lookup"><span data-stu-id="f5cc8-111">Members</span></span>

<span data-ttu-id="f5cc8-112">A **classe \_ \_ Result01 \_ ApplicationManagement02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f5cc8-112">The **MDM\_Policy\_Result01\_ApplicationManagement02** class has these types of members:</span></span>

-   [<span data-ttu-id="f5cc8-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f5cc8-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f5cc8-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f5cc8-114">Properties</span></span>

<span data-ttu-id="f5cc8-115">A **classe \_ \_ Result01 \_ ApplicationManagement02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f5cc8-115">The **MDM\_Policy\_Result01\_ApplicationManagement02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f5cc8-116">AllowAllTrustedApps</span><span class="sxs-lookup"><span data-stu-id="f5cc8-116">AllowAllTrustedApps</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowalltrustedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5cc8-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f5cc8-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5cc8-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f5cc8-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f5cc8-119">AllowAppStoreAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="f5cc8-119">AllowAppStoreAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowappstoreautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5cc8-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f5cc8-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5cc8-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f5cc8-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f5cc8-122">AllowDeveloperUnlock</span><span class="sxs-lookup"><span data-stu-id="f5cc8-122">AllowDeveloperUnlock</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowdeveloperunlock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5cc8-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f5cc8-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5cc8-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f5cc8-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f5cc8-125">AllowGameDVR</span><span class="sxs-lookup"><span data-stu-id="f5cc8-125">AllowGameDVR</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowgamedvr)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5cc8-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f5cc8-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5cc8-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f5cc8-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f5cc8-128">AllowSharedUserAppData</span><span class="sxs-lookup"><span data-stu-id="f5cc8-128">AllowSharedUserAppData</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowshareduserappdata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5cc8-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f5cc8-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5cc8-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f5cc8-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f5cc8-131">DisableStoreOriginatedApps</span><span class="sxs-lookup"><span data-stu-id="f5cc8-131">DisableStoreOriginatedApps</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-disablestoreoriginatedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5cc8-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f5cc8-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5cc8-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f5cc8-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f5cc8-134">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f5cc8-134">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5cc8-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f5cc8-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5cc8-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f5cc8-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5cc8-137">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f5cc8-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f5cc8-138">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="f5cc8-138">Identifies the name of the parent node.</span></span> <span data-ttu-id="f5cc8-139">Para essa classe, a cadeia de caracteres é "ApplicationManagement".</span><span class="sxs-lookup"><span data-stu-id="f5cc8-139">For this class, the string is "ApplicationManagement".</span></span>

</dd> <dt>

<span data-ttu-id="f5cc8-140">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f5cc8-140">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5cc8-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f5cc8-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5cc8-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f5cc8-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5cc8-143">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f5cc8-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f5cc8-144">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="f5cc8-144">Describes the full path to the parent node.</span></span> <span data-ttu-id="f5cc8-145">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="f5cc8-145">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="f5cc8-146">RestrictAppDataToSystemVolume</span><span class="sxs-lookup"><span data-stu-id="f5cc8-146">RestrictAppDataToSystemVolume</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-restrictappdatatosystemvolume)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5cc8-147">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f5cc8-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5cc8-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f5cc8-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f5cc8-149">RestrictAppToSystemVolume</span><span class="sxs-lookup"><span data-stu-id="f5cc8-149">RestrictAppToSystemVolume</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-restrictapptosystemvolume)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5cc8-150">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f5cc8-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5cc8-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f5cc8-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5cc8-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5cc8-152">Requirements</span></span>



| <span data-ttu-id="f5cc8-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5cc8-153">Requirement</span></span> | <span data-ttu-id="f5cc8-154">Valor</span><span class="sxs-lookup"><span data-stu-id="f5cc8-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5cc8-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5cc8-155">Minimum supported client</span></span><br/> | <span data-ttu-id="f5cc8-156">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f5cc8-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f5cc8-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5cc8-157">Minimum supported server</span></span><br/> | <span data-ttu-id="f5cc8-158">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f5cc8-158">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f5cc8-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="f5cc8-159">Namespace</span></span><br/>                | <span data-ttu-id="f5cc8-160">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="f5cc8-160">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="f5cc8-161">MOF</span><span class="sxs-lookup"><span data-stu-id="f5cc8-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5cc8-162"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5cc8-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5cc8-163">DLL</span><span class="sxs-lookup"><span data-stu-id="f5cc8-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5cc8-164"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5cc8-164"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5cc8-165">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f5cc8-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5cc8-166">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="f5cc8-166">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

