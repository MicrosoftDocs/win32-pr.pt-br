---
title: Classe MDM_Policy_Config01_EventLogService02
description: A \_ classe Config01 EventLogService02 de política de MDM \_ \_ configura o comportamento do log de eventos.
ms.assetid: 206934c4-6671-4f13-be79-22ff1fb7ce7e
keywords:
- Classe MDM_Policy_Config01_EventLogService02
- Classe MDM_Policy_Config01_EventLogService02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_EventLogService02
- MDM_Policy_Config01_EventLogService02.InstanceID
- MDM_Policy_Config01_EventLogService02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e39d3e78e686886e689ab2333b073108207446a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918252"
---
# <a name="mdm_policy_config01_eventlogservice02-class"></a><span data-ttu-id="9ad0f-105">\_Classe MDM \_ Config01 \_ EventLogService02</span><span class="sxs-lookup"><span data-stu-id="9ad0f-105">MDM\_Policy\_Config01\_EventLogService02 class</span></span>

<span data-ttu-id="9ad0f-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="9ad0f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9ad0f-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="9ad0f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9ad0f-108">A \_ classe Config01 EventLogService02 de política de MDM \_ \_ configura o comportamento do log de eventos.</span><span class="sxs-lookup"><span data-stu-id="9ad0f-108">The MDM\_Policy\_Config01\_EventLogService02 class configures the event log behavior.</span></span>

<span data-ttu-id="9ad0f-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9ad0f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ad0f-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ad0f-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_EventLogService02
{
  string InstanceID;
  string ParentID;
  string ControlEventLogBehavior;
  string SpecifyMaximumFileSizeApplicationLog;
  string SpecifyMaximumFileSizeSecurityLog;
  string SpecifyMaximumFileSizeSystemLog;
};
```

## <a name="members"></a><span data-ttu-id="9ad0f-111">Membros</span><span class="sxs-lookup"><span data-stu-id="9ad0f-111">Members</span></span>

<span data-ttu-id="9ad0f-112">A **classe \_ \_ Config01 \_ EventLogService02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9ad0f-112">The **MDM\_Policy\_Config01\_EventLogService02** class has these types of members:</span></span>

-   [<span data-ttu-id="9ad0f-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9ad0f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9ad0f-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9ad0f-114">Properties</span></span>

<span data-ttu-id="9ad0f-115">A **classe \_ \_ Config01 \_ EventLogService02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9ad0f-115">The **MDM\_Policy\_Config01\_EventLogService02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9ad0f-116">ControlEventLogBehavior</span><span class="sxs-lookup"><span data-stu-id="9ad0f-116">ControlEventLogBehavior</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-controleventlogbehavior)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad0f-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9ad0f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ad0f-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9ad0f-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9ad0f-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9ad0f-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad0f-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9ad0f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ad0f-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9ad0f-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ad0f-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9ad0f-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9ad0f-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9ad0f-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad0f-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9ad0f-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ad0f-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9ad0f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ad0f-126">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9ad0f-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ad0f-127">SpecifyMaximumFileSizeApplicationLog</span><span class="sxs-lookup"><span data-stu-id="9ad0f-127">SpecifyMaximumFileSizeApplicationLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizeapplicationlog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad0f-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9ad0f-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ad0f-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9ad0f-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ad0f-130">SpecifyMaximumFileSizeSecurityLog</span><span class="sxs-lookup"><span data-stu-id="9ad0f-130">SpecifyMaximumFileSizeSecurityLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizesecuritylog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad0f-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9ad0f-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ad0f-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9ad0f-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9ad0f-133">SpecifyMaximumFileSizeSystemLog</span><span class="sxs-lookup"><span data-stu-id="9ad0f-133">SpecifyMaximumFileSizeSystemLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizesystemlog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ad0f-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9ad0f-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ad0f-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9ad0f-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ad0f-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ad0f-136">Requirements</span></span>



| <span data-ttu-id="9ad0f-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ad0f-137">Requirement</span></span> | <span data-ttu-id="9ad0f-138">Valor</span><span class="sxs-lookup"><span data-stu-id="9ad0f-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ad0f-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ad0f-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9ad0f-140">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9ad0f-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9ad0f-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ad0f-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9ad0f-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9ad0f-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9ad0f-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="9ad0f-143">Namespace</span></span><br/>                | <span data-ttu-id="9ad0f-144">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="9ad0f-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="9ad0f-145">MOF</span><span class="sxs-lookup"><span data-stu-id="9ad0f-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ad0f-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ad0f-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ad0f-147">DLL</span><span class="sxs-lookup"><span data-stu-id="9ad0f-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ad0f-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ad0f-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

