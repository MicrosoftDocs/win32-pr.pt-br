---
description: Representa os recursos e o gerenciamento do controlador serial.
ms.assetid: 0F4DCF98-8EE4-4005-ADD5-BA23CB4CBE82
title: Classe Msvm_SerialController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialController
- Msvm_SerialController.SetPowerState
- Msvm_SerialController.EnableDevice
- Msvm_SerialController.OnlineDevice
- Msvm_SerialController.QuiesceDevice
- Msvm_SerialController.SaveProperties
- Msvm_SerialController.RestoreProperties
- Msvm_SerialController.InstanceID
- Msvm_SerialController.Caption
- Msvm_SerialController.Description
- Msvm_SerialController.ElementName
- Msvm_SerialController.InstallDate
- Msvm_SerialController.Name
- Msvm_SerialController.OperationalStatus
- Msvm_SerialController.StatusDescriptions
- Msvm_SerialController.Status
- Msvm_SerialController.HealthState
- Msvm_SerialController.CommunicationStatus
- Msvm_SerialController.DetailedStatus
- Msvm_SerialController.OperatingStatus
- Msvm_SerialController.PrimaryStatus
- Msvm_SerialController.EnabledState
- Msvm_SerialController.OtherEnabledState
- Msvm_SerialController.RequestedState
- Msvm_SerialController.EnabledDefault
- Msvm_SerialController.TimeOfLastStateChange
- Msvm_SerialController.AvailableRequestedStates
- Msvm_SerialController.TransitioningToState
- Msvm_SerialController.SystemCreationClassName
- Msvm_SerialController.SystemName
- Msvm_SerialController.CreationClassName
- Msvm_SerialController.DeviceID
- Msvm_SerialController.PowerManagementSupported
- Msvm_SerialController.PowerManagementCapabilities
- Msvm_SerialController.Availability
- Msvm_SerialController.StatusInfo
- Msvm_SerialController.LastErrorCode
- Msvm_SerialController.ErrorDescription
- Msvm_SerialController.ErrorCleared
- Msvm_SerialController.OtherIdentifyingInfo
- Msvm_SerialController.PowerOnHours
- Msvm_SerialController.TotalPowerOnHours
- Msvm_SerialController.IdentifyingDescriptions
- Msvm_SerialController.AdditionalAvailability
- Msvm_SerialController.MaxQuiesceTime
- Msvm_SerialController.TimeOfLastReset
- Msvm_SerialController.ProtocolSupported
- Msvm_SerialController.MaxNumberControlled
- Msvm_SerialController.ProtocolDescription
- Msvm_SerialController.Capabilities
- Msvm_SerialController.CapabilityDescriptions
- Msvm_SerialController.MaxBaudRate
- Msvm_SerialController.Security
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d3f1bbc9dabe078751d58875745a789895cb4c9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750025"
---
# <a name="msvm_serialcontroller-class"></a><span data-ttu-id="72241-103">\_Classe Msvm SerialController</span><span class="sxs-lookup"><span data-stu-id="72241-103">Msvm\_SerialController class</span></span>

<span data-ttu-id="72241-104">Representa os recursos e o gerenciamento do controlador serial.</span><span class="sxs-lookup"><span data-stu-id="72241-104">Represents the capabilities and management of the serial controller.</span></span> <span data-ttu-id="72241-105">Os controladores de série são dispositivos lógicos que estão sempre presentes em uma máquina virtual e, portanto, não são alocados por meio de um pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="72241-105">Serial controllers are logical devices that are always present in a virtual machine, and thus are not allocated through a resource pool.</span></span> <span data-ttu-id="72241-106">Uma instância do controlador serial está sempre presente em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="72241-106">One serial controller instance is always present in a virtual machine.</span></span> <span data-ttu-id="72241-107">Os controladores de série têm um número fixo de instâncias de porta.</span><span class="sxs-lookup"><span data-stu-id="72241-107">Serial controllers have a fixed number of port instances.</span></span> <span data-ttu-id="72241-108">Essa implementação dá suporte a duas portas por controlador.</span><span class="sxs-lookup"><span data-stu-id="72241-108">This implementation supports two ports per controller.</span></span>

