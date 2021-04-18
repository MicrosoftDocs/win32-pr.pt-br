---
description: Representa a mídia da unidade de armazenamento e é usada para preencher as unidades de armazenamento.
ms.assetid: 06955C09-CA56-4B4C-997B-9B65AF125375
title: Classe Msvm_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LogicalDisk
- Msvm_LogicalDisk.SetPowerState
- Msvm_LogicalDisk.EnableDevice
- Msvm_LogicalDisk.OnlineDevice
- Msvm_LogicalDisk.QuiesceDevice
- Msvm_LogicalDisk.SaveProperties
- Msvm_LogicalDisk.RestoreProperties
- Msvm_LogicalDisk.InstanceID
- Msvm_LogicalDisk.Caption
- Msvm_LogicalDisk.Description
- Msvm_LogicalDisk.ElementName
- Msvm_LogicalDisk.InstallDate
- Msvm_LogicalDisk.Name
- Msvm_LogicalDisk.OperationalStatus
- Msvm_LogicalDisk.StatusDescriptions
- Msvm_LogicalDisk.Status
- Msvm_LogicalDisk.HealthState
- Msvm_LogicalDisk.CommunicationStatus
- Msvm_LogicalDisk.DetailedStatus
- Msvm_LogicalDisk.OperatingStatus
- Msvm_LogicalDisk.PrimaryStatus
- Msvm_LogicalDisk.EnabledState
- Msvm_LogicalDisk.OtherEnabledState
- Msvm_LogicalDisk.RequestedState
- Msvm_LogicalDisk.EnabledDefault
- Msvm_LogicalDisk.TimeOfLastStateChange
- Msvm_LogicalDisk.AvailableRequestedStates
- Msvm_LogicalDisk.TransitioningToState
- Msvm_LogicalDisk.SystemCreationClassName
- Msvm_LogicalDisk.SystemName
- Msvm_LogicalDisk.CreationClassName
- Msvm_LogicalDisk.DeviceID
- Msvm_LogicalDisk.PowerManagementSupported
- Msvm_LogicalDisk.PowerManagementCapabilities
- Msvm_LogicalDisk.Availability
- Msvm_LogicalDisk.StatusInfo
- Msvm_LogicalDisk.LastErrorCode
- Msvm_LogicalDisk.ErrorDescription
- Msvm_LogicalDisk.ErrorCleared
- Msvm_LogicalDisk.OtherIdentifyingInfo
- Msvm_LogicalDisk.PowerOnHours
- Msvm_LogicalDisk.TotalPowerOnHours
- Msvm_LogicalDisk.IdentifyingDescriptions
- Msvm_LogicalDisk.AdditionalAvailability
- Msvm_LogicalDisk.MaxQuiesceTime
- Msvm_LogicalDisk.DataOrganization
- Msvm_LogicalDisk.Purpose
- Msvm_LogicalDisk.Access
- Msvm_LogicalDisk.ErrorMethodology
- Msvm_LogicalDisk.BlockSize
- Msvm_LogicalDisk.NumberOfBlocks
- Msvm_LogicalDisk.ConsumableBlocks
- Msvm_LogicalDisk.IsBasedOnUnderlyingRedundancy
- Msvm_LogicalDisk.SequentialAccess
- Msvm_LogicalDisk.ExtentStatus
- Msvm_LogicalDisk.NoSinglePointOfFailure
- Msvm_LogicalDisk.DataRedundancy
- Msvm_LogicalDisk.PackageRedundancy
- Msvm_LogicalDisk.DeltaReservation
- Msvm_LogicalDisk.Primordial
- Msvm_LogicalDisk.NameFormat
- Msvm_LogicalDisk.NameNamespace
- Msvm_LogicalDisk.OtherNameNamespace
- Msvm_LogicalDisk.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e5071f2a102a32364888c9c7de5121ede5249f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810344"
---
# <a name="msvm_logicaldisk-class"></a><span data-ttu-id="0d864-103">\_Classe Msvm LogicalDisk</span><span class="sxs-lookup"><span data-stu-id="0d864-103">Msvm\_LogicalDisk class</span></span>

<span data-ttu-id="0d864-104">Representa a mídia da unidade de armazenamento e é usada para preencher as unidades de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0d864-104">Represents storage drive media and is used to populate the storage drives.</span></span> <span data-ttu-id="0d864-105">Os tipos de mídia com suporte incluem arquivos de disco rígido virtual, arquivos de disquete virtuais, arquivos ISO e mídia de dispositivo físico.</span><span class="sxs-lookup"><span data-stu-id="0d864-105">The media types supported include virtual hard files, virtual floppy files, ISO files, and physical device media.</span></span>

