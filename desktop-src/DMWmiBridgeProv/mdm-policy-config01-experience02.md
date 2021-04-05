---
title: Classe MDM_Policy_Config01_Experience02
description: A \_ classe MDM Policy \_ Config01 \_ Experience02 representa as políticas de experiência disponíveis.
ms.assetid: 21052983-696c-4137-9c72-16ea3b4a1eb7
keywords:
- Classe MDM_Policy_Config01_Experience02
- Classe MDM_Policy_Config01_Experience02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Experience02
- MDM_Policy_Config01_Experience02.InstanceID
- MDM_Policy_Config01_Experience02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38885dbc22c51bfa9e1653f81dba38255f6ba6a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086236"
---
# <a name="mdm_policy_config01_experience02-class"></a><span data-ttu-id="0ff05-105">\_Classe MDM \_ Config01 \_ Experience02</span><span class="sxs-lookup"><span data-stu-id="0ff05-105">MDM\_Policy\_Config01\_Experience02 class</span></span>

<span data-ttu-id="0ff05-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="0ff05-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0ff05-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="0ff05-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0ff05-108">A classe **MDM \_ Policy \_ Config01 \_ Experience02** representa as políticas de experiência disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0ff05-108">The **MDM\_Policy\_Config01\_Experience02** class represents the experience policies available.</span></span>

<span data-ttu-id="0ff05-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0ff05-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ff05-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0ff05-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Experience02
{
  string InstanceID;
  string ParentID;
  sint32 AllowCortana;
  sint32 AllowDeviceDiscovery;
  sint32 AllowFindMyDevice;
  sint32 AllowManualMDMUnenrollment;
  sint32 AllowSaveAsOfOfficeFiles;
  sint32 AllowScreenCapture;
  sint32 AllowSIMErrorDialogPromptWhenNoSIM;
  sint32 AllowSharingOfOfficeFiles;
  sint32 AllowSyncMySettings;
  sint32 AllowWindowsTips;
  sint32 DoNotShowFeedbackNotifications;
};
```

## <a name="members"></a><span data-ttu-id="0ff05-111">Membros</span><span class="sxs-lookup"><span data-stu-id="0ff05-111">Members</span></span>

<span data-ttu-id="0ff05-112">A **classe \_ \_ Config01 \_ Experience02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0ff05-112">The **MDM\_Policy\_Config01\_Experience02** class has these types of members:</span></span>

-   [<span data-ttu-id="0ff05-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0ff05-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0ff05-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0ff05-114">Properties</span></span>

<span data-ttu-id="0ff05-115">A **classe \_ \_ Config01 \_ Experience02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0ff05-115">The **MDM\_Policy\_Config01\_Experience02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0ff05-116">AllowCortana</span><span class="sxs-lookup"><span data-stu-id="0ff05-116">AllowCortana</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowcortana)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ff05-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0ff05-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ff05-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0ff05-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ff05-119">AllowDeviceDiscovery</span><span class="sxs-lookup"><span data-stu-id="0ff05-119">AllowDeviceDiscovery</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowdevicediscovery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ff05-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0ff05-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ff05-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0ff05-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ff05-122">AllowFindMyDevice</span><span class="sxs-lookup"><span data-stu-id="0ff05-122">AllowFindMyDevice</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowfindmydevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ff05-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0ff05-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ff05-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0ff05-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ff05-125">AllowManualMDMUnenrollment</span><span class="sxs-lookup"><span data-stu-id="0ff05-125">AllowManualMDMUnenrollment</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowmanualmdmunenrollment)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ff05-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0ff05-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ff05-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0ff05-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ff05-128">AllowSaveAsOfOfficeFiles</span><span class="sxs-lookup"><span data-stu-id="0ff05-128">AllowSaveAsOfOfficeFiles</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsaveasofofficefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ff05-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0ff05-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ff05-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0ff05-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0ff05-131">AllowScreenCapture</span><span class="sxs-lookup"><span data-stu-id="0ff05-131">AllowScreenCapture</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ff05-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0ff05-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ff05-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0ff05-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ff05-134">AllowSharingOfOfficeFiles</span><span class="sxs-lookup"><span data-stu-id="0ff05-134">AllowSharingOfOfficeFiles</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsharingofofficefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ff05-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0ff05-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ff05-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0ff05-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0ff05-137">AllowSIMErrorDialogPromptWhenNoSIM</span><span class="sxs-lookup"><span data-stu-id="0ff05-137">AllowSIMErrorDialogPromptWhenNoSIM</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ff05-138">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0ff05-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ff05-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0ff05-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ff05-140">AllowSyncMySettings</span><span class="sxs-lookup"><span data-stu-id="0ff05-140">AllowSyncMySettings</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsyncmysettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ff05-141">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0ff05-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ff05-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0ff05-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ff05-143">AllowWindowsTips</span><span class="sxs-lookup"><span data-stu-id="0ff05-143">AllowWindowsTips</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowstips)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ff05-144">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0ff05-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ff05-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0ff05-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ff05-146">DoNotShowFeedbackNotifications</span><span class="sxs-lookup"><span data-stu-id="0ff05-146">DoNotShowFeedbackNotifications</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-donotshowfeedbacknotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ff05-147">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0ff05-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ff05-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0ff05-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0ff05-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0ff05-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ff05-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0ff05-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ff05-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ff05-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ff05-152">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0ff05-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0ff05-153">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="0ff05-153">Identifies the name of the parent node.</span></span> <span data-ttu-id="0ff05-154">Para essa classe, a cadeia de caracteres é "Experience".</span><span class="sxs-lookup"><span data-stu-id="0ff05-154">For this class, the string is "Experience".</span></span>

</dd> <dt>

<span data-ttu-id="0ff05-155">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0ff05-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ff05-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0ff05-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ff05-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ff05-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ff05-158">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0ff05-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0ff05-159">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="0ff05-159">Describes the full path to the parent node.</span></span> <span data-ttu-id="0ff05-160">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="0ff05-160">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ff05-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ff05-161">Requirements</span></span>



| <span data-ttu-id="0ff05-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ff05-162">Requirement</span></span> | <span data-ttu-id="0ff05-163">Valor</span><span class="sxs-lookup"><span data-stu-id="0ff05-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ff05-164">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ff05-164">Minimum supported client</span></span><br/> | <span data-ttu-id="0ff05-165">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0ff05-165">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0ff05-166">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ff05-166">Minimum supported server</span></span><br/> | <span data-ttu-id="0ff05-167">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0ff05-167">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0ff05-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="0ff05-168">Namespace</span></span><br/>                | <span data-ttu-id="0ff05-169">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="0ff05-169">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="0ff05-170">MOF</span><span class="sxs-lookup"><span data-stu-id="0ff05-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ff05-171"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ff05-171"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ff05-172">DLL</span><span class="sxs-lookup"><span data-stu-id="0ff05-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ff05-173"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ff05-173"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ff05-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ff05-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ff05-175">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="0ff05-175">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

