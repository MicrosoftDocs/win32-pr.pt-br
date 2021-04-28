---
description: Método ModifyResourceSettings da classe CIM_VirtualSystemManagementService-modifica as configurações de recurso virtual.
ms.assetid: 4942f167-0e53-4ae2-b973-4a06b636b44a
title: Método ModifyResourceSettings da classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 26971c80ce6f7d0ffcdcef069d76aef5fdc15138
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112284"
---
# <a name="modifyresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="79d8d-103">Método ModifyResourceSettings da \_ classe VIRTUALSYSTEMMANAGEMENTSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="79d8d-103">ModifyResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="79d8d-104">Modifica as configurações de recursos virtuais.</span><span class="sxs-lookup"><span data-stu-id="79d8d-104">Modifies virtual resource settings.</span></span>

<span data-ttu-id="79d8d-105">Quando aplicado a partes de uma configuração de sistema virtual "atual", como os recursos de efeito colateral do sistema virtual ativo podem ser modificados.</span><span class="sxs-lookup"><span data-stu-id="79d8d-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="79d8d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79d8d-106">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="79d8d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79d8d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79d8d-108">*ResourceSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="79d8d-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79d8d-109">Matriz de cadeias de caracteres que contém uma instância inserida da classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que descreve as modificações nos aspectos virtuais de um recurso virtual existente.</span><span class="sxs-lookup"><span data-stu-id="79d8d-109">Array of strings each containing an embedded instance of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that describes modifications to the virtual aspects of an existing virtual resource.</span></span> <span data-ttu-id="79d8d-110">Todas as instâncias devem ter uma **InstanceId** válida para identificar a configuração de recurso virtual a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="79d8d-110">All instances must have a valid **InstanceID** in order to identify the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="79d8d-111">*ResultingResourceSettings* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="79d8d-111">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79d8d-112">Matriz de referências a instâncias da classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representa aspectos virtuais dos recursos virtuais modificados.</span><span class="sxs-lookup"><span data-stu-id="79d8d-112">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="79d8d-113">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="79d8d-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79d8d-114">Se a operação for de longa execução, opcionalmente, um trabalho será retornado.</span><span class="sxs-lookup"><span data-stu-id="79d8d-114">If the operation is long running, then optionally a job be returned.</span></span> <span data-ttu-id="79d8d-115">Nesse caso, as instâncias da classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representa as configurações de recurso modificadas estão disponíveis por meio da **\_ ConreteComponent de CIM** de associação da instância da classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que representa a configuração do sistema virtual afetado.</span><span class="sxs-lookup"><span data-stu-id="79d8d-115">In this case, the instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing the modified resource settings are available via association **CIM\_ConreteComponent** from the instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) representing the affected virtual system configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79d8d-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="79d8d-116">Return value</span></span>

<span data-ttu-id="79d8d-117">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="79d8d-117">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="79d8d-118">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="79d8d-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="79d8d-119">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="79d8d-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="79d8d-120">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="79d8d-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="79d8d-121">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="79d8d-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="79d8d-122">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="79d8d-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="79d8d-123">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="79d8d-123">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="79d8d-124">**Parâmetros incompatíveis** (6)</span><span class="sxs-lookup"><span data-stu-id="79d8d-124">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="79d8d-125">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="79d8d-125">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="79d8d-126">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="79d8d-126">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="79d8d-127">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="79d8d-127">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="79d8d-128">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="79d8d-128">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="79d8d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79d8d-129">Requirements</span></span>



| <span data-ttu-id="79d8d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="79d8d-130">Requirement</span></span> | <span data-ttu-id="79d8d-131">Valor</span><span class="sxs-lookup"><span data-stu-id="79d8d-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79d8d-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79d8d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="79d8d-133">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="79d8d-133">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="79d8d-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79d8d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="79d8d-135">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="79d8d-135">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="79d8d-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="79d8d-136">Namespace</span></span><br/>                | <span data-ttu-id="79d8d-137">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="79d8d-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="79d8d-138">MOF</span><span class="sxs-lookup"><span data-stu-id="79d8d-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79d8d-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79d8d-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="79d8d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="79d8d-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79d8d-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="79d8d-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="79d8d-142">Consulte também</span><span class="sxs-lookup"><span data-stu-id="79d8d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79d8d-143">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="79d8d-143">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




