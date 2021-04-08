---
description: Representa as configurações específicas de virtualização para uma máquina virtual.
ms.assetid: BE81405E-E773-41CE-9441-33D60B63550E
title: Classe Msvm_VirtualSystemSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingData
- Msvm_VirtualSystemSettingData.InstanceID
- Msvm_VirtualSystemSettingData.Caption
- Msvm_VirtualSystemSettingData.Description
- Msvm_VirtualSystemSettingData.ElementName
- Msvm_VirtualSystemSettingData.VirtualSystemIdentifier
- Msvm_VirtualSystemSettingData.VirtualSystemType
- Msvm_VirtualSystemSettingData.Notes
- Msvm_VirtualSystemSettingData.CreationTime
- Msvm_VirtualSystemSettingData.ConfigurationID
- Msvm_VirtualSystemSettingData.ConfigurationDataRoot
- Msvm_VirtualSystemSettingData.ConfigurationFile
- Msvm_VirtualSystemSettingData.SnapshotDataRoot
- Msvm_VirtualSystemSettingData.SuspendDataRoot
- Msvm_VirtualSystemSettingData.SwapFileDataRoot
- Msvm_VirtualSystemSettingData.LogDataRoot
- Msvm_VirtualSystemSettingData.AutomaticStartupAction
- Msvm_VirtualSystemSettingData.AutomaticStartupActionDelay
- Msvm_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualSystemSettingData.AutomaticShutdownAction
- Msvm_VirtualSystemSettingData.AutomaticRecoveryAction
- Msvm_VirtualSystemSettingData.RecoveryFile
- Msvm_VirtualSystemSettingData.BIOSGUID
- Msvm_VirtualSystemSettingData.BIOSSerialNumber
- Msvm_VirtualSystemSettingData.BaseBoardSerialNumber
- Msvm_VirtualSystemSettingData.ChassisSerialNumber
- Msvm_VirtualSystemSettingData.Architecture
- Msvm_VirtualSystemSettingData.ChassisAssetTag
- Msvm_VirtualSystemSettingData.BIOSNumLock
- Msvm_VirtualSystemSettingData.BootOrder
- Msvm_VirtualSystemSettingData.Parent
- Msvm_VirtualSystemSettingData.UserSnapshotType
- Msvm_VirtualSystemSettingData.IsSaved
- Msvm_VirtualSystemSettingData.AdditionalRecoveryInformation
- Msvm_VirtualSystemSettingData.AllowFullSCSICommandSet
- Msvm_VirtualSystemSettingData.DebugChannelId
- Msvm_VirtualSystemSettingData.DebugPortEnabled
- Msvm_VirtualSystemSettingData.DebugPort
- Msvm_VirtualSystemSettingData.Version
- Msvm_VirtualSystemSettingData.IncrementalBackupEnabled
- Msvm_VirtualSystemSettingData.VirtualNumaEnabled
- Msvm_VirtualSystemSettingData.AllowReducedFcRedundancy
- Msvm_VirtualSystemSettingData.VirtualSystemSubType
- Msvm_VirtualSystemSettingData.BootSourceOrder
- Msvm_VirtualSystemSettingData.PauseAfterBootFailure
- Msvm_VirtualSystemSettingData.NetworkBootPreferredProtocol
- Msvm_VirtualSystemSettingData.GuestControlledCacheTypes
- Msvm_VirtualSystemSettingData.AutomaticSnapshotsEnabled
- Msvm_VirtualSystemSettingData.IsAutomaticSnapshot
- Msvm_VirtualSystemSettingData.GuestStateFile
- Msvm_VirtualSystemSettingData.GuestStateDataRoot
- Msvm_VirtualSystemSettingData.LockOnDisconnect
- Msvm_VirtualSystemSettingData.ParentPackage
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorActionTimeout
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorAction
- Msvm_VirtualSystemSettingData.ConsoleMode
- Msvm_VirtualSystemSettingData.SecureBootEnabled
- Msvm_VirtualSystemSettingData.SecureBootTemplateId
- Msvm_VirtualSystemSettingData.LowMmioGapSize
- Msvm_VirtualSystemSettingData.HighMmioGapSize
- Msvm_VirtualSystemSettingData.EnhancedSessionTransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2787abbacfe4220b135544eecd3aeb7e86596c81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920722"
---
# <a name="msvm_virtualsystemsettingdata-class"></a><span data-ttu-id="1b55d-103">\_Classe Msvm VirtualSystemSettingData</span><span class="sxs-lookup"><span data-stu-id="1b55d-103">Msvm\_VirtualSystemSettingData class</span></span>

<span data-ttu-id="1b55d-104">Representa as configurações específicas de virtualização para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1b55d-104">Represents the virtualization-specific settings for a virtual machine.</span></span>

