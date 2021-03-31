---
title: Classe MDM_Policy_Result01_AboveLock02
description: A \_ classe MDM Policy \_ Result01 \_ AboveLock02 representa políticas que determinam as ações que são permitidas acima da tela de bloqueio do dispositivo.
ms.assetid: 0b6d4083-2484-450b-9261-5ef339db4707
keywords:
- Classe MDM_Policy_Result01_AboveLock02
- Classe MDM_Policy_Result01_AboveLock02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_AboveLock02
- MDM_Policy_Result01_AboveLock02.InstanceID
- MDM_Policy_Result01_AboveLock02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530ed3c4afd3b6e888ee77d0963881c2b4d5ef93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918511"
---
# <a name="mdm_policy_result01_abovelock02-class"></a><span data-ttu-id="c76af-105">\_Classe MDM \_ Result01 \_ AboveLock02</span><span class="sxs-lookup"><span data-stu-id="c76af-105">MDM\_Policy\_Result01\_AboveLock02 class</span></span>

<span data-ttu-id="c76af-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="c76af-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c76af-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="c76af-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c76af-108">A classe **MDM \_ Policy \_ Result01 \_ AboveLock02** representa políticas que determinam as ações que são permitidas acima da tela de bloqueio do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c76af-108">The **MDM\_Policy\_Result01\_AboveLock02** class represents policies that determine actions that are allowed above the Device Lock screen.</span></span>

<span data-ttu-id="c76af-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c76af-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c76af-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c76af-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_AboveLock02
{
  string InstanceID;
  string ParentID;
  sint32 AllowToasts;
  sint32 AllowCortanaAboveLock;
};
```

## <a name="members"></a><span data-ttu-id="c76af-111">Membros</span><span class="sxs-lookup"><span data-stu-id="c76af-111">Members</span></span>

<span data-ttu-id="c76af-112">A **classe \_ \_ Result01 \_ AboveLock02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c76af-112">The **MDM\_Policy\_Result01\_AboveLock02** class has these types of members:</span></span>

-   [<span data-ttu-id="c76af-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c76af-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c76af-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c76af-114">Properties</span></span>

<span data-ttu-id="c76af-115">A **classe \_ \_ Result01 \_ AboveLock02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c76af-115">The **MDM\_Policy\_Result01\_AboveLock02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c76af-116">AllowCortanaAboveLock</span><span class="sxs-lookup"><span data-stu-id="c76af-116">AllowCortanaAboveLock</span></span>](/windows/client-management/mdm/policy-csp-abovelock#abovelock-allowcortanaabovelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c76af-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c76af-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c76af-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c76af-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c76af-119">AllowToasts</span><span class="sxs-lookup"><span data-stu-id="c76af-119">AllowToasts</span></span>](/windows/client-management/mdm/policy-csp-abovelock#abovelock-allowtoasts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c76af-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c76af-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c76af-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c76af-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c76af-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c76af-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c76af-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c76af-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c76af-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c76af-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c76af-125">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c76af-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c76af-126">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="c76af-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="c76af-127">Para essa classe, a cadeia de caracteres é "AboveLock".</span><span class="sxs-lookup"><span data-stu-id="c76af-127">For this class, the string is "AboveLock".</span></span>

</dd> <dt>

<span data-ttu-id="c76af-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c76af-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c76af-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c76af-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c76af-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c76af-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c76af-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c76af-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c76af-132">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="c76af-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="c76af-133">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="c76af-133">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c76af-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c76af-134">Requirements</span></span>



| <span data-ttu-id="c76af-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="c76af-135">Requirement</span></span> | <span data-ttu-id="c76af-136">Valor</span><span class="sxs-lookup"><span data-stu-id="c76af-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c76af-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c76af-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c76af-138">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c76af-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c76af-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c76af-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c76af-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c76af-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c76af-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="c76af-141">Namespace</span></span><br/>                | <span data-ttu-id="c76af-142">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="c76af-142">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="c76af-143">MOF</span><span class="sxs-lookup"><span data-stu-id="c76af-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c76af-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c76af-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c76af-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c76af-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c76af-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c76af-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c76af-147">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c76af-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c76af-148">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="c76af-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

