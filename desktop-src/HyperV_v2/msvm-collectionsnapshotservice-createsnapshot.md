---
description: Cria um instantâneo de uma coleção de sistemas virtuais.
ms.assetid: 2512d82f-06b9-4613-b920-d3a9be884a75
title: Método createsnapshot da classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 653dae65cc5fe50416b069da6a66e8c678c1b512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661795"
---
# <a name="createsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="fc958-103">Método createsnapshot da classe Msvm \_ CollectionSnapshotService</span><span class="sxs-lookup"><span data-stu-id="fc958-103">CreateSnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="fc958-104">Cria um instantâneo de uma coleção de sistemas virtuais.</span><span class="sxs-lookup"><span data-stu-id="fc958-104">Creates a snapshot of a virtual system collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc958-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc958-105">Syntax</span></span>


```mof
uint32 CreateSnapshot(
  [in]      CIM_CollectionOfMSEs REF Collection,
  [in]      string                   SnapshotSettings,
  [in]      uint16                   SnapshotType,
  [in, out] CIM_Collection       REF ResultingSnapshotCollection,
  [out]     CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="fc958-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc958-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc958-107">*Coleção* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="fc958-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc958-108">Referência a um [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) que descreve a coleção de sistema virtual afetada.</span><span class="sxs-lookup"><span data-stu-id="fc958-108">Reference to a [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) that describes the affected virtual system collection.</span></span>

</dd> <dt>

<span data-ttu-id="fc958-109">*SnapshotSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fc958-109">*SnapshotSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc958-110">Contém as configurações de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fc958-110">Contains the parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="fc958-111">*Instantâneotype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fc958-111">*SnapshotType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc958-112">Tipo de instantâneo solicitado:</span><span class="sxs-lookup"><span data-stu-id="fc958-112">Requested snapshot type:</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fc958-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="fc958-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>

<span data-ttu-id="fc958-114"><span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>**Instantâneo padrão** (1)</span><span class="sxs-lookup"><span data-stu-id="fc958-114"><span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>**Standard Snapshot** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fc958-115">Instantâneo padrão do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="fc958-115">Standard snapshot of the virtual system.</span></span>

</dd> <dt>

<span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>

<span data-ttu-id="fc958-116"><span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>**Instantâneo de recuperação** (2)</span><span class="sxs-lookup"><span data-stu-id="fc958-116"><span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>**Recovery Snapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fc958-117">Instantâneo para cenários de recuperação, incluindo replicação de failover e backup.</span><span class="sxs-lookup"><span data-stu-id="fc958-117">Snapshot for recovery scenarios including failover replication and backup.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="fc958-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="fc958-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="fc958-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="fc958-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="fc958-120">*ResultingSnapshotCollection* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="fc958-120">*ResultingSnapshotCollection* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc958-121">Em caso de sucesso, retorna uma referência de [**\_ coleção CIM**](cim-collection.md) que contém o instantâneo do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="fc958-121">On success, returns a [**CIM\_Collection**](cim-collection.md) reference containing the virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="fc958-122">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="fc958-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc958-123">Uma referência opcional que será retornada se a operação for executada de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="fc958-123">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="fc958-124">Se estiver presente, a referência retornada a uma instância de [**CIM \_ ConcreteJob**](cim-concretejob.md) poderá ser usada para monitorar o progresso e obter o resultado do método.</span><span class="sxs-lookup"><span data-stu-id="fc958-124">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc958-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fc958-125">Return value</span></span>

<span data-ttu-id="fc958-126">Em caso de sucesso, retorna 0 (completo) ou 4096 (trabalho iniciado); caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="fc958-126">On success, returns either 0 (Complete) or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="fc958-127">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="fc958-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fc958-128">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="fc958-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fc958-129">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="fc958-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fc958-130">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="fc958-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fc958-131">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="fc958-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fc958-132">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="fc958-132">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fc958-133">**Tipo inválido** (6)</span><span class="sxs-lookup"><span data-stu-id="fc958-133">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="fc958-134">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="fc958-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fc958-135">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="fc958-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fc958-136">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="fc958-136">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="fc958-137">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="fc958-137">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fc958-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc958-138">Requirements</span></span>



| <span data-ttu-id="fc958-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc958-139">Requirement</span></span> | <span data-ttu-id="fc958-140">Valor</span><span class="sxs-lookup"><span data-stu-id="fc958-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc958-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc958-141">Minimum supported client</span></span><br/> | <span data-ttu-id="fc958-142">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="fc958-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="fc958-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc958-143">Minimum supported server</span></span><br/> | <span data-ttu-id="fc958-144">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fc958-144">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="fc958-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="fc958-145">Namespace</span></span><br/>                | <span data-ttu-id="fc958-146">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="fc958-146">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fc958-147">MOF</span><span class="sxs-lookup"><span data-stu-id="fc958-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc958-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc958-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc958-149">DLL</span><span class="sxs-lookup"><span data-stu-id="fc958-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc958-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fc958-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fc958-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc958-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc958-152">**Msvm \_ CollectionSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="fc958-152">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




