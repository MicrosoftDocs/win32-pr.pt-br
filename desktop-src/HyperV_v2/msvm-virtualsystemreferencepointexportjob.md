---
description: Essa classe representa um trabalho de operação de exportação do ponto de referência do sistema virtual.
ms.assetid: 3d8e117c-4863-441a-9264-c33f05fbc5ef
title: Classe Msvm_VirtualSystemReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob
- Msvm_VirtualSystemReferencePointExportJob.Cancellable
- Msvm_VirtualSystemReferencePointExportJob.ErrorSummaryDescription
- Msvm_VirtualSystemReferencePointExportJob.ExportDirectory
- Msvm_VirtualSystemReferencePointExportJob.VirtualMachineId
- Msvm_VirtualSystemReferencePointExportJob.ReferencePointId
- Msvm_VirtualSystemReferencePointExportJob.BaseReferencePointId
- Msvm_VirtualSystemReferencePointExportJob.ExportedDisks
- Msvm_VirtualSystemReferencePointExportJob.ExportedLogFilePaths
- Msvm_VirtualSystemReferencePointExportJob.ExportedConfigFilePath
- Msvm_VirtualSystemReferencePointExportJob.ExportedRuntimeFilePath
- Msvm_VirtualSystemReferencePointExportJob.ExportedGuestStateFilePath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04b5d8f27efae4817062917541af9bb488cec32c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104506327"
---
# <a name="msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="9300b-103">\_Classe Msvm VirtualSystemReferencePointExportJob</span><span class="sxs-lookup"><span data-stu-id="9300b-103">Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="9300b-104">Essa classe representa um trabalho de operação de exportação do ponto de referência do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="9300b-104">This class represents a virtual system reference point export operation job.</span></span>