<span data-ttu-id="0d864-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0d864-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d864-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d864-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LogicalDisk : CIM_LogicalDisk
{
  string   InstanceID;
  string   Caption;
  uint64   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
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
  uint16   CreationClassName = "Msvm_LogicalDisk";
  string   DeviceID;
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
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  uint16   DataOrganization = 2;
  string   Purpose;
  uint16   Access;
  string   ErrorMethodology;
  uint64   BlockSize = 512;
  uint64   NumberOfBlocks = 266338304;
  uint64   ConsumableBlocks = 0;
  boolean  IsBasedOnUnderlyingRedundancy = False;
  boolean  SequentialAccess = False;
  uint16   ExtentStatus[] = { 2 };
  boolean  NoSinglePointOfFailure = False;
  uint16   DataRedundancy = 0;
  uint16   PackageRedundancy = 0;
  uint8    DeltaReservation = 0;
  boolean  Primordial = False;
  uint16   NameFormat = 12;
  uint16   NameNamespace = 8;
  string   OtherNameNamespace;
  string   OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="0d864-108">Membros</span><span class="sxs-lookup"><span data-stu-id="0d864-108">Members</span></span>

<span data-ttu-id="0d864-109">A classe **Msvm \_ LogicalDisk** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0d864-109">The **Msvm\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="0d864-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="0d864-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="0d864-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0d864-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0d864-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="0d864-112">Methods</span></span>

<span data-ttu-id="0d864-113">A classe **Msvm \_ LogicalDisk** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="0d864-113">The **Msvm\_LogicalDisk** class has these methods.</span></span>



| <span data-ttu-id="0d864-114">Método</span><span class="sxs-lookup"><span data-stu-id="0d864-114">Method</span></span>                                                            | <span data-ttu-id="0d864-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d864-115">Description</span></span>                              |
|:------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="0d864-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="0d864-116">**EnableDevice**</span></span>                                                  | <span data-ttu-id="0d864-117">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="0d864-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0d864-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="0d864-118">**OnlineDevice**</span></span>                                                  | <span data-ttu-id="0d864-119">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="0d864-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0d864-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="0d864-120">**QuiesceDevice**</span></span>                                                 | <span data-ttu-id="0d864-121">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="0d864-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="0d864-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="0d864-122">**RequestStateChange**</span></span>](msvm-logicaldisk-requeststatechange.md) | <span data-ttu-id="0d864-123">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="0d864-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="0d864-124">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="0d864-124">**Reset**</span></span>](msvm-logicaldisk-reset.md)                           | <span data-ttu-id="0d864-125">Redefine o serviço.</span><span class="sxs-lookup"><span data-stu-id="0d864-125">Resets the service.</span></span><br/>           |
| <span data-ttu-id="0d864-126">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="0d864-126">**RestoreProperties**</span></span>                                             | <span data-ttu-id="0d864-127">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="0d864-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0d864-128">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="0d864-128">**SaveProperties**</span></span>                                                | <span data-ttu-id="0d864-129">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="0d864-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0d864-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0d864-130">**SetPowerState**</span></span>                                                 | <span data-ttu-id="0d864-131">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="0d864-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0d864-132">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0d864-132">Properties</span></span>

