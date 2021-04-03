---
description: Representa a memória atualmente alocada para uma máquina virtual.
ms.assetid: 4CAA64FC-5A06-409B-9E92-32DF3F47D5FD
title: Classe Msvm_Memory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Memory
- Msvm_Memory.SetPowerState
- Msvm_Memory.EnableDevice
- Msvm_Memory.OnlineDevice
- Msvm_Memory.QuiesceDevice
- Msvm_Memory.SaveProperties
- Msvm_Memory.RestoreProperties
- Msvm_Memory.InstanceID
- Msvm_Memory.Caption
- Msvm_Memory.Description
- Msvm_Memory.ElementName
- Msvm_Memory.InstallDate
- Msvm_Memory.OperationalStatus
- Msvm_Memory.StatusDescriptions
- Msvm_Memory.Status
- Msvm_Memory.HealthState
- Msvm_Memory.CommunicationStatus
- Msvm_Memory.DetailedStatus
- Msvm_Memory.OperatingStatus
- Msvm_Memory.PrimaryStatus
- Msvm_Memory.EnabledState
- Msvm_Memory.OtherEnabledState
- Msvm_Memory.RequestedState
- Msvm_Memory.EnabledDefault
- Msvm_Memory.TimeOfLastStateChange
- Msvm_Memory.AvailableRequestedStates
- Msvm_Memory.TransitioningToState
- Msvm_Memory.SystemCreationClassName
- Msvm_Memory.SystemName
- Msvm_Memory.CreationClassName
- Msvm_Memory.DeviceID
- Msvm_Memory.PowerManagementSupported
- Msvm_Memory.PowerManagementCapabilities
- Msvm_Memory.Availability
- Msvm_Memory.StatusInfo
- Msvm_Memory.LastErrorCode
- Msvm_Memory.ErrorDescription
- Msvm_Memory.ErrorCleared
- Msvm_Memory.OtherIdentifyingInfo
- Msvm_Memory.PowerOnHours
- Msvm_Memory.TotalPowerOnHours
- Msvm_Memory.IdentifyingDescriptions
- Msvm_Memory.AdditionalAvailability
- Msvm_Memory.MaxQuiesceTime
- Msvm_Memory.DataOrganization
- Msvm_Memory.Purpose
- Msvm_Memory.Access
- Msvm_Memory.BlockSize
- Msvm_Memory.NumberOfBlocks
- Msvm_Memory.ConsumableBlocks
- Msvm_Memory.IsBasedOnUnderlyingRedundancy
- Msvm_Memory.SequentialAccess
- Msvm_Memory.ExtentStatus
- Msvm_Memory.NoSinglePointOfFailure
- Msvm_Memory.DataRedundancy
- Msvm_Memory.PackageRedundancy
- Msvm_Memory.DeltaReservation
- Msvm_Memory.Primordial
- Msvm_Memory.Name
- Msvm_Memory.NameFormat
- Msvm_Memory.NameNamespace
- Msvm_Memory.OtherNameNamespace
- Msvm_Memory.OtherNameFormat
- Msvm_Memory.Volatile
- Msvm_Memory.ErrorMethodology
- Msvm_Memory.StartingAddress
- Msvm_Memory.EndingAddress
- Msvm_Memory.ErrorInfo
- Msvm_Memory.OtherErrorDescription
- Msvm_Memory.CorrectableError
- Msvm_Memory.ErrorTime
- Msvm_Memory.ErrorAccess
- Msvm_Memory.ErrorTransferSize
- Msvm_Memory.ErrorData
- Msvm_Memory.ErrorDataOrder
- Msvm_Memory.ErrorAddress
- Msvm_Memory.SystemLevelAddress
- Msvm_Memory.ErrorResolution
- Msvm_Memory.AdditionalErrorData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ec6b287f3281fd0224e9c2efc39391781bd7f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837135"
---
# <a name="msvm_memory-class"></a><span data-ttu-id="dbb49-103">\_Classe de memória Msvm</span><span class="sxs-lookup"><span data-stu-id="dbb49-103">Msvm\_Memory class</span></span>

<span data-ttu-id="dbb49-104">Representa a memória atualmente alocada para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dbb49-104">Represents the memory currently allocated to a virtual machine.</span></span>

