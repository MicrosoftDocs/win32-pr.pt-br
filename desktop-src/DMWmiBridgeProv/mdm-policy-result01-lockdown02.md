---
title: Classe MDM_Policy_Result01_LockDown02
description: A \_ classe MDM Policy \_ Result01 \_ Lockdown02 representa as políticas de bloqueio disponíveis.
ms.assetid: 78eab50e-b1a7-4b96-a848-b8a86a3b82c3
keywords:
- Classe MDM_Policy_Result01_LockDown02
- Classe MDM_Policy_Result01_LockDown02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_LockDown02
- MDM_Policy_Result01_LockDown02.InstanceID
- MDM_Policy_Result01_LockDown02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 159e2178e3e5600bef4fc366a0cf49b7856ce886
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454998"
---
# <a name="mdm_policy_result01_lockdown02-class"></a><span data-ttu-id="2b02a-105">\_Classe MDM \_ Result01 \_ LockDown02</span><span class="sxs-lookup"><span data-stu-id="2b02a-105">MDM\_Policy\_Result01\_LockDown02 class</span></span>

<span data-ttu-id="2b02a-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="2b02a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2b02a-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="2b02a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2b02a-108">A classe **MDM \_ Policy \_ Result01 \_ Lockdown02** representa as políticas de bloqueio disponíveis.</span><span class="sxs-lookup"><span data-stu-id="2b02a-108">The **MDM\_Policy\_Result01\_Lockdown02** class represents the lockdown policies available.</span></span>

<span data-ttu-id="2b02a-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2b02a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b02a-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b02a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_LockDown02
{
  string InstanceID;
  string ParentID;
  sint32 AllowEdgeSwipe;
};
```

## <a name="members"></a><span data-ttu-id="2b02a-111">Membros</span><span class="sxs-lookup"><span data-stu-id="2b02a-111">Members</span></span>

<span data-ttu-id="2b02a-112">A **classe \_ \_ Result01 \_ LockDown02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2b02a-112">The **MDM\_Policy\_Result01\_LockDown02** class has these types of members:</span></span>

-   [<span data-ttu-id="2b02a-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2b02a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2b02a-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2b02a-114">Properties</span></span>

<span data-ttu-id="2b02a-115">A **classe \_ \_ Result01 \_ LockDown02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2b02a-115">The **MDM\_Policy\_Result01\_LockDown02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2b02a-116">AllowEdgeSwipe</span><span class="sxs-lookup"><span data-stu-id="2b02a-116">AllowEdgeSwipe</span></span>](/windows/client-management/mdm/policy-csp-lockdown#lockdown-allowedgeswipe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b02a-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2b02a-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2b02a-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2b02a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2b02a-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2b02a-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b02a-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2b02a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b02a-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2b02a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b02a-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2b02a-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2b02a-123">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="2b02a-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="2b02a-124">Para essa classe, a cadeia de caracteres é "bloqueio".</span><span class="sxs-lookup"><span data-stu-id="2b02a-124">For this class, the string is "Lockdown".</span></span>

</dd> <dt>

<span data-ttu-id="2b02a-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2b02a-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b02a-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2b02a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b02a-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2b02a-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b02a-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2b02a-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2b02a-129">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="2b02a-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="2b02a-130">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="2b02a-130">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2b02a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b02a-131">Requirements</span></span>



| <span data-ttu-id="2b02a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b02a-132">Requirement</span></span> | <span data-ttu-id="2b02a-133">Valor</span><span class="sxs-lookup"><span data-stu-id="2b02a-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b02a-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b02a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2b02a-135">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2b02a-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2b02a-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b02a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2b02a-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2b02a-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="2b02a-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="2b02a-138">Namespace</span></span><br/>                | <span data-ttu-id="2b02a-139">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="2b02a-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="2b02a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="2b02a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b02a-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b02a-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="2b02a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="2b02a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b02a-143"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="2b02a-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

