---
title: Classe MDM_Policy_Config01_Cellular02
description: A \_ classe Config01 Cellular02 de política de MDM \_ \_ configura as políticas de celular.
ms.assetid: e5926a21-a375-4d1c-8b37-7fe7f7532c50
keywords:
- Classe MDM_Policy_Config01_Cellular02
- Classe MDM_Policy_Config01_Cellular02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Cellular02
- MDM_Policy_Config01_Cellular02.InstanceID
- MDM_Policy_Config01_Cellular02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b1b6d9163723299b144368d9d2b73a12ccc7a91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085381"
---
# <a name="mdm_policy_config01_cellular02-class"></a><span data-ttu-id="79417-105">\_Classe MDM \_ Config01 \_ Cellular02</span><span class="sxs-lookup"><span data-stu-id="79417-105">MDM\_Policy\_Config01\_Cellular02 class</span></span>

<span data-ttu-id="79417-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="79417-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="79417-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="79417-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="79417-108">A \_ classe Config01 Cellular02 de política de MDM \_ \_ configura as políticas de celular.</span><span class="sxs-lookup"><span data-stu-id="79417-108">The MDM\_Policy\_Config01\_Cellular02 class configures the cellular policies.</span></span>

<span data-ttu-id="79417-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="79417-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="79417-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79417-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Cellular02
{
  string InstanceID;
  string ParentID;
  string LetAppsAccessCellularData_UserInControlOfTheseApps;
  string LetAppsAccessCellularData_ForceDenyTheseApps;
  string LetAppsAccessCellularData_ForceAllowTheseApps;
  sint32 LetAppsAccessCellularData;
  string ShowAppCellularAccessUI;
};
```

## <a name="members"></a><span data-ttu-id="79417-111">Membros</span><span class="sxs-lookup"><span data-stu-id="79417-111">Members</span></span>

<span data-ttu-id="79417-112">A **classe \_ \_ Config01 \_ Cellular02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="79417-112">The **MDM\_Policy\_Config01\_Cellular02** class has these types of members:</span></span>

-   [<span data-ttu-id="79417-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="79417-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="79417-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="79417-114">Properties</span></span>

<span data-ttu-id="79417-115">A **classe \_ \_ Config01 \_ Cellular02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="79417-115">The **MDM\_Policy\_Config01\_Cellular02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="79417-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="79417-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79417-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79417-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79417-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79417-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79417-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="79417-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="79417-120">LetAppsAccessCellularData</span><span class="sxs-lookup"><span data-stu-id="79417-120">LetAppsAccessCellularData</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="79417-121">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="79417-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="79417-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="79417-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="79417-123">LetAppsAccessCellularData \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="79417-123">LetAppsAccessCellularData\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="79417-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79417-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79417-125">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="79417-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="79417-126">LetAppsAccessCellularData \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="79417-126">LetAppsAccessCellularData\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="79417-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79417-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79417-128">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="79417-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="79417-129">LetAppsAccessCellularData \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="79417-129">LetAppsAccessCellularData\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="79417-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79417-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79417-131">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="79417-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="79417-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="79417-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79417-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79417-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79417-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79417-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79417-135">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="79417-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="79417-136">ShowAppCellularAccessUI</span><span class="sxs-lookup"><span data-stu-id="79417-136">ShowAppCellularAccessUI</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-showappcellularaccessui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="79417-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79417-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79417-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="79417-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="79417-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79417-139">Requirements</span></span>



| <span data-ttu-id="79417-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="79417-140">Requirement</span></span> | <span data-ttu-id="79417-141">Valor</span><span class="sxs-lookup"><span data-stu-id="79417-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79417-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79417-142">Minimum supported client</span></span><br/> | <span data-ttu-id="79417-143">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="79417-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="79417-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79417-144">Minimum supported server</span></span><br/> | <span data-ttu-id="79417-145">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="79417-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="79417-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="79417-146">Namespace</span></span><br/>                | <span data-ttu-id="79417-147">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="79417-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="79417-148">MOF</span><span class="sxs-lookup"><span data-stu-id="79417-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79417-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79417-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="79417-150">DLL</span><span class="sxs-lookup"><span data-stu-id="79417-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79417-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79417-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

