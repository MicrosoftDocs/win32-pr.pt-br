---
title: Classe MDM_Policy_Result01_Licensing02
description: A \_ classe MDM Policy \_ Result01 \_ Licensing02 representa as políticas de licenciamento disponíveis.
ms.assetid: 0f3faa78-c9ed-4166-a860-b5096b33772a
keywords:
- Classe MDM_Policy_Result01_Licensing02
- Classe MDM_Policy_Result01_Licensing02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Licensing02
- MDM_Policy_Result01_Licensing02.InstanceID
- MDM_Policy_Result01_Licensing02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa40b1aa0ff64ddd360a304f5366f961fc2c993c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009253"
---
# <a name="mdm_policy_result01_licensing02-class"></a><span data-ttu-id="32e38-105">\_Classe MDM \_ Result01 \_ Licensing02</span><span class="sxs-lookup"><span data-stu-id="32e38-105">MDM\_Policy\_Result01\_Licensing02 class</span></span>

<span data-ttu-id="32e38-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="32e38-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="32e38-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="32e38-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="32e38-108">A classe **MDM \_ Policy \_ Result01 \_ Licensing02** representa as políticas de licenciamento disponíveis.</span><span class="sxs-lookup"><span data-stu-id="32e38-108">The **MDM\_Policy\_Result01\_Licensing02** class represents the licensing policies available.</span></span>

<span data-ttu-id="32e38-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="32e38-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="32e38-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32e38-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Licensing02
{
  string InstanceID;
  string ParentID;
  sint32 AllowWindowsEntitlementReactivation;
  sint32 DisallowKMSClientOnlineAVSValidation;
};
```

## <a name="members"></a><span data-ttu-id="32e38-111">Membros</span><span class="sxs-lookup"><span data-stu-id="32e38-111">Members</span></span>

<span data-ttu-id="32e38-112">A **classe \_ \_ Result01 \_ Licensing02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="32e38-112">The **MDM\_Policy\_Result01\_Licensing02** class has these types of members:</span></span>

-   [<span data-ttu-id="32e38-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="32e38-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32e38-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="32e38-114">Properties</span></span>

<span data-ttu-id="32e38-115">A **classe \_ \_ Result01 \_ Licensing02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="32e38-115">The **MDM\_Policy\_Result01\_Licensing02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="32e38-116">AllowWindowsEntitlementReactivation</span><span class="sxs-lookup"><span data-stu-id="32e38-116">AllowWindowsEntitlementReactivation</span></span>](/windows/client-management/mdm/policy-csp-licensing#licensing-allowwindowsentitlementreactivation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e38-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="32e38-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="32e38-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="32e38-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="32e38-119">DisallowKMSClientOnlineAVSValidation</span><span class="sxs-lookup"><span data-stu-id="32e38-119">DisallowKMSClientOnlineAVSValidation</span></span>](/windows/client-management/mdm/policy-csp-licensing#licensing-disallowkmsclientonlineavsvalidation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e38-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="32e38-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="32e38-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="32e38-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="32e38-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="32e38-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e38-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="32e38-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32e38-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="32e38-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32e38-125">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="32e38-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="32e38-126">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="32e38-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="32e38-127">Para essa classe, a cadeia de caracteres é "licenciamento".</span><span class="sxs-lookup"><span data-stu-id="32e38-127">For this class, the string is "Licensing".</span></span>

</dd> <dt>

<span data-ttu-id="32e38-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="32e38-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e38-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="32e38-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32e38-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="32e38-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32e38-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="32e38-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="32e38-132">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="32e38-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="32e38-133">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="32e38-133">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32e38-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32e38-134">Requirements</span></span>



| <span data-ttu-id="32e38-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="32e38-135">Requirement</span></span> | <span data-ttu-id="32e38-136">Valor</span><span class="sxs-lookup"><span data-stu-id="32e38-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32e38-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32e38-137">Minimum supported client</span></span><br/> | <span data-ttu-id="32e38-138">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="32e38-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="32e38-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32e38-139">Minimum supported server</span></span><br/> | <span data-ttu-id="32e38-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="32e38-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="32e38-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="32e38-141">Namespace</span></span><br/>                | <span data-ttu-id="32e38-142">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="32e38-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="32e38-143">MOF</span><span class="sxs-lookup"><span data-stu-id="32e38-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32e38-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32e38-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="32e38-145">DLL</span><span class="sxs-lookup"><span data-stu-id="32e38-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32e38-146"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="32e38-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

