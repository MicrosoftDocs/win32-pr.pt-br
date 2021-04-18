---
description: Exclui um pool de recursos.
ms.assetid: bc3111a4-9687-49ec-890e-190358230c53
title: Método DeletePool da classe Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.DeletePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 84273daa0aa30dca8722d90d4fcec22b88325bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755111"
---
# <a name="deletepool-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="0805c-103">Método DeletePool da \_ classe ResourcePoolConfigurationService Msvm</span><span class="sxs-lookup"><span data-stu-id="0805c-103">DeletePool method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="0805c-104">Exclui um pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="0805c-104">Deletes a resource pool.</span></span> <span data-ttu-id="0805c-105">Para excluir um pool de recursos com êxito, nenhuma alocação pode ser pendente ou a exclusão falhará com 32774 (em uso).</span><span class="sxs-lookup"><span data-stu-id="0805c-105">To successfully delete a resource pool, no allocations can be outstanding or the delete will fail with 32774 (In Use).</span></span> <span data-ttu-id="0805c-106">Se o pool de recursos for um pool de recursos raiz, todos os recursos do host serão retornados para o sistema subjacente.</span><span class="sxs-lookup"><span data-stu-id="0805c-106">If the resource pool is a root resource pool, any host resources are returned back to the underlying system.</span></span>

## <a name="syntax"></a><span data-ttu-id="0805c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0805c-107">Syntax</span></span>


```mof
uint32 DeletePool(
  [in]  CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0805c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0805c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0805c-109">*Pool* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="0805c-109">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0805c-110">Uma referência a uma instância da classe [**CIM \_ ResourcePool**](cim-resourcepool.md) que representa o pool a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="0805c-110">A reference to an instance of the [**CIM\_ResourcePool**](cim-resourcepool.md) class that represents the pool to delete.</span></span>

</dd> <dt>

<span data-ttu-id="0805c-111">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="0805c-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0805c-112">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0805c-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0805c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0805c-113">Return value</span></span>

<span data-ttu-id="0805c-114">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="0805c-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0805c-115">**Trabalho concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="0805c-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0805c-116">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0805c-116">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0805c-117">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="0805c-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0805c-118">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="0805c-118">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="0805c-119">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="0805c-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="0805c-120">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="0805c-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="0805c-121">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="0805c-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="0805c-122">**Desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="0805c-122">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="0805c-123">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="0805c-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="0805c-124">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="0805c-124">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="0805c-125">**Em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="0805c-125">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="0805c-126">**Estado inválido** (32775)</span><span class="sxs-lookup"><span data-stu-id="0805c-126">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="0805c-127">**Tipo de recurso incorreto para o pool** (32776)</span><span class="sxs-lookup"><span data-stu-id="0805c-127">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="0805c-128">**Não disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="0805c-128">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="0805c-129">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="0805c-129">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="0805c-130">**Fornecedor reservado** (32779)</span><span class="sxs-lookup"><span data-stu-id="0805c-130">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="0805c-131">**Recursos insuficientes** (32780)</span><span class="sxs-lookup"><span data-stu-id="0805c-131">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="0805c-132">**Objeto não encontrado** (32781.. 32787)</span><span class="sxs-lookup"><span data-stu-id="0805c-132">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="0805c-133">O **objeto existe** (32788)</span><span class="sxs-lookup"><span data-stu-id="0805c-133">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="0805c-134">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0805c-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0805c-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0805c-135">Requirements</span></span>



| <span data-ttu-id="0805c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="0805c-136">Requirement</span></span> | <span data-ttu-id="0805c-137">Valor</span><span class="sxs-lookup"><span data-stu-id="0805c-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0805c-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0805c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="0805c-139">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0805c-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0805c-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0805c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="0805c-141">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0805c-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0805c-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="0805c-142">Namespace</span></span><br/>                | <span data-ttu-id="0805c-143">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="0805c-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0805c-144">MOF</span><span class="sxs-lookup"><span data-stu-id="0805c-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0805c-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0805c-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0805c-146">DLL</span><span class="sxs-lookup"><span data-stu-id="0805c-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0805c-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0805c-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0805c-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="0805c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0805c-149">**Msvm \_ ResourcePoolConfigurationService**</span><span class="sxs-lookup"><span data-stu-id="0805c-149">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

