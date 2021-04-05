---
title: Classe MDM_Policy_Config01_DataUsage02
description: A \_ classe Config01 DataUsage02 de política de MDM \_ \_ configura as políticas de uso de dados disponíveis.
ms.assetid: c5e77d82-df5e-4eed-90f5-50f2ed62e975
keywords:
- Classe MDM_Policy_Config01_DataUsage02
- Classe MDM_Policy_Config01_DataUsage02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DataUsage02
- MDM_Policy_Config01_DataUsage02.InstanceID
- MDM_Policy_Config01_DataUsage02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b878ec3bf38444dd82c08fe880e84028067bbd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085379"
---
# <a name="mdm_policy_config01_datausage02-class"></a><span data-ttu-id="87ec9-105">\_Classe MDM \_ Config01 \_ DataUsage02</span><span class="sxs-lookup"><span data-stu-id="87ec9-105">MDM\_Policy\_Config01\_DataUsage02 class</span></span>

<span data-ttu-id="87ec9-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="87ec9-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="87ec9-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="87ec9-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="87ec9-108">A \_ classe Config01 DataUsage02 de política de MDM \_ \_ configura as políticas de uso de dados disponíveis.</span><span class="sxs-lookup"><span data-stu-id="87ec9-108">The MDM\_Policy\_Config01\_DataUsage02 class configures the available data usage policies.</span></span>

<span data-ttu-id="87ec9-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="87ec9-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="87ec9-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87ec9-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DataUsage02
{
  string InstanceID;
  string ParentID;
  string SetCost3G;
  string SetCost4G;
};
```

## <a name="members"></a><span data-ttu-id="87ec9-111">Membros</span><span class="sxs-lookup"><span data-stu-id="87ec9-111">Members</span></span>

<span data-ttu-id="87ec9-112">A **classe \_ \_ Config01 \_ DataUsage02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="87ec9-112">The **MDM\_Policy\_Config01\_DataUsage02** class has these types of members:</span></span>

-   [<span data-ttu-id="87ec9-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="87ec9-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="87ec9-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="87ec9-114">Properties</span></span>

<span data-ttu-id="87ec9-115">A **classe \_ \_ Config01 \_ DataUsage02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="87ec9-115">The **MDM\_Policy\_Config01\_DataUsage02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="87ec9-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="87ec9-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ec9-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="87ec9-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87ec9-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87ec9-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87ec9-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="87ec9-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="87ec9-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="87ec9-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ec9-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="87ec9-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87ec9-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87ec9-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87ec9-123">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="87ec9-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="87ec9-124">SetCost3G</span><span class="sxs-lookup"><span data-stu-id="87ec9-124">SetCost3G</span></span>](/windows/client-management/mdm/policy-csp-datausage#datausage-setcost3g)
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ec9-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="87ec9-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87ec9-126">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="87ec9-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="87ec9-127">SetCost4G</span><span class="sxs-lookup"><span data-stu-id="87ec9-127">SetCost4G</span></span>](/windows/client-management/mdm/policy-csp-datausage#datausage-setcost4g)
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ec9-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="87ec9-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87ec9-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="87ec9-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="87ec9-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87ec9-130">Requirements</span></span>



| <span data-ttu-id="87ec9-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="87ec9-131">Requirement</span></span> | <span data-ttu-id="87ec9-132">Valor</span><span class="sxs-lookup"><span data-stu-id="87ec9-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87ec9-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87ec9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="87ec9-134">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="87ec9-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="87ec9-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87ec9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="87ec9-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="87ec9-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="87ec9-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="87ec9-137">Namespace</span></span><br/>                | <span data-ttu-id="87ec9-138">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="87ec9-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="87ec9-139">MOF</span><span class="sxs-lookup"><span data-stu-id="87ec9-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87ec9-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="87ec9-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="87ec9-141">DLL</span><span class="sxs-lookup"><span data-stu-id="87ec9-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87ec9-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87ec9-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

