---
description: Representa uma unidade de disco rígido dentro de uma máquina virtual.
ms.assetid: BF03CD02-7CDE-45E2-84D1-EC8E4457094A
title: Classe Msvm_DiskDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskDrive
- Msvm_DiskDrive.SetPowerState
- Msvm_DiskDrive.EnableDevice
- Msvm_DiskDrive.OnlineDevice
- Msvm_DiskDrive.QuiesceDevice
- Msvm_DiskDrive.SaveProperties
- Msvm_DiskDrive.RestoreProperties
- Msvm_DiskDrive.InstanceID
- Msvm_DiskDrive.Caption
- Msvm_DiskDrive.Description
- Msvm_DiskDrive.ElementName
- Msvm_DiskDrive.InstallDate
- Msvm_DiskDrive.Name
- Msvm_DiskDrive.OperationalStatus
- Msvm_DiskDrive.StatusDescriptions
- Msvm_DiskDrive.Status
- Msvm_DiskDrive.HealthState
- Msvm_DiskDrive.CommunicationStatus
- Msvm_DiskDrive.DetailedStatus
- Msvm_DiskDrive.OperatingStatus
- Msvm_DiskDrive.PrimaryStatus
- Msvm_DiskDrive.EnabledState
- Msvm_DiskDrive.OtherEnabledState
- Msvm_DiskDrive.RequestedState
- Msvm_DiskDrive.EnabledDefault
- Msvm_DiskDrive.TimeOfLastStateChange
- Msvm_DiskDrive.AvailableRequestedStates
- Msvm_DiskDrive.TransitioningToState
- Msvm_DiskDrive.SystemCreationClassName
- Msvm_DiskDrive.SystemName
- Msvm_DiskDrive.CreationClassName
- Msvm_DiskDrive.DeviceID
- Msvm_DiskDrive.PowerManagementSupported
- Msvm_DiskDrive.PowerManagementCapabilities
- Msvm_DiskDrive.Availability
- Msvm_DiskDrive.StatusInfo
- Msvm_DiskDrive.LastErrorCode
- Msvm_DiskDrive.ErrorDescription
- Msvm_DiskDrive.ErrorCleared
- Msvm_DiskDrive.OtherIdentifyingInfo
- Msvm_DiskDrive.PowerOnHours
- Msvm_DiskDrive.TotalPowerOnHours
- Msvm_DiskDrive.IdentifyingDescriptions
- Msvm_DiskDrive.AdditionalAvailability
- Msvm_DiskDrive.MaxQuiesceTime
- Msvm_DiskDrive.Capabilities
- Msvm_DiskDrive.CapabilityDescriptions
- Msvm_DiskDrive.ErrorMethodology
- Msvm_DiskDrive.CompressionMethod
- Msvm_DiskDrive.NumberOfMediaSupported
- Msvm_DiskDrive.MaxMediaSize
- Msvm_DiskDrive.DefaultBlockSize
- Msvm_DiskDrive.MaxBlockSize
- Msvm_DiskDrive.MinBlockSize
- Msvm_DiskDrive.NeedsCleaning
- Msvm_DiskDrive.MediaIsLocked
- Msvm_DiskDrive.Security
- Msvm_DiskDrive.LastCleaned
- Msvm_DiskDrive.MaxAccessTime
- Msvm_DiskDrive.UncompressedDataRate
- Msvm_DiskDrive.LoadTime
- Msvm_DiskDrive.UnloadTime
- Msvm_DiskDrive.MountCount
- Msvm_DiskDrive.TimeOfLastMount
- Msvm_DiskDrive.TotalMountTime
- Msvm_DiskDrive.UnitsDescription
- Msvm_DiskDrive.MaxUnitsBeforeCleaning
- Msvm_DiskDrive.UnitsUsed
- Msvm_DiskDrive.DriveNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 60a08a2b73149285ddf3b0edf0003e5490b1c5c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836859"
---
# <a name="msvm_diskdrive-class"></a><span data-ttu-id="709e1-103">\_Classe Msvm DiskDrive</span><span class="sxs-lookup"><span data-stu-id="709e1-103">Msvm\_DiskDrive class</span></span>

