---
description: Representa uma unidade de disquete dentro da máquina virtual.
ms.assetid: 4624ABAF-3761-416F-9044-7A39EBF53D3D
title: Classe Msvm_DisketteDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteDrive
- Msvm_DisketteDrive.SetPowerState
- Msvm_DisketteDrive.EnableDevice
- Msvm_DisketteDrive.OnlineDevice
- Msvm_DisketteDrive.QuiesceDevice
- Msvm_DisketteDrive.SaveProperties
- Msvm_DisketteDrive.RestoreProperties
- Msvm_DisketteDrive.InstanceID
- Msvm_DisketteDrive.Caption
- Msvm_DisketteDrive.Description
- Msvm_DisketteDrive.ElementName
- Msvm_DisketteDrive.InstallDate
- Msvm_DisketteDrive.Name
- Msvm_DisketteDrive.OperationalStatus
- Msvm_DisketteDrive.StatusDescriptions
- Msvm_DisketteDrive.Status
- Msvm_DisketteDrive.HealthState
- Msvm_DisketteDrive.CommunicationStatus
- Msvm_DisketteDrive.DetailedStatus
- Msvm_DisketteDrive.OperatingStatus
- Msvm_DisketteDrive.PrimaryStatus
- Msvm_DisketteDrive.EnabledState
- Msvm_DisketteDrive.OtherEnabledState
- Msvm_DisketteDrive.RequestedState
- Msvm_DisketteDrive.EnabledDefault
- Msvm_DisketteDrive.TimeOfLastStateChange
- Msvm_DisketteDrive.AvailableRequestedStates
- Msvm_DisketteDrive.TransitioningToState
- Msvm_DisketteDrive.SystemCreationClassName
- Msvm_DisketteDrive.SystemName
- Msvm_DisketteDrive.CreationClassName
- Msvm_DisketteDrive.DeviceID
- Msvm_DisketteDrive.PowerManagementSupported
- Msvm_DisketteDrive.PowerManagementCapabilities
- Msvm_DisketteDrive.Availability
- Msvm_DisketteDrive.StatusInfo
- Msvm_DisketteDrive.LastErrorCode
- Msvm_DisketteDrive.ErrorDescription
- Msvm_DisketteDrive.ErrorCleared
- Msvm_DisketteDrive.OtherIdentifyingInfo
- Msvm_DisketteDrive.PowerOnHours
- Msvm_DisketteDrive.TotalPowerOnHours
- Msvm_DisketteDrive.IdentifyingDescriptions
- Msvm_DisketteDrive.AdditionalAvailability
- Msvm_DisketteDrive.MaxQuiesceTime
- Msvm_DisketteDrive.Capabilities
- Msvm_DisketteDrive.CapabilityDescriptions
- Msvm_DisketteDrive.ErrorMethodology
- Msvm_DisketteDrive.CompressionMethod
- Msvm_DisketteDrive.NumberOfMediaSupported
- Msvm_DisketteDrive.MaxMediaSize
- Msvm_DisketteDrive.DefaultBlockSize
- Msvm_DisketteDrive.MaxBlockSize
- Msvm_DisketteDrive.MinBlockSize
- Msvm_DisketteDrive.NeedsCleaning
- Msvm_DisketteDrive.MediaIsLocked
- Msvm_DisketteDrive.Security
- Msvm_DisketteDrive.LastCleaned
- Msvm_DisketteDrive.MaxAccessTime
- Msvm_DisketteDrive.UncompressedDataRate
- Msvm_DisketteDrive.LoadTime
- Msvm_DisketteDrive.UnloadTime
- Msvm_DisketteDrive.MountCount
- Msvm_DisketteDrive.TimeOfLastMount
- Msvm_DisketteDrive.TotalMountTime
- Msvm_DisketteDrive.UnitsDescription
- Msvm_DisketteDrive.MaxUnitsBeforeCleaning
- Msvm_DisketteDrive.UnitsUsed
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1dbc9e21626e2f5e8269fb3a398dd48a6ea442e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662540"
---
# <a name="msvm_diskettedrive-class"></a><span data-ttu-id="51170-103">\_Classe Msvm DisketteDrive</span><span class="sxs-lookup"><span data-stu-id="51170-103">Msvm\_DisketteDrive class</span></span>

