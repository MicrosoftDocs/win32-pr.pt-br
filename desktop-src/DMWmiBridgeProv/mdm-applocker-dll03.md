---
title: Classe MDM_AppLocker_DLL03
description: A \_ classe DLL03 do MDM AppLocker \_ define as restrições de política para o processamento de arquivos dll.
ms.assetid: 956b2ec0-f8a8-41d1-a571-01e73c4cebf9
keywords:
- Classe MDM_AppLocker_DLL03
- Classe MDM_AppLocker_DLL03, descrita
topic_type:
- apiref
api_name:
- MDM_AppLocker_DLL03
- MDM_AppLocker_DLL03.InstanceID
- MDM_AppLocker_DLL03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c332a7d606b21ed9641c3c25f10a011cf7bea6e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769023"
---
# <a name="mdm_applocker_dll03-class"></a><span data-ttu-id="43575-105">\_ \_ Classe DLL03 do MDM AppLocker</span><span class="sxs-lookup"><span data-stu-id="43575-105">MDM\_AppLocker\_DLL03 class</span></span>

<span data-ttu-id="43575-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="43575-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="43575-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="43575-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="43575-108">A **classe \_ \_ DLL03 do MDM AppLocker** define as restrições de política para o processamento de arquivos dll.</span><span class="sxs-lookup"><span data-stu-id="43575-108">The **MDM\_AppLocker\_DLL03** class defines the policy restrictions for processing DLL files.</span></span>

<span data-ttu-id="43575-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="43575-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="43575-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43575-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_DLL03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
  string NonInteractiveProcessEnforcement;
};
```

## <a name="members"></a><span data-ttu-id="43575-111">Membros</span><span class="sxs-lookup"><span data-stu-id="43575-111">Members</span></span>

<span data-ttu-id="43575-112">A **classe \_ \_ DLL03 do MDM AppLocker** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="43575-112">The **MDM\_AppLocker\_DLL03** class has these types of members:</span></span>

-   [<span data-ttu-id="43575-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="43575-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="43575-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="43575-114">Properties</span></span>

<span data-ttu-id="43575-115">A **classe \_ \_ DLL03 do MDM AppLocker** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="43575-115">The **MDM\_AppLocker\_DLL03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="43575-116">**Imposiçãomode**</span><span class="sxs-lookup"><span data-stu-id="43575-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="43575-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="43575-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43575-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43575-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="43575-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="43575-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43575-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="43575-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43575-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43575-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43575-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="43575-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="43575-123">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="43575-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="43575-124">**NonInteractiveProcessEnforcement**</span><span class="sxs-lookup"><span data-stu-id="43575-124">**NonInteractiveProcessEnforcement**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="43575-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="43575-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43575-126">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43575-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="43575-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="43575-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43575-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="43575-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43575-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43575-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43575-130">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="43575-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="43575-131">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="43575-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="43575-132">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span><span class="sxs-lookup"><span data-stu-id="43575-132">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span></span>

</dd> <dt>

[<span data-ttu-id="43575-133">**Política**</span><span class="sxs-lookup"><span data-stu-id="43575-133">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="43575-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="43575-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43575-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43575-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="43575-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43575-136">Requirements</span></span>



| <span data-ttu-id="43575-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="43575-137">Requirement</span></span> | <span data-ttu-id="43575-138">Valor</span><span class="sxs-lookup"><span data-stu-id="43575-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43575-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43575-139">Minimum supported client</span></span><br/> | <span data-ttu-id="43575-140">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="43575-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="43575-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43575-141">Minimum supported server</span></span><br/> | <span data-ttu-id="43575-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="43575-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="43575-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="43575-143">Namespace</span></span><br/>                | <span data-ttu-id="43575-144">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="43575-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="43575-145">MOF</span><span class="sxs-lookup"><span data-stu-id="43575-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43575-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43575-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="43575-147">DLL</span><span class="sxs-lookup"><span data-stu-id="43575-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43575-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43575-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43575-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="43575-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43575-150">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="43575-150">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

