---
title: Classe MDM_WindowsAdvancedThreatProtection_Configuration01
description: A \_ classe MDM WindowsAdvancedThreatProtection \_ Configuration01 é usada para determinar a configuração dos pontos de extremidade do WDATP (proteção avançada contra ameaças) do Windows Defender.
ms.assetid: b4b2ff02-3836-4044-b8fa-d3405f433d8c
keywords:
- Classe MDM_WindowsAdvancedThreatProtection_Configuration01
- Classe MDM_WindowsAdvancedThreatProtection_Configuration01, descrita
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MDM_WindowsAdvancedThreatProtection_Configuration01
- MDM_WindowsAdvancedThreatProtection_Configuration01.InstanceID
- MDM_WindowsAdvancedThreatProtection_Configuration01.ParentID
- MDM_WindowsAdvancedThreatProtection_Configuration01.GroupIds
api_type:
- DllExport
api_location:
- Mofs\DMWmiBridgeProv.dll
ms.openlocfilehash: c6cd6689a66735790c381ac307a443c08464a379
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499590"
---
# <a name="mdm_windowsadvancedthreatprotection_configuration01-class"></a><span data-ttu-id="0ea3c-105">\_ \_ Classe CONFIGURATION01 do MDM WindowsAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="0ea3c-105">MDM\_WindowsAdvancedThreatProtection\_Configuration01 class</span></span>

<span data-ttu-id="0ea3c-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="0ea3c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0ea3c-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="0ea3c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0ea3c-108">A classe **MDM \_ WindowsAdvancedThreatProtection \_ Configuration01** é usada para determinar a configuração dos pontos de extremidade do WDATP (proteção avançada contra ameaças) do Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="0ea3c-108">The **MDM\_WindowsAdvancedThreatProtection\_Configuration01** class is used to determine the configuration of Windows Defender Advanced Threat Protection (WDATP) endpoints.</span></span>

<span data-ttu-id="0ea3c-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0ea3c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ea3c-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0ea3c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_Configuration01
{
  string InstanceID;
  string ParentID;
  sint32 SampleSharing;
  string GroupIds;
  sint32 TelemetryReportingFrequency;
};
```

## <a name="members"></a><span data-ttu-id="0ea3c-111">Membros</span><span class="sxs-lookup"><span data-stu-id="0ea3c-111">Members</span></span>

<span data-ttu-id="0ea3c-112">A **classe \_ \_ Configuration01 de MDM WindowsAdvancedThreatProtection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0ea3c-112">The **MDM\_WindowsAdvancedThreatProtection\_Configuration01** class has these types of members:</span></span>

-   [<span data-ttu-id="0ea3c-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0ea3c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0ea3c-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0ea3c-114">Properties</span></span>

<span data-ttu-id="0ea3c-115">A **classe \_ \_ Configuration01 do MDM WindowsAdvancedThreatProtection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0ea3c-115">The **MDM\_WindowsAdvancedThreatProtection\_Configuration01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0ea3c-116">**GroupIds**</span><span class="sxs-lookup"><span data-stu-id="0ea3c-116">**GroupIds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea3c-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0ea3c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ea3c-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0ea3c-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0ea3c-119">TBD</span><span class="sxs-lookup"><span data-stu-id="0ea3c-119">TBD</span></span>

</dd> <dt>

<span data-ttu-id="0ea3c-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0ea3c-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea3c-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0ea3c-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ea3c-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ea3c-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea3c-123">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0ea3c-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0ea3c-124">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="0ea3c-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="0ea3c-125">Para essa classe, a cadeia de caracteres é "configuração".</span><span class="sxs-lookup"><span data-stu-id="0ea3c-125">For this class, the string is "Configuration".</span></span>

</dd> <dt>

<span data-ttu-id="0ea3c-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0ea3c-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea3c-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0ea3c-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ea3c-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ea3c-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea3c-129">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0ea3c-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0ea3c-130">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="0ea3c-130">Describes the full path to the parent node.</span></span> <span data-ttu-id="0ea3c-131">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/WindowsAdvancedThreatProtection"</span><span class="sxs-lookup"><span data-stu-id="0ea3c-131">For this class, the string is "./Vendor/MSFT/WindowsAdvancedThreatProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="0ea3c-132">SampleSharing</span><span class="sxs-lookup"><span data-stu-id="0ea3c-132">SampleSharing</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#configuration-samplesharing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea3c-133">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0ea3c-133">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ea3c-134">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0ea3c-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ea3c-135">TelemetryReportingFrequency</span><span class="sxs-lookup"><span data-stu-id="0ea3c-135">TelemetryReportingFrequency</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#configuration-telemetryreportingfrequency)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea3c-136">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0ea3c-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ea3c-137">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0ea3c-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ea3c-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ea3c-138">Requirements</span></span>



| <span data-ttu-id="0ea3c-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ea3c-139">Requirement</span></span> | <span data-ttu-id="0ea3c-140">Valor</span><span class="sxs-lookup"><span data-stu-id="0ea3c-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ea3c-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ea3c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="0ea3c-142">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0ea3c-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0ea3c-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ea3c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="0ea3c-144">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0ea3c-144">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="0ea3c-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="0ea3c-145">Namespace</span></span><br/>                | <span data-ttu-id="0ea3c-146">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="0ea3c-146">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="0ea3c-147">MOF</span><span class="sxs-lookup"><span data-stu-id="0ea3c-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ea3c-148"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ea3c-148"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="0ea3c-149">DLL</span><span class="sxs-lookup"><span data-stu-id="0ea3c-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ea3c-150"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="0ea3c-150"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ea3c-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ea3c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ea3c-152">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="0ea3c-152">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

