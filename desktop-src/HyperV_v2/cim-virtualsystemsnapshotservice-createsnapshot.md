---
description: Cria um instantâneo de um sistema virtual.
ms.assetid: cad4cb4f-523f-4fda-ac88-8cece7abc227
title: Método createsnapshot da classe CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ee96098477501123cffc1fd59a52734bbbea35d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756768"
---
# <a name="createsnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="14012-103">Método createsnapshot da classe CIM \_ VirtualSystemSnapshotService</span><span class="sxs-lookup"><span data-stu-id="14012-103">CreateSnapshot method of the CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="14012-104">Cria um instantâneo de um sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="14012-104">Creates a snapshot of a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="14012-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14012-105">Syntax</span></span>


```mof
uint32 CreateSnapshot(
  [in]      CIM_ComputerSystem           REF AffectedSystem,
  [in]      string                           SnapshotSettings,
  [in]      uint16                           SnapshotType,
  [in, out] CIM_VirtualSystemSettingData REF ResultingSnapshot,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="14012-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14012-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14012-107">*AffectedSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14012-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14012-108">Uma referência de [**\_ ComputerSystem de CIM**](cim-computersystem.md) para o sistema virtual afetado.</span><span class="sxs-lookup"><span data-stu-id="14012-108">A [**CIM\_ComputerSystem**](cim-computersystem.md) reference to the affected virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="14012-109">*SnapshotSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14012-109">*SnapshotSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14012-110">Configurações de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="14012-110">Parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="14012-111">*Instantâneotype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14012-111">*SnapshotType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14012-112">Tipo de instantâneo solicitado:</span><span class="sxs-lookup"><span data-stu-id="14012-112">Requested snapshot type:</span></span>

<dt>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>

<span data-ttu-id="14012-113"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Instantâneo completo** (2)</span><span class="sxs-lookup"><span data-stu-id="14012-113"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Full Snapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="14012-114">Instantâneo completo do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="14012-114">Complete snapshot of the virtual system.</span></span>

</dd> <dt>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>

<span data-ttu-id="14012-115"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Instantâneo do disco** (3)</span><span class="sxs-lookup"><span data-stu-id="14012-115"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Disk Snapshot** (3)</span></span>


</dt> <dd>

<span data-ttu-id="14012-116">Instantâneo dos discos do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="14012-116">Snapshot of virtual system disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="14012-117"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="14012-117"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="14012-118"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="14012-118"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="14012-119">*ResultingSnapshot* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="14012-119">*ResultingSnapshot* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="14012-120">Uma referência do [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) ao instantâneo do sistema virtual resultante.</span><span class="sxs-lookup"><span data-stu-id="14012-120">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the resulting virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="14012-121">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="14012-121">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14012-122">Se a operação for de longa execução, opcionalmente, um trabalho poderá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="14012-122">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="14012-123">Nesse caso, a instância da classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que representa o novo instantâneo do sistema virtual é apresentada por meio da Associação [**\_ AffectedJobElement do CIM**](cim-affectedjobelement.md) com o valor **da propriedade** que se refere à nova instância da classe **CIM \_ VirtualSystemSettingData** que representa o instantâneo do sistema virtual e o valor do **ElementEffects** definido como 5 (criar).</span><span class="sxs-lookup"><span data-stu-id="14012-123">In this case, the instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing the new virtual system snapshot is presented via the [**CIM\_AffectedJobElement**](cim-affectedjobelement.md) association with the value of the **AffectedElement** property referring to the new instance of the **CIM\_VirtualSystemSettingData** class representing the virtual system snapshot and the value of the **ElementEffects** set to 5 (Create).</span></span>

> [!Note]  
> <span data-ttu-id="14012-124">Este parâmetro foi leitura/gravação em Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="14012-124">This parameter was read/write in Windows 8.1.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14012-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="14012-125">Return value</span></span>

<span data-ttu-id="14012-126">Em caso de sucesso, retorna 0; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="14012-126">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="14012-127">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="14012-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="14012-128">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="14012-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="14012-129">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="14012-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="14012-130">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="14012-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="14012-131">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="14012-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="14012-132">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="14012-132">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="14012-133">**Tipo inválido** (6)</span><span class="sxs-lookup"><span data-stu-id="14012-133">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="14012-134">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="14012-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="14012-135">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="14012-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="14012-136">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="14012-136">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="14012-137">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="14012-137">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="14012-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14012-138">Requirements</span></span>



| <span data-ttu-id="14012-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="14012-139">Requirement</span></span> | <span data-ttu-id="14012-140">Valor</span><span class="sxs-lookup"><span data-stu-id="14012-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14012-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14012-141">Minimum supported client</span></span><br/> | <span data-ttu-id="14012-142">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="14012-142">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="14012-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14012-143">Minimum supported server</span></span><br/> | <span data-ttu-id="14012-144">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="14012-144">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="14012-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="14012-145">Namespace</span></span><br/>                | <span data-ttu-id="14012-146">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="14012-146">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="14012-147">MOF</span><span class="sxs-lookup"><span data-stu-id="14012-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14012-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="14012-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="14012-149">DLL</span><span class="sxs-lookup"><span data-stu-id="14012-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14012-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="14012-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="14012-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="14012-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14012-152">**\_VIRTUALSYSTEMSNAPSHOTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="14012-152">**CIM\_VirtualSystemSnapshotService**</span></span>](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




