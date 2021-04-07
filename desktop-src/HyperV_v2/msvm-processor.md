---
description: Representa o processador virtual em uma máquina virtual.
ms.assetid: 4BA91C44-0F85-42D1-A8B5-147E1D532FB5
title: Classe Msvm_Processor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Processor
- Msvm_Processor.SetPowerState
- Msvm_Processor.EnableDevice
- Msvm_Processor.OnlineDevice
- Msvm_Processor.QuiesceDevice
- Msvm_Processor.SaveProperties
- Msvm_Processor.RestoreProperties
- Msvm_Processor.InstanceID
- Msvm_Processor.Caption
- Msvm_Processor.Description
- Msvm_Processor.ElementName
- Msvm_Processor.InstallDate
- Msvm_Processor.Name
- Msvm_Processor.OperationalStatus
- Msvm_Processor.StatusDescriptions
- Msvm_Processor.Status
- Msvm_Processor.HealthState
- Msvm_Processor.CommunicationStatus
- Msvm_Processor.DetailedStatus
- Msvm_Processor.OperatingStatus
- Msvm_Processor.PrimaryStatus
- Msvm_Processor.EnabledState
- Msvm_Processor.OtherEnabledState
- Msvm_Processor.RequestedState
- Msvm_Processor.EnabledDefault
- Msvm_Processor.TimeOfLastStateChange
- Msvm_Processor.AvailableRequestedStates
- Msvm_Processor.TransitioningToState
- Msvm_Processor.SystemCreationClassName
- Msvm_Processor.SystemName
- Msvm_Processor.CreationClassName
- Msvm_Processor.DeviceID
- Msvm_Processor.PowerManagementSupported
- Msvm_Processor.PowerManagementCapabilities
- Msvm_Processor.Availability
- Msvm_Processor.StatusInfo
- Msvm_Processor.LastErrorCode
- Msvm_Processor.ErrorDescription
- Msvm_Processor.ErrorCleared
- Msvm_Processor.OtherIdentifyingInfo
- Msvm_Processor.PowerOnHours
- Msvm_Processor.TotalPowerOnHours
- Msvm_Processor.IdentifyingDescriptions
- Msvm_Processor.AdditionalAvailability
- Msvm_Processor.MaxQuiesceTime
- Msvm_Processor.Role
- Msvm_Processor.Family
- Msvm_Processor.OtherFamilyDescription
- Msvm_Processor.UpgradeMethod
- Msvm_Processor.MaxClockSpeed
- Msvm_Processor.CurrentClockSpeed
- Msvm_Processor.DataWidth
- Msvm_Processor.AddressWidth
- Msvm_Processor.LoadPercentage
- Msvm_Processor.Stepping
- Msvm_Processor.UniqueID
- Msvm_Processor.CPUStatus
- Msvm_Processor.ExternalBusClockSpeed
- Msvm_Processor.LoadPercentageHistory
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 14ed1e2bbb9e15f89376234da8981faffb1a6809
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828594"
---
# <a name="msvm_processor-class"></a><span data-ttu-id="5c410-103">\_Classe de processador Msvm</span><span class="sxs-lookup"><span data-stu-id="5c410-103">Msvm\_Processor class</span></span>

<span data-ttu-id="5c410-104">Representa o processador virtual em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5c410-104">Represents the virtual processor in a virtual machine.</span></span>

