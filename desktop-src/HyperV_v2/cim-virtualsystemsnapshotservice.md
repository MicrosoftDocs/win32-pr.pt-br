---
description: Representa um serviço que pode criar, aplicar e excluir instantâneos de sistemas virtuais.
ms.assetid: 8d5d54a2-08f1-4f24-bca3-601dc698d018
title: Classe CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7ae74f85d1af9867b7a95c23aeda670b8f06f413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837521"
---
# <a name="cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="7f677-103">\_Classe CIM VirtualSystemSnapshotService</span><span class="sxs-lookup"><span data-stu-id="7f677-103">CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="7f677-104">Representa um serviço que pode criar, aplicar e excluir instantâneos de sistemas virtuais.</span><span class="sxs-lookup"><span data-stu-id="7f677-104">Represents a service that can create, apply, and delete snapshots of virtual systems.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f677-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f677-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemSnapshotService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="7f677-106">Membros</span><span class="sxs-lookup"><span data-stu-id="7f677-106">Members</span></span>

<span data-ttu-id="7f677-107">A classe **CIM \_ VirtualSystemSnapshotService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7f677-107">The **CIM\_VirtualSystemSnapshotService** class has these types of members:</span></span>

-   [<span data-ttu-id="7f677-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="7f677-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7f677-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="7f677-109">Methods</span></span>

<span data-ttu-id="7f677-110">A classe **CIM \_ VirtualSystemSnapshotService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="7f677-110">The **CIM\_VirtualSystemSnapshotService** class has these methods.</span></span>



| <span data-ttu-id="7f677-111">Método</span><span class="sxs-lookup"><span data-stu-id="7f677-111">Method</span></span>                                                                      | <span data-ttu-id="7f677-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f677-112">Description</span></span>                                                                                      |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f677-113">**ApplySnapshot**</span><span class="sxs-lookup"><span data-stu-id="7f677-113">**ApplySnapshot**</span></span>](cim-virtualsystemsnapshotservice-applysnapshot.md)     | <span data-ttu-id="7f677-114">Aplica um instantâneo do sistema virtual ao sistema virtual para o sistema virtual de origem.</span><span class="sxs-lookup"><span data-stu-id="7f677-114">Applies a virtual system snapshot to the virtual system to the source virtual system.</span></span><br/> |
| [<span data-ttu-id="7f677-115">**CreateSnapshot**</span><span class="sxs-lookup"><span data-stu-id="7f677-115">**CreateSnapshot**</span></span>](cim-virtualsystemsnapshotservice-createsnapshot.md)   | <span data-ttu-id="7f677-116">Cria um instantâneo de um sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="7f677-116">Creates a snapshot of a virtual system.</span></span><br/>                                               |
| [<span data-ttu-id="7f677-117">**DestroySnapshot**</span><span class="sxs-lookup"><span data-stu-id="7f677-117">**DestroySnapshot**</span></span>](cim-virtualsystemsnapshotservice-destroysnapshot.md) | <span data-ttu-id="7f677-118">Exclui um instantâneo do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="7f677-118">Deletes a virtual system snapshot.</span></span><br/>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="7f677-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f677-119">Requirements</span></span>



| <span data-ttu-id="7f677-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f677-120">Requirement</span></span> | <span data-ttu-id="7f677-121">Valor</span><span class="sxs-lookup"><span data-stu-id="7f677-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f677-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f677-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7f677-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7f677-123">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="7f677-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f677-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7f677-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7f677-125">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="7f677-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="7f677-126">Namespace</span></span><br/>                | <span data-ttu-id="7f677-127">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="7f677-127">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7f677-128">MOF</span><span class="sxs-lookup"><span data-stu-id="7f677-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f677-129"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f677-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f677-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7f677-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f677-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7f677-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7f677-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f677-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f677-133">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="7f677-133">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




