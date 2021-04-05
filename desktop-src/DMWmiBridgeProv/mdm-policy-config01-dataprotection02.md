---
title: Classe MDM_Policy_Config01_DataProtection02
description: A \_ classe MDM Policy \_ Config01 \_ DataProtection02 representa as políticas de proteção de dados disponíveis.
ms.assetid: 54750bae-ee5d-4db9-896f-28d9550c4d5d
keywords:
- Classe MDM_Policy_Config01_DataProtection02
- Classe MDM_Policy_Config01_DataProtection02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DataProtection02
- MDM_Policy_Config01_DataProtection02.InstanceID
- MDM_Policy_Config01_DataProtection02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 692dfd675c07ddc7eebbfcd75e09cb521126c746
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919016"
---
# <a name="mdm_policy_config01_dataprotection02-class"></a><span data-ttu-id="697ea-105">\_Classe MDM \_ Config01 \_ DataProtection02</span><span class="sxs-lookup"><span data-stu-id="697ea-105">MDM\_Policy\_Config01\_DataProtection02 class</span></span>

<span data-ttu-id="697ea-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="697ea-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="697ea-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="697ea-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="697ea-108">A classe **MDM \_ Policy \_ Config01 \_ DataProtection02** representa as políticas de proteção de dados disponíveis.</span><span class="sxs-lookup"><span data-stu-id="697ea-108">The **MDM\_Policy\_Config01\_DataProtection02** class represents the data protection policies available.</span></span>

<span data-ttu-id="697ea-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="697ea-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="697ea-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="697ea-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DataProtection02
{
  string InstanceID;
  string ParentID;
  sint32 AllowDirectMemoryAccess;
  string LegacySelectiveWipeID;
};
```

## <a name="members"></a><span data-ttu-id="697ea-111">Membros</span><span class="sxs-lookup"><span data-stu-id="697ea-111">Members</span></span>

<span data-ttu-id="697ea-112">A **classe \_ \_ Config01 \_ DataProtection02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="697ea-112">The **MDM\_Policy\_Config01\_DataProtection02** class has these types of members:</span></span>

-   [<span data-ttu-id="697ea-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="697ea-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="697ea-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="697ea-114">Properties</span></span>

<span data-ttu-id="697ea-115">A **classe \_ \_ Config01 \_ DataProtection02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="697ea-115">The **MDM\_Policy\_Config01\_DataProtection02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="697ea-116">AllowDirectMemoryAccess</span><span class="sxs-lookup"><span data-stu-id="697ea-116">AllowDirectMemoryAccess</span></span>](/windows/client-management/mdm/policy-csp-dataprotection#dataprotection-allowdirectmemoryaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="697ea-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="697ea-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="697ea-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="697ea-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="697ea-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="697ea-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="697ea-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="697ea-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="697ea-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="697ea-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="697ea-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="697ea-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="697ea-123">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="697ea-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="697ea-124">Para essa classe, a cadeia de caracteres é "dataprotection".</span><span class="sxs-lookup"><span data-stu-id="697ea-124">For this class, the string is "DataProtection".</span></span>

</dd> <dt>

[<span data-ttu-id="697ea-125">LegacySelectiveWipeID</span><span class="sxs-lookup"><span data-stu-id="697ea-125">LegacySelectiveWipeID</span></span>](/windows/client-management/mdm/policy-csp-dataprotection#dataprotection-legacyselectivewipeid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="697ea-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="697ea-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="697ea-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="697ea-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="697ea-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="697ea-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="697ea-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="697ea-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="697ea-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="697ea-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="697ea-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="697ea-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="697ea-132">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="697ea-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="697ea-133">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="697ea-133">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="697ea-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="697ea-134">Requirements</span></span>



| <span data-ttu-id="697ea-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="697ea-135">Requirement</span></span> | <span data-ttu-id="697ea-136">Valor</span><span class="sxs-lookup"><span data-stu-id="697ea-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="697ea-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="697ea-137">Minimum supported client</span></span><br/> | <span data-ttu-id="697ea-138">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="697ea-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="697ea-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="697ea-139">Minimum supported server</span></span><br/> | <span data-ttu-id="697ea-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="697ea-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="697ea-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="697ea-141">Namespace</span></span><br/>                | <span data-ttu-id="697ea-142">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="697ea-142">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="697ea-143">MOF</span><span class="sxs-lookup"><span data-stu-id="697ea-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="697ea-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="697ea-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="697ea-145">DLL</span><span class="sxs-lookup"><span data-stu-id="697ea-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="697ea-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="697ea-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="697ea-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="697ea-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="697ea-148">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="697ea-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

