---
description: Representa uma unidade de DVD dentro de uma máquina virtual.
ms.assetid: BA813950-436F-46F1-8C1F-79C5AB1A459B
title: Classe Msvm_DVDDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DVDDrive
- Msvm_DVDDrive.SetPowerState
- Msvm_DVDDrive.EnableDevice
- Msvm_DVDDrive.OnlineDevice
- Msvm_DVDDrive.QuiesceDevice
- Msvm_DVDDrive.SaveProperties
- Msvm_DVDDrive.RestoreProperties
- Msvm_DVDDrive.InstanceID
- Msvm_DVDDrive.Caption
- Msvm_DVDDrive.Description
- Msvm_DVDDrive.ElementName
- Msvm_DVDDrive.InstallDate
- Msvm_DVDDrive.Name
- Msvm_DVDDrive.OperationalStatus
- Msvm_DVDDrive.StatusDescriptions
- Msvm_DVDDrive.Status
- Msvm_DVDDrive.HealthState
- Msvm_DVDDrive.CommunicationStatus
- Msvm_DVDDrive.DetailedStatus
- Msvm_DVDDrive.OperatingStatus
- Msvm_DVDDrive.PrimaryStatus
- Msvm_DVDDrive.EnabledState
- Msvm_DVDDrive.OtherEnabledState
- Msvm_DVDDrive.RequestedState
- Msvm_DVDDrive.EnabledDefault
- Msvm_DVDDrive.TimeOfLastStateChange
- Msvm_DVDDrive.AvailableRequestedStates
- Msvm_DVDDrive.TransitioningToState
- Msvm_DVDDrive.SystemCreationClassName
- Msvm_DVDDrive.SystemName
- Msvm_DVDDrive.CreationClassName
- Msvm_DVDDrive.DeviceID
- Msvm_DVDDrive.PowerManagementSupported
- Msvm_DVDDrive.PowerManagementCapabilities
- Msvm_DVDDrive.Availability
- Msvm_DVDDrive.StatusInfo
- Msvm_DVDDrive.LastErrorCode
- Msvm_DVDDrive.ErrorDescription
- Msvm_DVDDrive.ErrorCleared
- Msvm_DVDDrive.OtherIdentifyingInfo
- Msvm_DVDDrive.PowerOnHours
- Msvm_DVDDrive.TotalPowerOnHours
- Msvm_DVDDrive.IdentifyingDescriptions
- Msvm_DVDDrive.AdditionalAvailability
- Msvm_DVDDrive.MaxQuiesceTime
- Msvm_DVDDrive.Capabilities
- Msvm_DVDDrive.CapabilityDescriptions
- Msvm_DVDDrive.ErrorMethodology
- Msvm_DVDDrive.CompressionMethod
- Msvm_DVDDrive.NumberOfMediaSupported
- Msvm_DVDDrive.MaxMediaSize
- Msvm_DVDDrive.DefaultBlockSize
- Msvm_DVDDrive.MaxBlockSize
- Msvm_DVDDrive.MinBlockSize
- Msvm_DVDDrive.NeedsCleaning
- Msvm_DVDDrive.MediaIsLocked
- Msvm_DVDDrive.Security
- Msvm_DVDDrive.LastCleaned
- Msvm_DVDDrive.MaxAccessTime
- Msvm_DVDDrive.UncompressedDataRate
- Msvm_DVDDrive.LoadTime
- Msvm_DVDDrive.UnloadTime
- Msvm_DVDDrive.MountCount
- Msvm_DVDDrive.TimeOfLastMount
- Msvm_DVDDrive.TotalMountTime
- Msvm_DVDDrive.UnitsDescription
- Msvm_DVDDrive.MaxUnitsBeforeCleaning
- Msvm_DVDDrive.UnitsUsed
- Msvm_DVDDrive.FormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e4b3c9006babb2c7e18b6aed6e85cbee47299429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836857"
---
# <a name="msvm_dvddrive-class"></a><span data-ttu-id="569c3-103">\_Classe Msvm DVDDrive</span><span class="sxs-lookup"><span data-stu-id="569c3-103">Msvm\_DVDDrive class</span></span>

<span data-ttu-id="569c3-104">Representa uma unidade de DVD dentro de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="569c3-104">Represents a DVD drive inside of a virtual machine.</span></span> <span data-ttu-id="569c3-105">Essa unidade de DVD pode ser um dispositivo de passagem (se um disco rígido físico tiver sido anexado à máquina virtual) ou sintético e preenchido com mídia de arquivo ISO.</span><span class="sxs-lookup"><span data-stu-id="569c3-105">This DVD drive can either be a pass-through device (if a physical hard disk was attached to the virtual machine) or synthetic and populated with ISO file media.</span></span> <span data-ttu-id="569c3-106">Como as unidades de DVD virtuais e físicas podem ser adicionadas e removidas da máquina virtual, há dois pools de recursos associados a essa classe, um para unidades de DVD de passagem e o outro para unidades de DVD virtuais.</span><span class="sxs-lookup"><span data-stu-id="569c3-106">Because virtual and physical DVD drives can be added and removed from the virtual machine, there are two resource pools associated with this class, one for pass-through DVD drives, and the other for virtual DVD drives.</span></span> <span data-ttu-id="569c3-107">As unidades de DVD só poderão ser adicionadas ou removidas se a máquina virtual estiver offline.</span><span class="sxs-lookup"><span data-stu-id="569c3-107">DVD drives can only be added or removed if the virtual machine is offline.</span></span>

