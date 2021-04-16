---
description: Aplica um instantâneo do sistema virtual ao sistema virtual do qual ele foi criado.
ms.assetid: acd90ce0-7f82-48d9-9d23-903ba6815779
title: Método ApplySnapshot da classe CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 252f7d7d9a57b439ac00fa663fa0a0e816ebada0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758804"
---
# <a name="applysnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="5bf24-103">Método ApplySnapshot da \_ classe VIRTUALSYSTEMSNAPSHOTSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="5bf24-103">ApplySnapshot method of the CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="5bf24-104">Aplica um instantâneo do sistema virtual ao sistema virtual do qual ele foi criado.</span><span class="sxs-lookup"><span data-stu-id="5bf24-104">Applies a virtual system snapshot to the virtual system that it was created from.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bf24-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5bf24-105">Syntax</span></span>


```mof
uint32 ApplySnapshot(
  [in]  CIM_VirtualSystemSettingData REF Snapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="5bf24-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5bf24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bf24-107">*Instantâneo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5bf24-107">*Snapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bf24-108">Uma referência do [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) ao instantâneo do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="5bf24-108">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="5bf24-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="5bf24-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bf24-110">Se a operação for de longa execução, opcionalmente, [**um \_ ConcreteJob CIM**](cim-concretejob.md) que representa o trabalho poderá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="5bf24-110">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

> [!Note]  
> <span data-ttu-id="5bf24-111">Este parâmetro foi leitura/gravação em Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="5bf24-111">This parameter was read/write in Windows 8.1.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bf24-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5bf24-112">Return value</span></span>

<span data-ttu-id="5bf24-113">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="5bf24-113">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="5bf24-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="5bf24-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5bf24-115">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="5bf24-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5bf24-116">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="5bf24-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5bf24-117">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="5bf24-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5bf24-118">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="5bf24-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5bf24-119">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="5bf24-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5bf24-120">**Tipo inválido** (6)</span><span class="sxs-lookup"><span data-stu-id="5bf24-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="5bf24-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="5bf24-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5bf24-122">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="5bf24-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5bf24-123">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="5bf24-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="5bf24-124">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="5bf24-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5bf24-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bf24-125">Requirements</span></span>



| <span data-ttu-id="5bf24-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bf24-126">Requirement</span></span> | <span data-ttu-id="5bf24-127">Valor</span><span class="sxs-lookup"><span data-stu-id="5bf24-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bf24-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bf24-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5bf24-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5bf24-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="5bf24-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bf24-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5bf24-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5bf24-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="5bf24-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="5bf24-132">Namespace</span></span><br/>                | <span data-ttu-id="5bf24-133">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="5bf24-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5bf24-134">MOF</span><span class="sxs-lookup"><span data-stu-id="5bf24-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5bf24-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5bf24-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5bf24-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5bf24-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bf24-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5bf24-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5bf24-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="5bf24-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bf24-139">**\_VIRTUALSYSTEMSNAPSHOTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="5bf24-139">**CIM\_VirtualSystemSnapshotService**</span></span>](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