<span data-ttu-id="dbb49-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="dbb49-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbb49-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dbb49-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Memory : CIM_Memory
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
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
  uint16   DataOrganization = 2;
  string   Purpose = "System Memory";
  uint16   Access = 3;
  uint64   BlockSize = 1048576;
  uint64   NumberOfBlocks;
  uint64   ConsumableBlocks;
  boolean  IsBasedOnUnderlyingRedundancy = False;
  boolean  SequentialAccess = False;
  uint16   ExtentStatus[] = 2;
  boolean  NoSinglePointOfFailure = False;
  uint16   DataRedundancy = 1;
  uint16   PackageRedundancy = 0;
  uint8    DeltaReservation = 0;
  boolean  Primordial;
  string   Name = "GUID";
  uint16   NameFormat = 0;
  uint16   NameNamespace = 0;
  string   OtherNameNamespace;
  string   OtherNameFormat;
  boolean  Volatile = True;
  string   ErrorMethodology;
  uint64   StartingAddress = 0;
  uint64   EndingAddress;
  uint16   ErrorInfo;
  string   OtherErrorDescription;
  boolean  CorrectableError;
  datetime ErrorTime;
  uint16   ErrorAccess;
  uint32   ErrorTransferSize;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint64   ErrorAddress;
  boolean  SystemLevelAddress;
  uint64   ErrorResolution;
  uint8    AdditionalErrorData[];
};
```

## <a name="members"></a><span data-ttu-id="dbb49-107">Membros</span><span class="sxs-lookup"><span data-stu-id="dbb49-107">Members</span></span>

<span data-ttu-id="dbb49-108">A classe de **\_ memória Msvm** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="dbb49-108">The **Msvm\_Memory** class has these types of members:</span></span>

-   [<span data-ttu-id="dbb49-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="dbb49-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="dbb49-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dbb49-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dbb49-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="dbb49-111">Methods</span></span>

<span data-ttu-id="dbb49-112">A classe de **\_ memória Msvm** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="dbb49-112">The **Msvm\_Memory** class has these methods.</span></span>



| <span data-ttu-id="dbb49-113">Método</span><span class="sxs-lookup"><span data-stu-id="dbb49-113">Method</span></span>                                                       | <span data-ttu-id="dbb49-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="dbb49-114">Description</span></span>                              |
|:-------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="dbb49-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="dbb49-115">**EnableDevice**</span></span>                                             | <span data-ttu-id="dbb49-116">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="dbb49-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="dbb49-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="dbb49-117">**OnlineDevice**</span></span>                                             | <span data-ttu-id="dbb49-118">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="dbb49-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="dbb49-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="dbb49-119">**QuiesceDevice**</span></span>                                            | <span data-ttu-id="dbb49-120">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="dbb49-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="dbb49-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="dbb49-121">**RequestStateChange**</span></span>](msvm-memory-requeststatechange.md) | <span data-ttu-id="dbb49-122">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="dbb49-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="dbb49-123">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="dbb49-123">**Reset**</span></span>](msvm-memory-reset.md)                           | <span data-ttu-id="dbb49-124">Redefine a memória virtual.</span><span class="sxs-lookup"><span data-stu-id="dbb49-124">Resets the virtual memory.</span></span><br/>    |
| <span data-ttu-id="dbb49-125">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="dbb49-125">**RestoreProperties**</span></span>                                        | <span data-ttu-id="dbb49-126">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="dbb49-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="dbb49-127">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="dbb49-127">**SaveProperties**</span></span>                                           | <span data-ttu-id="dbb49-128">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="dbb49-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="dbb49-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="dbb49-129">**SetPowerState**</span></span>                                            | <span data-ttu-id="dbb49-130">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="dbb49-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="dbb49-131">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dbb49-131">Properties</span></span>

<span data-ttu-id="dbb49-132">A classe de **\_ memória Msvm** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="dbb49-132">The **Msvm\_Memory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dbb49-133">**Acesso**</span><span class="sxs-lookup"><span data-stu-id="dbb49-133">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-134">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-136">Descreve as propriedades de leitura/gravação da mídia.</span><span class="sxs-lookup"><span data-stu-id="dbb49-136">Describes the read/write properties of the media.</span></span> <span data-ttu-id="dbb49-137">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)e é definida como 3 (suporte de leitura/gravação) por padrão.</span><span class="sxs-lookup"><span data-stu-id="dbb49-137">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is set to 3 (Read/Write Supported) by default.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="dbb49-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-139">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-141">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como 6 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="dbb49-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-142">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="dbb49-142">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-143">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="dbb49-143">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-145">Essa propriedade é herdada [**da \_ memória CIM**](/windows/desktop/CIMWin32Prov/cim-memory), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-145">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-146">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="dbb49-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-147">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-149">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="dbb49-149">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-150">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="dbb49-150">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-151">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-151">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-153">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="dbb49-153">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="dbb49-154">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dbb49-154">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-155">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="dbb49-155">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-156">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dbb49-156">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-158">O tamanho, em bytes, dos blocos que formam a extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="dbb49-158">The size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="dbb49-159">Se o tamanho do bloco variável, o tamanho máximo do bloco, em bytes, deverá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="dbb49-159">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="dbb49-160">Se o tamanho do bloco for desconhecido ou se um conceito de bloco não for válido (por exemplo, para extensões de agregação, memória ou discos lógicos), insira um 1 (um).</span><span class="sxs-lookup"><span data-stu-id="dbb49-160">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span> <span data-ttu-id="dbb49-161">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)e é sempre definida como 1048576.</span><span class="sxs-lookup"><span data-stu-id="dbb49-161">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 1048576.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-162">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="dbb49-162">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-163">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbb49-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-165">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="dbb49-165">A short description of the object.</span></span> <span data-ttu-id="dbb49-166">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dbb49-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-167">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="dbb49-167">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-168">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-170">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="dbb49-170">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="dbb49-171">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-171">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dbb49-172">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dbb49-172">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="dbb49-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="dbb49-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-174"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="dbb49-174"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-175"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="dbb49-175"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-176"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="dbb49-176"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-177"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="dbb49-177"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="dbb49-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="dbb49-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="dbb49-180">)</span><span class="sxs-lookup"><span data-stu-id="dbb49-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dbb49-181">**ConsumableBlocks**</span><span class="sxs-lookup"><span data-stu-id="dbb49-181">**ConsumableBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-182">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dbb49-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-184">O número máximo de blocos, de tamanho de **bloco**, que estão disponíveis para consumo ao encamar extensões de armazenamento usando a associação com base em.</span><span class="sxs-lookup"><span data-stu-id="dbb49-184">The maximum number of blocks, of size **BlockSize**, that are available for consumption when layering storage extents using the BasedOn association.</span></span> <span data-ttu-id="dbb49-185">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dbb49-185">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-186">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="dbb49-186">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-187">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="dbb49-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-189">Essa propriedade é herdada [**da \_ memória CIM**](/windows/desktop/CIMWin32Prov/cim-memory), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-189">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-190">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dbb49-190">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-191">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-193">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="dbb49-193">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="dbb49-194">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="dbb49-194">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-195">**Dataorganization**</span><span class="sxs-lookup"><span data-stu-id="dbb49-195">**DataOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-196">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-198">O tipo de organização de dados usado.</span><span class="sxs-lookup"><span data-stu-id="dbb49-198">The type of data organization used.</span></span> <span data-ttu-id="dbb49-199">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)e é sempre definida como 2.</span><span class="sxs-lookup"><span data-stu-id="dbb49-199">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 2.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-200">**Dataredundância**</span><span class="sxs-lookup"><span data-stu-id="dbb49-200">**DataRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-201">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-203">O número de cópias completas dos dados atualmente mantidos.</span><span class="sxs-lookup"><span data-stu-id="dbb49-203">The number of complete copies of data that is currently maintained.</span></span> <span data-ttu-id="dbb49-204">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)e é sempre definida como 1.</span><span class="sxs-lookup"><span data-stu-id="dbb49-204">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-205">**DeltaReservation**</span><span class="sxs-lookup"><span data-stu-id="dbb49-205">**DeltaReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-206">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="dbb49-206">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-208">O valor atual para reserva de deltas.</span><span class="sxs-lookup"><span data-stu-id="dbb49-208">The current value for delta reservation.</span></span> <span data-ttu-id="dbb49-209">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)e é sempre definida como 0.</span><span class="sxs-lookup"><span data-stu-id="dbb49-209">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-210">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="dbb49-210">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-211">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbb49-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-213">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="dbb49-213">A description of the object.</span></span> <span data-ttu-id="dbb49-214">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dbb49-214">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-215">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="dbb49-215">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-216">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-216">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-218">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="dbb49-218">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="dbb49-219">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-219">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dbb49-220">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dbb49-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="dbb49-221"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="dbb49-221"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-222"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="dbb49-222"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-223"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="dbb49-223"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-224"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="dbb49-224"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-225"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="dbb49-225"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-226"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="dbb49-226"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="dbb49-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="dbb49-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="dbb49-229">)</span><span class="sxs-lookup"><span data-stu-id="dbb49-229">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dbb49-230">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="dbb49-230">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-231">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbb49-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-232">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-233">Um endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="dbb49-233">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="dbb49-234">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="dbb49-234">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-235">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="dbb49-235">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-236">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbb49-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-237">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-238">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="dbb49-238">A display name for the object.</span></span> <span data-ttu-id="dbb49-239">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dbb49-239">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-240">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="dbb49-240">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-241">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-242">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-243">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="dbb49-243">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="dbb49-244">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dbb49-244">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-245">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="dbb49-245">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-246">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-247">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-248">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="dbb49-248">The enabled and disabled states of an element.</span></span> <span data-ttu-id="dbb49-249">Ele também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="dbb49-249">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="dbb49-250">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dbb49-250">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="dbb49-251">Valor</span><span class="sxs-lookup"><span data-stu-id="dbb49-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="dbb49-252">Significado</span><span class="sxs-lookup"><span data-stu-id="dbb49-252">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="dbb49-253"><dt></dt> <dt>0</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="dbb49-253"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="dbb49-254">Não foi possível determinar o estado do elemento.</span><span class="sxs-lookup"><span data-stu-id="dbb49-254">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="dbb49-255"><dt>**Outros**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="dbb49-255"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="dbb49-256"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="dbb49-256"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="dbb49-257">O elemento está em execução.</span><span class="sxs-lookup"><span data-stu-id="dbb49-257">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="dbb49-258"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="dbb49-258"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="dbb49-259">O elemento está desativado.</span><span class="sxs-lookup"><span data-stu-id="dbb49-259">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="dbb49-260"><dt>**Desligando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="dbb49-260"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="dbb49-261">O elemento está no processo de ir para um estado desabilitado.</span><span class="sxs-lookup"><span data-stu-id="dbb49-261">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="dbb49-262"><dt>**Não aplicável**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="dbb49-262"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="dbb49-263">O elemento não dá suporte a ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="dbb49-263">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="dbb49-264"><dt>**Habilitado, mas offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="dbb49-264"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="dbb49-265">O elemento pode estar concluindo comandos e removerá todas as novas solicitações.</span><span class="sxs-lookup"><span data-stu-id="dbb49-265">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="dbb49-266"><dt>**No teste**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="dbb49-266"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="dbb49-267">O elemento está em um estado de teste.</span><span class="sxs-lookup"><span data-stu-id="dbb49-267">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="dbb49-268"><dt>**Adiado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="dbb49-268"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="dbb49-269">O elemento pode estar concluindo comandos, mas colocará todas as novas solicitações na fila.</span><span class="sxs-lookup"><span data-stu-id="dbb49-269">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="dbb49-270"><dt>**Desativar**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="dbb49-270"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="dbb49-271">O elemento está habilitado, mas está em um modo restrito.</span><span class="sxs-lookup"><span data-stu-id="dbb49-271">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="dbb49-272">O comportamento do elemento é semelhante ao estado habilitado (2), mas processa apenas um conjunto restrito de comandos.</span><span class="sxs-lookup"><span data-stu-id="dbb49-272">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="dbb49-273">Todas as outras solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="dbb49-273">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="dbb49-274"><dt>**Iniciando**</dt> em <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="dbb49-274"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="dbb49-275">O elemento está no processo de ir para um estado habilitado (2).</span><span class="sxs-lookup"><span data-stu-id="dbb49-275">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="dbb49-276">Novas solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="dbb49-276">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="dbb49-277">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="dbb49-277">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-278">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dbb49-278">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-280">O endereço final do bloco de memória contíguo.</span><span class="sxs-lookup"><span data-stu-id="dbb49-280">The ending address of the contiguous memory block.</span></span> <span data-ttu-id="dbb49-281">Como a propriedade **StartingAddress** é sempre 0, esse valor sempre reflete a quantidade total de memória na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dbb49-281">Since the **StartingAddress** property is always 0, this value always reflects the total amount of memory in the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-282">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="dbb49-282">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-283">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-284">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-285">Essa propriedade é herdada [**da \_ memória CIM**](/windows/desktop/CIMWin32Prov/cim-memory), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-285">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-286">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="dbb49-286">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-287">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dbb49-287">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-288">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-289">Essa propriedade é herdada [**da \_ memória CIM**](/windows/desktop/CIMWin32Prov/cim-memory), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-289">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-290">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="dbb49-290">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-291">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="dbb49-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-292">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-293">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-293">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-294">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="dbb49-294">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-295">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="dbb49-295">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-296">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-297">Essa propriedade é herdada [**da \_ memória CIM**](/windows/desktop/CIMWin32Prov/cim-memory), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-297">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-298">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="dbb49-298">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-299">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-300">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-301">Essa propriedade é herdada [**da \_ memória CIM**](/windows/desktop/CIMWin32Prov/cim-memory), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-301">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="dbb49-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-303">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbb49-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-305">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-305">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-306">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="dbb49-306">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-307">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-307">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-308">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-309">Essa propriedade é herdada [**da \_ memória CIM**](/windows/desktop/CIMWin32Prov/cim-memory), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-309">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-310">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="dbb49-310">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-311">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbb49-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-312">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-313">Uma cadeia de caracteres que descreve o tipo de detecção de erros e correção com suporte nesta extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="dbb49-313">A string that describes the type of error detection and correction supported by this storage extent.</span></span> <span data-ttu-id="dbb49-314">Essa propriedade é herdada [**da \_ memória CIM**](/windows/desktop/CIMWin32Prov/cim-memory)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dbb49-314">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-315">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="dbb49-315">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-316">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dbb49-316">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-317">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-318">Essa propriedade é herdada [**da \_ memória CIM**](/windows/desktop/CIMWin32Prov/cim-memory), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-318">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-319">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="dbb49-319">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-320">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dbb49-320">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-322">Essa propriedade é herdada [**da \_ memória CIM**](/windows/desktop/CIMWin32Prov/cim-memory) , mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-322">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory) but it not used.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-323">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="dbb49-323">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-324">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dbb49-324">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-326">Essa propriedade é herdada [**da \_ memória CIM**](/windows/desktop/CIMWin32Prov/cim-memory), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-326">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-327">**ExtentStatus**</span><span class="sxs-lookup"><span data-stu-id="dbb49-327">**ExtentStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-328">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-328">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-329">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-330">As extensões de armazenamento têm informações de status adicionais além das capturadas no **OperationalStatus** e outras propriedades herdadas do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dbb49-330">Storage extents have additional status information beyond that captured in the **OperationalStatus** and other properties inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="dbb49-331">Essas informações adicionais (por exemplo, "proteção desabilitada", valor = 9) são capturadas na propriedade **VolumeStatus** .</span><span class="sxs-lookup"><span data-stu-id="dbb49-331">This additional information (for example, "Protection Disabled", value=9) is captured in the **VolumeStatus** property.</span></span> <span data-ttu-id="dbb49-332">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)e é sempre definida como 2 (nenhuma/não aplicável).</span><span class="sxs-lookup"><span data-stu-id="dbb49-332">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 2 (None/Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-333">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="dbb49-333">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-334">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-334">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-335">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-336">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="dbb49-336">The current health of the element.</span></span> <span data-ttu-id="dbb49-337">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="dbb49-337">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="dbb49-338">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="dbb49-338">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="dbb49-339">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5.</span><span class="sxs-lookup"><span data-stu-id="dbb49-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-340">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="dbb49-340">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-341">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbb49-341">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-342">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-343">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dbb49-343">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-344">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dbb49-344">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-345">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dbb49-345">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-346">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-347">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-347">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="dbb49-348">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dbb49-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-349">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dbb49-349">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-350">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbb49-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-351">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-352">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="dbb49-352">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-353">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="dbb49-353">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="dbb49-354">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dbb49-354">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-355">**IsBasedOnUnderlyingRedundancy**</span><span class="sxs-lookup"><span data-stu-id="dbb49-355">**IsBasedOnUnderlyingRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-356">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="dbb49-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-357">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-358">**True** se as extensões de armazenamento subjacentes participarem de um grupo de redundância de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="dbb49-358">**True** if the underlying storage extents participate in a Storage Redundancy Group.</span></span> <span data-ttu-id="dbb49-359">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)e é sempre definida como **false**.</span><span class="sxs-lookup"><span data-stu-id="dbb49-359">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-360">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="dbb49-360">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-361">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dbb49-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-362">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-363">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-363">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-364">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="dbb49-364">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-365">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dbb49-365">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-366">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-367">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-367">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-368">**Nome**</span><span class="sxs-lookup"><span data-stu-id="dbb49-368">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-369">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbb49-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-370">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-371">Qualificadores: **maxlen** (1024), **override** ("Name")</span><span class="sxs-lookup"><span data-stu-id="dbb49-371">Qualifiers: **MaxLen** (1024), **Override** ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-372">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="dbb49-372">The label by which the object is known.</span></span> <span data-ttu-id="dbb49-373">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="dbb49-373">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="dbb49-374">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)e é sempre definida como "*GUID*".</span><span class="sxs-lookup"><span data-stu-id="dbb49-374">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to "*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-375">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="dbb49-375">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-376">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-377">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-378">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)e é sempre definida como 0.</span><span class="sxs-lookup"><span data-stu-id="dbb49-378">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-379">**NameNamespace**</span><span class="sxs-lookup"><span data-stu-id="dbb49-379">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-380">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-380">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-381">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-382">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)e é sempre definida como 0.</span><span class="sxs-lookup"><span data-stu-id="dbb49-382">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-383">**NoSinglePointOfFailure**</span><span class="sxs-lookup"><span data-stu-id="dbb49-383">**NoSinglePointOfFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-384">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="dbb49-384">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-385">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-386">**True** se não existir nenhum ponto único de falha.</span><span class="sxs-lookup"><span data-stu-id="dbb49-386">**True** if there exists no single point of failure.</span></span> <span data-ttu-id="dbb49-387">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)e é sempre definida como **false**.</span><span class="sxs-lookup"><span data-stu-id="dbb49-387">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-388">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="dbb49-388">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-389">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dbb49-389">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-390">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-391">Um valor calculado que representa a quantidade total de memória dividida pelo **BlockSize**.</span><span class="sxs-lookup"><span data-stu-id="dbb49-391">A calculated value that represents the total amount of memory divided by the **BlockSize**.</span></span> <span data-ttu-id="dbb49-392">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="dbb49-392">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-393">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="dbb49-393">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-394">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-394">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-395">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-396">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="dbb49-396">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="dbb49-397">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-397">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dbb49-398">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dbb49-398">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="dbb49-399"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="dbb49-399"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-400"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="dbb49-400"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-401"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="dbb49-401"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-402"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="dbb49-402"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-403"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="dbb49-403"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-404"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="dbb49-404"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-405"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="dbb49-405"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-406"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="dbb49-406"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-407"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="dbb49-407"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-408"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="dbb49-408"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-409"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="dbb49-409"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-410"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="dbb49-410"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-411"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="dbb49-411"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-412"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="dbb49-412"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-413"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="dbb49-413"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-414"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="dbb49-414"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-415"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="dbb49-415"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="dbb49-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="dbb49-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="dbb49-418">)</span><span class="sxs-lookup"><span data-stu-id="dbb49-418">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dbb49-419">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="dbb49-419">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-420">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-420">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-421">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-422">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="dbb49-422">The current statuses of the object.</span></span> <span data-ttu-id="dbb49-423">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dbb49-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-424">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="dbb49-424">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-425">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbb49-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-426">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-427">O estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="dbb49-427">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="dbb49-428">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="dbb49-428">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="dbb49-429">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dbb49-429">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-430">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="dbb49-430">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-431">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbb49-431">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-432">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-433">Essa propriedade é herdada [**da \_ memória CIM**](/windows/desktop/CIMWin32Prov/cim-memory), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-433">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-434">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="dbb49-434">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-435">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbb49-435">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-436">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-437">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dbb49-437">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-438">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="dbb49-438">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-439">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbb49-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-440">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-441">O namespace da propriedade **Name** quando a propriedade **NameFormat** inclui o valor 1 (other ").</span><span class="sxs-lookup"><span data-stu-id="dbb49-441">The namespace of the **Name** property when the **NameFormat** property includes the value 1 (Other").</span></span> <span data-ttu-id="dbb49-442">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dbb49-442">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-443">**OtherNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="dbb49-443">**OtherNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-444">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbb49-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-445">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-446">O namespace da propriedade **Name** quando a propriedade **NameNamespace** inclui o valor 1 (Other).</span><span class="sxs-lookup"><span data-stu-id="dbb49-446">The namespace of the **Name** property when the **NameNamespace** property includes the value 1 (Other).</span></span> <span data-ttu-id="dbb49-447">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dbb49-447">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-448">**PackageRedundancy**</span><span class="sxs-lookup"><span data-stu-id="dbb49-448">**PackageRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-449">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-449">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-450">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-451">O número de pacotes físicos que podem falhar no momento sem perda de dados.</span><span class="sxs-lookup"><span data-stu-id="dbb49-451">The number of physical packages that can currently fail without data loss.</span></span> <span data-ttu-id="dbb49-452">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)e é sempre definida como 0.</span><span class="sxs-lookup"><span data-stu-id="dbb49-452">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-453">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="dbb49-453">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-454">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-454">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-455">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-456">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-456">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-457">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="dbb49-457">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-458">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="dbb49-458">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-459">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-460">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-460">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-461">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="dbb49-461">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-462">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dbb49-462">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-463">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-463">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-464">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-464">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-465">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="dbb49-465">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-466">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-466">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-467">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-468">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="dbb49-468">Provides high level status information.</span></span> <span data-ttu-id="dbb49-469">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="dbb49-469">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="dbb49-470">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-470">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dbb49-471">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dbb49-471">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="dbb49-472"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="dbb49-472"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-473"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="dbb49-473"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-474"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="dbb49-474"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-475"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="dbb49-475"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-476"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="dbb49-476"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="dbb49-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="dbb49-478">)</span><span class="sxs-lookup"><span data-stu-id="dbb49-478">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dbb49-479">**Primordial**</span><span class="sxs-lookup"><span data-stu-id="dbb49-479">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-480">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="dbb49-480">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-481">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-482">**True** se o sistema recipiente não tiver a capacidade de criar ou excluir este elemento operacional.</span><span class="sxs-lookup"><span data-stu-id="dbb49-482">**True** if the containing system does not have the ability to create or delete this operational element.</span></span> <span data-ttu-id="dbb49-483">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="dbb49-483">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-484">**Finalidade**</span><span class="sxs-lookup"><span data-stu-id="dbb49-484">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-485">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbb49-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-486">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-487">Uma cadeia de caracteres que descreve a mídia e seu uso.</span><span class="sxs-lookup"><span data-stu-id="dbb49-487">A string that describes the media and its use.</span></span> <span data-ttu-id="dbb49-488">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)e é sempre definida como "memória do sistema".</span><span class="sxs-lookup"><span data-stu-id="dbb49-488">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to "System Memory".</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-489">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="dbb49-489">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-490">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-490">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-491">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-491">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-492">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="dbb49-492">The last requested or desired state for the element.</span></span> <span data-ttu-id="dbb49-493">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="dbb49-493">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="dbb49-494">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="dbb49-494">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="dbb49-495">Uma determinada instância do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) pode não dar suporte ao método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="dbb49-495">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="dbb49-496">Se isso ocorrer, o valor 12 (não aplicável) será usado.</span><span class="sxs-lookup"><span data-stu-id="dbb49-496">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="dbb49-497">Essa propriedade é herdada do **CIM \_ EnabledLogicalElement**.</span><span class="sxs-lookup"><span data-stu-id="dbb49-497">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-498">**Tenha**</span><span class="sxs-lookup"><span data-stu-id="dbb49-498">**SequentialAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-499">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="dbb49-499">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-500">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-501">**True** se o armazenamento for acessado sequencialmente por um dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="dbb49-501">**True** if the storage is sequentially accessed by a media access device.</span></span> <span data-ttu-id="dbb49-502">Uma partição de fita é um exemplo de uma extensão de armazenamento acessada em sequência.</span><span class="sxs-lookup"><span data-stu-id="dbb49-502">A tape partition is an example of a sequentially accessed storage extent.</span></span> <span data-ttu-id="dbb49-503">Volumes de armazenamento, partições de disco e discos lógicos representam extensões acessadas aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="dbb49-503">Storage volumes, disk partitions, and logical disks represent randomly accessed extents.</span></span> <span data-ttu-id="dbb49-504">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)e é sempre definida como **false**.</span><span class="sxs-lookup"><span data-stu-id="dbb49-504">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-505">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="dbb49-505">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-506">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dbb49-506">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-507">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-508">O endereço inicial referenciado por um aplicativo ou sistema operacional e mapeado por um controlador de memória para esse objeto de memória.</span><span class="sxs-lookup"><span data-stu-id="dbb49-508">The beginning address referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="dbb49-509">Essa propriedade é herdada [**da \_ memória CIM**](/windows/desktop/CIMWin32Prov/cim-memory)e é sempre definida como 0.</span><span class="sxs-lookup"><span data-stu-id="dbb49-509">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-510">**Status**</span><span class="sxs-lookup"><span data-stu-id="dbb49-510">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-511">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbb49-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-512">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-512">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-513">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-513">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-514">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="dbb49-514">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-515">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbb49-515">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-516">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-517">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="dbb49-517">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="dbb49-518">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dbb49-518">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-519">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="dbb49-519">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-520">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-520">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-521">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-521">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-522">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-522">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-523">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dbb49-523">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-524">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbb49-524">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-525">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-525">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-526">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="dbb49-526">The scoping system's creation class name.</span></span> <span data-ttu-id="dbb49-527">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="dbb49-527">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-528">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="dbb49-528">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-529">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="dbb49-529">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-530">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-531">Essa propriedade é herdada [**da \_ memória CIM**](/windows/desktop/CIMWin32Prov/cim-memory), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-531">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-532">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="dbb49-532">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-533">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbb49-533">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-534">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-534">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-535">O identificador exclusivo para a máquina virtual de escopo.</span><span class="sxs-lookup"><span data-stu-id="dbb49-535">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="dbb49-536">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="dbb49-536">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-537">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="dbb49-537">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-538">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dbb49-538">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-539">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-539">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-540">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="dbb49-540">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="dbb49-541">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como "NULL".</span><span class="sxs-lookup"><span data-stu-id="dbb49-541">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to "NULL".</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-542">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="dbb49-542">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-543">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dbb49-543">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-544">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-544">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-545">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="dbb49-545">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-546">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="dbb49-546">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-547">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbb49-547">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-548">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-548">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-549">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="dbb49-549">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="dbb49-550">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dbb49-550">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="dbb49-551">**Volátil**</span><span class="sxs-lookup"><span data-stu-id="dbb49-551">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb49-552">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="dbb49-552">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbb49-553">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbb49-553">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb49-554">Indica se a memória é volátil.</span><span class="sxs-lookup"><span data-stu-id="dbb49-554">Indicates whether memory is volatile.</span></span> <span data-ttu-id="dbb49-555">Essa propriedade é herdada [**da \_ memória CIM**](/windows/desktop/CIMWin32Prov/cim-memory)e é sempre definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="dbb49-555">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), and it is always set to **True**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dbb49-556">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbb49-556">Remarks</span></span>

<span data-ttu-id="dbb49-557">O acesso à classe de **\_ memória Msvm** pode ser restringido pela filtragem UAC.</span><span class="sxs-lookup"><span data-stu-id="dbb49-557">Access to the **Msvm\_Memory** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="dbb49-558">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="dbb49-558">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="dbb49-559">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbb49-559">Requirements</span></span>



| <span data-ttu-id="dbb49-560">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbb49-560">Requirement</span></span> | <span data-ttu-id="dbb49-561">Valor</span><span class="sxs-lookup"><span data-stu-id="dbb49-561">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbb49-562">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbb49-562">Minimum supported client</span></span><br/> | <span data-ttu-id="dbb49-563">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dbb49-563">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dbb49-564">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbb49-564">Minimum supported server</span></span><br/> | <span data-ttu-id="dbb49-565">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dbb49-565">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dbb49-566">Namespace</span><span class="sxs-lookup"><span data-stu-id="dbb49-566">Namespace</span></span><br/>                | <span data-ttu-id="dbb49-567">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="dbb49-567">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dbb49-568">MOF</span><span class="sxs-lookup"><span data-stu-id="dbb49-568">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbb49-569"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dbb49-569"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dbb49-570">DLL</span><span class="sxs-lookup"><span data-stu-id="dbb49-570">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbb49-571"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dbb49-571"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dbb49-572">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbb49-572">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbb49-573">**\_Memória CIM**</span><span class="sxs-lookup"><span data-stu-id="dbb49-573">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> <dt>

[<span data-ttu-id="dbb49-574">**\_Memória CIM**</span><span class="sxs-lookup"><span data-stu-id="dbb49-574">**CIM\_Memory**</span></span>](/windows/desktop/CIMWin32Prov/cim-memory)
</dt> <dt>

[<span data-ttu-id="dbb49-575">Classes de memória</span><span class="sxs-lookup"><span data-stu-id="dbb49-575">Memory Classes</span></span>](memory-classes.md)
</dt> </dl>

 

