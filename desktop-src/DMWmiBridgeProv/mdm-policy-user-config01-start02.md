---
title: Classe MDM_Policy_User_Config01_Start02
description: A \_ classe Config01 Start02 do usuário da política de MDM \_ \_ \_ representa as políticas de início disponíveis que são definidas por usuário.
ms.assetid: bbb64553-4d93-433d-96e4-bfd3f5588138
keywords:
- Classe MDM_Policy_User_Config01_Start02
- Classe MDM_Policy_User_Config01_Start02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Start02
- MDM_Policy_User_Config01_Start02.InstanceID
- MDM_Policy_User_Config01_Start02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b98b25ee0c3118f741d3a52bc9001c6106d86f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369648"
---
# <a name="mdm_policy_user_config01_start02-class"></a><span data-ttu-id="b718e-105">Config01 de usuário de política de MDM- \_ \_ \_ \_ classe Start02</span><span class="sxs-lookup"><span data-stu-id="b718e-105">MDM\_Policy\_User\_Config01\_Start02 class</span></span>

<span data-ttu-id="b718e-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="b718e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b718e-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="b718e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b718e-108">A **classe \_ \_ \_ Config01 \_ Start02 do usuário da política de MDM** representa as políticas de início disponíveis que são definidas por usuário.</span><span class="sxs-lookup"><span data-stu-id="b718e-108">The **MDM\_Policy\_User\_Config01\_Start02** class represents the start policies available that are set on a per-user basis.</span></span>

<span data-ttu-id="b718e-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b718e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b718e-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b718e-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Start02
{
  string InstanceID;
  string ParentID;
  sint32 HidePeopleBar;
  string StartLayout;
};
```

## <a name="members"></a><span data-ttu-id="b718e-111">Membros</span><span class="sxs-lookup"><span data-stu-id="b718e-111">Members</span></span>

<span data-ttu-id="b718e-112">A **classe \_ \_ \_ Config01 \_ Start02 do usuário da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b718e-112">The **MDM\_Policy\_User\_Config01\_Start02** class has these types of members:</span></span>

-   [<span data-ttu-id="b718e-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b718e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b718e-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b718e-114">Properties</span></span>

<span data-ttu-id="b718e-115">A **classe \_ \_ \_ Config01 \_ Start02 do usuário da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b718e-115">The **MDM\_Policy\_User\_Config01\_Start02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b718e-116">HidePeopleBar</span><span class="sxs-lookup"><span data-stu-id="b718e-116">HidePeopleBar</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidepeoplebar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b718e-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b718e-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b718e-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b718e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b718e-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b718e-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b718e-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b718e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b718e-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b718e-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b718e-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b718e-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b718e-123">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="b718e-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="b718e-124">Para essa classe, a cadeia de caracteres é "Start"</span><span class="sxs-lookup"><span data-stu-id="b718e-124">For this class, the string is "Start"</span></span>

</dd> <dt>

<span data-ttu-id="b718e-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b718e-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b718e-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b718e-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b718e-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b718e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b718e-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b718e-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b718e-129">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="b718e-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="b718e-130">Para essa classe, a cadeia de caracteres é "./User/Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="b718e-130">For this class, the string is "./User/Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="b718e-131">StartLayout</span><span class="sxs-lookup"><span data-stu-id="b718e-131">StartLayout</span></span>](/windows/client-management/mdm/policy-csp-start#start-startlayout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b718e-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b718e-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b718e-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b718e-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b718e-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b718e-134">Requirements</span></span>



| <span data-ttu-id="b718e-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b718e-135">Requirement</span></span> | <span data-ttu-id="b718e-136">Valor</span><span class="sxs-lookup"><span data-stu-id="b718e-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b718e-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b718e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b718e-138">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b718e-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b718e-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b718e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b718e-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b718e-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b718e-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="b718e-141">Namespace</span></span><br/>                | <span data-ttu-id="b718e-142">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="b718e-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b718e-143">MOF</span><span class="sxs-lookup"><span data-stu-id="b718e-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b718e-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b718e-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b718e-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b718e-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b718e-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b718e-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b718e-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="b718e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b718e-148">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="b718e-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

