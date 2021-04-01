---
description: Representa o estado do serviço de troca de pares chave/valor, que fornece um mecanismo para trocar dados entre a máquina virtual e o sistema operacional em execução no sistema operacional de gerenciamento.
ms.assetid: AA68BC74-A919-4029-B703-E08F00449F20
title: Classe Msvm_KvpExchangeComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeComponent
- Msvm_KvpExchangeComponent.SetPowerState
- Msvm_KvpExchangeComponent.EnableDevice
- Msvm_KvpExchangeComponent.OnlineDevice
- Msvm_KvpExchangeComponent.QuiesceDevice
- Msvm_KvpExchangeComponent.SaveProperties
- Msvm_KvpExchangeComponent.RestoreProperties
- Msvm_KvpExchangeComponent.InstanceID
- Msvm_KvpExchangeComponent.Caption
- Msvm_KvpExchangeComponent.Description
- Msvm_KvpExchangeComponent.ElementName
- Msvm_KvpExchangeComponent.InstallDate
- Msvm_KvpExchangeComponent.Name
- Msvm_KvpExchangeComponent.OperationalStatus
- Msvm_KvpExchangeComponent.StatusDescriptions
- Msvm_KvpExchangeComponent.Status
- Msvm_KvpExchangeComponent.HealthState
- Msvm_KvpExchangeComponent.CommunicationStatus
- Msvm_KvpExchangeComponent.DetailedStatus
- Msvm_KvpExchangeComponent.OperatingStatus
- Msvm_KvpExchangeComponent.PrimaryStatus
- Msvm_KvpExchangeComponent.EnabledState
- Msvm_KvpExchangeComponent.OtherEnabledState
- Msvm_KvpExchangeComponent.RequestedState
- Msvm_KvpExchangeComponent.EnabledDefault
- Msvm_KvpExchangeComponent.TimeOfLastStateChange
- Msvm_KvpExchangeComponent.AvailableRequestedStates
- Msvm_KvpExchangeComponent.TransitioningToState
- Msvm_KvpExchangeComponent.SystemCreationClassName
- Msvm_KvpExchangeComponent.SystemName
- Msvm_KvpExchangeComponent.CreationClassName
- Msvm_KvpExchangeComponent.DeviceID
- Msvm_KvpExchangeComponent.PowerManagementSupported
- Msvm_KvpExchangeComponent.PowerManagementCapabilities
- Msvm_KvpExchangeComponent.Availability
- Msvm_KvpExchangeComponent.StatusInfo
- Msvm_KvpExchangeComponent.LastErrorCode
- Msvm_KvpExchangeComponent.ErrorDescription
- Msvm_KvpExchangeComponent.ErrorCleared
- Msvm_KvpExchangeComponent.OtherIdentifyingInfo
- Msvm_KvpExchangeComponent.PowerOnHours
- Msvm_KvpExchangeComponent.TotalPowerOnHours
- Msvm_KvpExchangeComponent.IdentifyingDescriptions
- Msvm_KvpExchangeComponent.AdditionalAvailability
- Msvm_KvpExchangeComponent.MaxQuiesceTime
- Msvm_KvpExchangeComponent.GuestExchangeItems
- Msvm_KvpExchangeComponent.GuestIntrinsicExchangeItems
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e3aa7f269d24c284eef3ad2c519f5fdbf48513a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837136"
---
# <a name="msvm_kvpexchangecomponent-class"></a><span data-ttu-id="d9891-103">\_Classe Msvm KvpExchangeComponent</span><span class="sxs-lookup"><span data-stu-id="d9891-103">Msvm\_KvpExchangeComponent class</span></span>

<span data-ttu-id="d9891-104">Representa o estado do serviço de troca de pares chave/valor, que fornece um mecanismo para trocar dados entre a máquina virtual e o sistema operacional em execução no sistema operacional de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="d9891-104">Represents the state of the key/value pair exchange service, which provides a mechanism to exchange data between the virtual machine and the operating system running on the management operating system.</span></span>

