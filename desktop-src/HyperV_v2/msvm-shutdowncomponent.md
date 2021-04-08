---
description: Representa o estado do serviço de desligamento, que fornece um mecanismo para desligar o sistema operacional da máquina virtual das interfaces de gerenciamento no sistema host.
ms.assetid: E9BBB08C-A3FE-4226-A2CF-458706E759D6
title: Classe Msvm_ShutdownComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent
- Msvm_ShutdownComponent.EnableDevice
- Msvm_ShutdownComponent.OnlineDevice
- Msvm_ShutdownComponent.QuiesceDevice
- Msvm_ShutdownComponent.RestoreProperties
- Msvm_ShutdownComponent.SaveProperties
- Msvm_ShutdownComponent.SetPowerState
- Msvm_ShutdownComponent.InstanceID
- Msvm_ShutdownComponent.Caption
- Msvm_ShutdownComponent.Description
- Msvm_ShutdownComponent.ElementName
- Msvm_ShutdownComponent.InstallDate
- Msvm_ShutdownComponent.Name
- Msvm_ShutdownComponent.OperationalStatus
- Msvm_ShutdownComponent.StatusDescriptions
- Msvm_ShutdownComponent.Status
- Msvm_ShutdownComponent.HealthState
- Msvm_ShutdownComponent.CommunicationStatus
- Msvm_ShutdownComponent.DetailedStatus
- Msvm_ShutdownComponent.OperatingStatus
- Msvm_ShutdownComponent.PrimaryStatus
- Msvm_ShutdownComponent.EnabledState
- Msvm_ShutdownComponent.OtherEnabledState
- Msvm_ShutdownComponent.RequestedState
- Msvm_ShutdownComponent.EnabledDefault
- Msvm_ShutdownComponent.TimeOfLastStateChange
- Msvm_ShutdownComponent.AvailableRequestedStates
- Msvm_ShutdownComponent.TransitioningToState
- Msvm_ShutdownComponent.SystemCreationClassName
- Msvm_ShutdownComponent.SystemName
- Msvm_ShutdownComponent.CreationClassName
- Msvm_ShutdownComponent.DeviceID
- Msvm_ShutdownComponent.PowerManagementSupported
- Msvm_ShutdownComponent.PowerManagementCapabilities
- Msvm_ShutdownComponent.Availability
- Msvm_ShutdownComponent.StatusInfo
- Msvm_ShutdownComponent.LastErrorCode
- Msvm_ShutdownComponent.ErrorDescription
- Msvm_ShutdownComponent.ErrorCleared
- Msvm_ShutdownComponent.OtherIdentifyingInfo
- Msvm_ShutdownComponent.PowerOnHours
- Msvm_ShutdownComponent.TotalPowerOnHours
- Msvm_ShutdownComponent.IdentifyingDescriptions
- Msvm_ShutdownComponent.AdditionalAvailability
- Msvm_ShutdownComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 49729568a1625b3df723b1b5b88cc1044b41e715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010710"
---
# <a name="msvm_shutdowncomponent-class"></a><span data-ttu-id="77ee4-103">\_Classe Msvm ShutdownComponent</span><span class="sxs-lookup"><span data-stu-id="77ee4-103">Msvm\_ShutdownComponent class</span></span>

<span data-ttu-id="77ee4-104">Representa o estado do serviço de desligamento, que fornece um mecanismo para desligar o sistema operacional da máquina virtual das interfaces de gerenciamento no sistema host.</span><span class="sxs-lookup"><span data-stu-id="77ee4-104">Represents the state of the shutdown service, which provides a mechanism to shut down the operating system of the virtual machine from the management interfaces on the host system.</span></span>

