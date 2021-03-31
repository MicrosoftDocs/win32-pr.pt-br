---
title: Classe MDM_Policy_Config01_System02
description: A \_ classe MDM Policy \_ Config01 \_ System02 representa as políticas do sistema disponíveis.
ms.assetid: 0C3E21DF-309C-4AF3-8682-E921BF45BDEF
keywords:
- Classe MDM_Policy_ConfigSource01_System02
- Classe MDM_Policy_ConfigSource01_System02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_ConfigSource01_System02
- MDM_Policy_ConfigSource01_System02.InstanceID
- MDM_Policy_ConfigSource01_System02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d45ae8061b3e383abdd075d461d5b6dc2c46a053
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644693"
---
# <a name="mdm_policy_config01_system02-class"></a><span data-ttu-id="e0a06-105">\_Classe MDM \_ Config01 \_ System02</span><span class="sxs-lookup"><span data-stu-id="e0a06-105">MDM\_Policy\_Config01\_System02 class</span></span>

<span data-ttu-id="e0a06-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="e0a06-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e0a06-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="e0a06-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e0a06-108">A classe **MDM \_ Policy \_ Config01 \_ System02** representa as políticas do sistema disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e0a06-108">The **MDM\_Policy\_Config01\_System02** class represents the System policies available.</span></span> <span data-ttu-id="e0a06-109">Essas políticas determinam as configurações do sistema que são permitidas.</span><span class="sxs-lookup"><span data-stu-id="e0a06-109">These policies determine System configurations that are allowed.</span></span>

