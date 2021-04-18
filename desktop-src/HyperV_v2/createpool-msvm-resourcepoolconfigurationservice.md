---
description: Cria um pool de recursos filho.
ms.assetid: 30a70231-f1b7-4f0e-ac47-cf5a79ddb8ab
title: Método createpool da classe Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.CreatePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fb29a4b5a47d88232a6b0df6a828d482030b3f1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778596"
---
# <a name="createpool-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="8a1d6-103">Método createpool da classe Msvm \_ ResourcePoolConfigurationService</span><span class="sxs-lookup"><span data-stu-id="8a1d6-103">CreatePool method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="8a1d6-104">Cria um pool de recursos filho.</span><span class="sxs-lookup"><span data-stu-id="8a1d6-104">Creates a child resource pool.</span></span> <span data-ttu-id="8a1d6-105">O pool de recursos será definido como escopo para o mesmo sistema que esse serviço.</span><span class="sxs-lookup"><span data-stu-id="8a1d6-105">The resource pool will be scoped to the same System as this Service.</span></span> <span data-ttu-id="8a1d6-106">O pool resultante será um pool filho.</span><span class="sxs-lookup"><span data-stu-id="8a1d6-106">The resulting pool will be a child pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a1d6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a1d6-107">Syntax</span></span>


```mof
uint32 CreatePool(
  [in]  string               PoolSettings,
  [in]  CIM_ResourcePool REF ParentPools[],
  [in]  string               AllocationSettings[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8a1d6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a1d6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a1d6-109">*PoolSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8a1d6-109">*PoolSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a1d6-110">Uma instância inserida da classe [**Msvm \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) que é usada para especificar as configurações de pool que não estão relacionadas à alocação.</span><span class="sxs-lookup"><span data-stu-id="8a1d6-110">An embedded instance of the [**Msvm\_ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) class that is used to specify the pool settings that are not allocation related.</span></span>

</dd> <dt>

<span data-ttu-id="8a1d6-111">*ParentPools* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8a1d6-111">*ParentPools* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a1d6-112">Uma matriz de referências de [**Msvm \_ ResourcePool**](msvm-resourcepool.md) que representam o pool ou pools dos quais criar o novo pool.</span><span class="sxs-lookup"><span data-stu-id="8a1d6-112">An array of [**Msvm\_ResourcePool**](msvm-resourcepool.md) references that represent the pool or pools from which to create the new pool.</span></span>

</dd> <dt>

<span data-ttu-id="8a1d6-113">*AllocationSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8a1d6-113">*AllocationSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a1d6-114">Uma matriz de uma ou mais instâncias inseridas da classe [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) que são usadas para especificar as configurações relacionadas à alocação de pool.</span><span class="sxs-lookup"><span data-stu-id="8a1d6-114">An array of one or more embedded instances of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that are used to specify the pool allocation related settings.</span></span> <span data-ttu-id="8a1d6-115">Essa matriz deve conter um elemento para cada elemento na matriz *ParentPools* ou exatamente um elemento.</span><span class="sxs-lookup"><span data-stu-id="8a1d6-115">This array must contain either one element for each element in the *ParentPools* array, or exactly one element.</span></span> <span data-ttu-id="8a1d6-116">Se essa matriz contiver um elemento e *ParentPools* contiver mais de um elemento, *AlllocationSettings* especificará uma alocação de capacidade compartilhada que pode ser satisfeita por qualquer um dos pools pai.</span><span class="sxs-lookup"><span data-stu-id="8a1d6-116">If this array contains one element and *ParentPools* contains more than one element, *AlllocationSettings* specifies a shared capacity allocation that can be satisfied by any of the parent pools.</span></span>

<span data-ttu-id="8a1d6-117">Isso é usado para restringir os recursos que podem ser alocados do filho para o pool a um limite inferior à capacidade agregada fornecida por seus pais.</span><span class="sxs-lookup"><span data-stu-id="8a1d6-117">This is used to restrict the resources that can be allocated from the child to the pool to a lower limit than the aggregate capacity provided by its parents.</span></span> <span data-ttu-id="8a1d6-118">Não há suporte para essa opção em todos os tipos de recurso.</span><span class="sxs-lookup"><span data-stu-id="8a1d6-118">This option is not supported by all resource types.</span></span> <span data-ttu-id="8a1d6-119">Se um tipo de recurso não for compatível com a alocação de capacidade compartilhada, esse método retornará 32770 (sem suporte).</span><span class="sxs-lookup"><span data-stu-id="8a1d6-119">If a resource type does not support shared capacity allocation, this method will return 32770 (Not Supported).</span></span>

</dd> <dt>

<span data-ttu-id="8a1d6-120">*Pool* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="8a1d6-120">*Pool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a1d6-121">Uma referência ao pool resultante.</span><span class="sxs-lookup"><span data-stu-id="8a1d6-121">A reference to the resulting pool.</span></span>

</dd> <dt>

<span data-ttu-id="8a1d6-122">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="8a1d6-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a1d6-123">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8a1d6-123">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a1d6-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8a1d6-124">Return value</span></span>

<span data-ttu-id="8a1d6-125">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8a1d6-125">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="8a1d6-126">**Trabalho concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="8a1d6-126">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8a1d6-127">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="8a1d6-127">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8a1d6-128">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="8a1d6-128">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8a1d6-129">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="8a1d6-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="8a1d6-130">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="8a1d6-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="8a1d6-131">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="8a1d6-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="8a1d6-132">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="8a1d6-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="8a1d6-133">**Desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="8a1d6-133">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="8a1d6-134">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="8a1d6-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="8a1d6-135">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="8a1d6-135">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="8a1d6-136">**Em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="8a1d6-136">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="8a1d6-137">**Estado inválido** (32775)</span><span class="sxs-lookup"><span data-stu-id="8a1d6-137">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="8a1d6-138">**Tipo de recurso incorreto para o pool** (32776)</span><span class="sxs-lookup"><span data-stu-id="8a1d6-138">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="8a1d6-139">**Não disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="8a1d6-139">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="8a1d6-140">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="8a1d6-140">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="8a1d6-141">**Fornecedor reservado** (32779)</span><span class="sxs-lookup"><span data-stu-id="8a1d6-141">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="8a1d6-142">**Recursos insuficientes** (32780)</span><span class="sxs-lookup"><span data-stu-id="8a1d6-142">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="8a1d6-143">**Objeto não encontrado** (32781.. 32787)</span><span class="sxs-lookup"><span data-stu-id="8a1d6-143">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="8a1d6-144">O **objeto existe** (32788)</span><span class="sxs-lookup"><span data-stu-id="8a1d6-144">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="8a1d6-145">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="8a1d6-145">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8a1d6-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a1d6-146">Requirements</span></span>



| <span data-ttu-id="8a1d6-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a1d6-147">Requirement</span></span> | <span data-ttu-id="8a1d6-148">Valor</span><span class="sxs-lookup"><span data-stu-id="8a1d6-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a1d6-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a1d6-149">Minimum supported client</span></span><br/> | <span data-ttu-id="8a1d6-150">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8a1d6-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8a1d6-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a1d6-151">Minimum supported server</span></span><br/> | <span data-ttu-id="8a1d6-152">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8a1d6-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8a1d6-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="8a1d6-153">Namespace</span></span><br/>                | <span data-ttu-id="8a1d6-154">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="8a1d6-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8a1d6-155">MOF</span><span class="sxs-lookup"><span data-stu-id="8a1d6-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a1d6-156"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a1d6-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a1d6-157">DLL</span><span class="sxs-lookup"><span data-stu-id="8a1d6-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a1d6-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8a1d6-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8a1d6-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a1d6-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a1d6-160">**Msvm \_ ResourcePoolConfigurationService**</span><span class="sxs-lookup"><span data-stu-id="8a1d6-160">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

