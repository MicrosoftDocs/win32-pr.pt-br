---
title: Classe MDM_Policy_Result01_Cellular02
description: a \_ classe MDM Policy \_ Result01 \_ Cellular02 representa as políticas de celular.
ms.assetid: df2b2461-5e4e-4b28-87f1-5ca348409192
keywords:
- Classe MDM_Policy_Result01_Cellular02
- Classe MDM_Policy_Result01_Cellular02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Cellular02
- MDM_Policy_Result01_Cellular02.InstanceID
- MDM_Policy_Result01_Cellular02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f2a8b9178ecd4d69b0c313eb7fdcb826e944317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085284"
---
# <a name="mdm_policy_result01_cellular02-class"></a><span data-ttu-id="7cb28-105">\_Classe MDM \_ Result01 \_ Cellular02</span><span class="sxs-lookup"><span data-stu-id="7cb28-105">MDM\_Policy\_Result01\_Cellular02 class</span></span>

<span data-ttu-id="7cb28-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="7cb28-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7cb28-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="7cb28-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7cb28-108">a \_ classe MDM Policy \_ Result01 \_ Cellular02 representa as políticas de celular.</span><span class="sxs-lookup"><span data-stu-id="7cb28-108">the MDM\_Policy\_Result01\_Cellular02 class represents the cellular policies.</span></span>

<span data-ttu-id="7cb28-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="7cb28-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cb28-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7cb28-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Cellular02
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

## <a name="members"></a><span data-ttu-id="7cb28-111">Membros</span><span class="sxs-lookup"><span data-stu-id="7cb28-111">Members</span></span>

<span data-ttu-id="7cb28-112">A **classe \_ \_ Result01 \_ Cellular02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7cb28-112">The **MDM\_Policy\_Result01\_Cellular02** class has these types of members:</span></span>

-   [<span data-ttu-id="7cb28-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7cb28-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7cb28-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7cb28-114">Properties</span></span>

<span data-ttu-id="7cb28-115">A **classe \_ \_ Result01 \_ Cellular02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7cb28-115">The **MDM\_Policy\_Result01\_Cellular02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7cb28-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7cb28-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7cb28-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7cb28-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7cb28-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7cb28-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7cb28-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7cb28-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7cb28-120">LetAppsAccessCellularData</span><span class="sxs-lookup"><span data-stu-id="7cb28-120">LetAppsAccessCellularData</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7cb28-121">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7cb28-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7cb28-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7cb28-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7cb28-123">LetAppsAccessCellularData \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="7cb28-123">LetAppsAccessCellularData\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7cb28-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7cb28-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7cb28-125">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7cb28-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7cb28-126">LetAppsAccessCellularData \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="7cb28-126">LetAppsAccessCellularData\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7cb28-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7cb28-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7cb28-128">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7cb28-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7cb28-129">LetAppsAccessCellularData \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="7cb28-129">LetAppsAccessCellularData\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7cb28-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7cb28-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7cb28-131">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7cb28-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7cb28-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7cb28-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7cb28-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7cb28-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7cb28-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7cb28-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7cb28-135">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7cb28-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7cb28-136">ShowAppCellularAccessUI</span><span class="sxs-lookup"><span data-stu-id="7cb28-136">ShowAppCellularAccessUI</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-showappcellularaccessui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7cb28-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7cb28-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7cb28-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7cb28-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7cb28-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cb28-139">Requirements</span></span>



| <span data-ttu-id="7cb28-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cb28-140">Requirement</span></span> | <span data-ttu-id="7cb28-141">Valor</span><span class="sxs-lookup"><span data-stu-id="7cb28-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cb28-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cb28-142">Minimum supported client</span></span><br/> | <span data-ttu-id="7cb28-143">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7cb28-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7cb28-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cb28-144">Minimum supported server</span></span><br/> | <span data-ttu-id="7cb28-145">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7cb28-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7cb28-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="7cb28-146">Namespace</span></span><br/>                | <span data-ttu-id="7cb28-147">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="7cb28-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7cb28-148">MOF</span><span class="sxs-lookup"><span data-stu-id="7cb28-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7cb28-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7cb28-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7cb28-150">DLL</span><span class="sxs-lookup"><span data-stu-id="7cb28-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cb28-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cb28-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