<span data-ttu-id="5c410-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5c410-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c410-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c410-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Processor : CIM_Processor
{
  string   InstanceID;
  string   Caption = "Processor";
  string   Description = " A logical processor of the hypervisor running on the host computer system.";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 2;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_Processor";
  string   DeviceID = "Microsoft:GUID\device specific data";
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
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  string   Role = "Central Processor";
  uint16   Family;
  string   OtherFamilyDescription;
  uint16   UpgradeMethod;
  uint32   MaxClockSpeed;
  uint32   CurrentClockSpeed;
  uint16   DataWidth;
  uint16   AddressWidth;
  uint16   LoadPercentage;
  string   Stepping;
  string   UniqueID;
  uint16   CPUStatus;
  uint32   ExternalBusClockSpeed;
  uint16   LoadPercentageHistory[];
};
```

## <a name="members"></a><span data-ttu-id="5c410-107">Membros</span><span class="sxs-lookup"><span data-stu-id="5c410-107">Members</span></span>

<span data-ttu-id="5c410-108">A classe de **\_ processador Msvm** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5c410-108">The **Msvm\_Processor** class has these types of members:</span></span>

-   [<span data-ttu-id="5c410-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5c410-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="5c410-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5c410-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5c410-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="5c410-111">Methods</span></span>

<span data-ttu-id="5c410-112">A classe de **\_ processador Msvm** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5c410-112">The **Msvm\_Processor** class has these methods.</span></span>



| <span data-ttu-id="5c410-113">Método</span><span class="sxs-lookup"><span data-stu-id="5c410-113">Method</span></span>                                                          | <span data-ttu-id="5c410-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5c410-114">Description</span></span>                              |
|:----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="5c410-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="5c410-115">**EnableDevice**</span></span>                                                | <span data-ttu-id="5c410-116">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="5c410-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="5c410-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="5c410-117">**OnlineDevice**</span></span>                                                | <span data-ttu-id="5c410-118">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="5c410-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="5c410-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="5c410-119">**QuiesceDevice**</span></span>                                               | <span data-ttu-id="5c410-120">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="5c410-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="5c410-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="5c410-121">**RequestStateChange**</span></span>](msvm-processor-requeststatechange.md) | <span data-ttu-id="5c410-122">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="5c410-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="5c410-123">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="5c410-123">**Reset**</span></span>](msvm-processor-reset.md)                           | <span data-ttu-id="5c410-124">Redefine o dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="5c410-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="5c410-125">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="5c410-125">**RestoreProperties**</span></span>                                           | <span data-ttu-id="5c410-126">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="5c410-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="5c410-127">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="5c410-127">**SaveProperties**</span></span>                                              | <span data-ttu-id="5c410-128">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="5c410-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="5c410-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="5c410-129">**SetPowerState**</span></span>                                               | <span data-ttu-id="5c410-130">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="5c410-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5c410-131">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5c410-131">Properties</span></span>

<span data-ttu-id="5c410-132">A classe de **\_ processador Msvm** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5c410-132">The **Msvm\_Processor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c410-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="5c410-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-134">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c410-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5c410-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-136">Qualquer disponibilidade e status adicionais do dispositivo, além do especificado na propriedade de **disponibilidade** .</span><span class="sxs-lookup"><span data-stu-id="5c410-136">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="5c410-137">A propriedade de **disponibilidade** denota o status primário e a disponibilidade do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c410-137">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="5c410-138">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="5c410-138">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-139">**AddressWidth**</span><span class="sxs-lookup"><span data-stu-id="5c410-139">**AddressWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-140">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c410-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-142">A largura do endereço do processador, em bits.</span><span class="sxs-lookup"><span data-stu-id="5c410-142">The processor address width, in bits.</span></span> <span data-ttu-id="5c410-143">Essa propriedade é herdada [**do \_ processador CIM**](/windows/desktop/CIMWin32Prov/cim-processor)e o valor é 32 ou 64, dependendo das características da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5c410-143">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and the value is either 32 or 64, depending on the characteristics of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="5c410-144">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="5c410-144">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-145">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c410-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-147">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c410-147">The primary availability and status of the device.</span></span> <span data-ttu-id="5c410-148">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="5c410-148">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c410-149">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="5c410-149">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-150">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c410-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5c410-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-152">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="5c410-152">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="5c410-153">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5c410-153">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5c410-154">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="5c410-154">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5c410-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c410-157">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="5c410-157">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="5c410-158">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="5c410-158">A short description of the object.</span></span> <span data-ttu-id="5c410-159">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5c410-159">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-160">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="5c410-160">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-161">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c410-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-163">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="5c410-163">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="5c410-164">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="5c410-164">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5c410-165">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5c410-165">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5c410-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="5c410-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-167"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="5c410-167"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-168"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="5c410-168"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-169"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="5c410-169"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-170"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="5c410-170"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-171"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="5c410-171"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-172"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5c410-172"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5c410-173">)</span><span class="sxs-lookup"><span data-stu-id="5c410-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5c410-174">**CPUStatus**</span><span class="sxs-lookup"><span data-stu-id="5c410-174">**CPUStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-175">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c410-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-177">O status atual do processador.</span><span class="sxs-lookup"><span data-stu-id="5c410-177">The current status of the processor.</span></span> <span data-ttu-id="5c410-178">Essa propriedade é herdada [**do \_ processador CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="5c410-178">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-179">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5c410-179">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5c410-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c410-182">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="5c410-182">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="5c410-183">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="5c410-183">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5c410-184">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="5c410-184">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="5c410-185">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="5c410-185">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-186">**CurrentClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="5c410-186">**CurrentClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-187">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c410-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-189">A velocidade máxima do processador físico, levando em conta a capacidade para o processador virtual.</span><span class="sxs-lookup"><span data-stu-id="5c410-189">The maximum speed of the physical processor, taking into account the capacity for the virtual processor.</span></span> <span data-ttu-id="5c410-190">Essa propriedade é herdada [**do \_ processador CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="5c410-190">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-191">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="5c410-191">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-192">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c410-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-194">A largura dos dados do processador, em bits.</span><span class="sxs-lookup"><span data-stu-id="5c410-194">The processor data width, in bits.</span></span> <span data-ttu-id="5c410-195">Essa propriedade é herdada [**do \_ processador CIM**](/windows/desktop/CIMWin32Prov/cim-processor)e o valor é 32 ou 64, dependendo das características da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5c410-195">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and the value is either 32 or 64, depending on the characteristics of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="5c410-196">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5c410-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-197">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5c410-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-199">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="5c410-199">A description of the object.</span></span> <span data-ttu-id="5c410-200">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5c410-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-201">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="5c410-201">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-202">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c410-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-204">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="5c410-204">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="5c410-205">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="5c410-205">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5c410-206">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5c410-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5c410-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="5c410-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="5c410-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="5c410-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="5c410-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="5c410-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="5c410-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="5c410-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5c410-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5c410-215">)</span><span class="sxs-lookup"><span data-stu-id="5c410-215">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5c410-216">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="5c410-216">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-217">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5c410-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-219">Um endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5c410-219">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="5c410-220">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como "Microsoft:*GUID* \\ *specific data específico*".</span><span class="sxs-lookup"><span data-stu-id="5c410-220">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*\\*device specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="5c410-221">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5c410-221">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-222">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5c410-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-223">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-224">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="5c410-224">A display name for the object.</span></span> <span data-ttu-id="5c410-225">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5c410-225">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-226">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="5c410-226">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-227">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c410-227">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-229">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="5c410-229">An administrator's default or startup configuration for the Enabled State of an element.</span></span> <span data-ttu-id="5c410-230">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5c410-230">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-231">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="5c410-231">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-232">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c410-232">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-234">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="5c410-234">The enabled and disabled states of an element.</span></span> <span data-ttu-id="5c410-235">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5c410-235">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-236">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="5c410-236">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-237">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5c410-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-239">Indica se o erro relatado em **LastErrorCode** agora está limpo.</span><span class="sxs-lookup"><span data-stu-id="5c410-239">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="5c410-240">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="5c410-240">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c410-241">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="5c410-241">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-242">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5c410-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-243">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-244">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="5c410-244">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="5c410-245">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="5c410-245">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c410-246">**ExternalBusClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="5c410-246">**ExternalBusClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-247">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c410-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-249">A velocidade de relógio do barramento externo do processador físico subjacente.</span><span class="sxs-lookup"><span data-stu-id="5c410-249">The external bus clock speed of the underlying physical processor.</span></span> <span data-ttu-id="5c410-250">Essa propriedade é herdada [**do \_ processador CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="5c410-250">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-251">**Família**</span><span class="sxs-lookup"><span data-stu-id="5c410-251">**Family**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-252">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c410-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-253">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-254">A família de processadores do processador físico subjacente.</span><span class="sxs-lookup"><span data-stu-id="5c410-254">The processor family of the underlying physical processor.</span></span> <span data-ttu-id="5c410-255">Essa propriedade é herdada [**do \_ processador CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="5c410-255">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-256">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="5c410-256">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-257">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c410-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-259">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="5c410-259">The current health of the element.</span></span> <span data-ttu-id="5c410-260">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5c410-260">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-261">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="5c410-261">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-262">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5c410-262">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5c410-263">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-264">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz [**OtherIdentifyingInfo**](msvm-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="5c410-264">An array of free-form strings that provide explanations and details behind the entries in the [**OtherIdentifyingInfo**](msvm-keyboard.md) array.</span></span> <span data-ttu-id="5c410-265">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5c410-265">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5c410-266">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5c410-266">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-267">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5c410-267">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-268">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-269">A data e a hora em que a máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="5c410-269">The date and time when the virtual machine was created.</span></span> <span data-ttu-id="5c410-270">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5c410-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-271">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5c410-271">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-272">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5c410-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-273">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c410-274">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="5c410-274">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5c410-275">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="5c410-275">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5c410-276">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5c410-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-277">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5c410-277">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-278">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c410-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-280">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5c410-280">The last error code reported by the logical device.</span></span> <span data-ttu-id="5c410-281">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="5c410-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c410-282">**Loadpercentual**</span><span class="sxs-lookup"><span data-stu-id="5c410-282">**LoadPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-283">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c410-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-284">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-285">A porcentagem atual da capacidade total de processamento consumida pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5c410-285">The current percentage of the total processing power being consumed by the virtual machine.</span></span> <span data-ttu-id="5c410-286">Essa propriedade é herdada [**do \_ processador CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="5c410-286">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-287">**LoadPercentageHistory**</span><span class="sxs-lookup"><span data-stu-id="5c410-287">**LoadPercentageHistory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-288">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c410-288">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5c410-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c410-290">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="5c410-290">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="5c410-291">O histórico registrado de percentual da potência de processamento total consumida pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5c410-291">The recorded history of percentage of the total processing power being consumed by the virtual machine.</span></span> <span data-ttu-id="5c410-292">Esta é uma matriz que contém exemplos.</span><span class="sxs-lookup"><span data-stu-id="5c410-292">This is an array containing samples.</span></span>

</dd> <dt>

<span data-ttu-id="5c410-293">**MaxClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="5c410-293">**MaxClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-294">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c410-294">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-296">A velocidade máxima do relógio, em megahertz, do processador virtual.</span><span class="sxs-lookup"><span data-stu-id="5c410-296">The maximum clock speed, in megahertz, of the virtual processor.</span></span> <span data-ttu-id="5c410-297">Essa propriedade é herdada [**do \_ processador CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="5c410-297">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-298">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="5c410-298">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-299">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5c410-299">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-300">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-301">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="5c410-301">This property has been deprecated.</span></span> <span data-ttu-id="5c410-302">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="5c410-302">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c410-303">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5c410-303">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-304">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5c410-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-305">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c410-306">Qualificadores: **maxlen** (1024)</span><span class="sxs-lookup"><span data-stu-id="5c410-306">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="5c410-307">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="5c410-307">The label by which the object is known.</span></span> <span data-ttu-id="5c410-308">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="5c410-308">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="5c410-309">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5c410-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-310">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="5c410-310">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-311">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c410-311">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-312">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-313">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="5c410-313">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="5c410-314">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="5c410-314">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5c410-315">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5c410-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5c410-316"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="5c410-316"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-317"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="5c410-317"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-318"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="5c410-318"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-319"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="5c410-319"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-320"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="5c410-320"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-321"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="5c410-321"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-322"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="5c410-322"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-323"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="5c410-323"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-324"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="5c410-324"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-325"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="5c410-325"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-326"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="5c410-326"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-327"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="5c410-327"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-328"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="5c410-328"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-329"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="5c410-329"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-330"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="5c410-330"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-331"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="5c410-331"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-332"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="5c410-332"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="5c410-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5c410-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5c410-335">)</span><span class="sxs-lookup"><span data-stu-id="5c410-335">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5c410-336">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="5c410-336">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-337">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c410-337">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5c410-338">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-339">O status atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="5c410-339">The current status of the element.</span></span> <span data-ttu-id="5c410-340">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5c410-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-341">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="5c410-341">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-342">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5c410-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-344">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="5c410-344">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="5c410-345">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="5c410-345">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="5c410-346">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5c410-346">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-347">**OtherFamilyDescription**</span><span class="sxs-lookup"><span data-stu-id="5c410-347">**OtherFamilyDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-348">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5c410-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-349">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-350">Uma descrição do tipo de família de processador.</span><span class="sxs-lookup"><span data-stu-id="5c410-350">A description of the processor family type.</span></span> <span data-ttu-id="5c410-351">Essa propriedade é herdada [**do \_ processador CIM**](/windows/desktop/CIMWin32Prov/cim-processor)e sempre é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5c410-351">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5c410-352">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="5c410-352">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-353">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5c410-353">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5c410-354">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-355">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5c410-355">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="5c410-356">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="5c410-356">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-357">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="5c410-357">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-358">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c410-358">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5c410-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-360">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c410-360">The power management capabilities of the device.</span></span> <span data-ttu-id="5c410-361">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="5c410-361">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c410-362">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="5c410-362">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-363">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5c410-363">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-364">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-365">Indica se o gerenciamento de energia tem suporte no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c410-365">Indicates whether power management is supported on the device.</span></span> <span data-ttu-id="5c410-366">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="5c410-366">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c410-367">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="5c410-367">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-368">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5c410-368">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-369">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-370">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="5c410-370">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="5c410-371">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="5c410-371">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c410-372">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="5c410-372">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-373">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c410-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-374">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-375">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="5c410-375">Provides high level status information.</span></span> <span data-ttu-id="5c410-376">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="5c410-376">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="5c410-377">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="5c410-377">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5c410-378">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5c410-378">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5c410-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="5c410-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-380"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="5c410-380"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="5c410-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-382"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="5c410-382"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-383"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="5c410-383"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5c410-384"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5c410-384"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5c410-385">)</span><span class="sxs-lookup"><span data-stu-id="5c410-385">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5c410-386">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="5c410-386">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-387">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c410-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-389">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="5c410-389">The last requested or desired state for the element.</span></span> <span data-ttu-id="5c410-390">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5c410-390">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-391">**Função**</span><span class="sxs-lookup"><span data-stu-id="5c410-391">**Role**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-392">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5c410-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-393">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-394">Uma cadeia de caracteres que descreve a função do processador.</span><span class="sxs-lookup"><span data-stu-id="5c410-394">A string that describes the role of the processor.</span></span> <span data-ttu-id="5c410-395">Por exemplo, "processador central" ou "processador matemático".</span><span class="sxs-lookup"><span data-stu-id="5c410-395">For example, "Central Processor" or "Math Processor".</span></span> <span data-ttu-id="5c410-396">Essa propriedade é herdada [**do \_ processador CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="5c410-396">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-397">**Status**</span><span class="sxs-lookup"><span data-stu-id="5c410-397">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-398">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5c410-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-399">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-400">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5c410-400">The current status of the object.</span></span> <span data-ttu-id="5c410-401">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="5c410-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c410-402">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="5c410-402">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-403">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5c410-403">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5c410-404">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-405">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="5c410-405">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="5c410-406">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5c410-406">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-407">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="5c410-407">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-408">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c410-408">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-409">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-410">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5c410-410">The current state of the logical device.</span></span> <span data-ttu-id="5c410-411">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="5c410-411">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c410-412">**Depuração**</span><span class="sxs-lookup"><span data-stu-id="5c410-412">**Stepping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-413">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5c410-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-414">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-415">O nível de revisão do processador na família de processadores do processador físico subjacente.</span><span class="sxs-lookup"><span data-stu-id="5c410-415">The revision level of the processor within the processor family of the underlying physical processor.</span></span> <span data-ttu-id="5c410-416">Essa propriedade é herdada [**do \_ processador CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="5c410-416">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-417">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5c410-417">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-418">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5c410-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-419">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c410-420">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="5c410-420">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="5c410-421">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="5c410-421">The creation class name of the scoping system.</span></span> <span data-ttu-id="5c410-422">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="5c410-422">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-423">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5c410-423">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-424">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5c410-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-425">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c410-426">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="5c410-426">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="5c410-427">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="5c410-427">The name of the scoping system.</span></span> <span data-ttu-id="5c410-428">Esse valor corresponde ao valor da propriedade [**Name**](msvm-computersystem.md) da classe **Msvm \_ ComputerSystem** para a máquina virtual de escopo.</span><span class="sxs-lookup"><span data-stu-id="5c410-428">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="5c410-429">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="5c410-429">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-430">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="5c410-430">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-431">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5c410-431">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-432">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-433">A data ou a hora em que o estado da máquina virtual foi alterado.</span><span class="sxs-lookup"><span data-stu-id="5c410-433">The date or time at which the virtual machine's state was changed.</span></span> <span data-ttu-id="5c410-434">Se o estado do elemento não tiver sido alterado e essa propriedade for populada, ela deverá ser definida como um valor de intervalo de 0.</span><span class="sxs-lookup"><span data-stu-id="5c410-434">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="5c410-435">Se uma alteração de estado foi solicitada, mas rejeitada ou ainda não processada, a propriedade não deve ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="5c410-435">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="5c410-436">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5c410-436">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5c410-437">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="5c410-437">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-438">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5c410-438">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-439">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-440">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="5c410-440">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="5c410-441">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="5c410-441">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c410-442">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="5c410-442">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-443">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c410-443">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-444">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-444">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-445">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="5c410-445">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="5c410-446">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="5c410-446">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c410-447">**UniqueID**</span><span class="sxs-lookup"><span data-stu-id="5c410-447">**UniqueID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-448">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5c410-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-449">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-450">Um identificador global exclusivo para o processador.</span><span class="sxs-lookup"><span data-stu-id="5c410-450">A globally unique identifier for the processor.</span></span> <span data-ttu-id="5c410-451">Esse identificador só pode ser exclusivo dentro de uma família de processadores.</span><span class="sxs-lookup"><span data-stu-id="5c410-451">This identifier can only be unique within a processor family.</span></span> <span data-ttu-id="5c410-452">Essa propriedade é herdada [**do \_ processador CIM**](/windows/desktop/CIMWin32Prov/cim-processor)e sempre é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5c410-452">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5c410-453">**UpgradeMethod**</span><span class="sxs-lookup"><span data-stu-id="5c410-453">**UpgradeMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c410-454">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c410-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c410-455">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c410-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c410-456">As informações de soquete da CPU, que incluem dados sobre como atualizar o processador (se houver suporte para atualizações).</span><span class="sxs-lookup"><span data-stu-id="5c410-456">The CPU socket information, which includes data on how to upgrade the processor (if upgrades are supported).</span></span> <span data-ttu-id="5c410-457">Essa propriedade é herdada [**do \_ processador CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="5c410-457">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c410-458">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c410-458">Remarks</span></span>

<span data-ttu-id="5c410-459">O acesso à classe de **\_ processador Msvm** pode ser restringido pela filtragem UAC.</span><span class="sxs-lookup"><span data-stu-id="5c410-459">Access to the **Msvm\_Processor** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="5c410-460">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="5c410-460">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c410-461">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c410-461">Requirements</span></span>



| <span data-ttu-id="5c410-462">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c410-462">Requirement</span></span> | <span data-ttu-id="5c410-463">Valor</span><span class="sxs-lookup"><span data-stu-id="5c410-463">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c410-464">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c410-464">Minimum supported client</span></span><br/> | <span data-ttu-id="5c410-465">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5c410-465">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5c410-466">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c410-466">Minimum supported server</span></span><br/> | <span data-ttu-id="5c410-467">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5c410-467">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5c410-468">Namespace</span><span class="sxs-lookup"><span data-stu-id="5c410-468">Namespace</span></span><br/>                | <span data-ttu-id="5c410-469">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="5c410-469">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5c410-470">MOF</span><span class="sxs-lookup"><span data-stu-id="5c410-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c410-471"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c410-471"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c410-472">DLL</span><span class="sxs-lookup"><span data-stu-id="5c410-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c410-473"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5c410-473"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5c410-474">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c410-474">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c410-475">**\_Processador CIM**</span><span class="sxs-lookup"><span data-stu-id="5c410-475">**CIM\_Processor**</span></span>](cim-processor.md)
</dt> <dt>

[<span data-ttu-id="5c410-476">**\_Processador CIM**</span><span class="sxs-lookup"><span data-stu-id="5c410-476">**CIM\_Processor**</span></span>](/windows/desktop/CIMWin32Prov/cim-processor)
</dt> <dt>

[<span data-ttu-id="5c410-477">Classes de processador</span><span class="sxs-lookup"><span data-stu-id="5c410-477">Processor Classes</span></span>](processor-classes.md)
</dt> </dl>

 