<span data-ttu-id="0d864-133">A classe **Msvm \_ LogicalDisk** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0d864-133">The **Msvm\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0d864-134">**Acesso**</span><span class="sxs-lookup"><span data-stu-id="0d864-134">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-135">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d864-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-137">Indica se a mídia é legível, gravável ou ambas.</span><span class="sxs-lookup"><span data-stu-id="0d864-137">Indicates whether the media is readable, writeable, or both.</span></span> <span data-ttu-id="0d864-138">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="0d864-138">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="0d864-139">Valor</span><span class="sxs-lookup"><span data-stu-id="0d864-139">Value</span></span>                                                                        | <span data-ttu-id="0d864-140">Significado</span><span class="sxs-lookup"><span data-stu-id="0d864-140">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="0d864-141"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0d864-141"><dt>0</dt></span></span> </dl> | <span data-ttu-id="0d864-142">Unknown</span><span class="sxs-lookup"><span data-stu-id="0d864-142">Unknown</span></span><br/>     |
| <dl> <span data-ttu-id="0d864-143"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0d864-143"><dt>1</dt></span></span> </dl> | <span data-ttu-id="0d864-144">Seres.</span><span class="sxs-lookup"><span data-stu-id="0d864-144">Readable.</span></span><br/>   |
| <dl> <span data-ttu-id="0d864-145"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0d864-145"><dt>2</dt></span></span> </dl> | <span data-ttu-id="0d864-146">Gravável.</span><span class="sxs-lookup"><span data-stu-id="0d864-146">Writeable.</span></span><br/>  |
| <dl> <span data-ttu-id="0d864-147"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0d864-147"><dt>3</dt></span></span> </dl> | <span data-ttu-id="0d864-148">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0d864-148">Read/write.</span></span><br/> |
| <dl> <span data-ttu-id="0d864-149"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="0d864-149"><dt>4</dt></span></span> </dl> | <span data-ttu-id="0d864-150">Gravar uma vez.</span><span class="sxs-lookup"><span data-stu-id="0d864-150">Write once.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0d864-151">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="0d864-151">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-152">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d864-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0d864-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-154">Qualquer disponibilidade e status adicionais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0d864-154">Any additional availability and status of the device.</span></span> <span data-ttu-id="0d864-155">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="0d864-155">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="0d864-156">Valor</span><span class="sxs-lookup"><span data-stu-id="0d864-156">Value</span></span>                                                                            | <span data-ttu-id="0d864-157">Significado</span><span class="sxs-lookup"><span data-stu-id="0d864-157">Meaning</span></span>                    |
|----------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="0d864-158"><dt>152</dt></span><span class="sxs-lookup"><span data-stu-id="0d864-158"><dt>{ 6 }</dt></span></span> </dl> | <span data-ttu-id="0d864-159">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="0d864-159">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0d864-160">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="0d864-160">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-161">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d864-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-163">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0d864-163">The primary availability and status of the device.</span></span> <span data-ttu-id="0d864-164">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="0d864-164">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="0d864-165">Valor</span><span class="sxs-lookup"><span data-stu-id="0d864-165">Value</span></span>                                                                        | <span data-ttu-id="0d864-166">Significado</span><span class="sxs-lookup"><span data-stu-id="0d864-166">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="0d864-167"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="0d864-167"><dt>6</dt></span></span> </dl> | <span data-ttu-id="0d864-168">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="0d864-168">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0d864-169">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="0d864-169">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-170">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d864-170">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0d864-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-172">Indica os valores possíveis para o parâmetro *requestedstate* do método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="0d864-172">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="0d864-173">Os valores listados serão um subconjunto dos valores contidos na propriedade **RequestedStatesSupported** da instância associada do **CIM \_ EnabledLogicalElementCapabilities**, em que os valores selecionados são uma função do estado atual do objeto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0d864-173">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="0d864-174">Essa propriedade pode ser não **nula** se uma implementação for capaz de anunciar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="0d864-174">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="0d864-175">Essa propriedade será **nula** se uma implementação não puder determinar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="0d864-175">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="0d864-176">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0d864-176">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-177">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="0d864-177">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-178">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0d864-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-180">O tamanho, em bytes, dos blocos que formam a extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0d864-180">The size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="0d864-181">Se o tamanho do bloco for variável, o tamanho máximo do bloco, em bytes, deverá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="0d864-181">If the block size is variable, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="0d864-182">Se o tamanho do bloco for desconhecido ou se um conceito de bloco não for válido (por exemplo, para extensões de agregação, memória ou discos lógicos), isso conterá 1.</span><span class="sxs-lookup"><span data-stu-id="0d864-182">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), this will contain 1.</span></span> <span data-ttu-id="0d864-183">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="0d864-183">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-184">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="0d864-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-185">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d864-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-187">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="0d864-187">A short description of the object.</span></span> <span data-ttu-id="0d864-188">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0d864-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="0d864-189">"Imagem de disco ISO"</span><span class="sxs-lookup"><span data-stu-id="0d864-189">"ISO Disk Image"</span></span>

<span data-ttu-id="0d864-190">"Imagem de disco rígido"</span><span class="sxs-lookup"><span data-stu-id="0d864-190">"Hard Disk Image"</span></span>

<span data-ttu-id="0d864-191">"Imagem de disquete"</span><span class="sxs-lookup"><span data-stu-id="0d864-191">"Floppy Disk Image"</span></span>

<span data-ttu-id="0d864-192">"Disco de CD/DVD"</span><span class="sxs-lookup"><span data-stu-id="0d864-192">"CD/DVD Disk"</span></span>

</dd> <dt>