> [!Note]  
> <span data-ttu-id="72241-109">Controladores de série são opcionais em [máquinas virtuais de geração 2](virtualization-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="72241-109">Serial controllers are optional in [generation 2 virtual machines](virtualization-glossary.md).</span></span>

 

<span data-ttu-id="72241-110">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="72241-110">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="72241-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72241-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialController : CIM_SerialController
{
  string   InstanceID;
  string   Caption = "Serial Controller";
  string   Description = "Microsoft Virtual Serial Controller";
  string   ElementName = "Serial Controller";
  datetime InstallDate;
  string   Name = "Serial Controller";
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
  string   CreationClassName = "Msvm_SerialController";
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
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 26;
  uint32   MaxNumberControlled = 2;
  string   ProtocolDescription;
  uint16   Capabilities[] = { 5 };
  string   CapabilityDescriptions[] = { "16550 compatible" };
  uint32   MaxBaudRate = 115200;
  uint16   Security = 3;
};
```

## <a name="members"></a><span data-ttu-id="72241-112">Membros</span><span class="sxs-lookup"><span data-stu-id="72241-112">Members</span></span>

<span data-ttu-id="72241-113">A classe **Msvm \_ SerialController** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="72241-113">The **Msvm\_SerialController** class has these types of members:</span></span>

-   [<span data-ttu-id="72241-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="72241-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="72241-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="72241-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="72241-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="72241-116">Methods</span></span>

<span data-ttu-id="72241-117">A classe **Msvm \_ SerialController** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="72241-117">The **Msvm\_SerialController** class has these methods.</span></span>



| <span data-ttu-id="72241-118">Método</span><span class="sxs-lookup"><span data-stu-id="72241-118">Method</span></span>                                                                 | <span data-ttu-id="72241-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="72241-119">Description</span></span>                              |
|:-----------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="72241-120">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="72241-120">**EnableDevice**</span></span>                                                       | <span data-ttu-id="72241-121">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="72241-121">This method is not supported.</span></span><br/> |
| <span data-ttu-id="72241-122">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="72241-122">**OnlineDevice**</span></span>                                                       | <span data-ttu-id="72241-123">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="72241-123">This method is not supported.</span></span><br/> |
| <span data-ttu-id="72241-124">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="72241-124">**QuiesceDevice**</span></span>                                                      | <span data-ttu-id="72241-125">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="72241-125">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="72241-126">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="72241-126">**RequestStateChange**</span></span>](msvm-serialcontroller-requeststatechange.md) | <span data-ttu-id="72241-127">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="72241-127">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="72241-128">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="72241-128">**Reset**</span></span>](msvm-serialcontroller-reset.md)                           | <span data-ttu-id="72241-129">Redefine o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72241-129">Resets the device.</span></span><br/>            |
| <span data-ttu-id="72241-130">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="72241-130">**RestoreProperties**</span></span>                                                  | <span data-ttu-id="72241-131">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="72241-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="72241-132">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="72241-132">**SaveProperties**</span></span>                                                     | <span data-ttu-id="72241-133">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="72241-133">This method is not supported.</span></span><br/> |
| <span data-ttu-id="72241-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="72241-134">**SetPowerState**</span></span>                                                      | <span data-ttu-id="72241-135">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="72241-135">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="72241-136">Propriedades</span><span class="sxs-lookup"><span data-stu-id="72241-136">Properties</span></span>

<span data-ttu-id="72241-137">A classe **Msvm \_ SerialController** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="72241-137">The **Msvm\_SerialController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="72241-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="72241-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-139">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72241-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="72241-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-141">Qualquer disponibilidade e status adicionais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72241-141">Any additional availability and status of the device.</span></span> <span data-ttu-id="72241-142">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="72241-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="72241-143">Valor</span><span class="sxs-lookup"><span data-stu-id="72241-143">Value</span></span>                                                                            | <span data-ttu-id="72241-144">Significado</span><span class="sxs-lookup"><span data-stu-id="72241-144">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="72241-145"><dt>152</dt></span><span class="sxs-lookup"><span data-stu-id="72241-145"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="72241-146"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="72241-146"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="72241-147">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="72241-147">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="72241-148">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="72241-148">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-149">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72241-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72241-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-151">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72241-151">The primary availability and status of the device.</span></span> <span data-ttu-id="72241-152">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="72241-152">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="72241-153">Valor</span><span class="sxs-lookup"><span data-stu-id="72241-153">Value</span></span>                                                                        | <span data-ttu-id="72241-154">Significado</span><span class="sxs-lookup"><span data-stu-id="72241-154">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="72241-155"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="72241-155"><dt>6</dt></span></span> </dl> | <span data-ttu-id="72241-156">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="72241-156">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="72241-157">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="72241-157">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-158">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72241-158">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="72241-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-160">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="72241-160">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="72241-161">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="72241-161">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="72241-162">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="72241-162">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-163">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72241-163">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="72241-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-165">O buffer e outros recursos do controlador serial que podem ser inerentes ao hardware do chip.</span><span class="sxs-lookup"><span data-stu-id="72241-165">The buffering and other capabilities of the serial controller that might be inherent in the chip hardware.</span></span> <span data-ttu-id="72241-166">Essa propriedade é herdada do [**CIM \_ SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span><span class="sxs-lookup"><span data-stu-id="72241-166">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="72241-167">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="72241-167">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-168">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="72241-168">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="72241-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-170">Uma matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para qualquer um dos recursos do controlador serial que são indicados na matriz **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="72241-170">An array of free-form strings that provides more detailed explanations for any of the serial controller features that are indicated in the **Capabilities** array.</span></span> <span data-ttu-id="72241-171">Essa propriedade é herdada do [**CIM \_ SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span><span class="sxs-lookup"><span data-stu-id="72241-171">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="72241-172">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="72241-172">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-173">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="72241-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72241-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-175">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="72241-175">A short description of the object.</span></span> <span data-ttu-id="72241-176">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="72241-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="72241-177">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="72241-177">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-178">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72241-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72241-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-180">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="72241-180">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="72241-181">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="72241-181">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="72241-182">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="72241-182">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="72241-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="72241-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="72241-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="72241-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="72241-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="72241-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="72241-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="72241-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="72241-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="72241-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="72241-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="72241-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="72241-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="72241-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="72241-190">)</span><span class="sxs-lookup"><span data-stu-id="72241-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="72241-191">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="72241-191">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="72241-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72241-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-194">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="72241-194">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="72241-195">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="72241-195">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="72241-196">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="72241-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-197">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="72241-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72241-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-199">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="72241-199">A description of the object.</span></span> <span data-ttu-id="72241-200">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="72241-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="72241-201">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="72241-201">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-202">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72241-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72241-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-204">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="72241-204">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="72241-205">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="72241-205">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="72241-206">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="72241-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="72241-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="72241-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="72241-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="72241-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="72241-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="72241-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="72241-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="72241-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="72241-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="72241-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="72241-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="72241-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="72241-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="72241-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="72241-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="72241-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="72241-215">)</span><span class="sxs-lookup"><span data-stu-id="72241-215">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="72241-216">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="72241-216">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-217">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="72241-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72241-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-219">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como "Microsoft: *<GUID>* ".</span><span class="sxs-lookup"><span data-stu-id="72241-219">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*<GUID>*".</span></span>

</dd> <dt>

<span data-ttu-id="72241-220">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="72241-220">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-221">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="72241-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72241-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-223">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="72241-223">A display name for the object.</span></span> <span data-ttu-id="72241-224">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="72241-224">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="72241-225">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="72241-225">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-226">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72241-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72241-227">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-228">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="72241-228">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="72241-229">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="72241-229">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="72241-230">Valor</span><span class="sxs-lookup"><span data-stu-id="72241-230">Value</span></span>                                                                        | <span data-ttu-id="72241-231">Significado</span><span class="sxs-lookup"><span data-stu-id="72241-231">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="72241-232"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="72241-232"><dt>2</dt></span></span> </dl> | <span data-ttu-id="72241-233">habilitado</span><span class="sxs-lookup"><span data-stu-id="72241-233">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="72241-234">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="72241-234">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-235">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72241-235">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72241-236">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-237">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="72241-237">The enabled and disabled states of an element.</span></span> <span data-ttu-id="72241-238">Ele também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="72241-238">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="72241-239">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="72241-239">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="72241-240">Valor</span><span class="sxs-lookup"><span data-stu-id="72241-240">Value</span></span>                                                                        | <span data-ttu-id="72241-241">Significado</span><span class="sxs-lookup"><span data-stu-id="72241-241">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="72241-242"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="72241-242"><dt>5</dt></span></span> </dl> | <span data-ttu-id="72241-243">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="72241-243">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="72241-244">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="72241-244">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-245">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="72241-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="72241-246">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-247">Indica se o erro relatado na propriedade **LastErrorCode** agora está apagado.</span><span class="sxs-lookup"><span data-stu-id="72241-247">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="72241-248">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="72241-248">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="72241-249">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="72241-249">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-250">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="72241-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72241-251">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-252">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado na propriedade **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="72241-252">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="72241-253">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="72241-253">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="72241-254">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="72241-254">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-255">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72241-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72241-256">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-257">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="72241-257">The current health of the element.</span></span> <span data-ttu-id="72241-258">Isso expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="72241-258">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="72241-259">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="72241-259">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="72241-260">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="72241-260">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="72241-261">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="72241-261">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-262">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="72241-262">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="72241-263">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-264">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz de propriedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="72241-264">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="72241-265">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="72241-265">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="72241-266">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="72241-266">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-267">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="72241-267">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="72241-268">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-269">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="72241-269">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="72241-270">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="72241-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="72241-271">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="72241-271">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-272">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="72241-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72241-273">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72241-274">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="72241-274">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="72241-275">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="72241-275">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="72241-276">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="72241-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="72241-277">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="72241-277">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-278">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72241-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72241-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-280">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="72241-280">The last error code reported by the logical device.</span></span> <span data-ttu-id="72241-281">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="72241-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="72241-282">**MaxBaudRate**</span><span class="sxs-lookup"><span data-stu-id="72241-282">**MaxBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-283">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72241-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72241-284">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-285">A taxa de transmissão máxima, em bits por segundo, com suporte do controlador serial.</span><span class="sxs-lookup"><span data-stu-id="72241-285">The maximum baud rate, in bits per second, that is supported by the serial controller.</span></span> <span data-ttu-id="72241-286">Essa propriedade é herdada do [**CIM \_ SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span><span class="sxs-lookup"><span data-stu-id="72241-286">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="72241-287">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="72241-287">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-288">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72241-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72241-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-290">O número máximo de entidades diretamente endereçáveis que são suportadas por este controlador.</span><span class="sxs-lookup"><span data-stu-id="72241-290">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="72241-291">Um valor de 0 deve ser usado se o número for desconhecido ou ilimitado.</span><span class="sxs-lookup"><span data-stu-id="72241-291">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="72241-292">O protocolo usado pelo controlador para acessar dispositivos controlados.</span><span class="sxs-lookup"><span data-stu-id="72241-292">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="72241-293">Essa propriedade é herdada [**do \_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="72241-293">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="72241-294">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="72241-294">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-295">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="72241-295">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="72241-296">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-297">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="72241-297">This property has been deprecated.</span></span> <span data-ttu-id="72241-298">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="72241-298">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="72241-299">**Nome**</span><span class="sxs-lookup"><span data-stu-id="72241-299">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-300">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="72241-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72241-301">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-302">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="72241-302">The label by which the object is known.</span></span> <span data-ttu-id="72241-303">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é a mesma que a propriedade **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="72241-303">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="72241-304">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="72241-304">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-305">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72241-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72241-306">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-307">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="72241-307">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="72241-308">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="72241-308">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="72241-309">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="72241-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="72241-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="72241-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="72241-311"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="72241-311"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="72241-312"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="72241-312"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="72241-313"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="72241-313"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="72241-314"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="72241-314"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="72241-315"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="72241-315"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="72241-316"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="72241-316"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="72241-317"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="72241-317"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="72241-318"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="72241-318"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="72241-319"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="72241-319"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="72241-320"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="72241-320"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="72241-321"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="72241-321"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="72241-322"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="72241-322"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="72241-323"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="72241-323"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="72241-324"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="72241-324"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="72241-325"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="72241-325"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="72241-326"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="72241-326"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="72241-327"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="72241-327"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="72241-328"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="72241-328"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="72241-329">)</span><span class="sxs-lookup"><span data-stu-id="72241-329">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="72241-330">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="72241-330">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-331">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72241-331">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="72241-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-333">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="72241-333">The current statuses of the object.</span></span> <span data-ttu-id="72241-334">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="72241-334">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="72241-335">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="72241-335">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-336">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="72241-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72241-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-338">O estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="72241-338">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="72241-339">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="72241-339">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="72241-340">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="72241-340">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="72241-341">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="72241-341">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-342">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="72241-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="72241-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-344">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="72241-344">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="72241-345">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="72241-345">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="72241-346">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="72241-346">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-347">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72241-347">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="72241-348">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-349">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72241-349">The power management capabilities of the device.</span></span> <span data-ttu-id="72241-350">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="72241-350">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="72241-351">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="72241-351">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-352">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="72241-352">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="72241-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-354">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="72241-354">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="72241-355">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="72241-355">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="72241-356">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="72241-356">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-357">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="72241-357">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="72241-358">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-359">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="72241-359">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="72241-360">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="72241-360">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="72241-361">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="72241-361">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-362">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72241-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72241-363">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-364">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="72241-364">Provides high level status information.</span></span> <span data-ttu-id="72241-365">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="72241-365">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="72241-366">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="72241-366">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="72241-367">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="72241-367">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="72241-368"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="72241-368"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="72241-369"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="72241-369"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="72241-370"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="72241-370"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="72241-371"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="72241-371"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="72241-372"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="72241-372"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="72241-373"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="72241-373"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="72241-374">)</span><span class="sxs-lookup"><span data-stu-id="72241-374">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="72241-375">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="72241-375">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-376">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="72241-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72241-377">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-378">Uma cadeia de caracteres que fornece mais informações relacionadas ao protocolo suportado pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="72241-378">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="72241-379">Essa propriedade é herdada [**do \_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="72241-379">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="72241-380">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="72241-380">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-381">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72241-381">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72241-382">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-383">O protocolo usado pelo controlador para acessar dispositivos controlados.</span><span class="sxs-lookup"><span data-stu-id="72241-383">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="72241-384">Essa propriedade é herdada [**do \_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="72241-384">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>



| <span data-ttu-id="72241-385">Valor</span><span class="sxs-lookup"><span data-stu-id="72241-385">Value</span></span>                                                                         | <span data-ttu-id="72241-386">Significado</span><span class="sxs-lookup"><span data-stu-id="72241-386">Meaning</span></span>             |
|-------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="72241-387"><dt>26</dt></span><span class="sxs-lookup"><span data-stu-id="72241-387"><dt>26</dt></span></span> </dl> | <span data-ttu-id="72241-388">IEEE-488</span><span class="sxs-lookup"><span data-stu-id="72241-388">IEEE-488</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="72241-389">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="72241-389">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-390">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72241-390">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72241-391">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-392">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="72241-392">The last requested or desired state for the element.</span></span> <span data-ttu-id="72241-393">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="72241-393">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="72241-394">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="72241-394">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="72241-395">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="72241-395">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="72241-396">Valor</span><span class="sxs-lookup"><span data-stu-id="72241-396">Value</span></span>                                                                         | <span data-ttu-id="72241-397">Significado</span><span class="sxs-lookup"><span data-stu-id="72241-397">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="72241-398"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="72241-398"><dt>12</dt></span></span> </dl> | <span data-ttu-id="72241-399">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="72241-399">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="72241-400">**Segurança**</span><span class="sxs-lookup"><span data-stu-id="72241-400">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-401">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72241-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72241-402">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-403">A segurança operacional para o controlador.</span><span class="sxs-lookup"><span data-stu-id="72241-403">The operational security for the controller.</span></span> <span data-ttu-id="72241-404">Essa propriedade é herdada do [**CIM \_ SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span><span class="sxs-lookup"><span data-stu-id="72241-404">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>



| <span data-ttu-id="72241-405">Valor</span><span class="sxs-lookup"><span data-stu-id="72241-405">Value</span></span>                                                                        | <span data-ttu-id="72241-406">Significado</span><span class="sxs-lookup"><span data-stu-id="72241-406">Meaning</span></span>         |
|------------------------------------------------------------------------------|-----------------|
| <dl> <span data-ttu-id="72241-407"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="72241-407"><dt>3</dt></span></span> </dl> | <span data-ttu-id="72241-408">Nenhum</span><span class="sxs-lookup"><span data-stu-id="72241-408">None</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="72241-409">**Status**</span><span class="sxs-lookup"><span data-stu-id="72241-409">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-410">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="72241-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72241-411">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-412">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="72241-412">The current status of the object.</span></span> <span data-ttu-id="72241-413">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="72241-413">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="72241-414">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="72241-414">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-415">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="72241-415">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="72241-416">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-417">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="72241-417">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="72241-418">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="72241-418">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="72241-419">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="72241-419">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-420">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72241-420">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72241-421">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-422">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="72241-422">The current state of the logical device.</span></span> <span data-ttu-id="72241-423">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="72241-423">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="72241-424">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="72241-424">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-425">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="72241-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72241-426">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-427">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="72241-427">The scoping system's creation class name.</span></span> <span data-ttu-id="72241-428">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="72241-428">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="72241-429">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="72241-429">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-430">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="72241-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72241-431">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-432">O identificador exclusivo para a máquina virtual de escopo.</span><span class="sxs-lookup"><span data-stu-id="72241-432">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="72241-433">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="72241-433">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="72241-434">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="72241-434">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-435">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="72241-435">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="72241-436">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-437">A última vez em que o controlador estava ligado.</span><span class="sxs-lookup"><span data-stu-id="72241-437">The last time the controller was powered on.</span></span> <span data-ttu-id="72241-438">Essa propriedade é herdada [**do \_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="72241-438">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="72241-439">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="72241-439">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-440">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="72241-440">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="72241-441">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-442">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="72241-442">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="72241-443">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="72241-443">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="72241-444">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="72241-444">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-445">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="72241-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="72241-446">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-447">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="72241-447">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="72241-448">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="72241-448">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="72241-449">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="72241-449">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72241-450">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72241-450">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72241-451">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72241-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72241-452">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="72241-452">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="72241-453">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="72241-453">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72241-454">Comentários</span><span class="sxs-lookup"><span data-stu-id="72241-454">Remarks</span></span>

<span data-ttu-id="72241-455">O acesso à classe **Msvm \_ SerialController** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="72241-455">Access to the **Msvm\_SerialController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="72241-456">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="72241-456">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="72241-457">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72241-457">Requirements</span></span>



| <span data-ttu-id="72241-458">Requisito</span><span class="sxs-lookup"><span data-stu-id="72241-458">Requirement</span></span> | <span data-ttu-id="72241-459">Valor</span><span class="sxs-lookup"><span data-stu-id="72241-459">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72241-460">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72241-460">Minimum supported client</span></span><br/> | <span data-ttu-id="72241-461">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="72241-461">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="72241-462">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72241-462">Minimum supported server</span></span><br/> | <span data-ttu-id="72241-463">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="72241-463">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="72241-464">Namespace</span><span class="sxs-lookup"><span data-stu-id="72241-464">Namespace</span></span><br/>                | <span data-ttu-id="72241-465">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="72241-465">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="72241-466">MOF</span><span class="sxs-lookup"><span data-stu-id="72241-466">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72241-467"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72241-467"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="72241-468">DLL</span><span class="sxs-lookup"><span data-stu-id="72241-468">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72241-469"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="72241-469"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="72241-470">Confira também</span><span class="sxs-lookup"><span data-stu-id="72241-470">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72241-471">**\_SERIALCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="72241-471">**CIM\_SerialController**</span></span>](cim-serialcontroller.md)
</dt> <dt>

[<span data-ttu-id="72241-472">**\_SERIALCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="72241-472">**CIM\_SerialController**</span></span>](/windows/desktop/CIMWin32Prov/cim-serialcontroller)
</dt> <dt>

[<span data-ttu-id="72241-473">Classes de dispositivos seriais</span><span class="sxs-lookup"><span data-stu-id="72241-473">Serial Devices Classes</span></span>](serial-devices-classes.md)
</dt> </dl>

 

