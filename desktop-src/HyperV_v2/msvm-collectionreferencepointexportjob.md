---
description: Essa classe representa um trabalho de operação de exportação de ponto de referência de coleção.
ms.assetid: c752ff1d-163c-4aa9-b29e-76478a18a08c
title: Classe Msvm_CollectionReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob
- Msvm_CollectionReferencePointExportJob.Cancellable
- Msvm_CollectionReferencePointExportJob.ErrorSummaryDescription
- Msvm_CollectionReferencePointExportJob.CollectionId
- Msvm_CollectionReferencePointExportJob.ReferencePointGroupId
- Msvm_CollectionReferencePointExportJob.BaseReferencePointGroupId
- Msvm_CollectionReferencePointExportJob.VirtualMachineId
- Msvm_CollectionReferencePointExportJob.ExportDirectory
- Msvm_CollectionReferencePointExportJob.ExportedDisks
- Msvm_CollectionReferencePointExportJob.ExportedLogFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedConfigFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedRuntimeFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedGuestStateFilePaths
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d21fab1519664471bdc2bb5d7102d94cbe3dde1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760857"
---
# <a name="msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="fdb07-103">\_Classe Msvm CollectionReferencePointExportJob</span><span class="sxs-lookup"><span data-stu-id="fdb07-103">Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="fdb07-104">Essa classe representa um trabalho de operação de exportação de ponto de referência de coleção.</span><span class="sxs-lookup"><span data-stu-id="fdb07-104">This class represents a collection reference point export operation job.</span></span>