<span data-ttu-id="0d864-193">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="0d864-193">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-194">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d864-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-196">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="0d864-196">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="0d864-197">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="0d864-197">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0d864-198">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0d864-198">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-199">**ConsumableBlocks**</span><span class="sxs-lookup"><span data-stu-id="0d864-199">**ConsumableBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-200">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0d864-200">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-201">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-202">O número máximo de blocos, de tamanho de **bloco**, que estão disponíveis para consumo ao encamar extensões de armazenamento usando a associação [**\_ com base em Msvm**](msvm-basedon.md) .</span><span class="sxs-lookup"><span data-stu-id="0d864-202">The maximum number of blocks, of size **BlockSize**, that are available for consumption when layering storage extents using the [**Msvm\_BasedOn**](msvm-basedon.md) association.</span></span> <span data-ttu-id="0d864-203">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="0d864-203">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-204">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0d864-204">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-205">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d864-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-207">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="0d864-207">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="0d864-208">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="0d864-208">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-209">**Dataorganization**</span><span class="sxs-lookup"><span data-stu-id="0d864-209">**DataOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-210">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d864-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-212">O tipo de organização de dados usado.</span><span class="sxs-lookup"><span data-stu-id="0d864-212">The type of data organization used.</span></span> <span data-ttu-id="0d864-213">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="0d864-213">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="0d864-214">Valor</span><span class="sxs-lookup"><span data-stu-id="0d864-214">Value</span></span>                                                                        | <span data-ttu-id="0d864-215">Significado</span><span class="sxs-lookup"><span data-stu-id="0d864-215">Meaning</span></span>                 |
|------------------------------------------------------------------------------|-------------------------|
| <dl> <span data-ttu-id="0d864-216"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0d864-216"><dt>2</dt></span></span> </dl> | <span data-ttu-id="0d864-217">Bloco fixo.</span><span class="sxs-lookup"><span data-stu-id="0d864-217">Fixed block.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0d864-218">**Dataredundância**</span><span class="sxs-lookup"><span data-stu-id="0d864-218">**DataRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-219">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d864-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-221">O número de cópias completas dos dados atualmente mantidas.</span><span class="sxs-lookup"><span data-stu-id="0d864-221">The number of complete copies of data currently maintained.</span></span> <span data-ttu-id="0d864-222">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="0d864-222">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-223">**DeltaReservation**</span><span class="sxs-lookup"><span data-stu-id="0d864-223">**DeltaReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-224">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="0d864-224">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-225">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-226">Uma porcentagem que especifica a quantidade de espaço que deve ser reservada em uma réplica para armazenar em cache as alterações.</span><span class="sxs-lookup"><span data-stu-id="0d864-226">A percentage that specifies the amount of space that should be reserved in a replica for caching changes.</span></span> <span data-ttu-id="0d864-227">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="0d864-227">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-228">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0d864-228">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-229">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0d864-229">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-230">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-231">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="0d864-231">A description of the object.</span></span> <span data-ttu-id="0d864-232">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0d864-232">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-233">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="0d864-233">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-234">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d864-234">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-235">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-236">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="0d864-236">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="0d864-237">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="0d864-237">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0d864-238">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0d864-238">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-239">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0d864-239">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-240">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d864-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-242">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como "Microsoft:*GUID*- \\ *specific-data*".</span><span class="sxs-lookup"><span data-stu-id="0d864-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="0d864-243">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0d864-243">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-244">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d864-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-245">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-246">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="0d864-246">A display name for the object.</span></span> <span data-ttu-id="0d864-247">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0d864-247">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="0d864-248">"Imagem de disco ISO"</span><span class="sxs-lookup"><span data-stu-id="0d864-248">"ISO Disk Image"</span></span>

<span data-ttu-id="0d864-249">"Imagem de disco rígido"</span><span class="sxs-lookup"><span data-stu-id="0d864-249">"Hard Disk Image"</span></span>

<span data-ttu-id="0d864-250">"Imagem de disquete"</span><span class="sxs-lookup"><span data-stu-id="0d864-250">"Floppy Disk Image"</span></span>

<span data-ttu-id="0d864-251">"Disco de CD/DVD"</span><span class="sxs-lookup"><span data-stu-id="0d864-251">"CD/DVD Disk"</span></span>

</dd> <dt>

<span data-ttu-id="0d864-252">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="0d864-252">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-253">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d864-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-254">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-255">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="0d864-255">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="0d864-256">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0d864-256">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-257">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="0d864-257">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-258">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d864-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-260">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="0d864-260">The enabled and disabled states of an element.</span></span> <span data-ttu-id="0d864-261">Ele também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="0d864-261">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="0d864-262">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0d864-262">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-263">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="0d864-263">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-264">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0d864-264">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-265">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-266">Indica se o erro relatado em **LastErrorCode** agora está limpo.</span><span class="sxs-lookup"><span data-stu-id="0d864-266">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="0d864-267">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="0d864-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0d864-268">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0d864-268">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-269">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d864-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-271">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="0d864-271">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="0d864-272">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="0d864-272">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0d864-273">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="0d864-273">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-274">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d864-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-275">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-276">Uma cadeia de caracteres que descreve os tipos de detecção de erros e correção com suporte neste dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0d864-276">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="0d864-277">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="0d864-277">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-278">**ExtentStatus**</span><span class="sxs-lookup"><span data-stu-id="0d864-278">**ExtentStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-279">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d864-279">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0d864-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-281">Qualquer informação de status adicional além daquela capturada no **OperationalStatus** e outras propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0d864-281">Any additional status information beyond that captured in the **OperationalStatus** and other inherited properties.</span></span>



