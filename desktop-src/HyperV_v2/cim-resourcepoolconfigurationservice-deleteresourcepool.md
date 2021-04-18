---
description: Inicie um trabalho para excluir um pool de recursos.
ms.assetid: af3d9c7c-a825-4568-822d-044b3d92d144
title: Método DeleteResourcePool da classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.DeleteResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9cab27df07a6a3a9679cb5e6595b6ba558d8b05e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770414"
---
# <a name="deleteresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="44a87-103">Método DeleteResourcePool da \_ classe RESOURCEPOOLCONFIGURATIONSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="44a87-103">DeleteResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="44a87-104">Inicie um trabalho para excluir um pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="44a87-104">Start a job to delete a resource pool.</span></span> <span data-ttu-id="44a87-105">Nenhuma alocação pode estar pendente ou a exclusão falhará com "em uso".</span><span class="sxs-lookup"><span data-stu-id="44a87-105">No allocations may be outstanding or the delete will fail with "In Use."</span></span> <span data-ttu-id="44a87-106">Se o pool de recursos for um pool de recursos raiz, todos os recursos do host serão retornados para o sistema subjacente.</span><span class="sxs-lookup"><span data-stu-id="44a87-106">If the resource pool is a root resource pool, any host resources are returned back to the underlying system.</span></span>

## <a name="syntax"></a><span data-ttu-id="44a87-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44a87-107">Syntax</span></span>


```mof
uint32 DeleteResourcePool(
  [in]  CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="44a87-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44a87-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44a87-109">*Pool* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="44a87-109">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44a87-110">Um [**\_ ResourcePool CIM**](cim-resourcepool.md) que faz referência ao pool a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="44a87-110">A [**CIM\_ResourcePool**](cim-resourcepool.md) that references to the pool to delete.</span></span>

</dd> <dt>

<span data-ttu-id="44a87-111">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="44a87-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44a87-112">Um [**\_ ConcreteJob CIM**](cim-concretejob.md) que referencia o trabalho (pode ser **nulo** se o trabalho for concluído).</span><span class="sxs-lookup"><span data-stu-id="44a87-112">A [**CIM\_ConcreteJob**](cim-concretejob.md) that references the job (may be **null** if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44a87-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="44a87-113">Return value</span></span>

<span data-ttu-id="44a87-114">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="44a87-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="44a87-115">**Trabalho concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="44a87-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="44a87-116">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="44a87-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="44a87-117">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="44a87-117">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="44a87-118">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="44a87-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="44a87-119">**Com falha** (4)</span><span class="sxs-lookup"><span data-stu-id="44a87-119">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="44a87-120">**Parâmetro inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="44a87-120">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="44a87-121">**Em uso** (6)</span><span class="sxs-lookup"><span data-stu-id="44a87-121">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="44a87-122">**ResourceType incorreto para o pool** (7)</span><span class="sxs-lookup"><span data-stu-id="44a87-122">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="44a87-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="44a87-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="44a87-124">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="44a87-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="44a87-125">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="44a87-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="44a87-126">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="44a87-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="44a87-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44a87-127">Requirements</span></span>



| <span data-ttu-id="44a87-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="44a87-128">Requirement</span></span> | <span data-ttu-id="44a87-129">Valor</span><span class="sxs-lookup"><span data-stu-id="44a87-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44a87-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44a87-130">Minimum supported client</span></span><br/> | <span data-ttu-id="44a87-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="44a87-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="44a87-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44a87-132">Minimum supported server</span></span><br/> | <span data-ttu-id="44a87-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="44a87-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="44a87-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="44a87-134">Namespace</span></span><br/>                | <span data-ttu-id="44a87-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="44a87-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="44a87-136">MOF</span><span class="sxs-lookup"><span data-stu-id="44a87-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44a87-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44a87-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="44a87-138">DLL</span><span class="sxs-lookup"><span data-stu-id="44a87-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44a87-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="44a87-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="44a87-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="44a87-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44a87-141">**\_RESOURCEPOOLCONFIGURATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="44a87-141">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