<span data-ttu-id="1b55d-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1b55d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b55d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1b55d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption = "Virtual Machine Settings";
  string   Description;
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   Architecture;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
  string   Parent;
  uint16   UserSnapshotType;
  boolean  IsSaved;
  string   AdditionalRecoveryInformation;
  boolean  AllowFullSCSICommandSet;
  uint32   DebugChannelId;
  uint16   DebugPortEnabled;
  uint32   DebugPort;
  string   Version;
  boolean  IncrementalBackupEnabled;
  boolean  VirtualNumaEnabled;
  boolean  AllowReducedFcRedundancy = False;
  string   VirtualSystemSubType;
  string   BootSourceOrder[];
  boolean  PauseAfterBootFailure;
  uint16   NetworkBootPreferredProtocol;
  boolean  GuestControlledCacheTypes;
  boolean  AutomaticSnapshotsEnabled;
  boolean  IsAutomaticSnapshot;
  string   GuestStateFile;
  string   GuestStateDataRoot;
  boolean  LockOnDisconnect;
  string   ParentPackage;
  datetime AutomaticCriticalErrorActionTimeout;
  uint16   AutomaticCriticalErrorAction;
  uint16   ConsoleMode;
  boolean  SecureBootEnabled;
  string   SecureBootTemplateId;
  uint64   LowMmioGapSize;
  uint64   HighMmioGapSize;
  uint16   EnhancedSessionTransportType;
};
```

## <a name="members"></a><span data-ttu-id="1b55d-107">Membros</span><span class="sxs-lookup"><span data-stu-id="1b55d-107">Members</span></span>

<span data-ttu-id="1b55d-108">A classe **Msvm \_ VirtualSystemSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1b55d-108">The **Msvm\_VirtualSystemSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="1b55d-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1b55d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1b55d-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1b55d-110">Properties</span></span>

<span data-ttu-id="1b55d-111">A classe **Msvm \_ VirtualSystemSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1b55d-111">The **Msvm\_VirtualSystemSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1b55d-112">**AdditionalRecoveryInformation**</span><span class="sxs-lookup"><span data-stu-id="1b55d-112">**AdditionalRecoveryInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-115">Quaisquer informações adicionais fornecidas para a ação de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1b55d-115">Any additional information provided to the recovery action.</span></span> <span data-ttu-id="1b55d-116">O significado dessa propriedade é definido pela ação em **AutomaticRecoveryAction**.</span><span class="sxs-lookup"><span data-stu-id="1b55d-116">The meaning of this property is defined by the action in **AutomaticRecoveryAction**.</span></span> <span data-ttu-id="1b55d-117">Se **AutomaticRecoveryAction** for 0 ("None") ou 1 ("restart"), esse valor será **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1b55d-117">If **AutomaticRecoveryAction** is 0 ("None") or 1 ("Restart"), this value is **Null**.</span></span> <span data-ttu-id="1b55d-118">Se **AutomaticRecoveryAction** for 2 ("reverter para instantâneo"), esse será o caminho do objeto para um instantâneo que deve ser aplicado em caso de falha do processo de trabalho da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1b55d-118">If **AutomaticRecoveryAction** is 2 ("Revert to Snapshot"), this is the object path to a snapshot that should be applied on failure of the virtual machine worker process.</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-119">**AllowFullSCSICommandSet**</span><span class="sxs-lookup"><span data-stu-id="1b55d-119">**AllowFullSCSICommandSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-120">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1b55d-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-122">**True** se os comandos SCSI do sistema operacional convidado forem passados para discos de passagem; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="1b55d-122">**True** if SCSI commands from the guest operating system are passed to pass-through disks; otherwise, **False**.</span></span> <span data-ttu-id="1b55d-123">Se **for verdadeiro**, os comandos SCSI emitidos pelo sistema operacional convidado para discos de passagem não serão filtrados.</span><span class="sxs-lookup"><span data-stu-id="1b55d-123">If **True**, SCSI commands emitted by the guest operating system to pass-through disks are not filtered.</span></span> <span data-ttu-id="1b55d-124">Recomendamos que a filtragem de SCSI permaneça habilitada para implantações de produção.</span><span class="sxs-lookup"><span data-stu-id="1b55d-124">We recommend that SCSI filtering remain enabled for production deployments.</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-125">**AllowReducedFcRedundancy**</span><span class="sxs-lookup"><span data-stu-id="1b55d-125">**AllowReducedFcRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-126">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1b55d-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-128">Especifica se a migração dinâmica de uma máquina virtual configurada com um adaptador de Fibre Channel virtual é permitida para um computador de destino que pode não ter caminhos ou não reduzidos para os dispositivos de Fibre Channel de destino.</span><span class="sxs-lookup"><span data-stu-id="1b55d-128">Specifies whether live migration of a virtual machine that is configured with a virtual Fibre Channel adapter is allowed to a destination computer that may have no or reduced paths to the target Fibre Channel devices.</span></span> <span data-ttu-id="1b55d-129">Essa propriedade deve ser limpa após uma migração ao vivo.</span><span class="sxs-lookup"><span data-stu-id="1b55d-129">This property should be cleared after a live migration.</span></span>



| <span data-ttu-id="1b55d-130">Valor</span><span class="sxs-lookup"><span data-stu-id="1b55d-130">Value</span></span>                                                                            | <span data-ttu-id="1b55d-131">Significado</span><span class="sxs-lookup"><span data-stu-id="1b55d-131">Meaning</span></span>                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1b55d-132"><dt>Falso</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-132"><dt>False</dt></span></span> </dl> | <span data-ttu-id="1b55d-133">A máquina virtual não pode ser migrada ao vivo para um computador de destino que pode não ter um ou menos caminhos para os dispositivos de Fibre Channel de destino.</span><span class="sxs-lookup"><span data-stu-id="1b55d-133">The virtual machine cannot be live migrated to a target computer that may have no or reduced paths to the target Fibre Channel devices.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="1b55d-134"><dt>True</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-134"><dt>True</dt></span></span> </dl>  | <span data-ttu-id="1b55d-135">A máquina virtual pode ser migrada ao vivo para um computador de destino que pode não ter um ou menos caminhos para os dispositivos de Fibre Channel de destino.</span><span class="sxs-lookup"><span data-stu-id="1b55d-135">The virtual machine can be live migrated to a target computer that may have no or reduced paths to the target Fibre Channel devices.</span></span> <span data-ttu-id="1b55d-136">O sistema operacional convidado pode perder conectividade com o armazenamento e pode se comportar de maneira imprevisível.</span><span class="sxs-lookup"><span data-stu-id="1b55d-136">The guest operating system may lose connectivity to storage and may behave in an unpredictable manner.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1b55d-137">**Arquitetura**</span><span class="sxs-lookup"><span data-stu-id="1b55d-137">**Architecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-140">A arquitetura deste sistema.</span><span class="sxs-lookup"><span data-stu-id="1b55d-140">The architecture of this system.</span></span>

> [!Note]  
> <span data-ttu-id="1b55d-141">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="1b55d-141">Added in Windows 10, version 1709.</span></span>

 

<dt>

<span id="x64"></span><span id="X64"></span>

<span data-ttu-id="1b55d-142">**x64** ()</span><span class="sxs-lookup"><span data-stu-id="1b55d-142">**x64** ()</span></span>


</dt> <dd></dd> <dt>

<span id="arm64"></span><span id="ARM64"></span>

<span data-ttu-id="1b55d-143">**arm64** ()</span><span class="sxs-lookup"><span data-stu-id="1b55d-143">**arm64** ()</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1b55d-144">**AutomaticCriticalErrorAction**</span><span class="sxs-lookup"><span data-stu-id="1b55d-144">**AutomaticCriticalErrorAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-145">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b55d-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-146">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-147">Identifica a ação a ser executada na VM, quando ocorre um erro crítico, como o armazenamento desconectado.</span><span class="sxs-lookup"><span data-stu-id="1b55d-147">Identifies the action to be taken on VM, when a critical error happens, like storage disconnect.</span></span>

> [!Note]  
> <span data-ttu-id="1b55d-148">Adicionado ao Windows 10 e ao Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="1b55d-148">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="1b55d-149"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Nenhum** (0)</span><span class="sxs-lookup"><span data-stu-id="1b55d-149"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1b55d-150">Nenhuma ação específica será tomada para condições de erro críticas.</span><span class="sxs-lookup"><span data-stu-id="1b55d-150">No specific action will be taken for critical error conditions.</span></span>

</dd> <dt>

<span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>

<span data-ttu-id="1b55d-151"><span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>**Pausar retomar** (1)</span><span class="sxs-lookup"><span data-stu-id="1b55d-151"><span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>**Pause Resume** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1b55d-152">Faz com que a VM seja pausada e retomada automaticamente quando a condição de erro crítico for resolvida.</span><span class="sxs-lookup"><span data-stu-id="1b55d-152">Causes the VM to be paused and automatically resumed when the critical error condition is resolved.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1b55d-153">**AutomaticCriticalErrorActionTimeout**</span><span class="sxs-lookup"><span data-stu-id="1b55d-153">**AutomaticCriticalErrorActionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-154">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1b55d-154">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-155">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-156">Qualificadores: [**subtipo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Interval")</span><span class="sxs-lookup"><span data-stu-id="1b55d-156">Qualifiers: [**SubType**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("interval")</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-157">Identifica a duração máxima para a qual o **AutomaticCriticalErrorAction** será executado para resolver o erro crítico.</span><span class="sxs-lookup"><span data-stu-id="1b55d-157">Identifies the maximum duration for which the **AutomaticCriticalErrorAction** will be performed to resolve the critical error.</span></span> <span data-ttu-id="1b55d-158">Isso é aplicável somente quando o valor da propriedade **AutomaticCriticalErrorAction** não é 0 (None).</span><span class="sxs-lookup"><span data-stu-id="1b55d-158">This is applicable only when the value of the **AutomaticCriticalErrorAction** property is not 0 (None).</span></span> <span data-ttu-id="1b55d-159">Quando o tempo limite expirar, a VM será desligada.</span><span class="sxs-lookup"><span data-stu-id="1b55d-159">Once the timeout expires, the VM will be powered off.</span></span> <span data-ttu-id="1b55d-160">O valor será arredondado para o minuto mais próximo.</span><span class="sxs-lookup"><span data-stu-id="1b55d-160">The value will be rounded up to the nearest minute.</span></span> <span data-ttu-id="1b55d-161">Um valor de 0 implica que a VM deve ser desligada imediatamente quando encontra uma condição de erro crítica.</span><span class="sxs-lookup"><span data-stu-id="1b55d-161">A value of 0 implies that the VM should be powered off immediately when it encounters a critical error condition.</span></span>

> [!Note]  
> <span data-ttu-id="1b55d-162">Adicionado ao Windows 10 e ao Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="1b55d-162">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="1b55d-163">**AutomaticRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="1b55d-163">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-164">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b55d-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-166">Ação a ser tomada para a máquina virtual quando o software executado pela máquina virtual falha.</span><span class="sxs-lookup"><span data-stu-id="1b55d-166">Action to take for the virtual machine when the software executed by the virtual machine fails.</span></span> <span data-ttu-id="1b55d-167">As falhas nesse caso significam uma falha que é detectável pela plataforma de host, como uma condição de estado de espera noninterruptible.</span><span class="sxs-lookup"><span data-stu-id="1b55d-167">Failures in this case means a failure that is detectable by the host platform, such as a noninterruptible wait state condition.</span></span> <span data-ttu-id="1b55d-168">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b55d-168">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="1b55d-169">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1b55d-169">This can be one of the following values.</span></span>



| <span data-ttu-id="1b55d-170">Valor</span><span class="sxs-lookup"><span data-stu-id="1b55d-170">Value</span></span>                                                                               | <span data-ttu-id="1b55d-171">Significado</span><span class="sxs-lookup"><span data-stu-id="1b55d-171">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="1b55d-172"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-172"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="1b55d-173">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="1b55d-173">None.</span></span><br/>               |
| <dl> <span data-ttu-id="1b55d-174"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-174"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="1b55d-175">Reiniciar.</span><span class="sxs-lookup"><span data-stu-id="1b55d-175">Restart.</span></span><br/>            |
| <dl> <span data-ttu-id="1b55d-176"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-176"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="1b55d-177">Reverter para instantâneo.</span><span class="sxs-lookup"><span data-stu-id="1b55d-177">Revert to snapshot.</span></span><br/> |
| <dl> <span data-ttu-id="1b55d-178"><dt>5.. 32768</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-178"><dt>5..32768</dt></span></span> </dl> | <span data-ttu-id="1b55d-179">Reservado.</span><span class="sxs-lookup"><span data-stu-id="1b55d-179">Reserved.</span></span><br/>           |



 

</dd> <dt>

<span data-ttu-id="1b55d-180">**AutomaticShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="1b55d-180">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-181">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b55d-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-183">Ação a ser tomada para a máquina virtual quando o host for desligado.</span><span class="sxs-lookup"><span data-stu-id="1b55d-183">Action to take for the virtual machine when the host is shut down.</span></span> <span data-ttu-id="1b55d-184">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b55d-184">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="1b55d-185">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1b55d-185">This can be one of the following values.</span></span>



| <span data-ttu-id="1b55d-186">Valor</span><span class="sxs-lookup"><span data-stu-id="1b55d-186">Value</span></span>                                                                               | <span data-ttu-id="1b55d-187">Significado</span><span class="sxs-lookup"><span data-stu-id="1b55d-187">Meaning</span></span>                |
|-------------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="1b55d-188"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-188"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="1b55d-189">Desativar.</span><span class="sxs-lookup"><span data-stu-id="1b55d-189">Turn off.</span></span><br/>   |
| <dl> <span data-ttu-id="1b55d-190"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-190"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="1b55d-191">Salvar estado.</span><span class="sxs-lookup"><span data-stu-id="1b55d-191">Save state.</span></span><br/> |
| <dl> <span data-ttu-id="1b55d-192"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-192"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="1b55d-193">Desligar.</span><span class="sxs-lookup"><span data-stu-id="1b55d-193">Shutdown.</span></span><br/>   |
| <dl> <span data-ttu-id="1b55d-194"><dt>5.. 32768</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-194"><dt>5..32768</dt></span></span> </dl> | <span data-ttu-id="1b55d-195">Reservado.</span><span class="sxs-lookup"><span data-stu-id="1b55d-195">Reserved.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="1b55d-196">**AutomaticSnapshotsEnabled**</span><span class="sxs-lookup"><span data-stu-id="1b55d-196">**AutomaticSnapshotsEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-197">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1b55d-197">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-198">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-198">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-199">Indica se esta máquina virtual deve ter instantâneos automáticos habilitados.</span><span class="sxs-lookup"><span data-stu-id="1b55d-199">Indicates whether this virtual machine should have automatic snapshots enabled.</span></span>

> [!Note]  
> <span data-ttu-id="1b55d-200">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="1b55d-200">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="1b55d-201">**AutomaticStartupAction**</span><span class="sxs-lookup"><span data-stu-id="1b55d-201">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-202">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b55d-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-204">Ação a ser tomada para a máquina virtual quando o host for iniciado.</span><span class="sxs-lookup"><span data-stu-id="1b55d-204">Action to take for the virtual machine when the host is started.</span></span> <span data-ttu-id="1b55d-205">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b55d-205">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="1b55d-206">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1b55d-206">This can be one of the following values.</span></span>



| <span data-ttu-id="1b55d-207">Valor</span><span class="sxs-lookup"><span data-stu-id="1b55d-207">Value</span></span>                                                                               | <span data-ttu-id="1b55d-208">Significado</span><span class="sxs-lookup"><span data-stu-id="1b55d-208">Meaning</span></span>                                  |
|-------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="1b55d-209"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-209"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="1b55d-210">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="1b55d-210">None.</span></span><br/>                         |
| <dl> <span data-ttu-id="1b55d-211"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-211"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="1b55d-212">Reinicie o se estiver ativo anteriormente.</span><span class="sxs-lookup"><span data-stu-id="1b55d-212">Restart if previously active.</span></span><br/> |
| <dl> <span data-ttu-id="1b55d-213"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-213"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="1b55d-214">Sempre iniciar.</span><span class="sxs-lookup"><span data-stu-id="1b55d-214">Always start.</span></span><br/>                 |
| <dl> <span data-ttu-id="1b55d-215"><dt>5.. 32768</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-215"><dt>5..32768</dt></span></span> </dl> | <span data-ttu-id="1b55d-216">Reservado.</span><span class="sxs-lookup"><span data-stu-id="1b55d-216">Reserved.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="1b55d-217">**AutomaticStartupActionDelay**</span><span class="sxs-lookup"><span data-stu-id="1b55d-217">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-218">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1b55d-218">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-219">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-220">O tempo de atraso antes que a máquina virtual seja iniciada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="1b55d-220">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="1b55d-221">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b55d-221">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-222">**AutomaticStartupActionSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="1b55d-222">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-223">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b55d-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-225">Um número que indica a sequência relativa de ativação da máquina virtual quando o sistema host é iniciado.</span><span class="sxs-lookup"><span data-stu-id="1b55d-225">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="1b55d-226">Um número mais baixo indica ativação anterior.</span><span class="sxs-lookup"><span data-stu-id="1b55d-226">A lower number indicates earlier activation.</span></span> <span data-ttu-id="1b55d-227">Se uma ou mais configurações mostrarem o mesmo valor, a sequência será dependente da implementação.</span><span class="sxs-lookup"><span data-stu-id="1b55d-227">If one or more configurations show the same value, the sequence is implementation dependent.</span></span> <span data-ttu-id="1b55d-228">Um valor de 0 indica que a sequência é dependente de implementação.</span><span class="sxs-lookup"><span data-stu-id="1b55d-228">A value of 0 indicates that the sequence is implementation dependent.</span></span> <span data-ttu-id="1b55d-229">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b55d-229">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-230">**BaseBoardSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="1b55d-230">**BaseBoardSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-231">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-232">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-232">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-233">O número de série da placa base para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1b55d-233">The serial number of the base board for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-234">**BIOSGUID**</span><span class="sxs-lookup"><span data-stu-id="1b55d-234">**BIOSGUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-235">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-236">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-236">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-237">O identificador global exclusivo para o BIOS da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1b55d-237">The globally unique identifier for the BIOS of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-238">**BIOSNumLock**</span><span class="sxs-lookup"><span data-stu-id="1b55d-238">**BIOSNumLock**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-239">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1b55d-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-240">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-240">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-241">**True** se a tecla num lock for definida como on pelo BIOS; **False** se a tecla num lock estiver definida como off pelo BIOS.</span><span class="sxs-lookup"><span data-stu-id="1b55d-241">**True** if the num lock key is set to on by the BIOS; **False** if the num lock key is set to off by the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-242">**BIOSSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="1b55d-242">**BIOSSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-243">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-244">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-244">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-245">O número de série do BIOS para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1b55d-245">The serial number of the BIOS for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-246">**BootOrder**</span><span class="sxs-lookup"><span data-stu-id="1b55d-246">**BootOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-247">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b55d-247">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-248">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-248">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-249">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span><span class="sxs-lookup"><span data-stu-id="1b55d-249">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-250">A ordem de inicialização definida no BIOS da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1b55d-250">The boot order set within the BIOS of the virtual machine.</span></span> <span data-ttu-id="1b55d-251">Essa propriedade é uma matriz de valores, **BootOrder** \[ 0 \] a **BootOrder** \[ 3 \] , inclusive, em que cada valor indica um dispositivo para inicializar.</span><span class="sxs-lookup"><span data-stu-id="1b55d-251">This property is an array of values, **BootOrder**\[0\] through **BootOrder**\[3\], inclusive, where each value indicates a device to boot from.</span></span> <span data-ttu-id="1b55d-252">Cada um dos quatro valores na matriz deve ser definido e não deve ser o mesmo que outro valor na matriz.</span><span class="sxs-lookup"><span data-stu-id="1b55d-252">Each of the 4 values in the array must be set and must not be the same as another value in the array.</span></span> <span data-ttu-id="1b55d-253">A máquina virtual tentará primeiro inicializar do dispositivo indicado pelo primeiro valor dentro da matriz.</span><span class="sxs-lookup"><span data-stu-id="1b55d-253">The virtual machine will first attempt to boot from the device indicated by the first value within the array.</span></span> <span data-ttu-id="1b55d-254">Se esse dispositivo não contiver um setor de inicialização, a máquina virtual tentará inicializar a partir do próximo dispositivo especificado pela propriedade **BootOrder** e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="1b55d-254">If that device does not contain a boot sector, the virtual machine will attempt to boot from the next device specified by the **BootOrder** property and so on.</span></span> <span data-ttu-id="1b55d-255">Se nenhum dispositivo especificado no **BootOrder** contiver um setor de inicialização, a máquina virtual falhará ao ser inicializada.</span><span class="sxs-lookup"><span data-stu-id="1b55d-255">If no device specified within the **BootOrder** contains a boot sector the virtual machine will fail to boot.</span></span> <span data-ttu-id="1b55d-256">O valor padrão de uma máquina virtual é \[ 0, 1, 2, 3 \] .</span><span class="sxs-lookup"><span data-stu-id="1b55d-256">The default value for a virtual machine is \[0, 1, 2, 3\].</span></span>

<dt>

<span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>

<span data-ttu-id="1b55d-257"><span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>**Disquete** (0)</span><span class="sxs-lookup"><span data-stu-id="1b55d-257"><span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>**Floppy** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1b55d-258">A máquina virtual tentará inicializar a partir do disquete dentro da unidade de disquete.</span><span class="sxs-lookup"><span data-stu-id="1b55d-258">The virtual machine will attempt to boot from the floppy disk within the floppy drive.</span></span>

</dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span data-ttu-id="1b55d-259"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (1)</span><span class="sxs-lookup"><span data-stu-id="1b55d-259"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1b55d-260">A máquina virtual tentará inicializar a partir do primeiro disco de CD ou DVD encontrado com um setor de inicialização.</span><span class="sxs-lookup"><span data-stu-id="1b55d-260">The virtual machine will attempt to boot from the first CD or DVD disk found with a boot sector.</span></span>

</dd> <dt>

<span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>

<span data-ttu-id="1b55d-261"><span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>**Disco rígido IDE** (2)</span><span class="sxs-lookup"><span data-stu-id="1b55d-261"><span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>**IDE Hard Drive** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1b55d-262">A máquina virtual tentará inicializar a partir da primeira unidade de disco rígido encontrada com um setor de inicialização.</span><span class="sxs-lookup"><span data-stu-id="1b55d-262">The virtual machine will attempt to boot from the first hard disk drive found with a boot sector.</span></span>

</dd> <dt>

<span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>

<span data-ttu-id="1b55d-263"><span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>**Inicialização PXE** (3)</span><span class="sxs-lookup"><span data-stu-id="1b55d-263"><span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>**PXE Boot** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1b55d-264">A máquina virtual tentará inicializar o PXE a partir da rede.</span><span class="sxs-lookup"><span data-stu-id="1b55d-264">The virtual machine will attempt to PXE boot from the network.</span></span>

</dd> <dt>

<span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>

<span data-ttu-id="1b55d-265"><span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>**Disco rígido SCSI** (4)</span><span class="sxs-lookup"><span data-stu-id="1b55d-265"><span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>**SCSI Hard Drive** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="1b55d-266"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reservado** (5.. 65535)</span><span class="sxs-lookup"><span data-stu-id="1b55d-266"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (5..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1b55d-267">**BootSourceOrder**</span><span class="sxs-lookup"><span data-stu-id="1b55d-267">**BootSourceOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-268">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-268">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-269">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-269">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-270">A ordem de origem da inicialização para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1b55d-270">The boot source order for the virtual machine.</span></span>

<span data-ttu-id="1b55d-271">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="1b55d-271">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-272">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="1b55d-272">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-273">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-274">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-275">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="1b55d-275">A short description of the object.</span></span> <span data-ttu-id="1b55d-276">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1b55d-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-277">**ChassisAssetTag**</span><span class="sxs-lookup"><span data-stu-id="1b55d-277">**ChassisAssetTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-278">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-279">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-279">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-280">A marca de ativo do chassi para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1b55d-280">The asset tag of the chassis for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-281">**ChassisSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="1b55d-281">**ChassisSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-282">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-283">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-283">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-284">O número de série do chassi para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1b55d-284">The serial number of the chassis for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-285">**ConfigurationDataRoot**</span><span class="sxs-lookup"><span data-stu-id="1b55d-285">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-286">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-287">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-288">O caminho de um diretório em que as informações sobre a configuração da máquina virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="1b55d-288">The path of a directory where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="1b55d-289">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b55d-289">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-290">**ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="1b55d-290">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-291">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-292">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-293">O caminho relativo e o nome de arquivo de um arquivo em que as informações sobre a configuração da máquina virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="1b55d-293">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="1b55d-294">Esse caminho é relativo à propriedade **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="1b55d-294">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="1b55d-295">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b55d-295">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-296">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="1b55d-296">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-297">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-299">O identificador exclusivo da configuração da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1b55d-299">The unique identifier of the virtual machine configuration.</span></span> <span data-ttu-id="1b55d-300">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b55d-300">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-301">**Consolemode**</span><span class="sxs-lookup"><span data-stu-id="1b55d-301">**ConsoleMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-302">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b55d-302">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-303">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-303">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-304">Identifica o modo de console para a VM.</span><span class="sxs-lookup"><span data-stu-id="1b55d-304">Identifies the Console Mode for the VM.</span></span>

> [!Note]  
> <span data-ttu-id="1b55d-305">Essa propriedade foi adicionada no Windows 10 e no Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="1b55d-305">This property was added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="1b55d-306">**Padrão** (0)</span><span class="sxs-lookup"><span data-stu-id="1b55d-306">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="COM1"></span><span id="com1"></span>

<span data-ttu-id="1b55d-307">**COM1** (1)</span><span class="sxs-lookup"><span data-stu-id="1b55d-307">**COM1** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="COM2"></span><span id="com2"></span>

<span data-ttu-id="1b55d-308">**COM2** (2)</span><span class="sxs-lookup"><span data-stu-id="1b55d-308">**COM2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="1b55d-309">**Nenhum** (3)</span><span class="sxs-lookup"><span data-stu-id="1b55d-309">**None** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1b55d-310">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="1b55d-310">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-311">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1b55d-311">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-312">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-313">A data e a hora em que as configurações da máquina virtual foram criadas.</span><span class="sxs-lookup"><span data-stu-id="1b55d-313">The date and time at which the settings for the virtual machine were created.</span></span> <span data-ttu-id="1b55d-314">Se esse objeto representar as configurações atuais para a máquina virtual, esse valor será a hora em que o sistema foi criado.</span><span class="sxs-lookup"><span data-stu-id="1b55d-314">If this object represents the current settings for the virtual machine, this value would be the time at which the system was created.</span></span> <span data-ttu-id="1b55d-315">Se esse objeto representar as configurações de instantâneo para a máquina virtual, esse valor será a hora em que o instantâneo foi tirado.</span><span class="sxs-lookup"><span data-stu-id="1b55d-315">If this object represents the snapshot settings for the virtual machine, this value would be the time at which the snapshot was taken.</span></span> <span data-ttu-id="1b55d-316">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b55d-316">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-317">**DebugChannelId**</span><span class="sxs-lookup"><span data-stu-id="1b55d-317">**DebugChannelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-318">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1b55d-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-319">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-319">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-320">O identificador de canal usado para depurar a máquina virtual usando o depurador unificado.</span><span class="sxs-lookup"><span data-stu-id="1b55d-320">The channel identifier used to debug the virtual machine using the unified debugger.</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-321">**DebugPort**</span><span class="sxs-lookup"><span data-stu-id="1b55d-321">**DebugPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-322">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1b55d-322">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-323">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-323">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-324">A porta TCP/IP usada para depurar a máquina virtual usando a depuração sintética.</span><span class="sxs-lookup"><span data-stu-id="1b55d-324">The TCP/IP port used to debug the virtual machine using synthetic debugging.</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-325">**DebugPortEnabled**</span><span class="sxs-lookup"><span data-stu-id="1b55d-325">**DebugPortEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-326">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b55d-326">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-327">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-327">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-328">Especifica se a máquina virtual está usando a depuração sintética.</span><span class="sxs-lookup"><span data-stu-id="1b55d-328">Specifies whether the virtual machine is using synthetic debugging.</span></span> <span data-ttu-id="1b55d-329">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1b55d-329">This can be one of the following values.</span></span>

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="1b55d-330"><span id="Off"></span><span id="off"></span><span id="OFF"></span>**Desativado** (0)</span><span class="sxs-lookup"><span data-stu-id="1b55d-330"><span id="Off"></span><span id="off"></span><span id="OFF"></span>**Off** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="On"></span><span id="on"></span><span id="ON"></span>

<span data-ttu-id="1b55d-331"><span id="On"></span><span id="on"></span><span id="ON"></span>**Em** (1)</span><span class="sxs-lookup"><span data-stu-id="1b55d-331"><span id="On"></span><span id="on"></span><span id="ON"></span>**On** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>

<span data-ttu-id="1b55d-332"><span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>**OnAutoAssigned** (2)</span><span class="sxs-lookup"><span data-stu-id="1b55d-332"><span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>**OnAutoAssigned** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1b55d-333">Atribuído automaticamente</span><span class="sxs-lookup"><span data-stu-id="1b55d-333">Auto-assigned</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1b55d-334">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1b55d-334">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-335">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-337">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="1b55d-337">A description of the object.</span></span> <span data-ttu-id="1b55d-338">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1b55d-338">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to one of the following values.</span></span>



| <span data-ttu-id="1b55d-339">Valor</span><span class="sxs-lookup"><span data-stu-id="1b55d-339">Value</span></span>                                                                                                                  | <span data-ttu-id="1b55d-340">Significado</span><span class="sxs-lookup"><span data-stu-id="1b55d-340">Meaning</span></span>                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="1b55d-341"><dt>"Configurações ativas para a máquina virtual"</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-341"><dt>"Active settings for the virtual machine"</dt></span></span> </dl>   | <span data-ttu-id="1b55d-342">Essa instância se refere a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1b55d-342">This instance refers to a virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="1b55d-343"><dt>"Configurações de instantâneo para a máquina virtual"</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-343"><dt>"Snapshot settings for the virtual machine"</dt></span></span> </dl> | <span data-ttu-id="1b55d-344">Essa instância se refere a um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="1b55d-344">This instance refers to a snapshot.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="1b55d-345">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1b55d-345">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-346">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-348">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="1b55d-348">A display name for the object.</span></span> <span data-ttu-id="1b55d-349">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e é sempre definida como o nome de exibição do computador.</span><span class="sxs-lookup"><span data-stu-id="1b55d-349">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and it is always set to the display name for the machine.</span></span> <span data-ttu-id="1b55d-350">Esse nome não pode exceder 100 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="1b55d-350">This name may not exceed 100 characters in length.</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-351">**EnhancedSessionTransportType**</span><span class="sxs-lookup"><span data-stu-id="1b55d-351">**EnhancedSessionTransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-352">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b55d-352">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-353">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-353">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-354">Indica o tipo de transporte a ser usado ao se conectar a uma sessão avançada.</span><span class="sxs-lookup"><span data-stu-id="1b55d-354">Indicates the transport type to use when connecting to an enhanced session.</span></span>

> [!Note]  
> <span data-ttu-id="1b55d-355">Essa propriedade foi adicionada no Windows 10, versão 1803.</span><span class="sxs-lookup"><span data-stu-id="1b55d-355">This property was added in Windows 10, version 1803.</span></span>

 

<dt>

<span id="VMBus_Pipe"></span><span id="vmbus_pipe"></span><span id="VMBUS_PIPE"></span>

<span data-ttu-id="1b55d-356">**Pipe VMBus** (0)</span><span class="sxs-lookup"><span data-stu-id="1b55d-356">**VMBus Pipe** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Hyper-V_Socket"></span><span id="hyper-v_socket"></span><span id="HYPER-V_SOCKET"></span>

<span data-ttu-id="1b55d-357">**Soquete do Hyper-V** (1)</span><span class="sxs-lookup"><span data-stu-id="1b55d-357">**Hyper-V Socket** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1b55d-358">**GuestControlledCacheTypes**</span><span class="sxs-lookup"><span data-stu-id="1b55d-358">**GuestControlledCacheTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-359">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1b55d-359">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-360">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-360">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-361">Indica se o convidado pode controlar os tipos de cache.</span><span class="sxs-lookup"><span data-stu-id="1b55d-361">Indicates whether the guest can control cache types.</span></span>

> [!Note]  
> <span data-ttu-id="1b55d-362">Adicionado ao Windows 10 e ao Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="1b55d-362">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="1b55d-363">**GuestStateDataRoot**</span><span class="sxs-lookup"><span data-stu-id="1b55d-363">**GuestStateDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-364">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-365">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-366">FilePath de um diretório em que as informações sobre o estado do tempo de execução do convidado são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="1b55d-366">Filepath of a directory where information about the guest runtime state is stored.</span></span>

> [!Note]  
> <span data-ttu-id="1b55d-367">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="1b55d-367">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="1b55d-368">**GuestStateFile**</span><span class="sxs-lookup"><span data-stu-id="1b55d-368">**GuestStateFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-369">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-370">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-371">FilePath de um arquivo em que as informações sobre o estado do tempo de execução do convidado são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="1b55d-371">Filepath of a file where information about the guest runtime state is stored.</span></span> <span data-ttu-id="1b55d-372">Um caminho relativo é acrescentado ao valor da propriedade **GuestStateDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="1b55d-372">A relative path appends to the value of the **GuestStateDataRoot** property.</span></span>

> [!Note]  
> <span data-ttu-id="1b55d-373">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="1b55d-373">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="1b55d-374">**HighMmioGapSize**</span><span class="sxs-lookup"><span data-stu-id="1b55d-374">**HighMmioGapSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-375">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1b55d-375">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-376">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-376">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-377">O tamanho do intervalo de e/s alto (acima de 4GB) Memory-Mapped em MB</span><span class="sxs-lookup"><span data-stu-id="1b55d-377">The size of the High (above 4GB) Memory-Mapped IO Gap in MB</span></span>

> [!Note]  
> <span data-ttu-id="1b55d-378">Essa propriedade foi adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="1b55d-378">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="1b55d-379">**IncrementalBackupEnabled**</span><span class="sxs-lookup"><span data-stu-id="1b55d-379">**IncrementalBackupEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-380">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1b55d-380">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-381">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-381">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-382">Indica se o gravador VSS do Hyper-V dá suporte para fazer backups incrementais desta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1b55d-382">Indicates whether the Hyper-V VSS writer supports taking incremental backups of this virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-383">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1b55d-383">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-384">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-385">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-386">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="1b55d-386">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-387">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="1b55d-387">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1b55d-388">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b55d-388">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-389">**IsAutomaticSnapshot**</span><span class="sxs-lookup"><span data-stu-id="1b55d-389">**IsAutomaticSnapshot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-390">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1b55d-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-391">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-392">Indica se este é um instantâneo criado automaticamente para o usuário.</span><span class="sxs-lookup"><span data-stu-id="1b55d-392">Indicates whether this is a snapshot created automatically for the user.</span></span>

> [!Note]  
> <span data-ttu-id="1b55d-393">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="1b55d-393">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="1b55d-394">**IsSaved**</span><span class="sxs-lookup"><span data-stu-id="1b55d-394">**IsSaved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-395">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1b55d-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-396">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-397">**True** se a configuração tiver uma referência a um arquivo de estado salvo; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="1b55d-397">**True** if the configuration has a reference to a saved state file; otherwise, **False**.</span></span> <span data-ttu-id="1b55d-398">Isso não indica a presença desse arquivo, apenas que a configuração especifica um.</span><span class="sxs-lookup"><span data-stu-id="1b55d-398">This does not indicate the presence of such a file, only that the configuration specifies one.</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-399">**LockOnDisconnect**</span><span class="sxs-lookup"><span data-stu-id="1b55d-399">**LockOnDisconnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-400">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1b55d-400">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-401">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-401">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-402">Bloqueie o console ao desconectar do vmconnect.</span><span class="sxs-lookup"><span data-stu-id="1b55d-402">Lock the console when disconnecting from vmconnect.</span></span>

> [!Note]  
> <span data-ttu-id="1b55d-403">Adicionado ao Windows 10 e ao Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="1b55d-403">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="1b55d-404">**LogDataRoot**</span><span class="sxs-lookup"><span data-stu-id="1b55d-404">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-405">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-406">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-407">O caminho de um diretório em que as informações de log para a máquina virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="1b55d-407">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="1b55d-408">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b55d-408">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-409">**LowMmioGapSize**</span><span class="sxs-lookup"><span data-stu-id="1b55d-409">**LowMmioGapSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-410">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1b55d-410">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-411">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-411">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-412">Configura o tamanho, em megabytes, da primeira lacuna de MMIO para uma VM (máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="1b55d-412">Configures the size, in megabytes, of the first MMIO gap for a virtual machine (VM).</span></span>

<span data-ttu-id="1b55d-413">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="1b55d-413">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<span data-ttu-id="1b55d-414">Intervalo: 128 3584</span><span class="sxs-lookup"><span data-stu-id="1b55d-414">Range: 128 3584</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-415">**NetworkBootPreferredProtocol**</span><span class="sxs-lookup"><span data-stu-id="1b55d-415">**NetworkBootPreferredProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-416">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b55d-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-417">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-417">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-418">Determina se o protocolo preferencial para inicialização PXE é IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="1b55d-418">Determines if the preferred protocol for PXE boot is IPv4 or IPv6.</span></span>

<span data-ttu-id="1b55d-419">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="1b55d-419">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="1b55d-420">**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="1b55d-420">**IPv4** (4096)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="1b55d-421">**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="1b55d-421">**IPv6** (4097)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1b55d-422">**Observações**</span><span class="sxs-lookup"><span data-stu-id="1b55d-422">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-423">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-423">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-424">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-425">Notas fornecidas pelo usuário que estão relacionadas à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1b55d-425">User supplied notes that are related to the virtual machine.</span></span> <span data-ttu-id="1b55d-426">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b55d-426">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-427">**Pai**</span><span class="sxs-lookup"><span data-stu-id="1b55d-427">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-428">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-429">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-430">Se essa instância não representar um sistema baseado em um instantâneo de uma máquina virtual, essa propriedade será **nula**.</span><span class="sxs-lookup"><span data-stu-id="1b55d-430">If this instance does not represent a system based on a snapshot of a virtual machine, this property is **Null**.</span></span> <span data-ttu-id="1b55d-431">Caso contrário, a propriedade contém o caminho do objeto do objeto **Msvm \_ VirtualSystemSettingData** no qual essa instância se baseia.</span><span class="sxs-lookup"><span data-stu-id="1b55d-431">Otherwise, the property holds the object path of the **Msvm\_VirtualSystemSettingData** object on which this instance is based.</span></span> <span data-ttu-id="1b55d-432">Ao criar uma hierarquia de árvore de instantâneo para a máquina virtual, essa propriedade faz referência ao objeto do qual a instância atual é derivada (a instância atual é o nó filho e o objeto referenciado nessa propriedade é o nó pai).</span><span class="sxs-lookup"><span data-stu-id="1b55d-432">When building a snapshot tree hierarchy for the virtual machine, this property references the object from which the current instance is derived (the current instance is the child node and the object referenced in this property is the parent node.)</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-433">**ParentPackage**</span><span class="sxs-lookup"><span data-stu-id="1b55d-433">**ParentPackage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-434">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-435">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-435">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-436">Se esse sistema for um contêiner, o caminho para o Msvm \_ ContainerPackage do qual esse sistema se baseia.</span><span class="sxs-lookup"><span data-stu-id="1b55d-436">If this system is a container, the path to the Msvm\_ContainerPackage from which this system is based.</span></span>

> [!Note]  
> <span data-ttu-id="1b55d-437">Adicionado no Windows 10; removido no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="1b55d-437">Added in Windows 10; removed in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="1b55d-438">**PauseAfterBootFailure**</span><span class="sxs-lookup"><span data-stu-id="1b55d-438">**PauseAfterBootFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-439">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1b55d-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-440">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-440">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-441">Indica se o BIOS pausa após cada falha na entrada de inicialização aguardando que o usuário pressione uma tecla.</span><span class="sxs-lookup"><span data-stu-id="1b55d-441">Indicates whether the BIOS pauses after every boot entry failure waiting for the user to press a key.</span></span> <span data-ttu-id="1b55d-442">**True** se o BIOS pausar; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="1b55d-442">**True** if the BIOS pauses; otherwise, **False**.</span></span>

<span data-ttu-id="1b55d-443">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="1b55d-443">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-444">**Recuperação de**</span><span class="sxs-lookup"><span data-stu-id="1b55d-444">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-445">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-446">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-447">O caminho completo de um arquivo em que as informações relacionadas à recuperação para a máquina virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="1b55d-447">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="1b55d-448">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b55d-448">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-449">**SecureBootEnabled**</span><span class="sxs-lookup"><span data-stu-id="1b55d-449">**SecureBootEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-450">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1b55d-450">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-451">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-451">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-452">Indica se a inicialização segura está habilitada para a VM (máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="1b55d-452">Indicates whether secure boot is enabled for the virtual machine (VM).</span></span> <span data-ttu-id="1b55d-453">**Verdadeiro** se habilitado; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="1b55d-453">**True** if enabled; otherwise, **False**.</span></span>

> [!Note]  
> <span data-ttu-id="1b55d-454">A inicialização segura só pode ser habilitada para VMs de geração 2.</span><span class="sxs-lookup"><span data-stu-id="1b55d-454">Secure boot can only be enabled for generation 2 VMs.</span></span>

 

<span data-ttu-id="1b55d-455">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="1b55d-455">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-456">**SecureBootTemplateId**</span><span class="sxs-lookup"><span data-stu-id="1b55d-456">**SecureBootTemplateId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-457">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-458">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-458">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-459">O identificador global exclusivo do modelo de valores iniciales de variáveis relacionadas à inicialização segura de UEFI.</span><span class="sxs-lookup"><span data-stu-id="1b55d-459">The globally-unique identifier of the template of intial values of UEFI Secure Boot related variables.</span></span>

<span data-ttu-id="1b55d-460">Esta é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyVirtualSystem**](https://www.bing.com/search?q=**ModifyVirtualSystem**) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="1b55d-460">This is a read-only property, but it can be changed using the [**ModifyVirtualSystem**](https://www.bing.com/search?q=**ModifyVirtualSystem**) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="1b55d-461">Adicionado ao Windows 10 e ao Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="1b55d-461">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="1b55d-462">**SnapshotDataRoot**</span><span class="sxs-lookup"><span data-stu-id="1b55d-462">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-463">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-464">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-465">O caminho de um diretório em que as informações sobre os instantâneos de máquina virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="1b55d-465">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="1b55d-466">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b55d-466">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-467">**SuspendDataRoot**</span><span class="sxs-lookup"><span data-stu-id="1b55d-467">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-468">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-469">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-470">O caminho de um diretório em que informações sobre as informações relacionadas à suspensão da máquina virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="1b55d-470">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="1b55d-471">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b55d-471">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-472">**SwapFileDataRoot**</span><span class="sxs-lookup"><span data-stu-id="1b55d-472">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-473">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-473">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-474">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-474">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-475">O caminho de um diretório em que os arquivos de permuta para a máquina virtual são armazenados.</span><span class="sxs-lookup"><span data-stu-id="1b55d-475">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="1b55d-476">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b55d-476">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-477">**Userinstantâneotype**</span><span class="sxs-lookup"><span data-stu-id="1b55d-477">**UserSnapshotType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-478">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b55d-478">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-479">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-479">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-480">Indica o tipo de instantâneo definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="1b55d-480">Indicates the user-defined snapshot type.</span></span>

> [!Note]  
> <span data-ttu-id="1b55d-481">Adicionado ao Windows 10 e ao Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="1b55d-481">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="1b55d-482"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Desabilitar** (2)</span><span class="sxs-lookup"><span data-stu-id="1b55d-482"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1b55d-483">Desabilite a criação de qualquer instantâneo.</span><span class="sxs-lookup"><span data-stu-id="1b55d-483">Disable the creation of any snapshot.</span></span>

</dd> <dt>

<span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>

<span data-ttu-id="1b55d-484"><span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>**ProductionFallbackToTest** (3)</span><span class="sxs-lookup"><span data-stu-id="1b55d-484"><span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>**ProductionFallbackToTest** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1b55d-485">Instantâneo consistente de dados para uso no ambiente de produção. Executa um instantâneo com o estado do aplicativo quando a capacidade de criar um instantâneo consistente de dados não está disponível.</span><span class="sxs-lookup"><span data-stu-id="1b55d-485">Data-consistent snapshot for use in the production environment.Performs a snapshot with application state when the ability to create data consistent snapshot is not available.</span></span>

</dd> <dt>

<span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>

<span data-ttu-id="1b55d-486"><span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>**ProductionNoFallback** (4)</span><span class="sxs-lookup"><span data-stu-id="1b55d-486"><span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>**ProductionNoFallback** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1b55d-487">Instantâneo consistente de dados para uso no ambiente de produção. Não criará um instantâneo com o estado do aplicativo se não for possível criar um instantâneo de dados consistente.</span><span class="sxs-lookup"><span data-stu-id="1b55d-487">Data-consistent snapshot for use in the production environment.Does not create a snapshot with application state if it is not possible to create a data consistent snapshot.</span></span>

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="1b55d-488"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Teste** (5)</span><span class="sxs-lookup"><span data-stu-id="1b55d-488"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (5)</span></span>


</dt> <dd>

<span data-ttu-id="1b55d-489">Instantâneo que contém informações de memória e dispositivo para fins de teste e desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="1b55d-489">Snapshot that contains memory and device information for test and development purpose.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1b55d-490">**Versão**</span><span class="sxs-lookup"><span data-stu-id="1b55d-490">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-491">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-491">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-492">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-492">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-493">A versão da máquina virtual em um formato de "Major. Minor", por exemplo, "2,0".</span><span class="sxs-lookup"><span data-stu-id="1b55d-493">The version of the virtual machine in a format of "major.minor", for example "2.0".</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-494">**VirtualNumaEnabled**</span><span class="sxs-lookup"><span data-stu-id="1b55d-494">**VirtualNumaEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-495">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1b55d-495">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-496">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b55d-496">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-497">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm \_ ProcessorSettingData**](msvm-processorsettingdata.md).**MaxProcessorsPerNumaNode**","[**Msvm \_ MemorySettingData**](msvm-memorysettingdata.md).**MaxMemoryBlocksPerNumaNode**")</span><span class="sxs-lookup"><span data-stu-id="1b55d-497">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_ProcessorSettingData**](msvm-processorsettingdata.md).**MaxProcessorsPerNumaNode**", "[**Msvm\_MemorySettingData**](msvm-memorysettingdata.md).**MaxMemoryBlocksPerNumaNode**")</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-498">**True** se os nós numa (acesso não uniforme à memória) estiverem projetados na máquina virtual; **False** se a máquina virtual tiver um único nó.</span><span class="sxs-lookup"><span data-stu-id="1b55d-498">**True** if virtual non-uniform memory access (NUMA) nodes are projected into the virtual machine; **False** if the virtual machine will have a single node.</span></span> <span data-ttu-id="1b55d-499">Se **for true**, o número de nós numa virtuais projetados na máquina virtual será determinado com os valores das propriedades [**Msvm \_ ProcessorSettingData. MaxProcessorsPerNumaNode**](msvm-processorsettingdata.md) e [**Msvm \_ MemorySettingData. MaxMemoryBlocksPerNumaNode**](msvm-memorysettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="1b55d-499">If **True**, the number of virtual NUMA nodes projected into the virtual machine is determined from the values of the [**Msvm\_ProcessorSettingData.MaxProcessorsPerNumaNode**](msvm-processorsettingdata.md) and [**Msvm\_MemorySettingData.MaxMemoryBlocksPerNumaNode**](msvm-memorysettingdata.md) properties.</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-500">**VirtualSystemIdentifier**</span><span class="sxs-lookup"><span data-stu-id="1b55d-500">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-501">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-501">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-502">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-503">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemSettingData. VirtualSystemIdentifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="1b55d-503">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemSettingData.VirtualSystemIdentifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-504">O nome do objeto [**de \_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de dados CIM ao qual esses dados de configuração pertencem.</span><span class="sxs-lookup"><span data-stu-id="1b55d-504">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="1b55d-505">Essa propriedade é uma substituição do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b55d-505">This property is an override from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1b55d-506">**VirtualSystemSubType**</span><span class="sxs-lookup"><span data-stu-id="1b55d-506">**VirtualSystemSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-507">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-507">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-508">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-509">Os valores válidos para essa propriedade são Microsoft: Hyper-V: subtipo: 1 e Microsoft: Hyper-V: subtipo: 2.</span><span class="sxs-lookup"><span data-stu-id="1b55d-509">The valid values for this property are Microsoft:Hyper-V:SubType:1 and Microsoft:Hyper-V:SubType:2.</span></span> <span data-ttu-id="1b55d-510">Uma VM de geração 1 é o subtipo 1.</span><span class="sxs-lookup"><span data-stu-id="1b55d-510">A  Generation 1  VM is subtype 1.</span></span> <span data-ttu-id="1b55d-511">Uma VM de geração 2 é o subtipo 2.</span><span class="sxs-lookup"><span data-stu-id="1b55d-511">A  Generation 2  VM is subtype 2.</span></span>

<span data-ttu-id="1b55d-512">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="1b55d-512">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

<span data-ttu-id="1b55d-513">**Microsoft: Hyper-v: subtipo: 1** ("Microsoft: Hyper-v: subtipo: 1")</span><span class="sxs-lookup"><span data-stu-id="1b55d-513">**Microsoft:Hyper-V:SubType:1** ("Microsoft:Hyper-V:SubType:1")</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

<span data-ttu-id="1b55d-514">**Microsoft: Hyper-v: subtipo: 2** ("Microsoft: Hyper-v: subtipo: 2")</span><span class="sxs-lookup"><span data-stu-id="1b55d-514">**Microsoft:Hyper-V:SubType:2** ("Microsoft:Hyper-V:SubType:2")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1b55d-515">**VirtualSystemType**</span><span class="sxs-lookup"><span data-stu-id="1b55d-515">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b55d-516">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b55d-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b55d-517">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b55d-517">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b55d-518">Especifica o tipo de máquina virtual que os dados de configuração representam.</span><span class="sxs-lookup"><span data-stu-id="1b55d-518">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="1b55d-519">Essa propriedade é herdada da classe [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1b55d-519">This property is inherited from the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) class.</span></span> <span data-ttu-id="1b55d-520">Esse será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1b55d-520">This will be one of the following values.</span></span>



| <span data-ttu-id="1b55d-521">Valor</span><span class="sxs-lookup"><span data-stu-id="1b55d-521">Value</span></span>                                                                                                                                 | <span data-ttu-id="1b55d-522">Significado</span><span class="sxs-lookup"><span data-stu-id="1b55d-522">Meaning</span></span>                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="1b55d-523"><dt>"Microsoft: Hyper-V: System: percebido"</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-523"><dt>"Microsoft:Hyper-V:System:Realized"</dt></span></span> </dl>                        | <span data-ttu-id="1b55d-524">Uma máquina virtual realizada.</span><span class="sxs-lookup"><span data-stu-id="1b55d-524">A realized virtual machine.</span></span><br/>               |
| <dl> <span data-ttu-id="1b55d-525"><dt>"Microsoft: Hyper-V: System: planejado"</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-525"><dt>"Microsoft:Hyper-V:System:Planned"</dt></span></span> </dl>                         | <span data-ttu-id="1b55d-526">Uma máquina virtual planejada.</span><span class="sxs-lookup"><span data-stu-id="1b55d-526">A planned virtual machine.</span></span><br/>                |
| <dl> <span data-ttu-id="1b55d-527"><dt>"Microsoft: Hyper-V: instantâneo: percebido"</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-527"><dt>"Microsoft:Hyper-V:Snapshot:Realized"</dt></span></span> </dl>                      | <span data-ttu-id="1b55d-528">Um instantâneo de uma máquina virtual realizada.</span><span class="sxs-lookup"><span data-stu-id="1b55d-528">A snapshot of a realized virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="1b55d-529"><dt>"Microsoft: Hyper-V: snapshot: Recovery"</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-529"><dt>"Microsoft:Hyper-V:Snapshot:Recovery"</dt></span></span> </dl>                      | <span data-ttu-id="1b55d-530">Um instantâneo de uma máquina virtual de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1b55d-530">A snapshot of a recovery virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="1b55d-531"><dt>"Microsoft: Hyper-V: snapshot: planejado"</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-531"><dt>"Microsoft:Hyper-V:Snapshot:Planned"</dt></span></span> </dl>                       | <span data-ttu-id="1b55d-532">Um instantâneo de uma máquina virtual planejada.</span><span class="sxs-lookup"><span data-stu-id="1b55d-532">A snapshot of a planned virtual machine.</span></span><br/>  |
| <dl> <span data-ttu-id="1b55d-533"><dt>"Microsoft: Hyper-V: snapshot: ausente"</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-533"><dt>"Microsoft:Hyper-V:Snapshot:Missing"</dt></span></span> </dl>                       | <span data-ttu-id="1b55d-534">Um instantâneo ausente.</span><span class="sxs-lookup"><span data-stu-id="1b55d-534">A missing snapshot.</span></span><br/>                       |
| <dl> <span data-ttu-id="1b55d-535"><dt>"Microsoft: Hyper-V: snapshot: réplica: Standard"</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-535"><dt>"Microsoft:Hyper-V:Snapshot:Replica:Standard"</dt></span></span> </dl>              | <span data-ttu-id="1b55d-536">Um instantâneo de ponto de replicação baseado em tempo.</span><span class="sxs-lookup"><span data-stu-id="1b55d-536">A time-based replication point snapshot.</span></span><br/>  |
| <dl> <span data-ttu-id="1b55d-537"><dt>"Microsoft: Hyper-V: snapshot: Replica: ApplicationConsistent"</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-537"><dt>"Microsoft:Hyper-V:Snapshot:Replica:ApplicationConsistent"</dt></span></span> </dl> | <span data-ttu-id="1b55d-538">Um instantâneo de ponto de replicação do VSS.</span><span class="sxs-lookup"><span data-stu-id="1b55d-538">A VSS replication point snapshot.</span></span><br/>         |
| <dl> <span data-ttu-id="1b55d-539"><dt>"Microsoft: Hyper-V: snapshot: Replica: PlannedFailover"</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-539"><dt>"Microsoft:Hyper-V:Snapshot:Replica:PlannedFailover"</dt></span></span> </dl>       | <span data-ttu-id="1b55d-540">Um instantâneo de replicação planejado.</span><span class="sxs-lookup"><span data-stu-id="1b55d-540">A planned replication snapshot.</span></span><br/>           |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1b55d-541">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b55d-541">Remarks</span></span>

<span data-ttu-id="1b55d-542">O acesso à classe **Msvm \_ VirtualSystemSettingData** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="1b55d-542">Access to the **Msvm\_VirtualSystemSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1b55d-543">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="1b55d-543">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="1b55d-544">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b55d-544">Requirements</span></span>



| <span data-ttu-id="1b55d-545">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b55d-545">Requirement</span></span> | <span data-ttu-id="1b55d-546">Valor</span><span class="sxs-lookup"><span data-stu-id="1b55d-546">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b55d-547">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b55d-547">Minimum supported client</span></span><br/> | <span data-ttu-id="1b55d-548">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1b55d-548">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1b55d-549">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b55d-549">Minimum supported server</span></span><br/> | <span data-ttu-id="1b55d-550">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1b55d-550">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1b55d-551">Namespace</span><span class="sxs-lookup"><span data-stu-id="1b55d-551">Namespace</span></span><br/>                | <span data-ttu-id="1b55d-552">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="1b55d-552">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1b55d-553">MOF</span><span class="sxs-lookup"><span data-stu-id="1b55d-553">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b55d-554"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-554"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b55d-555">DLL</span><span class="sxs-lookup"><span data-stu-id="1b55d-555">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b55d-556"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1b55d-556"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1b55d-557">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b55d-557">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b55d-558">**\_VIRTUALSYSTEMSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="1b55d-558">**CIM\_VirtualSystemSettingData**</span></span>](cim-virtualsystemsettingdata.md)
</dt> <dt>

<span data-ttu-id="1b55d-559">[**\_VIRTUALSYSTEMSETTINGDATA CIM**](/previous-versions//cc136954(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1b55d-559">[**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1b55d-560">Classes de sistema virtual</span><span class="sxs-lookup"><span data-stu-id="1b55d-560">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

