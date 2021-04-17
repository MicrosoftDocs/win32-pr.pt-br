---
description: Recupera informações sobre um instantâneo VHD em um arquivo de conjunto VHD.
ms.assetid: 43745935-9bc3-4a87-8762-54693b2cdef6
title: Método GetVHDSnapshotInformation da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVHDSnapshotInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 85ea18e2be5329345ba49f4956307c4b29134ed6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754669"
---
# <a name="getvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="7b977-103">Método GetVHDSnapshotInformation da \_ classe imagens Msvm</span><span class="sxs-lookup"><span data-stu-id="7b977-103">GetVHDSnapshotInformation method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="7b977-104">Recupera informações sobre um instantâneo VHD em um arquivo de conjunto VHD.</span><span class="sxs-lookup"><span data-stu-id="7b977-104">Retrieves information about a VHD Snapshot within a VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b977-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b977-105">Syntax</span></span>


```mof
uint32 GetVHDSnapshotInformation(
  [in]  string              VHDSetPath,
  [in]  string              SnapshotIds[],
  [in]  uint32              AdditionalInformation[],
  [out] string              SnapshotInformation[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7b977-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b977-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b977-107">*VHDSetPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b977-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b977-108">Um caminho totalmente qualificado que especifica o local do arquivo de conjunto de VHD.</span><span class="sxs-lookup"><span data-stu-id="7b977-108">A fully-qualified path that specifies the location of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="7b977-109">*SnapshotIds* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b977-109">*SnapshotIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b977-110">Uma lista de GUIDs que representa as IDs de instantâneo de cada instantâneo para o qual as informações estão sendo solicitadas.</span><span class="sxs-lookup"><span data-stu-id="7b977-110">A list of GUIDs representing the Snapshot Ids of each Snapshot for which information is being requested.</span></span> <span data-ttu-id="7b977-111">Se esse parâmetro for nulo, as informações de todos os instantâneos serão recuperadas.</span><span class="sxs-lookup"><span data-stu-id="7b977-111">If this parameter is NULL, information for all Snapshots will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="7b977-112">*AdditionalInformation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b977-112">*AdditionalInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b977-113">Uma matriz que especifica quais informações adicionais devem ser coletadas sobre cada instantâneo do VHD.</span><span class="sxs-lookup"><span data-stu-id="7b977-113">An array specifying what additional information should be gathered about each VHD Snapshot.</span></span> <span data-ttu-id="7b977-114">Cada entrada na matriz é um tipo de informação adicional.</span><span class="sxs-lookup"><span data-stu-id="7b977-114">Each entry in the array is a type of additional information.</span></span> <span data-ttu-id="7b977-115">Se esse parâmetro for nulo, nenhuma informação adicional será recuperada.</span><span class="sxs-lookup"><span data-stu-id="7b977-115">If this parameter is NULL, no additional information will be retrieved.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7b977-116">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="7b977-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7b977-117">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="7b977-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Parent_Paths"></span><span id="parent_paths"></span><span id="PARENT_PATHS"></span>

<span data-ttu-id="7b977-118">**Caminhos pai** (2)</span><span class="sxs-lookup"><span data-stu-id="7b977-118">**Parent Paths** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="7b977-119">*SnapshotInformation* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7b977-119">*SnapshotInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b977-120">Se for bem-sucedido, uma matriz de informações sobre cada instantâneo solicitado.</span><span class="sxs-lookup"><span data-stu-id="7b977-120">If successful, an array of information about each requested snapshot.</span></span> <span data-ttu-id="7b977-121">Cada elemento é uma instância incorporada de [**Msvm \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).</span><span class="sxs-lookup"><span data-stu-id="7b977-121">Each element is an embedded instance of [**Msvm\_VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b977-122">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="7b977-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b977-123">Uma referência ao trabalho (pode ser NULL se a tarefa for concluída).</span><span class="sxs-lookup"><span data-stu-id="7b977-123">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b977-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7b977-124">Return value</span></span>

<span data-ttu-id="7b977-125">Esse método retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="7b977-125">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="7b977-126">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="7b977-126">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7b977-127">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="7b977-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7b977-128">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="7b977-128">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="7b977-129">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="7b977-129">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="7b977-130">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="7b977-130">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="7b977-131">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="7b977-131">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="7b977-132">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="7b977-132">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="7b977-133">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="7b977-133">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="7b977-134">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="7b977-134">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="7b977-135">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="7b977-135">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="7b977-136">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="7b977-136">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="7b977-137">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="7b977-137">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="7b977-138">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="7b977-138">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="7b977-139">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="7b977-139">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7b977-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b977-140">Requirements</span></span>



| <span data-ttu-id="7b977-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b977-141">Requirement</span></span> | <span data-ttu-id="7b977-142">Valor</span><span class="sxs-lookup"><span data-stu-id="7b977-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b977-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b977-143">Minimum supported client</span></span><br/> | <span data-ttu-id="7b977-144">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7b977-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="7b977-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b977-145">Minimum supported server</span></span><br/> | <span data-ttu-id="7b977-146">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7b977-146">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7b977-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="7b977-147">Namespace</span></span><br/>                | <span data-ttu-id="7b977-148">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="7b977-148">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7b977-149">MOF</span><span class="sxs-lookup"><span data-stu-id="7b977-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b977-150"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b977-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b977-151">DLL</span><span class="sxs-lookup"><span data-stu-id="7b977-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b977-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7b977-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7b977-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b977-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b977-154">**Msvm \_ imagens**</span><span class="sxs-lookup"><span data-stu-id="7b977-154">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




