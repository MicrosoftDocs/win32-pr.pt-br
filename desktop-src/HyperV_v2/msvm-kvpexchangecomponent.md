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
# <a name="msvm_kvpexchangecomponent-class"></a><span data-ttu-id="b5f45-103">\_Classe Msvm KvpExchangeComponent</span><span class="sxs-lookup"><span data-stu-id="b5f45-103">Msvm\_KvpExchangeComponent class</span></span>

<span data-ttu-id="b5f45-104">Representa o estado do serviço de troca de pares chave/valor, que fornece um mecanismo para trocar dados entre a máquina virtual e o sistema operacional em execução no sistema operacional de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="b5f45-104">Represents the state of the key/value pair exchange service, which provides a mechanism to exchange data between the virtual machine and the operating system running on the management operating system.</span></span>

<span data-ttu-id="b5f45-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b5f45-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5f45-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5f45-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="b5f45-107">Membros</span><span class="sxs-lookup"><span data-stu-id="b5f45-107">Members</span></span>

<span data-ttu-id="b5f45-108">A classe **Msvm \_ KvpExchangeComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b5f45-108">The **Msvm\_KvpExchangeComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="b5f45-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="b5f45-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="b5f45-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b5f45-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b5f45-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="b5f45-111">Methods</span></span>

<span data-ttu-id="b5f45-112">A classe **Msvm \_ KvpExchangeComponent** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b5f45-112">The **Msvm\_KvpExchangeComponent** class has these methods.</span></span>



| <span data-ttu-id="b5f45-113">Método</span><span class="sxs-lookup"><span data-stu-id="b5f45-113">Method</span></span>                                                                     | <span data-ttu-id="b5f45-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5f45-114">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="b5f45-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="b5f45-115">**EnableDevice**</span></span>                                                           | <span data-ttu-id="b5f45-116">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="b5f45-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="b5f45-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="b5f45-117">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="b5f45-118">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="b5f45-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="b5f45-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="b5f45-119">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="b5f45-120">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="b5f45-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="b5f45-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="b5f45-121">**RequestStateChange**</span></span>](msvm-kvpexchangecomponent-requeststatechange.md) | <span data-ttu-id="b5f45-122">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="b5f45-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="b5f45-123">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="b5f45-123">**Reset**</span></span>](msvm-kvpexchangecomponent-reset.md)                           | <span data-ttu-id="b5f45-124">Redefine o componente.</span><span class="sxs-lookup"><span data-stu-id="b5f45-124">Resets the component.</span></span><br/>         |
| <span data-ttu-id="b5f45-125">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="b5f45-125">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="b5f45-126">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="b5f45-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="b5f45-127">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="b5f45-127">**SaveProperties**</span></span>                                                         | <span data-ttu-id="b5f45-128">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="b5f45-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="b5f45-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b5f45-129">**SetPowerState**</span></span>                                                          | <span data-ttu-id="b5f45-130">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="b5f45-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b5f45-131">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b5f45-131">Properties</span></span>