| <span data-ttu-id="0d864-282">Valor</span><span class="sxs-lookup"><span data-stu-id="0d864-282">Value</span></span>                                                                            | <span data-ttu-id="0d864-283">Significado</span><span class="sxs-lookup"><span data-stu-id="0d864-283">Meaning</span></span>                         |
|----------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="0d864-284"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0d864-284"><dt>{ 2 }</dt></span></span> </dl> | <span data-ttu-id="0d864-285">Nenhum/não aplicável.</span><span class="sxs-lookup"><span data-stu-id="0d864-285">None/Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0d864-286">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="0d864-286">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-287">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d864-287">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-288">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-289">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="0d864-289">The current health of the element.</span></span> <span data-ttu-id="0d864-290">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="0d864-290">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="0d864-291">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="0d864-291">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="0d864-292">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0d864-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-293">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0d864-293">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-294">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d864-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0d864-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-296">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz de propriedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="0d864-296">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="0d864-297">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0d864-297">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0d864-298">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0d864-298">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-299">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0d864-299">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-300">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-301">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="0d864-301">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="0d864-302">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0d864-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-303">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0d864-303">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-304">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d864-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-305">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d864-306">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="0d864-306">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0d864-307">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="0d864-307">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0d864-308">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0d864-308">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-309">**IsBasedOnUnderlyingRedundancy**</span><span class="sxs-lookup"><span data-stu-id="0d864-309">**IsBasedOnUnderlyingRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-310">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0d864-310">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-311">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-312">Indica se as extensões de armazenamento subjacentes participam de um grupo de redundância de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0d864-312">Indicates whether the underlying storage extents participate in a storage redundancy group.</span></span> <span data-ttu-id="0d864-313">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="0d864-313">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-314">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0d864-314">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-315">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0d864-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-317">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0d864-317">The last error code reported by the logical device.</span></span> <span data-ttu-id="0d864-318">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="0d864-318">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0d864-319">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="0d864-319">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-320">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0d864-320">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-322">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="0d864-322">This property has been deprecated.</span></span> <span data-ttu-id="0d864-323">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="0d864-323">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0d864-324">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0d864-324">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-325">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d864-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-326">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-327">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="0d864-327">The label by which the object is known.</span></span> <span data-ttu-id="0d864-328">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é a mesma que a propriedade **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="0d864-328">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="0d864-329">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="0d864-329">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-330">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d864-330">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-331">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-332">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="0d864-332">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="0d864-333">Valor</span><span class="sxs-lookup"><span data-stu-id="0d864-333">Value</span></span>                                                                         | <span data-ttu-id="0d864-334">Significado</span><span class="sxs-lookup"><span data-stu-id="0d864-334">Meaning</span></span>                                 |
|-------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="0d864-335"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0d864-335"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="0d864-336">Outro</span><span class="sxs-lookup"><span data-stu-id="0d864-336">Other</span></span><br/>                        |
| <dl> <span data-ttu-id="0d864-337"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="0d864-337"><dt>12</dt></span></span> </dl> | <span data-ttu-id="0d864-338">Nome do dispositivo do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="0d864-338">Operating system device name</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0d864-339">**NameNamespace**</span><span class="sxs-lookup"><span data-stu-id="0d864-339">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-340">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d864-340">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-342">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="0d864-342">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="0d864-343">Valor</span><span class="sxs-lookup"><span data-stu-id="0d864-343">Value</span></span>                                                                        | <span data-ttu-id="0d864-344">Significado</span><span class="sxs-lookup"><span data-stu-id="0d864-344">Meaning</span></span>                                      |
|------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="0d864-345"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0d864-345"><dt>1</dt></span></span> </dl> | <span data-ttu-id="0d864-346">Outro</span><span class="sxs-lookup"><span data-stu-id="0d864-346">Other</span></span><br/>                             |
| <dl> <span data-ttu-id="0d864-347"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="0d864-347"><dt>8</dt></span></span> </dl> | <span data-ttu-id="0d864-348">Namespace de dispositivo do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="0d864-348">Operating system device namespace</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0d864-349">**NoSinglePointOfFailure**</span><span class="sxs-lookup"><span data-stu-id="0d864-349">**NoSinglePointOfFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-350">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0d864-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-351">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-352">Indica se não existe nenhum ponto único de falha.</span><span class="sxs-lookup"><span data-stu-id="0d864-352">Indicates whether there exists no single point of failure.</span></span> <span data-ttu-id="0d864-353">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="0d864-353">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-354">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="0d864-354">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-355">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0d864-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-356">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-357">O número de blocos consecutivos, cada um deles com o tamanho do valor contido na propriedade **BlockSize** , que forma a extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0d864-357">The number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="0d864-358">O tamanho total da extensão de armazenamento pode ser calculado multiplicando o valor da propriedade **BlockSize** pelo valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="0d864-358">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="0d864-359">Se o valor de **BlockSize** for 1, essa propriedade será o tamanho total da extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0d864-359">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span> <span data-ttu-id="0d864-360">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="0d864-360">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-361">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="0d864-361">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-362">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d864-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-363">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-364">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="0d864-364">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="0d864-365">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="0d864-365">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0d864-366">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0d864-366">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-367">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="0d864-367">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-368">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d864-368">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0d864-369">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d864-370">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="0d864-370">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="0d864-371">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="0d864-371">The current statuses of the object.</span></span> <span data-ttu-id="0d864-372">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0d864-372">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="0d864-373">Quando o nível de QoS necessário para o disco virtual não puder ser satisfeito, o status principal (OperationalStatus \[ 0 \] ) será definido como degradado (3) e a matriz OperationalStatus também conterá um valor de status secundário que indica o motivo específico para a condição de QoS, de acordo com esta tabela.</span><span class="sxs-lookup"><span data-stu-id="0d864-373">When the required QoS level for the virtual disk can't be satisfied, the primary status (OperationalStatus\[0\]) is set to Degraded (3) and the OperationalStatus array additionally contains a secondary status value that indicates the specific reason for the QoS condition, according to this table.</span></span>



