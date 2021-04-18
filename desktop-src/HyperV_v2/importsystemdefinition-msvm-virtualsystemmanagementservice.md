---
description: Cria um novo sistema de computador planejado com base na definição de máquina virtual especificada.
ms.assetid: 885d399f-5bcf-4f34-b2f1-582cbfcd7c10
title: Método ImportSystemDefinition da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bb38ab343a3d92fabd1dc44ed100d2d2f7f7bf01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759411"
---
# <a name="importsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="373ef-103">Método ImportSystemDefinition da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="373ef-103">ImportSystemDefinition method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="373ef-104">Cria um novo sistema de computador planejado com base na definição de máquina virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="373ef-104">Creates a new planned computer system based on the specified virtual machine definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="373ef-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="373ef-105">Syntax</span></span>


```mof
uint32 ImportSystemDefinition(
  [in]  string                         SystemDefinitionFile,
  [in]  string                         SnapshotFolder,
  [in]  boolean                        GenerateNewSystemIdentifier,
  [out] Msvm_PlannedComputerSystem REF ImportedSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="373ef-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="373ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="373ef-107">*SystemDefinitionFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="373ef-107">*SystemDefinitionFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="373ef-108">O caminho totalmente qualificado para o arquivo de definição do sistema (. xml ou. exp) que representa a máquina virtual que deve ser importada.</span><span class="sxs-lookup"><span data-stu-id="373ef-108">The fully qualified path to the system definition file (.xml or .exp) representing the virtual machine which is to be imported.</span></span> <span data-ttu-id="373ef-109">O arquivo de definição ainda não deve estar em uso pelo sistema host ou pela plataforma de virtualização.</span><span class="sxs-lookup"><span data-stu-id="373ef-109">The definition file must not already be in use by the host system or the virtualization platform.</span></span>

</dd> <dt>

<span data-ttu-id="373ef-110">*SnapshotFolder* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="373ef-110">*SnapshotFolder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="373ef-111">O caminho totalmente qualificado para a pasta em que as configurações de instantâneo para esta máquina virtual podem ser encontradas.</span><span class="sxs-lookup"><span data-stu-id="373ef-111">The fully qualified path to the folder where the snapshot configurations for this virtual machine can be found.</span></span> <span data-ttu-id="373ef-112">Essa pasta será pesquisada para localizar todos os instantâneos referenciados pela definição da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="373ef-112">This folder will be searched in order to locate any snapshots referenced by the virtual machine definition.</span></span> <span data-ttu-id="373ef-113">Todos os instantâneos referenciados não encontrados nesse local devem ser excluídos usando o método [**DestroySnapshot**](destroysnapshot-msvm-virtualsystemsnapshotservice.md) ou importados usando o método [**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md) antes de concretizar o sistema de computador planejado.</span><span class="sxs-lookup"><span data-stu-id="373ef-113">Any referenced snapshots not found in this location must be deleted using the [**DestroySnapshot**](destroysnapshot-msvm-virtualsystemsnapshotservice.md) method, or imported using the [**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md) method prior to realizing the planned computer system.</span></span>

</dd> <dt>

<span data-ttu-id="373ef-114">*GenerateNewSystemIdentifier* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="373ef-114">*GenerateNewSystemIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="373ef-115">Indica se o identificador exclusivo deve ser reutilizado para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="373ef-115">Indicates whether to reuse the unique identifier for the virtual machine.</span></span> <span data-ttu-id="373ef-116">Se esse parâmetro for **true**, um novo identificador do sistema será gerado.</span><span class="sxs-lookup"><span data-stu-id="373ef-116">If this parameter is **True**, then a new system identifier is generated.</span></span> <span data-ttu-id="373ef-117">Se esse parâmetro for **false**, o identificador do sistema existente será usado.</span><span class="sxs-lookup"><span data-stu-id="373ef-117">If this parameter is **False**, then the existing system identifier is used.</span></span>

</dd> <dt>

<span data-ttu-id="373ef-118">*ImportedSystem* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="373ef-118">*ImportedSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="373ef-119">Se a operação for concluída de forma síncrona, uma referência a um objeto [**Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) que representa a máquina virtual importada.</span><span class="sxs-lookup"><span data-stu-id="373ef-119">If the operation completes synchronously, a reference to an [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) object that represents the imported virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="373ef-120">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="373ef-120">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="373ef-121">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="373ef-121">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="373ef-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="373ef-122">Return value</span></span>

<span data-ttu-id="373ef-123">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="373ef-123">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="373ef-124">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="373ef-124">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="373ef-125">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="373ef-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="373ef-126">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="373ef-126">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="373ef-127">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="373ef-127">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="373ef-128">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="373ef-128">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="373ef-129">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="373ef-129">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="373ef-130">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="373ef-130">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="373ef-131">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="373ef-131">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="373ef-132">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="373ef-132">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="373ef-133">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="373ef-133">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="373ef-134">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="373ef-134">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="373ef-135">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="373ef-135">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="373ef-136">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="373ef-136">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="373ef-137">**Arquivo em uso** (32779)</span><span class="sxs-lookup"><span data-stu-id="373ef-137">**File in Use** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="373ef-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="373ef-138">Requirements</span></span>



| <span data-ttu-id="373ef-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="373ef-139">Requirement</span></span> | <span data-ttu-id="373ef-140">Valor</span><span class="sxs-lookup"><span data-stu-id="373ef-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="373ef-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="373ef-141">Minimum supported client</span></span><br/> | <span data-ttu-id="373ef-142">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="373ef-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="373ef-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="373ef-143">Minimum supported server</span></span><br/> | <span data-ttu-id="373ef-144">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="373ef-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="373ef-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="373ef-145">Namespace</span></span><br/>                | <span data-ttu-id="373ef-146">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="373ef-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="373ef-147">MOF</span><span class="sxs-lookup"><span data-stu-id="373ef-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="373ef-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="373ef-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="373ef-149">DLL</span><span class="sxs-lookup"><span data-stu-id="373ef-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="373ef-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="373ef-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="373ef-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="373ef-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="373ef-152">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="373ef-152">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