<span data-ttu-id="e0a06-110">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e0a06-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0a06-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0a06-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_System02
{
  string InstanceID = "System";
  string ParentID;
  sint32 AllowBuildPreview;
  sint32 AllowEmbeddedMode;
  sint32 AllowExperimentation;
  sint32 AllowFontProviders;
  sint32 AllowLocation;
  sint32 AllowStorageCard;
  sint32 AllowTelemetry;
  string TelemetryProxy;
  sint32 AllowUserToResetPhone;
  string BootStartDriverInitialization;
  sint32 DisableEnterpriseAuthProxy;
  sint32 DisableOneDriveFileSync;
  string DisableSystemRestore;
  sint32 LimitEnhancedDiagnosticDataWindowsAnalytics;
  sint32 FeedbackHubAlwaysSaveDiagnosticsLocally;
};
```

## <a name="members"></a><span data-ttu-id="e0a06-112">Membros</span><span class="sxs-lookup"><span data-stu-id="e0a06-112">Members</span></span>

<span data-ttu-id="e0a06-113">A **classe \_ \_ ConfigSource01 \_ System02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e0a06-113">The **MDM\_Policy\_ConfigSource01\_System02** class has these types of members:</span></span>

-   [<span data-ttu-id="e0a06-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e0a06-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e0a06-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e0a06-115">Properties</span></span>

<span data-ttu-id="e0a06-116">A **classe \_ \_ ConfigSource01 \_ System02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e0a06-116">The **MDM\_Policy\_ConfigSource01\_System02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e0a06-117">AllowBuildPreview</span><span class="sxs-lookup"><span data-stu-id="e0a06-117">AllowBuildPreview</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowbuildpreview)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0a06-118">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e0a06-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0a06-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e0a06-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e0a06-120">AllowEmbeddedMode</span><span class="sxs-lookup"><span data-stu-id="e0a06-120">AllowEmbeddedMode</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowembeddedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0a06-121">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e0a06-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0a06-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e0a06-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e0a06-123">AllowExperimentation</span><span class="sxs-lookup"><span data-stu-id="e0a06-123">AllowExperimentation</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowexperimentation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0a06-124">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e0a06-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0a06-125">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e0a06-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e0a06-126">AllowFontProviders</span><span class="sxs-lookup"><span data-stu-id="e0a06-126">AllowFontProviders</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowfontproviders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0a06-127">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e0a06-127">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0a06-128">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e0a06-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e0a06-129">AllowLocation</span><span class="sxs-lookup"><span data-stu-id="e0a06-129">AllowLocation</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowlocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0a06-130">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e0a06-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0a06-131">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e0a06-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e0a06-132">AllowStorageCard</span><span class="sxs-lookup"><span data-stu-id="e0a06-132">AllowStorageCard</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowstoragecard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0a06-133">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e0a06-133">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0a06-134">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e0a06-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e0a06-135">AllowTelemetry</span><span class="sxs-lookup"><span data-stu-id="e0a06-135">AllowTelemetry</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowtelemetry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0a06-136">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e0a06-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0a06-137">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e0a06-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e0a06-138">AllowUserToResetPhone</span><span class="sxs-lookup"><span data-stu-id="e0a06-138">AllowUserToResetPhone</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowusertoresetphone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0a06-139">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e0a06-139">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0a06-140">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e0a06-140">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e0a06-141">BootStartDriverInitialization</span><span class="sxs-lookup"><span data-stu-id="e0a06-141">BootStartDriverInitialization</span></span>](/windows/client-management/mdm/policy-csp-system#system-bootstartdriverinitialization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0a06-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e0a06-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0a06-143">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e0a06-143">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e0a06-144">DisableEnterpriseAuthProxy</span><span class="sxs-lookup"><span data-stu-id="e0a06-144">DisableEnterpriseAuthProxy</span></span>](/windows/client-management/mdm/policy-csp-system#system-disableenterpriseauthproxy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0a06-145">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e0a06-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0a06-146">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e0a06-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e0a06-147">DisableOneDriveFileSync</span><span class="sxs-lookup"><span data-stu-id="e0a06-147">DisableOneDriveFileSync</span></span>](/windows/client-management/mdm/policy-csp-system#system-disableonedrivefilesync)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0a06-148">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e0a06-148">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0a06-149">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e0a06-149">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e0a06-150">DisableSystemRestore</span><span class="sxs-lookup"><span data-stu-id="e0a06-150">DisableSystemRestore</span></span>](/windows/client-management/mdm/policy-csp-system#system-disablesystemrestore)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0a06-151">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e0a06-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0a06-152">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e0a06-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e0a06-153">FeedbackHubAlwaysSaveDiagnosticsLocally</span><span class="sxs-lookup"><span data-stu-id="e0a06-153">FeedbackHubAlwaysSaveDiagnosticsLocally</span></span>](/windows/client-management/mdm/policy-csp-system#system-feedbackhubalwayssavediagnosticslocally)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0a06-154">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e0a06-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0a06-155">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e0a06-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e0a06-156">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e0a06-156">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0a06-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e0a06-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0a06-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e0a06-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0a06-159">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e0a06-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e0a06-160">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="e0a06-160">Identifies the name of the parent node.</span></span> <span data-ttu-id="e0a06-161">Para essa classe, a cadeia de caracteres é "System".</span><span class="sxs-lookup"><span data-stu-id="e0a06-161">For this class, the string is "System".</span></span>

</dd> <dt>

[<span data-ttu-id="e0a06-162">LimitEnhancedDiagnosticDataWindowsAnalytics</span><span class="sxs-lookup"><span data-stu-id="e0a06-162">LimitEnhancedDiagnosticDataWindowsAnalytics</span></span>](/windows/client-management/mdm/policy-csp-system#system-limitenhanceddiagnosticdatawindowsanalytics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0a06-163">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e0a06-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0a06-164">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e0a06-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e0a06-165">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e0a06-165">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0a06-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e0a06-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0a06-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e0a06-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0a06-168">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e0a06-168">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e0a06-169">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="e0a06-169">Describes the full path to the parent node.</span></span> <span data-ttu-id="e0a06-170">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="e0a06-170">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

<span data-ttu-id="e0a06-171">"./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="e0a06-171">"./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="e0a06-172">TelemetryProxy</span><span class="sxs-lookup"><span data-stu-id="e0a06-172">TelemetryProxy</span></span>](/windows/client-management/mdm/policy-csp-system#system-telemetryproxy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0a06-173">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e0a06-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0a06-174">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e0a06-174">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e0a06-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0a06-175">Requirements</span></span>



| <span data-ttu-id="e0a06-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0a06-176">Requirement</span></span> | <span data-ttu-id="e0a06-177">Valor</span><span class="sxs-lookup"><span data-stu-id="e0a06-177">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0a06-178">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0a06-178">Minimum supported client</span></span><br/> | <span data-ttu-id="e0a06-179">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e0a06-179">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e0a06-180">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0a06-180">Minimum supported server</span></span><br/> | <span data-ttu-id="e0a06-181">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e0a06-181">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e0a06-182">Namespace</span><span class="sxs-lookup"><span data-stu-id="e0a06-182">Namespace</span></span><br/>                | <span data-ttu-id="e0a06-183">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="e0a06-183">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="e0a06-184">MOF</span><span class="sxs-lookup"><span data-stu-id="e0a06-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0a06-185"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0a06-185"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0a06-186">DLL</span><span class="sxs-lookup"><span data-stu-id="e0a06-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0a06-187"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0a06-187"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0a06-188">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0a06-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0a06-189">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="e0a06-189">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