<span data-ttu-id="709e1-104">Representa uma unidade de disco rígido dentro de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="709e1-104">Represents a hard disk drive inside of a virtual machine.</span></span> <span data-ttu-id="709e1-105">Essa unidade de disco rígido pode ser um dispositivo de passagem (se um disco rígido físico tiver sido anexado à máquina virtual) ou um dispositivo sintético que é populado com mídia de disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="709e1-105">This hard disk drive can be either a pass-through device (if a physical hard disk was attached to the virtual machine) or a synthetic device that is populated with virtual hard disk media.</span></span> <span data-ttu-id="709e1-106">Como discos rígidos virtuais e físicos podem ser adicionados e removidos da máquina virtual, há dois pools de recursos associados a essa classe, um para discos rígidos de passagem e o outro para discos rígidos virtuais.</span><span class="sxs-lookup"><span data-stu-id="709e1-106">Because virtual and physical hard disks can be added and removed from the virtual machine, there are two resource pools associated with this class, one for pass-through hard disks and the other for virtual hard disks.</span></span> <span data-ttu-id="709e1-107">Os discos rígidos só podem ser adicionados ou removidos do controlador SCSI virtual quando a máquina virtual está online.</span><span class="sxs-lookup"><span data-stu-id="709e1-107">Hard disks can only be added to or removed from the virtual SCSI controller when the virtual machine is online.</span></span> <span data-ttu-id="709e1-108">Os discos só podem ser adicionados ou removidos do controlador IDE virtual quando a máquina virtual estiver offline.</span><span class="sxs-lookup"><span data-stu-id="709e1-108">Disks can only be added to or removed from the virtual IDE controller when the virtual machine is offline.</span></span>

