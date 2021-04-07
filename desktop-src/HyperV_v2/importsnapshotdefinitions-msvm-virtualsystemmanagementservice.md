---
description: Pesquisa a pasta especificada em busca de quaisquer arquivos de definição de instantâneo associados ao sistema de computador planejado especificado e cria um novo instantâneo no sistema de computador planejado para cada arquivo de definição associado neste local.
ms.assetid: d240c24b-f788-4ea9-b3bd-af1f75f4f460
title: Método ImportSnapshotDefinitions da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSnapshotDefinitions
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9ebb36b030786ab88eab899190afcc7f3022286a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827615"
---
# <a name="importsnapshotdefinitions-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="47c3e-103">Método ImportSnapshotDefinitions da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="47c3e-103">ImportSnapshotDefinitions method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="47c3e-104">Pesquisa a pasta especificada em busca de quaisquer arquivos de definição de instantâneo associados ao sistema de computador planejado especificado e cria um novo instantâneo no sistema de computador planejado para cada arquivo de definição associado neste local.</span><span class="sxs-lookup"><span data-stu-id="47c3e-104">Searches the specified folder for any snapshot definition files associated with the specified planned computer system, and creates a new snapshot on the planned computer system for every associated definition file in this location.</span></span>

## <a name="syntax"></a><span data-ttu-id="47c3e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47c3e-105">Syntax</span></span>


```mof
uint32 ImportSnapshotDefinitions(
  [in]  Msvm_PlannedComputerSystem    REF PlannedSystem,
  [in]  string                            SnapshotFolder,
  [out] Msvm_VirtualSystemSettingData REF ImportedSnapshots[],
  [out] CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="47c3e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47c3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47c3e-107">*PlannedSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="47c3e-107">*PlannedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47c3e-108">Uma referência a um objeto [**Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) que representa a máquina virtual planejada que faz referência aos instantâneos a serem importados.</span><span class="sxs-lookup"><span data-stu-id="47c3e-108">A reference to an [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) object that represents the planned virtual machine which references the snapshots to be imported.</span></span>

</dd> <dt>

<span data-ttu-id="47c3e-109">*SnapshotFolder* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="47c3e-109">*SnapshotFolder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47c3e-110">O caminho totalmente qualificado para a pasta em que as configurações de instantâneo para esta máquina virtual podem ser encontradas.</span><span class="sxs-lookup"><span data-stu-id="47c3e-110">The fully qualified path to the folder where the snapshot configurations for this virtual machine can be found.</span></span>

</dd> <dt>

<span data-ttu-id="47c3e-111">*ImportedSnapshots* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="47c3e-111">*ImportedSnapshots* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47c3e-112">Se a operação for concluída de forma síncrona, uma matriz de referências às instâncias [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa os instantâneos que foram importados com êxito.</span><span class="sxs-lookup"><span data-stu-id="47c3e-112">If the operation completes synchronously, an array of references to the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instances representing the snapshots which were successfully imported.</span></span>

</dd> <dt>

<span data-ttu-id="47c3e-113">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="47c3e-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47c3e-114">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="47c3e-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47c3e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="47c3e-115">Return value</span></span>

<span data-ttu-id="47c3e-116">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="47c3e-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="47c3e-117">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="47c3e-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="47c3e-118">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="47c3e-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="47c3e-119">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="47c3e-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="47c3e-120">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="47c3e-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="47c3e-121">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="47c3e-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="47c3e-122">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="47c3e-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="47c3e-123">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="47c3e-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="47c3e-124">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="47c3e-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="47c3e-125">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="47c3e-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="47c3e-126">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="47c3e-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="47c3e-127">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="47c3e-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="47c3e-128">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="47c3e-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="47c3e-129">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="47c3e-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="47c3e-130">**Arquivo em uso** (32779)</span><span class="sxs-lookup"><span data-stu-id="47c3e-130">**File in Use** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="47c3e-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47c3e-131">Requirements</span></span>



| <span data-ttu-id="47c3e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="47c3e-132">Requirement</span></span> | <span data-ttu-id="47c3e-133">Valor</span><span class="sxs-lookup"><span data-stu-id="47c3e-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47c3e-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47c3e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="47c3e-135">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="47c3e-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="47c3e-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47c3e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="47c3e-137">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="47c3e-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="47c3e-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="47c3e-138">Namespace</span></span><br/>                | <span data-ttu-id="47c3e-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="47c3e-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="47c3e-140">MOF</span><span class="sxs-lookup"><span data-stu-id="47c3e-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47c3e-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47c3e-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="47c3e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="47c3e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47c3e-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="47c3e-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="47c3e-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="47c3e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47c3e-145">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="47c3e-145">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

