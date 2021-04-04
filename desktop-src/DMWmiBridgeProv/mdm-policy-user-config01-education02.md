---
title: Classe MDM_Policy_User_Config01_Education02
description: A \_ \_ classe Config01 Education02 do usuário da política de MDM \_ \_ configura as políticas de educação.
ms.assetid: d9a263c7-ee9c-4857-b9a6-f0efdb373e13
keywords:
- Classe MDM_Policy_User_Config01_Education02
- Classe MDM_Policy_User_Config01_Education02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Education02
- MDM_Policy_User_Config01_Education02.InstanceID
- MDM_Policy_User_Config01_Education02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42ae8508668b95edce1d4c4a2d0e99cbba2bc6d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918156"
---
# <a name="mdm_policy_user_config01_education02-class"></a><span data-ttu-id="419c0-105">Config01 de usuário de política de MDM- \_ \_ \_ \_ classe Education02</span><span class="sxs-lookup"><span data-stu-id="419c0-105">MDM\_Policy\_User\_Config01\_Education02 class</span></span>

<span data-ttu-id="419c0-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="419c0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="419c0-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="419c0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="419c0-108">A \_ \_ classe Config01 Education02 do usuário da política de MDM \_ \_ configura as políticas de educação.</span><span class="sxs-lookup"><span data-stu-id="419c0-108">The MDM\_Policy\_User\_Config01\_Education02 class configures the education policies.</span></span>

<span data-ttu-id="419c0-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="419c0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="419c0-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="419c0-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Education02
{
  string InstanceID;
  string ParentID;
  string DefaultPrinterName;
  sint32 PreventAddingNewPrinters;
  string PrinterNames;
};
```

## <a name="members"></a><span data-ttu-id="419c0-111">Membros</span><span class="sxs-lookup"><span data-stu-id="419c0-111">Members</span></span>

<span data-ttu-id="419c0-112">A **classe \_ \_ \_ Config01 \_ Education02 do usuário da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="419c0-112">The **MDM\_Policy\_User\_Config01\_Education02** class has these types of members:</span></span>

-   [<span data-ttu-id="419c0-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="419c0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="419c0-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="419c0-114">Properties</span></span>

<span data-ttu-id="419c0-115">A **classe \_ \_ \_ Config01 \_ Education02 do usuário da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="419c0-115">The **MDM\_Policy\_User\_Config01\_Education02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="419c0-116">Defaultprintername</span><span class="sxs-lookup"><span data-stu-id="419c0-116">DefaultPrinterName</span></span>](/windows/client-management/mdm/policy-csp-education#education-defaultprintername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="419c0-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="419c0-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419c0-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="419c0-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="419c0-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="419c0-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419c0-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="419c0-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419c0-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="419c0-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419c0-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="419c0-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="419c0-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="419c0-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419c0-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="419c0-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419c0-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="419c0-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419c0-126">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="419c0-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="419c0-127">PreventAddingNewPrinters</span><span class="sxs-lookup"><span data-stu-id="419c0-127">PreventAddingNewPrinters</span></span>](/windows/client-management/mdm/policy-csp-education#education-preventaddingnewprinters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="419c0-128">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="419c0-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="419c0-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="419c0-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="419c0-130">Impressoras</span><span class="sxs-lookup"><span data-stu-id="419c0-130">PrinterNames</span></span>](/windows/client-management/mdm/policy-csp-education#education-printernames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="419c0-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="419c0-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419c0-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="419c0-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="419c0-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="419c0-133">Requirements</span></span>



| <span data-ttu-id="419c0-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="419c0-134">Requirement</span></span> | <span data-ttu-id="419c0-135">Valor</span><span class="sxs-lookup"><span data-stu-id="419c0-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="419c0-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="419c0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="419c0-137">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="419c0-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="419c0-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="419c0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="419c0-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="419c0-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="419c0-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="419c0-140">Namespace</span></span><br/>                | <span data-ttu-id="419c0-141">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="419c0-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="419c0-142">MOF</span><span class="sxs-lookup"><span data-stu-id="419c0-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="419c0-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="419c0-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="419c0-144">DLL</span><span class="sxs-lookup"><span data-stu-id="419c0-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="419c0-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="419c0-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

