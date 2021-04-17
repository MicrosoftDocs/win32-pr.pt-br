---
description: Fornece informações adicionais a serem usadas com o método ExportSystemDefinition da classe Msvm \_ VirtualSystemManagementService.
ms.assetid: 86396A76-83EC-476E-86A9-83861A002152
title: Classe Msvm_VirtualSystemExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemExportSettingData
- Msvm_VirtualSystemExportSettingData.CaptureLiveState
- Msvm_VirtualSystemExportSettingData.InstanceID
- Msvm_VirtualSystemExportSettingData.Caption
- Msvm_VirtualSystemExportSettingData.Description
- Msvm_VirtualSystemExportSettingData.ElementName
- Msvm_VirtualSystemExportSettingData.CopySnapshotConfiguration
- Msvm_VirtualSystemExportSettingData.CopyVmRuntimeInformation
- Msvm_VirtualSystemExportSettingData.CopyVmStorage
- Msvm_VirtualSystemExportSettingData.CreateVmExportSubdirectory
- Msvm_VirtualSystemExportSettingData.SnapshotVirtualSystem
- Msvm_VirtualSystemExportSettingData.BackupIntent
- Msvm_VirtualSystemExportSettingData.ExportForLiveMigration
- Msvm_VirtualSystemExportSettingData.DisableDifferentialOfIgnoredStorage
- Msvm_VirtualSystemExportSettingData.ExcludedVirtualHardDisks
- Msvm_VirtualSystemExportSettingData.DifferentialBackupBase
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 77bd451912063ec1164abf14247d81e1d258f56f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775723"
---
# <a name="msvm_virtualsystemexportsettingdata-class"></a><span data-ttu-id="b3918-103">\_Classe Msvm VirtualSystemExportSettingData</span><span class="sxs-lookup"><span data-stu-id="b3918-103">Msvm\_VirtualSystemExportSettingData class</span></span>

