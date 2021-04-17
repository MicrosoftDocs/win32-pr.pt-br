---
description: Modifica as configurações de recursos virtuais.
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
ms.openlocfilehash: e27729429d02c2412e05344779cc40461dbd9dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461220"
---
# <a name="modifyresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="d19e7-103">Método ModifyResourceSettings da \_ classe VIRTUALSYSTEMMANAGEMENTSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="d19e7-103">ModifyResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="d19e7-104">Modifica as configurações de recursos virtuais.</span><span class="sxs-lookup"><span data-stu-id="d19e7-104">Modifies virtual resource settings.</span></span>

<span data-ttu-id="d19e7-105">Quando aplicado a partes de uma configuração de sistema virtual "atual", como os recursos de efeito colateral do sistema virtual ativo podem ser modificados.</span><span class="sxs-lookup"><span data-stu-id="d19e7-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="d19e7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d19e7-106">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d19e7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d19e7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d19e7-108">*ResourceSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d19e7-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d19e7-109">Matriz de cadeias de caracteres que contém uma instância inserida da classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que descreve as modificações nos aspectos virtuais de um recurso virtual existente.</span><span class="sxs-lookup"><span data-stu-id="d19e7-109">Array of strings each containing an embedded instance of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that describes modifications to the virtual aspects of an existing virtual resource.</span></span> <span data-ttu-id="d19e7-110">Todas as instâncias devem ter uma **InstanceId** válida para identificar a configuração de recurso virtual a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="d19e7-110">All instances must have a valid **InstanceID** in order to identify the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="d19e7-111">*ResultingResourceSettings* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d19e7-111">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d19e7-112">Matriz de referências a instâncias da classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representa aspectos virtuais dos recursos virtuais modificados.</span><span class="sxs-lookup"><span data-stu-id="d19e7-112">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="d19e7-113">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="d19e7-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d19e7-114">Se a operação for de longa execução, opcionalmente, um trabalho será retornado.</span><span class="sxs-lookup"><span data-stu-id="d19e7-114">If the operation is long running, then optionally a job be returned.</span></span> <span data-ttu-id="d19e7-115">Nesse caso, as instâncias da classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representa as configurações de recurso modificadas estão disponíveis por meio da **\_ ConreteComponent de CIM** de associação da instância da classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que representa a configuração do sistema virtual afetado.</span><span class="sxs-lookup"><span data-stu-id="d19e7-115">In this case, the instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing the modified resource settings are available via association **CIM\_ConreteComponent** from the instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) representing the affected virtual system configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d19e7-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d19e7-116">Return value</span></span>

<span data-ttu-id="d19e7-117">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="d19e7-117">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="d19e7-118">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="d19e7-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d19e7-119">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="d19e7-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d19e7-120">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="d19e7-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d19e7-121">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="d19e7-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d19e7-122">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="d19e7-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d19e7-123">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="d19e7-123">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d19e7-124">**Parâmetros incompatíveis** (6)</span><span class="sxs-lookup"><span data-stu-id="d19e7-124">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d19e7-125">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d19e7-125">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d19e7-126">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="d19e7-126">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d19e7-127">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="d19e7-127">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="d19e7-128">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="d19e7-128">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d19e7-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d19e7-129">Requirements</span></span>



| <span data-ttu-id="d19e7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d19e7-130">Requirement</span></span> | <span data-ttu-id="d19e7-131">Valor</span><span class="sxs-lookup"><span data-stu-id="d19e7-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d19e7-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d19e7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d19e7-133">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d19e7-133">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="d19e7-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d19e7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d19e7-135">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d19e7-135">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="d19e7-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="d19e7-136">Namespace</span></span><br/>                | <span data-ttu-id="d19e7-137">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d19e7-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d19e7-138">MOF</span><span class="sxs-lookup"><span data-stu-id="d19e7-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d19e7-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d19e7-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d19e7-140">DLL</span><span class="sxs-lookup"><span data-stu-id="d19e7-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d19e7-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d19e7-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d19e7-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="d19e7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d19e7-143">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="d19e7-143">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




