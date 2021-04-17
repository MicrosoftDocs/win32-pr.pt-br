---
description: Inicie um trabalho para criar um subpool de um pool pai usando as configurações de alocação especificadas.
ms.assetid: 9b09221a-7c4e-4648-a2a8-012df1818c3e
title: Método CreateChildResourcePool da classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateChildResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e4e709fd240c849581f6dcd343001a9b1dee7003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755114"
---
# <a name="createchildresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="14f84-103">Método CreateChildResourcePool da \_ classe RESOURCEPOOLCONFIGURATIONSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="14f84-103">CreateChildResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="14f84-104">Inicie um trabalho para criar um subpool de um pool pai usando as configurações de alocação especificadas.</span><span class="sxs-lookup"><span data-stu-id="14f84-104">Start a job to create a sub-pool from a parent pool using the specified allocation settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="14f84-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14f84-105">Syntax</span></span>


```mof
uint32 CreateChildResourcePool(
  [in]  string               ElementName,
  [in]  string               Settings[],
  [in]  CIM_ResourcePool REF ParentPool[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="14f84-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14f84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14f84-107">*ElementName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14f84-107">*ElementName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14f84-108">Um nome relevante do usuário final para o pool que está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="14f84-108">A end user relevant name for the pool being created.</span></span> <span data-ttu-id="14f84-109">Se for **NULL**, um nome padrão fornecido pelo sistema poderá ser usado.</span><span class="sxs-lookup"><span data-stu-id="14f84-109">If **NULL**, then a system supplied default name can be used.</span></span> <span data-ttu-id="14f84-110">O valor será armazenado na propriedade **ElementName** do elemento criado.</span><span class="sxs-lookup"><span data-stu-id="14f84-110">The value will be stored in the **ElementName** property for the created element.</span></span>

</dd> <dt>

<span data-ttu-id="14f84-111">*Configurações* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="14f84-111">*Settings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14f84-112">Cadeia de caracteres que contém uma representação de uma instância de [**CIM \_ SettingData**](cim-settingdata.md) que é usada para especificar as configurações para o pool filho.</span><span class="sxs-lookup"><span data-stu-id="14f84-112">String containing a representation of a [**CIM\_SettingData**](cim-settingdata.md) instance that is used to specify the settings for the child Pool.</span></span>

</dd> <dt>

<span data-ttu-id="14f84-113">*ParentPool* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14f84-113">*ParentPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14f84-114">Um [**\_ ResourcePool CIM**](cim-resourcepool.md) do qual criar o novo pool.</span><span class="sxs-lookup"><span data-stu-id="14f84-114">A [**CIM\_ResourcePool**](cim-resourcepool.md) from which to create the new Pool.</span></span>

</dd> <dt>

<span data-ttu-id="14f84-115">*Pool* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="14f84-115">*Pool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14f84-116">Um [**\_ ResourcePool CIM**](cim-resourcepool.md) que faz referência ao pool resultante.</span><span class="sxs-lookup"><span data-stu-id="14f84-116">A [**CIM\_ResourcePool**](cim-resourcepool.md) that references the resulting pool.</span></span>

</dd> <dt>

<span data-ttu-id="14f84-117">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="14f84-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14f84-118">Referência ao trabalho (pode ser NULL se o trabalho for concluído).</span><span class="sxs-lookup"><span data-stu-id="14f84-118">Reference to the job (may be null if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14f84-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="14f84-119">Return value</span></span>

<span data-ttu-id="14f84-120">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="14f84-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="14f84-121">**Trabalho concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="14f84-121">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="14f84-122">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="14f84-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="14f84-123">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="14f84-123">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="14f84-124">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="14f84-124">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="14f84-125">**Com falha** (4)</span><span class="sxs-lookup"><span data-stu-id="14f84-125">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="14f84-126">**Parâmetro inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="14f84-126">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="14f84-127">**Em uso** (6)</span><span class="sxs-lookup"><span data-stu-id="14f84-127">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="14f84-128">**ResourceType incorreto para o pool** (7)</span><span class="sxs-lookup"><span data-stu-id="14f84-128">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="14f84-129">**Recursos insuficientes** (8)</span><span class="sxs-lookup"><span data-stu-id="14f84-129">**Insufficient Resources** (8)</span></span>
</dt> <dt>

<span data-ttu-id="14f84-130">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="14f84-130">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="14f84-131">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="14f84-131">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="14f84-132">**Tamanho sem suporte** (4097)</span><span class="sxs-lookup"><span data-stu-id="14f84-132">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="14f84-133">**Método reservado** (4098.. 32767)</span><span class="sxs-lookup"><span data-stu-id="14f84-133">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="14f84-134">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="14f84-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="14f84-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14f84-135">Requirements</span></span>



| <span data-ttu-id="14f84-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="14f84-136">Requirement</span></span> | <span data-ttu-id="14f84-137">Valor</span><span class="sxs-lookup"><span data-stu-id="14f84-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14f84-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14f84-138">Minimum supported client</span></span><br/> | <span data-ttu-id="14f84-139">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="14f84-139">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="14f84-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14f84-140">Minimum supported server</span></span><br/> | <span data-ttu-id="14f84-141">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="14f84-141">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="14f84-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="14f84-142">Namespace</span></span><br/>                | <span data-ttu-id="14f84-143">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="14f84-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="14f84-144">MOF</span><span class="sxs-lookup"><span data-stu-id="14f84-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14f84-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="14f84-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="14f84-146">DLL</span><span class="sxs-lookup"><span data-stu-id="14f84-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14f84-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="14f84-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="14f84-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="14f84-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14f84-149">**\_RESOURCEPOOLCONFIGURATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="14f84-149">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




