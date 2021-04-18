---
description: Recupera uma lista de alterações na região especificada de um disco virtual desde a ID de Controle de Alterações resiliente fornecida ou a ID de instantâneo VHDSet.
ms.assetid: c1dac403-96e0-4c0d-ad71-858f04bf07cd
title: Método GetVirtualDiskChanges da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVirtualDiskChanges
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 55a9cb9a63e05e002f99984a306566c50d9e1d7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787105"
---
# <a name="getvirtualdiskchanges-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="3ea9b-103">Método GetVirtualDiskChanges da \_ classe imagens Msvm</span><span class="sxs-lookup"><span data-stu-id="3ea9b-103">GetVirtualDiskChanges method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="3ea9b-104">Recupera uma lista de alterações na região especificada de um disco virtual desde a ID de Controle de Alterações resiliente fornecida ou a ID de instantâneo VHDSet.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-104">Retrieves a list of changes in the specified region of a virtual disk since the provided Resilient Change Tracking Id or VHDSet Snapshot Id.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ea9b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ea9b-105">Syntax</span></span>


```mof
uint32 GetVirtualDiskChanges(
  [in]  string              Path,
  [in]  string              LimitId,
  [in]  string              TargetSnapshotId,
  [in]  uint64              ByteOffset,
  [in]  uint64              ByteLength,
  [out] uint64              ProcessedByteLength,
  [out] uint64              ChangedByteOffsets[],
  [out] uint64              ChangedByteLengths[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3ea9b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ea9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ea9b-107">*Caminho* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="3ea9b-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ea9b-108">Um caminho totalmente qualificado que especifica o local do arquivo de disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-108">A fully-qualified path that specifies the location of the Virtual Hard Disk file.</span></span>

</dd> <dt>

<span data-ttu-id="3ea9b-109">*Limitid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3ea9b-109">*LimitId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ea9b-110">Uma ID de Controle de Alterações resiliente ou uma ID de instantâneo de conjunto de VHD que indica a linha de base para alterações no disco virtual.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-110">A Resilient Change Tracking Id or VHD Set Snapshot Id indicating the baseline for changes in the virtual disk.</span></span>

</dd> <dt>

<span data-ttu-id="3ea9b-111">*TargetSnapshotId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3ea9b-111">*TargetSnapshotId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ea9b-112">Uma ID de instantâneo VHDSet que indica o instantâneo a ser comparado com a linha de base ao fazer o deprazo das alterações no disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-112">A VHDSet Snapshot Id indicating the snapshot to compare to the baseline when determing changes in the virtual hard disk.</span></span> <span data-ttu-id="3ea9b-113">Este parâmetro só é válido para arquivos de conjunto VHD.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-113">This parameter is only valid for VHD Set files.</span></span>

</dd> <dt>

<span data-ttu-id="3ea9b-114">*ByteOffset* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3ea9b-114">*ByteOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ea9b-115">O deslocamento de byte da região no disco virtual para consulta de alterações.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-115">The byte offset of the region in the virtual disk to query changes for.</span></span>

</dd> <dt>

<span data-ttu-id="3ea9b-116">*ByteLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3ea9b-116">*ByteLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ea9b-117">O comprimento de bytes da região no disco virtual para consulta de alterações.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-117">The byte length of the region in the virtual disk to query changes for.</span></span> <span data-ttu-id="3ea9b-118">Isso deve ser menor que o tamanho do disco virtual.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-118">This must be less than the size of the Virtual Disk.</span></span>

</dd> <dt>

<span data-ttu-id="3ea9b-119">*ProcessedByteLength* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3ea9b-119">*ProcessedByteLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ea9b-120">O comprimento total de bytes que foi processado.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-120">The total byte length that was processed.</span></span> <span data-ttu-id="3ea9b-121">Isso pode ser igual a ByteLength ou menos.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-121">This may be equal to ByteLength or less.</span></span>

</dd> <dt>

<span data-ttu-id="3ea9b-122">*ChangedByteOffsets* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3ea9b-122">*ChangedByteOffsets* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ea9b-123">A lista de deslocamentos de bytes no disco virtual que indica o início de cada intervalo alterado.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-123">The list of byte offsets into the virtual disk indicating the beginning of each changed range.</span></span>

</dd> <dt>

<span data-ttu-id="3ea9b-124">*ChangedByteLengths* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3ea9b-124">*ChangedByteLengths* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ea9b-125">A lista de comprimentos de bytes dos intervalos alterados no disco virtual.</span><span class="sxs-lookup"><span data-stu-id="3ea9b-125">The list of byte lengths of the changed ranges in the virtual disk.</span></span>

</dd> <dt>

<span data-ttu-id="3ea9b-126">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="3ea9b-126">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ea9b-127">Uma referência ao trabalho (pode ser NULL se a tarefa for concluída).</span><span class="sxs-lookup"><span data-stu-id="3ea9b-127">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ea9b-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3ea9b-128">Return value</span></span>

<span data-ttu-id="3ea9b-129">Esse método retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="3ea9b-129">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="3ea9b-130">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="3ea9b-130">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3ea9b-131">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="3ea9b-131">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3ea9b-132">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="3ea9b-132">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3ea9b-133">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="3ea9b-133">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3ea9b-134">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="3ea9b-134">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3ea9b-135">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="3ea9b-135">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3ea9b-136">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="3ea9b-136">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3ea9b-137">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="3ea9b-137">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3ea9b-138">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="3ea9b-138">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3ea9b-139">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="3ea9b-139">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3ea9b-140">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="3ea9b-140">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3ea9b-141">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="3ea9b-141">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3ea9b-142">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="3ea9b-142">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="3ea9b-143">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="3ea9b-143">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3ea9b-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ea9b-144">Requirements</span></span>



| <span data-ttu-id="3ea9b-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ea9b-145">Requirement</span></span> | <span data-ttu-id="3ea9b-146">Valor</span><span class="sxs-lookup"><span data-stu-id="3ea9b-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ea9b-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ea9b-147">Minimum supported client</span></span><br/> | <span data-ttu-id="3ea9b-148">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3ea9b-148">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="3ea9b-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ea9b-149">Minimum supported server</span></span><br/> | <span data-ttu-id="3ea9b-150">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3ea9b-150">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3ea9b-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="3ea9b-151">Namespace</span></span><br/>                | <span data-ttu-id="3ea9b-152">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="3ea9b-152">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3ea9b-153">MOF</span><span class="sxs-lookup"><span data-stu-id="3ea9b-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ea9b-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ea9b-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ea9b-155">DLL</span><span class="sxs-lookup"><span data-stu-id="3ea9b-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ea9b-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3ea9b-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3ea9b-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ea9b-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ea9b-158">**Msvm \_ imagens**</span><span class="sxs-lookup"><span data-stu-id="3ea9b-158">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




