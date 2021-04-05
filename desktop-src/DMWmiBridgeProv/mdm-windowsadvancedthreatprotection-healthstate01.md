---
title: Classe MDM_WindowsAdvancedThreatProtection_HealthState01
description: A \_ classe MDM WindowsAdvancedThreatProtection \_ HealthState01 é usada para determinar o status de integridade dos pontos de extremidade do WDATP (proteção avançada contra ameaças) do Windows Defender.
ms.assetid: 8d630b95-9895-4cb8-99f2-8f869c4dfd18
keywords:
- Classe MDM_WindowsAdvancedThreatProtection_HealthState01
- Classe MDM_WindowsAdvancedThreatProtection_HealthState01, descrita
topic_type:
- apiref
api_name:
- MDM_WindowsAdvancedThreatProtection_HealthState01
- MDM_WindowsAdvancedThreatProtection_HealthState01.InstanceID
- MDM_WindowsAdvancedThreatProtection_HealthState01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5519b731cf54a633a659ec865e7a1f0e12deda75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918838"
---
# <a name="mdm_windowsadvancedthreatprotection_healthstate01-class"></a><span data-ttu-id="0b611-105">\_ \_ Classe HEALTHSTATE01 do MDM WindowsAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="0b611-105">MDM\_WindowsAdvancedThreatProtection\_HealthState01 class</span></span>

<span data-ttu-id="0b611-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="0b611-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0b611-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="0b611-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0b611-108">A classe **MDM \_ WindowsAdvancedThreatProtection \_ HealthState01** é usada para determinar o status de integridade dos pontos de extremidade do WDATP (proteção avançada contra ameaças) do Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="0b611-108">The **MDM\_WindowsAdvancedThreatProtection\_HealthState01** class is used to determine the health status of Windows Defender Advanced Threat Protection (WDATP) endpoints.</span></span>

<span data-ttu-id="0b611-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0b611-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b611-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b611-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_HealthState01
{
  string   InstanceID;
  string   ParentID;
  datetime LastConnected;
  boolean  SenseIsRunning;
  sint32   OnboardingState;
  string   OrgId;
};
```

## <a name="members"></a><span data-ttu-id="0b611-111">Membros</span><span class="sxs-lookup"><span data-stu-id="0b611-111">Members</span></span>

<span data-ttu-id="0b611-112">A **classe \_ \_ HealthState01 de MDM WindowsAdvancedThreatProtection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0b611-112">The **MDM\_WindowsAdvancedThreatProtection\_HealthState01** class has these types of members:</span></span>

-   [<span data-ttu-id="0b611-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0b611-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b611-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0b611-114">Properties</span></span>

<span data-ttu-id="0b611-115">A **classe \_ \_ HealthState01 do MDM WindowsAdvancedThreatProtection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0b611-115">The **MDM\_WindowsAdvancedThreatProtection\_HealthState01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0b611-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0b611-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b611-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b611-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b611-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b611-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b611-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0b611-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0b611-120">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="0b611-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="0b611-121">Para essa classe, a cadeia de caracteres é "HealthState".</span><span class="sxs-lookup"><span data-stu-id="0b611-121">For this class, the string is "HealthState".</span></span>

</dd> <dt>

[<span data-ttu-id="0b611-122">LastConnected</span><span class="sxs-lookup"><span data-stu-id="0b611-122">LastConnected</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-lastconnected)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b611-123">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0b611-123">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0b611-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b611-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b611-125">OnboardingState</span><span class="sxs-lookup"><span data-stu-id="0b611-125">OnboardingState</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-onboardingstate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b611-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b611-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b611-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b611-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b611-128">OrgId</span><span class="sxs-lookup"><span data-stu-id="0b611-128">OrgId</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-orgid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b611-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b611-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b611-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b611-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b611-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0b611-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b611-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b611-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b611-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b611-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b611-134">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0b611-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0b611-135">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="0b611-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="0b611-136">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/WindowsAdvancedThreatProtection"</span><span class="sxs-lookup"><span data-stu-id="0b611-136">For this class, the string is "./Vendor/MSFT/WindowsAdvancedThreatProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="0b611-137">SenseIsRunning</span><span class="sxs-lookup"><span data-stu-id="0b611-137">SenseIsRunning</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-senseisrunning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b611-138">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0b611-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0b611-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b611-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b611-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b611-140">Requirements</span></span>



| <span data-ttu-id="0b611-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b611-141">Requirement</span></span> | <span data-ttu-id="0b611-142">Valor</span><span class="sxs-lookup"><span data-stu-id="0b611-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b611-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b611-143">Minimum supported client</span></span><br/> | <span data-ttu-id="0b611-144">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0b611-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0b611-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b611-145">Minimum supported server</span></span><br/> | <span data-ttu-id="0b611-146">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0b611-146">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="0b611-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="0b611-147">Namespace</span></span><br/>                | <span data-ttu-id="0b611-148">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="0b611-148">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="0b611-149">MOF</span><span class="sxs-lookup"><span data-stu-id="0b611-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b611-150"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b611-150"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="0b611-151">DLL</span><span class="sxs-lookup"><span data-stu-id="0b611-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b611-152"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="0b611-152"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b611-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b611-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b611-154">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="0b611-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

