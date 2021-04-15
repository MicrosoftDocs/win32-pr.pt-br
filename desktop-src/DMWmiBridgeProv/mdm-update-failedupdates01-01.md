---
title: Classe MDM_Update_FailedUpdates01_01
description: A \_ classe MDM update \_ FailedUpdates01 \_ 01 é usada para gerenciar atualizações com falha.
ms.assetid: 3bb7993b-b44b-44d1-84ee-dbdda0093ca0
keywords:
- Classe MDM_Update_FailedUpdates01_01
- Classe MDM_Update_FailedUpdates01_01, descrita
topic_type:
- apiref
api_name:
- MDM_Update_FailedUpdates01_01
- MDM_Update_FailedUpdates01_01.InstanceID
- MDM_Update_FailedUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0ba8d42d97b15cd195e87f536abad9610492e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454665"
---
# <a name="mdm_update_failedupdates01_01-class"></a><span data-ttu-id="2384f-105">\_ \_ Classe FailedUpdates01 01 de atualização \_ do MDM</span><span class="sxs-lookup"><span data-stu-id="2384f-105">MDM\_Update\_FailedUpdates01\_01 class</span></span>

<span data-ttu-id="2384f-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="2384f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2384f-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="2384f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2384f-108">A classe **MDM \_ Update \_ FailedUpdates01 \_ 01** é usada para gerenciar atualizações com falha.</span><span class="sxs-lookup"><span data-stu-id="2384f-108">The **MDM\_Update\_FailedUpdates01\_01** class is used to manage failed updates.</span></span>

<span data-ttu-id="2384f-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2384f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2384f-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2384f-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_FailedUpdates01_01
{
  string InstanceID;
  string ParentID;
  sint32 HResult;
  sint32 State;
};
```

## <a name="members"></a><span data-ttu-id="2384f-111">Membros</span><span class="sxs-lookup"><span data-stu-id="2384f-111">Members</span></span>

<span data-ttu-id="2384f-112">A classe **MDM \_ Update \_ FailedUpdates01 \_ 01** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2384f-112">The **MDM\_Update\_FailedUpdates01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="2384f-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2384f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2384f-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2384f-114">Properties</span></span>

<span data-ttu-id="2384f-115">A classe **MDM \_ Update \_ FailedUpdates01 \_ 01** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2384f-115">The **MDM\_Update\_FailedUpdates01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2384f-116">Resultado</span><span class="sxs-lookup"><span data-stu-id="2384f-116">HResult</span></span>](/windows/client-management/mdm/update-csp#failedupdates-failed-update-guid-hresult)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2384f-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2384f-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2384f-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2384f-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2384f-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2384f-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2384f-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2384f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2384f-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2384f-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2384f-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2384f-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2384f-123">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="2384f-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="2384f-124">Para essa classe, a cadeia de caracteres é o GUID da atualização com falha.</span><span class="sxs-lookup"><span data-stu-id="2384f-124">For this class, the string is the GUID of the failed update.</span></span>

</dd> <dt>

<span data-ttu-id="2384f-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2384f-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2384f-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2384f-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2384f-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2384f-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2384f-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2384f-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2384f-129">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="2384f-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="2384f-130">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Update/FailedUpdates"</span><span class="sxs-lookup"><span data-stu-id="2384f-130">For this class, the string is "./Vendor/MSFT/Update/FailedUpdates"</span></span>

</dd> <dt>

[<span data-ttu-id="2384f-131">**Status**</span><span class="sxs-lookup"><span data-stu-id="2384f-131">**State**</span></span>](/windows/client-management/mdm/update-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2384f-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2384f-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2384f-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2384f-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2384f-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2384f-134">Requirements</span></span>



| <span data-ttu-id="2384f-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="2384f-135">Requirement</span></span> | <span data-ttu-id="2384f-136">Valor</span><span class="sxs-lookup"><span data-stu-id="2384f-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2384f-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2384f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="2384f-138">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2384f-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2384f-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2384f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="2384f-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2384f-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="2384f-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="2384f-141">Namespace</span></span><br/>                | <span data-ttu-id="2384f-142">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="2384f-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="2384f-143">MOF</span><span class="sxs-lookup"><span data-stu-id="2384f-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2384f-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2384f-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="2384f-145">DLL</span><span class="sxs-lookup"><span data-stu-id="2384f-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2384f-146"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="2384f-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

