---
description: Converta um instantâneo de coleção existente em uma coleção de pontos de referência. A coleção de instantâneos é excluída como um efeito colateral. Somente instantâneos de recuperação podem ser convertidos em pontos de referência.
ms.assetid: 6b304782-9e5e-43b1-af7d-08617d65850c
title: Método ConvertToReferencePoint da classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ConvertToReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 810761b67303ad33ced6fdaef857c96f65365091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837422"
---
# <a name="converttoreferencepoint-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="44678-105">Método ConvertToReferencePoint da \_ classe CollectionSnapshotService Msvm</span><span class="sxs-lookup"><span data-stu-id="44678-105">ConvertToReferencePoint method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="44678-106">Converta um instantâneo de coleção existente em uma coleção de pontos de referência.</span><span class="sxs-lookup"><span data-stu-id="44678-106">Convert an existing collection snapshot to a reference point collection.</span></span> <span data-ttu-id="44678-107">A coleção de instantâneos é excluída como um efeito colateral.</span><span class="sxs-lookup"><span data-stu-id="44678-107">The snapshot collection gets deleted as a side effect.</span></span> <span data-ttu-id="44678-108">Somente instantâneos de recuperação podem ser convertidos em pontos de referência.</span><span class="sxs-lookup"><span data-stu-id="44678-108">Only recovery snapshots can be converted to reference points.</span></span>

## <a name="syntax"></a><span data-ttu-id="44678-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44678-109">Syntax</span></span>


```mof
uint32 ConvertToReferencePoint(
  [in]      Msvm_SnapshotCollection       REF AffectedSnapshotCollection,
  [in, out] Msvm_ReferencePointCollection REF ResultingReferencePointCollection,
  [out]     CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="44678-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44678-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44678-111">*AffectedSnapshotCollection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="44678-111">*AffectedSnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44678-112">Referência a um [**Msvm \_ snapshotcollection**](msvm-snapshotcollection.md) que contém a coleção de instantâneos do sistema virtual afetada.</span><span class="sxs-lookup"><span data-stu-id="44678-112">Reference to a [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) containing the affected virtual system snapshot collection.</span></span>

</dd> <dt>

<span data-ttu-id="44678-113">*ResultingReferencePointCollection* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="44678-113">*ResultingReferencePointCollection* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="44678-114">Referência a um [**Msvm \_ ReferencePointCollection**](msvm-referencepointcollection.md) que contém a coleção de pontos de referência do sistema virtual resultante</span><span class="sxs-lookup"><span data-stu-id="44678-114">Reference to a [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) containing the resulting virtual system reference point collection</span></span>

</dd> <dt>

<span data-ttu-id="44678-115">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="44678-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44678-116">Se a operação for de longa execução, opcionalmente, um trabalho poderá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="44678-116">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44678-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="44678-117">Return value</span></span>

<span data-ttu-id="44678-118">Em caso de sucesso, retorna 0 (completo) ou 4096 (trabalho iniciado); caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="44678-118">On success, returns either 0 (Complete) or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="44678-119">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="44678-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="44678-120">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="44678-120">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="44678-121">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="44678-121">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="44678-122">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="44678-122">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="44678-123">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="44678-123">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="44678-124">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="44678-124">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="44678-125">**Tipo inválido** (6)</span><span class="sxs-lookup"><span data-stu-id="44678-125">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="44678-126">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="44678-126">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="44678-127">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="44678-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="44678-128">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="44678-128">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="44678-129">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="44678-129">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="44678-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44678-130">Requirements</span></span>



| <span data-ttu-id="44678-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="44678-131">Requirement</span></span> | <span data-ttu-id="44678-132">Valor</span><span class="sxs-lookup"><span data-stu-id="44678-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44678-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44678-133">Minimum supported client</span></span><br/> | <span data-ttu-id="44678-134">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="44678-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="44678-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44678-135">Minimum supported server</span></span><br/> | <span data-ttu-id="44678-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="44678-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="44678-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="44678-137">Namespace</span></span><br/>                | <span data-ttu-id="44678-138">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="44678-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="44678-139">MOF</span><span class="sxs-lookup"><span data-stu-id="44678-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44678-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44678-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="44678-141">DLL</span><span class="sxs-lookup"><span data-stu-id="44678-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44678-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="44678-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="44678-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="44678-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44678-144">**Msvm \_ CollectionSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="44678-144">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