| <span data-ttu-id="0d864-374">Valor</span><span class="sxs-lookup"><span data-stu-id="0d864-374">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="0d864-375">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d864-375">Description</span></span>                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d864-376"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Taxa de transferência insuficiente (32788)</span><span class="sxs-lookup"><span data-stu-id="0d864-376"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Insufficient Throughput  (32788)</span></span><br/> | <span data-ttu-id="0d864-377">A taxa mínima de IOPS solicitada não está disponível para o dispositivo no momento.</span><span class="sxs-lookup"><span data-stu-id="0d864-377">The requested minimum IOPS rate is currently not available to the device.</span></span> <br/> |



 

> [!Note]  
> <span data-ttu-id="0d864-378">OperationalStatus também é usado para relatar outras condições de erro ou de aviso (por exemplo, incompatibilidade de protocolo entre VSP e VSC).</span><span class="sxs-lookup"><span data-stu-id="0d864-378">OperationalStatus is also used to report other error or warning conditions (for example, protocol mismatch between VSP and VSC).</span></span> <span data-ttu-id="0d864-379">Se houver várias condições, o status principal será definido como degradado e um ou mais valores de status secundários, em qualquer ordem a partir do índice 1, será preenchido na matriz.</span><span class="sxs-lookup"><span data-stu-id="0d864-379">If multiple conditions exists, the primary status is set Degraded, and one or more secondary status values, in any order starting at index 1, is filled in the array.</span></span>

 

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0d864-380"><span id="OK"></span><span id="ok"></span>**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="0d864-380"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0d864-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (3)</span><span class="sxs-lookup"><span data-stu-id="0d864-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="0d864-382"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (7)</span><span class="sxs-lookup"><span data-stu-id="0d864-382"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span data-ttu-id="0d864-383"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (11)</span><span class="sxs-lookup"><span data-stu-id="0d864-383"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (11)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="0d864-384">Adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0d864-384">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0d864-385"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sem contato** (12)</span><span class="sxs-lookup"><span data-stu-id="0d864-385"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="0d864-386"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (13)</span><span class="sxs-lookup"><span data-stu-id="0d864-386"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span data-ttu-id="0d864-387"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (16)</span><span class="sxs-lookup"><span data-stu-id="0d864-387"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (16)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="0d864-388">Adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0d864-388">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>

<span data-ttu-id="0d864-389"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Incompatibilidade de protocolo** (32775)</span><span class="sxs-lookup"><span data-stu-id="0d864-389"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Protocol Mismatch** (32775)</span></span>


</dt> <dd></dd> <dt>

<span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>

<span data-ttu-id="0d864-390"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Tempo limite de comunicação** (32783)</span><span class="sxs-lookup"><span data-stu-id="0d864-390"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Communication Timed Out** (32783)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="0d864-391">Adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0d864-391">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>

<span data-ttu-id="0d864-392"><span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>**Taxa de transferência insuficiente** (32788)</span><span class="sxs-lookup"><span data-stu-id="0d864-392"><span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>**Insufficient Throughput** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown_QoS_Policy_ID"></span><span id="unknown_qos_policy_id"></span><span id="UNKNOWN_QOS_POLICY_ID"></span>

<span data-ttu-id="0d864-393"><span id="Unknown_QoS_Policy_ID"></span><span id="unknown_qos_policy_id"></span><span id="UNKNOWN_QOS_POLICY_ID"></span>**ID de política de QoS desconhecida** (32791)</span><span class="sxs-lookup"><span data-stu-id="0d864-393"><span id="Unknown_QoS_Policy_ID"></span><span id="unknown_qos_policy_id"></span><span id="UNKNOWN_QOS_POLICY_ID"></span>**Unknown QoS Policy ID** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="QoS_Not_Supported"></span><span id="qos_not_supported"></span><span id="QOS_NOT_SUPPORTED"></span>

<span data-ttu-id="0d864-394"><span id="QoS_Not_Supported"></span><span id="qos_not_supported"></span><span id="QOS_NOT_SUPPORTED"></span>**QoS sem suporte** (32792)</span><span class="sxs-lookup"><span data-stu-id="0d864-394"><span id="QoS_Not_Supported"></span><span id="qos_not_supported"></span><span id="QOS_NOT_SUPPORTED"></span>**QoS Not Supported** (32792)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="0d864-395">Adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0d864-395">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="QoS_Configuration_Mismatch"></span><span id="qos_configuration_mismatch"></span><span id="QOS_CONFIGURATION_MISMATCH"></span>

