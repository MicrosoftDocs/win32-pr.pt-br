---
title: Classe MDM_Update_ApprovedUpdates01_01
description: A \_ classe MDM update \_ ApprovedUpdates01 \_ 01 é usada para gerenciar e controlar a distribuição de atualizações aprovadas.
ms.assetid: 3903dbc1-c745-4e9a-a7f7-455338b77563
keywords:
- Classe MDM_Update_ApprovedUpdates01_01
- Classe MDM_Update_ApprovedUpdates01_01, descrita
topic_type:
- apiref
api_name:
- MDM_Update_ApprovedUpdates01_01
- MDM_Update_ApprovedUpdates01_01.InstanceID
- MDM_Update_ApprovedUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e6e12700b04f6e48fdf746cb27953da5849169d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918017"
---
# <a name="mdm_update_approvedupdates01_01-class"></a><span data-ttu-id="e6f35-105">\_ \_ Classe ApprovedUpdates01 01 de atualização \_ do MDM</span><span class="sxs-lookup"><span data-stu-id="e6f35-105">MDM\_Update\_ApprovedUpdates01\_01 class</span></span>

<span data-ttu-id="e6f35-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="e6f35-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e6f35-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="e6f35-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e6f35-108">A classe **MDM \_ Update \_ ApprovedUpdates01 \_ 01** é usada para gerenciar e controlar a distribuição de atualizações aprovadas.</span><span class="sxs-lookup"><span data-stu-id="e6f35-108">The **MDM\_Update\_ApprovedUpdates01\_01** class is used to manage and control the rollout of approved updates.</span></span>

<span data-ttu-id="e6f35-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e6f35-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6f35-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6f35-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_ApprovedUpdates01_01
{
  string   InstanceID;
  string   ParentID;
  datetime ApprovedTime;
};
```

## <a name="members"></a><span data-ttu-id="e6f35-111">Membros</span><span class="sxs-lookup"><span data-stu-id="e6f35-111">Members</span></span>

<span data-ttu-id="e6f35-112">A classe **MDM \_ Update \_ ApprovedUpdates01 \_ 01** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e6f35-112">The **MDM\_Update\_ApprovedUpdates01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="e6f35-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e6f35-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e6f35-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e6f35-114">Properties</span></span>

<span data-ttu-id="e6f35-115">A classe **MDM \_ Update \_ ApprovedUpdates01 \_ 01** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e6f35-115">The **MDM\_Update\_ApprovedUpdates01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e6f35-116">Aprovadotime</span><span class="sxs-lookup"><span data-stu-id="e6f35-116">ApprovedTime</span></span>](/windows/client-management/mdm/update-csp#approvedupdates-approved-update-guid-approvedtime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f35-117">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e6f35-117">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e6f35-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e6f35-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e6f35-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e6f35-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f35-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6f35-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6f35-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f35-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6f35-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e6f35-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e6f35-123">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="e6f35-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="e6f35-124">Para essa classe, a cadeia de caracteres é o GUID da atualização aprovada.</span><span class="sxs-lookup"><span data-stu-id="e6f35-124">For this class, the string is the GUID of the approved update.</span></span>

</dd> <dt>

<span data-ttu-id="e6f35-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e6f35-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f35-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6f35-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6f35-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f35-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6f35-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e6f35-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e6f35-129">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="e6f35-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="e6f35-130">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Update/ApprovedUpdates"</span><span class="sxs-lookup"><span data-stu-id="e6f35-130">For this class, the string is "./Vendor/MSFT/Update/ApprovedUpdates"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e6f35-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6f35-131">Requirements</span></span>



| <span data-ttu-id="e6f35-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6f35-132">Requirement</span></span> | <span data-ttu-id="e6f35-133">Valor</span><span class="sxs-lookup"><span data-stu-id="e6f35-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6f35-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6f35-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e6f35-135">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e6f35-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e6f35-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6f35-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e6f35-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e6f35-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="e6f35-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="e6f35-138">Namespace</span></span><br/>                | <span data-ttu-id="e6f35-139">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="e6f35-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="e6f35-140">MOF</span><span class="sxs-lookup"><span data-stu-id="e6f35-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6f35-141"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6f35-141"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="e6f35-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e6f35-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6f35-143"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="e6f35-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

