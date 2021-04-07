---
description: Representa uma porta serial associada ao controlador serial.
ms.assetid: 856823A5-7481-453A-8476-1CDAB1D84123
title: Classe Msvm_SerialPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPort
- Msvm_SerialPort.SetPowerState
- Msvm_SerialPort.EnableDevice
- Msvm_SerialPort.OnlineDevice
- Msvm_SerialPort.QuiesceDevice
- Msvm_SerialPort.SaveProperties
- Msvm_SerialPort.RestoreProperties
- Msvm_SerialPort.InstanceID
- Msvm_SerialPort.Caption
- Msvm_SerialPort.Description
- Msvm_SerialPort.ElementName
- Msvm_SerialPort.InstallDate
- Msvm_SerialPort.Name
- Msvm_SerialPort.OperationalStatus
- Msvm_SerialPort.StatusDescriptions
- Msvm_SerialPort.Status
- Msvm_SerialPort.HealthState
- Msvm_SerialPort.CommunicationStatus
- Msvm_SerialPort.DetailedStatus
- Msvm_SerialPort.OperatingStatus
- Msvm_SerialPort.PrimaryStatus
- Msvm_SerialPort.EnabledState
- Msvm_SerialPort.OtherEnabledState
- Msvm_SerialPort.RequestedState
- Msvm_SerialPort.EnabledDefault
- Msvm_SerialPort.TimeOfLastStateChange
- Msvm_SerialPort.AvailableRequestedStates
- Msvm_SerialPort.TransitioningToState
- Msvm_SerialPort.SystemCreationClassName
- Msvm_SerialPort.SystemName
- Msvm_SerialPort.CreationClassName
- Msvm_SerialPort.DeviceID
- Msvm_SerialPort.PowerManagementSupported
- Msvm_SerialPort.PowerManagementCapabilities
- Msvm_SerialPort.Availability
- Msvm_SerialPort.StatusInfo
- Msvm_SerialPort.LastErrorCode
- Msvm_SerialPort.ErrorDescription
- Msvm_SerialPort.ErrorCleared
- Msvm_SerialPort.OtherIdentifyingInfo
- Msvm_SerialPort.PowerOnHours
- Msvm_SerialPort.TotalPowerOnHours
- Msvm_SerialPort.IdentifyingDescriptions
- Msvm_SerialPort.AdditionalAvailability
- Msvm_SerialPort.MaxQuiesceTime
- Msvm_SerialPort.Speed
- Msvm_SerialPort.MaxSpeed
- Msvm_SerialPort.RequestedSpeed
- Msvm_SerialPort.UsageRestriction
- Msvm_SerialPort.PortType
- Msvm_SerialPort.OtherPortType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bc9ff5e1ce4b0a750866a9957c0cffc4bc8501e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828587"
---
# <a name="msvm_serialport-class"></a><span data-ttu-id="a2c53-103">\_Classe SerialPort Msvm</span><span class="sxs-lookup"><span data-stu-id="a2c53-103">Msvm\_SerialPort class</span></span>

<span data-ttu-id="a2c53-104">Representa uma porta serial associada ao controlador serial.</span><span class="sxs-lookup"><span data-stu-id="a2c53-104">Represents a serial port associated with the serial controller.</span></span>