<span data-ttu-id="fdb07-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="fdb07-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdb07-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fdb07-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionReferencePointExportJob : CIM_ConcreteJob
{
  boolean Cancellable;
  string  ErrorSummaryDescription;
  string  CollectionId;
  string  ReferencePointGroupId;
  string  BaseReferencePointGroupId;
  string  VirtualMachineId[];
  string  ExportDirectory;
  string  ExportedDisks[];
  string  ExportedLogFilePaths[];
  string  ExportedConfigFilePaths[];
  string  ExportedRuntimeFilePaths[];
  string  ExportedGuestStateFilePaths[];
};
```

## <a name="members"></a><span data-ttu-id="fdb07-107">Membros</span><span class="sxs-lookup"><span data-stu-id="fdb07-107">Members</span></span>

<span data-ttu-id="fdb07-108">A classe **Msvm \_ CollectionReferencePointExportJob** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fdb07-108">The **Msvm\_CollectionReferencePointExportJob** class has these types of members:</span></span>

-   [<span data-ttu-id="fdb07-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="fdb07-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="fdb07-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fdb07-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fdb07-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="fdb07-111">Methods</span></span>

<span data-ttu-id="fdb07-112">A classe **Msvm \_ CollectionReferencePointExportJob** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="fdb07-112">The **Msvm\_CollectionReferencePointExportJob** class has these methods.</span></span>



| <span data-ttu-id="fdb07-113">Método</span><span class="sxs-lookup"><span data-stu-id="fdb07-113">Method</span></span>                                                                                  | <span data-ttu-id="fdb07-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="fdb07-114">Description</span></span>                                        |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="fdb07-115">**GetError**</span><span class="sxs-lookup"><span data-stu-id="fdb07-115">**GetError**</span></span>](msvm-collectionreferencepointexportjob-geterror.md)                     | <span data-ttu-id="fdb07-116">Recupera um erro.</span><span class="sxs-lookup"><span data-stu-id="fdb07-116">Retrieves an error.</span></span><br/>                     |
| [<span data-ttu-id="fdb07-117">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="fdb07-117">**GetErrorEx**</span></span>](msvm-collectionreferencepointexportjob-geterrorex.md)                 | <span data-ttu-id="fdb07-118">Recupera informações de erro adicionais.</span><span class="sxs-lookup"><span data-stu-id="fdb07-118">Retrieves additional error information.</span></span><br/> |
| [<span data-ttu-id="fdb07-119">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="fdb07-119">**RequestStateChange**</span></span>](msvm-collectionreferencepointexportjob-requeststatechange.md) | <span data-ttu-id="fdb07-120">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="fdb07-120">Requests a state change.</span></span><br/>                |



 

### <a name="properties"></a><span data-ttu-id="fdb07-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fdb07-121">Properties</span></span>

<span data-ttu-id="fdb07-122">A classe **Msvm \_ CollectionReferencePointExportJob** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fdb07-122">The **Msvm\_CollectionReferencePointExportJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fdb07-123">**BaseReferencePointGroupId**</span><span class="sxs-lookup"><span data-stu-id="fdb07-123">**BaseReferencePointGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb07-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fdb07-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fdb07-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fdb07-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fdb07-126">GUID do ponto de referência de coleção que é usado como base no ExportOperation.</span><span class="sxs-lookup"><span data-stu-id="fdb07-126">GUID of the collection reference point which is used as the base in the exportoperation.</span></span>

</dd> <dt>

<span data-ttu-id="fdb07-127">**Cancelável**</span><span class="sxs-lookup"><span data-stu-id="fdb07-127">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb07-128">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fdb07-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fdb07-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fdb07-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fdb07-130">Indica se o trabalho pode ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="fdb07-130">Indicates whether the job can be cancelled.</span></span> <span data-ttu-id="fdb07-131">O valor dessa propriedade não garante que uma solicitação para cancelar o trabalho seja realizada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="fdb07-131">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="fdb07-132">**CollectionId**</span><span class="sxs-lookup"><span data-stu-id="fdb07-132">**CollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb07-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fdb07-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fdb07-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fdb07-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fdb07-135">GUID do grupo de máquinas virtuais para o qual os arquivos de log wereexported.</span><span class="sxs-lookup"><span data-stu-id="fdb07-135">GUID of the virtual machine group for which log files wereexported.</span></span>

</dd> <dt>

<span data-ttu-id="fdb07-136">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="fdb07-136">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb07-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fdb07-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fdb07-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fdb07-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fdb07-139">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ trabalho CIM**](cim-job.md).**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="fdb07-139">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="fdb07-140">Contém uma descrição resumida de erro.</span><span class="sxs-lookup"><span data-stu-id="fdb07-140">Contains an error summary description.</span></span>

</dd> <dt>

<span data-ttu-id="fdb07-141">**ExportDirectory**</span><span class="sxs-lookup"><span data-stu-id="fdb07-141">**ExportDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb07-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fdb07-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fdb07-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fdb07-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fdb07-144">Local de exportação.</span><span class="sxs-lookup"><span data-stu-id="fdb07-144">Export Location.</span></span>

</dd> <dt>

<span data-ttu-id="fdb07-145">**ExportedConfigFilePaths**</span><span class="sxs-lookup"><span data-stu-id="fdb07-145">**ExportedConfigFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb07-146">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fdb07-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fdb07-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fdb07-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fdb07-148">Caminho do arquivo de configuração de máquina virtual exportado.</span><span class="sxs-lookup"><span data-stu-id="fdb07-148">Path of the exported virtual machine config file.</span></span>

</dd> <dt>

<span data-ttu-id="fdb07-149">**ExportedDisks**</span><span class="sxs-lookup"><span data-stu-id="fdb07-149">**ExportedDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb07-150">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fdb07-150">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fdb07-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fdb07-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fdb07-152">IDs de instância de discos virtuais para os quais os arquivos de log foram exportados.</span><span class="sxs-lookup"><span data-stu-id="fdb07-152">Instance IDs of virtual disks for which log files were exported.</span></span>

</dd> <dt>

<span data-ttu-id="fdb07-153">**ExportedGuestStateFilePaths**</span><span class="sxs-lookup"><span data-stu-id="fdb07-153">**ExportedGuestStateFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb07-154">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fdb07-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fdb07-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fdb07-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fdb07-156">Caminho do arquivo de estado de convidado da máquina virtual exportado.</span><span class="sxs-lookup"><span data-stu-id="fdb07-156">Path of the exported virtual machine guest state file.</span></span>

> [!Note]  
> <span data-ttu-id="fdb07-157">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="fdb07-157">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="fdb07-158">**ExportedLogFilePaths**</span><span class="sxs-lookup"><span data-stu-id="fdb07-158">**ExportedLogFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb07-159">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fdb07-159">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fdb07-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fdb07-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fdb07-161">Caminhos dos arquivos de log que foram exportados.</span><span class="sxs-lookup"><span data-stu-id="fdb07-161">Paths of the log files which were exported.</span></span>

</dd> <dt>

<span data-ttu-id="fdb07-162">**ExportedRuntimeFilePaths**</span><span class="sxs-lookup"><span data-stu-id="fdb07-162">**ExportedRuntimeFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb07-163">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fdb07-163">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fdb07-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fdb07-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fdb07-165">Caminho do arquivo de estado do tempo de execução da máquina virtual exportado.</span><span class="sxs-lookup"><span data-stu-id="fdb07-165">Path of the exported virtual machine runtime state file.</span></span>

</dd> <dt>

<span data-ttu-id="fdb07-166">**ReferencePointGroupId**</span><span class="sxs-lookup"><span data-stu-id="fdb07-166">**ReferencePointGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb07-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fdb07-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fdb07-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fdb07-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fdb07-169">GUID do ponto de referência de coleção que é exportado.</span><span class="sxs-lookup"><span data-stu-id="fdb07-169">GUID of the collection reference point which is exported.</span></span>

</dd> <dt>

<span data-ttu-id="fdb07-170">**VirtualMachineId**</span><span class="sxs-lookup"><span data-stu-id="fdb07-170">**VirtualMachineId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb07-171">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fdb07-171">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fdb07-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fdb07-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fdb07-173">GUID das máquinas virtuais para as quais a operação de exportação foi executada.</span><span class="sxs-lookup"><span data-stu-id="fdb07-173">GUID of the virtual machines for which export operation has been performed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fdb07-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdb07-174">Requirements</span></span>



| <span data-ttu-id="fdb07-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdb07-175">Requirement</span></span> | <span data-ttu-id="fdb07-176">Valor</span><span class="sxs-lookup"><span data-stu-id="fdb07-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdb07-177">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fdb07-177">Minimum supported client</span></span><br/> | <span data-ttu-id="fdb07-178">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="fdb07-178">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fdb07-179">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fdb07-179">Minimum supported server</span></span><br/> | <span data-ttu-id="fdb07-180">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fdb07-180">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="fdb07-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="fdb07-181">Namespace</span></span><br/>                | <span data-ttu-id="fdb07-182">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="fdb07-182">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fdb07-183">MOF</span><span class="sxs-lookup"><span data-stu-id="fdb07-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fdb07-184"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fdb07-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fdb07-185">DLL</span><span class="sxs-lookup"><span data-stu-id="fdb07-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdb07-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fdb07-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fdb07-187">Confira também</span><span class="sxs-lookup"><span data-stu-id="fdb07-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdb07-188">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="fdb07-188">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

