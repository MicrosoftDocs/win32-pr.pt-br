---
description: Inicia um trabalho para remover recursos de um pool de recursos.
ms.assetid: 1689ccbf-a524-45b7-bf95-6341a3b28f6c
title: Método RemoveResourcesFromResourcePool da classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.RemoveResourcesFromResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 41c8a7d1608b9c4d5ea629aa9c053e022d59d9ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501899"
---
# <a name="removeresourcesfromresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="a2094-103">Método RemoveResourcesFromResourcePool da \_ classe RESOURCEPOOLCONFIGURATIONSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="a2094-103">RemoveResourcesFromResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="a2094-104">Inicia um trabalho para remover recursos de um pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="a2094-104">Starts a job to remove resources from a resource pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2094-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2094-105">Syntax</span></span>


```mof
uint32 RemoveResourcesFromResourcePool(
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a2094-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2094-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2094-107">*Recursos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a2094-107">*HostResources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2094-108">Matriz de instâncias de [**\_ LogicalDevice CIM**](cim-logicaldevice.md) a serem removidas do pool.</span><span class="sxs-lookup"><span data-stu-id="a2094-108">Array of [**CIM\_LogicalDevice**](cim-logicaldevice.md) instances to remove from the pool.</span></span>

</dd> <dt>

<span data-ttu-id="a2094-109">*Pool* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="a2094-109">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2094-110">Um [**\_ ResourcePool CIM**](cim-resourcepool.md) que representa o pool do qual remover os recursos.</span><span class="sxs-lookup"><span data-stu-id="a2094-110">A [**CIM\_ResourcePool**](cim-resourcepool.md) representing the pool to remove the resources from.</span></span>

</dd> <dt>

<span data-ttu-id="a2094-111">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="a2094-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2094-112">Um [**\_ ConcreteJob CIM**](cim-concretejob.md) que referencia o trabalho (pode ser **nulo** se o trabalho for concluído).</span><span class="sxs-lookup"><span data-stu-id="a2094-112">A [**CIM\_ConcreteJob**](cim-concretejob.md) that references the job (may be **null** if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2094-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a2094-113">Return value</span></span>

<span data-ttu-id="a2094-114">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="a2094-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="a2094-115">**Trabalho concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="a2094-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a2094-116">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="a2094-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a2094-117">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="a2094-117">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a2094-118">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="a2094-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a2094-119">**Com falha** (4)</span><span class="sxs-lookup"><span data-stu-id="a2094-119">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a2094-120">**Parâmetro inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="a2094-120">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a2094-121">**Em uso** (6)</span><span class="sxs-lookup"><span data-stu-id="a2094-121">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a2094-122">**ResourceType incorreto para o pool** (7)</span><span class="sxs-lookup"><span data-stu-id="a2094-122">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="a2094-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a2094-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a2094-124">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="a2094-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a2094-125">**Tamanho sem suporte** (4097)</span><span class="sxs-lookup"><span data-stu-id="a2094-125">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="a2094-126">**Método reservado** (4098.. 32767)</span><span class="sxs-lookup"><span data-stu-id="a2094-126">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="a2094-127">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="a2094-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a2094-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2094-128">Requirements</span></span>



| <span data-ttu-id="a2094-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2094-129">Requirement</span></span> | <span data-ttu-id="a2094-130">Valor</span><span class="sxs-lookup"><span data-stu-id="a2094-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2094-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2094-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a2094-132">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a2094-132">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="a2094-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2094-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a2094-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a2094-134">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="a2094-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="a2094-135">Namespace</span></span><br/>                | <span data-ttu-id="a2094-136">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="a2094-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a2094-137">MOF</span><span class="sxs-lookup"><span data-stu-id="a2094-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2094-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2094-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2094-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a2094-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2094-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a2094-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a2094-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2094-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2094-142">**\_RESOURCEPOOLCONFIGURATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="a2094-142">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




