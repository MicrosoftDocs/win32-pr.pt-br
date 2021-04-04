---
title: Classe MDM_Policy_Config01_Printers02
description: A \_ classe Config01 Printers02 de política de MDM \_ \_ configura as políticas de impressora.
ms.assetid: c0e6dc53-5f84-4cef-a4c4-08db6486784a
keywords:
- Classe MDM_Policy_Config01_Printers02
- Classe MDM_Policy_Config01_Printers02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Printers02
- MDM_Policy_Config01_Printers02.InstanceID
- MDM_Policy_Config01_Printers02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca2cfdc41cfb956d00a509ba499b22e2435d7973
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824394"
---
# <a name="mdm_policy_config01_printers02-class"></a><span data-ttu-id="713d6-105">\_Classe MDM \_ Config01 \_ Printers02</span><span class="sxs-lookup"><span data-stu-id="713d6-105">MDM\_Policy\_Config01\_Printers02 class</span></span>

<span data-ttu-id="713d6-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="713d6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="713d6-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="713d6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="713d6-108">A \_ classe Config01 Printers02 de política de MDM \_ \_ configura as políticas de impressora.</span><span class="sxs-lookup"><span data-stu-id="713d6-108">The MDM\_Policy\_Config01\_Printers02 class configures the printer policies.</span></span>

<span data-ttu-id="713d6-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="713d6-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="713d6-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="713d6-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Printers02
{
  string InstanceID;
  string ParentID;
  string PointAndPrintRestrictions;
  string PublishPrinters;
};
```

## <a name="members"></a><span data-ttu-id="713d6-111">Membros</span><span class="sxs-lookup"><span data-stu-id="713d6-111">Members</span></span>

<span data-ttu-id="713d6-112">A **classe \_ \_ Config01 \_ Printers02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="713d6-112">The **MDM\_Policy\_Config01\_Printers02** class has these types of members:</span></span>

-   [<span data-ttu-id="713d6-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="713d6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="713d6-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="713d6-114">Properties</span></span>

<span data-ttu-id="713d6-115">A **classe \_ \_ Config01 \_ Printers02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="713d6-115">The **MDM\_Policy\_Config01\_Printers02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="713d6-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="713d6-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="713d6-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="713d6-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="713d6-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="713d6-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="713d6-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="713d6-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="713d6-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="713d6-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="713d6-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="713d6-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="713d6-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="713d6-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="713d6-123">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="713d6-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="713d6-124">PointAndPrintRestrictions</span><span class="sxs-lookup"><span data-stu-id="713d6-124">PointAndPrintRestrictions</span></span>](/windows/client-management/mdm/policy-csp-printers#printers-pointandprintrestrictions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="713d6-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="713d6-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="713d6-126">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="713d6-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="713d6-127">PublishPrinters</span><span class="sxs-lookup"><span data-stu-id="713d6-127">PublishPrinters</span></span>](/windows/client-management/mdm/policy-csp-printers#printers-publishprinters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="713d6-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="713d6-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="713d6-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="713d6-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="713d6-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="713d6-130">Requirements</span></span>



| <span data-ttu-id="713d6-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="713d6-131">Requirement</span></span> | <span data-ttu-id="713d6-132">Valor</span><span class="sxs-lookup"><span data-stu-id="713d6-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="713d6-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="713d6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="713d6-134">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="713d6-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="713d6-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="713d6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="713d6-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="713d6-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="713d6-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="713d6-137">Namespace</span></span><br/>                | <span data-ttu-id="713d6-138">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="713d6-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="713d6-139">MOF</span><span class="sxs-lookup"><span data-stu-id="713d6-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="713d6-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="713d6-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="713d6-141">DLL</span><span class="sxs-lookup"><span data-stu-id="713d6-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="713d6-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="713d6-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