<span data-ttu-id="51170-104">Representa uma unidade de disquete dentro da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="51170-104">Represents a floppy drive inside the virtual machine.</span></span> <span data-ttu-id="51170-105">Uma unidade de disquete pode ser populada com um arquivo que representa a mídia de disquete ou a unidade pode estar vazia.</span><span class="sxs-lookup"><span data-stu-id="51170-105">A floppy drive can be populated with a file representing floppy media or the drive can be empty.</span></span> <span data-ttu-id="51170-106">Não há suporte para mídia física.</span><span class="sxs-lookup"><span data-stu-id="51170-106">Physical media is not supported.</span></span> <span data-ttu-id="51170-107">Há exatamente uma unidade de disquete por controlador de disquete e ela não é removível.</span><span class="sxs-lookup"><span data-stu-id="51170-107">There is exactly one floppy drive per floppy controller and it is not removable.</span></span>

<span data-ttu-id="51170-108">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="51170-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="51170-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51170-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DisketteDrive : CIM_DisketteDrive
{
  string   InstanceID;
  string   Caption = "Diskette Drive";
  string   Description = "Microsoft Virtual Diskette Drive";
  string   ElementName = "Diskette Drive";
  datetime InstallDate;
  string   Name = "Diskette Drive";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_DisketteDrive";
  string   DeviceID = "Microsoft:GUID\device-specific-data";
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint16   Capabilities[] = {3, 4, 7};
  string   CapabilityDescriptions[] = {"Random Access", "Supports Writing", "Supports Removable Media"};
  string   ErrorMethodology = { "None" };
  string   CompressionMethod = "Not Compressed";
  uint32   NumberOfMediaSupported = 1;
  uint64   MaxMediaSize = 1440;
  uint64   DefaultBlockSize = 512;
  uint64   MaxBlockSize = 512;
  uint64   MinBlockSize = 512;
  boolean  NeedsCleaning = False;
  boolean  MediaIsLocked = False;
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
  uint64   MaxUnitsBeforeCleaning = 18446744073709551615;
  uint64   UnitsUsed = 0;
};
```

## <a name="members"></a><span data-ttu-id="51170-110">Membros</span><span class="sxs-lookup"><span data-stu-id="51170-110">Members</span></span>

<span data-ttu-id="51170-111">A classe **Msvm \_ DisketteDrive** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="51170-111">The **Msvm\_DisketteDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="51170-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="51170-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="51170-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="51170-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="51170-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="51170-114">Methods</span></span>

<span data-ttu-id="51170-115">A classe **Msvm \_ DisketteDrive** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="51170-115">The **Msvm\_DisketteDrive** class has these methods.</span></span>



| <span data-ttu-id="51170-116">Método</span><span class="sxs-lookup"><span data-stu-id="51170-116">Method</span></span>                                                              | <span data-ttu-id="51170-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="51170-117">Description</span></span>                              |
|:--------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="51170-118">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="51170-118">**EnableDevice**</span></span>                                                    | <span data-ttu-id="51170-119">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="51170-119">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="51170-120">**LockMedia**</span><span class="sxs-lookup"><span data-stu-id="51170-120">**LockMedia**</span></span>](msvm-diskettedrive-lockmedia.md)                   | <span data-ttu-id="51170-121">Bloqueia ou libera a mídia.</span><span class="sxs-lookup"><span data-stu-id="51170-121">Locks or releases the media.</span></span><br/>  |
| <span data-ttu-id="51170-122">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="51170-122">**OnlineDevice**</span></span>                                                    | <span data-ttu-id="51170-123">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="51170-123">This method is not supported.</span></span><br/> |
| <span data-ttu-id="51170-124">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="51170-124">**QuiesceDevice**</span></span>                                                   | <span data-ttu-id="51170-125">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="51170-125">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="51170-126">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="51170-126">**RequestStateChange**</span></span>](msvm-diskettedrive-requeststatechange.md) | <span data-ttu-id="51170-127">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="51170-127">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="51170-128">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="51170-128">**Reset**</span></span>](msvm-diskettedrive-reset.md)                           | <span data-ttu-id="51170-129">Redefine o dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="51170-129">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="51170-130">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="51170-130">**RestoreProperties**</span></span>                                               | <span data-ttu-id="51170-131">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="51170-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="51170-132">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="51170-132">**SaveProperties**</span></span>                                                  | <span data-ttu-id="51170-133">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="51170-133">This method is not supported.</span></span><br/> |
| <span data-ttu-id="51170-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="51170-134">**SetPowerState**</span></span>                                                   | <span data-ttu-id="51170-135">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="51170-135">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="51170-136">Propriedades</span><span class="sxs-lookup"><span data-stu-id="51170-136">Properties</span></span>

<span data-ttu-id="51170-137">A classe **Msvm \_ DisketteDrive** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="51170-137">The **Msvm\_DisketteDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="51170-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="51170-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-139">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51170-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="51170-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-141">Qualquer disponibilidade e status adicionais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="51170-141">Any additional availability and status of the device.</span></span> <span data-ttu-id="51170-142">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="51170-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="51170-143">Valor</span><span class="sxs-lookup"><span data-stu-id="51170-143">Value</span></span>                                                                        | <span data-ttu-id="51170-144">Significado</span><span class="sxs-lookup"><span data-stu-id="51170-144">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="51170-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="51170-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="51170-146">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="51170-146">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="51170-147">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="51170-147">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-148">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51170-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51170-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-150">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="51170-150">The primary availability and status of the device.</span></span> <span data-ttu-id="51170-151">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="51170-151">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="51170-152">Valor</span><span class="sxs-lookup"><span data-stu-id="51170-152">Value</span></span>                                                                        | <span data-ttu-id="51170-153">Significado</span><span class="sxs-lookup"><span data-stu-id="51170-153">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="51170-154"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="51170-154"><dt>6</dt></span></span> </dl> | <span data-ttu-id="51170-155">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="51170-155">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="51170-156">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="51170-156">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-157">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51170-157">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="51170-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-159">Indica os valores possíveis para o parâmetro *requestedstate* do método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="51170-159">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="51170-160">Os valores listados serão um subconjunto dos valores contidos na propriedade **RequestedStatesSupported** da instância associada do **CIM \_ EnabledLogicalElementCapabilities**, em que os valores selecionados são uma função do estado atual do objeto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="51170-160">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="51170-161">Essa propriedade pode ser não **nula** se uma implementação for capaz de anunciar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="51170-161">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="51170-162">Essa propriedade será **nula** se uma implementação não puder determinar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="51170-162">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="51170-163">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="51170-163">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="51170-164">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="51170-164">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-165">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51170-165">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="51170-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-167">Os recursos do dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="51170-167">The capabilities of the media access device.</span></span> <span data-ttu-id="51170-168">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)e é definida com os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="51170-168">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to the following values.</span></span>



| <span data-ttu-id="51170-169">Valor</span><span class="sxs-lookup"><span data-stu-id="51170-169">Value</span></span>                                                                                | <span data-ttu-id="51170-170">Significado</span><span class="sxs-lookup"><span data-stu-id="51170-170">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="51170-171"><dt>{3, 4, 7}</dt></span><span class="sxs-lookup"><span data-stu-id="51170-171"><dt>{3, 4, 7}</dt></span></span> </dl> |                                                                                                 |
| <dl> <span data-ttu-id="51170-172"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="51170-172"><dt>3</dt></span></span> </dl>         | <span data-ttu-id="51170-173">A entrada correspondente em **CapabilityDescriptions** é "acesso aleatório".</span><span class="sxs-lookup"><span data-stu-id="51170-173">The corresponding entry in **CapabilityDescriptions** is "Random Access".</span></span><br/>            |
| <dl> <span data-ttu-id="51170-174"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="51170-174"><dt>4</dt></span></span> </dl>         | <span data-ttu-id="51170-175">A entrada correspondente em **CapabilityDescriptions** é "suporta gravação".</span><span class="sxs-lookup"><span data-stu-id="51170-175">The corresponding entry in **CapabilityDescriptions** is "Supports Writing".</span></span><br/>         |
| <dl> <span data-ttu-id="51170-176"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="51170-176"><dt>7</dt></span></span> </dl>         | <span data-ttu-id="51170-177">A entrada correspondente em **CapabilityDescriptions** é "dá suporte à mídia removível".</span><span class="sxs-lookup"><span data-stu-id="51170-177">The corresponding entry in **CapabilityDescriptions** is "Supports Removable Media".</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="51170-178">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="51170-178">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-179">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51170-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="51170-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-181">Uma matriz de cadeias de caracteres de forma livre que fornece explicações detalhadas para acessar recursos do dispositivo indicados na matriz de propriedades **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="51170-181">An array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="51170-182">Cada entrada dessa matriz está relacionada à entrada na matriz **Capabilities** , localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="51170-182">Each entry of this array is related to the entry in the **Capabilities** array, located at the same index.</span></span> <span data-ttu-id="51170-183">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="51170-183">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="51170-184">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="51170-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-185">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51170-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51170-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-187">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="51170-187">A short description of the object.</span></span> <span data-ttu-id="51170-188">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="51170-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="51170-189">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="51170-189">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-190">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51170-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51170-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-192">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="51170-192">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="51170-193">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="51170-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="51170-194">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="51170-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="51170-195">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="51170-195">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-196">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51170-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51170-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-198">Uma cadeia de caracteres que indica o algoritmo ou a ferramenta usada para compactar o arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="51170-198">A string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="51170-199">Se o esquema de compactação for desconhecido ou não estiver descrito, use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="51170-199">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="51170-200">Se o arquivo lógico estiver compactado, mas o esquema de compactação for desconhecido ou não estiver descrito, use "compactado".</span><span class="sxs-lookup"><span data-stu-id="51170-200">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="51170-201">Se o arquivo lógico não estiver compactado, use "não compactado".</span><span class="sxs-lookup"><span data-stu-id="51170-201">If the logical file is not compressed, use "Not Compressed".</span></span> <span data-ttu-id="51170-202">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="51170-202">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

<span data-ttu-id="51170-203">"Não compactado"</span><span class="sxs-lookup"><span data-stu-id="51170-203">"Not Compressed"</span></span>

<span data-ttu-id="51170-204">Conhecidos</span><span class="sxs-lookup"><span data-stu-id="51170-204">"Unknown"</span></span>

<span data-ttu-id="51170-205">Compactados</span><span class="sxs-lookup"><span data-stu-id="51170-205">"Compressed"</span></span>

<span data-ttu-id="51170-206">"Não compactado"</span><span class="sxs-lookup"><span data-stu-id="51170-206">"Not Compressed"</span></span>

</dd> <dt>

<span data-ttu-id="51170-207">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="51170-207">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-208">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51170-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51170-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-210">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="51170-210">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="51170-211">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="51170-211">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="51170-212">**Defaultblockize**</span><span class="sxs-lookup"><span data-stu-id="51170-212">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-213">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="51170-213">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="51170-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-215">O tamanho do bloco padrão, em bytes, para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="51170-215">The default block size, in bytes, for the device.</span></span> <span data-ttu-id="51170-216">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="51170-216">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="51170-217">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="51170-217">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-218">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51170-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51170-219">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-220">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="51170-220">A description of the object.</span></span> <span data-ttu-id="51170-221">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="51170-221">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="51170-222">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="51170-222">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-223">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51170-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51170-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-225">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="51170-225">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="51170-226">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="51170-226">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="51170-227">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="51170-227">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="51170-228">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="51170-228">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-229">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51170-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51170-230">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-231">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como "Microsoft:*GUID*- \\ *specific-data*".</span><span class="sxs-lookup"><span data-stu-id="51170-231">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="51170-232">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="51170-232">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-233">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51170-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51170-234">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-235">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="51170-235">A display name for the object.</span></span> <span data-ttu-id="51170-236">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="51170-236">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="51170-237">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="51170-237">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-238">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51170-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51170-239">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-240">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="51170-240">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="51170-241">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="51170-241">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="51170-242">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="51170-242">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-243">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51170-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51170-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-245">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="51170-245">The enabled and disabled states of an element.</span></span> <span data-ttu-id="51170-246">Ele também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="51170-246">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="51170-247">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 5 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="51170-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="51170-248">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="51170-248">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-249">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="51170-249">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51170-250">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-251">Indica se o erro relatado em **LastErrorCode** agora está limpo.</span><span class="sxs-lookup"><span data-stu-id="51170-251">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="51170-252">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="51170-252">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51170-253">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="51170-253">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-254">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51170-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51170-255">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-256">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="51170-256">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="51170-257">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="51170-257">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51170-258">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="51170-258">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-259">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51170-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51170-260">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-261">Uma cadeia de caracteres que descreve os tipos de detecção de erros e correção com suporte neste dispositivo.</span><span class="sxs-lookup"><span data-stu-id="51170-261">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="51170-262">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="51170-262">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="51170-263">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="51170-263">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-264">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51170-264">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51170-265">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-266">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="51170-266">The current health of the element.</span></span> <span data-ttu-id="51170-267">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="51170-267">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="51170-268">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="51170-268">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="51170-269">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5.</span><span class="sxs-lookup"><span data-stu-id="51170-269">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="51170-270">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="51170-270">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-271">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51170-271">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="51170-272">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-273">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz de propriedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="51170-273">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="51170-274">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="51170-274">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="51170-275">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="51170-275">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-276">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="51170-276">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="51170-277">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-278">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="51170-278">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="51170-279">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="51170-279">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="51170-280">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="51170-280">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-281">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51170-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51170-282">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51170-283">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="51170-283">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="51170-284">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="51170-284">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="51170-285">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="51170-285">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="51170-286">**LastCleaned**</span><span class="sxs-lookup"><span data-stu-id="51170-286">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-287">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="51170-287">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="51170-288">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-289">A data e a hora em que o dispositivo foi limpo pela última vez.</span><span class="sxs-lookup"><span data-stu-id="51170-289">The date and time on which the device was last cleaned.</span></span> <span data-ttu-id="51170-290">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="51170-290">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="51170-291">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="51170-291">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-292">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51170-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51170-293">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-294">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="51170-294">The last error code reported by the logical device.</span></span> <span data-ttu-id="51170-295">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="51170-295">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51170-296">**Loadtime**</span><span class="sxs-lookup"><span data-stu-id="51170-296">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-297">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="51170-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="51170-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-299">O tempo, em milissegundos, do carregamento para poder ler ou gravar uma mídia.</span><span class="sxs-lookup"><span data-stu-id="51170-299">The time, in milliseconds, from load to being able to read or write a media.</span></span> <span data-ttu-id="51170-300">Por exemplo, para unidades de disco, esse é o intervalo entre um disco que não está girando para o disco que está pronto para leitura/gravação (ou seja, o disco girando em velocidades nominais).</span><span class="sxs-lookup"><span data-stu-id="51170-300">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write (that is, the disk spinning at nominal speeds).</span></span> <span data-ttu-id="51170-301">Para unidades de fita, esse é o tempo de uma mídia que está sendo injetada para relatar que está pronta para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="51170-301">For tape drives, this is the time from a media being injected to reporting that it is ready for an application.</span></span> <span data-ttu-id="51170-302">Isso geralmente ocorre na área de BOT da fita.</span><span class="sxs-lookup"><span data-stu-id="51170-302">This is usually at the tape's BOT area.</span></span> <span data-ttu-id="51170-303">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="51170-303">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="51170-304">**MaxAccessTime**</span><span class="sxs-lookup"><span data-stu-id="51170-304">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-305">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="51170-305">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="51170-306">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-307">O tempo, em milissegundos, a ser movido do primeiro local na mídia para o local mais distante em relação ao tempo.</span><span class="sxs-lookup"><span data-stu-id="51170-307">The time, in milliseconds, to move from the first location on the media to the location that is furthest with respect to time.</span></span> <span data-ttu-id="51170-308">Para uma unidade de disco, isso representa a busca completa + atraso de rotação completo.</span><span class="sxs-lookup"><span data-stu-id="51170-308">For a disk drive, this represents full seek + full rotational delay.</span></span> <span data-ttu-id="51170-309">Para unidades de fita, isso representa uma pesquisa desde o início da fita até o ponto distante fisicamente.</span><span class="sxs-lookup"><span data-stu-id="51170-309">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span> <span data-ttu-id="51170-310">(O fim de uma fita pode estar em seu ponto mais distante fisicamente, mas isso não é necessariamente verdadeiro.) Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="51170-310">(The end of a tape may be at its most physically distant point, but this is not necessarily true.) This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="51170-311">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="51170-311">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-312">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="51170-312">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="51170-313">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-314">O tamanho máximo do bloco, em bytes, para a mídia acessada pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="51170-314">The maximum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="51170-315">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="51170-315">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="51170-316">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="51170-316">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-317">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="51170-317">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="51170-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-319">O tamanho máximo, em kilobytes, da mídia com suporte neste dispositivo.</span><span class="sxs-lookup"><span data-stu-id="51170-319">The maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="51170-320">Kilobytes são interpretados como o número de bytes multiplicado por 1000 (não o número de bytes multiplicado por 1024).</span><span class="sxs-lookup"><span data-stu-id="51170-320">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span> <span data-ttu-id="51170-321">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="51170-321">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="51170-322">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="51170-322">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-323">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="51170-323">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="51170-324">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-325">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="51170-325">This property has been deprecated.</span></span> <span data-ttu-id="51170-326">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="51170-326">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51170-327">**MaxUnitsBeforeCleaning**</span><span class="sxs-lookup"><span data-stu-id="51170-327">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-328">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="51170-328">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="51170-329">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-330">As unidades máximas que podem ser usadas antes de o dispositivo ser limpo.</span><span class="sxs-lookup"><span data-stu-id="51170-330">The maximum units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="51170-331">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="51170-331">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="51170-332">**MediaIsLocked**</span><span class="sxs-lookup"><span data-stu-id="51170-332">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-333">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="51170-333">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51170-334">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-335">**True** se a mídia estiver bloqueada no dispositivo e não puder ser ejetada; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="51170-335">**True** if the media is locked in the device and cannot be ejected; otherwise, **False**.</span></span> <span data-ttu-id="51170-336">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="51170-336">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="51170-337">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="51170-337">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-338">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="51170-338">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="51170-339">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-340">O tamanho mínimo do bloco, em bytes, para a mídia acessada pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="51170-340">The minimum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="51170-341">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="51170-341">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="51170-342">**MountCount**</span><span class="sxs-lookup"><span data-stu-id="51170-342">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-343">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="51170-343">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="51170-344">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-345">Para um dispositivo que oferece suporte a mídia removível, o número de vezes que a mídia foi montada para transferência de dados ou para limpar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="51170-345">For a device that supports removable media, the number of times that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="51170-346">Para dispositivos que acessam mídia nonremovable, como discos rígidos, essa propriedade não é aplicável e deve ser definida como 0.</span><span class="sxs-lookup"><span data-stu-id="51170-346">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="51170-347">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="51170-347">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="51170-348">**Nome**</span><span class="sxs-lookup"><span data-stu-id="51170-348">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-349">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51170-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51170-350">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-351">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="51170-351">The label by which the object is known.</span></span> <span data-ttu-id="51170-352">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é a mesma que a propriedade **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="51170-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="51170-353">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="51170-353">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-354">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="51170-354">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51170-355">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-356">**True** se o dispositivo de acesso à mídia precisar de limpeza; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="51170-356">**True** if the media access device needs cleaning; otherwise, **False**.</span></span> <span data-ttu-id="51170-357">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="51170-357">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="51170-358">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="51170-358">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-359">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51170-359">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51170-360">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-361">O número máximo de várias mídias individuais que podem ser suportadas ou inseridas.</span><span class="sxs-lookup"><span data-stu-id="51170-361">The maximum number of multiple individual media that can be supported or inserted.</span></span> <span data-ttu-id="51170-362">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="51170-362">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="51170-363">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="51170-363">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-364">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51170-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51170-365">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-366">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="51170-366">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="51170-367">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="51170-367">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="51170-368">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="51170-368">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="51170-369">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="51170-369">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-370">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51170-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="51170-371">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-372">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="51170-372">The current statuses of the object.</span></span> <span data-ttu-id="51170-373">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="51170-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="51170-374">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="51170-374">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-375">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51170-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51170-376">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-377">O estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="51170-377">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="51170-378">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="51170-378">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="51170-379">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="51170-379">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="51170-380">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="51170-380">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-381">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51170-381">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="51170-382">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-383">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="51170-383">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="51170-384">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="51170-384">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="51170-385">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="51170-385">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-386">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51170-386">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="51170-387">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-388">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="51170-388">The power management capabilities of the device.</span></span> <span data-ttu-id="51170-389">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="51170-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51170-390">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="51170-390">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-391">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="51170-391">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51170-392">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-393">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="51170-393">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="51170-394">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="51170-394">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51170-395">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="51170-395">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-396">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="51170-396">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="51170-397">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-398">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="51170-398">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="51170-399">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="51170-399">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51170-400">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="51170-400">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-401">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51170-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51170-402">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-403">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="51170-403">Provides high level status information.</span></span> <span data-ttu-id="51170-404">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer informações de status de integridade detalhadas e de alto nível para o elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="51170-404">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="51170-405">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="51170-405">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="51170-406">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="51170-406">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="51170-407">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="51170-407">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-408">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51170-408">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51170-409">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-410">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="51170-410">The last requested or desired state for the element.</span></span> <span data-ttu-id="51170-411">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="51170-411">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="51170-412">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="51170-412">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="51170-413">Uma determinada instância do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) pode não dar suporte A **RequestStateChange**.</span><span class="sxs-lookup"><span data-stu-id="51170-413">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="51170-414">Se isso ocorrer, o valor 12 (não aplicável) será usado.</span><span class="sxs-lookup"><span data-stu-id="51170-414">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="51170-415">Essa propriedade é herdada do **CIM \_ EnabledLogicalElement** e é sempre definida como 12 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="51170-415">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="51170-416">**Segurança**</span><span class="sxs-lookup"><span data-stu-id="51170-416">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-417">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51170-417">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51170-418">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-419">A segurança operacional definida para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="51170-419">The operational security defined for the device.</span></span> <span data-ttu-id="51170-420">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="51170-420">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>



| <span data-ttu-id="51170-421">Valor</span><span class="sxs-lookup"><span data-stu-id="51170-421">Value</span></span>                                                                        | <span data-ttu-id="51170-422">Significado</span><span class="sxs-lookup"><span data-stu-id="51170-422">Meaning</span></span>         |
|------------------------------------------------------------------------------|-----------------|
| <dl> <span data-ttu-id="51170-423"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="51170-423"><dt>3</dt></span></span> </dl> | <span data-ttu-id="51170-424">Nenhum</span><span class="sxs-lookup"><span data-stu-id="51170-424">None</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="51170-425">**Status**</span><span class="sxs-lookup"><span data-stu-id="51170-425">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-426">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51170-426">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51170-427">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-427">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-428">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="51170-428">The current status of the object.</span></span> <span data-ttu-id="51170-429">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="51170-429">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51170-430">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="51170-430">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-431">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51170-431">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="51170-432">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-433">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="51170-433">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="51170-434">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como "OK".</span><span class="sxs-lookup"><span data-stu-id="51170-434">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="51170-435">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="51170-435">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-436">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51170-436">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51170-437">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-438">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="51170-438">The current state of the logical device.</span></span> <span data-ttu-id="51170-439">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="51170-439">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51170-440">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="51170-440">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-441">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51170-441">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51170-442">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-443">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="51170-443">The scoping system's creation class name.</span></span> <span data-ttu-id="51170-444">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="51170-444">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="51170-445">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="51170-445">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-446">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51170-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51170-447">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-448">O identificador exclusivo para a máquina virtual de escopo.</span><span class="sxs-lookup"><span data-stu-id="51170-448">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="51170-449">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="51170-449">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="51170-450">**TimeOfLastMount**</span><span class="sxs-lookup"><span data-stu-id="51170-450">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-451">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="51170-451">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="51170-452">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-453">Para um dispositivo que oferece suporte a mídia removível, a data e a hora mais recentes em que a mídia foi montada no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="51170-453">For a device that supports removable media, the most recent date and time that media was mounted on the device.</span></span> <span data-ttu-id="51170-454">Para dispositivos que acessam mídia nonremovable, como discos rígidos, essa propriedade não tem significado e não é aplicável.</span><span class="sxs-lookup"><span data-stu-id="51170-454">For devices accessing nonremovable media, such as hard disks, this property has no meaning and is not applicable.</span></span> <span data-ttu-id="51170-455">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="51170-455">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="51170-456">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="51170-456">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-457">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="51170-457">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="51170-458">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-459">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="51170-459">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="51170-460">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="51170-460">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="51170-461">**TotalMountTime**</span><span class="sxs-lookup"><span data-stu-id="51170-461">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-462">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="51170-462">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="51170-463">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-463">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-464">Para um dispositivo que dá suporte à mídia removível, o tempo total (em segundos) que a mídia foi montada para transferência de dados ou para limpar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="51170-464">For a device that supports removable media, the total time (in seconds) that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="51170-465">Para dispositivos que acessam mídia nonremovable, como discos rígidos, essa propriedade não é aplicável e deve ser definida como 0.</span><span class="sxs-lookup"><span data-stu-id="51170-465">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="51170-466">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="51170-466">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="51170-467">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="51170-467">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-468">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="51170-468">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="51170-469">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-470">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="51170-470">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="51170-471">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="51170-471">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51170-472">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="51170-472">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-473">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51170-473">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51170-474">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-474">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-475">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="51170-475">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="51170-476">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="51170-476">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51170-477">**UncompressedDataRate**</span><span class="sxs-lookup"><span data-stu-id="51170-477">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-478">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51170-478">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51170-479">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-480">A taxa de transferência de dados sustentada, em KB/s, que o dispositivo pode ler e gravar em uma mídia.</span><span class="sxs-lookup"><span data-stu-id="51170-480">The sustained data transfer rate, in KB/sec, that the device can read from and write to a media.</span></span> <span data-ttu-id="51170-481">Essa é uma taxa de dados bruta e prolongada.</span><span class="sxs-lookup"><span data-stu-id="51170-481">This is a sustained, raw data rate.</span></span> <span data-ttu-id="51170-482">Taxas ou taxas máximas supondo que a compactação não deve ser relatada nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="51170-482">Maximum rates or rates assuming compression should not be reported in this property.</span></span> <span data-ttu-id="51170-483">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="51170-483">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="51170-484">**UnitsDescription**</span><span class="sxs-lookup"><span data-stu-id="51170-484">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-485">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51170-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51170-486">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-487">As unidades relativas ao seu uso em **MaxUnitsBeforeCleaning**.</span><span class="sxs-lookup"><span data-stu-id="51170-487">The units relative to its use in **MaxUnitsBeforeCleaning**.</span></span> <span data-ttu-id="51170-488">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="51170-488">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="51170-489">**UnitsUsed**</span><span class="sxs-lookup"><span data-stu-id="51170-489">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-490">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="51170-490">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="51170-491">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-491">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-492">O número atual de unidades usadas.</span><span class="sxs-lookup"><span data-stu-id="51170-492">The current number of units used.</span></span> <span data-ttu-id="51170-493">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="51170-493">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="51170-494">**Descarregar**</span><span class="sxs-lookup"><span data-stu-id="51170-494">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51170-495">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="51170-495">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="51170-496">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51170-496">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51170-497">O tempo, em milissegundos, de ser capaz de ler ou gravar uma mídia em seu ' Unload '.</span><span class="sxs-lookup"><span data-stu-id="51170-497">The time, in milliseconds, from being able to read or write a media to its 'unload'.</span></span> <span data-ttu-id="51170-498">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="51170-498">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51170-499">Comentários</span><span class="sxs-lookup"><span data-stu-id="51170-499">Remarks</span></span>

<span data-ttu-id="51170-500">O acesso à classe **Msvm \_ DisketteDrive** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="51170-500">Access to the **Msvm\_DisketteDrive** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="51170-501">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="51170-501">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="51170-502">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51170-502">Requirements</span></span>



| <span data-ttu-id="51170-503">Requisito</span><span class="sxs-lookup"><span data-stu-id="51170-503">Requirement</span></span> | <span data-ttu-id="51170-504">Valor</span><span class="sxs-lookup"><span data-stu-id="51170-504">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51170-505">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51170-505">Minimum supported client</span></span><br/> | <span data-ttu-id="51170-506">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="51170-506">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="51170-507">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51170-507">Minimum supported server</span></span><br/> | <span data-ttu-id="51170-508">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="51170-508">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="51170-509">Namespace</span><span class="sxs-lookup"><span data-stu-id="51170-509">Namespace</span></span><br/>                | <span data-ttu-id="51170-510">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="51170-510">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="51170-511">MOF</span><span class="sxs-lookup"><span data-stu-id="51170-511">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51170-512"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="51170-512"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="51170-513">DLL</span><span class="sxs-lookup"><span data-stu-id="51170-513">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51170-514"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="51170-514"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="51170-515">Confira também</span><span class="sxs-lookup"><span data-stu-id="51170-515">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51170-516">**\_DISKETTEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="51170-516">**CIM\_DisketteDrive**</span></span>](cim-diskettedrive.md)
</dt> <dt>

[<span data-ttu-id="51170-517">**\_DISKETTEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="51170-517">**CIM\_DisketteDrive**</span></span>](/windows/desktop/CIMWin32Prov/cim-diskettedrive)
</dt> <dt>

[<span data-ttu-id="51170-518">Classes de armazenamento</span><span class="sxs-lookup"><span data-stu-id="51170-518">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

