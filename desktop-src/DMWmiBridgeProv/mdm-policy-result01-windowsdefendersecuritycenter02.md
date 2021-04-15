---
title: Classe MDM_Policy_Result01_WindowsDefenderSecurityCenter02
description: A \_ classe MDM Policy \_ Result01 \_ WindowsDefenderSecurityCenter02 representa as políticas da central de segurança do Windows Defender.
ms.assetid: 59047e16-a188-4ec9-9d1b-db2b15c1109b
keywords:
- Classe MDM_Policy_Result01_WindowsDefenderSecurityCenter02
- Classe MDM_Policy_Result01_WindowsDefenderSecurityCenter02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_WindowsDefenderSecurityCenter02
- MDM_Policy_Result01_WindowsDefenderSecurityCenter02.InstanceID
- MDM_Policy_Result01_WindowsDefenderSecurityCenter02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7739410347169637ca5f27fef5627e26f8347c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454678"
---
# <a name="mdm_policy_result01_windowsdefendersecuritycenter02-class"></a><span data-ttu-id="0a54d-105">\_Classe MDM \_ Result01 \_ WindowsDefenderSecurityCenter02</span><span class="sxs-lookup"><span data-stu-id="0a54d-105">MDM\_Policy\_Result01\_WindowsDefenderSecurityCenter02 class</span></span>

<span data-ttu-id="0a54d-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="0a54d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0a54d-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="0a54d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0a54d-108">A \_ classe MDM Policy \_ Result01 \_ WindowsDefenderSecurityCenter02 representa as políticas da central de segurança do Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="0a54d-108">The MDM\_Policy\_Result01\_WindowsDefenderSecurityCenter02 class represents the Windows Defender Security Center policies.</span></span>

<span data-ttu-id="0a54d-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0a54d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a54d-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a54d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_WindowsDefenderSecurityCenter02
{
  string InstanceID;
  string ParentID;
  string CompanyName;
  sint32 DisableAppBrowserUI;
  sint32 DisableEnhancedNotifications;
  sint32 DisableFamilyUI;
  sint32 DisableHealthUI;
  sint32 DisableNetworkUI;
  sint32 DisableNotifications;
  sint32 DisableVirusUI;
  sint32 DisallowExploitProtectionOverride;
  string Email;
  sint32 EnableCustomizedToasts;
  sint32 EnableInAppCustomization;
  string Phone;
  string URL;
};
```

## <a name="members"></a><span data-ttu-id="0a54d-111">Membros</span><span class="sxs-lookup"><span data-stu-id="0a54d-111">Members</span></span>

<span data-ttu-id="0a54d-112">A **classe \_ \_ Result01 \_ WindowsDefenderSecurityCenter02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0a54d-112">The **MDM\_Policy\_Result01\_WindowsDefenderSecurityCenter02** class has these types of members:</span></span>

-   [<span data-ttu-id="0a54d-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0a54d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0a54d-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0a54d-114">Properties</span></span>

<span data-ttu-id="0a54d-115">A **classe \_ \_ Result01 \_ WindowsDefenderSecurityCenter02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0a54d-115">The **MDM\_Policy\_Result01\_WindowsDefenderSecurityCenter02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0a54d-116">CompanyName</span><span class="sxs-lookup"><span data-stu-id="0a54d-116">CompanyName</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-companyname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a54d-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0a54d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a54d-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0a54d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0a54d-119">DisableAppBrowserUI</span><span class="sxs-lookup"><span data-stu-id="0a54d-119">DisableAppBrowserUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disableappbrowserui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a54d-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0a54d-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a54d-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0a54d-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0a54d-122">DisableEnhancedNotifications</span><span class="sxs-lookup"><span data-stu-id="0a54d-122">DisableEnhancedNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disableenhancednotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a54d-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0a54d-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a54d-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0a54d-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0a54d-125">DisableFamilyUI</span><span class="sxs-lookup"><span data-stu-id="0a54d-125">DisableFamilyUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablefamilyui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a54d-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0a54d-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a54d-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0a54d-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0a54d-128">DisableHealthUI</span><span class="sxs-lookup"><span data-stu-id="0a54d-128">DisableHealthUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablehealthui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a54d-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0a54d-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a54d-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0a54d-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0a54d-131">DisableNetworkUI</span><span class="sxs-lookup"><span data-stu-id="0a54d-131">DisableNetworkUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablenetworkui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a54d-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0a54d-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a54d-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0a54d-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0a54d-134">DisableNotifications</span><span class="sxs-lookup"><span data-stu-id="0a54d-134">DisableNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablenotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a54d-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0a54d-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a54d-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0a54d-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0a54d-137">DisableVirusUI</span><span class="sxs-lookup"><span data-stu-id="0a54d-137">DisableVirusUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablevirusui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a54d-138">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0a54d-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a54d-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0a54d-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0a54d-140">DisallowExploitProtectionOverride</span><span class="sxs-lookup"><span data-stu-id="0a54d-140">DisallowExploitProtectionOverride</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disallowexploitprotectionoverride)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a54d-141">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0a54d-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a54d-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0a54d-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0a54d-143">Email</span><span class="sxs-lookup"><span data-stu-id="0a54d-143">Email</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-email)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a54d-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0a54d-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a54d-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0a54d-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0a54d-146">EnableCustomizedToasts</span><span class="sxs-lookup"><span data-stu-id="0a54d-146">EnableCustomizedToasts</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-enablecustomizedtoasts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a54d-147">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0a54d-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a54d-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0a54d-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0a54d-149">EnableInAppCustomization</span><span class="sxs-lookup"><span data-stu-id="0a54d-149">EnableInAppCustomization</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-enableinappcustomization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a54d-150">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0a54d-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a54d-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0a54d-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0a54d-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0a54d-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a54d-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0a54d-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a54d-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0a54d-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a54d-155">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0a54d-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0a54d-156">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0a54d-156">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a54d-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0a54d-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a54d-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0a54d-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a54d-159">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0a54d-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0a54d-160">Telefone</span><span class="sxs-lookup"><span data-stu-id="0a54d-160">Phone</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-phone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a54d-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0a54d-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a54d-162">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0a54d-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0a54d-163">URL</span><span class="sxs-lookup"><span data-stu-id="0a54d-163">URL</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-url)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a54d-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0a54d-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a54d-165">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0a54d-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0a54d-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a54d-166">Requirements</span></span>



| <span data-ttu-id="0a54d-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a54d-167">Requirement</span></span> | <span data-ttu-id="0a54d-168">Valor</span><span class="sxs-lookup"><span data-stu-id="0a54d-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a54d-169">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a54d-169">Minimum supported client</span></span><br/> | <span data-ttu-id="0a54d-170">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0a54d-170">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0a54d-171">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a54d-171">Minimum supported server</span></span><br/> | <span data-ttu-id="0a54d-172">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0a54d-172">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0a54d-173">Namespace</span><span class="sxs-lookup"><span data-stu-id="0a54d-173">Namespace</span></span><br/>                | <span data-ttu-id="0a54d-174">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="0a54d-174">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0a54d-175">MOF</span><span class="sxs-lookup"><span data-stu-id="0a54d-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a54d-176"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0a54d-176"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a54d-177">DLL</span><span class="sxs-lookup"><span data-stu-id="0a54d-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a54d-178"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a54d-178"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

