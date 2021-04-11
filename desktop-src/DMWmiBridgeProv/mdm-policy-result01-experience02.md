---
title: Classe MDM_Policy_Result01_Experience02
description: A \_ classe MDM Policy \_ Result01 \_ Experience02 representa as políticas de experiência disponíveis.
ms.assetid: c6dc2ef1-1f12-40b0-9d5f-9e886fe1e128
keywords:
- Classe MDM_Policy_Result01_Experience02
- Classe MDM_Policy_Result01_Experience02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Experience02
- MDM_Policy_Result01_Experience02.InstanceID
- MDM_Policy_Result01_Experience02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a767c96d7ee23b4dad9719fa74850b39f0759b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008914"
---
# <a name="mdm_policy_result01_experience02-class"></a><span data-ttu-id="e1148-105">\_Classe MDM \_ Result01 \_ Experience02</span><span class="sxs-lookup"><span data-stu-id="e1148-105">MDM\_Policy\_Result01\_Experience02 class</span></span>

<span data-ttu-id="e1148-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="e1148-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e1148-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="e1148-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e1148-108">A classe **MDM \_ Policy \_ Result01 \_ Experience02** representa as políticas de experiência disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e1148-108">The **MDM\_Policy\_Result01\_Experience02** class represents the experience policies available.</span></span>

<span data-ttu-id="e1148-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e1148-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1148-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1148-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Experience02
{
  string InstanceID;
  string ParentID;
  sint32 AllowCortana;
  sint32 AllowDeviceDiscovery;
  sint32 AllowFindMyDevice;
  sint32 AllowManualMDMUnenrollment;
  sint32 AllowSharingOfOfficeFiles;
  sint32 AllowSIMErrorDialogPromptWhenNoSIM;
  sint32 AllowSaveAsOfOfficeFiles;
  sint32 AllowScreenCapture;
  sint32 AllowSyncMySettings;
  sint32 AllowWindowsTips;
  sint32 DoNotShowFeedbackNotifications;
};
```

## <a name="members"></a><span data-ttu-id="e1148-111">Membros</span><span class="sxs-lookup"><span data-stu-id="e1148-111">Members</span></span>

<span data-ttu-id="e1148-112">A **classe \_ \_ Result01 \_ Experience02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e1148-112">The **MDM\_Policy\_Result01\_Experience02** class has these types of members:</span></span>

-   [<span data-ttu-id="e1148-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e1148-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e1148-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e1148-114">Properties</span></span>

<span data-ttu-id="e1148-115">A **classe \_ \_ Result01 \_ Experience02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e1148-115">The **MDM\_Policy\_Result01\_Experience02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e1148-116">AllowCortana</span><span class="sxs-lookup"><span data-stu-id="e1148-116">AllowCortana</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowcortana)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1148-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e1148-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1148-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e1148-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e1148-119">AllowDeviceDiscovery</span><span class="sxs-lookup"><span data-stu-id="e1148-119">AllowDeviceDiscovery</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowdevicediscovery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1148-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e1148-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1148-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e1148-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e1148-122">AllowFindMyDevice</span><span class="sxs-lookup"><span data-stu-id="e1148-122">AllowFindMyDevice</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowfindmydevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1148-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e1148-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1148-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e1148-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e1148-125">AllowManualMDMUnenrollment</span><span class="sxs-lookup"><span data-stu-id="e1148-125">AllowManualMDMUnenrollment</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowmanualmdmunenrollment)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1148-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e1148-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1148-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e1148-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e1148-128">AllowSaveAsOfOfficeFiles</span><span class="sxs-lookup"><span data-stu-id="e1148-128">AllowSaveAsOfOfficeFiles</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsaveasofofficefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1148-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e1148-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1148-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e1148-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e1148-131">AllowScreenCapture</span><span class="sxs-lookup"><span data-stu-id="e1148-131">AllowScreenCapture</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1148-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e1148-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1148-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e1148-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e1148-134">AllowSharingOfOfficeFiles</span><span class="sxs-lookup"><span data-stu-id="e1148-134">AllowSharingOfOfficeFiles</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsharingofofficefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1148-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e1148-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1148-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e1148-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e1148-137">AllowSIMErrorDialogPromptWhenNoSIM</span><span class="sxs-lookup"><span data-stu-id="e1148-137">AllowSIMErrorDialogPromptWhenNoSIM</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1148-138">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e1148-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1148-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e1148-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e1148-140">AllowSyncMySettings</span><span class="sxs-lookup"><span data-stu-id="e1148-140">AllowSyncMySettings</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsyncmysettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1148-141">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e1148-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1148-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e1148-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e1148-143">AllowWindowsTips</span><span class="sxs-lookup"><span data-stu-id="e1148-143">AllowWindowsTips</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowstips)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1148-144">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e1148-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1148-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e1148-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e1148-146">DoNotShowFeedbackNotifications</span><span class="sxs-lookup"><span data-stu-id="e1148-146">DoNotShowFeedbackNotifications</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-donotshowfeedbacknotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1148-147">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e1148-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1148-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e1148-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e1148-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e1148-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1148-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e1148-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1148-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e1148-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1148-152">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e1148-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e1148-153">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="e1148-153">Identifies the name of the parent node.</span></span> <span data-ttu-id="e1148-154">Para essa classe, a cadeia de caracteres é "Experience".</span><span class="sxs-lookup"><span data-stu-id="e1148-154">For this class, the string is "Experience".</span></span>

</dd> <dt>

<span data-ttu-id="e1148-155">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e1148-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1148-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e1148-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1148-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e1148-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1148-158">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e1148-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e1148-159">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="e1148-159">Describes the full path to the parent node.</span></span> <span data-ttu-id="e1148-160">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="e1148-160">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e1148-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1148-161">Requirements</span></span>



| <span data-ttu-id="e1148-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1148-162">Requirement</span></span> | <span data-ttu-id="e1148-163">Valor</span><span class="sxs-lookup"><span data-stu-id="e1148-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1148-164">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1148-164">Minimum supported client</span></span><br/> | <span data-ttu-id="e1148-165">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e1148-165">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e1148-166">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1148-166">Minimum supported server</span></span><br/> | <span data-ttu-id="e1148-167">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e1148-167">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e1148-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="e1148-168">Namespace</span></span><br/>                | <span data-ttu-id="e1148-169">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="e1148-169">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="e1148-170">MOF</span><span class="sxs-lookup"><span data-stu-id="e1148-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1148-171"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e1148-171"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e1148-172">DLL</span><span class="sxs-lookup"><span data-stu-id="e1148-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1148-173"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1148-173"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1148-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1148-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1148-175">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="e1148-175">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

