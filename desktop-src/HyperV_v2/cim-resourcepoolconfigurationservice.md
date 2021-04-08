---
description: Gerencia a configuração de pools de recursos usando trabalhos.
ms.assetid: cc0f0236-2335-4dd9-9132-51b3e6b9fcf4
title: Classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e8dbbce21f7749b7f436e2f49acb7ce6c7340faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827262"
---
# <a name="cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="81edf-103">\_Classe CIM ResourcePoolConfigurationService</span><span class="sxs-lookup"><span data-stu-id="81edf-103">CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="81edf-104">Gerencia a configuração de pools de recursos usando trabalhos.</span><span class="sxs-lookup"><span data-stu-id="81edf-104">Manages the configuration of resource pools by using jobs.</span></span>

## <a name="syntax"></a><span data-ttu-id="81edf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81edf-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_ResourcePoolConfigurationService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="81edf-106">Membros</span><span class="sxs-lookup"><span data-stu-id="81edf-106">Members</span></span>

<span data-ttu-id="81edf-107">A classe **CIM \_ ResourcePoolConfigurationService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="81edf-107">The **CIM\_ResourcePoolConfigurationService** class has these types of members:</span></span>

-   [<span data-ttu-id="81edf-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="81edf-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="81edf-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="81edf-109">Methods</span></span>

<span data-ttu-id="81edf-110">A classe **CIM \_ ResourcePoolConfigurationService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="81edf-110">The **CIM\_ResourcePoolConfigurationService** class has these methods.</span></span>



| <span data-ttu-id="81edf-111">Método</span><span class="sxs-lookup"><span data-stu-id="81edf-111">Method</span></span>                                                                                                          | <span data-ttu-id="81edf-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="81edf-112">Description</span></span>                                                                   |
|:----------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="81edf-113">**AddResourcesToResourcePool**</span><span class="sxs-lookup"><span data-stu-id="81edf-113">**AddResourcesToResourcePool**</span></span>](cim-resourcepoolconfigurationservice-addresourcestoresourcepool.md)           | <span data-ttu-id="81edf-114">Inicia um trabalho para adicionar recursos a um pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="81edf-114">Starts a job to add resources to a resource pool.</span></span><br/>                  |
| [<span data-ttu-id="81edf-115">**ChangeParentResourcePool**</span><span class="sxs-lookup"><span data-stu-id="81edf-115">**ChangeParentResourcePool**</span></span>](cim-resourcepoolconfigurationservice-changeparentresourcepool.md)               | <span data-ttu-id="81edf-116">Inicie um trabalho para alterar o pool de recursos pai de um pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="81edf-116">Start a job to change the parent resource pool of a resource pool.</span></span><br/> |
| [<span data-ttu-id="81edf-117">**CreateChildResourcePool**</span><span class="sxs-lookup"><span data-stu-id="81edf-117">**CreateChildResourcePool**</span></span>](cim-resourcepoolconfigurationservice-createchildresourcepool.md)                 | <span data-ttu-id="81edf-118">Inicie um trabalho para criar um pool de recursos de um pool de recursos pai.</span><span class="sxs-lookup"><span data-stu-id="81edf-118">Start a job to create a resource pool from a parent resource pool.</span></span><br/> |
| [<span data-ttu-id="81edf-119">**CreateResourcePool**</span><span class="sxs-lookup"><span data-stu-id="81edf-119">**CreateResourcePool**</span></span>](cim-resourcepoolconfigurationservice-createresourcepool.md)                           | <span data-ttu-id="81edf-120">Inicia um trabalho para criar um pool de recursos raiz.</span><span class="sxs-lookup"><span data-stu-id="81edf-120">Starts a job to create a root resource pool.</span></span><br/>                       |
| [<span data-ttu-id="81edf-121">**DeleteResourcePool**</span><span class="sxs-lookup"><span data-stu-id="81edf-121">**DeleteResourcePool**</span></span>](cim-resourcepoolconfigurationservice-deleteresourcepool.md)                           | <span data-ttu-id="81edf-122">Inicie um trabalho para excluir um pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="81edf-122">Start a job to delete a resource pool.</span></span><br/>                             |
| [<span data-ttu-id="81edf-123">**RemoveResourcesFromResourcePool**</span><span class="sxs-lookup"><span data-stu-id="81edf-123">**RemoveResourcesFromResourcePool**</span></span>](cim-resourcepoolconfigurationservice-removeresourcesfromresourcepool.md) | <span data-ttu-id="81edf-124">Inicia um trabalho para remover recursos de um pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="81edf-124">Starts a job to remove resources from a resource pool.</span></span><br/>             |



 

## <a name="requirements"></a><span data-ttu-id="81edf-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81edf-125">Requirements</span></span>



| <span data-ttu-id="81edf-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="81edf-126">Requirement</span></span> | <span data-ttu-id="81edf-127">Valor</span><span class="sxs-lookup"><span data-stu-id="81edf-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81edf-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81edf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="81edf-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="81edf-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="81edf-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81edf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="81edf-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="81edf-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="81edf-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="81edf-132">Namespace</span></span><br/>                | <span data-ttu-id="81edf-133">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="81edf-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="81edf-134">MOF</span><span class="sxs-lookup"><span data-stu-id="81edf-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81edf-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81edf-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="81edf-136">DLL</span><span class="sxs-lookup"><span data-stu-id="81edf-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81edf-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="81edf-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="81edf-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="81edf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81edf-139">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="81edf-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




