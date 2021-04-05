---
title: Classe MDM_WindowsAdvancedThreatProtection_DeviceTagging01
description: A \_ classe MDM WindowsAdvancedThreatProtection \_ DeviceTagging01 é usada para carregar, determinar o status de integridade e a configuração e os pontos de extremidade transferir para a proteção avançada contra ameaças do Windows Defender.
ms.assetid: b56d5d46-e994-404a-865a-c59bb948f2b3
keywords:
- Classe MDM_WindowsAdvancedThreatProtection_DeviceTagging01
- Classe MDM_WindowsAdvancedThreatProtection_DeviceTagging01, descrita
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.InstanceID
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.ParentID
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.IdMethod
api_type:
- DllExport
api_location:
- DMWmiBridgeProv.dll
ms.openlocfilehash: 12cf3863ba67f422b42572a6934807d86abbc0e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085977"
---
# <a name="mdm_windowsadvancedthreatprotection_devicetagging01-class"></a><span data-ttu-id="4c238-105">\_ \_ Classe DEVICETAGGING01 do MDM WindowsAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="4c238-105">MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01 class</span></span>

<span data-ttu-id="4c238-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="4c238-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4c238-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="4c238-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4c238-108">A \_ classe MDM WindowsAdvancedThreatProtection \_ DeviceTagging01 é usada para carregar, determinar o status de integridade e a configuração e os pontos de extremidade transferir para a proteção avançada contra ameaças do Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="4c238-108">The MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01 class is used to onboard, determine configuration and health status, and offboard endpoints for Windows Defender Advanced Threat Protection.</span></span>

<span data-ttu-id="4c238-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="4c238-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c238-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c238-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_DeviceTagging01
{
  string InstanceID;
  string ParentID;
  string Group;
  sint32 Criticality;
  sint32 IdMethod;
};
```

## <a name="members"></a><span data-ttu-id="4c238-111">Membros</span><span class="sxs-lookup"><span data-stu-id="4c238-111">Members</span></span>

<span data-ttu-id="4c238-112">A **classe \_ \_ DeviceTagging01 de MDM WindowsAdvancedThreatProtection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4c238-112">The **MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01** class has these types of members:</span></span>

-   [<span data-ttu-id="4c238-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4c238-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4c238-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4c238-114">Properties</span></span>

<span data-ttu-id="4c238-115">A **classe \_ \_ DeviceTagging01 do MDM WindowsAdvancedThreatProtection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4c238-115">The **MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="4c238-116">Criticalidade</span><span class="sxs-lookup"><span data-stu-id="4c238-116">Criticality</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#criticality)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c238-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4c238-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c238-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4c238-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4c238-119">Grupo</span><span class="sxs-lookup"><span data-stu-id="4c238-119">Group</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#group)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c238-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4c238-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c238-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4c238-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4c238-122">**IdMethod**</span><span class="sxs-lookup"><span data-stu-id="4c238-122">**IdMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c238-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4c238-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c238-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4c238-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4c238-125">TBD</span><span class="sxs-lookup"><span data-stu-id="4c238-125">TBD</span></span>

</dd> <dt>

<span data-ttu-id="4c238-126">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4c238-126">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c238-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4c238-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c238-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c238-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c238-129">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4c238-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4c238-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="4c238-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c238-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4c238-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c238-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c238-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c238-133">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4c238-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4c238-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c238-134">Requirements</span></span>



| <span data-ttu-id="4c238-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c238-135">Requirement</span></span> | <span data-ttu-id="4c238-136">Valor</span><span class="sxs-lookup"><span data-stu-id="4c238-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c238-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c238-137">Minimum supported client</span></span><br/> | <span data-ttu-id="4c238-138">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4c238-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4c238-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c238-139">Minimum supported server</span></span><br/> | <span data-ttu-id="4c238-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4c238-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="4c238-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="4c238-141">Namespace</span></span><br/>                | <span data-ttu-id="4c238-142">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="4c238-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="4c238-143">MOF</span><span class="sxs-lookup"><span data-stu-id="4c238-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c238-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c238-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="4c238-145">DLL</span><span class="sxs-lookup"><span data-stu-id="4c238-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c238-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c238-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

