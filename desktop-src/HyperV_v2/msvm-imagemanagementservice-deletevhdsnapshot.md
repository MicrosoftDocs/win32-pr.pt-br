---
description: Exclui uma entrada de instantâneo VHD em um arquivo de conjunto VHD.
ms.assetid: 37d55a5f-209d-42ce-8f69-8b494055e263
title: Método DeleteVHDSnapshot da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.DeleteVHDSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5c7f3f115825aedb3a21a8f33326a712c52e0780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758643"
---
# <a name="deletevhdsnapshot-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="efe79-103">Método DeleteVHDSnapshot da \_ classe imagens Msvm</span><span class="sxs-lookup"><span data-stu-id="efe79-103">DeleteVHDSnapshot method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="efe79-104">Exclui uma entrada de instantâneo VHD em um arquivo de conjunto VHD.</span><span class="sxs-lookup"><span data-stu-id="efe79-104">Deletes a VHD Snapshot entry within a VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="efe79-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="efe79-105">Syntax</span></span>


```mof
uint32 DeleteVHDSnapshot(
  [in]  string              VHDSetPath,
  [in]  string              SnapshotId,
  [in]  boolean             PersistReferenceSnapshot,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="efe79-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="efe79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efe79-107">*VHDSetPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="efe79-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efe79-108">Cadeia de caracteres que contém o caminho para o arquivo de conjunto VHD que contém o instantâneo em questão.</span><span class="sxs-lookup"><span data-stu-id="efe79-108">String containing the path to the VHD Set file containing the snapshot in question.</span></span>

</dd> <dt>

<span data-ttu-id="efe79-109">*Instantâneoid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="efe79-109">*SnapshotId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efe79-110">Um GUID que representa a ID de instantâneo para a entrada de instantâneo VHD a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="efe79-110">A GUID representing the Snapshot ID for the VHD Snapshot entry to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="efe79-111">*PersistReferenceSnapshot* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="efe79-111">*PersistReferenceSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efe79-112">Se um registro de instantâneo somente de referência deve ou não persistir após a exclusão do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="efe79-112">Whether or not a reference-only snapshot record should be persisted after the snapshot is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="efe79-113">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="efe79-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="efe79-114">Uma referência ao trabalho (pode ser NULL se a tarefa for concluída).</span><span class="sxs-lookup"><span data-stu-id="efe79-114">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efe79-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="efe79-115">Return value</span></span>

<span data-ttu-id="efe79-116">Esse método retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="efe79-116">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="efe79-117">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="efe79-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="efe79-118">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="efe79-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="efe79-119">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="efe79-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="efe79-120">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="efe79-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="efe79-121">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="efe79-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="efe79-122">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="efe79-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="efe79-123">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="efe79-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="efe79-124">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="efe79-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="efe79-125">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="efe79-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="efe79-126">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="efe79-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="efe79-127">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="efe79-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="efe79-128">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="efe79-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="efe79-129">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="efe79-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="efe79-130">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="efe79-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="efe79-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efe79-131">Requirements</span></span>



| <span data-ttu-id="efe79-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="efe79-132">Requirement</span></span> | <span data-ttu-id="efe79-133">Valor</span><span class="sxs-lookup"><span data-stu-id="efe79-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efe79-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efe79-134">Minimum supported client</span></span><br/> | <span data-ttu-id="efe79-135">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="efe79-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="efe79-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efe79-136">Minimum supported server</span></span><br/> | <span data-ttu-id="efe79-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="efe79-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="efe79-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="efe79-138">Namespace</span></span><br/>                | <span data-ttu-id="efe79-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="efe79-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="efe79-140">MOF</span><span class="sxs-lookup"><span data-stu-id="efe79-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="efe79-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="efe79-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="efe79-142">DLL</span><span class="sxs-lookup"><span data-stu-id="efe79-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efe79-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="efe79-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="efe79-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="efe79-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efe79-145">**Msvm \_ imagens**</span><span class="sxs-lookup"><span data-stu-id="efe79-145">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