<span data-ttu-id="709e1-109">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="709e1-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="709e1-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="709e1-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DiskDrive : CIM_DiskDrive
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   CreationClassName;
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   ErrorMethodology = "None";
  string   CompressionMethod = "Not Compressed";
  uint32   NumberOfMediaSupported = 1;
  uint64   MaxMediaSize = 2000000000;
  uint64   DefaultBlockSize = 512;
  uint64   MaxBlockSize;
  uint64   MinBlockSize = 512;
  boolean  NeedsCleaning = False;
  boolean  MediaIsLocked = True;
  uint16   Security = 3;
  datetime LastCleaned;
  uint64   MaxAccessTime = 0;
  uint32   UncompressedDataRate;
  uint64   LoadTime = 0;
  uint64   UnloadTime = 0;
  uint64   MountCount = 0;
  datetime TimeOfLastMount;
  uint64   TotalMountTime = 0;
  string   UnitsDescription;
  uint64   MaxUnitsBeforeCleaning = 0xffffffffffffffff;
  uint64   UnitsUsed = 0;
  uint32   DriveNumber;
};
```

## <a name="members"></a><span data-ttu-id="709e1-111">Membros</span><span class="sxs-lookup"><span data-stu-id="709e1-111">Members</span></span>

<span data-ttu-id="709e1-112">A classe **Msvm \_ DiskDrive** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="709e1-112">The **Msvm\_DiskDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="709e1-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="709e1-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="709e1-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="709e1-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="709e1-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="709e1-115">Methods</span></span>

<span data-ttu-id="709e1-116">A classe **Msvm \_ DiskDrive** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="709e1-116">The **Msvm\_DiskDrive** class has these methods.</span></span>



| <span data-ttu-id="709e1-117">Método</span><span class="sxs-lookup"><span data-stu-id="709e1-117">Method</span></span>                                                          | <span data-ttu-id="709e1-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="709e1-118">Description</span></span>                              |
|:----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="709e1-119">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="709e1-119">**EnableDevice**</span></span>                                                | <span data-ttu-id="709e1-120">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="709e1-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="709e1-121">**LockMedia**</span><span class="sxs-lookup"><span data-stu-id="709e1-121">**LockMedia**</span></span>](msvm-diskdrive-lockmedia.md)                   | <span data-ttu-id="709e1-122">Bloqueia ou libera a mídia.</span><span class="sxs-lookup"><span data-stu-id="709e1-122">Locks or releases the media.</span></span><br/>  |
| <span data-ttu-id="709e1-123">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="709e1-123">**OnlineDevice**</span></span>                                                | <span data-ttu-id="709e1-124">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="709e1-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="709e1-125">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="709e1-125">**QuiesceDevice**</span></span>                                               | <span data-ttu-id="709e1-126">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="709e1-126">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="709e1-127">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="709e1-127">**RequestStateChange**</span></span>](msvm-diskdrive-requeststatechange.md) | <span data-ttu-id="709e1-128">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="709e1-128">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="709e1-129">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="709e1-129">**Reset**</span></span>](msvm-diskdrive-reset.md)                           | <span data-ttu-id="709e1-130">Redefine o dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="709e1-130">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="709e1-131">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="709e1-131">**RestoreProperties**</span></span>                                           | <span data-ttu-id="709e1-132">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="709e1-132">This method is not supported.</span></span><br/> |
| <span data-ttu-id="709e1-133">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="709e1-133">**SaveProperties**</span></span>                                              | <span data-ttu-id="709e1-134">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="709e1-134">This method is not supported.</span></span><br/> |
| <span data-ttu-id="709e1-135">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="709e1-135">**SetPowerState**</span></span>                                               | <span data-ttu-id="709e1-136">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="709e1-136">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="709e1-137">Propriedades</span><span class="sxs-lookup"><span data-stu-id="709e1-137">Properties</span></span>

<span data-ttu-id="709e1-138">A classe **Msvm \_ DiskDrive** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="709e1-138">The **Msvm\_DiskDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="709e1-139">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="709e1-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-140">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="709e1-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="709e1-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-142">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como 6 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="709e1-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="709e1-143">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="709e1-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-144">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="709e1-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-146">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="709e1-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="709e1-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="709e1-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-148">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="709e1-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="709e1-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-150">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="709e1-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="709e1-151">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="709e1-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="709e1-152">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="709e1-152">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-153">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="709e1-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="709e1-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-155">Os recursos do dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="709e1-155">The capabilities of the media access device.</span></span> <span data-ttu-id="709e1-156">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)e é definida com os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="709e1-156">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to the following values.</span></span>



| <span data-ttu-id="709e1-157">Valor</span><span class="sxs-lookup"><span data-stu-id="709e1-157">Value</span></span>                                                                        | <span data-ttu-id="709e1-158">Significado</span><span class="sxs-lookup"><span data-stu-id="709e1-158">Meaning</span></span>                                                                                 |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="709e1-159"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="709e1-159"><dt>3</dt></span></span> </dl> | <span data-ttu-id="709e1-160">A entrada correspondente em **CapabilityDescriptions** é "acesso aleatório".</span><span class="sxs-lookup"><span data-stu-id="709e1-160">The corresponding entry in **CapabilityDescriptions** is "Random Access".</span></span><br/>    |
| <dl> <span data-ttu-id="709e1-161"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="709e1-161"><dt>4</dt></span></span> </dl> | <span data-ttu-id="709e1-162">A entrada correspondente em **CapabilityDescriptions** é "suporta gravação".</span><span class="sxs-lookup"><span data-stu-id="709e1-162">The corresponding entry in **CapabilityDescriptions** is "Supports Writing".</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="709e1-163">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="709e1-163">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-164">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="709e1-164">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="709e1-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-166">Uma matriz de cadeias de caracteres de forma livre que fornece explicações detalhadas para acessar recursos do dispositivo indicados na matriz de propriedades **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="709e1-166">An array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="709e1-167">Cada entrada dessa matriz está relacionada à entrada na matriz de propriedades de **recursos** , localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="709e1-167">Each entry of this array is related to the entry in the **Capabilities** property array, located at the same index.</span></span> <span data-ttu-id="709e1-168">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="709e1-168">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="709e1-169">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="709e1-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-170">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="709e1-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-172">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="709e1-172">A short description of the object.</span></span> <span data-ttu-id="709e1-173">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="709e1-173">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="709e1-174">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="709e1-174">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-175">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="709e1-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-177">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="709e1-177">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="709e1-178">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="709e1-178">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="709e1-179">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="709e1-179">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="709e1-180"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="709e1-180"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-181"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="709e1-181"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-182"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="709e1-182"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-183"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="709e1-183"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-184"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="709e1-184"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-185"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="709e1-185"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-186"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="709e1-186"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="709e1-187">)</span><span class="sxs-lookup"><span data-stu-id="709e1-187">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="709e1-188">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="709e1-188">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="709e1-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-191">Uma cadeia de caracteres que indica o algoritmo ou a ferramenta usada para compactar o arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="709e1-191">A string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="709e1-192">Se o esquema de compactação for desconhecido ou não estiver descrito, use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="709e1-192">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="709e1-193">Se o arquivo lógico estiver compactado, mas o esquema de compactação for desconhecido ou não estiver descrito, use "compactado".</span><span class="sxs-lookup"><span data-stu-id="709e1-193">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="709e1-194">Se o arquivo lógico não estiver compactado, use "não compactado".</span><span class="sxs-lookup"><span data-stu-id="709e1-194">If the logical file is not compressed, use "Not Compressed".</span></span> <span data-ttu-id="709e1-195">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)e é definida como "não compactada".</span><span class="sxs-lookup"><span data-stu-id="709e1-195">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to "Not Compressed".</span></span>

</dd> <dt>

<span data-ttu-id="709e1-196">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="709e1-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-197">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="709e1-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-199">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="709e1-199">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="709e1-200">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="709e1-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="709e1-201">**Defaultblockize**</span><span class="sxs-lookup"><span data-stu-id="709e1-201">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-202">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="709e1-202">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-204">O tamanho do bloco padrão, em bytes, para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="709e1-204">The default block size, in bytes, for the device.</span></span> <span data-ttu-id="709e1-205">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)e é definida como 512.</span><span class="sxs-lookup"><span data-stu-id="709e1-205">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 512.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-206">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="709e1-206">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-207">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="709e1-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-209">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="709e1-209">A description of the object.</span></span> <span data-ttu-id="709e1-210">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="709e1-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="709e1-211">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="709e1-211">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-212">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="709e1-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-214">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="709e1-214">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="709e1-215">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="709e1-215">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="709e1-216">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="709e1-216">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="709e1-217"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="709e1-217"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-218"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="709e1-218"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-219"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="709e1-219"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-220"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="709e1-220"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-221"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="709e1-221"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-222"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="709e1-222"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="709e1-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="709e1-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="709e1-225">)</span><span class="sxs-lookup"><span data-stu-id="709e1-225">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="709e1-226">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="709e1-226">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-227">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="709e1-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-229">Um endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="709e1-229">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="709e1-230">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="709e1-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="709e1-231">**DriveNumber**</span><span class="sxs-lookup"><span data-stu-id="709e1-231">**DriveNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-232">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="709e1-232">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-234">O número de unidades físicas no sistema de computador de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="709e1-234">The number of the physical drives on the hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-235">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="709e1-235">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-236">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="709e1-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-237">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-238">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="709e1-238">A display name for the object.</span></span> <span data-ttu-id="709e1-239">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="709e1-239">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="709e1-240">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="709e1-240">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-241">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="709e1-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-242">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-243">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="709e1-243">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="709e1-244">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="709e1-244">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="709e1-245">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="709e1-245">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-246">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="709e1-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-247">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-248">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="709e1-248">The enabled and disabled states of an element.</span></span> <span data-ttu-id="709e1-249">Ele também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="709e1-249">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="709e1-250">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="709e1-250">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="709e1-251">Valor</span><span class="sxs-lookup"><span data-stu-id="709e1-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="709e1-252">Significado</span><span class="sxs-lookup"><span data-stu-id="709e1-252">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="709e1-253"><dt></dt> <dt>0</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="709e1-253"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="709e1-254">Não foi possível determinar o estado do elemento.</span><span class="sxs-lookup"><span data-stu-id="709e1-254">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="709e1-255"><dt>**Outros**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="709e1-255"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="709e1-256"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="709e1-256"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="709e1-257">O elemento está em execução.</span><span class="sxs-lookup"><span data-stu-id="709e1-257">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="709e1-258"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="709e1-258"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="709e1-259">O elemento está desativado.</span><span class="sxs-lookup"><span data-stu-id="709e1-259">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="709e1-260"><dt>**Desligando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="709e1-260"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="709e1-261">O elemento está no processo de ir para um estado desabilitado.</span><span class="sxs-lookup"><span data-stu-id="709e1-261">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="709e1-262"><dt>**Não aplicável**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="709e1-262"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="709e1-263">O elemento não dá suporte a ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="709e1-263">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="709e1-264"><dt>**Habilitado, mas offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="709e1-264"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="709e1-265">O elemento pode estar concluindo comandos e removerá todas as novas solicitações.</span><span class="sxs-lookup"><span data-stu-id="709e1-265">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="709e1-266"><dt>**No teste**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="709e1-266"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="709e1-267">O elemento está em um estado de teste.</span><span class="sxs-lookup"><span data-stu-id="709e1-267">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="709e1-268"><dt>**Adiado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="709e1-268"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="709e1-269">O elemento pode estar concluindo comandos, mas colocará todas as novas solicitações na fila.</span><span class="sxs-lookup"><span data-stu-id="709e1-269">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="709e1-270"><dt>**Desativar**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="709e1-270"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="709e1-271">O elemento está habilitado, mas está em um modo restrito.</span><span class="sxs-lookup"><span data-stu-id="709e1-271">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="709e1-272">O comportamento do elemento é semelhante ao estado habilitado (2), mas processa apenas um conjunto restrito de comandos.</span><span class="sxs-lookup"><span data-stu-id="709e1-272">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="709e1-273">Todas as outras solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="709e1-273">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="709e1-274"><dt>**Iniciando**</dt> em <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="709e1-274"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="709e1-275">O elemento está no processo de ir para um estado habilitado (2).</span><span class="sxs-lookup"><span data-stu-id="709e1-275">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="709e1-276">Novas solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="709e1-276">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="709e1-277">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="709e1-277">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-278">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="709e1-278">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-280">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="709e1-280">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-281">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="709e1-281">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-282">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="709e1-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-283">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-284">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="709e1-284">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-285">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="709e1-285">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-286">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="709e1-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-287">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-288">Uma cadeia de caracteres que descreve os tipos de detecção de erros e correção com suporte neste dispositivo.</span><span class="sxs-lookup"><span data-stu-id="709e1-288">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="709e1-289">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)e é definida como "None".</span><span class="sxs-lookup"><span data-stu-id="709e1-289">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to "None".</span></span>

</dd> <dt>

<span data-ttu-id="709e1-290">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="709e1-290">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-291">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="709e1-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-292">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-293">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="709e1-293">The current health of the element.</span></span> <span data-ttu-id="709e1-294">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="709e1-294">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="709e1-295">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="709e1-295">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="709e1-296">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5.</span><span class="sxs-lookup"><span data-stu-id="709e1-296">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-297">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="709e1-297">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-298">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="709e1-298">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="709e1-299">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-300">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="709e1-300">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-301">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="709e1-301">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-302">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="709e1-302">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-303">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-304">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="709e1-304">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="709e1-305">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="709e1-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="709e1-306">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="709e1-306">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-307">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="709e1-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-308">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="709e1-309">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="709e1-309">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="709e1-310">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="709e1-310">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="709e1-311">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="709e1-311">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="709e1-312">**LastCleaned**</span><span class="sxs-lookup"><span data-stu-id="709e1-312">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-313">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="709e1-313">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-315">A data e a hora da última limpeza do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="709e1-315">The date and time when the device was last cleaned.</span></span> <span data-ttu-id="709e1-316">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="709e1-316">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-317">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="709e1-317">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-318">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="709e1-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-319">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-320">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="709e1-320">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-321">**Loadtime**</span><span class="sxs-lookup"><span data-stu-id="709e1-321">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-322">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="709e1-322">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-323">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-324">O tempo, em milissegundos, do carregamento para poder ler ou gravar uma mídia.</span><span class="sxs-lookup"><span data-stu-id="709e1-324">The time, in milliseconds, from load to being able to read or write a media.</span></span> <span data-ttu-id="709e1-325">Por exemplo, para unidades de disco, esse é o intervalo entre um disco que não está girando para o disco que está pronto para leitura/gravação (ou seja, o disco girando em velocidades nominais).</span><span class="sxs-lookup"><span data-stu-id="709e1-325">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write (that is, the disk spinning at nominal speeds).</span></span> <span data-ttu-id="709e1-326">Para unidades de fita, esse é o tempo de uma mídia que está sendo injetada para relatar que está pronta para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="709e1-326">For tape drives, this is the time from a media being injected to reporting that it is ready for an application.</span></span> <span data-ttu-id="709e1-327">Isso geralmente ocorre na área de BOT da fita.</span><span class="sxs-lookup"><span data-stu-id="709e1-327">This is usually at the tape's BOT area.</span></span> <span data-ttu-id="709e1-328">Essa propriedade é herdada de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice) e é definida como 0.</span><span class="sxs-lookup"><span data-stu-id="709e1-328">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice) and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-329">**MaxAccessTime**</span><span class="sxs-lookup"><span data-stu-id="709e1-329">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-330">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="709e1-330">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-331">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-332">O tempo, em milissegundos, a ser movido do primeiro local na mídia para o local mais distante em relação ao tempo.</span><span class="sxs-lookup"><span data-stu-id="709e1-332">The time, in milliseconds, to move from the first location on the media to the location that is furthest with respect to time.</span></span> <span data-ttu-id="709e1-333">Para uma unidade de disco, isso representa a busca completa e o atraso de rotação completo.</span><span class="sxs-lookup"><span data-stu-id="709e1-333">For a disk drive, this represents full seek and full rotational delay.</span></span> <span data-ttu-id="709e1-334">Para unidades de fita, isso representa uma pesquisa desde o início da fita até o ponto distante fisicamente.</span><span class="sxs-lookup"><span data-stu-id="709e1-334">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span> <span data-ttu-id="709e1-335">(O fim de uma fita pode estar em seu ponto mais distante fisicamente, mas isso não é necessariamente verdadeiro.) Essa propriedade é herdada de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)e é definida como 0.</span><span class="sxs-lookup"><span data-stu-id="709e1-335">(The end of a tape may be at its most physically distant point, but this is not necessarily true.) This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-336">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="709e1-336">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-337">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="709e1-337">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-338">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-339">O tamanho máximo do bloco, em bytes, para a mídia acessada pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="709e1-339">The maximum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="709e1-340">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)e é definida como 512 para unidades de disco rígido virtual, variável para unidades de passagem.</span><span class="sxs-lookup"><span data-stu-id="709e1-340">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 512 for virtual hard disk drives, variable for pass-through drives.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-341">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="709e1-341">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-342">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="709e1-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-344">O tamanho máximo, em kilobytes, da mídia com suporte neste dispositivo.</span><span class="sxs-lookup"><span data-stu-id="709e1-344">The maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="709e1-345">Kilobytes são interpretados como o número de bytes multiplicado por 1000 (não o número de bytes multiplicado por 1024).</span><span class="sxs-lookup"><span data-stu-id="709e1-345">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span> <span data-ttu-id="709e1-346">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)e é definida como 2.000.000.000 para unidades de disco rígido virtual, variável para unidades de passagem.</span><span class="sxs-lookup"><span data-stu-id="709e1-346">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 2,000,000,000 for virtual hard disk drives, variable for pass-through drives.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-347">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="709e1-347">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-348">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="709e1-348">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-349">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-350">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="709e1-350">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-351">**MaxUnitsBeforeCleaning**</span><span class="sxs-lookup"><span data-stu-id="709e1-351">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-352">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="709e1-352">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-354">As unidades máximas que podem ser usadas antes de o dispositivo ser limpo.</span><span class="sxs-lookup"><span data-stu-id="709e1-354">The maximum units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="709e1-355">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)e é definida como 0xFFFFFFFFFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="709e1-355">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0xffffffffffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-356">**MediaIsLocked**</span><span class="sxs-lookup"><span data-stu-id="709e1-356">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-357">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="709e1-357">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-358">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-359">**True** se a mídia estiver bloqueada no dispositivo e não puder ser ejetada; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="709e1-359">**True** if the media is locked in the device and cannot be ejected; otherwise, **False**.</span></span> <span data-ttu-id="709e1-360">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)e é definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="709e1-360">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-361">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="709e1-361">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-362">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="709e1-362">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-363">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-364">O tamanho mínimo do bloco, em bytes, para a mídia acessada pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="709e1-364">The minimum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="709e1-365">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)e é definida como 512.</span><span class="sxs-lookup"><span data-stu-id="709e1-365">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 512.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-366">**MountCount**</span><span class="sxs-lookup"><span data-stu-id="709e1-366">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-367">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="709e1-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-368">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-369">Para um dispositivo que oferece suporte a mídia removível, o número de vezes que a mídia foi montada para transferência de dados ou para limpar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="709e1-369">For a device that supports removable media, the number of times that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="709e1-370">Para dispositivos que acessam mídia nonremovable, como discos rígidos, essa propriedade não é aplicável e deve ser definida como 0.</span><span class="sxs-lookup"><span data-stu-id="709e1-370">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="709e1-371">Essa propriedade é herdada de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)e é definida como 0.</span><span class="sxs-lookup"><span data-stu-id="709e1-371">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-372">**Nome**</span><span class="sxs-lookup"><span data-stu-id="709e1-372">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-373">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="709e1-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-374">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-375">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="709e1-375">The label by which the object is known.</span></span> <span data-ttu-id="709e1-376">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="709e1-376">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="709e1-377">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="709e1-377">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-378">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="709e1-378">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-379">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-380">**True** se o dispositivo de acesso à mídia precisar de limpeza; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="709e1-380">**True** if the media access device needs cleaning; otherwise, **False**.</span></span> <span data-ttu-id="709e1-381">Essa propriedade é herdada de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)e é definida como **false**.</span><span class="sxs-lookup"><span data-stu-id="709e1-381">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-382">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="709e1-382">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-383">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="709e1-383">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-384">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-385">O número máximo de várias mídias individuais que podem ser suportadas ou inseridas.</span><span class="sxs-lookup"><span data-stu-id="709e1-385">The maximum number of multiple individual media that can be supported or inserted.</span></span> <span data-ttu-id="709e1-386">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)e é definida como 1.</span><span class="sxs-lookup"><span data-stu-id="709e1-386">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-387">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="709e1-387">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-388">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="709e1-388">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-389">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-390">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="709e1-390">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="709e1-391">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="709e1-391">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="709e1-392">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="709e1-392">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="709e1-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="709e1-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-394"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="709e1-394"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-395"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="709e1-395"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-396"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="709e1-396"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-397"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="709e1-397"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-398"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="709e1-398"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-399"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="709e1-399"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-400"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="709e1-400"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-401"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="709e1-401"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-402"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="709e1-402"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-403"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="709e1-403"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-404"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="709e1-404"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-405"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="709e1-405"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-406"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="709e1-406"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-407"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="709e1-407"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-408"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="709e1-408"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-409"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="709e1-409"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-410"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="709e1-410"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-411"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="709e1-411"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="709e1-412">)</span><span class="sxs-lookup"><span data-stu-id="709e1-412">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="709e1-413">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="709e1-413">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-414">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="709e1-414">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="709e1-415">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-416">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="709e1-416">The current statuses of the object.</span></span> <span data-ttu-id="709e1-417">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="709e1-417">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="709e1-418">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="709e1-418">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-419">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="709e1-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-420">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-421">O estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="709e1-421">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="709e1-422">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="709e1-422">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="709e1-423">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="709e1-423">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-424">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="709e1-424">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-425">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="709e1-425">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="709e1-426">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-427">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="709e1-427">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-428">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="709e1-428">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-429">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="709e1-429">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="709e1-430">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-431">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="709e1-431">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-432">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="709e1-432">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-433">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="709e1-433">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-434">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-435">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="709e1-435">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-436">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="709e1-436">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-437">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="709e1-437">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-438">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-439">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="709e1-439">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-440">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="709e1-440">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-441">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="709e1-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-442">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-443">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="709e1-443">Provides high level status information.</span></span> <span data-ttu-id="709e1-444">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="709e1-444">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="709e1-445">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="709e1-445">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="709e1-446">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="709e1-446">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="709e1-447"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="709e1-447"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-448"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="709e1-448"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-449"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="709e1-449"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-450"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="709e1-450"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-451"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="709e1-451"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="709e1-452"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="709e1-452"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="709e1-453">)</span><span class="sxs-lookup"><span data-stu-id="709e1-453">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="709e1-454">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="709e1-454">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-455">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="709e1-455">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-456">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-457">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="709e1-457">The last requested or desired state for the element.</span></span> <span data-ttu-id="709e1-458">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="709e1-458">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="709e1-459">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="709e1-459">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="709e1-460">Uma determinada instância do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) pode não dar suporte ao método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="709e1-460">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="709e1-461">Se isso ocorrer, o valor 12 (não aplicável) será usado.</span><span class="sxs-lookup"><span data-stu-id="709e1-461">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="709e1-462">Essa propriedade é herdada do **CIM \_ EnabledLogicalElement**.</span><span class="sxs-lookup"><span data-stu-id="709e1-462">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-463">**Segurança**</span><span class="sxs-lookup"><span data-stu-id="709e1-463">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-464">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="709e1-464">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-465">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-466">A segurança operacional definida para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="709e1-466">The operational security defined for the device.</span></span> <span data-ttu-id="709e1-467">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)e é definida como 3 (nenhuma).</span><span class="sxs-lookup"><span data-stu-id="709e1-467">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 3 (None).</span></span>

</dd> <dt>

<span data-ttu-id="709e1-468">**Status**</span><span class="sxs-lookup"><span data-stu-id="709e1-468">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-469">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="709e1-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-470">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-471">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="709e1-471">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-472">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="709e1-472">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-473">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="709e1-473">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="709e1-474">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-474">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-475">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="709e1-475">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="709e1-476">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="709e1-476">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="709e1-477">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="709e1-477">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-478">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="709e1-478">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-479">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-480">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="709e1-480">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-481">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="709e1-481">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-482">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="709e1-482">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-483">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-484">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="709e1-484">The scoping system's creation class name.</span></span> <span data-ttu-id="709e1-485">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="709e1-485">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="709e1-486">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="709e1-486">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-487">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="709e1-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-488">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-488">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-489">O identificador exclusivo para a máquina virtual de escopo.</span><span class="sxs-lookup"><span data-stu-id="709e1-489">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="709e1-490">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="709e1-490">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="709e1-491">**TimeOfLastMount**</span><span class="sxs-lookup"><span data-stu-id="709e1-491">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-492">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="709e1-492">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-493">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-493">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-494">Para um dispositivo que oferece suporte a mídia removível, a data e a hora mais recentes em que a mídia foi montada no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="709e1-494">For a device that supports removable media, the most recent date and time that media was mounted on the device.</span></span> <span data-ttu-id="709e1-495">Para dispositivos que acessam mídia nonremovable, como discos rígidos, essa propriedade não tem significado e não é aplicável.</span><span class="sxs-lookup"><span data-stu-id="709e1-495">For devices accessing nonremovable media, such as hard disks, this property has no meaning and is not applicable.</span></span> <span data-ttu-id="709e1-496">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="709e1-496">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-497">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="709e1-497">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-498">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="709e1-498">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-499">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-500">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="709e1-500">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="709e1-501">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como "NULL".</span><span class="sxs-lookup"><span data-stu-id="709e1-501">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to "NULL".</span></span>

</dd> <dt>

<span data-ttu-id="709e1-502">**TotalMountTime**</span><span class="sxs-lookup"><span data-stu-id="709e1-502">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-503">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="709e1-503">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-504">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-505">Para um dispositivo que dá suporte à mídia removível, o tempo total (em segundos) que a mídia foi montada para transferência de dados ou para limpar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="709e1-505">For a device that supports removable media, the total time (in seconds) that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="709e1-506">Para dispositivos que acessam mídia nonremovable, como discos rígidos, essa propriedade não é aplicável e deve ser definida como 0.</span><span class="sxs-lookup"><span data-stu-id="709e1-506">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="709e1-507">Essa propriedade é herdada de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)e é definida como 0.</span><span class="sxs-lookup"><span data-stu-id="709e1-507">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-508">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="709e1-508">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-509">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="709e1-509">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-510">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-511">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="709e1-511">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-512">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="709e1-512">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-513">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="709e1-513">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-514">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-515">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="709e1-515">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="709e1-516">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="709e1-516">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="709e1-517">**UncompressedDataRate**</span><span class="sxs-lookup"><span data-stu-id="709e1-517">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-518">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="709e1-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-519">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-520">A taxa de transferência de dados sustentada em KB/s que o dispositivo pode ler e gravar em uma mídia.</span><span class="sxs-lookup"><span data-stu-id="709e1-520">The sustained data transfer rate in KB/sec that the device can read from and write to a media.</span></span> <span data-ttu-id="709e1-521">Essa é uma taxa de dados bruta e prolongada.</span><span class="sxs-lookup"><span data-stu-id="709e1-521">This is a sustained, raw data rate.</span></span> <span data-ttu-id="709e1-522">Taxas ou taxas máximas supondo que a compactação não deve ser relatada nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="709e1-522">Maximum rates or rates assuming compression should not be reported in this property.</span></span> <span data-ttu-id="709e1-523">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="709e1-523">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-524">**UnitsDescription**</span><span class="sxs-lookup"><span data-stu-id="709e1-524">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-525">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="709e1-525">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-526">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-526">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-527">As unidades relativas ao seu uso em **MaxUnitsBeforeCleaning**.</span><span class="sxs-lookup"><span data-stu-id="709e1-527">The units relative to its use in **MaxUnitsBeforeCleaning**.</span></span> <span data-ttu-id="709e1-528">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="709e1-528">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-529">**UnitsUsed**</span><span class="sxs-lookup"><span data-stu-id="709e1-529">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-530">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="709e1-530">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-531">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-531">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-532">O número atual de unidades usadas.</span><span class="sxs-lookup"><span data-stu-id="709e1-532">The current number of units used.</span></span> <span data-ttu-id="709e1-533">Essa propriedade é herdada de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)e é definida como 0.</span><span class="sxs-lookup"><span data-stu-id="709e1-533">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="709e1-534">**Descarregar**</span><span class="sxs-lookup"><span data-stu-id="709e1-534">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="709e1-535">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="709e1-535">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="709e1-536">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="709e1-536">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="709e1-537">O tempo, em milissegundos, de ser capaz de ler ou gravar uma mídia em seu descarregamento.</span><span class="sxs-lookup"><span data-stu-id="709e1-537">The time, in milliseconds, from being able to read or write a media to its unload.</span></span> <span data-ttu-id="709e1-538">Essa propriedade é herdada de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)e é definida como 0.</span><span class="sxs-lookup"><span data-stu-id="709e1-538">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="709e1-539">Comentários</span><span class="sxs-lookup"><span data-stu-id="709e1-539">Remarks</span></span>

<span data-ttu-id="709e1-540">O acesso à classe **Msvm \_ DiskDrive** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="709e1-540">Access to the **Msvm\_DiskDrive** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="709e1-541">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="709e1-541">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="709e1-542">Requisitos</span><span class="sxs-lookup"><span data-stu-id="709e1-542">Requirements</span></span>



| <span data-ttu-id="709e1-543">Requisito</span><span class="sxs-lookup"><span data-stu-id="709e1-543">Requirement</span></span> | <span data-ttu-id="709e1-544">Valor</span><span class="sxs-lookup"><span data-stu-id="709e1-544">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="709e1-545">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="709e1-545">Minimum supported client</span></span><br/> | <span data-ttu-id="709e1-546">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="709e1-546">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="709e1-547">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="709e1-547">Minimum supported server</span></span><br/> | <span data-ttu-id="709e1-548">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="709e1-548">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="709e1-549">Namespace</span><span class="sxs-lookup"><span data-stu-id="709e1-549">Namespace</span></span><br/>                | <span data-ttu-id="709e1-550">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="709e1-550">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="709e1-551">MOF</span><span class="sxs-lookup"><span data-stu-id="709e1-551">MOF</span></span><br/>                      | <dl> <span data-ttu-id="709e1-552"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="709e1-552"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="709e1-553">DLL</span><span class="sxs-lookup"><span data-stu-id="709e1-553">DLL</span></span><br/>                      | <dl> <span data-ttu-id="709e1-554"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="709e1-554"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="709e1-555">Confira também</span><span class="sxs-lookup"><span data-stu-id="709e1-555">See also</span></span>

<dl> <dt>

[<span data-ttu-id="709e1-556">**\_DISKDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="709e1-556">**CIM\_DiskDrive**</span></span>](cim-diskdrive.md)
</dt> <dt>

[<span data-ttu-id="709e1-557">**\_DISKDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="709e1-557">**CIM\_DiskDrive**</span></span>](/windows/desktop/CIMWin32Prov/cim-diskdrive)
</dt> <dt>

[<span data-ttu-id="709e1-558">Classes de armazenamento</span><span class="sxs-lookup"><span data-stu-id="709e1-558">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

