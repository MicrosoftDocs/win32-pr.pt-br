---
title: Classe MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
description: A \_ classe MDM AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03 permite que você ESPECIFIQUE quais aplicativos exe podem ser iniciados.
ms.assetid: 27f10b5c-bc3b-4344-afcf-5718ea13e909
keywords:
- Classe MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
- Classe MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03, descrita
topic_type:
- apiref
api_name:
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03.InstanceID
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58aeb86edc21fec974c099fd8d25bd2e3fb244ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824332"
---
# <a name="mdm_applocker_applicationlaunchrestrictions01_exe03-class"></a><span data-ttu-id="3ffe9-105">\_Classe EXE03 do MDM AppLocker \_ ApplicationLaunchRestrictions01 \_</span><span class="sxs-lookup"><span data-stu-id="3ffe9-105">MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03 class</span></span>

<span data-ttu-id="3ffe9-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="3ffe9-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3ffe9-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="3ffe9-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3ffe9-108">A classe **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03** permite que você especifique quais aplicativos exe podem ser iniciados.</span><span class="sxs-lookup"><span data-stu-id="3ffe9-108">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03** class allows you to specify which EXE applications are allowed to launch.</span></span>

<span data-ttu-id="3ffe9-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3ffe9-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ffe9-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ffe9-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
  string NonInteractiveProcessEnforcement;
};
```

## <a name="members"></a><span data-ttu-id="3ffe9-111">Membros</span><span class="sxs-lookup"><span data-stu-id="3ffe9-111">Members</span></span>

<span data-ttu-id="3ffe9-112">A classe **EXE03 do MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3ffe9-112">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03** class has these types of members:</span></span>

-   [<span data-ttu-id="3ffe9-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3ffe9-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3ffe9-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3ffe9-114">Properties</span></span>

<span data-ttu-id="3ffe9-115">A classe **EXE03 do MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3ffe9-115">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3ffe9-116">**Imposiçãomode**</span><span class="sxs-lookup"><span data-stu-id="3ffe9-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffe9-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3ffe9-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ffe9-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3ffe9-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3ffe9-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3ffe9-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffe9-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3ffe9-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ffe9-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3ffe9-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffe9-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3ffe9-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3ffe9-123">Define as restrições para iniciar aplicativos executáveis.</span><span class="sxs-lookup"><span data-stu-id="3ffe9-123">Defines restrictions for launching executable applications.</span></span>

</dd> <dt>

[<span data-ttu-id="3ffe9-124">**NonInteractiveProcessEnforcement**</span><span class="sxs-lookup"><span data-stu-id="3ffe9-124">**NonInteractiveProcessEnforcement**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffe9-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3ffe9-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ffe9-126">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3ffe9-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3ffe9-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3ffe9-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffe9-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3ffe9-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ffe9-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3ffe9-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffe9-130">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3ffe9-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3ffe9-131">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="3ffe9-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="3ffe9-132">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*GROUPING*"</span><span class="sxs-lookup"><span data-stu-id="3ffe9-132">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="3ffe9-133">**Política**</span><span class="sxs-lookup"><span data-stu-id="3ffe9-133">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffe9-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3ffe9-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ffe9-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3ffe9-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ffe9-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ffe9-136">Requirements</span></span>



| <span data-ttu-id="3ffe9-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ffe9-137">Requirement</span></span> | <span data-ttu-id="3ffe9-138">Valor</span><span class="sxs-lookup"><span data-stu-id="3ffe9-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ffe9-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ffe9-139">Minimum supported client</span></span><br/> | <span data-ttu-id="3ffe9-140">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3ffe9-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3ffe9-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ffe9-141">Minimum supported server</span></span><br/> | <span data-ttu-id="3ffe9-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3ffe9-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3ffe9-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="3ffe9-143">Namespace</span></span><br/>                | <span data-ttu-id="3ffe9-144">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="3ffe9-144">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="3ffe9-145">MOF</span><span class="sxs-lookup"><span data-stu-id="3ffe9-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ffe9-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ffe9-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ffe9-147">DLL</span><span class="sxs-lookup"><span data-stu-id="3ffe9-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ffe9-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ffe9-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ffe9-149">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3ffe9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ffe9-150">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="3ffe9-150">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

