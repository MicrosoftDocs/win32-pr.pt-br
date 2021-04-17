---
description: Representa o estado do serviço de Serviço de Cópias de Sombra de Volume (VSS), que implementa o solicitante VSS no sistema operacional convidado.
ms.assetid: 4DD38929-1E3F-4105-BC1A-B367516F7B6E
title: Classe Msvm_VssComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssComponent
- Msvm_VssComponent.SetPowerState
- Msvm_VssComponent.EnableDevice
- Msvm_VssComponent.OnlineDevice
- Msvm_VssComponent.QuiesceDevice
- Msvm_VssComponent.SaveProperties
- Msvm_VssComponent.RestoreProperties
- Msvm_VssComponent.InstanceID
- Msvm_VssComponent.Caption
- Msvm_VssComponent.Description
- Msvm_VssComponent.ElementName
- Msvm_VssComponent.InstallDate
- Msvm_VssComponent.Name
- Msvm_VssComponent.OperationalStatus
- Msvm_VssComponent.StatusDescriptions
- Msvm_VssComponent.Status
- Msvm_VssComponent.HealthState
- Msvm_VssComponent.CommunicationStatus
- Msvm_VssComponent.DetailedStatus
- Msvm_VssComponent.OperatingStatus
- Msvm_VssComponent.PrimaryStatus
- Msvm_VssComponent.EnabledState
- Msvm_VssComponent.OtherEnabledState
- Msvm_VssComponent.RequestedState
- Msvm_VssComponent.EnabledDefault
- Msvm_VssComponent.TimeOfLastStateChange
- Msvm_VssComponent.AvailableRequestedStates
- Msvm_VssComponent.TransitioningToState
- Msvm_VssComponent.SystemCreationClassName
- Msvm_VssComponent.SystemName
- Msvm_VssComponent.CreationClassName
- Msvm_VssComponent.DeviceID
- Msvm_VssComponent.PowerManagementSupported
- Msvm_VssComponent.PowerManagementCapabilities
- Msvm_VssComponent.Availability
- Msvm_VssComponent.StatusInfo
- Msvm_VssComponent.LastErrorCode
- Msvm_VssComponent.ErrorDescription
- Msvm_VssComponent.ErrorCleared
- Msvm_VssComponent.OtherIdentifyingInfo
- Msvm_VssComponent.PowerOnHours
- Msvm_VssComponent.TotalPowerOnHours
- Msvm_VssComponent.IdentifyingDescriptions
- Msvm_VssComponent.AdditionalAvailability
- Msvm_VssComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab4039ce110af9fa023a662c31d1f9962b080e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783289"
---
# <a name="msvm_vsscomponent-class"></a><span data-ttu-id="13673-103">\_Classe Msvm VssComponent</span><span class="sxs-lookup"><span data-stu-id="13673-103">Msvm\_VssComponent class</span></span>

<span data-ttu-id="13673-104">Representa o estado do serviço de Serviço de Cópias de Sombra de Volume (VSS), que implementa o solicitante VSS no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="13673-104">Represents the state of the Volume Shadow Copy Service (VSS) service, which implements the VSS Requester in the guest operating system.</span></span>