<span data-ttu-id="9300b-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9300b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9300b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9300b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePointExportJob : CIM_ConcreteJob
{
  boolean Cancellable;
  string  ErrorSummaryDescription;
  string  ExportDirectory;
  string  VirtualMachineId;
  string  ReferencePointId;
  string  BaseReferencePointId;
  string  ExportedDisks[];
  string  ExportedLogFilePaths[];
  string  ExportedConfigFilePath;
  string  ExportedRuntimeFilePath;
  string  ExportedGuestStateFilePath;
};
```

## <a name="members"></a><span data-ttu-id="9300b-107">Membros</span><span class="sxs-lookup"><span data-stu-id="9300b-107">Members</span></span>

<span data-ttu-id="9300b-108">A classe **Msvm \_ VirtualSystemReferencePointExportJob** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9300b-108">The **Msvm\_VirtualSystemReferencePointExportJob** class has these types of members:</span></span>

-   [<span data-ttu-id="9300b-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="9300b-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="9300b-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9300b-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9300b-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="9300b-111">Methods</span></span>

<span data-ttu-id="9300b-112">A classe **Msvm \_ VirtualSystemReferencePointExportJob** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="9300b-112">The **Msvm\_VirtualSystemReferencePointExportJob** class has these methods.</span></span>



| <span data-ttu-id="9300b-113">Método</span><span class="sxs-lookup"><span data-stu-id="9300b-113">Method</span></span>                                                                                     | <span data-ttu-id="9300b-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="9300b-114">Description</span></span>                                        |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="9300b-115">**GetError**</span><span class="sxs-lookup"><span data-stu-id="9300b-115">**GetError**</span></span>](msvm-virtualsystemreferencepointexportjob-geterror.md)                     | <span data-ttu-id="9300b-116">Recupera o erro.</span><span class="sxs-lookup"><span data-stu-id="9300b-116">Retrieves the error.</span></span><br/>                    |
| [<span data-ttu-id="9300b-117">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="9300b-117">**GetErrorEx**</span></span>](msvm-virtualsystemreferencepointexportjob-geterrorex.md)                 | <span data-ttu-id="9300b-118">Recupera informações de erro adicionais.</span><span class="sxs-lookup"><span data-stu-id="9300b-118">Retrieves additional error information.</span></span><br/> |
| [<span data-ttu-id="9300b-119">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="9300b-119">**RequestStateChange**</span></span>](msvm-virtualsystemreferencepointexportjob-requeststatechange.md) | <span data-ttu-id="9300b-120">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="9300b-120">Requests a state change.</span></span><br/>                |



 

### <a name="properties"></a><span data-ttu-id="9300b-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9300b-121">Properties</span></span>

<span data-ttu-id="9300b-122">A classe **Msvm \_ VirtualSystemReferencePointExportJob** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9300b-122">The **Msvm\_VirtualSystemReferencePointExportJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9300b-123">**BaseReferencePointId**</span><span class="sxs-lookup"><span data-stu-id="9300b-123">**BaseReferencePointId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9300b-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9300b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9300b-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9300b-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9300b-126">GUID do ponto de referência que é usado como base na operação de exportação.</span><span class="sxs-lookup"><span data-stu-id="9300b-126">GUID of the reference point which is used as the base in the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="9300b-127">**Cancelável**</span><span class="sxs-lookup"><span data-stu-id="9300b-127">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9300b-128">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9300b-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9300b-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9300b-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9300b-130">Indica se o trabalho pode ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="9300b-130">Indicates whether the job can be cancelled.</span></span> <span data-ttu-id="9300b-131">O valor dessa propriedade não garante que uma solicitação para cancelar o trabalho seja realizada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="9300b-131">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="9300b-132">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="9300b-132">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9300b-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9300b-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9300b-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9300b-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9300b-135">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ trabalho CIM**](cim-job.md).**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="9300b-135">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="9300b-136">Contém uma descrição resumida de erro.</span><span class="sxs-lookup"><span data-stu-id="9300b-136">Contains an error summary description.</span></span>

</dd> <dt>

<span data-ttu-id="9300b-137">**ExportDirectory**</span><span class="sxs-lookup"><span data-stu-id="9300b-137">**ExportDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9300b-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9300b-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9300b-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9300b-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9300b-140">O local de exportação.</span><span class="sxs-lookup"><span data-stu-id="9300b-140">The export location.</span></span>

</dd> <dt>

<span data-ttu-id="9300b-141">**ExportedConfigFilePath**</span><span class="sxs-lookup"><span data-stu-id="9300b-141">**ExportedConfigFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9300b-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9300b-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9300b-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9300b-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9300b-144">Caminho do arquivo de configuração exportado.</span><span class="sxs-lookup"><span data-stu-id="9300b-144">Path of the exported config file.</span></span>

</dd> <dt>

<span data-ttu-id="9300b-145">**ExportedDisks**</span><span class="sxs-lookup"><span data-stu-id="9300b-145">**ExportedDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9300b-146">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9300b-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9300b-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9300b-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9300b-148">IDs de instância de discos virtuais para os quais os arquivos de log foram exportados.</span><span class="sxs-lookup"><span data-stu-id="9300b-148">Instance IDs of virtual disks for which log files were exported.</span></span>

</dd> <dt>

<span data-ttu-id="9300b-149">**ExportedGuestStateFilePath**</span><span class="sxs-lookup"><span data-stu-id="9300b-149">**ExportedGuestStateFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9300b-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9300b-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9300b-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9300b-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9300b-152">Caminho do arquivo de estado de convidado exportado.</span><span class="sxs-lookup"><span data-stu-id="9300b-152">Path of the exported guest state file.</span></span>

> [!Note]  
> <span data-ttu-id="9300b-153">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="9300b-153">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="9300b-154">**ExportedLogFilePaths**</span><span class="sxs-lookup"><span data-stu-id="9300b-154">**ExportedLogFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9300b-155">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9300b-155">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9300b-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9300b-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9300b-157">Caminhos dos arquivos de log que foram exportados.</span><span class="sxs-lookup"><span data-stu-id="9300b-157">Paths of the log files which were exported.</span></span>

</dd> <dt>

<span data-ttu-id="9300b-158">**ExportedRuntimeFilePath**</span><span class="sxs-lookup"><span data-stu-id="9300b-158">**ExportedRuntimeFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9300b-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9300b-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9300b-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9300b-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9300b-161">Caminho do arquivo de estado de tempo de execução exportado.</span><span class="sxs-lookup"><span data-stu-id="9300b-161">Path of the exported runtime state file.</span></span>

</dd> <dt>

<span data-ttu-id="9300b-162">**ReferencePointId**</span><span class="sxs-lookup"><span data-stu-id="9300b-162">**ReferencePointId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9300b-163">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9300b-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9300b-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9300b-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9300b-165">GUID do ponto de referência que é exportado.</span><span class="sxs-lookup"><span data-stu-id="9300b-165">GUID of the reference point which is exported.</span></span>

</dd> <dt>

<span data-ttu-id="9300b-166">**VirtualMachineId**</span><span class="sxs-lookup"><span data-stu-id="9300b-166">**VirtualMachineId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9300b-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9300b-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9300b-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9300b-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9300b-169">GUID da máquina virtual para a qual os arquivos de log foram exportados.</span><span class="sxs-lookup"><span data-stu-id="9300b-169">GUID of the virtual machine for which log files were exported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9300b-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9300b-170">Requirements</span></span>



| <span data-ttu-id="9300b-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="9300b-171">Requirement</span></span> | <span data-ttu-id="9300b-172">Valor</span><span class="sxs-lookup"><span data-stu-id="9300b-172">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9300b-173">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9300b-173">Minimum supported client</span></span><br/> | <span data-ttu-id="9300b-174">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="9300b-174">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9300b-175">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9300b-175">Minimum supported server</span></span><br/> | <span data-ttu-id="9300b-176">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9300b-176">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="9300b-177">Namespace</span><span class="sxs-lookup"><span data-stu-id="9300b-177">Namespace</span></span><br/>                | <span data-ttu-id="9300b-178">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="9300b-178">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9300b-179">MOF</span><span class="sxs-lookup"><span data-stu-id="9300b-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9300b-180"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9300b-180"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9300b-181">DLL</span><span class="sxs-lookup"><span data-stu-id="9300b-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9300b-182"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9300b-182"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9300b-183">Confira também</span><span class="sxs-lookup"><span data-stu-id="9300b-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9300b-184">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="9300b-184">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

