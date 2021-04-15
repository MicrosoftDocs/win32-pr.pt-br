---
description: Representa um controlador SCSI sintético.
ms.assetid: 4ABAB4C8-F922-4AA3-8FEE-5F5AA969E8B4
title: Classe Msvm_SCSIProtocolController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SCSIProtocolController
- Msvm_SCSIProtocolController.SetPowerState
- Msvm_SCSIProtocolController.EnableDevice
- Msvm_SCSIProtocolController.OnlineDevice
- Msvm_SCSIProtocolController.QuiesceDevice
- Msvm_SCSIProtocolController.SaveProperties
- Msvm_SCSIProtocolController.RestoreProperties
- Msvm_SCSIProtocolController.InstanceID
- Msvm_SCSIProtocolController.Caption
- Msvm_SCSIProtocolController.Description
- Msvm_SCSIProtocolController.ElementName
- Msvm_SCSIProtocolController.InstallDate
- Msvm_SCSIProtocolController.Name
- Msvm_SCSIProtocolController.OperationalStatus
- Msvm_SCSIProtocolController.StatusDescriptions
- Msvm_SCSIProtocolController.Status
- Msvm_SCSIProtocolController.HealthState
- Msvm_SCSIProtocolController.CommunicationStatus
- Msvm_SCSIProtocolController.DetailedStatus
- Msvm_SCSIProtocolController.OperatingStatus
- Msvm_SCSIProtocolController.PrimaryStatus
- Msvm_SCSIProtocolController.EnabledState
- Msvm_SCSIProtocolController.OtherEnabledState
- Msvm_SCSIProtocolController.RequestedState
- Msvm_SCSIProtocolController.EnabledDefault
- Msvm_SCSIProtocolController.TimeOfLastStateChange
- Msvm_SCSIProtocolController.AvailableRequestedStates
- Msvm_SCSIProtocolController.TransitioningToState
- Msvm_SCSIProtocolController.SystemCreationClassName
- Msvm_SCSIProtocolController.SystemName
- Msvm_SCSIProtocolController.CreationClassName
- Msvm_SCSIProtocolController.DeviceID
- Msvm_SCSIProtocolController.PowerManagementSupported
- Msvm_SCSIProtocolController.PowerManagementCapabilities
- Msvm_SCSIProtocolController.Availability
- Msvm_SCSIProtocolController.StatusInfo
- Msvm_SCSIProtocolController.LastErrorCode
- Msvm_SCSIProtocolController.ErrorDescription
- Msvm_SCSIProtocolController.ErrorCleared
- Msvm_SCSIProtocolController.OtherIdentifyingInfo
- Msvm_SCSIProtocolController.PowerOnHours
- Msvm_SCSIProtocolController.TotalPowerOnHours
- Msvm_SCSIProtocolController.IdentifyingDescriptions
- Msvm_SCSIProtocolController.AdditionalAvailability
- Msvm_SCSIProtocolController.MaxQuiesceTime
- Msvm_SCSIProtocolController.MaxUnitsControlled
- Msvm_SCSIProtocolController.NameFormat
- Msvm_SCSIProtocolController.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b65390c7cb03f195e9de39aedc3629688717e0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506305"
---
# <a name="msvm_scsiprotocolcontroller-class"></a><span data-ttu-id="23b9e-103">\_Classe Msvm SCSIProtocolController</span><span class="sxs-lookup"><span data-stu-id="23b9e-103">Msvm\_SCSIProtocolController class</span></span>

<span data-ttu-id="23b9e-104">Representa um controlador SCSI sintético.</span><span class="sxs-lookup"><span data-stu-id="23b9e-104">Represents a synthetic SCSI controller.</span></span> <span data-ttu-id="23b9e-105">Um controlador SCSI sintético pode dar suporte a até 256 unidades.</span><span class="sxs-lookup"><span data-stu-id="23b9e-105">A synthetic SCSI controller can support up to 256 drives.</span></span>