<span data-ttu-id="d9891-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d9891-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9891-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d9891-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_KvpExchangeComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Key-Value Pair Exchange";
  string   Description = "Microsoft Key-Value Pair Exchange Service";
  string   ElementName = "Key-Value pair Exchange";
  datetime InstallDate;
  string   Name = "Key-Value Pair Exchange";
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 7;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_KvpExchangeComponent";
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
  string   GuestExchangeItems[];
  string   GuestIntrinsicExchangeItems[];
};
```

## <a name="members"></a><span data-ttu-id="d9891-107">Membros</span><span class="sxs-lookup"><span data-stu-id="d9891-107">Members</span></span>

<span data-ttu-id="d9891-108">A classe **Msvm \_ KvpExchangeComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d9891-108">The **Msvm\_KvpExchangeComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="d9891-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="d9891-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="d9891-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d9891-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d9891-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="d9891-111">Methods</span></span>

<span data-ttu-id="d9891-112">A classe **Msvm \_ KvpExchangeComponent** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d9891-112">The **Msvm\_KvpExchangeComponent** class has these methods.</span></span>



| <span data-ttu-id="d9891-113">Método</span><span class="sxs-lookup"><span data-stu-id="d9891-113">Method</span></span>                                                                     | <span data-ttu-id="d9891-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="d9891-114">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="d9891-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="d9891-115">**EnableDevice**</span></span>                                                           | <span data-ttu-id="d9891-116">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d9891-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d9891-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="d9891-117">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="d9891-118">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d9891-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d9891-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="d9891-119">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="d9891-120">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d9891-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="d9891-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="d9891-121">**RequestStateChange**</span></span>](msvm-kvpexchangecomponent-requeststatechange.md) | <span data-ttu-id="d9891-122">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="d9891-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="d9891-123">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="d9891-123">**Reset**</span></span>](msvm-kvpexchangecomponent-reset.md)                           | <span data-ttu-id="d9891-124">Redefine o componente.</span><span class="sxs-lookup"><span data-stu-id="d9891-124">Resets the component.</span></span><br/>         |
| <span data-ttu-id="d9891-125">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="d9891-125">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="d9891-126">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d9891-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d9891-127">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="d9891-127">**SaveProperties**</span></span>                                                         | <span data-ttu-id="d9891-128">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d9891-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d9891-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d9891-129">**SetPowerState**</span></span>                                                          | <span data-ttu-id="d9891-130">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d9891-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d9891-131">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d9891-131">Properties</span></span>

<span data-ttu-id="d9891-132">A classe **Msvm \_ KvpExchangeComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d9891-132">The **Msvm\_KvpExchangeComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d9891-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="d9891-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-134">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d9891-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d9891-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-136">Qualquer disponibilidade e status adicionais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d9891-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="d9891-137">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d9891-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="d9891-138">Valor</span><span class="sxs-lookup"><span data-stu-id="d9891-138">Value</span></span>                                                                            | <span data-ttu-id="d9891-139">Significado</span><span class="sxs-lookup"><span data-stu-id="d9891-139">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="d9891-140"><dt>152</dt></span><span class="sxs-lookup"><span data-stu-id="d9891-140"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="d9891-141"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d9891-141"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="d9891-142">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="d9891-142">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d9891-143">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="d9891-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-144">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d9891-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-146">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d9891-146">The primary availability and status of the device.</span></span> <span data-ttu-id="d9891-147">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d9891-147">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="d9891-148">Valor</span><span class="sxs-lookup"><span data-stu-id="d9891-148">Value</span></span>                                                                        | <span data-ttu-id="d9891-149">Significado</span><span class="sxs-lookup"><span data-stu-id="d9891-149">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="d9891-150"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d9891-150"><dt>6</dt></span></span> </dl> | <span data-ttu-id="d9891-151">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="d9891-151">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d9891-152">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="d9891-152">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-153">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d9891-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d9891-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-155">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="d9891-155">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="d9891-156">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d9891-156">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9891-157">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="d9891-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9891-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-160">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="d9891-160">A short description of the object.</span></span> <span data-ttu-id="d9891-161">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d9891-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d9891-162">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="d9891-162">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-163">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d9891-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-165">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="d9891-165">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="d9891-166">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="d9891-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d9891-167">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d9891-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d9891-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d9891-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="d9891-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="d9891-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="d9891-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="d9891-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d9891-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d9891-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d9891-175">)</span><span class="sxs-lookup"><span data-stu-id="d9891-175">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d9891-176">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d9891-176">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9891-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-179">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="d9891-179">The scoping system's creation class name.</span></span> <span data-ttu-id="d9891-180">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d9891-180">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d9891-181">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d9891-181">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9891-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-184">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="d9891-184">A description of the object.</span></span> <span data-ttu-id="d9891-185">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d9891-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d9891-186">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="d9891-186">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-187">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d9891-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-189">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="d9891-189">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="d9891-190">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="d9891-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d9891-191">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d9891-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d9891-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="d9891-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="d9891-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="d9891-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="d9891-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="d9891-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="d9891-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d9891-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d9891-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d9891-200">)</span><span class="sxs-lookup"><span data-stu-id="d9891-200">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d9891-201">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d9891-201">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-202">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9891-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-204">Um endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d9891-204">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="d9891-205">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d9891-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d9891-206">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d9891-206">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-207">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9891-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-209">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="d9891-209">A display name for the object.</span></span> <span data-ttu-id="d9891-210">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d9891-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d9891-211">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="d9891-211">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-212">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d9891-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-214">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d9891-214">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="d9891-215">Valor</span><span class="sxs-lookup"><span data-stu-id="d9891-215">Value</span></span>                                                                        | <span data-ttu-id="d9891-216">Significado</span><span class="sxs-lookup"><span data-stu-id="d9891-216">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="d9891-217"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="d9891-217"><dt>7</dt></span></span> </dl> | <span data-ttu-id="d9891-218">Nenhum padrão</span><span class="sxs-lookup"><span data-stu-id="d9891-218">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d9891-219">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d9891-219">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-220">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d9891-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-221">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-222">O estado habilitado do elemento.</span><span class="sxs-lookup"><span data-stu-id="d9891-222">The enabled state of the element.</span></span> <span data-ttu-id="d9891-223">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d9891-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="d9891-224"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="d9891-224"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-225"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="d9891-225"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d9891-226">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d9891-226">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-227">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d9891-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-229">Indica se o erro relatado na propriedade **LastErrorCode** agora está apagado.</span><span class="sxs-lookup"><span data-stu-id="d9891-229">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="d9891-230">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d9891-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9891-231">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d9891-231">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-232">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9891-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-234">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado na propriedade **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="d9891-234">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="d9891-235">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d9891-235">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9891-236">**GuestExchangeItems**</span><span class="sxs-lookup"><span data-stu-id="d9891-236">**GuestExchangeItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-237">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9891-237">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d9891-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9891-239">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), **HyperVEmbeddedInstance** ("Msvm \_ KvpExchangeDataItem")</span><span class="sxs-lookup"><span data-stu-id="d9891-239">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="d9891-240">Uma matriz de instâncias [**de \_ KvpExchangeDataItem Msvm**](msvm-kvpexchangedataitem.md) inseridas que contêm o conjunto de pares chave-valor que os serviços em execução no sistema operacional convidado foram disponibilizados para acesso por clientes externos.</span><span class="sxs-lookup"><span data-stu-id="d9891-240">An array of embedded [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances which contain the set of key-value pairs that services running within the guest operating system have pushed up to be available for access by external clients.</span></span> <span data-ttu-id="d9891-241">Essa matriz não conterá nenhum item intrínseco enviado diretamente pelo serviço de integração.</span><span class="sxs-lookup"><span data-stu-id="d9891-241">This array will not contain any intrinsic items that are pushed by the integration service directly.</span></span>

</dd> <dt>

<span data-ttu-id="d9891-242">**GuestIntrinsicExchangeItems**</span><span class="sxs-lookup"><span data-stu-id="d9891-242">**GuestIntrinsicExchangeItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-243">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9891-243">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d9891-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9891-245">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), **HyperVEmbeddedInstance** ("Msvm \_ KvpExchangeDataItem")</span><span class="sxs-lookup"><span data-stu-id="d9891-245">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="d9891-246">Uma matriz de instâncias do [**Msvm \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) inseridas que contêm o conjunto de pares chave-valor que o sistema operacional convidado propagau para estar disponível para acesso por clientes externos.</span><span class="sxs-lookup"><span data-stu-id="d9891-246">An array of embedded [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances which contain the set of key-value pairs that the guest operating system has pushed up to be available for access by external clients.</span></span> <span data-ttu-id="d9891-247">Essa matriz não conterá nenhum item de dados Enviado por outros serviços em execução no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="d9891-247">This array will not contain any data items pushed by other services running within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="d9891-248">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="d9891-248">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-249">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d9891-249">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-250">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-251">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="d9891-251">The current health of the element.</span></span> <span data-ttu-id="d9891-252">Isso expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="d9891-252">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="d9891-253">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="d9891-253">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="d9891-254">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d9891-254">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d9891-255">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d9891-255">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-256">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9891-256">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d9891-257">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-258">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz de propriedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="d9891-258">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="d9891-259">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d9891-259">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9891-260">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d9891-260">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-261">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d9891-261">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-262">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-263">A data e a hora em que o serviço de integração foi instalado na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d9891-263">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="d9891-264">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d9891-264">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d9891-265">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d9891-265">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-266">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9891-266">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-267">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9891-268">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="d9891-268">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d9891-269">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="d9891-269">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d9891-270">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d9891-270">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d9891-271">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d9891-271">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-272">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d9891-272">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-273">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-274">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d9891-274">The last error code reported by the logical device.</span></span> <span data-ttu-id="d9891-275">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d9891-275">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9891-276">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="d9891-276">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-277">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d9891-277">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-278">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-279">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="d9891-279">This property has been deprecated.</span></span> <span data-ttu-id="d9891-280">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d9891-280">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d9891-281">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d9891-281">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-282">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9891-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-283">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-284">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="d9891-284">The label by which the object is known.</span></span> <span data-ttu-id="d9891-285">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d9891-285">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d9891-286">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="d9891-286">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-287">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d9891-287">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-288">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-289">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="d9891-289">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="d9891-290">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="d9891-290">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d9891-291">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d9891-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d9891-292"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d9891-292"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-293"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="d9891-293"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-294"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="d9891-294"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-295"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="d9891-295"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-296"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="d9891-296"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-297"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="d9891-297"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-298"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="d9891-298"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-299"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="d9891-299"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-300"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="d9891-300"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-301"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="d9891-301"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-302"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="d9891-302"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-303"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="d9891-303"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-304"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="d9891-304"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-305"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="d9891-305"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-306"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="d9891-306"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-307"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="d9891-307"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-308"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="d9891-308"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-309"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d9891-309"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-310"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d9891-310"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d9891-311">)</span><span class="sxs-lookup"><span data-stu-id="d9891-311">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d9891-312">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d9891-312">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-313">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d9891-313">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d9891-314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-315">O status atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="d9891-315">The current status of the element.</span></span> <span data-ttu-id="d9891-316">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d9891-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="d9891-317">A seguir estão os valores possíveis para o  \[ valor da \] Propriedade OperationalStatus 0.</span><span class="sxs-lookup"><span data-stu-id="d9891-317">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="d9891-318">Valor</span><span class="sxs-lookup"><span data-stu-id="d9891-318">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="d9891-319">Significado</span><span class="sxs-lookup"><span data-stu-id="d9891-319">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="d9891-320"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d9891-320"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="d9891-321">O serviço está funcionando normalmente.</span><span class="sxs-lookup"><span data-stu-id="d9891-321">The service is operating normally.</span></span> <span data-ttu-id="d9891-322">Os  \[ valores de \] Propriedade OperationalStatus 1 e **StatusDescriptions** \[ 1 \] podem conter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d9891-322">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="d9891-323"><dt>**Degradado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d9891-323"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="d9891-324">O serviço está funcionando normalmente, mas o serviço convidado negocia uma versão de protocolo de comunicação compatível.</span><span class="sxs-lookup"><span data-stu-id="d9891-324">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="d9891-325">Os  \[ valores de \] Propriedade OperationalStatus 1 e **StatusDescriptions** \[ 1 \] podem conter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d9891-325">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="d9891-326"><dt>**Erro não recuperável**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="d9891-326"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="d9891-327">O convidado não oferece suporte a uma versão de protocolo compatível.</span><span class="sxs-lookup"><span data-stu-id="d9891-327">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="d9891-328">Os  \[ valores de \] Propriedade OperationalStatus 1 e **StatusDescriptions** \[ 1 \] podem conter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d9891-328">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="d9891-329"><dt>**Nenhum contato**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="d9891-329"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="d9891-330">O serviço convidado não está instalado ou ainda não foi contatado.</span><span class="sxs-lookup"><span data-stu-id="d9891-330">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="d9891-331"><dt>**Comunicação perdida**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="d9891-331"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="d9891-332">O serviço convidado não está mais respondendo normalmente.</span><span class="sxs-lookup"><span data-stu-id="d9891-332">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="d9891-333">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="d9891-333">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-334">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9891-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-335">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-336">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="d9891-336">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="d9891-337">Essa propriedade deve ser definida como **NULL** quando a propriedade **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="d9891-337">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="d9891-338">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d9891-338">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d9891-339">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="d9891-339">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-340">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9891-340">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d9891-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-342">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d9891-342">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="d9891-343">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d9891-343">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d9891-344">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d9891-344">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-345">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d9891-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d9891-346">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-347">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d9891-347">The power management capabilities of the device.</span></span> <span data-ttu-id="d9891-348">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d9891-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9891-349">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d9891-349">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-350">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d9891-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-351">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-352">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="d9891-352">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="d9891-353">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d9891-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9891-354">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="d9891-354">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-355">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d9891-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-356">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-357">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="d9891-357">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="d9891-358">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d9891-358">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9891-359">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="d9891-359">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-360">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d9891-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-362">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="d9891-362">Provides high level status information.</span></span> <span data-ttu-id="d9891-363">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="d9891-363">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="d9891-364">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="d9891-364">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d9891-365">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d9891-365">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d9891-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d9891-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-367"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="d9891-367"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="d9891-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="d9891-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d9891-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d9891-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d9891-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d9891-372">)</span><span class="sxs-lookup"><span data-stu-id="d9891-372">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d9891-373">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="d9891-373">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-374">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d9891-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-376">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="d9891-376">The last requested or desired state for the element.</span></span> <span data-ttu-id="d9891-377">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d9891-377">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="d9891-378">Valor</span><span class="sxs-lookup"><span data-stu-id="d9891-378">Value</span></span>                                                                         | <span data-ttu-id="d9891-379">Significado</span><span class="sxs-lookup"><span data-stu-id="d9891-379">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="d9891-380"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="d9891-380"><dt>12</dt></span></span> </dl> | <span data-ttu-id="d9891-381">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="d9891-381">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d9891-382">**Status**</span><span class="sxs-lookup"><span data-stu-id="d9891-382">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-383">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9891-383">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-384">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-385">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="d9891-385">The current status of the object.</span></span> <span data-ttu-id="d9891-386">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) , mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d9891-386">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9891-387">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d9891-387">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-388">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9891-388">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d9891-389">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-390">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="d9891-390">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="d9891-391">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d9891-391">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d9891-392">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d9891-392">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-393">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d9891-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-394">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-395">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d9891-395">The current state of the logical device.</span></span> <span data-ttu-id="d9891-396">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d9891-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9891-397">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d9891-397">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-398">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9891-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-399">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-400">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="d9891-400">The scoping system's creation class name.</span></span> <span data-ttu-id="d9891-401">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d9891-401">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d9891-402">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d9891-402">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-403">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9891-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-404">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-405">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="d9891-405">The scoping system's name.</span></span> <span data-ttu-id="d9891-406">Esse valor corresponde ao valor da propriedade [**Name**](msvm-computersystem.md) da classe **Msvm \_ ComputerSystem** para a máquina virtual de escopo.</span><span class="sxs-lookup"><span data-stu-id="d9891-406">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="d9891-407">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d9891-407">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d9891-408">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="d9891-408">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-409">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d9891-409">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-410">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-411">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="d9891-411">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="d9891-412">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d9891-412">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9891-413">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="d9891-413">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-414">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d9891-414">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-415">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-416">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="d9891-416">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="d9891-417">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d9891-417">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9891-418">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="d9891-418">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9891-419">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d9891-419">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d9891-420">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9891-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9891-421">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="d9891-421">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="d9891-422">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d9891-422">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d9891-423">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9891-423">Remarks</span></span>

<span data-ttu-id="d9891-424">O acesso à classe **Msvm \_ KvpExchangeComponent** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="d9891-424">Access to the **Msvm\_KvpExchangeComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d9891-425">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d9891-425">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9891-426">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9891-426">Requirements</span></span>



| <span data-ttu-id="d9891-427">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9891-427">Requirement</span></span> | <span data-ttu-id="d9891-428">Valor</span><span class="sxs-lookup"><span data-stu-id="d9891-428">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9891-429">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9891-429">Minimum supported client</span></span><br/> | <span data-ttu-id="d9891-430">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d9891-430">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d9891-431">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9891-431">Minimum supported server</span></span><br/> | <span data-ttu-id="d9891-432">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d9891-432">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d9891-433">Namespace</span><span class="sxs-lookup"><span data-stu-id="d9891-433">Namespace</span></span><br/>                | <span data-ttu-id="d9891-434">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d9891-434">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d9891-435">MOF</span><span class="sxs-lookup"><span data-stu-id="d9891-435">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9891-436"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9891-436"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9891-437">DLL</span><span class="sxs-lookup"><span data-stu-id="d9891-437">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9891-438"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d9891-438"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d9891-439">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9891-439">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9891-440">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="d9891-440">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="d9891-441">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="d9891-441">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

