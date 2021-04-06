---
description: Inicia um trabalho para criar um ResourcePool raiz. O ResourcePool será definido como escopo para o mesmo sistema que esse serviço.
ms.assetid: 357880dc-125a-452c-89f5-44cd17684436
title: Método CreateResourcePool da classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ca339eb2e2a4ec0fb441c5ed1a657608d71248bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647336"
---
# <a name="createresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="78521-104">Método CreateResourcePool da \_ classe RESOURCEPOOLCONFIGURATIONSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="78521-104">CreateResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="78521-105">Inicia um trabalho para criar um ResourcePool raiz.</span><span class="sxs-lookup"><span data-stu-id="78521-105">Starts a job to create a root ResourcePool.</span></span> <span data-ttu-id="78521-106">O ResourcePool será definido como escopo para o mesmo sistema que esse serviço.</span><span class="sxs-lookup"><span data-stu-id="78521-106">The ResourcePool will be scoped to the same System as this Service.</span></span>

## <a name="syntax"></a><span data-ttu-id="78521-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78521-107">Syntax</span></span>


```mof
uint32 CreateResourcePool(
  [in]  string                ElementName,
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  string                ResourceType,
  [out] CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="78521-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78521-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78521-109">*ElementName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78521-109">*ElementName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78521-110">Um nome relevante do usuário final para o pool que está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="78521-110">A end user relevant name for the pool being created.</span></span> <span data-ttu-id="78521-111">Se for **NULL**, um nome padrão fornecido pelo sistema poderá ser usado.</span><span class="sxs-lookup"><span data-stu-id="78521-111">If **NULL**, then a system supplied default name can be used.</span></span> <span data-ttu-id="78521-112">O valor será armazenado na propriedade **ElementName** do pool criado.</span><span class="sxs-lookup"><span data-stu-id="78521-112">The value will be stored in the **ElementName** property for the created pool.</span></span>

</dd> <dt>

<span data-ttu-id="78521-113">*Recursos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78521-113">*HostResources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78521-114">Matriz de zero ou mais dispositivos [**CIM \_ LogicalDevice**](cim-logicaldevice.md) que são usados para criar o pool ou modificar as extensões de origem.</span><span class="sxs-lookup"><span data-stu-id="78521-114">Array of zero or more [**CIM\_LogicalDevice**](cim-logicaldevice.md) devices that are used to create the Pool or modify the source extents.</span></span> <span data-ttu-id="78521-115">Todos os elementos na matriz devem ser do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="78521-115">All elements in the array must be of the same type.</span></span>

</dd> <dt>

<span data-ttu-id="78521-116">*ResourceType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78521-116">*ResourceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78521-117">O tipo de recursos que o pool criado irá gerenciar.</span><span class="sxs-lookup"><span data-stu-id="78521-117">The type of resources the created pool will manage.</span></span> <span data-ttu-id="78521-118">Se *recursos* contiver elementos, essa propriedade deverá Mach seu tipo.</span><span class="sxs-lookup"><span data-stu-id="78521-118">If *HostResources* contains elements, this property must mach their type.</span></span>

</dd> <dt>

<span data-ttu-id="78521-119">*Pool* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="78521-119">*Pool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78521-120">Em caso de sucesso, retorna uma referência para [**o \_ ResourcePool CIM**](cim-resourcepool.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="78521-120">On success, returns a reference to the resulting [**CIM\_ResourcePool**](cim-resourcepool.md).</span></span> <span data-ttu-id="78521-121">Quando um trabalho é retornado, isso pode ser **nulo**; nesse caso, o cliente deve usar o trabalho para localizar o ResourcePool resultante quando o trabalho for concluído.</span><span class="sxs-lookup"><span data-stu-id="78521-121">When a Job is returned, this may be **NULL**, in which case, the client must use the Job to find the resulting ResourcePool once the Job completes.</span></span>

</dd> <dt>

<span data-ttu-id="78521-122">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="78521-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78521-123">Referência a um [**\_ ConcreteJob CIM**](cim-concretejob.md) que representa o trabalho (pode ser NULL se o trabalho for concluído).</span><span class="sxs-lookup"><span data-stu-id="78521-123">Reference to a [**CIM\_ConcreteJob**](cim-concretejob.md) that represents the job (may be null if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78521-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="78521-124">Return value</span></span>

<span data-ttu-id="78521-125">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="78521-125">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="78521-126">**Trabalho concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="78521-126">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="78521-127">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="78521-127">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="78521-128">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="78521-128">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="78521-129">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="78521-129">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="78521-130">**Com falha** (4)</span><span class="sxs-lookup"><span data-stu-id="78521-130">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="78521-131">**Parâmetro inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="78521-131">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="78521-132">**Em uso** (6)</span><span class="sxs-lookup"><span data-stu-id="78521-132">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="78521-133">**ResourceType incorreto para o pool** (7)</span><span class="sxs-lookup"><span data-stu-id="78521-133">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="78521-134">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="78521-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="78521-135">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="78521-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="78521-136">**Tamanho sem suporte** (4097)</span><span class="sxs-lookup"><span data-stu-id="78521-136">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="78521-137">**Método reservado** (4098.. 32767)</span><span class="sxs-lookup"><span data-stu-id="78521-137">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="78521-138">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="78521-138">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="78521-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78521-139">Requirements</span></span>



| <span data-ttu-id="78521-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="78521-140">Requirement</span></span> | <span data-ttu-id="78521-141">Valor</span><span class="sxs-lookup"><span data-stu-id="78521-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78521-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78521-142">Minimum supported client</span></span><br/> | <span data-ttu-id="78521-143">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="78521-143">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="78521-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78521-144">Minimum supported server</span></span><br/> | <span data-ttu-id="78521-145">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="78521-145">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="78521-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="78521-146">Namespace</span></span><br/>                | <span data-ttu-id="78521-147">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="78521-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="78521-148">MOF</span><span class="sxs-lookup"><span data-stu-id="78521-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78521-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="78521-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="78521-150">DLL</span><span class="sxs-lookup"><span data-stu-id="78521-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78521-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="78521-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="78521-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="78521-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78521-153">**\_RESOURCEPOOLCONFIGURATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="78521-153">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