<span data-ttu-id="0d864-396"><span id="QoS_Configuration_Mismatch"></span><span id="qos_configuration_mismatch"></span><span id="QOS_CONFIGURATION_MISMATCH"></span>**Incompatibilidade de configuração de QoS** (32793)</span><span class="sxs-lookup"><span data-stu-id="0d864-396"><span id="QoS_Configuration_Mismatch"></span><span id="qos_configuration_mismatch"></span><span id="QOS_CONFIGURATION_MISMATCH"></span>**QoS Configuration Mismatch** (32793)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="0d864-397">Adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0d864-397">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Disk_Full"></span><span id="disk_full"></span><span id="DISK_FULL"></span>

<span data-ttu-id="0d864-398"><span id="Disk_Full"></span><span id="disk_full"></span><span id="DISK_FULL"></span>**Disco cheio** (32794)</span><span class="sxs-lookup"><span data-stu-id="0d864-398"><span id="Disk_Full"></span><span id="disk_full"></span><span id="DISK_FULL"></span>**Disk Full** (32794)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="0d864-399">Adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0d864-399">Added in Windows 10.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0d864-400">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="0d864-400">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-401">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d864-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-402">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-403">O estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="0d864-403">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="0d864-404">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="0d864-404">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="0d864-405">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0d864-405">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-406">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="0d864-406">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-407">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d864-407">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0d864-408">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-409">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0d864-409">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="0d864-410">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0d864-410">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0d864-411">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="0d864-411">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-412">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d864-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-413">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-414">Uma cadeia de caracteres que descreve o formato da propriedade **Name** quando **NameFormat** contém o valor 1 (Other).</span><span class="sxs-lookup"><span data-stu-id="0d864-414">A string that describes the format of the **Name** property when **NameFormat** contains the value 1 (Other).</span></span> <span data-ttu-id="0d864-415">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="0d864-415">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-416">**OtherNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="0d864-416">**OtherNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-417">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d864-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-418">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-419">Uma cadeia de caracteres que descreve o namespace da propriedade **Name** quando **NameNamespace** contém o valor 1 (Other).</span><span class="sxs-lookup"><span data-stu-id="0d864-419">A string that describes the namespace of the **Name** property when **NameNamespace** contains the value 1 (Other).</span></span> <span data-ttu-id="0d864-420">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="0d864-420">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-421">**PackageRedundancy**</span><span class="sxs-lookup"><span data-stu-id="0d864-421">**PackageRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-422">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d864-422">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-423">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-424">O número de pacotes físicos que podem falhar no momento sem perda de dados.</span><span class="sxs-lookup"><span data-stu-id="0d864-424">The number of physical packages that can currently fail without data loss.</span></span> <span data-ttu-id="0d864-425">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="0d864-425">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-426">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0d864-426">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-427">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d864-427">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0d864-428">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-429">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0d864-429">The power management capabilities of the device.</span></span> <span data-ttu-id="0d864-430">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="0d864-430">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0d864-431">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="0d864-431">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-432">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0d864-432">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-433">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-434">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="0d864-434">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="0d864-435">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="0d864-435">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0d864-436">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="0d864-436">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-437">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0d864-437">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-438">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-439">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="0d864-439">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="0d864-440">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="0d864-440">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0d864-441">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="0d864-441">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-442">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d864-442">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-443">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-444">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="0d864-444">Provides high level status information.</span></span> <span data-ttu-id="0d864-445">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer informações de status de integridade detalhadas e de alto nível para o elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="0d864-445">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="0d864-446">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="0d864-446">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0d864-447">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0d864-447">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-448">**Primordial**</span><span class="sxs-lookup"><span data-stu-id="0d864-448">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-449">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0d864-449">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-450">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-451">Indica se o sistema recipiente tem a capacidade de criar ou excluir este elemento operacional.</span><span class="sxs-lookup"><span data-stu-id="0d864-451">Indicates whether the containing system has the ability to create or delete this operational element.</span></span> <span data-ttu-id="0d864-452">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)e é definida como **false** para mídia baseada em arquivo e **true** para mídia de passagem.</span><span class="sxs-lookup"><span data-stu-id="0d864-452">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is set to **False** for file-based media and **True** for pass-through media.</span></span>

</dd> <dt>