<span data-ttu-id="a2c53-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a2c53-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2c53-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2c53-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPort : CIM_LogicalPort
{
  string   InstanceID;
  string   Caption;
  string   Description = "Microsoft Virtual Serial Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
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
  string   CreationClassName = "Msvm_SerialPort";
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
  uint64   Speed = 115200;
  uint32   MaxSpeed = 115200;
  uint64   RequestedSpeed = 115200;
  uint16   UsageRestriction = 4;
  uint16   PortType = 1;
  string   OtherPortType = "Serial Port";
};
```

## <a name="members"></a><span data-ttu-id="a2c53-107">Membros</span><span class="sxs-lookup"><span data-stu-id="a2c53-107">Members</span></span>

<span data-ttu-id="a2c53-108">A **classe \_ SerialPort Msvm** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a2c53-108">The **Msvm\_SerialPort** class has these types of members:</span></span>

-   [<span data-ttu-id="a2c53-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="a2c53-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="a2c53-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a2c53-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a2c53-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="a2c53-111">Methods</span></span>

<span data-ttu-id="a2c53-112">A **classe \_ SerialPort Msvm** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a2c53-112">The **Msvm\_SerialPort** class has these methods.</span></span>



| <span data-ttu-id="a2c53-113">Método</span><span class="sxs-lookup"><span data-stu-id="a2c53-113">Method</span></span>                                                           | <span data-ttu-id="a2c53-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2c53-114">Description</span></span>                              |
|:-----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="a2c53-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="a2c53-115">**EnableDevice**</span></span>                                                 | <span data-ttu-id="a2c53-116">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="a2c53-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="a2c53-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="a2c53-117">**OnlineDevice**</span></span>                                                 | <span data-ttu-id="a2c53-118">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="a2c53-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="a2c53-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="a2c53-119">**QuiesceDevice**</span></span>                                                | <span data-ttu-id="a2c53-120">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="a2c53-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="a2c53-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="a2c53-121">**RequestStateChange**</span></span>](msvm-serialport-requeststatechange.md) | <span data-ttu-id="a2c53-122">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="a2c53-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="a2c53-123">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="a2c53-123">**Reset**</span></span>](msvm-serialport-reset.md)                           | <span data-ttu-id="a2c53-124">Redefine o dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="a2c53-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="a2c53-125">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="a2c53-125">**RestoreProperties**</span></span>                                            | <span data-ttu-id="a2c53-126">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="a2c53-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="a2c53-127">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="a2c53-127">**SaveProperties**</span></span>                                               | <span data-ttu-id="a2c53-128">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="a2c53-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="a2c53-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a2c53-129">**SetPowerState**</span></span>                                                | <span data-ttu-id="a2c53-130">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="a2c53-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a2c53-131">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a2c53-131">Properties</span></span>

<span data-ttu-id="a2c53-132">A **classe \_ SerialPort Msvm** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a2c53-132">The **Msvm\_SerialPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a2c53-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="a2c53-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-134">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2c53-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-136">Qualquer disponibilidade e status adicionais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a2c53-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="a2c53-137">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="a2c53-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="a2c53-138">Valor</span><span class="sxs-lookup"><span data-stu-id="a2c53-138">Value</span></span>                                                                            | <span data-ttu-id="a2c53-139">Significado</span><span class="sxs-lookup"><span data-stu-id="a2c53-139">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="a2c53-140"><dt>152</dt></span><span class="sxs-lookup"><span data-stu-id="a2c53-140"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="a2c53-141"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="a2c53-141"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="a2c53-142">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="a2c53-142">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a2c53-143">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="a2c53-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-144">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2c53-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-146">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a2c53-146">The primary availability and status of the device.</span></span> <span data-ttu-id="a2c53-147">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="a2c53-147">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="a2c53-148">Valor</span><span class="sxs-lookup"><span data-stu-id="a2c53-148">Value</span></span>                                                                        | <span data-ttu-id="a2c53-149">Significado</span><span class="sxs-lookup"><span data-stu-id="a2c53-149">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="a2c53-150"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="a2c53-150"><dt>6</dt></span></span> </dl> | <span data-ttu-id="a2c53-151">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="a2c53-151">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a2c53-152">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="a2c53-152">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-153">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2c53-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-155">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="a2c53-155">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="a2c53-156">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="a2c53-156">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-157">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="a2c53-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a2c53-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-160">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="a2c53-160">A short description of the object.</span></span> <span data-ttu-id="a2c53-161">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a2c53-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-162">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="a2c53-162">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-163">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2c53-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-165">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="a2c53-165">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="a2c53-166">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="a2c53-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a2c53-167">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a2c53-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a2c53-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="a2c53-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="a2c53-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="a2c53-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="a2c53-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="a2c53-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a2c53-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="a2c53-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a2c53-175">)</span><span class="sxs-lookup"><span data-stu-id="a2c53-175">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a2c53-176">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a2c53-176">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a2c53-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-179">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="a2c53-179">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a2c53-180">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="a2c53-180">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-181">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a2c53-181">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a2c53-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-184">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="a2c53-184">A description of the object.</span></span> <span data-ttu-id="a2c53-185">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a2c53-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-186">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="a2c53-186">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-187">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2c53-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-189">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="a2c53-189">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="a2c53-190">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="a2c53-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a2c53-191">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a2c53-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a2c53-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="a2c53-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="a2c53-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="a2c53-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="a2c53-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="a2c53-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="a2c53-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a2c53-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="a2c53-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a2c53-200">)</span><span class="sxs-lookup"><span data-stu-id="a2c53-200">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a2c53-201">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="a2c53-201">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-202">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a2c53-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-204">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como "Microsoft:*GUID* \\ *Device-specific-data*", em que *os dados específicos do dispositivo* são opcionais.</span><span class="sxs-lookup"><span data-stu-id="a2c53-204">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*", where *device-specific-data* is optional.</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-205">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a2c53-205">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-206">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a2c53-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-208">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="a2c53-208">A display name for the object.</span></span> <span data-ttu-id="a2c53-209">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a2c53-209">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-210">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="a2c53-210">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-211">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2c53-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-213">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="a2c53-213">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="a2c53-214">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a2c53-214">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="a2c53-215">Valor</span><span class="sxs-lookup"><span data-stu-id="a2c53-215">Value</span></span>                                                                        | <span data-ttu-id="a2c53-216">Significado</span><span class="sxs-lookup"><span data-stu-id="a2c53-216">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="a2c53-217"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a2c53-217"><dt>2</dt></span></span> </dl> | <span data-ttu-id="a2c53-218">habilitado</span><span class="sxs-lookup"><span data-stu-id="a2c53-218">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a2c53-219">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="a2c53-219">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-220">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2c53-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-221">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-222">O estado habilitado do elemento.</span><span class="sxs-lookup"><span data-stu-id="a2c53-222">The enabled state of the element.</span></span> <span data-ttu-id="a2c53-223">Ele também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="a2c53-223">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="a2c53-224">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a2c53-224">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="a2c53-225">Valor</span><span class="sxs-lookup"><span data-stu-id="a2c53-225">Value</span></span>                                                                        | <span data-ttu-id="a2c53-226">Significado</span><span class="sxs-lookup"><span data-stu-id="a2c53-226">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="a2c53-227"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="a2c53-227"><dt>5</dt></span></span> </dl> | <span data-ttu-id="a2c53-228">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="a2c53-228">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a2c53-229">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="a2c53-229">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-230">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a2c53-230">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-232">Indica se o erro relatado na propriedade **LastErrorCode** agora está apagado.</span><span class="sxs-lookup"><span data-stu-id="a2c53-232">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="a2c53-233">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="a2c53-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-234">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a2c53-234">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-235">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a2c53-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-236">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-237">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado na propriedade **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="a2c53-237">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="a2c53-238">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="a2c53-238">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-239">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="a2c53-239">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-240">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2c53-240">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-242">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="a2c53-242">The current health of the element.</span></span> <span data-ttu-id="a2c53-243">Isso expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="a2c53-243">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="a2c53-244">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="a2c53-244">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="a2c53-245">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a2c53-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-246">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a2c53-246">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-247">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a2c53-247">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-249">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz de propriedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="a2c53-249">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="a2c53-250">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a2c53-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-251">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a2c53-251">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-252">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a2c53-252">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-253">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-254">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="a2c53-254">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="a2c53-255">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a2c53-255">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-256">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a2c53-256">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-257">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a2c53-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-259">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="a2c53-259">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-260">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="a2c53-260">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a2c53-261">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a2c53-261">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-262">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a2c53-262">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-263">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a2c53-263">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-264">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-265">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a2c53-265">The last error code reported by the logical device.</span></span> <span data-ttu-id="a2c53-266">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="a2c53-266">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-267">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="a2c53-267">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-268">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a2c53-268">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-269">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-270">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="a2c53-270">This property has been deprecated.</span></span> <span data-ttu-id="a2c53-271">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="a2c53-271">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-272">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="a2c53-272">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-273">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a2c53-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-274">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-275">A largura de banda máxima da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="a2c53-275">The maximum bandwidth of the port, in bits-per-second.</span></span> <span data-ttu-id="a2c53-276">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a2c53-276">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-277">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a2c53-277">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-278">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a2c53-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-280">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="a2c53-280">The label by which the object is known.</span></span> <span data-ttu-id="a2c53-281">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é a mesma que a propriedade **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="a2c53-281">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-282">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="a2c53-282">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-283">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2c53-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-284">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-285">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="a2c53-285">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="a2c53-286">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="a2c53-286">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a2c53-287">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a2c53-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a2c53-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="a2c53-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="a2c53-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="a2c53-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="a2c53-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="a2c53-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="a2c53-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="a2c53-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="a2c53-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="a2c53-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="a2c53-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="a2c53-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="a2c53-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="a2c53-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="a2c53-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="a2c53-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="a2c53-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="a2c53-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a2c53-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="a2c53-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a2c53-307">)</span><span class="sxs-lookup"><span data-stu-id="a2c53-307">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a2c53-308">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="a2c53-308">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-309">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2c53-309">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-310">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-311">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="a2c53-311">The current statuses of the object.</span></span> <span data-ttu-id="a2c53-312">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a2c53-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-313">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="a2c53-313">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-314">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a2c53-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-315">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-316">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="a2c53-316">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="a2c53-317">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="a2c53-317">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="a2c53-318">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a2c53-318">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-319">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="a2c53-319">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-320">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a2c53-320">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-322">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a2c53-322">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="a2c53-323">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a2c53-323">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-324">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="a2c53-324">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-325">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a2c53-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-326">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-327">O tipo de módulo, quando **PortType** é definido como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="a2c53-327">The type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="a2c53-328">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a2c53-328">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-329">**PortType**</span><span class="sxs-lookup"><span data-stu-id="a2c53-329">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-330">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2c53-330">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-331">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-332">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a2c53-332">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>



| <span data-ttu-id="a2c53-333">Valor</span><span class="sxs-lookup"><span data-stu-id="a2c53-333">Value</span></span>                                                                        | <span data-ttu-id="a2c53-334">Significado</span><span class="sxs-lookup"><span data-stu-id="a2c53-334">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="a2c53-335"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a2c53-335"><dt>1</dt></span></span> </dl> | <span data-ttu-id="a2c53-336">Outro</span><span class="sxs-lookup"><span data-stu-id="a2c53-336">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a2c53-337">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a2c53-337">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-338">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2c53-338">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-339">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-340">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a2c53-340">The power management capabilities of the device.</span></span> <span data-ttu-id="a2c53-341">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="a2c53-341">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-342">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="a2c53-342">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-343">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a2c53-343">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-344">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-345">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="a2c53-345">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="a2c53-346">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="a2c53-346">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-347">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="a2c53-347">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-348">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a2c53-348">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-349">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-350">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="a2c53-350">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="a2c53-351">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="a2c53-351">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-352">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="a2c53-352">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-353">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2c53-353">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-354">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-355">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="a2c53-355">Provides high level status information.</span></span> <span data-ttu-id="a2c53-356">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="a2c53-356">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="a2c53-357">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="a2c53-357">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a2c53-358">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a2c53-358">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a2c53-359"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="a2c53-359"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-360"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="a2c53-360"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-361"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="a2c53-361"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-362"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="a2c53-362"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-363"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a2c53-363"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-364"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="a2c53-364"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a2c53-365">)</span><span class="sxs-lookup"><span data-stu-id="a2c53-365">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a2c53-366">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="a2c53-366">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-367">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a2c53-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-368">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-369">A largura de banda solicitada da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="a2c53-369">The requested bandwidth of the port, in bits-per-second.</span></span> <span data-ttu-id="a2c53-370">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a2c53-370">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-371">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="a2c53-371">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-372">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2c53-372">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-373">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-374">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="a2c53-374">The last requested or desired state for the element.</span></span> <span data-ttu-id="a2c53-375">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="a2c53-375">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="a2c53-376">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="a2c53-376">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="a2c53-377">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a2c53-377">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="a2c53-378">Valor</span><span class="sxs-lookup"><span data-stu-id="a2c53-378">Value</span></span>                                                                         | <span data-ttu-id="a2c53-379">Significado</span><span class="sxs-lookup"><span data-stu-id="a2c53-379">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="a2c53-380"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="a2c53-380"><dt>12</dt></span></span> </dl> | <span data-ttu-id="a2c53-381">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="a2c53-381">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a2c53-382">**Velocidade**</span><span class="sxs-lookup"><span data-stu-id="a2c53-382">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-383">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a2c53-383">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-384">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-385">A largura de banda da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="a2c53-385">The bandwidth of the port, in bits-per-second.</span></span> <span data-ttu-id="a2c53-386">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a2c53-386">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-387">**Status**</span><span class="sxs-lookup"><span data-stu-id="a2c53-387">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-388">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a2c53-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-389">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-390">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="a2c53-390">The current status of the object.</span></span> <span data-ttu-id="a2c53-391">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="a2c53-391">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-392">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a2c53-392">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-393">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a2c53-393">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-394">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-395">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="a2c53-395">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="a2c53-396">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a2c53-396">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-397">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a2c53-397">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-398">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2c53-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-399">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-400">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a2c53-400">The current state of the logical device.</span></span> <span data-ttu-id="a2c53-401">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="a2c53-401">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-402">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a2c53-402">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-403">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a2c53-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-404">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-405">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="a2c53-405">The scoping system's creation class name.</span></span> <span data-ttu-id="a2c53-406">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="a2c53-406">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-407">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a2c53-407">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-408">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a2c53-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-409">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-410">O identificador exclusivo para a máquina virtual de escopo.</span><span class="sxs-lookup"><span data-stu-id="a2c53-410">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="a2c53-411">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="a2c53-411">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-412">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="a2c53-412">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-413">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a2c53-413">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-414">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-415">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="a2c53-415">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="a2c53-416">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a2c53-416">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-417">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="a2c53-417">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-418">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a2c53-418">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-419">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-420">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="a2c53-420">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="a2c53-421">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="a2c53-421">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-422">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="a2c53-422">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-423">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2c53-423">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-424">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-425">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="a2c53-425">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="a2c53-426">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="a2c53-426">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a2c53-427">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="a2c53-427">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c53-428">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2c53-428">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2c53-429">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c53-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2c53-430">Em algumas circunstâncias, uma porta lógica pode ser identificável como uma porta de front-end ou de back-end.</span><span class="sxs-lookup"><span data-stu-id="a2c53-430">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="a2c53-431">Um exemplo dessa situação seria uma matriz de armazenamento que pode ter portas de back-end para se comunicar com unidades de disco e portas de front-end para se comunicar com os hosts.</span><span class="sxs-lookup"><span data-stu-id="a2c53-431">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="a2c53-432">Se não houver nenhuma restrição sobre o uso da porta, o valor deverá ser definido como 4 (não restrito).</span><span class="sxs-lookup"><span data-stu-id="a2c53-432">If there is no restriction on the use of the port, then the value should be set to 4 (Not Restricted).</span></span> <span data-ttu-id="a2c53-433">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a2c53-433">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>



| <span data-ttu-id="a2c53-434">Valor</span><span class="sxs-lookup"><span data-stu-id="a2c53-434">Value</span></span>                                                                        | <span data-ttu-id="a2c53-435">Significado</span><span class="sxs-lookup"><span data-stu-id="a2c53-435">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="a2c53-436"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="a2c53-436"><dt>4</dt></span></span> </dl> | <span data-ttu-id="a2c53-437">Não restrito</span><span class="sxs-lookup"><span data-stu-id="a2c53-437">Not Restricted</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2c53-438">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2c53-438">Remarks</span></span>

<span data-ttu-id="a2c53-439">O acesso à **classe \_ SerialPort Msvm** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="a2c53-439">Access to the **Msvm\_SerialPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a2c53-440">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a2c53-440">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2c53-441">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2c53-441">Requirements</span></span>



| <span data-ttu-id="a2c53-442">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2c53-442">Requirement</span></span> | <span data-ttu-id="a2c53-443">Valor</span><span class="sxs-lookup"><span data-stu-id="a2c53-443">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2c53-444">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2c53-444">Minimum supported client</span></span><br/> | <span data-ttu-id="a2c53-445">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a2c53-445">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a2c53-446">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2c53-446">Minimum supported server</span></span><br/> | <span data-ttu-id="a2c53-447">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a2c53-447">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a2c53-448">Namespace</span><span class="sxs-lookup"><span data-stu-id="a2c53-448">Namespace</span></span><br/>                | <span data-ttu-id="a2c53-449">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="a2c53-449">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a2c53-450">MOF</span><span class="sxs-lookup"><span data-stu-id="a2c53-450">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2c53-451"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2c53-451"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2c53-452">DLL</span><span class="sxs-lookup"><span data-stu-id="a2c53-452">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2c53-453"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a2c53-453"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a2c53-454">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2c53-454">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2c53-455">**\_LOGICALPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="a2c53-455">**CIM\_LogicalPort**</span></span>](cim-logicalport.md)
</dt> <dt>

<span data-ttu-id="a2c53-456">[**\_LOGICALPORT CIM**](/previous-versions//cc136869(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a2c53-456">[**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a2c53-457">Classes de dispositivos seriais</span><span class="sxs-lookup"><span data-stu-id="a2c53-457">Serial Devices Classes</span></span>](serial-devices-classes.md)
</dt> </dl>

 