<span data-ttu-id="569c3-108">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="569c3-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="569c3-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="569c3-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DVDDrive : CIM_DVDDrive
{
  string   InstanceID;
  string   Caption = "DVD Drive";
  string   Description = "Microsoft Virtual DVD Drive";
  string   ElementName = "DVD Drive";
  datetime InstallDate;
  string   Name = "DVD Drive";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_DVDDrive";
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
  uint32   Capabilities[] = {3, 7};
  string   CapabilityDescriptions[] = {"Random Access", "Supports Removable Media"};
  string   ErrorMethodology = "None";
  string   CompressionMethod = "Not Compressed";
  uint32   NumberOfMediaSupported = 1;
  uint64   MaxMediaSize = 9400000;
  uint64   DefaultBlockSize = 2048;
  uint64   MaxBlockSize = 2048;
  uint64   MinBlockSize = 2048;
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
  uint64   MaxUnitsBeforeCleaning = 0xffffffffffffffff;
  uint64   UnitsUsed = 0;
  uint16   FormatsSupported[] = {16, 22};
};
```

## <a name="members"></a><span data-ttu-id="569c3-110">Membros</span><span class="sxs-lookup"><span data-stu-id="569c3-110">Members</span></span>

<span data-ttu-id="569c3-111">A classe **Msvm \_ DVDDrive** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="569c3-111">The **Msvm\_DVDDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="569c3-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="569c3-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="569c3-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="569c3-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="569c3-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="569c3-114">Methods</span></span>

<span data-ttu-id="569c3-115">A classe **Msvm \_ DVDDrive** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="569c3-115">The **Msvm\_DVDDrive** class has these methods.</span></span>



| <span data-ttu-id="569c3-116">Método</span><span class="sxs-lookup"><span data-stu-id="569c3-116">Method</span></span>                                                         | <span data-ttu-id="569c3-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="569c3-117">Description</span></span>                              |
|:---------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="569c3-118">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="569c3-118">**EnableDevice**</span></span>                                               | <span data-ttu-id="569c3-119">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="569c3-119">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="569c3-120">**LockMedia**</span><span class="sxs-lookup"><span data-stu-id="569c3-120">**LockMedia**</span></span>](msvm-dvddrive-lockmedia.md)                   | <span data-ttu-id="569c3-121">Bloqueia ou libera a mídia.</span><span class="sxs-lookup"><span data-stu-id="569c3-121">Locks or releases the media.</span></span><br/>  |
| <span data-ttu-id="569c3-122">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="569c3-122">**OnlineDevice**</span></span>                                               | <span data-ttu-id="569c3-123">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="569c3-123">This method is not supported.</span></span><br/> |
| <span data-ttu-id="569c3-124">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="569c3-124">**QuiesceDevice**</span></span>                                              | <span data-ttu-id="569c3-125">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="569c3-125">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="569c3-126">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="569c3-126">**RequestStateChange**</span></span>](msvm-dvddrive-requeststatechange.md) | <span data-ttu-id="569c3-127">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="569c3-127">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="569c3-128">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="569c3-128">**Reset**</span></span>](msvm-dvddrive-reset.md)                           | <span data-ttu-id="569c3-129">Redefine o dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="569c3-129">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="569c3-130">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="569c3-130">**RestoreProperties**</span></span>                                          | <span data-ttu-id="569c3-131">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="569c3-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="569c3-132">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="569c3-132">**SaveProperties**</span></span>                                             | <span data-ttu-id="569c3-133">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="569c3-133">This method is not supported.</span></span><br/> |
| <span data-ttu-id="569c3-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="569c3-134">**SetPowerState**</span></span>                                              | <span data-ttu-id="569c3-135">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="569c3-135">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="569c3-136">Propriedades</span><span class="sxs-lookup"><span data-stu-id="569c3-136">Properties</span></span>

<span data-ttu-id="569c3-137">A classe **Msvm \_ DVDDrive** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="569c3-137">The **Msvm\_DVDDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="569c3-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="569c3-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-139">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="569c3-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="569c3-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-141">Qualquer disponibilidade e status adicionais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="569c3-141">Any additional availability and status of the device.</span></span> <span data-ttu-id="569c3-142">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como 6 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="569c3-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-143">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="569c3-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-144">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="569c3-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-146">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="569c3-146">The primary availability and status of the device.</span></span> <span data-ttu-id="569c3-147">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como 6 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="569c3-147">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-148">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="569c3-148">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-149">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="569c3-149">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="569c3-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-151">Indica os valores possíveis para o parâmetro *requestedstate* do método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="569c3-151">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="569c3-152">Os valores listados serão um subconjunto dos valores contidos na propriedade **RequestedStatesSupported** da instância associada do **CIM \_ EnabledLogicalElementCapabilities**, em que os valores selecionados são uma função do estado atual do objeto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="569c3-152">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="569c3-153">Essa propriedade pode ser não **nula** se uma implementação for capaz de anunciar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="569c3-153">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="569c3-154">Essa propriedade será **nula** se uma implementação não puder determinar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="569c3-154">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="569c3-155">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="569c3-155">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-156">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="569c3-156">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-157">Tipo de dados: matriz **UInt32**</span><span class="sxs-lookup"><span data-stu-id="569c3-157">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="569c3-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-159">Os recursos do dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="569c3-159">The capabilities of the media access device.</span></span> <span data-ttu-id="569c3-160">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)e é definida com os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="569c3-160">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to the following values.</span></span>



| <span data-ttu-id="569c3-161">Valor</span><span class="sxs-lookup"><span data-stu-id="569c3-161">Value</span></span>                                                                             | <span data-ttu-id="569c3-162">Significado</span><span class="sxs-lookup"><span data-stu-id="569c3-162">Meaning</span></span>                                                                                         |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="569c3-163"><dt>{3, 7}</dt></span><span class="sxs-lookup"><span data-stu-id="569c3-163"><dt>{3, 7}</dt></span></span> </dl> |                                                                                                 |
| <dl> <span data-ttu-id="569c3-164"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="569c3-164"><dt>3</dt></span></span> </dl>      | <span data-ttu-id="569c3-165">A entrada correspondente em **CapabilityDescriptions** é "acesso aleatório".</span><span class="sxs-lookup"><span data-stu-id="569c3-165">The corresponding entry in **CapabilityDescriptions** is "Random Access".</span></span><br/>            |
| <dl> <span data-ttu-id="569c3-166"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="569c3-166"><dt>7</dt></span></span> </dl>      | <span data-ttu-id="569c3-167">A entrada correspondente em **CapabilityDescriptions** é "dá suporte à mídia removível".</span><span class="sxs-lookup"><span data-stu-id="569c3-167">The corresponding entry in **CapabilityDescriptions** is "Supports Removable Media".</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="569c3-168">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="569c3-168">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-169">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="569c3-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="569c3-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-171">Uma matriz de cadeias de caracteres de forma livre que fornece explicações detalhadas para acessar recursos do dispositivo indicados na matriz de propriedades **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="569c3-171">An array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="569c3-172">Cada entrada dessa matriz está relacionada à entrada na matriz de propriedades de **recursos** , localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="569c3-172">Each entry of this array is related to the entry in the **Capabilities** property array, located at the same index.</span></span> <span data-ttu-id="569c3-173">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="569c3-173">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-174">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="569c3-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-175">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="569c3-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-177">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="569c3-177">A short description of the object.</span></span> <span data-ttu-id="569c3-178">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="569c3-178">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-179">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="569c3-179">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-180">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="569c3-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-182">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="569c3-182">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="569c3-183">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="569c3-183">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="569c3-184">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="569c3-184">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-185">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="569c3-185">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-186">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="569c3-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-188">Uma cadeia de caracteres que indica o algoritmo ou a ferramenta usada para compactar o arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="569c3-188">A string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="569c3-189">Se o esquema de compactação for desconhecido ou não estiver descrito, use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="569c3-189">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="569c3-190">Se o arquivo lógico estiver compactado, mas o esquema de compactação for desconhecido ou não estiver descrito, use "compactado".</span><span class="sxs-lookup"><span data-stu-id="569c3-190">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="569c3-191">Se o arquivo lógico não estiver compactado, use "não compactado".</span><span class="sxs-lookup"><span data-stu-id="569c3-191">If the logical file is not compressed, use "Not Compressed".</span></span> <span data-ttu-id="569c3-192">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="569c3-192">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

<span data-ttu-id="569c3-193">"Não compactado"</span><span class="sxs-lookup"><span data-stu-id="569c3-193">"Not Compressed"</span></span>

<span data-ttu-id="569c3-194">Conhecidos</span><span class="sxs-lookup"><span data-stu-id="569c3-194">"Unknown"</span></span>

<span data-ttu-id="569c3-195">Compactados</span><span class="sxs-lookup"><span data-stu-id="569c3-195">"Compressed"</span></span>

<span data-ttu-id="569c3-196">"Não compactado"</span><span class="sxs-lookup"><span data-stu-id="569c3-196">"Not Compressed"</span></span>

</dd> <dt>

<span data-ttu-id="569c3-197">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="569c3-197">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-198">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="569c3-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-200">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="569c3-200">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="569c3-201">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="569c3-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-202">**Defaultblockize**</span><span class="sxs-lookup"><span data-stu-id="569c3-202">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-203">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="569c3-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-205">O tamanho do bloco padrão, em bytes, para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="569c3-205">The default block size, in bytes, for the device.</span></span> <span data-ttu-id="569c3-206">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="569c3-206">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-207">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="569c3-207">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-208">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="569c3-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-210">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="569c3-210">A description of the object.</span></span> <span data-ttu-id="569c3-211">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="569c3-211">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-212">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="569c3-212">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-213">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="569c3-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-215">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="569c3-215">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="569c3-216">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="569c3-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="569c3-217">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="569c3-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-218">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="569c3-218">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-219">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="569c3-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-221">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como "Microsoft:*GUID*- \\ *specific-data*".</span><span class="sxs-lookup"><span data-stu-id="569c3-221">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="569c3-222">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="569c3-222">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-223">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="569c3-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-225">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="569c3-225">A display name for the object.</span></span> <span data-ttu-id="569c3-226">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="569c3-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-227">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="569c3-227">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-228">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="569c3-228">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-229">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-230">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="569c3-230">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="569c3-231">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="569c3-231">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-232">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="569c3-232">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-233">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="569c3-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-234">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-235">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="569c3-235">The enabled and disabled states of an element.</span></span> <span data-ttu-id="569c3-236">Ele também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="569c3-236">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="569c3-237">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="569c3-237">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-238">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="569c3-238">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-239">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="569c3-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-240">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-241">Indica se o erro relatado em **LastErrorCode** agora está limpo.</span><span class="sxs-lookup"><span data-stu-id="569c3-241">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="569c3-242">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="569c3-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="569c3-243">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="569c3-243">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-244">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="569c3-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-245">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-246">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="569c3-246">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="569c3-247">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="569c3-247">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="569c3-248">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="569c3-248">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-249">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="569c3-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-250">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-251">Uma cadeia de caracteres que descreve os tipos de detecção de erros e correção com suporte neste dispositivo.</span><span class="sxs-lookup"><span data-stu-id="569c3-251">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="569c3-252">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="569c3-252">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-253">**FormatsSupported**</span><span class="sxs-lookup"><span data-stu-id="569c3-253">**FormatsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-254">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="569c3-254">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="569c3-255">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-256">Os formatos de CD e DVD com suporte neste dispositivo.</span><span class="sxs-lookup"><span data-stu-id="569c3-256">The CD and DVD formats that are supported by this device.</span></span> <span data-ttu-id="569c3-257">Essa propriedade é herdada do [**CIM \_ DVDDrive**](/previous-versions//cc136812(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="569c3-257">This property is inherited from [**CIM\_DVDDrive**](/previous-versions//cc136812(v=vs.85)).</span></span>

<span data-ttu-id="569c3-258">Essa matriz contém os seguintes valores para ISO.</span><span class="sxs-lookup"><span data-stu-id="569c3-258">This array contains the following values for ISO.</span></span>

<dl> <dt>

<span data-ttu-id="569c3-259">{16, 22}</span><span class="sxs-lookup"><span data-stu-id="569c3-259">{16, 22}</span></span>
</dt> <dt>

<span data-ttu-id="569c3-260"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span><span class="sxs-lookup"><span data-stu-id="569c3-260"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span></span>
</dt> <dt>

<span data-ttu-id="569c3-261"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span><span class="sxs-lookup"><span data-stu-id="569c3-261"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span></span>
</dt> </dl>

<span data-ttu-id="569c3-262">Essa matriz contém os seguintes valores para passagem física.</span><span class="sxs-lookup"><span data-stu-id="569c3-262">This array contains the following values for physical pass-through.</span></span>

<dl> <dt>

<span data-ttu-id="569c3-263"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="569c3-263"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="569c3-264"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="569c3-264"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="569c3-265"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span><span class="sxs-lookup"><span data-stu-id="569c3-265"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span></span>
</dt> <dt>

<span data-ttu-id="569c3-266"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span><span class="sxs-lookup"><span data-stu-id="569c3-266"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span></span>
</dt> <dt>

<span data-ttu-id="569c3-267"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)</span><span class="sxs-lookup"><span data-stu-id="569c3-267"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)</span></span>
</dt> <dt>

<span data-ttu-id="569c3-268"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD gravável** (19)</span><span class="sxs-lookup"><span data-stu-id="569c3-268"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD Recordable** (19)</span></span>
</dt> <dt>

<span data-ttu-id="569c3-269"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span><span class="sxs-lookup"><span data-stu-id="569c3-269"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span></span>
</dt> <dt>

<span data-ttu-id="569c3-270"><span id="DVD-RW_"></span><span id="dvd-rw_"></span>**DVD-RW +** (23)</span><span class="sxs-lookup"><span data-stu-id="569c3-270"><span id="DVD-RW_"></span><span id="dvd-rw_"></span>**DVD-RW+** (23)</span></span>
</dt> <dt>

<span data-ttu-id="569c3-271"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span><span class="sxs-lookup"><span data-stu-id="569c3-271"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span></span>
</dt> <dt>

<span data-ttu-id="569c3-272"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span><span class="sxs-lookup"><span data-stu-id="569c3-272"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span></span>
</dt> <dt>

<span data-ttu-id="569c3-273"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-vídeo** (26)</span><span class="sxs-lookup"><span data-stu-id="569c3-273"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-Video** (26)</span></span>
</dt> <dt>

<span data-ttu-id="569c3-274"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**DivX** (27)</span><span class="sxs-lookup"><span data-stu-id="569c3-274"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**Divx** (27)</span></span>
</dt> <dt>

<span data-ttu-id="569c3-275"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span><span class="sxs-lookup"><span data-stu-id="569c3-275"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span></span>
</dt> <dt>

<span data-ttu-id="569c3-276"><span id="CD-DA"></span><span id="cd-da"></span>**CD-da** (34)</span><span class="sxs-lookup"><span data-stu-id="569c3-276"><span id="CD-DA"></span><span id="cd-da"></span>**CD-DA** (34)</span></span>
</dt> <dt>

<span data-ttu-id="569c3-277"><span id="CD_"></span><span id="cd_"></span>**CD +** (35)</span><span class="sxs-lookup"><span data-stu-id="569c3-277"><span id="CD_"></span><span id="cd_"></span>**CD+** (35)</span></span>
</dt> <dt>

<span data-ttu-id="569c3-278"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD gravável** (36)</span><span class="sxs-lookup"><span data-stu-id="569c3-278"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD Recordable** (36)</span></span>
</dt> <dt>

<span data-ttu-id="569c3-279"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span><span class="sxs-lookup"><span data-stu-id="569c3-279"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span></span>
</dt> <dt>

<span data-ttu-id="569c3-280"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-áudio** (38)</span><span class="sxs-lookup"><span data-stu-id="569c3-280"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-Audio** (38)</span></span>
</dt> <dt>

<span data-ttu-id="569c3-281"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span><span class="sxs-lookup"><span data-stu-id="569c3-281"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span></span>
</dt> <dt>

<span data-ttu-id="569c3-282"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span><span class="sxs-lookup"><span data-stu-id="569c3-282"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span></span>
</dt> <dt>

<span data-ttu-id="569c3-283"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span><span class="sxs-lookup"><span data-stu-id="569c3-283"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span></span>
</dt> <dt>

<span data-ttu-id="569c3-284"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span><span class="sxs-lookup"><span data-stu-id="569c3-284"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="569c3-285">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="569c3-285">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-286">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="569c3-286">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-287">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-288">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="569c3-288">The current health of the element.</span></span> <span data-ttu-id="569c3-289">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="569c3-289">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="569c3-290">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="569c3-290">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="569c3-291">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="569c3-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-292">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="569c3-292">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-293">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="569c3-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="569c3-294">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-295">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz de propriedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="569c3-295">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="569c3-296">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="569c3-296">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="569c3-297">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="569c3-297">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-298">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="569c3-298">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-299">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-300">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="569c3-300">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="569c3-301">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="569c3-301">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-302">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="569c3-302">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-303">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="569c3-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="569c3-305">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="569c3-305">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="569c3-306">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="569c3-306">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="569c3-307">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="569c3-307">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-308">**LastCleaned**</span><span class="sxs-lookup"><span data-stu-id="569c3-308">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-309">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="569c3-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-310">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-311">A data e a hora em que o dispositivo foi limpo pela última vez.</span><span class="sxs-lookup"><span data-stu-id="569c3-311">The date and time on which the device was last cleaned.</span></span> <span data-ttu-id="569c3-312">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="569c3-312">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-313">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="569c3-313">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-314">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="569c3-314">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-315">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-316">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="569c3-316">The last error code reported by the logical device.</span></span> <span data-ttu-id="569c3-317">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="569c3-317">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="569c3-318">**Loadtime**</span><span class="sxs-lookup"><span data-stu-id="569c3-318">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-319">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="569c3-319">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-320">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-321">O tempo, em milissegundos, de ' carregar ' para poder ler ou gravar uma mídia.</span><span class="sxs-lookup"><span data-stu-id="569c3-321">The time, in milliseconds, from 'load' to being able to read or write a media.</span></span> <span data-ttu-id="569c3-322">Por exemplo, para unidades de disco, esse é o intervalo entre um disco que não está girando para o disco que está pronto para leitura/gravação (ou seja, o disco girando em velocidades nominais).</span><span class="sxs-lookup"><span data-stu-id="569c3-322">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write (that is, the disk spinning at nominal speeds).</span></span> <span data-ttu-id="569c3-323">Para unidades de fita, esse é o tempo de uma mídia que está sendo injetada para relatar que está pronta para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="569c3-323">For tape drives, this is the time from a media being injected to reporting that it is ready for an application.</span></span> <span data-ttu-id="569c3-324">Isso geralmente ocorre na área de BOT da fita.</span><span class="sxs-lookup"><span data-stu-id="569c3-324">This is usually at the tape's BOT area.</span></span> <span data-ttu-id="569c3-325">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="569c3-325">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-326">**MaxAccessTime**</span><span class="sxs-lookup"><span data-stu-id="569c3-326">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-327">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="569c3-327">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-329">O tempo, em milissegundos, a ser movido do primeiro local na mídia para o local mais distante em relação ao tempo.</span><span class="sxs-lookup"><span data-stu-id="569c3-329">The time, in milliseconds, to move from the first location on the media to the location that is furthest with respect to time.</span></span> <span data-ttu-id="569c3-330">Para uma unidade de disco, isso representa a busca completa + atraso de rotação completo.</span><span class="sxs-lookup"><span data-stu-id="569c3-330">For a disk drive, this represents full seek + full rotational delay.</span></span> <span data-ttu-id="569c3-331">Para unidades de fita, isso representa uma pesquisa desde o início da fita até o ponto distante fisicamente.</span><span class="sxs-lookup"><span data-stu-id="569c3-331">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span> <span data-ttu-id="569c3-332">(O fim de uma fita pode estar em seu ponto mais distante fisicamente, mas isso não é necessariamente verdadeiro.) Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="569c3-332">(The end of a tape may be at its most physically distant point, but this is not necessarily true.) This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-333">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="569c3-333">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-334">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="569c3-334">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-335">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-336">O tamanho máximo do bloco, em bytes, para a mídia acessada pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="569c3-336">The maximum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="569c3-337">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="569c3-337">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-338">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="569c3-338">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-339">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="569c3-339">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-340">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-341">O tamanho máximo, em kilobytes, da mídia com suporte neste dispositivo.</span><span class="sxs-lookup"><span data-stu-id="569c3-341">The maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="569c3-342">Kilobytes são interpretados como o número de bytes multiplicado por 1000 (não o número de bytes multiplicado por 1024).</span><span class="sxs-lookup"><span data-stu-id="569c3-342">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span> <span data-ttu-id="569c3-343">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="569c3-343">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-344">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="569c3-344">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-345">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="569c3-345">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-346">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-347">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="569c3-347">This property has been deprecated.</span></span> <span data-ttu-id="569c3-348">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="569c3-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="569c3-349">**MaxUnitsBeforeCleaning**</span><span class="sxs-lookup"><span data-stu-id="569c3-349">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-350">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="569c3-350">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-351">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-352">As unidades máximas que podem ser usadas antes de o dispositivo ser limpo.</span><span class="sxs-lookup"><span data-stu-id="569c3-352">The maximum units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="569c3-353">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="569c3-353">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-354">**MediaIsLocked**</span><span class="sxs-lookup"><span data-stu-id="569c3-354">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-355">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="569c3-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-356">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-357">**True** se a mídia estiver bloqueada no dispositivo e não puder ser ejetada; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="569c3-357">**True** if the media is locked in the device and cannot be ejected; otherwise, **False**.</span></span> <span data-ttu-id="569c3-358">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="569c3-358">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-359">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="569c3-359">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-360">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="569c3-360">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-362">O tamanho mínimo do bloco, em bytes, para a mídia acessada pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="569c3-362">The minimum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="569c3-363">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="569c3-363">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-364">**MountCount**</span><span class="sxs-lookup"><span data-stu-id="569c3-364">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-365">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="569c3-365">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-366">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-367">Para um dispositivo que oferece suporte a mídia removível, o número de vezes que a mídia foi montada para transferência de dados ou para limpar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="569c3-367">For a device that supports removable media, the number of times that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="569c3-368">Para dispositivos que acessam mídia nonremovable, como discos rígidos, essa propriedade não é aplicável e deve ser definida como 0.</span><span class="sxs-lookup"><span data-stu-id="569c3-368">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="569c3-369">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="569c3-369">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-370">**Nome**</span><span class="sxs-lookup"><span data-stu-id="569c3-370">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-371">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="569c3-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-372">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-373">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="569c3-373">The label by which the object is known.</span></span> <span data-ttu-id="569c3-374">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é a mesma que a propriedade **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="569c3-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="569c3-375">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="569c3-375">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-376">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="569c3-376">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-377">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-378">**True** se o dispositivo de acesso à mídia precisar de limpeza; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="569c3-378">**True** if the media access device needs cleaning; otherwise, **False**.</span></span> <span data-ttu-id="569c3-379">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="569c3-379">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-380">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="569c3-380">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-381">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="569c3-381">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-382">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-383">O número máximo de várias mídias individuais que podem ser suportadas ou inseridas.</span><span class="sxs-lookup"><span data-stu-id="569c3-383">The maximum number of multiple individual media that can be supported or inserted.</span></span> <span data-ttu-id="569c3-384">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="569c3-384">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-385">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="569c3-385">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-386">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="569c3-386">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-387">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-388">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="569c3-388">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="569c3-389">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="569c3-389">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="569c3-390">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="569c3-390">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-391">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="569c3-391">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-392">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="569c3-392">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="569c3-393">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-394">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="569c3-394">The current statuses of the object.</span></span> <span data-ttu-id="569c3-395">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="569c3-395">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-396">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="569c3-396">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-397">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="569c3-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-398">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-399">O estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="569c3-399">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="569c3-400">Essa propriedade deve ser definida como **NULL** quando a propriedade **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="569c3-400">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="569c3-401">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="569c3-401">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-402">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="569c3-402">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-403">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="569c3-403">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="569c3-404">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-405">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="569c3-405">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="569c3-406">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="569c3-406">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="569c3-407">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="569c3-407">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-408">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="569c3-408">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="569c3-409">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-410">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="569c3-410">The power management capabilities of the device.</span></span> <span data-ttu-id="569c3-411">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="569c3-411">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="569c3-412">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="569c3-412">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-413">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="569c3-413">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-414">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-415">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="569c3-415">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="569c3-416">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="569c3-416">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="569c3-417">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="569c3-417">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-418">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="569c3-418">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-419">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-420">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="569c3-420">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="569c3-421">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="569c3-421">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="569c3-422">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="569c3-422">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-423">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="569c3-423">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-424">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-425">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="569c3-425">Provides high level status information.</span></span> <span data-ttu-id="569c3-426">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer informações de status de integridade detalhadas e de alto nível para o elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="569c3-426">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="569c3-427">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="569c3-427">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="569c3-428">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="569c3-428">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-429">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="569c3-429">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-430">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="569c3-430">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-431">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-432">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="569c3-432">The last requested or desired state for the element.</span></span> <span data-ttu-id="569c3-433">O estado real do elemento é representado pela propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="569c3-433">The actual state of the element is represented by the **EnabledState** property.</span></span> <span data-ttu-id="569c3-434">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="569c3-434">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="569c3-435">Uma determinada instância do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) pode não dar suporte ao método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="569c3-435">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="569c3-436">Se isso ocorrer, o valor 12 (não aplicável) será usado.</span><span class="sxs-lookup"><span data-stu-id="569c3-436">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="569c3-437">Essa propriedade é herdada do **CIM \_ EnabledLogicalElement**.</span><span class="sxs-lookup"><span data-stu-id="569c3-437">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="569c3-438">**Segurança**</span><span class="sxs-lookup"><span data-stu-id="569c3-438">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-439">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="569c3-439">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-440">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-441">A segurança operacional definida para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="569c3-441">The operational security defined for the device.</span></span> <span data-ttu-id="569c3-442">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="569c3-442">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-443">**Status**</span><span class="sxs-lookup"><span data-stu-id="569c3-443">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-444">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="569c3-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-445">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-446">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="569c3-446">The current status of the object.</span></span> <span data-ttu-id="569c3-447">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="569c3-447">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="569c3-448">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="569c3-448">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-449">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="569c3-449">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="569c3-450">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-451">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="569c3-451">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="569c3-452">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="569c3-452">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-453">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="569c3-453">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-454">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="569c3-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-455">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-456">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="569c3-456">The current state of the logical device.</span></span> <span data-ttu-id="569c3-457">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="569c3-457">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="569c3-458">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="569c3-458">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-459">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="569c3-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-460">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-461">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="569c3-461">The scoping system's creation class name.</span></span> <span data-ttu-id="569c3-462">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="569c3-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-463">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="569c3-463">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-464">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="569c3-464">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-465">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-466">O identificador exclusivo para a máquina virtual de escopo.</span><span class="sxs-lookup"><span data-stu-id="569c3-466">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="569c3-467">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="569c3-467">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-468">**TimeOfLastMount**</span><span class="sxs-lookup"><span data-stu-id="569c3-468">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-469">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="569c3-469">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-470">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-471">Para um dispositivo que oferece suporte a mídia removível, a data e a hora mais recentes em que a mídia foi montada no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="569c3-471">For a device that supports removable media, the most recent date and time that media was mounted on the device.</span></span> <span data-ttu-id="569c3-472">Para dispositivos que acessam mídia nonremovable, como discos rígidos, essa propriedade não tem significado e não é aplicável.</span><span class="sxs-lookup"><span data-stu-id="569c3-472">For devices accessing nonremovable media, such as hard disks, this property has no meaning and is not applicable.</span></span> <span data-ttu-id="569c3-473">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="569c3-473">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-474">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="569c3-474">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-475">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="569c3-475">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-476">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-477">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="569c3-477">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="569c3-478">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="569c3-478">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="569c3-479">**TotalMountTime**</span><span class="sxs-lookup"><span data-stu-id="569c3-479">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-480">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="569c3-480">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-481">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-482">Para um dispositivo que dá suporte à mídia removível, o tempo total (em segundos) que a mídia foi montada para transferência de dados ou para limpar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="569c3-482">For a device that supports removable media, the total time (in seconds) that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="569c3-483">Para dispositivos que acessam mídia nonremovable, como discos rígidos, essa propriedade não é aplicável e deve ser definida como 0.</span><span class="sxs-lookup"><span data-stu-id="569c3-483">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="569c3-484">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="569c3-484">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-485">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="569c3-485">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-486">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="569c3-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-487">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-488">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="569c3-488">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="569c3-489">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="569c3-489">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="569c3-490">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="569c3-490">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-491">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="569c3-491">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-492">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-492">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-493">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="569c3-493">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="569c3-494">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="569c3-494">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="569c3-495">**UncompressedDataRate**</span><span class="sxs-lookup"><span data-stu-id="569c3-495">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-496">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="569c3-496">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-497">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-497">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-498">A taxa de transferência de dados sustentada, em KB/s, que o dispositivo pode ler e gravar em uma mídia.</span><span class="sxs-lookup"><span data-stu-id="569c3-498">The sustained data transfer rate, in KB/sec, that the device can read from and write to a media.</span></span> <span data-ttu-id="569c3-499">Essa é uma taxa de dados bruta e prolongada.</span><span class="sxs-lookup"><span data-stu-id="569c3-499">This is a sustained, raw data rate.</span></span> <span data-ttu-id="569c3-500">Taxas ou taxas máximas supondo que a compactação não deve ser relatada nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="569c3-500">Maximum rates or rates assuming compression should not be reported in this property.</span></span> <span data-ttu-id="569c3-501">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="569c3-501">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-502">**UnitsDescription**</span><span class="sxs-lookup"><span data-stu-id="569c3-502">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-503">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="569c3-503">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-504">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-505">As unidades relativas ao seu uso em **MaxUnitsBeforeCleaning**.</span><span class="sxs-lookup"><span data-stu-id="569c3-505">The units relative to its use in **MaxUnitsBeforeCleaning**.</span></span> <span data-ttu-id="569c3-506">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="569c3-506">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-507">**UnitsUsed**</span><span class="sxs-lookup"><span data-stu-id="569c3-507">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-508">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="569c3-508">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-509">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-509">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-510">O número atual de unidades usadas.</span><span class="sxs-lookup"><span data-stu-id="569c3-510">The current number of units used.</span></span> <span data-ttu-id="569c3-511">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="569c3-511">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="569c3-512">**Descarregar**</span><span class="sxs-lookup"><span data-stu-id="569c3-512">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="569c3-513">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="569c3-513">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="569c3-514">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="569c3-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="569c3-515">O tempo, em milissegundos, de ser capaz de ler ou gravar uma mídia em seu ' Unload '.</span><span class="sxs-lookup"><span data-stu-id="569c3-515">The time, in milliseconds, from being able to read or write a media to its 'unload'.</span></span> <span data-ttu-id="569c3-516">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="569c3-516">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="569c3-517">Comentários</span><span class="sxs-lookup"><span data-stu-id="569c3-517">Remarks</span></span>

<span data-ttu-id="569c3-518">O acesso à classe **Msvm \_ DVDDrive** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="569c3-518">Access to the **Msvm\_DVDDrive** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="569c3-519">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="569c3-519">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="569c3-520">Requisitos</span><span class="sxs-lookup"><span data-stu-id="569c3-520">Requirements</span></span>



| <span data-ttu-id="569c3-521">Requisito</span><span class="sxs-lookup"><span data-stu-id="569c3-521">Requirement</span></span> | <span data-ttu-id="569c3-522">Valor</span><span class="sxs-lookup"><span data-stu-id="569c3-522">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="569c3-523">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="569c3-523">Minimum supported client</span></span><br/> | <span data-ttu-id="569c3-524">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="569c3-524">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="569c3-525">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="569c3-525">Minimum supported server</span></span><br/> | <span data-ttu-id="569c3-526">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="569c3-526">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="569c3-527">Namespace</span><span class="sxs-lookup"><span data-stu-id="569c3-527">Namespace</span></span><br/>                | <span data-ttu-id="569c3-528">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="569c3-528">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="569c3-529">MOF</span><span class="sxs-lookup"><span data-stu-id="569c3-529">MOF</span></span><br/>                      | <dl> <span data-ttu-id="569c3-530"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="569c3-530"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="569c3-531">DLL</span><span class="sxs-lookup"><span data-stu-id="569c3-531">DLL</span></span><br/>                      | <dl> <span data-ttu-id="569c3-532"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="569c3-532"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="569c3-533">Confira também</span><span class="sxs-lookup"><span data-stu-id="569c3-533">See also</span></span>

<dl> <dt>

[<span data-ttu-id="569c3-534">**\_DVDDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="569c3-534">**CIM\_DVDDrive**</span></span>](cim-dvddrive.md)
</dt> <dt>

<span data-ttu-id="569c3-535">[**\_DVDDRIVE CIM**](/previous-versions//cc136812(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="569c3-535">[**CIM\_DVDDrive**](/previous-versions//cc136812(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="569c3-536">Classes de armazenamento</span><span class="sxs-lookup"><span data-stu-id="569c3-536">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

