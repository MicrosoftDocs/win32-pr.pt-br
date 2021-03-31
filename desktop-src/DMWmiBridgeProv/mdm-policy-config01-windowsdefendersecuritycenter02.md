---
title: Classe MDM_Policy_Config01_WindowsDefenderSecurityCenter02
description: A \_ classe MDM Policy \_ Config01 \_ WindowsDefenderSecurityCenter02 representa as políticas da central de segurança do Windows Defender.
ms.assetid: 406c3992-e9ed-49c5-a4c4-97d91013d416
keywords:
- Classe MDM_Policy_Config01_WindowsDefenderSecurityCenter02
- Classe MDM_Policy_Config01_WindowsDefenderSecurityCenter02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_WindowsDefenderSecurityCenter02
- MDM_Policy_Config01_WindowsDefenderSecurityCenter02.InstanceID
- MDM_Policy_Config01_WindowsDefenderSecurityCenter02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b341eb66cc5d1186a962278babce536c0050523d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824443"
---
# <a name="mdm_policy_config01_windowsdefendersecuritycenter02-class"></a><span data-ttu-id="72a61-105">\_Classe MDM \_ Config01 \_ WindowsDefenderSecurityCenter02</span><span class="sxs-lookup"><span data-stu-id="72a61-105">MDM\_Policy\_Config01\_WindowsDefenderSecurityCenter02 class</span></span>

<span data-ttu-id="72a61-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="72a61-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="72a61-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="72a61-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="72a61-108">A \_ classe MDM Policy \_ Config01 \_ WindowsDefenderSecurityCenter02 representa as políticas da central de segurança do Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="72a61-108">The MDM\_Policy\_Config01\_WindowsDefenderSecurityCenter02 class represents the Windows Defender Security Center policies.</span></span>

<span data-ttu-id="72a61-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="72a61-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="72a61-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72a61-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_WindowsDefenderSecurityCenter02
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

## <a name="members"></a><span data-ttu-id="72a61-111">Membros</span><span class="sxs-lookup"><span data-stu-id="72a61-111">Members</span></span>

<span data-ttu-id="72a61-112">A **classe \_ \_ Config01 \_ WindowsDefenderSecurityCenter02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="72a61-112">The **MDM\_Policy\_Config01\_WindowsDefenderSecurityCenter02** class has these types of members:</span></span>

-   [<span data-ttu-id="72a61-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="72a61-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="72a61-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="72a61-114">Properties</span></span>

<span data-ttu-id="72a61-115">A **classe \_ \_ Config01 \_ WindowsDefenderSecurityCenter02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="72a61-115">The **MDM\_Policy\_Config01\_WindowsDefenderSecurityCenter02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="72a61-116">CompanyName</span><span class="sxs-lookup"><span data-stu-id="72a61-116">CompanyName</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-companyname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="72a61-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="72a61-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72a61-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="72a61-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="72a61-119">DisableAppBrowserUI</span><span class="sxs-lookup"><span data-stu-id="72a61-119">DisableAppBrowserUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disableappbrowserui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="72a61-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="72a61-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="72a61-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="72a61-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="72a61-122">DisableEnhancedNotifications</span><span class="sxs-lookup"><span data-stu-id="72a61-122">DisableEnhancedNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disableenhancednotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="72a61-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="72a61-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="72a61-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="72a61-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="72a61-125">DisableFamilyUI</span><span class="sxs-lookup"><span data-stu-id="72a61-125">DisableFamilyUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablefamilyui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="72a61-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="72a61-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="72a61-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="72a61-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="72a61-128">DisableHealthUI</span><span class="sxs-lookup"><span data-stu-id="72a61-128">DisableHealthUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablehealthui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="72a61-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="72a61-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="72a61-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="72a61-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="72a61-131">DisableNetworkUI</span><span class="sxs-lookup"><span data-stu-id="72a61-131">DisableNetworkUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablenetworkui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="72a61-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="72a61-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="72a61-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="72a61-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="72a61-134">DisableNotifications</span><span class="sxs-lookup"><span data-stu-id="72a61-134">DisableNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablenotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="72a61-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="72a61-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="72a61-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="72a61-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="72a61-137">DisableVirusUI</span><span class="sxs-lookup"><span data-stu-id="72a61-137">DisableVirusUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablevirusui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="72a61-138">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="72a61-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="72a61-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="72a61-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="72a61-140">DisallowExploitProtectionOverride</span><span class="sxs-lookup"><span data-stu-id="72a61-140">DisallowExploitProtectionOverride</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disallowexploitprotectionoverride)
</dt> <dd> <dl> <dt>

<span data-ttu-id="72a61-141">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="72a61-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="72a61-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="72a61-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="72a61-143">Email</span><span class="sxs-lookup"><span data-stu-id="72a61-143">Email</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-email)
</dt> <dd> <dl> <dt>

<span data-ttu-id="72a61-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="72a61-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72a61-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="72a61-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="72a61-146">EnableCustomizedToasts</span><span class="sxs-lookup"><span data-stu-id="72a61-146">EnableCustomizedToasts</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-enablecustomizedtoasts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="72a61-147">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="72a61-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="72a61-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="72a61-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="72a61-149">EnableInAppCustomization</span><span class="sxs-lookup"><span data-stu-id="72a61-149">EnableInAppCustomization</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-enableinappcustomization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="72a61-150">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="72a61-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="72a61-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="72a61-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="72a61-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="72a61-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72a61-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="72a61-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72a61-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72a61-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72a61-155">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="72a61-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="72a61-156">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="72a61-156">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72a61-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="72a61-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72a61-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72a61-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72a61-159">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="72a61-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="72a61-160">Telemóvel</span><span class="sxs-lookup"><span data-stu-id="72a61-160">Phone</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-phone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="72a61-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="72a61-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72a61-162">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="72a61-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="72a61-163">URL</span><span class="sxs-lookup"><span data-stu-id="72a61-163">URL</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-url)
</dt> <dd> <dl> <dt>

<span data-ttu-id="72a61-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="72a61-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72a61-165">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="72a61-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="72a61-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72a61-166">Requirements</span></span>



| <span data-ttu-id="72a61-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="72a61-167">Requirement</span></span> | <span data-ttu-id="72a61-168">Valor</span><span class="sxs-lookup"><span data-stu-id="72a61-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72a61-169">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72a61-169">Minimum supported client</span></span><br/> | <span data-ttu-id="72a61-170">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="72a61-170">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="72a61-171">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72a61-171">Minimum supported server</span></span><br/> | <span data-ttu-id="72a61-172">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="72a61-172">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="72a61-173">Namespace</span><span class="sxs-lookup"><span data-stu-id="72a61-173">Namespace</span></span><br/>                | <span data-ttu-id="72a61-174">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="72a61-174">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="72a61-175">MOF</span><span class="sxs-lookup"><span data-stu-id="72a61-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72a61-176"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72a61-176"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="72a61-177">DLL</span><span class="sxs-lookup"><span data-stu-id="72a61-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72a61-178"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72a61-178"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

