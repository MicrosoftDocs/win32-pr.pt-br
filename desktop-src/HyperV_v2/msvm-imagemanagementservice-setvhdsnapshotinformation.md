---
description: Edita uma entrada de instantâneo VHD em um arquivo de conjunto VHD. Se a ID de instantâneo em questão já existir, a entrada de instantâneo existente será substituída pela nova entrada. Caso contrário, a nova entrada será adicionada ao arquivo do conjunto VHD.
ms.assetid: dd14960d-3fb8-4d47-986f-fbbbb08eb37d
title: Método SetVHDSnapshotInformation da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetVHDSnapshotInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 54f5ac23cdf8f49532a05eee3fd23293715cd02a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780975"
---
# <a name="setvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="e2939-105">Método SetVHDSnapshotInformation da \_ classe imagens Msvm</span><span class="sxs-lookup"><span data-stu-id="e2939-105">SetVHDSnapshotInformation method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="e2939-106">Edita uma entrada de instantâneo VHD em um arquivo de conjunto VHD.</span><span class="sxs-lookup"><span data-stu-id="e2939-106">Edits a VHD Snapshot entry within a VHD Set file.</span></span> <span data-ttu-id="e2939-107">Se a ID de instantâneo em questão já existir, a entrada de instantâneo existente será substituída pela nova entrada.</span><span class="sxs-lookup"><span data-stu-id="e2939-107">If the Snapshot Id in question already exists, the existing Snapshot entry will be overwritten with the new entry.</span></span> <span data-ttu-id="e2939-108">Caso contrário, a nova entrada será adicionada ao arquivo do conjunto VHD.</span><span class="sxs-lookup"><span data-stu-id="e2939-108">Otherwise, the new entry will be added to the VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2939-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2939-109">Syntax</span></span>


```mof
uint32 SetVHDSnapshotInformation(
  [in]  string              Information,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e2939-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2939-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2939-111">*Informações* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="e2939-111">*Information* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2939-112">Informações de instantâneo do VHD a serem alteradas ou adicionadas no arquivo do conjunto VHD.</span><span class="sxs-lookup"><span data-stu-id="e2939-112">VHD Snapshot Information to be changed or added in the VHD Set file.</span></span> <span data-ttu-id="e2939-113">A cadeia de caracteres é uma instância incorporada de [**Msvm \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).</span><span class="sxs-lookup"><span data-stu-id="e2939-113">The string is an embedded instance of [**Msvm\_VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2939-114">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="e2939-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2939-115">Uma referência ao trabalho (pode ser NULL se a tarefa for concluída).</span><span class="sxs-lookup"><span data-stu-id="e2939-115">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2939-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e2939-116">Return value</span></span>

<span data-ttu-id="e2939-117">Esse método retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="e2939-117">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="e2939-118">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="e2939-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e2939-119">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="e2939-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e2939-120">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="e2939-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e2939-121">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="e2939-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e2939-122">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="e2939-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e2939-123">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="e2939-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e2939-124">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="e2939-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e2939-125">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="e2939-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e2939-126">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="e2939-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e2939-127">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="e2939-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e2939-128">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="e2939-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e2939-129">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="e2939-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e2939-130">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="e2939-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="e2939-131">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="e2939-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e2939-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2939-132">Requirements</span></span>



| <span data-ttu-id="e2939-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2939-133">Requirement</span></span> | <span data-ttu-id="e2939-134">Valor</span><span class="sxs-lookup"><span data-stu-id="e2939-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2939-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2939-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e2939-136">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e2939-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e2939-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2939-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e2939-138">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e2939-138">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e2939-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="e2939-139">Namespace</span></span><br/>                | <span data-ttu-id="e2939-140">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e2939-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e2939-141">MOF</span><span class="sxs-lookup"><span data-stu-id="e2939-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2939-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2939-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2939-143">DLL</span><span class="sxs-lookup"><span data-stu-id="e2939-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2939-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e2939-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e2939-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2939-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2939-146">**Msvm \_ imagens**</span><span class="sxs-lookup"><span data-stu-id="e2939-146">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




