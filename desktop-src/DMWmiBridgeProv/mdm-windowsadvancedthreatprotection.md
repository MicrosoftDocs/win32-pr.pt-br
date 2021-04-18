---
title: Classe MDM_WindowsAdvancedThreatProtection
description: A \_ classe MDM WindowsAdvancedThreatProtection é usada para os pontos de extremidade integrados e transferir para o WDATP (proteção avançada contra ameaças) do Windows Defender.
ms.assetid: 7a95253e-6d13-4c1b-b78d-c56c6378f7c3
keywords:
- Classe MDM_WindowsAdvancedThreatProtection
- Classe MDM_WindowsAdvancedThreatProtection, descrita
topic_type:
- apiref
api_name:
- MDM_WindowsAdvancedThreatProtection
- MDM_WindowsAdvancedThreatProtection.InstanceID
- MDM_WindowsAdvancedThreatProtection.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c369406a3c8bcf982aeb18b4bbb53c1af4983e84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105752935"
---
# <a name="mdm_windowsadvancedthreatprotection-class"></a><span data-ttu-id="2ca92-105">\_Classe WindowsAdvancedThreatProtection do MDM</span><span class="sxs-lookup"><span data-stu-id="2ca92-105">MDM\_WindowsAdvancedThreatProtection class</span></span>

<span data-ttu-id="2ca92-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="2ca92-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2ca92-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="2ca92-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2ca92-108">A classe **MDM \_ WindowsAdvancedThreatProtection** é usada para os pontos de extremidade integrados e transferir para o WDATP (proteção avançada contra ameaças) do Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="2ca92-108">The **MDM\_WindowsAdvancedThreatProtection** class is used to onboard and offboard endpoints for Windows Defender Advanced Threat Protection (WDATP).</span></span>

<span data-ttu-id="2ca92-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2ca92-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ca92-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ca92-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection
{
  string InstanceID;
  string ParentID;
  string Onboarding;
  string Offboarding;
};
```

## <a name="members"></a><span data-ttu-id="2ca92-111">Membros</span><span class="sxs-lookup"><span data-stu-id="2ca92-111">Members</span></span>

<span data-ttu-id="2ca92-112">A classe **MDM \_ WindowsAdvancedThreatProtection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2ca92-112">The **MDM\_WindowsAdvancedThreatProtection** class has these types of members:</span></span>

-   [<span data-ttu-id="2ca92-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2ca92-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2ca92-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2ca92-114">Properties</span></span>

<span data-ttu-id="2ca92-115">A classe **MDM \_ WindowsAdvancedThreatProtection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2ca92-115">The **MDM\_WindowsAdvancedThreatProtection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2ca92-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2ca92-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ca92-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2ca92-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ca92-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2ca92-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ca92-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2ca92-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2ca92-120">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="2ca92-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="2ca92-121">Para essa classe, a cadeia de caracteres é "WindowsAdvancedThreatProtection".</span><span class="sxs-lookup"><span data-stu-id="2ca92-121">For this class, the string is "WindowsAdvancedThreatProtection".</span></span>

</dd> <dt>

[<span data-ttu-id="2ca92-122">Desintegração</span><span class="sxs-lookup"><span data-stu-id="2ca92-122">Offboarding</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#offboarding)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ca92-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2ca92-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ca92-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2ca92-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2ca92-125">Integração</span><span class="sxs-lookup"><span data-stu-id="2ca92-125">Onboarding</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#onboarding)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ca92-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2ca92-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ca92-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2ca92-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2ca92-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2ca92-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ca92-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2ca92-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ca92-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2ca92-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ca92-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2ca92-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2ca92-132">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="2ca92-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="2ca92-133">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="2ca92-133">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2ca92-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ca92-134">Requirements</span></span>



| <span data-ttu-id="2ca92-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ca92-135">Requirement</span></span> | <span data-ttu-id="2ca92-136">Valor</span><span class="sxs-lookup"><span data-stu-id="2ca92-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca92-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ca92-137">Minimum supported client</span></span><br/> | <span data-ttu-id="2ca92-138">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2ca92-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2ca92-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ca92-139">Minimum supported server</span></span><br/> | <span data-ttu-id="2ca92-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2ca92-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="2ca92-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="2ca92-141">Namespace</span></span><br/>                | <span data-ttu-id="2ca92-142">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="2ca92-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="2ca92-143">MOF</span><span class="sxs-lookup"><span data-stu-id="2ca92-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ca92-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2ca92-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="2ca92-145">DLL</span><span class="sxs-lookup"><span data-stu-id="2ca92-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ca92-146"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="2ca92-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ca92-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ca92-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ca92-148">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="2ca92-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

