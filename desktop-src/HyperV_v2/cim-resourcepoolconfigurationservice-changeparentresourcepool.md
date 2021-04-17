---
description: Inicie um trabalho para alterar um pool pai usando as configurações de alocação especificadas.
ms.assetid: 2eea1a60-fbf0-49a7-8f79-52c62c295316
title: Método ChangeParentResourcePool da classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.ChangeParentResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6ef852d6af8f0973b6b3f29fca5fcd90e9ce726a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789810"
---
# <a name="changeparentresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="26a99-103">Método ChangeParentResourcePool da \_ classe RESOURCEPOOLCONFIGURATIONSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="26a99-103">ChangeParentResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="26a99-104">Inicie um trabalho para alterar um pool pai usando as configurações de alocação especificadas.</span><span class="sxs-lookup"><span data-stu-id="26a99-104">Start a job to change a parent pool using the specified allocation settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="26a99-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26a99-105">Syntax</span></span>


```mof
uint32 ChangeParentResourcePool(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  CIM_ResourcePool REF ParentPool[],
  [in]  string               Settings[],
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="26a99-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26a99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26a99-107">*ChildPool* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="26a99-107">*ChildPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26a99-108">Um [**\_ ResourcePool CIM**](cim-resourcepool.md) que faz referência ao pool filho.</span><span class="sxs-lookup"><span data-stu-id="26a99-108">A [**CIM\_ResourcePool**](cim-resourcepool.md) that references the child pool.</span></span>

</dd> <dt>

<span data-ttu-id="26a99-109">*ParentPool* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="26a99-109">*ParentPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26a99-110">Uma [**matriz \_ ResourcePool do CIM**](cim-resourcepool.md) que faz referência ao pool (s) pai.</span><span class="sxs-lookup"><span data-stu-id="26a99-110">A [**CIM\_ResourcePool**](cim-resourcepool.md) array that references the parent pool(s).</span></span>

</dd> <dt>

<span data-ttu-id="26a99-111">*Configurações* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="26a99-111">*Settings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26a99-112">Cadeia de caracteres opcional que contém uma representação de uma instância do [**CIM \_ SettingData**](cim-settingdata.md) que é usada para especificar as configurações para o pool pai.</span><span class="sxs-lookup"><span data-stu-id="26a99-112">Optional string containing a representation of a [**CIM\_SettingData**](cim-settingdata.md) instance that is used to specify the settings for the parent pool.</span></span>

</dd> <dt>

<span data-ttu-id="26a99-113">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="26a99-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26a99-114">Um [**\_ ConcreteJob CIM**](cim-concretejob.md) que referencia o trabalho (pode ser **nulo** se o trabalho for concluído).</span><span class="sxs-lookup"><span data-stu-id="26a99-114">A [**CIM\_ConcreteJob**](cim-concretejob.md) that references the job (may be **null** if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26a99-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="26a99-115">Return value</span></span>

<span data-ttu-id="26a99-116">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="26a99-116">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="26a99-117">**Trabalho concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="26a99-117">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="26a99-118">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="26a99-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="26a99-119">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="26a99-119">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="26a99-120">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="26a99-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="26a99-121">**Com falha** (4)</span><span class="sxs-lookup"><span data-stu-id="26a99-121">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="26a99-122">**Parâmetro inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="26a99-122">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="26a99-123">**Em uso** (6)</span><span class="sxs-lookup"><span data-stu-id="26a99-123">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="26a99-124">**ResourceType incorreto para o pool** (7)</span><span class="sxs-lookup"><span data-stu-id="26a99-124">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="26a99-125">**Recursos insuficientes** (8)</span><span class="sxs-lookup"><span data-stu-id="26a99-125">**Insufficient Resources** (8)</span></span>
</dt> <dt>

<span data-ttu-id="26a99-126">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="26a99-126">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="26a99-127">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="26a99-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="26a99-128">**Tamanho sem suporte** (4097)</span><span class="sxs-lookup"><span data-stu-id="26a99-128">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="26a99-129">**Método reservado** (4098.. 32767)</span><span class="sxs-lookup"><span data-stu-id="26a99-129">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="26a99-130">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="26a99-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="26a99-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26a99-131">Requirements</span></span>



| <span data-ttu-id="26a99-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="26a99-132">Requirement</span></span> | <span data-ttu-id="26a99-133">Valor</span><span class="sxs-lookup"><span data-stu-id="26a99-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26a99-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26a99-134">Minimum supported client</span></span><br/> | <span data-ttu-id="26a99-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="26a99-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="26a99-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26a99-136">Minimum supported server</span></span><br/> | <span data-ttu-id="26a99-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="26a99-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="26a99-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="26a99-138">Namespace</span></span><br/>                | <span data-ttu-id="26a99-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="26a99-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="26a99-140">MOF</span><span class="sxs-lookup"><span data-stu-id="26a99-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26a99-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26a99-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="26a99-142">DLL</span><span class="sxs-lookup"><span data-stu-id="26a99-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26a99-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="26a99-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="26a99-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="26a99-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26a99-145">**\_RESOURCEPOOLCONFIGURATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="26a99-145">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