<span data-ttu-id="0d864-453">**Finalidade**</span><span class="sxs-lookup"><span data-stu-id="0d864-453">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-454">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d864-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-455">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-456">Uma cadeia de caracteres que descreve a mídia e/ou seu uso.</span><span class="sxs-lookup"><span data-stu-id="0d864-456">A string that describes the media and/or its use.</span></span> <span data-ttu-id="0d864-457">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="0d864-457">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-458">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="0d864-458">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-459">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d864-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-460">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-461">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="0d864-461">The last requested or desired state for the element.</span></span> <span data-ttu-id="0d864-462">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="0d864-462">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="0d864-463">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="0d864-463">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="0d864-464">Uma determinada instância do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) pode não dar suporte ao método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="0d864-464">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="0d864-465">Se isso ocorrer, o valor 12 (não aplicável) será usado.</span><span class="sxs-lookup"><span data-stu-id="0d864-465">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="0d864-466">Essa propriedade é herdada do **CIM \_ EnabledLogicalElement**.</span><span class="sxs-lookup"><span data-stu-id="0d864-466">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="0d864-467">**Tenha**</span><span class="sxs-lookup"><span data-stu-id="0d864-467">**SequentialAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-468">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0d864-468">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-469">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-470">Indica se o armazenamento é acessado sequencialmente por um dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="0d864-470">Indicates whether the storage is sequentially accessed by a media access device.</span></span> <span data-ttu-id="0d864-471">A mídia de fita de passagem é um exemplo de uma extensão de armazenamento acessada em sequência.</span><span class="sxs-lookup"><span data-stu-id="0d864-471">Pass-through tape media is an example of a sequentially accessed storage extent.</span></span> <span data-ttu-id="0d864-472">Essa propriedade é herdada do [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="0d864-472">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-473">**Status**</span><span class="sxs-lookup"><span data-stu-id="0d864-473">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-474">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d864-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-475">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-476">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="0d864-476">The current status of the object.</span></span> <span data-ttu-id="0d864-477">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="0d864-477">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0d864-478">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0d864-478">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-479">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d864-479">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0d864-480">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-481">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="0d864-481">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="0d864-482">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0d864-482">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-483">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0d864-483">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-484">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d864-484">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-485">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-485">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-486">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0d864-486">The current state of the logical device.</span></span> <span data-ttu-id="0d864-487">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="0d864-487">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0d864-488">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0d864-488">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-489">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d864-489">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-490">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-491">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="0d864-491">The scoping system's creation class name.</span></span> <span data-ttu-id="0d864-492">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="0d864-492">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-493">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0d864-493">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-494">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d864-494">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-495">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-495">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-496">O identificador exclusivo para a máquina virtual de escopo.</span><span class="sxs-lookup"><span data-stu-id="0d864-496">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="0d864-497">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="0d864-497">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-498">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="0d864-498">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-499">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0d864-499">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-500">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-501">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="0d864-501">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="0d864-502">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0d864-502">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0d864-503">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="0d864-503">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-504">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0d864-504">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-505">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-505">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-506">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="0d864-506">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="0d864-507">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="0d864-507">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0d864-508">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="0d864-508">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d864-509">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d864-509">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d864-510">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d864-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d864-511">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="0d864-511">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="0d864-512">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="0d864-512">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d864-513">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d864-513">Remarks</span></span>

<span data-ttu-id="0d864-514">O acesso à classe do **\_ LogicalDisk Msvm** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="0d864-514">Access to the **Msvm\_LogicalDisk** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0d864-515">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="0d864-515">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d864-516">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d864-516">Requirements</span></span>



| <span data-ttu-id="0d864-517">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d864-517">Requirement</span></span> | <span data-ttu-id="0d864-518">Valor</span><span class="sxs-lookup"><span data-stu-id="0d864-518">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d864-519">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d864-519">Minimum supported client</span></span><br/> | <span data-ttu-id="0d864-520">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0d864-520">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0d864-521">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d864-521">Minimum supported server</span></span><br/> | <span data-ttu-id="0d864-522">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0d864-522">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0d864-523">Namespace</span><span class="sxs-lookup"><span data-stu-id="0d864-523">Namespace</span></span><br/>                | <span data-ttu-id="0d864-524">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="0d864-524">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0d864-525">MOF</span><span class="sxs-lookup"><span data-stu-id="0d864-525">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d864-526"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d864-526"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d864-527">DLL</span><span class="sxs-lookup"><span data-stu-id="0d864-527">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d864-528"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0d864-528"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0d864-529">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d864-529">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d864-530">**\_LOGICALDISK CIM**</span><span class="sxs-lookup"><span data-stu-id="0d864-530">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="0d864-531">**\_LOGICALDISK CIM**</span><span class="sxs-lookup"><span data-stu-id="0d864-531">**CIM\_LogicalDisk**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldisk)
</dt> <dt>

[<span data-ttu-id="0d864-532">**Msvm \_ StorageAlert**</span><span class="sxs-lookup"><span data-stu-id="0d864-532">**Msvm\_StorageAlert**</span></span>](msvm-storagealert.md)
</dt> <dt>

[<span data-ttu-id="0d864-533">Classes de armazenamento</span><span class="sxs-lookup"><span data-stu-id="0d864-533">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

