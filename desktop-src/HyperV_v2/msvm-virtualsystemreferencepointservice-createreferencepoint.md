---
description: Cria um ponto de referência de um sistema virtual.
ms.assetid: 9cc7665a-9562-4267-bcd0-3162e426fbad
title: Método CreateReferencePoint da classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.CreateReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 08d28970288ba62346894d758ebac5ac156962ff
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105753139"
---
# <a name="createreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="1aaa1-103">Método CreateReferencePoint da \_ classe VirtualSystemReferencePointService Msvm</span><span class="sxs-lookup"><span data-stu-id="1aaa1-103">CreateReferencePoint method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="1aaa1-104">Cria um ponto de referência de um sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="1aaa1-104">Creates a reference point of a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="1aaa1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1aaa1-105">Syntax</span></span>


```mof
uint32 CreateReferencePoint(
  [in]      Msvm_ComputerSystem              REF AffectedSystem,
  [in]      string                               ReferencePointSettings,
  [in]      uint16                               ReferencePointType,
  [in, out] Msvm_VirtualSystemReferencePoint REF ResultingReferencePoint,
  [out]     CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="1aaa1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1aaa1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1aaa1-107">*AffectedSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1aaa1-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1aaa1-108">Um [**\_ ComputerSystem Msvm**](msvm-computersystem.md) que faz referência ao sistema virtual afetado.</span><span class="sxs-lookup"><span data-stu-id="1aaa1-108">A [**Msvm\_ComputerSystem**](msvm-computersystem.md) that references the affected virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="1aaa1-109">*ReferencePointSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1aaa1-109">*ReferencePointSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1aaa1-110">Contém as configurações de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1aaa1-110">Contains the parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="1aaa1-111">*ReferencePointType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1aaa1-111">*ReferencePointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1aaa1-112">Tipo de ponto de referência solicitado:</span><span class="sxs-lookup"><span data-stu-id="1aaa1-112">Requested reference point type:</span></span>

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="1aaa1-113"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Baseado em log** (0)</span><span class="sxs-lookup"><span data-stu-id="1aaa1-113"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1aaa1-114">Com base no rastreamento de log de réplica do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="1aaa1-114">Based on Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="1aaa1-115"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**Baseado em RCT** (1)</span><span class="sxs-lookup"><span data-stu-id="1aaa1-115"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1aaa1-116">Com base em Controle de Alterações resilientes de discos virtuais.</span><span class="sxs-lookup"><span data-stu-id="1aaa1-116">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1aaa1-117">*ResultingReferencePoint* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="1aaa1-117">*ResultingReferencePoint* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1aaa1-118">Ponto de referência do sistema virtual resultante</span><span class="sxs-lookup"><span data-stu-id="1aaa1-118">Resulting virtual system reference point</span></span>

</dd> <dt>

<span data-ttu-id="1aaa1-119">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="1aaa1-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1aaa1-120">Se a operação for de longa execução, opcionalmente, um trabalho poderá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="1aaa1-120">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="1aaa1-121">Nesse caso, a instância da classe [**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) que representa o novo ponto de referência do sistema virtual é apresentada por meio da Associação de [**\_ AffectedJobElement do CIM**](cim-affectedjobelement.md) com o valor da propriedade **afetou** que se refere à nova instância da classe **Msvm \_ VirtualSystemReferencePoint** que representa o ponto de referência do sistema virtual e o valor do **ElementEffects** definido como 5 (criar).</span><span class="sxs-lookup"><span data-stu-id="1aaa1-121">In this case, the instance of the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) class representing the new virtual system reference point is presented via the [**CIM\_AffectedJobElement**](cim-affectedjobelement.md) association with the value of the **AffectedElement** property referring to the new instance of the **Msvm\_VirtualSystemReferencePoint** class representing the virtual system reference point and the value of the **ElementEffects** set to 5 (Create).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1aaa1-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1aaa1-122">Return value</span></span>

<span data-ttu-id="1aaa1-123">Em caso de sucesso, retorna 0; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="1aaa1-123">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="1aaa1-124">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="1aaa1-124">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1aaa1-125">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="1aaa1-125">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1aaa1-126">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="1aaa1-126">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1aaa1-127">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="1aaa1-127">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1aaa1-128">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="1aaa1-128">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1aaa1-129">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="1aaa1-129">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1aaa1-130">**Tipo inválido** (6)</span><span class="sxs-lookup"><span data-stu-id="1aaa1-130">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1aaa1-131">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1aaa1-131">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1aaa1-132">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="1aaa1-132">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1aaa1-133">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="1aaa1-133">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="1aaa1-134">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="1aaa1-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1aaa1-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1aaa1-135">Requirements</span></span>



| <span data-ttu-id="1aaa1-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="1aaa1-136">Requirement</span></span> | <span data-ttu-id="1aaa1-137">Valor</span><span class="sxs-lookup"><span data-stu-id="1aaa1-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1aaa1-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1aaa1-138">Minimum supported client</span></span><br/> | <span data-ttu-id="1aaa1-139">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1aaa1-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="1aaa1-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1aaa1-140">Minimum supported server</span></span><br/> | <span data-ttu-id="1aaa1-141">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1aaa1-141">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="1aaa1-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="1aaa1-142">Namespace</span></span><br/>                | <span data-ttu-id="1aaa1-143">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="1aaa1-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1aaa1-144">MOF</span><span class="sxs-lookup"><span data-stu-id="1aaa1-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1aaa1-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1aaa1-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1aaa1-146">DLL</span><span class="sxs-lookup"><span data-stu-id="1aaa1-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1aaa1-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1aaa1-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1aaa1-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="1aaa1-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aaa1-149">**Msvm \_ VirtualSystemReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="1aaa1-149">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