<span data-ttu-id="13673-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="13673-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="13673-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="13673-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "VSS";
  string   Description = "Microsoft VSS Service";
  string   ElementName = "VSS";
  datetime InstallDate;
  string   Name = "VSS";
  uint16   OperationalStatus[] = { 2 };
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
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_VssComponent";
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
  uint16   AdditionalAvailability[] = {6};
  uint64   MaxQuiesceTime;
};
```

## <a name="members"></a><span data-ttu-id="13673-107">Membros</span><span class="sxs-lookup"><span data-stu-id="13673-107">Members</span></span>

<span data-ttu-id="13673-108">A classe **Msvm \_ VssComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="13673-108">The **Msvm\_VssComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="13673-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="13673-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="13673-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="13673-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="13673-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="13673-111">Methods</span></span>

<span data-ttu-id="13673-112">A classe **Msvm \_ VssComponent** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="13673-112">The **Msvm\_VssComponent** class has these methods.</span></span>



| <span data-ttu-id="13673-113">Método</span><span class="sxs-lookup"><span data-stu-id="13673-113">Method</span></span>                                                             | <span data-ttu-id="13673-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="13673-114">Description</span></span>                              |
|:-------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="13673-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="13673-115">**EnableDevice**</span></span>                                                   | <span data-ttu-id="13673-116">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="13673-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="13673-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="13673-117">**OnlineDevice**</span></span>                                                   | <span data-ttu-id="13673-118">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="13673-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="13673-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="13673-119">**QuiesceDevice**</span></span>                                                  | <span data-ttu-id="13673-120">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="13673-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="13673-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="13673-121">**RequestStateChange**</span></span>](msvm-vsscomponent-requeststatechange.md) | <span data-ttu-id="13673-122">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="13673-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="13673-123">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="13673-123">**Reset**</span></span>](msvm-vsscomponent-reset.md)                           | <span data-ttu-id="13673-124">Redefine o dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="13673-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="13673-125">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="13673-125">**RestoreProperties**</span></span>                                              | <span data-ttu-id="13673-126">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="13673-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="13673-127">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="13673-127">**SaveProperties**</span></span>                                                 | <span data-ttu-id="13673-128">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="13673-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="13673-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="13673-129">**SetPowerState**</span></span>                                                  | <span data-ttu-id="13673-130">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="13673-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="13673-131">Propriedades</span><span class="sxs-lookup"><span data-stu-id="13673-131">Properties</span></span>

<span data-ttu-id="13673-132">A classe **Msvm \_ VssComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="13673-132">The **Msvm\_VssComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13673-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="13673-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-134">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13673-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="13673-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-136">Qualquer disponibilidade e status adicionais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13673-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="13673-137">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="13673-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="13673-138">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="13673-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-139">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13673-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13673-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-141">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13673-141">The primary availability and status of the device.</span></span> <span data-ttu-id="13673-142">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="13673-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="13673-143">Valor</span><span class="sxs-lookup"><span data-stu-id="13673-143">Value</span></span>                                                                        | <span data-ttu-id="13673-144">Significado</span><span class="sxs-lookup"><span data-stu-id="13673-144">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="13673-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="13673-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="13673-146">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="13673-146">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="13673-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="13673-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-148">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13673-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="13673-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-150">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="13673-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="13673-151">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="13673-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="13673-152">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="13673-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="13673-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13673-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-155">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="13673-155">A short description of the object.</span></span> <span data-ttu-id="13673-156">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="13673-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="13673-157">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="13673-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-158">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13673-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13673-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-160">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="13673-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="13673-161">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="13673-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="13673-162">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="13673-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="13673-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="13673-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="13673-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="13673-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="13673-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="13673-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="13673-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="13673-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="13673-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="13673-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="13673-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="13673-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="13673-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="13673-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="13673-170">)</span><span class="sxs-lookup"><span data-stu-id="13673-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="13673-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="13673-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-172">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="13673-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13673-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-174">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="13673-174">The scoping system's creation class name.</span></span> <span data-ttu-id="13673-175">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="13673-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="13673-176">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="13673-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="13673-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13673-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-179">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="13673-179">A description of the object.</span></span> <span data-ttu-id="13673-180">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="13673-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="13673-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="13673-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-182">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13673-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13673-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-184">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="13673-184">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="13673-185">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="13673-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="13673-186">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="13673-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="13673-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="13673-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="13673-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="13673-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="13673-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="13673-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="13673-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="13673-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="13673-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="13673-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="13673-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="13673-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="13673-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="13673-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="13673-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="13673-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="13673-195">)</span><span class="sxs-lookup"><span data-stu-id="13673-195">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="13673-196">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="13673-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-197">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="13673-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13673-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-199">Um endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="13673-199">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="13673-200">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como "Microsoft:*VMGUID* \\ *GUID*", em *que VMGUID* é a propriedade **Name** do [**Msvm \_ ComputerSystem**](msvm-computersystem.md) associado a este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13673-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="13673-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="13673-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-202">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="13673-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13673-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-204">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="13673-204">A display name for the object.</span></span> <span data-ttu-id="13673-205">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="13673-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="13673-206">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="13673-206">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-207">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13673-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13673-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-209">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 7 (não padrão).</span><span class="sxs-lookup"><span data-stu-id="13673-209">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 7 (No Default).</span></span>



| <span data-ttu-id="13673-210">Valor</span><span class="sxs-lookup"><span data-stu-id="13673-210">Value</span></span>                                                                        | <span data-ttu-id="13673-211">Significado</span><span class="sxs-lookup"><span data-stu-id="13673-211">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="13673-212"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="13673-212"><dt>2</dt></span></span> </dl> | <span data-ttu-id="13673-213">habilitado</span><span class="sxs-lookup"><span data-stu-id="13673-213">Enabled</span></span><br/>    |
| <dl> <span data-ttu-id="13673-214"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="13673-214"><dt>3</dt></span></span> </dl> | <span data-ttu-id="13673-215">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="13673-215">Disabled</span></span><br/>   |
| <dl> <span data-ttu-id="13673-216"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="13673-216"><dt>7</dt></span></span> </dl> | <span data-ttu-id="13673-217">Nenhum padrão</span><span class="sxs-lookup"><span data-stu-id="13673-217">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="13673-218">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="13673-218">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-219">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13673-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13673-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-221">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="13673-221">The enabled and disabled states of an element.</span></span> <span data-ttu-id="13673-222">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="13673-222">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="13673-223">Valor</span><span class="sxs-lookup"><span data-stu-id="13673-223">Value</span></span>                                                                        | <span data-ttu-id="13673-224">Significado</span><span class="sxs-lookup"><span data-stu-id="13673-224">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="13673-225"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="13673-225"><dt>2</dt></span></span> </dl> | <span data-ttu-id="13673-226">habilitado</span><span class="sxs-lookup"><span data-stu-id="13673-226">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="13673-227"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="13673-227"><dt>3</dt></span></span> </dl> | <span data-ttu-id="13673-228">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="13673-228">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="13673-229">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="13673-229">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-230">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="13673-230">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="13673-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-232">Indica se o erro relatado em **LastErrorCode** agora está limpo.</span><span class="sxs-lookup"><span data-stu-id="13673-232">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="13673-233">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="13673-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="13673-234">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="13673-234">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-235">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="13673-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13673-236">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-237">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="13673-237">A string that provides more information about the error recorded in **LastErrorCode**, and information on any corrective actions that can be taken.</span></span> <span data-ttu-id="13673-238">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="13673-238">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="13673-239">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="13673-239">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-240">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13673-240">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13673-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-242">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="13673-242">The current health of the element.</span></span> <span data-ttu-id="13673-243">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="13673-243">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="13673-244">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="13673-244">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="13673-245">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="13673-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="13673-246">Valor</span><span class="sxs-lookup"><span data-stu-id="13673-246">Value</span></span>                                                                        | <span data-ttu-id="13673-247">Significado</span><span class="sxs-lookup"><span data-stu-id="13673-247">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="13673-248"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="13673-248"><dt>5</dt></span></span> </dl> | <span data-ttu-id="13673-249">OK</span><span class="sxs-lookup"><span data-stu-id="13673-249">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="13673-250">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="13673-250">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-251">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="13673-251">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="13673-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-253">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="13673-253">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="13673-254">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="13673-254">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="13673-255">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="13673-255">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-256">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="13673-256">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="13673-257">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-258">A data e a hora em que o serviço de integração foi instalado na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="13673-258">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="13673-259">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="13673-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="13673-260">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="13673-260">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-261">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="13673-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13673-262">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13673-263">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="13673-263">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="13673-264">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="13673-264">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="13673-265">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="13673-265">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="13673-266">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="13673-266">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-267">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13673-267">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13673-268">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-269">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="13673-269">The last error code reported by the logical device.</span></span> <span data-ttu-id="13673-270">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="13673-270">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="13673-271">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="13673-271">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-272">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="13673-272">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="13673-273">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-274">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="13673-274">This property has been deprecated.</span></span> <span data-ttu-id="13673-275">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="13673-275">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="13673-276">**Nome**</span><span class="sxs-lookup"><span data-stu-id="13673-276">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-277">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="13673-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13673-278">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-279">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="13673-279">The label by which the object is known.</span></span> <span data-ttu-id="13673-280">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="13673-280">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="13673-281">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="13673-281">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-282">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13673-282">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13673-283">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-284">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="13673-284">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="13673-285">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="13673-285">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="13673-286">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="13673-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="13673-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="13673-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="13673-288"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="13673-288"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="13673-289"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="13673-289"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="13673-290"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="13673-290"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="13673-291"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="13673-291"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="13673-292"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="13673-292"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="13673-293"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="13673-293"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="13673-294"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="13673-294"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="13673-295"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="13673-295"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="13673-296"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="13673-296"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="13673-297"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="13673-297"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="13673-298"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="13673-298"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="13673-299"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="13673-299"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="13673-300"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="13673-300"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="13673-301"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="13673-301"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="13673-302"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="13673-302"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="13673-303"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="13673-303"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="13673-304"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="13673-304"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="13673-305"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="13673-305"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="13673-306">)</span><span class="sxs-lookup"><span data-stu-id="13673-306">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="13673-307">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="13673-307">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-308">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13673-308">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="13673-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-310">O status atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="13673-310">The current status of the element.</span></span> <span data-ttu-id="13673-311">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="13673-311">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="13673-312">A seguir estão os valores possíveis para o  \[ valor da \] Propriedade OperationalStatus 0.</span><span class="sxs-lookup"><span data-stu-id="13673-312">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="13673-313">Valor</span><span class="sxs-lookup"><span data-stu-id="13673-313">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="13673-314">Significado</span><span class="sxs-lookup"><span data-stu-id="13673-314">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="13673-315"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="13673-315"><dt>{ 2 }</dt></span></span> </dl>                                                                                                                                                                                                    |                                                                                                                                                                                                                                          |
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="13673-316"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="13673-316"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="13673-317">O serviço está funcionando normalmente.</span><span class="sxs-lookup"><span data-stu-id="13673-317">The service is operating normally.</span></span> <span data-ttu-id="13673-318">Os  \[ valores de \] Propriedade OperationalStatus 1 e **StatusDescriptions** \[ 1 \] podem conter mais informações.</span><span class="sxs-lookup"><span data-stu-id="13673-318">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="13673-319"><dt>**Degradado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="13673-319"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="13673-320">O serviço está funcionando normalmente, mas o serviço convidado negocia uma versão de protocolo de comunicação compatível.</span><span class="sxs-lookup"><span data-stu-id="13673-320">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="13673-321">Os  \[ valores de \] Propriedade OperationalStatus 1 e **StatusDescriptions** \[ 1 \] podem conter mais informações.</span><span class="sxs-lookup"><span data-stu-id="13673-321">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="13673-322"><dt>**Erro não recuperável**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="13673-322"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="13673-323">O convidado não oferece suporte a uma versão de protocolo compatível.</span><span class="sxs-lookup"><span data-stu-id="13673-323">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="13673-324">Os  \[ valores de \] Propriedade OperationalStatus 1 e **StatusDescriptions** \[ 1 \] podem conter mais informações.</span><span class="sxs-lookup"><span data-stu-id="13673-324">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="13673-325"><dt>**Nenhum contato**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="13673-325"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="13673-326">O serviço convidado não está instalado ou ainda não foi contatado.</span><span class="sxs-lookup"><span data-stu-id="13673-326">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="13673-327"><dt>**Comunicação perdida**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="13673-327"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="13673-328">O serviço convidado não está mais respondendo normalmente.</span><span class="sxs-lookup"><span data-stu-id="13673-328">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="13673-329">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="13673-329">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-330">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="13673-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13673-331">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-332">O estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="13673-332">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="13673-333">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="13673-333">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="13673-334">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="13673-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="13673-335">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="13673-335">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-336">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="13673-336">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="13673-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-338">Dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="13673-338">Additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="13673-339">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="13673-339">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="13673-340">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="13673-340">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-341">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13673-341">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="13673-342">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-343">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13673-343">The power management capabilities of the device.</span></span> <span data-ttu-id="13673-344">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="13673-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="13673-345">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="13673-345">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-346">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="13673-346">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="13673-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-348">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="13673-348">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="13673-349">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="13673-349">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="13673-350">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="13673-350">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-351">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="13673-351">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="13673-352">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-353">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="13673-353">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="13673-354">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="13673-354">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="13673-355">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="13673-355">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-356">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13673-356">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13673-357">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-358">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="13673-358">Provides high level status information.</span></span> <span data-ttu-id="13673-359">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="13673-359">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="13673-360">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="13673-360">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="13673-361">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="13673-361">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="13673-362"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="13673-362"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="13673-363"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="13673-363"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="13673-364"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="13673-364"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="13673-365"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="13673-365"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="13673-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="13673-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="13673-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="13673-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="13673-368">)</span><span class="sxs-lookup"><span data-stu-id="13673-368">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="13673-369">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="13673-369">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-370">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13673-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13673-371">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-372">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="13673-372">The last requested or desired state for the element.</span></span> <span data-ttu-id="13673-373">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="13673-373">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="13673-374">Valor</span><span class="sxs-lookup"><span data-stu-id="13673-374">Value</span></span>                                                                         | <span data-ttu-id="13673-375">Significado</span><span class="sxs-lookup"><span data-stu-id="13673-375">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="13673-376"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="13673-376"><dt>12</dt></span></span> </dl> | <span data-ttu-id="13673-377">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="13673-377">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="13673-378">**Status**</span><span class="sxs-lookup"><span data-stu-id="13673-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-379">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="13673-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13673-380">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-381">Uma cadeia de caracteres que especifica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="13673-381">A string that specifies the current status of the object.</span></span> <span data-ttu-id="13673-382">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) , mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="13673-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="13673-383">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="13673-383">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-384">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="13673-384">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="13673-385">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-386">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="13673-386">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="13673-387">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="13673-387">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="13673-388">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="13673-388">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-389">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13673-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13673-390">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-391">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="13673-391">The current state of the logical device.</span></span> <span data-ttu-id="13673-392">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="13673-392">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="13673-393">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="13673-393">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-394">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="13673-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13673-395">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-396">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="13673-396">The scoping system's creation class name.</span></span> <span data-ttu-id="13673-397">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="13673-397">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="13673-398">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="13673-398">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-399">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="13673-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13673-400">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-401">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="13673-401">The scoping system's name.</span></span> <span data-ttu-id="13673-402">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="13673-402">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="13673-403">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="13673-403">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-404">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="13673-404">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="13673-405">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-406">A data ou a hora em que o **enabledstate** do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="13673-406">The date or time when the **EnabledState** of the element last changed.</span></span> <span data-ttu-id="13673-407">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="13673-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="13673-408">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="13673-408">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-409">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="13673-409">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="13673-410">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-411">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="13673-411">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="13673-412">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="13673-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="13673-413">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="13673-413">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13673-414">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13673-414">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13673-415">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13673-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13673-416">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="13673-416">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="13673-417">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="13673-417">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="13673-418">Valor</span><span class="sxs-lookup"><span data-stu-id="13673-418">Value</span></span>                                                                         | <span data-ttu-id="13673-419">Significado</span><span class="sxs-lookup"><span data-stu-id="13673-419">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="13673-420"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="13673-420"><dt>12</dt></span></span> </dl> | <span data-ttu-id="13673-421">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="13673-421">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13673-422">Comentários</span><span class="sxs-lookup"><span data-stu-id="13673-422">Remarks</span></span>

<span data-ttu-id="13673-423">O acesso à classe **Msvm \_ VssComponent** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="13673-423">Access to the **Msvm\_VssComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="13673-424">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="13673-424">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="13673-425">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13673-425">Requirements</span></span>



| <span data-ttu-id="13673-426">Requisito</span><span class="sxs-lookup"><span data-stu-id="13673-426">Requirement</span></span> | <span data-ttu-id="13673-427">Valor</span><span class="sxs-lookup"><span data-stu-id="13673-427">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13673-428">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13673-428">Minimum supported client</span></span><br/> | <span data-ttu-id="13673-429">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="13673-429">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="13673-430">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13673-430">Minimum supported server</span></span><br/> | <span data-ttu-id="13673-431">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="13673-431">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="13673-432">Namespace</span><span class="sxs-lookup"><span data-stu-id="13673-432">Namespace</span></span><br/>                | <span data-ttu-id="13673-433">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="13673-433">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="13673-434">MOF</span><span class="sxs-lookup"><span data-stu-id="13673-434">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13673-435"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13673-435"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="13673-436">DLL</span><span class="sxs-lookup"><span data-stu-id="13673-436">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13673-437"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="13673-437"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="13673-438">Confira também</span><span class="sxs-lookup"><span data-stu-id="13673-438">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13673-439">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="13673-439">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="13673-440">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="13673-440">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

