---
description: Método RemoveResourceSettings da classe CIM_VirtualSystemManagementService-remove as configurações de recurso virtual de uma configuração de sistema virtual.
ms.assetid: 7934a5e4-f54c-43fd-9ec3-d1fc1aad0acd
title: Método RemoveResourceSettings da classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e5c7daabcdcd732c3a5693664e1768ebf66668d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112254"
---
# <a name="removeresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="6720f-103">Método RemoveResourceSettings da \_ classe VIRTUALSYSTEMMANAGEMENTSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="6720f-103">RemoveResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="6720f-104">Remove as configurações de recursos virtuais de uma configuração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="6720f-104">Removes virtual resource settings from a virtual system configuration.</span></span>

<span data-ttu-id="6720f-105">Quando aplicado a partes de uma configuração de sistema virtual "atual", como os recursos de efeito colateral do sistema virtual ativo podem ser removidos.</span><span class="sxs-lookup"><span data-stu-id="6720f-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="6720f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6720f-106">Syntax</span></span>


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6720f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6720f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6720f-108">*ResourceSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6720f-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6720f-109">Matriz de referências a instâncias da classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) em que cada instância representa as configurações de um recurso virtual em uma configuração de sistema virtual que devem ser removidas.</span><span class="sxs-lookup"><span data-stu-id="6720f-109">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) where each instance represents the settings of a virtual resource within a virtual system configuration that are to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="6720f-110">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="6720f-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6720f-111">Se a operação for de longa execução, opcionalmente, [**um \_ ConcreteJob CIM**](cim-concretejob.md) que representa o trabalho poderá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="6720f-111">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6720f-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6720f-112">Return value</span></span>

<span data-ttu-id="6720f-113">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="6720f-113">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="6720f-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="6720f-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6720f-115">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="6720f-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6720f-116">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="6720f-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6720f-117">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="6720f-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6720f-118">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="6720f-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6720f-119">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="6720f-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6720f-120">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="6720f-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6720f-121">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="6720f-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6720f-122">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="6720f-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="6720f-123">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="6720f-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6720f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6720f-124">Requirements</span></span>



| <span data-ttu-id="6720f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6720f-125">Requirement</span></span> | <span data-ttu-id="6720f-126">Valor</span><span class="sxs-lookup"><span data-stu-id="6720f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6720f-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6720f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6720f-128">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6720f-128">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="6720f-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6720f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6720f-130">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6720f-130">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="6720f-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="6720f-131">Namespace</span></span><br/>                | <span data-ttu-id="6720f-132">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="6720f-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6720f-133">MOF</span><span class="sxs-lookup"><span data-stu-id="6720f-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6720f-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6720f-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6720f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6720f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6720f-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6720f-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6720f-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6720f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6720f-138">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="6720f-138">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




