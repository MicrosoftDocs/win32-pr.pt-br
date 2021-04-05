---
title: Classe MDM_Policy_Config01_SmartScreen02
description: A \_ classe Config01 SmartScreen02 de política de MDM \_ \_ configura as políticas de tela inteligente.
ms.assetid: e5ad04a1-afa9-4887-a4c1-c92c574a5398
keywords:
- Classe MDM_Policy_Config01_SmartScreen02
- Classe MDM_Policy_Config01_SmartScreen02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_SmartScreen02
- MDM_Policy_Config01_SmartScreen02.InstanceID
- MDM_Policy_Config01_SmartScreen02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09e0b8ca0c1e53005ab2a2ab80cce3f18dec40b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009420"
---
# <a name="mdm_policy_config01_smartscreen02-class"></a><span data-ttu-id="a5b93-105">\_Classe MDM \_ Config01 \_ SmartScreen02</span><span class="sxs-lookup"><span data-stu-id="a5b93-105">MDM\_Policy\_Config01\_SmartScreen02 class</span></span>

<span data-ttu-id="a5b93-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="a5b93-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a5b93-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="a5b93-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a5b93-108">A \_ classe Config01 SmartScreen02 de política de MDM \_ \_ configura as políticas de tela inteligente.</span><span class="sxs-lookup"><span data-stu-id="a5b93-108">The MDM\_Policy\_Config01\_SmartScreen02 class configures the smart screen policies.</span></span>

<span data-ttu-id="a5b93-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a5b93-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5b93-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5b93-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_SmartScreen02
{
  string InstanceID;
  string ParentID;
  sint32 EnableAppInstallControl;
  sint32 EnableSmartScreenInShell;
  sint32 PreventOverrideForFilesInShell;
};
```

## <a name="members"></a><span data-ttu-id="a5b93-111">Membros</span><span class="sxs-lookup"><span data-stu-id="a5b93-111">Members</span></span>

<span data-ttu-id="a5b93-112">A **classe \_ \_ Config01 \_ SmartScreen02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a5b93-112">The **MDM\_Policy\_Config01\_SmartScreen02** class has these types of members:</span></span>

-   [<span data-ttu-id="a5b93-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a5b93-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a5b93-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a5b93-114">Properties</span></span>

<span data-ttu-id="a5b93-115">A **classe \_ \_ Config01 \_ SmartScreen02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a5b93-115">The **MDM\_Policy\_Config01\_SmartScreen02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a5b93-116">EnableAppInstallControl</span><span class="sxs-lookup"><span data-stu-id="a5b93-116">EnableAppInstallControl</span></span>](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-enableappinstallcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5b93-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a5b93-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a5b93-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a5b93-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a5b93-119">EnableSmartScreenInShell</span><span class="sxs-lookup"><span data-stu-id="a5b93-119">EnableSmartScreenInShell</span></span>](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-enablesmartscreeninshell)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5b93-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a5b93-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a5b93-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a5b93-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a5b93-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a5b93-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5b93-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a5b93-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5b93-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a5b93-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5b93-125">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a5b93-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a5b93-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a5b93-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5b93-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a5b93-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5b93-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a5b93-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5b93-129">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a5b93-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a5b93-130">PreventOverrideForFilesInShell</span><span class="sxs-lookup"><span data-stu-id="a5b93-130">PreventOverrideForFilesInShell</span></span>](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-preventoverrideforfilesinshell)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5b93-131">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a5b93-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a5b93-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a5b93-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5b93-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5b93-133">Requirements</span></span>



| <span data-ttu-id="a5b93-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5b93-134">Requirement</span></span> | <span data-ttu-id="a5b93-135">Valor</span><span class="sxs-lookup"><span data-stu-id="a5b93-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b93-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5b93-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a5b93-137">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a5b93-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a5b93-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5b93-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a5b93-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a5b93-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a5b93-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="a5b93-140">Namespace</span></span><br/>                | <span data-ttu-id="a5b93-141">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="a5b93-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a5b93-142">MOF</span><span class="sxs-lookup"><span data-stu-id="a5b93-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5b93-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5b93-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5b93-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a5b93-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5b93-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5b93-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

