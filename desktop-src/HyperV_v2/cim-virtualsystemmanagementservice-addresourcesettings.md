---
description: Adiciona recursos a uma configuração de sistema virtual.
ms.assetid: c2541571-74f0-48f8-997c-56c152980eea
title: Método AddResourceSettings da classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9563b1e8421dfa6724971450b117780435f6f39e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789807"
---
# <a name="addresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="8191c-103">Método AddResourceSettings da \_ classe VIRTUALSYSTEMMANAGEMENTSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="8191c-103">AddResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="8191c-104">Adiciona recursos a uma configuração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="8191c-104">Adds resources to a virtual system configuration.</span></span>

<span data-ttu-id="8191c-105">Quando aplicado a uma configuração de sistema virtual "State", como os recursos de efeito colateral são adicionados ao sistema virtual ativo.</span><span class="sxs-lookup"><span data-stu-id="8191c-105">When applied to a "state" virtual system configuration, as a side effect resources are added to the active virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="8191c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8191c-106">Syntax</span></span>


```mof
uint32 AddResourceSettings(
  [in]  CIM_VirtualSystemSettingData      REF AffectedConfiguration,
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8191c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8191c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8191c-108">*AffectedConfiguration* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8191c-108">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8191c-109">Uma referência do [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) à configuração do sistema virtual afetada.</span><span class="sxs-lookup"><span data-stu-id="8191c-109">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the affected virtual system configuration.</span></span>

</dd> <dt>

<span data-ttu-id="8191c-110">*ResourceSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8191c-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8191c-111">Matriz de cadeias de caracteres que contém uma instância inserida da classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que descreve os aspectos virtuais de um recurso virtual a ser adicionado ao sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="8191c-111">Array of strings each containing one embedded instance of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that describes the virtual aspects of a virtual resource to be added to the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="8191c-112">*ResultingResourceSettings* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8191c-112">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8191c-113">Matriz de referências a instâncias da classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representa aspectos virtuais dos recursos virtuais adicionados.</span><span class="sxs-lookup"><span data-stu-id="8191c-113">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing virtual aspects of the added virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="8191c-114">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="8191c-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8191c-115">Se a operação for de longa execução, opcionalmente, um trabalho poderá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="8191c-115">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="8191c-116">Nesse caso, as instâncias da classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representa as configurações de recurso adicionadas estão disponíveis por meio da **\_ ConreteComponent de CIM** de associação da instância da classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que representa a configuração do sistema virtual afetado.</span><span class="sxs-lookup"><span data-stu-id="8191c-116">In this case, the instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing the added resource settings are available via association **CIM\_ConreteComponent** from the instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) representing the affected virtual system configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8191c-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8191c-117">Return value</span></span>

<span data-ttu-id="8191c-118">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="8191c-118">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="8191c-119">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="8191c-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8191c-120">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="8191c-120">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8191c-121">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="8191c-121">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8191c-122">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="8191c-122">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8191c-123">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="8191c-123">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8191c-124">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="8191c-124">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8191c-125">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="8191c-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8191c-126">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="8191c-126">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="8191c-127">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="8191c-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8191c-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8191c-128">Requirements</span></span>



| <span data-ttu-id="8191c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8191c-129">Requirement</span></span> | <span data-ttu-id="8191c-130">Valor</span><span class="sxs-lookup"><span data-stu-id="8191c-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8191c-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8191c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8191c-132">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8191c-132">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="8191c-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8191c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8191c-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8191c-134">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="8191c-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="8191c-135">Namespace</span></span><br/>                | <span data-ttu-id="8191c-136">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="8191c-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8191c-137">MOF</span><span class="sxs-lookup"><span data-stu-id="8191c-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8191c-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8191c-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8191c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="8191c-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8191c-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8191c-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8191c-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="8191c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8191c-142">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="8191c-142">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