<span data-ttu-id="b3918-104">Fornece informações adicionais a serem usadas com o método [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="b3918-104">Provides additional information to be used with the [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="b3918-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b3918-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3918-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3918-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemExportSettingData : CIM_SettingData
{
  uint8   CaptureLiveState;
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  uint8   CopySnapshotConfiguration;
  boolean CopyVmRuntimeInformation;
  boolean CopyVmStorage;
  boolean CreateVmExportSubdirectory;
  string  SnapshotVirtualSystem;
  uint8   BackupIntent;
  boolean ExportForLiveMigration;
  boolean DisableDifferentialOfIgnoredStorage;
  string  ExcludedVirtualHardDisks[];
  string  DifferentialBackupBase;
};
```

## <a name="members"></a><span data-ttu-id="b3918-107">Membros</span><span class="sxs-lookup"><span data-stu-id="b3918-107">Members</span></span>

<span data-ttu-id="b3918-108">A classe **Msvm \_ VirtualSystemExportSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b3918-108">The **Msvm\_VirtualSystemExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="b3918-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b3918-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b3918-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b3918-110">Properties</span></span>

<span data-ttu-id="b3918-111">A classe **Msvm \_ VirtualSystemExportSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b3918-111">The **Msvm\_VirtualSystemExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b3918-112">**BackupIntent**</span><span class="sxs-lookup"><span data-stu-id="b3918-112">**BackupIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3918-113">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="b3918-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b3918-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b3918-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3918-115">Indica a intenção de como os conjuntos de backup exportados seriam usados.</span><span class="sxs-lookup"><span data-stu-id="b3918-115">Indicates the intent on how the exported backup sets would be used.</span></span>

> [!Note]  
> <span data-ttu-id="b3918-116">Essa propriedade foi adicionada no Windows 10 e no Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="b3918-116">This property was added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span data-ttu-id="b3918-117"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (0)</span><span class="sxs-lookup"><span data-stu-id="b3918-117"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b3918-118">Todos os conjuntos de backup exportados completos e diferenciais seriam preservados como estão.</span><span class="sxs-lookup"><span data-stu-id="b3918-118">All exported full and differential backup sets would be preserved as they are.</span></span>

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span data-ttu-id="b3918-119"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (1)</span><span class="sxs-lookup"><span data-stu-id="b3918-119"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b3918-120">Os conjuntos de backup exportados completos e diferenciais seriam mesclados para sintetizar conjuntos de backup completos.</span><span class="sxs-lookup"><span data-stu-id="b3918-120">The exported full and differential backup sets would be merged to synthesize full backup sets.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b3918-121">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="b3918-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3918-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b3918-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3918-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b3918-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3918-124">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="b3918-124">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="b3918-125">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="b3918-125">A short description of the object.</span></span> <span data-ttu-id="b3918-126">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b3918-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b3918-127">**CaptureLiveState**</span><span class="sxs-lookup"><span data-stu-id="b3918-127">**CaptureLiveState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3918-128">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="b3918-128">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b3918-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b3918-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3918-130">Indica qual estado capturar se o destino da exportação for uma VM em execução.</span><span class="sxs-lookup"><span data-stu-id="b3918-130">Indicates what state to capture if the target of the export is a running VM.</span></span>

<dt>

<span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>

<span data-ttu-id="b3918-131"><span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>**CaptureCrashConsistentState** (0)</span><span class="sxs-lookup"><span data-stu-id="b3918-131"><span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>**CaptureCrashConsistentState** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b3918-132">Nenhum arquivo de estado salvo será exportado para a VM em execução, colocando-o em um estado consistente de falha.</span><span class="sxs-lookup"><span data-stu-id="b3918-132">No saved state files will be exported for the running VM, placing it in a crash consistent state.</span></span>

</dd> <dt>

<span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>

<span data-ttu-id="b3918-133"><span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>**CaptureSavedState** (1)</span><span class="sxs-lookup"><span data-stu-id="b3918-133"><span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>**CaptureSavedState** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b3918-134">Os arquivos de estado salvos para a VM em execução serão exportados junto com a configuração da VM.</span><span class="sxs-lookup"><span data-stu-id="b3918-134">Saved state files for the running VM will be exported along with the VM configuration.</span></span>

</dd> <dt>

<span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>

<span data-ttu-id="b3918-135"><span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>**CaptureAppConsistentState** (2)</span><span class="sxs-lookup"><span data-stu-id="b3918-135"><span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>**CaptureAppConsistentState** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b3918-136">O estado consistente com o aplicativo da VM em execução será exportado.</span><span class="sxs-lookup"><span data-stu-id="b3918-136">Application-consistent state of the running VM will be exported.</span></span>

> [!Note]  
> <span data-ttu-id="b3918-137">Adicionado ao Windows 10 e ao Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="b3918-137">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b3918-138">**CopySnapshotConfiguration**</span><span class="sxs-lookup"><span data-stu-id="b3918-138">**CopySnapshotConfiguration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3918-139">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="b3918-139">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b3918-140">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b3918-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3918-141">Indica quais instantâneos devem ser exportados com a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b3918-141">Indicates what snapshots are to be exported with the virtual machine.</span></span>

<dt>

<span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>

<span data-ttu-id="b3918-142"><span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>**ExportAllSnapshots** (0)</span><span class="sxs-lookup"><span data-stu-id="b3918-142"><span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>**ExportAllSnapshots** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b3918-143">Todos os instantâneos serão exportados com a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b3918-143">All snapshots will be exported with the virtual machine.</span></span>

</dd> <dt>

<span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>

<span data-ttu-id="b3918-144"><span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>**ExportNoSnapshots** (1)</span><span class="sxs-lookup"><span data-stu-id="b3918-144"><span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>**ExportNoSnapshots** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b3918-145">Nenhum instantâneo será exportado com a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b3918-145">No snapshots will be exported with the virtual machine.</span></span>

</dd> <dt>

<span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>

<span data-ttu-id="b3918-146"><span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>**ExportOneSnapshot** (2)</span><span class="sxs-lookup"><span data-stu-id="b3918-146"><span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>**ExportOneSnapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b3918-147">Os instantâneos identificados pela propriedade **SnapshotVirtualSystem** serão exportados com a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b3918-147">The snapshots identified by the **SnapshotVirtualSystem** property will be exported with the virtual machine.</span></span> <span data-ttu-id="b3918-148">As propriedades **CopyVmStorage** e **CopyVmRuntimeInformation** são ignoradas, as informações de armazenamento e tempo de execução são exportadas com a máquina virtual e todos os discos diferenciais VHD serão mesclados em um novo VHD.</span><span class="sxs-lookup"><span data-stu-id="b3918-148">The **CopyVmStorage** and **CopyVmRuntimeInformation** properties are ignored, storage and run-time information is exported with the virtual machine, and any VHD differencing disks will be merged into a new VHD.</span></span>

</dd> <dt>

<span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>

<span data-ttu-id="b3918-149"><span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>**ExportOneSnapshotForBackup** (3)</span><span class="sxs-lookup"><span data-stu-id="b3918-149"><span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>**ExportOneSnapshotForBackup** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b3918-150">O instantâneo identificado pela propriedade **SnapshotVirtualSystem** será exportado para fins de backup da VM.</span><span class="sxs-lookup"><span data-stu-id="b3918-150">The snapshot identified by the **SnapshotVirtualSystem** property will be exported for the purpose of backing up the VM.</span></span> <span data-ttu-id="b3918-151">A configuração exportada usará a ID da VM.</span><span class="sxs-lookup"><span data-stu-id="b3918-151">The exported configuration will use ID of the VM.</span></span>

> [!Note]  
> <span data-ttu-id="b3918-152">Adicionado ao Windows 10 e ao Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="b3918-152">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b3918-153">**CopyVmRuntimeInformation**</span><span class="sxs-lookup"><span data-stu-id="b3918-153">**CopyVmRuntimeInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3918-154">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b3918-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b3918-155">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b3918-155">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3918-156">Indica se as informações de tempo de execução da máquina virtual serão copiadas quando a máquina virtual for exportada.</span><span class="sxs-lookup"><span data-stu-id="b3918-156">Indicates whether the virtual machine run-time information will be copied when the virtual machine is exported.</span></span>



| <span data-ttu-id="b3918-157">Valor</span><span class="sxs-lookup"><span data-stu-id="b3918-157">Value</span></span>                                                                                | <span data-ttu-id="b3918-158">Significado</span><span class="sxs-lookup"><span data-stu-id="b3918-158">Meaning</span></span>                                                                 |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3918-159"><dt>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="b3918-159"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="b3918-160">As informações de tempo de execução da máquina virtual serão copiadas.</span><span class="sxs-lookup"><span data-stu-id="b3918-160">The virtual machine run-time information will be copied.</span></span><br/>     |
| <dl> <span data-ttu-id="b3918-161"><dt>**For**</dt></span><span class="sxs-lookup"><span data-stu-id="b3918-161"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="b3918-162">As informações de tempo de execução da máquina virtual não serão copiadas.</span><span class="sxs-lookup"><span data-stu-id="b3918-162">The virtual machine run-time information will not be copied.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b3918-163">**CopyVmStorage**</span><span class="sxs-lookup"><span data-stu-id="b3918-163">**CopyVmStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3918-164">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b3918-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b3918-165">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b3918-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3918-166">Indica se o armazenamento da máquina virtual será copiado quando a máquina virtual for exportada.</span><span class="sxs-lookup"><span data-stu-id="b3918-166">Indicates whether the virtual machine storage will be copied when the virtual machine is exported.</span></span>



| <span data-ttu-id="b3918-167">Valor</span><span class="sxs-lookup"><span data-stu-id="b3918-167">Value</span></span>                                                                                | <span data-ttu-id="b3918-168">Significado</span><span class="sxs-lookup"><span data-stu-id="b3918-168">Meaning</span></span>                                                    |
|--------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="b3918-169"><dt>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="b3918-169"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="b3918-170">O armazenamento da máquina virtual será copiado.</span><span class="sxs-lookup"><span data-stu-id="b3918-170">The virtual machine storage will be copied.</span></span><br/>     |
| <dl> <span data-ttu-id="b3918-171"><dt>**For**</dt></span><span class="sxs-lookup"><span data-stu-id="b3918-171"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="b3918-172">O armazenamento da máquina virtual não será copiado.</span><span class="sxs-lookup"><span data-stu-id="b3918-172">The virtual machine storage will not be copied.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b3918-173">**CreateVmExportSubdirectory**</span><span class="sxs-lookup"><span data-stu-id="b3918-173">**CreateVmExportSubdirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3918-174">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b3918-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b3918-175">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b3918-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3918-176">Indica se um subdiretório com o nome da máquina virtual será criado quando a máquina virtual for exportada.</span><span class="sxs-lookup"><span data-stu-id="b3918-176">Indicates whether a subdirectory with the name of the virtual machine will be created when the virtual machine is exported.</span></span>



| <span data-ttu-id="b3918-177">Valor</span><span class="sxs-lookup"><span data-stu-id="b3918-177">Value</span></span>                                                                                | <span data-ttu-id="b3918-178">Significado</span><span class="sxs-lookup"><span data-stu-id="b3918-178">Meaning</span></span>                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="b3918-179"><dt>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="b3918-179"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="b3918-180">Um subdiretório será criado.</span><span class="sxs-lookup"><span data-stu-id="b3918-180">A subdirectory will be created.</span></span><br/>     |
| <dl> <span data-ttu-id="b3918-181"><dt>**For**</dt></span><span class="sxs-lookup"><span data-stu-id="b3918-181"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="b3918-182">Um subdiretório não será criado.</span><span class="sxs-lookup"><span data-stu-id="b3918-182">A subdirectory will not be created.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b3918-183">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b3918-183">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3918-184">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b3918-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3918-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b3918-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3918-186">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="b3918-186">A description of the object.</span></span> <span data-ttu-id="b3918-187">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b3918-187">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b3918-188">**DifferentialBackupBase**</span><span class="sxs-lookup"><span data-stu-id="b3918-188">**DifferentialBackupBase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3918-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b3918-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3918-190">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b3918-190">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3918-191">Base para exportação diferencial.</span><span class="sxs-lookup"><span data-stu-id="b3918-191">Base for differential export.</span></span> <span data-ttu-id="b3918-192">Esse é o caminho para uma instância [**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) que representa o ponto de referência ou o caminho para uma instância [**\_ VirtualSystemSettingData Msvm**](msvm-virtualsystemsettingdata.md) que representa o instantâneo a ser usado como base para a exportação diferencial.</span><span class="sxs-lookup"><span data-stu-id="b3918-192">This is either path to a [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance that represents the reference point or path to a [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instance that represents the snapshot to be used as a base for differential export.</span></span> <span data-ttu-id="b3918-193">Se a propriedade **CopySnapshotConfiguration** não estiver definida como 3 (**ExportOneSnapshotForBackup**), essa propriedade será ignorada.</span><span class="sxs-lookup"><span data-stu-id="b3918-193">If the **CopySnapshotConfiguration** property is not set to 3(**ExportOneSnapshotForBackup**), this property is ignored.</span></span>

> [!Note]  
> <span data-ttu-id="b3918-194">Adicionado ao Windows 10 e ao Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="b3918-194">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="b3918-195">**DisableDifferentialOfIgnoredStorage**</span><span class="sxs-lookup"><span data-stu-id="b3918-195">**DisableDifferentialOfIgnoredStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3918-196">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b3918-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b3918-197">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b3918-197">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3918-198">Indica se os discos diferenciais serão criados ou não para armazenamento ignorado durante a exportação.</span><span class="sxs-lookup"><span data-stu-id="b3918-198">Indicates whether differencing disks will be created or not for storage ignored during export.</span></span> <span data-ttu-id="b3918-199">Por padrão, isso é definido como false, o que significa que os discos diferenciais são criados para o armazenamento que não será copiado para o destino de exportação.</span><span class="sxs-lookup"><span data-stu-id="b3918-199">By default this is set to false, which means that differencing disks are created for the storage that is not going to be copied over to the export destination.</span></span>

> [!Note]  
> <span data-ttu-id="b3918-200">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="b3918-200">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="b3918-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b3918-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3918-202">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b3918-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3918-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b3918-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3918-204">O nome de exibição desta instância.</span><span class="sxs-lookup"><span data-stu-id="b3918-204">The display name for this instance.</span></span> <span data-ttu-id="b3918-205">Além disso, o nome de exibição pode ser usado como uma propriedade de índice para uma pesquisa ou consulta.</span><span class="sxs-lookup"><span data-stu-id="b3918-205">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="b3918-206">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b3918-206">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b3918-207">**ExcludedVirtualHardDisks**</span><span class="sxs-lookup"><span data-stu-id="b3918-207">**ExcludedVirtualHardDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3918-208">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b3918-208">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b3918-209">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b3918-209">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3918-210">Matriz de IDs de instância de RASD ( [**Msvm \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) ) que representam os discos rígidos virtuais que são solicitados a serem excluídos da operação de exportação.</span><span class="sxs-lookup"><span data-stu-id="b3918-210">Array of [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) (RASD) instance IDs that represent the virtual hard disks that are requested to be excluded from the export operation.</span></span> <span data-ttu-id="b3918-211">Se pelo menos uma das IDs fornecidas não for um disco rígido virtual anexado válido, a operação falhará.</span><span class="sxs-lookup"><span data-stu-id="b3918-211">If at least one of the supplied IDs is not a valid attached virtual hard disk, the operation will fail.</span></span>

<span data-ttu-id="b3918-212">Os discos rígidos virtuais referenciados por essa propriedade podem ser da VM e/ou de qualquer um de seus instantâneos.</span><span class="sxs-lookup"><span data-stu-id="b3918-212">The virtual hard disks referenced by this property may be from the VM and/or from any of its snapshots.</span></span> <span data-ttu-id="b3918-213">Não há suporte para a exclusão de discos rígidos virtuais quando a propriedade **CopySnapshotConfiguration** está definida como 0 (ExportAllSnapshots).</span><span class="sxs-lookup"><span data-stu-id="b3918-213">Exclusion of virtual hard disks is not supported when property **CopySnapshotConfiguration** is set to 0(ExportAllSnapshots).</span></span>

<span data-ttu-id="b3918-214">Observe que a ID da instância do RASD para discos rígidos virtuais representa o local ao qual eles estão anexados e a exclusão por meio dessa ID exclui todos os discos rígidos virtuais anexados nesse local na árvore de instantâneo da máquina virtual, independentemente de serem realmente uma cadeia de disco rígido virtual válida.</span><span class="sxs-lookup"><span data-stu-id="b3918-214">Note that the RASD instance ID for virtual hard disks represents the location they are attached to, and excluding through this ID excludes all virtual hard disks attached in that location throughout the virtual machine's snapshot tree, regardless of them really being a valid virtual hard disk chain.</span></span>

> [!Note]  
> <span data-ttu-id="b3918-215">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="b3918-215">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="b3918-216">**ExportForLiveMigration**</span><span class="sxs-lookup"><span data-stu-id="b3918-216">**ExportForLiveMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3918-217">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b3918-217">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b3918-218">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b3918-218">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3918-219">Indica se a VM exportada deve ser usada na migração dinâmica.</span><span class="sxs-lookup"><span data-stu-id="b3918-219">Indicates whether the exported VM is intended to be used in live migration.</span></span>

> [!Note]  
> <span data-ttu-id="b3918-220">Adicionado no Windows 10, versão 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="b3918-220">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="b3918-221">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b3918-221">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3918-222">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b3918-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3918-223">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b3918-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3918-224">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="b3918-224">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b3918-225">Dentro do escopo do namespace de instanciação, ele identifica de forma opaca e exclusiva uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="b3918-225">Within the scope of the instantiating Namespace, opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b3918-226">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b3918-226">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b3918-227">**SnapshotVirtualSystem**</span><span class="sxs-lookup"><span data-stu-id="b3918-227">**SnapshotVirtualSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3918-228">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b3918-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3918-229">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b3918-229">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3918-230">Caminho para uma instância de [**\_ VirtualSystemSettingData Msvm**](msvm-virtualsystemsettingdata.md) que representa o instantâneo a ser exportado com a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b3918-230">Path to a [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instance that represents the snapshot to be exported with the virtual machine.</span></span> <span data-ttu-id="b3918-231">Se a propriedade **CopySnapshotConfiguration** não estiver definida como 2 (ExportOneSnapshot), essa propriedade será ignorada.</span><span class="sxs-lookup"><span data-stu-id="b3918-231">If the **CopySnapshotConfiguration** property is not set to 2 (ExportOneSnapshot), this property is ignored.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3918-232">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3918-232">Remarks</span></span>

<span data-ttu-id="b3918-233">O acesso à classe **Msvm \_ VirtualSystemExportSettingData** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="b3918-233">Access to the **Msvm\_VirtualSystemExportSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b3918-234">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b3918-234">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3918-235">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3918-235">Requirements</span></span>



| <span data-ttu-id="b3918-236">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3918-236">Requirement</span></span> | <span data-ttu-id="b3918-237">Valor</span><span class="sxs-lookup"><span data-stu-id="b3918-237">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3918-238">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3918-238">Minimum supported client</span></span><br/> | <span data-ttu-id="b3918-239">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b3918-239">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b3918-240">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3918-240">Minimum supported server</span></span><br/> | <span data-ttu-id="b3918-241">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b3918-241">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b3918-242">Namespace</span><span class="sxs-lookup"><span data-stu-id="b3918-242">Namespace</span></span><br/>                | <span data-ttu-id="b3918-243">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="b3918-243">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b3918-244">MOF</span><span class="sxs-lookup"><span data-stu-id="b3918-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3918-245"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3918-245"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3918-246">DLL</span><span class="sxs-lookup"><span data-stu-id="b3918-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3918-247"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b3918-247"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b3918-248">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3918-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3918-249">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="b3918-249">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="b3918-250">Classes de gerenciamento do sistema virtual</span><span class="sxs-lookup"><span data-stu-id="b3918-250">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> <dt>

[<span data-ttu-id="b3918-251">**ExportSystemDefinition**</span><span class="sxs-lookup"><span data-stu-id="b3918-251">**ExportSystemDefinition**</span></span>](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

