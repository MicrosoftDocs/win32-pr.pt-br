---
title: Classe MDM_Policy_Config01_DeviceGuard02
description: A política de MDM \_ \_ Config01 \_ DeviceGuard02 configura as políticas de proteção do dispositivo.
ms.assetid: b8edf906-2486-4d8d-9410-d216bacf1728
keywords:
- Classe MDM_Policy_Config01_DeviceGuard02
- Classe MDM_Policy_Config01_DeviceGuard02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DeviceGuard02
- MDM_Policy_Config01_DeviceGuard02.InstanceID
- MDM_Policy_Config01_DeviceGuard02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ebcc8f3d929708cdff3ada8fe440f49a1aeb1ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008915"
---
# <a name="mdm_policy_config01_deviceguard02-class"></a><span data-ttu-id="ac2e9-105">\_Classe MDM \_ Config01 \_ DeviceGuard02</span><span class="sxs-lookup"><span data-stu-id="ac2e9-105">MDM\_Policy\_Config01\_DeviceGuard02 class</span></span>

<span data-ttu-id="ac2e9-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="ac2e9-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ac2e9-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="ac2e9-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ac2e9-108">A política de MDM \_ \_ Config01 \_ DeviceGuard02 configura as políticas de proteção do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac2e9-108">The MDM\_Policy\_Config01\_DeviceGuard02 configures the Device Guard policies.</span></span>

<span data-ttu-id="ac2e9-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ac2e9-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac2e9-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac2e9-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DeviceGuard02
{
  string InstanceID;
  string ParentID;
  sint32 EnableVirtualizationBasedSecurity;
  sint32 LsaCfgFlags;
  sint32 RequirePlatformSecurityFeatures;
};
```

## <a name="members"></a><span data-ttu-id="ac2e9-111">Membros</span><span class="sxs-lookup"><span data-stu-id="ac2e9-111">Members</span></span>

<span data-ttu-id="ac2e9-112">A **classe \_ \_ Config01 \_ DeviceGuard02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ac2e9-112">The **MDM\_Policy\_Config01\_DeviceGuard02** class has these types of members:</span></span>

-   [<span data-ttu-id="ac2e9-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ac2e9-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ac2e9-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ac2e9-114">Properties</span></span>

<span data-ttu-id="ac2e9-115">A **classe \_ \_ Config01 \_ DeviceGuard02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ac2e9-115">The **MDM\_Policy\_Config01\_DeviceGuard02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ac2e9-116">EnableVirtualizationBasedSecurity</span><span class="sxs-lookup"><span data-stu-id="ac2e9-116">EnableVirtualizationBasedSecurity</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-enablevirtualizationbasedsecurity)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac2e9-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac2e9-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac2e9-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ac2e9-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac2e9-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ac2e9-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac2e9-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ac2e9-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac2e9-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac2e9-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac2e9-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ac2e9-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac2e9-123">LsaCfgFlags</span><span class="sxs-lookup"><span data-stu-id="ac2e9-123">LsaCfgFlags</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-lsacfgflags)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac2e9-124">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac2e9-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac2e9-125">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ac2e9-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac2e9-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ac2e9-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac2e9-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ac2e9-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac2e9-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac2e9-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac2e9-129">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ac2e9-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac2e9-130">RequirePlatformSecurityFeatures</span><span class="sxs-lookup"><span data-stu-id="ac2e9-130">RequirePlatformSecurityFeatures</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-requireplatformsecurityfeatures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac2e9-131">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac2e9-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac2e9-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ac2e9-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac2e9-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac2e9-133">Requirements</span></span>



| <span data-ttu-id="ac2e9-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac2e9-134">Requirement</span></span> | <span data-ttu-id="ac2e9-135">Valor</span><span class="sxs-lookup"><span data-stu-id="ac2e9-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac2e9-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac2e9-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ac2e9-137">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ac2e9-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ac2e9-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac2e9-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ac2e9-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ac2e9-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ac2e9-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac2e9-140">Namespace</span></span><br/>                | <span data-ttu-id="ac2e9-141">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="ac2e9-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ac2e9-142">MOF</span><span class="sxs-lookup"><span data-stu-id="ac2e9-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac2e9-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac2e9-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac2e9-144">DLL</span><span class="sxs-lookup"><span data-stu-id="ac2e9-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac2e9-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac2e9-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

