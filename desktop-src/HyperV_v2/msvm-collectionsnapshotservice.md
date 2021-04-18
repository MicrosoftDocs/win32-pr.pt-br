---
description: Serviço para criar, destruir e exportar a coleção de instantâneos de sistemas virtuais.
ms.assetid: 55a6c7b4-5352-4766-b5b7-6699b1f40b78
title: Classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f9e835ad54773d69fab19861c7a9c417ac7d8a19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756929"
---
# <a name="msvm_collectionsnapshotservice-class"></a><span data-ttu-id="e9299-103">\_Classe Msvm CollectionSnapshotService</span><span class="sxs-lookup"><span data-stu-id="e9299-103">Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="e9299-104">Serviço para criar, destruir e exportar a coleção de instantâneos de sistemas virtuais.</span><span class="sxs-lookup"><span data-stu-id="e9299-104">Service to create, destroy and export snapshot collection of virtual systems.</span></span>

<span data-ttu-id="e9299-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e9299-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9299-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9299-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="e9299-107">Membros</span><span class="sxs-lookup"><span data-stu-id="e9299-107">Members</span></span>

<span data-ttu-id="e9299-108">A classe **Msvm \_ CollectionSnapshotService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e9299-108">The **Msvm\_CollectionSnapshotService** class has these types of members:</span></span>

-   [<span data-ttu-id="e9299-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="e9299-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e9299-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="e9299-110">Methods</span></span>

<span data-ttu-id="e9299-111">A classe **Msvm \_ CollectionSnapshotService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e9299-111">The **Msvm\_CollectionSnapshotService** class has these methods.</span></span>



| <span data-ttu-id="e9299-112">Método</span><span class="sxs-lookup"><span data-stu-id="e9299-112">Method</span></span>                                                                                    | <span data-ttu-id="e9299-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="e9299-113">Description</span></span>                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9299-114">**ApplySnapshot**</span><span class="sxs-lookup"><span data-stu-id="e9299-114">**ApplySnapshot**</span></span>](msvm-collectionsnapshotservice-applysnapshot.md)                     | <span data-ttu-id="e9299-115">Aplica uma coleção de instantâneos à coleção do sistema de computador virtual.</span><span class="sxs-lookup"><span data-stu-id="e9299-115">Applies a snapshot collection to the collection of virtual computer system.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="e9299-116">**ConvertToReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="e9299-116">**ConvertToReferencePoint**</span></span>](msvm-collectionsnapshotservice-converttoreferencepoint.md) | <span data-ttu-id="e9299-117">Converta um instantâneo de coleção existente em uma coleção de pontos de referência.</span><span class="sxs-lookup"><span data-stu-id="e9299-117">Convert an existing collection snapshot to a reference point collection.</span></span> <span data-ttu-id="e9299-118">A coleção de instantâneos é excluída como um efeito colateral.</span><span class="sxs-lookup"><span data-stu-id="e9299-118">The snapshot collection gets deleted as a side effect.</span></span> <span data-ttu-id="e9299-119">Somente instantâneos de recuperação podem ser convertidos em pontos de referência.</span><span class="sxs-lookup"><span data-stu-id="e9299-119">Only recovery snapshots can be converted to reference points.</span></span><br/>                      |
| [<span data-ttu-id="e9299-120">**CreateSnapshot**</span><span class="sxs-lookup"><span data-stu-id="e9299-120">**CreateSnapshot**</span></span>](msvm-collectionsnapshotservice-createsnapshot.md)                   | <span data-ttu-id="e9299-121">Cria um instantâneo de uma coleção de sistemas virtuais.</span><span class="sxs-lookup"><span data-stu-id="e9299-121">Creates a snapshot of a virtual system collection.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="e9299-122">**DestroySnapshot**</span><span class="sxs-lookup"><span data-stu-id="e9299-122">**DestroySnapshot**</span></span>](msvm-collectionsnapshotservice-destroysnapshot.md)                 | <span data-ttu-id="e9299-123">Destruir um instantâneo existente da coleção de sistemas virtuais.</span><span class="sxs-lookup"><span data-stu-id="e9299-123">Destroy an existing snapshot of virtual system collection.</span></span> <span data-ttu-id="e9299-124">Esse método pode, como um efeito colateral, destruir outros instantâneos que dependem do instantâneo afetado.</span><span class="sxs-lookup"><span data-stu-id="e9299-124">This method may as a side effect destroy other snapshots that are dependent on the affected snapshot.</span></span><br/>                                                   |
| [<span data-ttu-id="e9299-125">**ExportSnapshot**</span><span class="sxs-lookup"><span data-stu-id="e9299-125">**ExportSnapshot**</span></span>](msvm-collectionsnapshotservice-exportsnapshot.md)                   | <span data-ttu-id="e9299-126">Exporta uma coleção de instantâneos de sistemas de computador virtual para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="e9299-126">Exports a snapshot collection of virtual computer systems to a file.</span></span> <span data-ttu-id="e9299-127">A coleção de instantâneos, suas definições de configuração associadas e suas configurações de recurso associadas serão preservadas no arquivo resultante.</span><span class="sxs-lookup"><span data-stu-id="e9299-127">The snapshot collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e9299-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9299-128">Requirements</span></span>



| <span data-ttu-id="e9299-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9299-129">Requirement</span></span> | <span data-ttu-id="e9299-130">Valor</span><span class="sxs-lookup"><span data-stu-id="e9299-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9299-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9299-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e9299-132">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e9299-132">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e9299-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9299-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e9299-134">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e9299-134">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e9299-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="e9299-135">Namespace</span></span><br/>                | <span data-ttu-id="e9299-136">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e9299-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e9299-137">MOF</span><span class="sxs-lookup"><span data-stu-id="e9299-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9299-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9299-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9299-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e9299-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9299-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e9299-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e9299-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9299-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9299-142">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="e9299-142">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




