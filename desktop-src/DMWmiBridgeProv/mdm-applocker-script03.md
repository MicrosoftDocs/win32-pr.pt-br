---
title: Classe MDM_AppLocker_Script03
description: A \_ classe Script03 do MDM AppLocker \_ define as restrições de política para o processamento de arquivos dll.
ms.assetid: 61fada02-7245-4825-945c-b41e9eff8e74
keywords:
- Classe MDM_AppLocker_Script03
- Classe MDM_AppLocker_Script03, descrita
topic_type:
- apiref
api_name:
- MDM_AppLocker_Script03
- MDM_AppLocker_Script03.InstanceID
- MDM_AppLocker_Script03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402efedb1e15a0ea0df3dea654328de4ba0ddd86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009738"
---
# <a name="mdm_applocker_script03-class"></a><span data-ttu-id="e6bb2-105">\_ \_ Classe SCRIPT03 do MDM AppLocker</span><span class="sxs-lookup"><span data-stu-id="e6bb2-105">MDM\_AppLocker\_Script03 class</span></span>

<span data-ttu-id="e6bb2-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="e6bb2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e6bb2-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="e6bb2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e6bb2-108">A **classe \_ \_ Script03 do MDM AppLocker** define as restrições de política para o processamento de arquivos dll.</span><span class="sxs-lookup"><span data-stu-id="e6bb2-108">The **MDM\_AppLocker\_Script03** class defines the policy restrictions for processing DLL files.</span></span>

<span data-ttu-id="e6bb2-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e6bb2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6bb2-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6bb2-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_Script03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
};
```

## <a name="members"></a><span data-ttu-id="e6bb2-111">Membros</span><span class="sxs-lookup"><span data-stu-id="e6bb2-111">Members</span></span>

<span data-ttu-id="e6bb2-112">A **classe \_ \_ Script03 do MDM AppLocker** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e6bb2-112">The **MDM\_AppLocker\_Script03** class has these types of members:</span></span>

-   [<span data-ttu-id="e6bb2-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e6bb2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e6bb2-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e6bb2-114">Properties</span></span>

<span data-ttu-id="e6bb2-115">A **classe \_ \_ Script03 do MDM AppLocker** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e6bb2-115">The **MDM\_AppLocker\_Script03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e6bb2-116">**Imposiçãomode**</span><span class="sxs-lookup"><span data-stu-id="e6bb2-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6bb2-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6bb2-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6bb2-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e6bb2-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e6bb2-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e6bb2-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6bb2-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6bb2-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6bb2-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6bb2-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6bb2-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e6bb2-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e6bb2-123">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="e6bb2-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="e6bb2-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e6bb2-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6bb2-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6bb2-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6bb2-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6bb2-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6bb2-127">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e6bb2-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e6bb2-128">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="e6bb2-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="e6bb2-129">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span><span class="sxs-lookup"><span data-stu-id="e6bb2-129">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span></span>

</dd> <dt>

[<span data-ttu-id="e6bb2-130">**Política**</span><span class="sxs-lookup"><span data-stu-id="e6bb2-130">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6bb2-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6bb2-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6bb2-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e6bb2-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e6bb2-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6bb2-133">Requirements</span></span>



| <span data-ttu-id="e6bb2-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6bb2-134">Requirement</span></span> | <span data-ttu-id="e6bb2-135">Valor</span><span class="sxs-lookup"><span data-stu-id="e6bb2-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6bb2-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6bb2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e6bb2-137">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e6bb2-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e6bb2-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6bb2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e6bb2-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e6bb2-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e6bb2-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="e6bb2-140">Namespace</span></span><br/>                | <span data-ttu-id="e6bb2-141">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="e6bb2-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e6bb2-142">MOF</span><span class="sxs-lookup"><span data-stu-id="e6bb2-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6bb2-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6bb2-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6bb2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e6bb2-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6bb2-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6bb2-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6bb2-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6bb2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6bb2-147">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="e6bb2-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