<span data-ttu-id="b5f45-132">A classe **Msvm \_ KvpExchangeComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b5f45-132">The **Msvm\_KvpExchangeComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b5f45-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="b5f45-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-134">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5f45-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-136">Qualquer disponibilidade e status adicionais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b5f45-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="b5f45-137">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b5f45-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="b5f45-138">Valor</span><span class="sxs-lookup"><span data-stu-id="b5f45-138">Value</span></span>                                                                            | <span data-ttu-id="b5f45-139">Significado</span><span class="sxs-lookup"><span data-stu-id="b5f45-139">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="b5f45-140"><dt>152</dt></span><span class="sxs-lookup"><span data-stu-id="b5f45-140"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="b5f45-141"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="b5f45-141"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="b5f45-142">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="b5f45-142">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b5f45-143">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="b5f45-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-144">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5f45-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-146">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b5f45-146">The primary availability and status of the device.</span></span> <span data-ttu-id="b5f45-147">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b5f45-147">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="b5f45-148">Valor</span><span class="sxs-lookup"><span data-stu-id="b5f45-148">Value</span></span>                                                                        | <span data-ttu-id="b5f45-149">Significado</span><span class="sxs-lookup"><span data-stu-id="b5f45-149">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="b5f45-150"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="b5f45-150"><dt>6</dt></span></span> </dl> | <span data-ttu-id="b5f45-151">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="b5f45-151">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b5f45-152">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="b5f45-152">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-153">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5f45-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-155">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="b5f45-155">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="b5f45-156">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="b5f45-156">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-157">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="b5f45-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5f45-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-160">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="b5f45-160">A short description of the object.</span></span> <span data-ttu-id="b5f45-161">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b5f45-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-162">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="b5f45-162">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-163">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5f45-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-165">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="b5f45-165">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="b5f45-166">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="b5f45-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b5f45-167">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b5f45-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b5f45-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="b5f45-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="b5f45-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="b5f45-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="b5f45-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="b5f45-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="b5f45-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="b5f45-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b5f45-175">)</span><span class="sxs-lookup"><span data-stu-id="b5f45-175">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b5f45-176">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b5f45-176">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5f45-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-179">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="b5f45-179">The scoping system's creation class name.</span></span> <span data-ttu-id="b5f45-180">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b5f45-180">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-181">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b5f45-181">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5f45-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-184">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="b5f45-184">A description of the object.</span></span> <span data-ttu-id="b5f45-185">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b5f45-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-186">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="b5f45-186">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-187">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5f45-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-189">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="b5f45-189">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="b5f45-190">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="b5f45-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b5f45-191">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b5f45-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b5f45-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="b5f45-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="b5f45-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="b5f45-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="b5f45-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="b5f45-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="b5f45-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="b5f45-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="b5f45-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b5f45-200">)</span><span class="sxs-lookup"><span data-stu-id="b5f45-200">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b5f45-201">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b5f45-201">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-202">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5f45-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-204">Um endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b5f45-204">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="b5f45-205">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b5f45-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-206">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b5f45-206">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-207">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5f45-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-209">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="b5f45-209">A display name for the object.</span></span> <span data-ttu-id="b5f45-210">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b5f45-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-211">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="b5f45-211">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-212">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5f45-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-214">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b5f45-214">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="b5f45-215">Valor</span><span class="sxs-lookup"><span data-stu-id="b5f45-215">Value</span></span>                                                                        | <span data-ttu-id="b5f45-216">Significado</span><span class="sxs-lookup"><span data-stu-id="b5f45-216">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="b5f45-217"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="b5f45-217"><dt>7</dt></span></span> </dl> | <span data-ttu-id="b5f45-218">Nenhum padrão</span><span class="sxs-lookup"><span data-stu-id="b5f45-218">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b5f45-219">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="b5f45-219">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-220">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5f45-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-221">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-222">O estado habilitado do elemento.</span><span class="sxs-lookup"><span data-stu-id="b5f45-222">The enabled state of the element.</span></span> <span data-ttu-id="b5f45-223">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b5f45-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="b5f45-224"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="b5f45-224"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-225"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="b5f45-225"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b5f45-226">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="b5f45-226">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-227">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b5f45-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-229">Indica se o erro relatado na propriedade **LastErrorCode** agora está apagado.</span><span class="sxs-lookup"><span data-stu-id="b5f45-229">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="b5f45-230">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="b5f45-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-231">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b5f45-231">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-232">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5f45-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-234">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado na propriedade **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="b5f45-234">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="b5f45-235">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="b5f45-235">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-236">**GuestExchangeItems**</span><span class="sxs-lookup"><span data-stu-id="b5f45-236">**GuestExchangeItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-237">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5f45-237">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-239">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), **HyperVEmbeddedInstance** ("Msvm \_ KvpExchangeDataItem")</span><span class="sxs-lookup"><span data-stu-id="b5f45-239">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-240">Uma matriz de instâncias [**de \_ KvpExchangeDataItem Msvm**](msvm-kvpexchangedataitem.md) inseridas que contêm o conjunto de pares chave-valor que os serviços em execução no sistema operacional convidado foram disponibilizados para acesso por clientes externos.</span><span class="sxs-lookup"><span data-stu-id="b5f45-240">An array of embedded [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances which contain the set of key-value pairs that services running within the guest operating system have pushed up to be available for access by external clients.</span></span> <span data-ttu-id="b5f45-241">Essa matriz não conterá nenhum item intrínseco enviado diretamente pelo serviço de integração.</span><span class="sxs-lookup"><span data-stu-id="b5f45-241">This array will not contain any intrinsic items that are pushed by the integration service directly.</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-242">**GuestIntrinsicExchangeItems**</span><span class="sxs-lookup"><span data-stu-id="b5f45-242">**GuestIntrinsicExchangeItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-243">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5f45-243">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-245">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), **HyperVEmbeddedInstance** ("Msvm \_ KvpExchangeDataItem")</span><span class="sxs-lookup"><span data-stu-id="b5f45-245">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-246">Uma matriz de instâncias do [**Msvm \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) inseridas que contêm o conjunto de pares chave-valor que o sistema operacional convidado propagau para estar disponível para acesso por clientes externos.</span><span class="sxs-lookup"><span data-stu-id="b5f45-246">An array of embedded [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances which contain the set of key-value pairs that the guest operating system has pushed up to be available for access by external clients.</span></span> <span data-ttu-id="b5f45-247">Essa matriz não conterá nenhum item de dados Enviado por outros serviços em execução no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="b5f45-247">This array will not contain any data items pushed by other services running within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-248">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="b5f45-248">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-249">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5f45-249">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-250">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-251">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="b5f45-251">The current health of the element.</span></span> <span data-ttu-id="b5f45-252">Isso expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="b5f45-252">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="b5f45-253">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="b5f45-253">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="b5f45-254">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b5f45-254">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-255">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="b5f45-255">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-256">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5f45-256">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-257">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-258">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz de propriedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="b5f45-258">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="b5f45-259">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="b5f45-259">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-260">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b5f45-260">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-261">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b5f45-261">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-262">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-263">A data e a hora em que o serviço de integração foi instalado na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b5f45-263">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="b5f45-264">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b5f45-264">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-265">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b5f45-265">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-266">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5f45-266">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-267">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-268">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="b5f45-268">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-269">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="b5f45-269">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b5f45-270">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b5f45-270">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-271">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b5f45-271">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-272">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5f45-272">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-273">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-274">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b5f45-274">The last error code reported by the logical device.</span></span> <span data-ttu-id="b5f45-275">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="b5f45-275">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-276">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="b5f45-276">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-277">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b5f45-277">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-278">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-279">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="b5f45-279">This property has been deprecated.</span></span> <span data-ttu-id="b5f45-280">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b5f45-280">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-281">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b5f45-281">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-282">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5f45-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-283">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-284">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="b5f45-284">The label by which the object is known.</span></span> <span data-ttu-id="b5f45-285">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b5f45-285">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-286">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="b5f45-286">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-287">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5f45-287">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-288">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-289">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="b5f45-289">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="b5f45-290">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="b5f45-290">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b5f45-291">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b5f45-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b5f45-292"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="b5f45-292"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-293"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="b5f45-293"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-294"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="b5f45-294"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-295"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="b5f45-295"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-296"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="b5f45-296"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-297"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="b5f45-297"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-298"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="b5f45-298"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-299"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="b5f45-299"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-300"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="b5f45-300"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-301"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="b5f45-301"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-302"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="b5f45-302"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-303"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="b5f45-303"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-304"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="b5f45-304"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-305"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="b5f45-305"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-306"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="b5f45-306"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-307"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="b5f45-307"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-308"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="b5f45-308"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-309"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="b5f45-309"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-310"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="b5f45-310"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b5f45-311">)</span><span class="sxs-lookup"><span data-stu-id="b5f45-311">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b5f45-312">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="b5f45-312">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-313">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5f45-313">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-315">O status atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="b5f45-315">The current status of the element.</span></span> <span data-ttu-id="b5f45-316">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b5f45-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="b5f45-317">A seguir estão os valores possíveis para o  \[ valor da \] Propriedade OperationalStatus 0.</span><span class="sxs-lookup"><span data-stu-id="b5f45-317">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="b5f45-318">Valor</span><span class="sxs-lookup"><span data-stu-id="b5f45-318">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="b5f45-319">Significado</span><span class="sxs-lookup"><span data-stu-id="b5f45-319">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="b5f45-320"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b5f45-320"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="b5f45-321">O serviço está funcionando normalmente.</span><span class="sxs-lookup"><span data-stu-id="b5f45-321">The service is operating normally.</span></span> <span data-ttu-id="b5f45-322">Os  \[ valores de \] Propriedade OperationalStatus 1 e **StatusDescriptions** \[ 1 \] podem conter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b5f45-322">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="b5f45-323"><dt>**Degradado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b5f45-323"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="b5f45-324">O serviço está funcionando normalmente, mas o serviço convidado negocia uma versão de protocolo de comunicação compatível.</span><span class="sxs-lookup"><span data-stu-id="b5f45-324">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="b5f45-325">Os  \[ valores de \] Propriedade OperationalStatus 1 e **StatusDescriptions** \[ 1 \] podem conter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b5f45-325">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="b5f45-326"><dt>**Erro não recuperável**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="b5f45-326"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="b5f45-327">O convidado não oferece suporte a uma versão de protocolo compatível.</span><span class="sxs-lookup"><span data-stu-id="b5f45-327">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="b5f45-328">Os  \[ valores de \] Propriedade OperationalStatus 1 e **StatusDescriptions** \[ 1 \] podem conter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b5f45-328">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="b5f45-329"><dt>**Nenhum contato**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="b5f45-329"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="b5f45-330">O serviço convidado não está instalado ou ainda não foi contatado.</span><span class="sxs-lookup"><span data-stu-id="b5f45-330">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="b5f45-331"><dt>**Comunicação perdida**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="b5f45-331"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="b5f45-332">O serviço convidado não está mais respondendo normalmente.</span><span class="sxs-lookup"><span data-stu-id="b5f45-332">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="b5f45-333">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="b5f45-333">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-334">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5f45-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-335">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-336">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="b5f45-336">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="b5f45-337">Essa propriedade deve ser definida como **NULL** quando a propriedade **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="b5f45-337">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="b5f45-338">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b5f45-338">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-339">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="b5f45-339">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-340">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5f45-340">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-342">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b5f45-342">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="b5f45-343">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b5f45-343">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-344">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b5f45-344">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-345">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5f45-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-346">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-347">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b5f45-347">The power management capabilities of the device.</span></span> <span data-ttu-id="b5f45-348">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="b5f45-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-349">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="b5f45-349">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-350">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b5f45-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-351">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-352">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="b5f45-352">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="b5f45-353">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="b5f45-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-354">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="b5f45-354">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-355">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b5f45-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-356">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-357">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="b5f45-357">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="b5f45-358">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="b5f45-358">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-359">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="b5f45-359">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-360">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5f45-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-362">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="b5f45-362">Provides high level status information.</span></span> <span data-ttu-id="b5f45-363">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="b5f45-363">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="b5f45-364">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="b5f45-364">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b5f45-365">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b5f45-365">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b5f45-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="b5f45-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-367"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="b5f45-367"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="b5f45-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="b5f45-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="b5f45-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="b5f45-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b5f45-372">)</span><span class="sxs-lookup"><span data-stu-id="b5f45-372">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b5f45-373">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="b5f45-373">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-374">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5f45-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-376">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="b5f45-376">The last requested or desired state for the element.</span></span> <span data-ttu-id="b5f45-377">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b5f45-377">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="b5f45-378">Valor</span><span class="sxs-lookup"><span data-stu-id="b5f45-378">Value</span></span>                                                                         | <span data-ttu-id="b5f45-379">Significado</span><span class="sxs-lookup"><span data-stu-id="b5f45-379">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="b5f45-380"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="b5f45-380"><dt>12</dt></span></span> </dl> | <span data-ttu-id="b5f45-381">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="b5f45-381">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b5f45-382">**Status**</span><span class="sxs-lookup"><span data-stu-id="b5f45-382">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-383">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5f45-383">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-384">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-385">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="b5f45-385">The current status of the object.</span></span> <span data-ttu-id="b5f45-386">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) , mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="b5f45-386">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-387">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="b5f45-387">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-388">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5f45-388">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-389">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-390">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="b5f45-390">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="b5f45-391">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b5f45-391">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-392">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b5f45-392">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-393">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5f45-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-394">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-395">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b5f45-395">The current state of the logical device.</span></span> <span data-ttu-id="b5f45-396">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="b5f45-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-397">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b5f45-397">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-398">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5f45-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-399">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-400">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="b5f45-400">The scoping system's creation class name.</span></span> <span data-ttu-id="b5f45-401">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b5f45-401">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-402">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b5f45-402">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-403">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5f45-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-404">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-405">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="b5f45-405">The scoping system's name.</span></span> <span data-ttu-id="b5f45-406">Esse valor corresponde ao valor da propriedade [**Name**](msvm-computersystem.md) da classe **Msvm \_ ComputerSystem** para a máquina virtual de escopo.</span><span class="sxs-lookup"><span data-stu-id="b5f45-406">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="b5f45-407">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b5f45-407">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-408">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="b5f45-408">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-409">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b5f45-409">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-410">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-411">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="b5f45-411">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="b5f45-412">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="b5f45-412">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-413">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="b5f45-413">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-414">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b5f45-414">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-415">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-416">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="b5f45-416">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="b5f45-417">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="b5f45-417">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b5f45-418">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="b5f45-418">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5f45-419">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5f45-419">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5f45-420">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5f45-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5f45-421">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="b5f45-421">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="b5f45-422">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="b5f45-422">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5f45-423">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5f45-423">Remarks</span></span>

