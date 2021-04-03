---
description: Altera as configurações de recurso de pool pai para recursos atribuídos a um pool filho.
ms.assetid: 419fca70-5f15-4593-80ac-ef2af2c3dde5
title: Método ModifyPoolResources da classe Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.ModifyPoolResources
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2efffdbcc34577f675556874c4153eea2670768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829365"
---
# <a name="modifypoolresources-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="69d81-103">Método ModifyPoolResources da \_ classe ResourcePoolConfigurationService Msvm</span><span class="sxs-lookup"><span data-stu-id="69d81-103">ModifyPoolResources method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="69d81-104">Altera as configurações de recurso de pool pai para recursos atribuídos a um pool filho.</span><span class="sxs-lookup"><span data-stu-id="69d81-104">Changes the parent pool resource settings for resources assigned to a child pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="69d81-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69d81-105">Syntax</span></span>


```mof
uint32 ModifyPoolResources(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  CIM_ResourcePool REF ParentPools[],
  [in]  string               AllocationSettings[],
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="69d81-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69d81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69d81-107">*ChildPool* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="69d81-107">*ChildPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69d81-108">Uma referência a uma instância da classe [**CIM \_ ResourcePool**](cim-resourcepool.md) que representa o pool filho a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="69d81-108">A reference to an instance of the [**CIM\_ResourcePool**](cim-resourcepool.md) class that represents the child pool to modify.</span></span>

</dd> <dt>

<span data-ttu-id="69d81-109">*ParentPools* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="69d81-109">*ParentPools* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69d81-110">Uma matriz de referências do [**CIM \_ ResourcePool**](cim-resourcepool.md) que representam os novos pools pai a serem atribuídos ao pool filho.</span><span class="sxs-lookup"><span data-stu-id="69d81-110">An array of [**CIM\_ResourcePool**](cim-resourcepool.md) references that represent the new parent pools to assign to the child pool.</span></span>

</dd> <dt>

<span data-ttu-id="69d81-111">*AllocationSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="69d81-111">*AllocationSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69d81-112">Uma matriz opcional de uma ou mais instâncias inseridas da classe [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) que são usadas para especificar as configurações relacionadas à alocação de pool.</span><span class="sxs-lookup"><span data-stu-id="69d81-112">An optional array of one or more embedded instances of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that are used to specify the pool allocation related settings.</span></span>

</dd> <dt>

<span data-ttu-id="69d81-113">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="69d81-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69d81-114">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="69d81-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69d81-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="69d81-115">Return value</span></span>

<span data-ttu-id="69d81-116">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="69d81-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="69d81-117">**Trabalho concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="69d81-117">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="69d81-118">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="69d81-118">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="69d81-119">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="69d81-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="69d81-120">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="69d81-120">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="69d81-121">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="69d81-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="69d81-122">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="69d81-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="69d81-123">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="69d81-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="69d81-124">**Desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="69d81-124">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="69d81-125">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="69d81-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="69d81-126">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="69d81-126">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="69d81-127">**Em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="69d81-127">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="69d81-128">**Estado inválido** (32775)</span><span class="sxs-lookup"><span data-stu-id="69d81-128">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="69d81-129">**Tipo de recurso incorreto para o pool** (32776)</span><span class="sxs-lookup"><span data-stu-id="69d81-129">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="69d81-130">**Não disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="69d81-130">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="69d81-131">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="69d81-131">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="69d81-132">**Fornecedor reservado** (32779)</span><span class="sxs-lookup"><span data-stu-id="69d81-132">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="69d81-133">**Recursos insuficientes** (32780)</span><span class="sxs-lookup"><span data-stu-id="69d81-133">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="69d81-134">**Objeto não encontrado** (32781.. 32787)</span><span class="sxs-lookup"><span data-stu-id="69d81-134">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="69d81-135">O **objeto existe** (32788)</span><span class="sxs-lookup"><span data-stu-id="69d81-135">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="69d81-136">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="69d81-136">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="69d81-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69d81-137">Requirements</span></span>



| <span data-ttu-id="69d81-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="69d81-138">Requirement</span></span> | <span data-ttu-id="69d81-139">Valor</span><span class="sxs-lookup"><span data-stu-id="69d81-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69d81-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69d81-140">Minimum supported client</span></span><br/> | <span data-ttu-id="69d81-141">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="69d81-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="69d81-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69d81-142">Minimum supported server</span></span><br/> | <span data-ttu-id="69d81-143">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="69d81-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="69d81-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="69d81-144">Namespace</span></span><br/>                | <span data-ttu-id="69d81-145">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="69d81-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="69d81-146">MOF</span><span class="sxs-lookup"><span data-stu-id="69d81-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69d81-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="69d81-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="69d81-148">DLL</span><span class="sxs-lookup"><span data-stu-id="69d81-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69d81-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="69d81-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="69d81-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="69d81-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69d81-151">**Msvm \_ ResourcePoolConfigurationService**</span><span class="sxs-lookup"><span data-stu-id="69d81-151">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