<span data-ttu-id="23b9e-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="23b9e-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="23b9e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23b9e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SCSIProtocolController : CIM_SCSIProtocolController
{
  string   InstanceID;
  string   Caption = "SCSI Controller";
  string   Description = "Microsoft Virtual SCSI Controller";
  string   ElementName = "SCSI Controller";
  datetime InstallDate;
  string   Name = "SCSI Controller";
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
  string   CreationClassName = "Msvm_SCSIProtocolController";
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
  uint32   MaxUnitsControlled = 256;
  uint16   NameFormat = 0;
  string   OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="23b9e-108">Membros</span><span class="sxs-lookup"><span data-stu-id="23b9e-108">Members</span></span>

<span data-ttu-id="23b9e-109">A classe **Msvm \_ SCSIProtocolController** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="23b9e-109">The **Msvm\_SCSIProtocolController** class has these types of members:</span></span>

-   [<span data-ttu-id="23b9e-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="23b9e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="23b9e-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="23b9e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="23b9e-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="23b9e-112">Methods</span></span>

<span data-ttu-id="23b9e-113">A classe **Msvm \_ SCSIProtocolController** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="23b9e-113">The **Msvm\_SCSIProtocolController** class has these methods.</span></span>



| <span data-ttu-id="23b9e-114">Método</span><span class="sxs-lookup"><span data-stu-id="23b9e-114">Method</span></span>                                                                       | <span data-ttu-id="23b9e-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="23b9e-115">Description</span></span>                              |
|:-----------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="23b9e-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="23b9e-116">**EnableDevice**</span></span>                                                             | <span data-ttu-id="23b9e-117">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="23b9e-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="23b9e-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="23b9e-118">**OnlineDevice**</span></span>                                                             | <span data-ttu-id="23b9e-119">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="23b9e-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="23b9e-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="23b9e-120">**QuiesceDevice**</span></span>                                                            | <span data-ttu-id="23b9e-121">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="23b9e-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="23b9e-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="23b9e-122">**RequestStateChange**</span></span>](msvm-scsiprotocolcontroller-requeststatechange.md) | <span data-ttu-id="23b9e-123">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="23b9e-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="23b9e-124">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="23b9e-124">**Reset**</span></span>](msvm-scsiprotocolcontroller-reset.md)                           | <span data-ttu-id="23b9e-125">Redefine o dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="23b9e-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="23b9e-126">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="23b9e-126">**RestoreProperties**</span></span>                                                        | <span data-ttu-id="23b9e-127">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="23b9e-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="23b9e-128">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="23b9e-128">**SaveProperties**</span></span>                                                           | <span data-ttu-id="23b9e-129">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="23b9e-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="23b9e-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="23b9e-130">**SetPowerState**</span></span>                                                            | <span data-ttu-id="23b9e-131">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="23b9e-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="23b9e-132">Propriedades</span><span class="sxs-lookup"><span data-stu-id="23b9e-132">Properties</span></span>

<span data-ttu-id="23b9e-133">A classe **Msvm \_ SCSIProtocolController** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="23b9e-133">The **Msvm\_SCSIProtocolController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="23b9e-134">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="23b9e-134">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-135">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23b9e-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-137">Qualquer disponibilidade e status adicionais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="23b9e-137">Any additional availability and status of the device.</span></span> <span data-ttu-id="23b9e-138">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="23b9e-138">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="23b9e-139">Valor</span><span class="sxs-lookup"><span data-stu-id="23b9e-139">Value</span></span>                                                                            | <span data-ttu-id="23b9e-140">Significado</span><span class="sxs-lookup"><span data-stu-id="23b9e-140">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="23b9e-141"><dt>152</dt></span><span class="sxs-lookup"><span data-stu-id="23b9e-141"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="23b9e-142"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="23b9e-142"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="23b9e-143">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="23b9e-143">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="23b9e-144">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="23b9e-144">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-145">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23b9e-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-147">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="23b9e-147">The primary availability and status of the device.</span></span> <span data-ttu-id="23b9e-148">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="23b9e-148">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="23b9e-149">Valor</span><span class="sxs-lookup"><span data-stu-id="23b9e-149">Value</span></span>                                                                        | <span data-ttu-id="23b9e-150">Significado</span><span class="sxs-lookup"><span data-stu-id="23b9e-150">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="23b9e-151"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="23b9e-151"><dt>6</dt></span></span> </dl> | <span data-ttu-id="23b9e-152">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="23b9e-152">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="23b9e-153">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="23b9e-153">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-154">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23b9e-154">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-156">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="23b9e-156">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="23b9e-157">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="23b9e-157">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-158">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="23b9e-158">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="23b9e-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-161">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="23b9e-161">A short description of the object.</span></span> <span data-ttu-id="23b9e-162">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="23b9e-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-163">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="23b9e-163">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-164">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23b9e-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-166">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="23b9e-166">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="23b9e-167">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="23b9e-167">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="23b9e-168">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="23b9e-168">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="23b9e-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="23b9e-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="23b9e-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="23b9e-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="23b9e-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="23b9e-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="23b9e-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="23b9e-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="23b9e-176">)</span><span class="sxs-lookup"><span data-stu-id="23b9e-176">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="23b9e-177">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="23b9e-177">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="23b9e-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-180">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="23b9e-180">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="23b9e-181">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="23b9e-181">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-182">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="23b9e-182">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="23b9e-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-185">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="23b9e-185">A description of the object.</span></span> <span data-ttu-id="23b9e-186">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="23b9e-186">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-187">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="23b9e-187">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-188">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23b9e-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-190">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="23b9e-190">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="23b9e-191">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="23b9e-191">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="23b9e-192">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="23b9e-192">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="23b9e-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="23b9e-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="23b9e-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="23b9e-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="23b9e-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="23b9e-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="23b9e-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="23b9e-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="23b9e-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="23b9e-201">)</span><span class="sxs-lookup"><span data-stu-id="23b9e-201">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="23b9e-202">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="23b9e-202">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-203">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="23b9e-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-205">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como "Microsoft:*GUID*- \\ *specific-data*".</span><span class="sxs-lookup"><span data-stu-id="23b9e-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-206">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="23b9e-206">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-207">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="23b9e-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-209">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="23b9e-209">A display name for the object.</span></span> <span data-ttu-id="23b9e-210">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="23b9e-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-211">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="23b9e-211">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-212">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23b9e-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-214">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="23b9e-214">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="23b9e-215">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="23b9e-215">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="23b9e-216">Valor</span><span class="sxs-lookup"><span data-stu-id="23b9e-216">Value</span></span>                                                                        | <span data-ttu-id="23b9e-217">Significado</span><span class="sxs-lookup"><span data-stu-id="23b9e-217">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="23b9e-218"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="23b9e-218"><dt>2</dt></span></span> </dl> | <span data-ttu-id="23b9e-219">habilitado</span><span class="sxs-lookup"><span data-stu-id="23b9e-219">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="23b9e-220">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="23b9e-220">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-221">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23b9e-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-223">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="23b9e-223">The enabled and disabled states of an element.</span></span> <span data-ttu-id="23b9e-224">Ele também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="23b9e-224">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="23b9e-225">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="23b9e-225">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="23b9e-226">Valor</span><span class="sxs-lookup"><span data-stu-id="23b9e-226">Value</span></span>                                                                        | <span data-ttu-id="23b9e-227">Significado</span><span class="sxs-lookup"><span data-stu-id="23b9e-227">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="23b9e-228"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="23b9e-228"><dt>5</dt></span></span> </dl> | <span data-ttu-id="23b9e-229">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="23b9e-229">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="23b9e-230">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="23b9e-230">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-231">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="23b9e-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-232">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-233">Indica se o erro relatado na propriedade **LastErrorCode** agora está apagado.</span><span class="sxs-lookup"><span data-stu-id="23b9e-233">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="23b9e-234">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="23b9e-234">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-235">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="23b9e-235">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-236">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="23b9e-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-237">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-238">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado na propriedade **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="23b9e-238">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="23b9e-239">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="23b9e-239">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-240">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="23b9e-240">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-241">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23b9e-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-242">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-243">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="23b9e-243">The current health of the element.</span></span> <span data-ttu-id="23b9e-244">Isso expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="23b9e-244">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="23b9e-245">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="23b9e-245">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="23b9e-246">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="23b9e-246">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-247">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="23b9e-247">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-248">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="23b9e-248">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-249">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-250">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz de propriedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="23b9e-250">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="23b9e-251">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="23b9e-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-252">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="23b9e-252">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-253">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="23b9e-253">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-254">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-255">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="23b9e-255">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="23b9e-256">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="23b9e-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-257">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="23b9e-257">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-258">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="23b9e-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-260">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="23b9e-260">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-261">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="23b9e-261">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="23b9e-262">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="23b9e-262">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-263">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="23b9e-263">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-264">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="23b9e-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-265">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-266">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="23b9e-266">The last error code reported by the logical device.</span></span> <span data-ttu-id="23b9e-267">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="23b9e-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-268">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="23b9e-268">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-269">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="23b9e-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-271">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="23b9e-271">This property has been deprecated.</span></span> <span data-ttu-id="23b9e-272">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="23b9e-272">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-273">**MaxUnitsControlled**</span><span class="sxs-lookup"><span data-stu-id="23b9e-273">**MaxUnitsControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-274">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="23b9e-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-275">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-276">O número máximo de unidades que podem ser controladas pelo ou acessadas por meio desse controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="23b9e-276">The maximum number of units that can be controlled by or accessed through this protocol controller.</span></span> <span data-ttu-id="23b9e-277">Essa propriedade é herdada do [**CIM \_ ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span><span class="sxs-lookup"><span data-stu-id="23b9e-277">This property is inherited from [**CIM\_ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-278">**Nome**</span><span class="sxs-lookup"><span data-stu-id="23b9e-278">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-279">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="23b9e-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-281">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="23b9e-281">The label by which the object is known.</span></span> <span data-ttu-id="23b9e-282">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="23b9e-282">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-283">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="23b9e-283">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-284">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23b9e-284">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-285">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-286">Identifica como o nome do controlador de protocolo SCSI é selecionado.</span><span class="sxs-lookup"><span data-stu-id="23b9e-286">Identifies how the name of the SCSI protocol controller is selected.</span></span> <span data-ttu-id="23b9e-287">Essa propriedade é herdada do [**CIM \_ SCSIProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span><span class="sxs-lookup"><span data-stu-id="23b9e-287">This property is inherited from [**CIM\_SCSIProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span></span>



| <span data-ttu-id="23b9e-288">Valor</span><span class="sxs-lookup"><span data-stu-id="23b9e-288">Value</span></span>                                                                        | <span data-ttu-id="23b9e-289">Significado</span><span class="sxs-lookup"><span data-stu-id="23b9e-289">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="23b9e-290"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="23b9e-290"><dt>0</dt></span></span> </dl> | <span data-ttu-id="23b9e-291">Unknown</span><span class="sxs-lookup"><span data-stu-id="23b9e-291">Unknown</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="23b9e-292">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="23b9e-292">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-293">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23b9e-293">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-294">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-295">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="23b9e-295">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="23b9e-296">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="23b9e-296">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="23b9e-297">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="23b9e-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="23b9e-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="23b9e-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-299"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="23b9e-299"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-300"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="23b9e-300"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-301"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="23b9e-301"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-302"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="23b9e-302"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-303"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="23b9e-303"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-304"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="23b9e-304"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-305"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="23b9e-305"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-306"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="23b9e-306"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-307"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="23b9e-307"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-308"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="23b9e-308"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-309"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="23b9e-309"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-310"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="23b9e-310"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-311"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="23b9e-311"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-312"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="23b9e-312"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-313"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="23b9e-313"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-314"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="23b9e-314"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="23b9e-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="23b9e-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="23b9e-317">)</span><span class="sxs-lookup"><span data-stu-id="23b9e-317">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="23b9e-318">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="23b9e-318">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-319">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23b9e-319">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-320">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-321">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="23b9e-321">The current status of the object.</span></span> <span data-ttu-id="23b9e-322">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="23b9e-322">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="23b9e-323">Valor</span><span class="sxs-lookup"><span data-stu-id="23b9e-323">Value</span></span>                                                                            | <span data-ttu-id="23b9e-324">Significado</span><span class="sxs-lookup"><span data-stu-id="23b9e-324">Meaning</span></span>       |
|----------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="23b9e-325"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="23b9e-325"><dt>{ 2 }</dt></span></span> </dl> |               |
| <dl> <span data-ttu-id="23b9e-326"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="23b9e-326"><dt>2</dt></span></span> </dl>     | <span data-ttu-id="23b9e-327">OK</span><span class="sxs-lookup"><span data-stu-id="23b9e-327">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="23b9e-328">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="23b9e-328">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-329">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="23b9e-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-331">O estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="23b9e-331">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="23b9e-332">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="23b9e-332">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="23b9e-333">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="23b9e-333">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-334">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="23b9e-334">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-335">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="23b9e-335">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-337">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="23b9e-337">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="23b9e-338">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="23b9e-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-339">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="23b9e-339">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-340">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="23b9e-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-342">Uma cadeia de caracteres que descreve como o controlador de protocolo é identificado quando o **NameFormat** é 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="23b9e-342">A string that describes how the protocol controller is identified when the **NameFormat** is 1 (Other).</span></span> <span data-ttu-id="23b9e-343">Essa propriedade é herdada do [**CIM \_ SCSIProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span><span class="sxs-lookup"><span data-stu-id="23b9e-343">This property is inherited from [**CIM\_SCSIProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-344">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="23b9e-344">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-345">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23b9e-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-346">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-347">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="23b9e-347">The power management capabilities of the device.</span></span> <span data-ttu-id="23b9e-348">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="23b9e-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-349">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="23b9e-349">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-350">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="23b9e-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-351">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-352">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="23b9e-352">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="23b9e-353">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="23b9e-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-354">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="23b9e-354">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-355">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="23b9e-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-356">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-357">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="23b9e-357">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="23b9e-358">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="23b9e-358">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-359">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="23b9e-359">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-360">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23b9e-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-362">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="23b9e-362">Provides high level status information.</span></span> <span data-ttu-id="23b9e-363">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="23b9e-363">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="23b9e-364">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="23b9e-364">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="23b9e-365">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="23b9e-365">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="23b9e-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="23b9e-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-367"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="23b9e-367"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="23b9e-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="23b9e-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="23b9e-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="23b9e-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="23b9e-372">)</span><span class="sxs-lookup"><span data-stu-id="23b9e-372">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="23b9e-373">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="23b9e-373">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-374">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23b9e-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-376">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="23b9e-376">The last requested or desired state for the element.</span></span> <span data-ttu-id="23b9e-377">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="23b9e-377">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="23b9e-378">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="23b9e-378">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="23b9e-379">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="23b9e-379">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="23b9e-380">Valor</span><span class="sxs-lookup"><span data-stu-id="23b9e-380">Value</span></span>                                                                         | <span data-ttu-id="23b9e-381">Significado</span><span class="sxs-lookup"><span data-stu-id="23b9e-381">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="23b9e-382"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="23b9e-382"><dt>12</dt></span></span> </dl> | <span data-ttu-id="23b9e-383">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="23b9e-383">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="23b9e-384">**Status**</span><span class="sxs-lookup"><span data-stu-id="23b9e-384">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-385">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="23b9e-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-386">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-386">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-387">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="23b9e-387">The current status of the object.</span></span> <span data-ttu-id="23b9e-388">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="23b9e-388">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-389">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="23b9e-389">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-390">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="23b9e-390">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-391">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-392">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="23b9e-392">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="23b9e-393">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como "OK".</span><span class="sxs-lookup"><span data-stu-id="23b9e-393">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-394">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="23b9e-394">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-395">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23b9e-395">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-396">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-397">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="23b9e-397">The current state of the logical device.</span></span> <span data-ttu-id="23b9e-398">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="23b9e-398">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-399">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="23b9e-399">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-400">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="23b9e-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-401">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-401">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-402">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="23b9e-402">The scoping system's creation class name.</span></span> <span data-ttu-id="23b9e-403">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="23b9e-403">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-404">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="23b9e-404">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-405">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="23b9e-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-406">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-407">O identificador exclusivo para a máquina virtual de escopo.</span><span class="sxs-lookup"><span data-stu-id="23b9e-407">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="23b9e-408">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="23b9e-408">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-409">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="23b9e-409">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-410">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="23b9e-410">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-411">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-412">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="23b9e-412">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="23b9e-413">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="23b9e-413">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-414">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="23b9e-414">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-415">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="23b9e-415">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-416">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-417">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="23b9e-417">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="23b9e-418">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="23b9e-418">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="23b9e-419">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="23b9e-419">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23b9e-420">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23b9e-420">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23b9e-421">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23b9e-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23b9e-422">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="23b9e-422">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="23b9e-423">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="23b9e-423">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23b9e-424">Comentários</span><span class="sxs-lookup"><span data-stu-id="23b9e-424">Remarks</span></span>

<span data-ttu-id="23b9e-425">O acesso à classe **Msvm \_ SCSIProtocolController** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="23b9e-425">Access to the **Msvm\_SCSIProtocolController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="23b9e-426">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="23b9e-426">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="23b9e-427">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23b9e-427">Requirements</span></span>



| <span data-ttu-id="23b9e-428">Requisito</span><span class="sxs-lookup"><span data-stu-id="23b9e-428">Requirement</span></span> | <span data-ttu-id="23b9e-429">Valor</span><span class="sxs-lookup"><span data-stu-id="23b9e-429">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23b9e-430">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23b9e-430">Minimum supported client</span></span><br/> | <span data-ttu-id="23b9e-431">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="23b9e-431">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="23b9e-432">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23b9e-432">Minimum supported server</span></span><br/> | <span data-ttu-id="23b9e-433">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="23b9e-433">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="23b9e-434">Namespace</span><span class="sxs-lookup"><span data-stu-id="23b9e-434">Namespace</span></span><br/>                | <span data-ttu-id="23b9e-435">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="23b9e-435">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="23b9e-436">MOF</span><span class="sxs-lookup"><span data-stu-id="23b9e-436">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23b9e-437"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="23b9e-437"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="23b9e-438">DLL</span><span class="sxs-lookup"><span data-stu-id="23b9e-438">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23b9e-439"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="23b9e-439"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="23b9e-440">Confira também</span><span class="sxs-lookup"><span data-stu-id="23b9e-440">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23b9e-441">**\_SCSIPROTOCOLCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="23b9e-441">**CIM\_SCSIProtocolController**</span></span>](cim-scsiprotocolcontroller.md)
</dt> <dt>

[<span data-ttu-id="23b9e-442">**\_SCSIPROTOCOLCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="23b9e-442">**CIM\_SCSIProtocolController**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)
</dt> <dt>

[<span data-ttu-id="23b9e-443">Classes de armazenamento</span><span class="sxs-lookup"><span data-stu-id="23b9e-443">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

