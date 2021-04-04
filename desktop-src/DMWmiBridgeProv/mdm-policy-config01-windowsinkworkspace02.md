---
title: Classe MDM_Policy_Config01_WindowsInkWorkspace02
description: A \_ classe MDM Policy \_ Config01 \_ WindowsInkWorkspace02 representa as políticas de espaço de trabalho de tinta disponíveis.
ms.assetid: 676a459f-25b0-4cf7-bf64-635ac4a93f59
keywords:
- Classe MDM_Policy_Config01_WindowsInkWorkspace02
- Classe MDM_Policy_Config01_WindowsInkWorkspace02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_WindowsInkWorkspace02
- MDM_Policy_Config01_WindowsInkWorkspace02.InstanceID
- MDM_Policy_Config01_WindowsInkWorkspace02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f654326b0a44ed40faa06dfe80d933dc2c52c4f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918512"
---
# <a name="mdm_policy_config01_windowsinkworkspace02-class"></a><span data-ttu-id="d71a1-105">\_Classe MDM \_ Config01 \_ WindowsInkWorkspace02</span><span class="sxs-lookup"><span data-stu-id="d71a1-105">MDM\_Policy\_Config01\_WindowsInkWorkspace02 class</span></span>

<span data-ttu-id="d71a1-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="d71a1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d71a1-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="d71a1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d71a1-108">A classe **MDM \_ Policy \_ Config01 \_ WindowsInkWorkspace02** representa as políticas de espaço de trabalho de tinta disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d71a1-108">The **MDM\_Policy\_Config01\_WindowsInkWorkspace02** class represents the ink workspace policies available.</span></span>

<span data-ttu-id="d71a1-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d71a1-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d71a1-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d71a1-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_WindowsInkWorkspace02
{
  string InstanceID;
  string ParentID;
  sint32 AllowWindowsInkWorkspace;
  sint32 AllowSuggestedAppsInWindowsInkWorkspace;
};
```

## <a name="members"></a><span data-ttu-id="d71a1-111">Membros</span><span class="sxs-lookup"><span data-stu-id="d71a1-111">Members</span></span>

<span data-ttu-id="d71a1-112">A **classe \_ \_ Config01 \_ WindowsInkWorkspace02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d71a1-112">The **MDM\_Policy\_Config01\_WindowsInkWorkspace02** class has these types of members:</span></span>

-   [<span data-ttu-id="d71a1-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d71a1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d71a1-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d71a1-114">Properties</span></span>

<span data-ttu-id="d71a1-115">A **classe \_ \_ Config01 \_ WindowsInkWorkspace02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d71a1-115">The **MDM\_Policy\_Config01\_WindowsInkWorkspace02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d71a1-116">AllowSuggestedAppsInWindowsInkWorkspace</span><span class="sxs-lookup"><span data-stu-id="d71a1-116">AllowSuggestedAppsInWindowsInkWorkspace</span></span>](/windows/client-management/mdm/policy-csp-windowsinkworkspace#windowsinkworkspace-allowsuggestedappsinwindowsinkworkspace)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d71a1-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d71a1-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d71a1-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d71a1-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d71a1-119">AllowWindowsInkWorkspace</span><span class="sxs-lookup"><span data-stu-id="d71a1-119">AllowWindowsInkWorkspace</span></span>](/windows/client-management/mdm/policy-csp-windowsinkworkspace#windowsinkworkspace-allowwindowsinkworkspace)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d71a1-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d71a1-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d71a1-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d71a1-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d71a1-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d71a1-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d71a1-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d71a1-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d71a1-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d71a1-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d71a1-125">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d71a1-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d71a1-126">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="d71a1-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="d71a1-127">Para essa classe, a cadeia de caracteres é "WindowsInkWorkspace".</span><span class="sxs-lookup"><span data-stu-id="d71a1-127">For this class, the string is "WindowsInkWorkspace".</span></span>

</dd> <dt>

<span data-ttu-id="d71a1-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d71a1-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d71a1-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d71a1-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d71a1-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d71a1-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d71a1-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d71a1-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d71a1-132">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="d71a1-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="d71a1-133">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="d71a1-133">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d71a1-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d71a1-134">Requirements</span></span>



| <span data-ttu-id="d71a1-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="d71a1-135">Requirement</span></span> | <span data-ttu-id="d71a1-136">Valor</span><span class="sxs-lookup"><span data-stu-id="d71a1-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d71a1-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d71a1-137">Minimum supported client</span></span><br/> | <span data-ttu-id="d71a1-138">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d71a1-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d71a1-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d71a1-139">Minimum supported server</span></span><br/> | <span data-ttu-id="d71a1-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d71a1-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="d71a1-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="d71a1-141">Namespace</span></span><br/>                | <span data-ttu-id="d71a1-142">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="d71a1-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="d71a1-143">MOF</span><span class="sxs-lookup"><span data-stu-id="d71a1-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d71a1-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d71a1-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="d71a1-145">DLL</span><span class="sxs-lookup"><span data-stu-id="d71a1-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d71a1-146"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="d71a1-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