<span data-ttu-id="77ee4-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="77ee4-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="77ee4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77ee4-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ShutdownComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Shutdown";
  string   Description = "Microsoft Shutdown Service";
  string   ElementName = "Shutdown";
  datetime InstallDate;
  string   Name = "Shutdown";
  uint16   OperationalStatus[];
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 7;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_ShutdownComponent";
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
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
};
```

## <a name="members"></a><span data-ttu-id="77ee4-107">Membros</span><span class="sxs-lookup"><span data-stu-id="77ee4-107">Members</span></span>

<span data-ttu-id="77ee4-108">A classe **Msvm \_ ShutdownComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="77ee4-108">The **Msvm\_ShutdownComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="77ee4-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="77ee4-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="77ee4-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="77ee4-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="77ee4-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="77ee4-111">Methods</span></span>

<span data-ttu-id="77ee4-112">A classe **Msvm \_ ShutdownComponent** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="77ee4-112">The **Msvm\_ShutdownComponent** class has these methods.</span></span>



| <span data-ttu-id="77ee4-113">Método</span><span class="sxs-lookup"><span data-stu-id="77ee4-113">Method</span></span>                                                                  | <span data-ttu-id="77ee4-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="77ee4-114">Description</span></span>                                                                                        |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77ee4-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="77ee4-115">**EnableDevice**</span></span>                                                        | <span data-ttu-id="77ee4-116">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="77ee4-116">This method is not supported.</span></span><br/>                                                           |
| [<span data-ttu-id="77ee4-117">**InitiateReboot**</span><span class="sxs-lookup"><span data-stu-id="77ee4-117">**InitiateReboot**</span></span>](msvm-shutdowncomponent-initiatereboot.md)         | <span data-ttu-id="77ee4-118">Inicia uma operação de reinicialização do sistema operacional na máquina virtual filho associada.</span><span class="sxs-lookup"><span data-stu-id="77ee4-118">Initiates an operating system reboot operation on the associated child virtual machine.</span></span><br/> |
| [<span data-ttu-id="77ee4-119">**InitiateShutdown**</span><span class="sxs-lookup"><span data-stu-id="77ee4-119">**InitiateShutdown**</span></span>](msvm-shutdowncomponent-initiateshutdown.md)     | <span data-ttu-id="77ee4-120">Inicia uma operação de desligamento do sistema operacional na máquina virtual filha associada.</span><span class="sxs-lookup"><span data-stu-id="77ee4-120">Initiates an operating system shutdown operation on associated child virtual machine.</span></span><br/>   |
| <span data-ttu-id="77ee4-121">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="77ee4-121">**OnlineDevice**</span></span>                                                        | <span data-ttu-id="77ee4-122">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="77ee4-122">This method is not supported.</span></span><br/>                                                           |
| <span data-ttu-id="77ee4-123">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="77ee4-123">**QuiesceDevice**</span></span>                                                       | <span data-ttu-id="77ee4-124">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="77ee4-124">This method is not supported.</span></span><br/>                                                           |
| [<span data-ttu-id="77ee4-125">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="77ee4-125">**RequestStateChange**</span></span>](msvm-shutdowncomponent-requeststatechange.md) | <span data-ttu-id="77ee4-126">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="77ee4-126">Requests a state change.</span></span><br/>                                                                |
| [<span data-ttu-id="77ee4-127">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="77ee4-127">**Reset**</span></span>](msvm-shutdowncomponent-reset.md)                           | <span data-ttu-id="77ee4-128">Redefine o componente.</span><span class="sxs-lookup"><span data-stu-id="77ee4-128">Resets the component.</span></span><br/>                                                                   |
| <span data-ttu-id="77ee4-129">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="77ee4-129">**RestoreProperties**</span></span>                                                   | <span data-ttu-id="77ee4-130">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="77ee4-130">This method is not supported.</span></span><br/>                                                           |
| <span data-ttu-id="77ee4-131">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="77ee4-131">**SaveProperties**</span></span>                                                      | <span data-ttu-id="77ee4-132">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="77ee4-132">This method is not supported.</span></span><br/>                                                           |
| <span data-ttu-id="77ee4-133">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="77ee4-133">**SetPowerState**</span></span>                                                       | <span data-ttu-id="77ee4-134">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="77ee4-134">This method is not supported.</span></span><br/>                                                           |



 

### <a name="properties"></a><span data-ttu-id="77ee4-135">Propriedades</span><span class="sxs-lookup"><span data-stu-id="77ee4-135">Properties</span></span>

<span data-ttu-id="77ee4-136">A classe **Msvm \_ ShutdownComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="77ee4-136">The **Msvm\_ShutdownComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="77ee4-137">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="77ee4-137">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-138">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="77ee4-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-140">Disponibilidade e status adicionais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="77ee4-140">Additional availability and status of the device.</span></span> <span data-ttu-id="77ee4-141">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="77ee4-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="77ee4-142">Valor</span><span class="sxs-lookup"><span data-stu-id="77ee4-142">Value</span></span>                                                                        | <span data-ttu-id="77ee4-143">Significado</span><span class="sxs-lookup"><span data-stu-id="77ee4-143">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="77ee4-144"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="77ee4-144"><dt>6</dt></span></span> </dl> | <span data-ttu-id="77ee4-145">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="77ee4-145">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="77ee4-146">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="77ee4-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-147">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="77ee4-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-149">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="77ee4-149">The primary availability and status of the device.</span></span> <span data-ttu-id="77ee4-150">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="77ee4-150">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>



| <span data-ttu-id="77ee4-151">Valor</span><span class="sxs-lookup"><span data-stu-id="77ee4-151">Value</span></span>                                                                        | <span data-ttu-id="77ee4-152">Significado</span><span class="sxs-lookup"><span data-stu-id="77ee4-152">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="77ee4-153"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="77ee4-153"><dt>6</dt></span></span> </dl> | <span data-ttu-id="77ee4-154">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="77ee4-154">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="77ee4-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="77ee4-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-156">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="77ee4-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-158">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="77ee4-158">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="77ee4-159">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="77ee4-159">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-160">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="77ee4-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="77ee4-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-163">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="77ee4-163">A short description of the object.</span></span> <span data-ttu-id="77ee4-164">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="77ee4-164">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-165">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="77ee4-165">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-166">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="77ee4-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-168">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="77ee4-168">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="77ee4-169">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="77ee4-169">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="77ee4-170">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="77ee4-170">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="77ee4-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="77ee4-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="77ee4-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-173"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="77ee4-173"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-174"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="77ee4-174"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-175"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="77ee4-175"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="77ee4-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="77ee4-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="77ee4-178">)</span><span class="sxs-lookup"><span data-stu-id="77ee4-178">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="77ee4-179">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="77ee4-179">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="77ee4-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-182">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="77ee4-182">The scoping system's creation class name.</span></span> <span data-ttu-id="77ee4-183">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="77ee4-183">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-184">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="77ee4-184">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-185">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="77ee4-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-187">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="77ee4-187">A description of the object.</span></span> <span data-ttu-id="77ee4-188">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="77ee4-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-189">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="77ee4-189">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-190">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="77ee4-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-192">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="77ee4-192">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="77ee4-193">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="77ee4-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="77ee4-194">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="77ee4-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="77ee4-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="77ee4-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="77ee4-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="77ee4-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="77ee4-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="77ee4-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="77ee4-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="77ee4-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="77ee4-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="77ee4-203">)</span><span class="sxs-lookup"><span data-stu-id="77ee4-203">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="77ee4-204">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="77ee4-204">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-205">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="77ee4-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-207">Um endereço ou outras informações de identificação para nomear exclusivamente o LogicalDevice.</span><span class="sxs-lookup"><span data-stu-id="77ee4-207">An address or other identifying information to uniquely name the LogicalDevice.</span></span> <span data-ttu-id="77ee4-208">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como "Microsoft:*VMGUID* \\ *GUID*", em *que VMGUID* é a propriedade **Name** da instância do [**Msvm \_ ComputerSystem**](msvm-computersystem.md) associada a este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="77ee4-208">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) instance associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-209">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="77ee4-209">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="77ee4-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-212">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="77ee4-212">A display name for the object.</span></span> <span data-ttu-id="77ee4-213">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="77ee4-213">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-214">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="77ee4-214">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-215">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="77ee4-215">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-216">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-217">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="77ee4-217">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="77ee4-218">Valor</span><span class="sxs-lookup"><span data-stu-id="77ee4-218">Value</span></span>                                                                        | <span data-ttu-id="77ee4-219">Significado</span><span class="sxs-lookup"><span data-stu-id="77ee4-219">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="77ee4-220"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="77ee4-220"><dt>7</dt></span></span> </dl> | <span data-ttu-id="77ee4-221">Nenhum padrão</span><span class="sxs-lookup"><span data-stu-id="77ee4-221">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="77ee4-222">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="77ee4-222">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-223">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="77ee4-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-225">O estado habilitado do elemento.</span><span class="sxs-lookup"><span data-stu-id="77ee4-225">The enabled state of the element.</span></span> <span data-ttu-id="77ee4-226">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e é definida como 2 (habilitado) ou 3 (desabilitado).</span><span class="sxs-lookup"><span data-stu-id="77ee4-226">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is either set to 2 (Enabled) or 3 (Disabled).</span></span>



| <span data-ttu-id="77ee4-227">Valor</span><span class="sxs-lookup"><span data-stu-id="77ee4-227">Value</span></span>                                                                        | <span data-ttu-id="77ee4-228">Significado</span><span class="sxs-lookup"><span data-stu-id="77ee4-228">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="77ee4-229"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="77ee4-229"><dt>2</dt></span></span> </dl> | <span data-ttu-id="77ee4-230">habilitado</span><span class="sxs-lookup"><span data-stu-id="77ee4-230">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="77ee4-231"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="77ee4-231"><dt>3</dt></span></span> </dl> | <span data-ttu-id="77ee4-232">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="77ee4-232">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="77ee4-233">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="77ee4-233">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-234">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="77ee4-234">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-235">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-236">Indica se o erro relatado na propriedade **LastErrorCode** agora está apagado.</span><span class="sxs-lookup"><span data-stu-id="77ee4-236">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="77ee4-237">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="77ee4-237">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-238">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="77ee4-238">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-239">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="77ee4-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-240">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-241">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado na propriedade **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="77ee4-241">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="77ee4-242">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="77ee4-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-243">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="77ee4-243">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-244">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="77ee4-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-245">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-246">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="77ee4-246">The current health of the element.</span></span> <span data-ttu-id="77ee4-247">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="77ee4-247">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="77ee4-248">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="77ee4-248">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-249">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="77ee4-249">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-250">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="77ee4-250">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-251">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-252">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="77ee4-252">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="77ee4-253">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="77ee4-253">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-254">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="77ee4-254">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-255">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="77ee4-255">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-256">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-257">A data e a hora em que o serviço de integração foi instalado na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="77ee4-257">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="77ee4-258">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="77ee4-258">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-259">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="77ee4-259">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-260">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="77ee4-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-261">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-262">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="77ee4-262">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-263">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="77ee4-263">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="77ee4-264">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="77ee4-264">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-265">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="77ee4-265">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-266">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="77ee4-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-267">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-268">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="77ee4-268">The last error code reported by the logical device.</span></span> <span data-ttu-id="77ee4-269">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="77ee4-269">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-270">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="77ee4-270">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-271">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="77ee4-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-272">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-273">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="77ee4-273">This property has been deprecated.</span></span> <span data-ttu-id="77ee4-274">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="77ee4-274">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-275">**Nome**</span><span class="sxs-lookup"><span data-stu-id="77ee4-275">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-276">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="77ee4-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-277">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-278">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="77ee4-278">The label by which the object is known.</span></span> <span data-ttu-id="77ee4-279">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="77ee4-279">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-280">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="77ee4-280">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-281">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="77ee4-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-282">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-283">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="77ee4-283">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="77ee4-284">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="77ee4-284">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="77ee4-285">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="77ee4-285">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="77ee4-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="77ee4-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-287"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="77ee4-287"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-288"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="77ee4-288"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-289"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="77ee4-289"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-290"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="77ee4-290"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-291"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="77ee4-291"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-292"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="77ee4-292"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-293"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="77ee4-293"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-294"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="77ee4-294"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-295"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="77ee4-295"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-296"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="77ee4-296"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-297"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="77ee4-297"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-298"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="77ee4-298"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-299"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="77ee4-299"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-300"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="77ee4-300"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-301"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="77ee4-301"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-302"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="77ee4-302"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-303"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="77ee4-303"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-304"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="77ee4-304"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="77ee4-305">)</span><span class="sxs-lookup"><span data-stu-id="77ee4-305">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="77ee4-306">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="77ee4-306">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-307">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="77ee4-307">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-308">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-309">O status atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="77ee4-309">The current status of the element.</span></span> <span data-ttu-id="77ee4-310">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="77ee4-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="77ee4-311">A seguir estão os valores possíveis para o  \[ valor da \] Propriedade OperationalStatus 0.</span><span class="sxs-lookup"><span data-stu-id="77ee4-311">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="77ee4-312">Valor</span><span class="sxs-lookup"><span data-stu-id="77ee4-312">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="77ee4-313">Significado</span><span class="sxs-lookup"><span data-stu-id="77ee4-313">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="77ee4-314"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="77ee4-314"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="77ee4-315">O serviço está funcionando normalmente.</span><span class="sxs-lookup"><span data-stu-id="77ee4-315">The service is operating normally.</span></span> <span data-ttu-id="77ee4-316">Os  \[ valores de \] Propriedade OperationalStatus 1 e **StatusDescriptions** \[ 1 \] podem conter mais informações.</span><span class="sxs-lookup"><span data-stu-id="77ee4-316">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="77ee4-317"><dt>**Degradado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="77ee4-317"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="77ee4-318">O serviço está funcionando normalmente, mas o serviço convidado negocia uma versão de protocolo de comunicação compatível.</span><span class="sxs-lookup"><span data-stu-id="77ee4-318">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="77ee4-319">Os  \[ valores de \] Propriedade OperationalStatus 1 e **StatusDescriptions** \[ 1 \] podem conter mais informações.</span><span class="sxs-lookup"><span data-stu-id="77ee4-319">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="77ee4-320"><dt>**Erro não recuperável**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="77ee4-320"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="77ee4-321">O convidado não oferece suporte a uma versão de protocolo compatível.</span><span class="sxs-lookup"><span data-stu-id="77ee4-321">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="77ee4-322">Os  \[ valores de \] Propriedade OperationalStatus 1 e **StatusDescriptions** \[ 1 \] podem conter mais informações.</span><span class="sxs-lookup"><span data-stu-id="77ee4-322">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="77ee4-323"><dt>**Nenhum contato**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="77ee4-323"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="77ee4-324">O serviço convidado não está instalado ou ainda não foi contatado.</span><span class="sxs-lookup"><span data-stu-id="77ee4-324">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="77ee4-325"><dt>**Comunicação perdida**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="77ee4-325"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="77ee4-326">O serviço convidado não está mais respondendo normalmente.</span><span class="sxs-lookup"><span data-stu-id="77ee4-326">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="77ee4-327">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="77ee4-327">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-328">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="77ee4-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-329">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-330">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="77ee4-330">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="77ee4-331">Essa propriedade deve ser definida como **NULL** quando a propriedade **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="77ee4-331">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="77ee4-332">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="77ee4-332">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-333">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="77ee4-333">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-334">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="77ee4-334">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-335">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-336">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="77ee4-336">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="77ee4-337">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="77ee4-337">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-338">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="77ee4-338">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-339">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="77ee4-339">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-340">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-341">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="77ee4-341">The power management capabilities of the device.</span></span> <span data-ttu-id="77ee4-342">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="77ee4-342">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-343">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="77ee4-343">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-344">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="77ee4-344">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-345">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-346">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="77ee4-346">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="77ee4-347">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="77ee4-347">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-348">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="77ee4-348">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-349">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="77ee4-349">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-350">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-351">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="77ee4-351">The number of consecutive hours that this Device has been powered on since its last power cycle.</span></span> <span data-ttu-id="77ee4-352">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="77ee4-352">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-353">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="77ee4-353">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-354">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="77ee4-354">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-355">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-356">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="77ee4-356">Provides high level status information.</span></span> <span data-ttu-id="77ee4-357">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="77ee4-357">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="77ee4-358">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="77ee4-358">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="77ee4-359">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="77ee4-359">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="77ee4-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="77ee4-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-361"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="77ee4-361"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="77ee4-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="77ee4-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="77ee4-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="77ee4-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="77ee4-366">)</span><span class="sxs-lookup"><span data-stu-id="77ee4-366">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="77ee4-367">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="77ee4-367">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-368">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="77ee4-368">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-369">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-370">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="77ee4-370">The last requested or desired state for the element.</span></span> <span data-ttu-id="77ee4-371">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="77ee4-371">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="77ee4-372">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="77ee4-372">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="77ee4-373">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 12 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="77ee4-373">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="77ee4-374">Valor</span><span class="sxs-lookup"><span data-stu-id="77ee4-374">Value</span></span>                                                                         | <span data-ttu-id="77ee4-375">Significado</span><span class="sxs-lookup"><span data-stu-id="77ee4-375">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="77ee4-376"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="77ee4-376"><dt>12</dt></span></span> </dl> | <span data-ttu-id="77ee4-377">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="77ee4-377">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="77ee4-378">**Status**</span><span class="sxs-lookup"><span data-stu-id="77ee4-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-379">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="77ee4-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-380">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-381">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="77ee4-381">The current status of the object.</span></span> <span data-ttu-id="77ee4-382">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) , mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="77ee4-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-383">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="77ee4-383">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-384">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="77ee4-384">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-385">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-386">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="77ee4-386">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="77ee4-387">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="77ee4-387">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-388">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="77ee4-388">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-389">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="77ee4-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-390">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-391">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="77ee4-391">The current state of the logical device.</span></span> <span data-ttu-id="77ee4-392">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="77ee4-392">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-393">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="77ee4-393">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-394">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="77ee4-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-395">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-396">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="77ee4-396">The scoping system's creation class name.</span></span> <span data-ttu-id="77ee4-397">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="77ee4-397">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-398">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="77ee4-398">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-399">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="77ee4-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-400">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-401">O identificador exclusivo para a máquina virtual de escopo.</span><span class="sxs-lookup"><span data-stu-id="77ee4-401">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="77ee4-402">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="77ee4-402">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-403">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="77ee4-403">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-404">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="77ee4-404">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-405">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-406">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="77ee4-406">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="77ee4-407">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="77ee4-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-408">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="77ee4-408">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-409">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="77ee4-409">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-410">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-411">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="77ee4-411">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="77ee4-412">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="77ee4-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="77ee4-413">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="77ee4-413">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ee4-414">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="77ee4-414">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="77ee4-415">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="77ee4-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77ee4-416">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="77ee4-416">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="77ee4-417">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="77ee4-417">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77ee4-418">Comentários</span><span class="sxs-lookup"><span data-stu-id="77ee4-418">Remarks</span></span>

<span data-ttu-id="77ee4-419">O acesso à classe **Msvm \_ ShutdownComponent** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="77ee4-419">Access to the **Msvm\_ShutdownComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="77ee4-420">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="77ee4-420">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="77ee4-421">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77ee4-421">Requirements</span></span>



| <span data-ttu-id="77ee4-422">Requisito</span><span class="sxs-lookup"><span data-stu-id="77ee4-422">Requirement</span></span> | <span data-ttu-id="77ee4-423">Valor</span><span class="sxs-lookup"><span data-stu-id="77ee4-423">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77ee4-424">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77ee4-424">Minimum supported client</span></span><br/> | <span data-ttu-id="77ee4-425">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="77ee4-425">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="77ee4-426">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77ee4-426">Minimum supported server</span></span><br/> | <span data-ttu-id="77ee4-427">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="77ee4-427">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="77ee4-428">Namespace</span><span class="sxs-lookup"><span data-stu-id="77ee4-428">Namespace</span></span><br/>                | <span data-ttu-id="77ee4-429">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="77ee4-429">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="77ee4-430">MOF</span><span class="sxs-lookup"><span data-stu-id="77ee4-430">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77ee4-431"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="77ee4-431"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="77ee4-432">DLL</span><span class="sxs-lookup"><span data-stu-id="77ee4-432">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77ee4-433"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="77ee4-433"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="77ee4-434">Confira também</span><span class="sxs-lookup"><span data-stu-id="77ee4-434">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77ee4-435">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="77ee4-435">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="77ee4-436">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="77ee4-436">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