<span data-ttu-id="b5f45-424">O acesso à classe **Msvm \_ KvpExchangeComponent** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="b5f45-424">Access to the **Msvm\_KvpExchangeComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b5f45-425">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b5f45-425">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5f45-426">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5f45-426">Requirements</span></span>



| <span data-ttu-id="b5f45-427">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5f45-427">Requirement</span></span> | <span data-ttu-id="b5f45-428">Valor</span><span class="sxs-lookup"><span data-stu-id="b5f45-428">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5f45-429">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5f45-429">Minimum supported client</span></span><br/> | <span data-ttu-id="b5f45-430">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b5f45-430">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b5f45-431">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5f45-431">Minimum supported server</span></span><br/> | <span data-ttu-id="b5f45-432">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b5f45-432">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b5f45-433">Namespace</span><span class="sxs-lookup"><span data-stu-id="b5f45-433">Namespace</span></span><br/>                | <span data-ttu-id="b5f45-434">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="b5f45-434">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b5f45-435">MOF</span><span class="sxs-lookup"><span data-stu-id="b5f45-435">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5f45-436"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5f45-436"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5f45-437">DLL</span><span class="sxs-lookup"><span data-stu-id="b5f45-437">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5f45-438"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b5f45-438"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b5f45-439">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5f45-439">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5f45-440">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="b5f45-440">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="b5f45-441">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="b5f45-441">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

