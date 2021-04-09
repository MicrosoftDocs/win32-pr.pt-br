---
title: Classe MDM_Policy_User_Config01_ApplicationManagement02
description: A \_ classe Config01 ApplicationManagement02 do usuário da política de MDM \_ \_ \_ representa as políticas de início disponíveis que são definidas por usuário.
ms.assetid: 3dd20364-6723-4ed6-87c0-729789ddd948
keywords:
- Classe MDM_Policy_User_Config01_ApplicationManagement02
- Classe MDM_Policy_User_Config01_ApplicationManagement02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_ApplicationManagement02
- MDM_Policy_User_Config01_ApplicationManagement02.InstanceID
- MDM_Policy_User_Config01_ApplicationManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88226122eefb3335ef1b19680268ea5acf1d5388
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085206"
---
# <a name="mdm_policy_user_config01_applicationmanagement02-class"></a><span data-ttu-id="2b2ed-105">Config01 de usuário de política de MDM- \_ \_ \_ \_ classe ApplicationManagement02</span><span class="sxs-lookup"><span data-stu-id="2b2ed-105">MDM\_Policy\_User\_Config01\_ApplicationManagement02 class</span></span>

<span data-ttu-id="2b2ed-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="2b2ed-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2b2ed-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="2b2ed-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2b2ed-108">A **classe \_ \_ \_ Config01 \_ ApplicationManagement02 do usuário da política de MDM** representa as políticas de início disponíveis que são definidas por usuário.</span><span class="sxs-lookup"><span data-stu-id="2b2ed-108">The **MDM\_Policy\_User\_Config01\_ApplicationManagement02** class represents the start policies available that are set on a per-user basis.</span></span>

<span data-ttu-id="2b2ed-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2b2ed-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b2ed-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b2ed-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_ApplicationManagement02
{
  string InstanceID;
  string ParentID;
  sint32 RequirePrivateStoreOnly;
};
```

## <a name="members"></a><span data-ttu-id="2b2ed-111">Membros</span><span class="sxs-lookup"><span data-stu-id="2b2ed-111">Members</span></span>

<span data-ttu-id="2b2ed-112">A **classe \_ \_ \_ Config01 \_ ApplicationManagement02 do usuário da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2b2ed-112">The **MDM\_Policy\_User\_Config01\_ApplicationManagement02** class has these types of members:</span></span>

-   [<span data-ttu-id="2b2ed-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2b2ed-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2b2ed-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2b2ed-114">Properties</span></span>

<span data-ttu-id="2b2ed-115">A **classe \_ \_ \_ Config01 \_ ApplicationManagement02 do usuário da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2b2ed-115">The **MDM\_Policy\_User\_Config01\_ApplicationManagement02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2b2ed-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2b2ed-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b2ed-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2b2ed-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b2ed-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2b2ed-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b2ed-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2b2ed-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2b2ed-120">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="2b2ed-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="2b2ed-121">Para essa classe, a cadeia de caracteres é "ApplicationManagement"</span><span class="sxs-lookup"><span data-stu-id="2b2ed-121">For this class, the string is "ApplicationManagement"</span></span>

</dd> <dt>

<span data-ttu-id="2b2ed-122">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2b2ed-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b2ed-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2b2ed-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b2ed-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2b2ed-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b2ed-125">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2b2ed-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2b2ed-126">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="2b2ed-126">Describes the full path to the parent node.</span></span> <span data-ttu-id="2b2ed-127">Para essa classe, a cadeia de caracteres é "./User/Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="2b2ed-127">For this class, the string is "./User/Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="2b2ed-128">RequirePrivateStoreOnly</span><span class="sxs-lookup"><span data-stu-id="2b2ed-128">RequirePrivateStoreOnly</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-requireprivatestoreonly)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b2ed-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2b2ed-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2b2ed-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2b2ed-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2b2ed-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b2ed-131">Requirements</span></span>



| <span data-ttu-id="2b2ed-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b2ed-132">Requirement</span></span> | <span data-ttu-id="2b2ed-133">Valor</span><span class="sxs-lookup"><span data-stu-id="2b2ed-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b2ed-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b2ed-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2b2ed-135">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2b2ed-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2b2ed-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b2ed-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2b2ed-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2b2ed-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2b2ed-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="2b2ed-138">Namespace</span></span><br/>                | <span data-ttu-id="2b2ed-139">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="2b2ed-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2b2ed-140">MOF</span><span class="sxs-lookup"><span data-stu-id="2b2ed-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b2ed-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b2ed-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b2ed-142">DLL</span><span class="sxs-lookup"><span data-stu-id="2b2ed-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b2ed-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b2ed-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b2ed-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b2ed-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b2ed-145">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="2b2ed-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

