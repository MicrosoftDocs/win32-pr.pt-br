---
title: Classe MDM_Policy_Result01_Printers02
description: A \_ classe MDM Policy \_ Result01 \_ Printers02 representa as políticas de impressora.
ms.assetid: f64fbb03-c62c-4f8e-97ad-e08e068a31d1
keywords:
- Classe MDM_Policy_Result01_Printers02
- Classe MDM_Policy_Result01_Printers02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Printers02
- MDM_Policy_Result01_Printers02.InstanceID
- MDM_Policy_Result01_Printers02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042820825441928aa04d499a06df3a05ced3889d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369350"
---
# <a name="mdm_policy_result01_printers02-class"></a><span data-ttu-id="f96cc-105">\_Classe MDM \_ Result01 \_ Printers02</span><span class="sxs-lookup"><span data-stu-id="f96cc-105">MDM\_Policy\_Result01\_Printers02 class</span></span>

<span data-ttu-id="f96cc-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="f96cc-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f96cc-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="f96cc-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f96cc-108">A \_ classe MDM Policy \_ Result01 \_ Printers02 representa as políticas de impressora.</span><span class="sxs-lookup"><span data-stu-id="f96cc-108">The MDM\_Policy\_Result01\_Printers02 class represents the printer policies.</span></span>

<span data-ttu-id="f96cc-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f96cc-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f96cc-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f96cc-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Printers02
{
  string InstanceID;
  string ParentID;
  string PointAndPrintRestrictions;
  string PublishPrinters;
};
```

## <a name="members"></a><span data-ttu-id="f96cc-111">Membros</span><span class="sxs-lookup"><span data-stu-id="f96cc-111">Members</span></span>

<span data-ttu-id="f96cc-112">A **classe \_ \_ Result01 \_ Printers02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f96cc-112">The **MDM\_Policy\_Result01\_Printers02** class has these types of members:</span></span>

-   [<span data-ttu-id="f96cc-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f96cc-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f96cc-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f96cc-114">Properties</span></span>

<span data-ttu-id="f96cc-115">A **classe \_ \_ Result01 \_ Printers02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f96cc-115">The **MDM\_Policy\_Result01\_Printers02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f96cc-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f96cc-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f96cc-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f96cc-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f96cc-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f96cc-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f96cc-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f96cc-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f96cc-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f96cc-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f96cc-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f96cc-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f96cc-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f96cc-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f96cc-123">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f96cc-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f96cc-124">PointAndPrintRestrictions</span><span class="sxs-lookup"><span data-stu-id="f96cc-124">PointAndPrintRestrictions</span></span>](/windows/client-management/mdm/policy-csp-printers#printers-pointandprintrestrictions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f96cc-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f96cc-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f96cc-126">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f96cc-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f96cc-127">PublishPrinters</span><span class="sxs-lookup"><span data-stu-id="f96cc-127">PublishPrinters</span></span>](/windows/client-management/mdm/policy-csp-printers#printers-publishprinters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f96cc-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f96cc-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f96cc-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f96cc-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f96cc-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f96cc-130">Requirements</span></span>



| <span data-ttu-id="f96cc-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f96cc-131">Requirement</span></span> | <span data-ttu-id="f96cc-132">Valor</span><span class="sxs-lookup"><span data-stu-id="f96cc-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f96cc-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f96cc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f96cc-134">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f96cc-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f96cc-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f96cc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f96cc-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f96cc-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f96cc-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="f96cc-137">Namespace</span></span><br/>                | <span data-ttu-id="f96cc-138">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="f96cc-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f96cc-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f96cc-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f96cc-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f96cc-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f96cc-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f96cc-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f96cc-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f96cc-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

