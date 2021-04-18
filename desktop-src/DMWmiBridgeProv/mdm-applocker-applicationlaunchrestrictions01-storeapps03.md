---
title: Classe MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
description: A \_ classe MDM AppLocker \_ ApplicationLaunchRestrictions01 \_ StoreApps03 permite que você ESPECIFIQUE quais aplicativos exe são permitidos ou despermitidos para a proteção de dados empresariais.
ms.assetid: de5ceaea-589a-4ed7-8dd6-eb9477d68e0e
keywords:
- Classe MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
- Classe MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03, descrita
topic_type:
- apiref
api_name:
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03.InstanceID
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54c58610c10e672a6fbc1406b2d022b8ce211871
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769024"
---
# <a name="mdm_applocker_applicationlaunchrestrictions01_storeapps03-class"></a><span data-ttu-id="3e2dc-105">\_Classe StoreApps03 do MDM AppLocker \_ ApplicationLaunchRestrictions01 \_</span><span class="sxs-lookup"><span data-stu-id="3e2dc-105">MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03 class</span></span>

<span data-ttu-id="3e2dc-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="3e2dc-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3e2dc-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="3e2dc-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3e2dc-108">A classe **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ StoreApps03** permite que você especifique quais aplicativos exe são permitidos ou despermitidos para a proteção de dados empresariais.</span><span class="sxs-lookup"><span data-stu-id="3e2dc-108">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03** class allows you to specify which EXE applications are allowed or disallowed for Enterprise Data Protection.</span></span>

<span data-ttu-id="3e2dc-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3e2dc-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e2dc-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e2dc-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
};
```

## <a name="members"></a><span data-ttu-id="3e2dc-111">Membros</span><span class="sxs-lookup"><span data-stu-id="3e2dc-111">Members</span></span>

<span data-ttu-id="3e2dc-112">A classe **StoreApps03 do MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3e2dc-112">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03** class has these types of members:</span></span>

-   [<span data-ttu-id="3e2dc-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3e2dc-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3e2dc-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3e2dc-114">Properties</span></span>

<span data-ttu-id="3e2dc-115">A classe **StoreApps03 do MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3e2dc-115">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3e2dc-116">**Imposiçãomode**</span><span class="sxs-lookup"><span data-stu-id="3e2dc-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e2dc-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e2dc-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e2dc-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3e2dc-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3e2dc-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3e2dc-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e2dc-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e2dc-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e2dc-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e2dc-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e2dc-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3e2dc-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3e2dc-123">Define as restrições para a execução de aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="3e2dc-123">Defines restrictions for running apps from the Windows Store.</span></span>

</dd> <dt>

<span data-ttu-id="3e2dc-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3e2dc-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e2dc-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e2dc-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e2dc-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e2dc-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e2dc-127">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3e2dc-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3e2dc-128">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="3e2dc-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="3e2dc-129">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*GROUPING*"</span><span class="sxs-lookup"><span data-stu-id="3e2dc-129">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="3e2dc-130">**Política**</span><span class="sxs-lookup"><span data-stu-id="3e2dc-130">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e2dc-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e2dc-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e2dc-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3e2dc-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e2dc-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e2dc-133">Requirements</span></span>



| <span data-ttu-id="3e2dc-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e2dc-134">Requirement</span></span> | <span data-ttu-id="3e2dc-135">Valor</span><span class="sxs-lookup"><span data-stu-id="3e2dc-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e2dc-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e2dc-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3e2dc-137">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3e2dc-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e2dc-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e2dc-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3e2dc-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3e2dc-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3e2dc-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e2dc-140">Namespace</span></span><br/>                | <span data-ttu-id="3e2dc-141">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="3e2dc-141">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="3e2dc-142">MOF</span><span class="sxs-lookup"><span data-stu-id="3e2dc-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e2dc-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e2dc-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e2dc-144">DLL</span><span class="sxs-lookup"><span data-stu-id="3e2dc-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e2dc-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e2dc-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e2dc-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e2dc-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e2dc-147">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="3e2dc-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

