---
title: Classe MDM_Policy_Result01_DeviceGuard02
description: A \_ classe Result01 DeviceGuard02 de política de MDM \_ \_ configura as políticas de proteção do dispositivo.
ms.assetid: ba21d324-85dc-4cb5-8123-196413e457eb
keywords:
- Classe MDM_Policy_Result01_DeviceGuard02
- Classe MDM_Policy_Result01_DeviceGuard02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DeviceGuard02
- MDM_Policy_Result01_DeviceGuard02.InstanceID
- MDM_Policy_Result01_DeviceGuard02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e206a732628e442a391cb8b29f7712f5a5ec8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009104"
---
# <a name="mdm_policy_result01_deviceguard02-class"></a><span data-ttu-id="721ec-105">\_Classe MDM \_ Result01 \_ DeviceGuard02</span><span class="sxs-lookup"><span data-stu-id="721ec-105">MDM\_Policy\_Result01\_DeviceGuard02 class</span></span>

<span data-ttu-id="721ec-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="721ec-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="721ec-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="721ec-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="721ec-108">A \_ classe Result01 DeviceGuard02 de política de MDM \_ \_ configura as políticas de proteção do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="721ec-108">The MDM\_Policy\_Result01\_DeviceGuard02 class configures the Device Guard policies.</span></span>

<span data-ttu-id="721ec-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="721ec-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="721ec-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="721ec-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DeviceGuard02
{
  string InstanceID;
  string ParentID;
  sint32 EnableVirtualizationBasedSecurity;
  sint32 LsaCfgFlags;
  sint32 RequirePlatformSecurityFeatures;
};
```

## <a name="members"></a><span data-ttu-id="721ec-111">Membros</span><span class="sxs-lookup"><span data-stu-id="721ec-111">Members</span></span>

<span data-ttu-id="721ec-112">A **classe \_ \_ Result01 \_ DeviceGuard02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="721ec-112">The **MDM\_Policy\_Result01\_DeviceGuard02** class has these types of members:</span></span>

-   [<span data-ttu-id="721ec-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="721ec-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="721ec-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="721ec-114">Properties</span></span>

<span data-ttu-id="721ec-115">A **classe \_ \_ Result01 \_ DeviceGuard02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="721ec-115">The **MDM\_Policy\_Result01\_DeviceGuard02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="721ec-116">EnableVirtualizationBasedSecurity</span><span class="sxs-lookup"><span data-stu-id="721ec-116">EnableVirtualizationBasedSecurity</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-enablevirtualizationbasedsecurity)
</dt> <dd> <dl> <dt>

<span data-ttu-id="721ec-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="721ec-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="721ec-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="721ec-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="721ec-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="721ec-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="721ec-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="721ec-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="721ec-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="721ec-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="721ec-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="721ec-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="721ec-123">LsaCfgFlags</span><span class="sxs-lookup"><span data-stu-id="721ec-123">LsaCfgFlags</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-lsacfgflags)
</dt> <dd> <dl> <dt>

<span data-ttu-id="721ec-124">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="721ec-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="721ec-125">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="721ec-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="721ec-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="721ec-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="721ec-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="721ec-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="721ec-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="721ec-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="721ec-129">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="721ec-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="721ec-130">RequirePlatformSecurityFeatures</span><span class="sxs-lookup"><span data-stu-id="721ec-130">RequirePlatformSecurityFeatures</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-requireplatformsecurityfeatures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="721ec-131">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="721ec-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="721ec-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="721ec-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="721ec-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="721ec-133">Requirements</span></span>



| <span data-ttu-id="721ec-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="721ec-134">Requirement</span></span> | <span data-ttu-id="721ec-135">Valor</span><span class="sxs-lookup"><span data-stu-id="721ec-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="721ec-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="721ec-136">Minimum supported client</span></span><br/> | <span data-ttu-id="721ec-137">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="721ec-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="721ec-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="721ec-138">Minimum supported server</span></span><br/> | <span data-ttu-id="721ec-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="721ec-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="721ec-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="721ec-140">Namespace</span></span><br/>                | <span data-ttu-id="721ec-141">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="721ec-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="721ec-142">MOF</span><span class="sxs-lookup"><span data-stu-id="721ec-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="721ec-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="721ec-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="721ec-144">DLL</span><span class="sxs-lookup"><span data-stu-id="721ec-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="721ec-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="721ec-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

