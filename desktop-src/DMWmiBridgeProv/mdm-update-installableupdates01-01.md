---
title: Classe MDM_Update_InstallableUpdates01_01
description: A \_ classe MDM update \_ InstallableUpdates01 \_ 01 é usada para gerenciar e controlar a distribuição de atualizações aprovadas.
ms.assetid: 53ca2291-a92a-46ed-948d-6d2a2dddd296
keywords:
- Classe MDM_Update_InstallableUpdates01_01
- Classe MDM_Update_InstallableUpdates01_01, descrita
topic_type:
- apiref
api_name:
- MDM_Update_InstallableUpdates01_01
- MDM_Update_InstallableUpdates01_01.InstanceID
- MDM_Update_InstallableUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2bcb9dd3ec026e6894d4ba7155cc41f12bc01e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824184"
---
# <a name="mdm_update_installableupdates01_01-class"></a><span data-ttu-id="3e501-105">\_ \_ Classe InstallableUpdates01 01 de atualização \_ do MDM</span><span class="sxs-lookup"><span data-stu-id="3e501-105">MDM\_Update\_InstallableUpdates01\_01 class</span></span>

<span data-ttu-id="3e501-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="3e501-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3e501-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="3e501-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3e501-108">A classe **MDM \_ Update \_ InstallableUpdates01 \_ 01** é usada para gerenciar e controlar a distribuição de atualizações aprovadas.</span><span class="sxs-lookup"><span data-stu-id="3e501-108">The **MDM\_Update\_InstallableUpdates01\_01** class is used to manage and control the rollout of approved updates.</span></span>

<span data-ttu-id="3e501-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3e501-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e501-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e501-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_InstallableUpdates01_01
{
  string InstanceID;
  string ParentID;
  sint32 Type;
  sint32 RevisionNumber;
};
```

## <a name="members"></a><span data-ttu-id="3e501-111">Membros</span><span class="sxs-lookup"><span data-stu-id="3e501-111">Members</span></span>

<span data-ttu-id="3e501-112">A classe **MDM \_ Update \_ InstallableUpdates01 \_ 01** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3e501-112">The **MDM\_Update\_InstallableUpdates01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="3e501-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3e501-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3e501-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3e501-114">Properties</span></span>

<span data-ttu-id="3e501-115">A classe **MDM \_ Update \_ InstallableUpdates01 \_ 01** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3e501-115">The **MDM\_Update\_InstallableUpdates01\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3e501-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3e501-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e501-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e501-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e501-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e501-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e501-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3e501-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3e501-120">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="3e501-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="3e501-121">Para essa classe, a cadeia de caracteres é o GUID da atualização aprovada.</span><span class="sxs-lookup"><span data-stu-id="3e501-121">For this class, the string is the GUID of the approved update.</span></span>

</dd> <dt>

<span data-ttu-id="3e501-122">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3e501-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e501-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e501-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e501-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e501-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e501-125">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3e501-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3e501-126">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="3e501-126">Describes the full path to the parent node.</span></span> <span data-ttu-id="3e501-127">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Update/InstallableUpdates"</span><span class="sxs-lookup"><span data-stu-id="3e501-127">For this class, the string is "./Vendor/MSFT/Update/InstallableUpdates"</span></span>

</dd> <dt>

[<span data-ttu-id="3e501-128">RevisionNumber</span><span class="sxs-lookup"><span data-stu-id="3e501-128">RevisionNumber</span></span>](/windows/client-management/mdm/update-csp#failedupdates-failed-update-guid-revisionnumber)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e501-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3e501-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e501-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3e501-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e501-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="3e501-131">Type</span></span>](/windows/client-management/mdm/update-csp#installableupdates-installable-update-guid-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e501-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3e501-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e501-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3e501-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e501-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e501-134">Requirements</span></span>



| <span data-ttu-id="3e501-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e501-135">Requirement</span></span> | <span data-ttu-id="3e501-136">Valor</span><span class="sxs-lookup"><span data-stu-id="3e501-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e501-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e501-137">Minimum supported client</span></span><br/> | <span data-ttu-id="3e501-138">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3e501-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3e501-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e501-139">Minimum supported server</span></span><br/> | <span data-ttu-id="3e501-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3e501-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="3e501-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e501-141">Namespace</span></span><br/>                | <span data-ttu-id="3e501-142">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="3e501-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="3e501-143">MOF</span><span class="sxs-lookup"><span data-stu-id="3e501-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e501-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e501-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="3e501-145">DLL</span><span class="sxs-lookup"><span data-stu-id="3e501-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e501-146"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="3e501-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

