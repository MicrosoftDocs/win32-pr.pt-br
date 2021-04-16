---
description: Converta um instantâneo do sistema virtual existente em um ponto de referência. O instantâneo é excluído como um efeito colateral. Somente instantâneos de recuperação podem ser convertidos em pontos de referência.
ms.assetid: c634d749-e18f-4a11-a574-2aee705c0722
title: Método ConvertToReferencePoint da classe Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ConvertToReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 18eecc1677abaec5893b3749b4ee82f757cbe93e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768504"
---
# <a name="converttoreferencepoint-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="7faa1-105">Método ConvertToReferencePoint da \_ classe VirtualSystemSnapshotService Msvm</span><span class="sxs-lookup"><span data-stu-id="7faa1-105">ConvertToReferencePoint method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="7faa1-106">Converta um instantâneo do sistema virtual existente em um ponto de referência.</span><span class="sxs-lookup"><span data-stu-id="7faa1-106">Convert an existing virtual system snapshot to a reference point.</span></span> <span data-ttu-id="7faa1-107">O instantâneo é excluído como um efeito colateral.</span><span class="sxs-lookup"><span data-stu-id="7faa1-107">The snapshot gets deleted as a side effect.</span></span> <span data-ttu-id="7faa1-108">Somente instantâneos de recuperação podem ser convertidos em pontos de referência.</span><span class="sxs-lookup"><span data-stu-id="7faa1-108">Only recovery snapshots can be converted to reference points.</span></span>

## <a name="syntax"></a><span data-ttu-id="7faa1-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7faa1-109">Syntax</span></span>


```mof
uint32 ConvertToReferencePoint(
  [in]      CIM_VirtualSystemSettingData     REF AffectedSnapshot,
  [in]      string                               ReferencePointSettings,
  [in, out] Msvm_VirtualSystemReferencePoint REF ResultingReferencePoint,
  [out]     CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7faa1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7faa1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7faa1-111">*AffectedSnapshot* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7faa1-111">*AffectedSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7faa1-112">Referência ao instantâneo do sistema virtual afetado.</span><span class="sxs-lookup"><span data-stu-id="7faa1-112">Reference to the affected virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="7faa1-113">*ReferencePointSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7faa1-113">*ReferencePointSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7faa1-114">Configurações de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7faa1-114">Parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="7faa1-115">*ResultingReferencePoint* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="7faa1-115">*ResultingReferencePoint* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7faa1-116">Ponto de referência do sistema virtual resultante</span><span class="sxs-lookup"><span data-stu-id="7faa1-116">Resulting virtual system reference point</span></span>

</dd> <dt>

<span data-ttu-id="7faa1-117">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="7faa1-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7faa1-118">Se a operação for de longa execução, opcionalmente, um trabalho poderá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="7faa1-118">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7faa1-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7faa1-119">Return value</span></span>

<span data-ttu-id="7faa1-120">Retorna um 0 em caso de êxito; caso contrário, retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="7faa1-120">Returns a 0 on success; otherwise, returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="7faa1-121">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="7faa1-121">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7faa1-122">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="7faa1-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7faa1-123">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="7faa1-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7faa1-124">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="7faa1-124">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7faa1-125">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="7faa1-125">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7faa1-126">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="7faa1-126">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7faa1-127">**Tipo inválido** (6)</span><span class="sxs-lookup"><span data-stu-id="7faa1-127">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7faa1-128">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="7faa1-128">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7faa1-129">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="7faa1-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7faa1-130">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="7faa1-130">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="7faa1-131">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="7faa1-131">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7faa1-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7faa1-132">Requirements</span></span>



| <span data-ttu-id="7faa1-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="7faa1-133">Requirement</span></span> | <span data-ttu-id="7faa1-134">Valor</span><span class="sxs-lookup"><span data-stu-id="7faa1-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7faa1-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7faa1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7faa1-136">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7faa1-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="7faa1-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7faa1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7faa1-138">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7faa1-138">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7faa1-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="7faa1-139">Namespace</span></span><br/>                | <span data-ttu-id="7faa1-140">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="7faa1-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7faa1-141">MOF</span><span class="sxs-lookup"><span data-stu-id="7faa1-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7faa1-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7faa1-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7faa1-143">DLL</span><span class="sxs-lookup"><span data-stu-id="7faa1-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7faa1-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7faa1-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7faa1-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="7faa1-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7faa1-146">**Msvm \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="7faa1-146">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




