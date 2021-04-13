---
description: Representa o estado do serviço de pulsação, que é responsável por monitorar o estado de uma máquina virtual, relatando uma pulsação em intervalos regulares.
ms.assetid: 72DB3CD9-B083-4483-BCCD-DC8C140DDBF4
title: Classe Msvm_HeartbeatComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HeartbeatComponent
- Msvm_HeartbeatComponent.SetPowerState
- Msvm_HeartbeatComponent.EnableDevice
- Msvm_HeartbeatComponent.OnlineDevice
- Msvm_HeartbeatComponent.QuiesceDevice
- Msvm_HeartbeatComponent.SaveProperties
- Msvm_HeartbeatComponent.RestoreProperties
- Msvm_HeartbeatComponent.InstanceID
- Msvm_HeartbeatComponent.Caption
- Msvm_HeartbeatComponent.Description
- Msvm_HeartbeatComponent.ElementName
- Msvm_HeartbeatComponent.InstallDate
- Msvm_HeartbeatComponent.Name
- Msvm_HeartbeatComponent.OperationalStatus
- Msvm_HeartbeatComponent.StatusDescriptions
- Msvm_HeartbeatComponent.Status
- Msvm_HeartbeatComponent.HealthState
- Msvm_HeartbeatComponent.CommunicationStatus
- Msvm_HeartbeatComponent.DetailedStatus
- Msvm_HeartbeatComponent.OperatingStatus
- Msvm_HeartbeatComponent.PrimaryStatus
- Msvm_HeartbeatComponent.EnabledState
- Msvm_HeartbeatComponent.OtherEnabledState
- Msvm_HeartbeatComponent.RequestedState
- Msvm_HeartbeatComponent.EnabledDefault
- Msvm_HeartbeatComponent.TimeOfLastStateChange
- Msvm_HeartbeatComponent.AvailableRequestedStates
- Msvm_HeartbeatComponent.TransitioningToState
- Msvm_HeartbeatComponent.SystemCreationClassName
- Msvm_HeartbeatComponent.SystemName
- Msvm_HeartbeatComponent.CreationClassName
- Msvm_HeartbeatComponent.DeviceID
- Msvm_HeartbeatComponent.PowerManagementSupported
- Msvm_HeartbeatComponent.PowerManagementCapabilities
- Msvm_HeartbeatComponent.Availability
- Msvm_HeartbeatComponent.StatusInfo
- Msvm_HeartbeatComponent.LastErrorCode
- Msvm_HeartbeatComponent.ErrorDescription
- Msvm_HeartbeatComponent.ErrorCleared
- Msvm_HeartbeatComponent.OtherIdentifyingInfo
- Msvm_HeartbeatComponent.PowerOnHours
- Msvm_HeartbeatComponent.TotalPowerOnHours
- Msvm_HeartbeatComponent.IdentifyingDescriptions
- Msvm_HeartbeatComponent.AdditionalAvailability
- Msvm_HeartbeatComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 61a3efaba52c2e592f405e1b95f1c62568a59229
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501381"
---
# <a name="msvm_heartbeatcomponent-class"></a><span data-ttu-id="09e6f-103">\_Classe Msvm HeartbeatComponent</span><span class="sxs-lookup"><span data-stu-id="09e6f-103">Msvm\_HeartbeatComponent class</span></span>

<span data-ttu-id="09e6f-104">Representa o estado do serviço de pulsação, que é responsável por monitorar o estado de uma máquina virtual, relatando uma pulsação em intervalos regulares.</span><span class="sxs-lookup"><span data-stu-id="09e6f-104">Represents the state of the heartbeat service, which is responsible for monitoring the state of a virtual machine by reporting a heartbeat at regular intervals.</span></span>

<span data-ttu-id="09e6f-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="09e6f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="09e6f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09e6f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HeartbeatComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Heartbeat";
  string   Description = "Microsoft Heartbeat Service";
  string   ElementName = "Heartbeat";
  datetime InstallDate;
  string   Name;
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
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 7;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_HeartbeatComponent";
  string   DeviceID = "Microsoft:VMGUID\GUID";
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
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
};
```

## <a name="members"></a><span data-ttu-id="09e6f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="09e6f-107">Members</span></span>

<span data-ttu-id="09e6f-108">A classe **Msvm \_ HeartbeatComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="09e6f-108">The **Msvm\_HeartbeatComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="09e6f-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="09e6f-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="09e6f-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="09e6f-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="09e6f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="09e6f-111">Methods</span></span>

<span data-ttu-id="09e6f-112">A classe **Msvm \_ HeartbeatComponent** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="09e6f-112">The **Msvm\_HeartbeatComponent** class has these methods.</span></span>



| <span data-ttu-id="09e6f-113">Método</span><span class="sxs-lookup"><span data-stu-id="09e6f-113">Method</span></span>                                                                   | <span data-ttu-id="09e6f-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="09e6f-114">Description</span></span>                              |
|:-------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="09e6f-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="09e6f-115">**EnableDevice**</span></span>                                                         | <span data-ttu-id="09e6f-116">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="09e6f-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="09e6f-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="09e6f-117">**OnlineDevice**</span></span>                                                         | <span data-ttu-id="09e6f-118">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="09e6f-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="09e6f-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="09e6f-119">**QuiesceDevice**</span></span>                                                        | <span data-ttu-id="09e6f-120">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="09e6f-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="09e6f-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="09e6f-121">**RequestStateChange**</span></span>](msvm-heartbeatcomponent-requeststatechange.md) | <span data-ttu-id="09e6f-122">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="09e6f-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="09e6f-123">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="09e6f-123">**Reset**</span></span>](msvm-heartbeatcomponent-reset.md)                           | <span data-ttu-id="09e6f-124">Redefine o dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="09e6f-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="09e6f-125">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="09e6f-125">**RestoreProperties**</span></span>                                                    | <span data-ttu-id="09e6f-126">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="09e6f-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="09e6f-127">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="09e6f-127">**SaveProperties**</span></span>                                                       | <span data-ttu-id="09e6f-128">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="09e6f-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="09e6f-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="09e6f-129">**SetPowerState**</span></span>                                                        | <span data-ttu-id="09e6f-130">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="09e6f-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="09e6f-131">Propriedades</span><span class="sxs-lookup"><span data-stu-id="09e6f-131">Properties</span></span>

<span data-ttu-id="09e6f-132">A classe **Msvm \_ HeartbeatComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="09e6f-132">The **Msvm\_HeartbeatComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="09e6f-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="09e6f-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-134">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09e6f-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-136">Qualquer disponibilidade e status adicionais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09e6f-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="09e6f-137">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como 6 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="09e6f-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-138">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="09e6f-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-139">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09e6f-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-141">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09e6f-141">The primary availability and status of the device.</span></span> <span data-ttu-id="09e6f-142">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="09e6f-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-143">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="09e6f-143">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-144">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09e6f-144">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-146">Indica os valores possíveis para o parâmetro *requestedstate* do método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="09e6f-146">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="09e6f-147">Os valores listados serão um subconjunto dos valores contidos na propriedade **RequestedStatesSupported** da instância associada do **CIM \_ EnabledLogicalElementCapabilities**, em que os valores selecionados são uma função do estado atual do [**\_ EnabledLogicalElement do CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="09e6f-147">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="09e6f-148">Essa propriedade pode ser não **nula** se uma implementação for capaz de anunciar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="09e6f-148">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="09e6f-149">Essa propriedade será **nula** se uma implementação não puder determinar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="09e6f-149">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="09e6f-150">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="09e6f-150">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="09e6f-151"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="09e6f-151"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-152"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="09e6f-152"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-153"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="09e6f-153"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-154"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="09e6f-154"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-155"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="09e6f-155"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-156"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="09e6f-156"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-157"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="09e6f-157"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-158"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="09e6f-158"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-159"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="09e6f-159"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-160"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="09e6f-160"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="09e6f-161">)</span><span class="sxs-lookup"><span data-stu-id="09e6f-161">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="09e6f-162">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="09e6f-162">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-163">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09e6f-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-165">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="09e6f-165">A short description of the object.</span></span> <span data-ttu-id="09e6f-166">Essa propriedade é herdada da classe [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) e é sempre definida como "Heartbeat".</span><span class="sxs-lookup"><span data-stu-id="09e6f-166">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Heartbeat".</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-167">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="09e6f-167">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-168">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09e6f-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-170">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="09e6f-170">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="09e6f-171">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="09e6f-171">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="09e6f-172">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="09e6f-172">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-173">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="09e6f-173">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09e6f-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-176">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="09e6f-176">The scoping system's creation class name.</span></span> <span data-ttu-id="09e6f-177">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como "Msvm \_ HeartbeatComponent".</span><span class="sxs-lookup"><span data-stu-id="09e6f-177">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_HeartbeatComponent".</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-178">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="09e6f-178">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09e6f-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-181">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="09e6f-181">A description of the object.</span></span> <span data-ttu-id="09e6f-182">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "serviço de pulsação da Microsoft".</span><span class="sxs-lookup"><span data-stu-id="09e6f-182">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Heartbeat Service".</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-183">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="09e6f-183">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-184">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09e6f-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-186">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="09e6f-186">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="09e6f-187">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="09e6f-187">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="09e6f-188">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="09e6f-188">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-189">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="09e6f-189">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-190">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09e6f-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-192">Um endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="09e6f-192">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="09e6f-193">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como "Microsoft:*VMGUID* \\ *GUID*", em *que VMGUID* é a propriedade **Name** do [**Msvm \_ ComputerSystem**](msvm-computersystem.md) associado a este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09e6f-193">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-194">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="09e6f-194">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-195">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09e6f-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-197">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="09e6f-197">A display name for the object.</span></span> <span data-ttu-id="09e6f-198">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "Heartbeat".</span><span class="sxs-lookup"><span data-stu-id="09e6f-198">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Heartbeat".</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-199">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="09e6f-199">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-200">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09e6f-200">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-201">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-202">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 7 (não padrão).</span><span class="sxs-lookup"><span data-stu-id="09e6f-202">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 7 (No Default).</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-203">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="09e6f-203">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-204">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09e6f-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-206">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="09e6f-206">The enabled and disabled states of an element.</span></span> <span data-ttu-id="09e6f-207">Essa propriedade é herdada de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="09e6f-207">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>



| <span data-ttu-id="09e6f-208">Valor</span><span class="sxs-lookup"><span data-stu-id="09e6f-208">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="09e6f-209">Significado</span><span class="sxs-lookup"><span data-stu-id="09e6f-209">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="09e6f-210"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="09e6f-210"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="09e6f-211">O elemento está em execução.</span><span class="sxs-lookup"><span data-stu-id="09e6f-211">The element is running.</span></span><br/>    |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="09e6f-212"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="09e6f-212"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="09e6f-213">O elemento está desativado.</span><span class="sxs-lookup"><span data-stu-id="09e6f-213">The element is turned off.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="09e6f-214">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="09e6f-214">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-215">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="09e6f-215">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-216">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-217">Indica se o erro relatado em **LastErrorCode** agora está limpo.</span><span class="sxs-lookup"><span data-stu-id="09e6f-217">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="09e6f-218">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="09e6f-218">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-219">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="09e6f-219">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-220">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09e6f-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-221">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-222">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="09e6f-222">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="09e6f-223">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="09e6f-223">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-224">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="09e6f-224">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-225">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09e6f-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-227">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="09e6f-227">The current health of the element.</span></span> <span data-ttu-id="09e6f-228">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="09e6f-228">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-229">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="09e6f-229">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-230">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09e6f-230">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-232">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz de propriedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="09e6f-232">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="09e6f-233">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="09e6f-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-234">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="09e6f-234">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-235">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="09e6f-235">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-236">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-237">A data e a hora em que o serviço de integração foi instalado na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="09e6f-237">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="09e6f-238">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="09e6f-238">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-239">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="09e6f-239">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-240">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09e6f-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-242">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="09e6f-242">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-243">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="09e6f-243">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="09e6f-244">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="09e6f-244">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-245">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="09e6f-245">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-246">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="09e6f-246">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-247">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-248">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="09e6f-248">The last error code reported by the logical device.</span></span> <span data-ttu-id="09e6f-249">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="09e6f-249">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-250">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="09e6f-250">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-251">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="09e6f-251">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-253">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="09e6f-253">This property has been deprecated.</span></span> <span data-ttu-id="09e6f-254">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="09e6f-254">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-255">**Nome**</span><span class="sxs-lookup"><span data-stu-id="09e6f-255">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-256">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09e6f-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-257">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-258">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="09e6f-258">The label by which the object is known.</span></span> <span data-ttu-id="09e6f-259">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="09e6f-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-260">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="09e6f-260">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-261">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09e6f-261">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-262">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-263">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="09e6f-263">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="09e6f-264">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="09e6f-264">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="09e6f-265">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="09e6f-265">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-266">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="09e6f-266">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-267">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09e6f-267">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-268">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-269">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="09e6f-269">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-270">O status atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="09e6f-270">The current status of the element.</span></span> <span data-ttu-id="09e6f-271">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="09e6f-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="09e6f-272">A seguir estão os valores possíveis para o  \[ valor da \] Propriedade OperationalStatus 0.</span><span class="sxs-lookup"><span data-stu-id="09e6f-272">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="09e6f-273"><span id="OK"></span><span id="ok"></span>**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="09e6f-273"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd>

<span data-ttu-id="09e6f-274">O serviço está funcionando normalmente.</span><span class="sxs-lookup"><span data-stu-id="09e6f-274">The service is operating normally.</span></span> <span data-ttu-id="09e6f-275">Os  \[ valores de \] Propriedade OperationalStatus 1 e **StatusDescriptions** \[ 1 \] podem conter mais informações.</span><span class="sxs-lookup"><span data-stu-id="09e6f-275">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span>

</dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="09e6f-276"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (3)</span><span class="sxs-lookup"><span data-stu-id="09e6f-276"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (3)</span></span>


</dt> <dd>

<span data-ttu-id="09e6f-277">O serviço está funcionando normalmente, mas o serviço convidado negocia uma versão de protocolo de comunicação compatível.</span><span class="sxs-lookup"><span data-stu-id="09e6f-277">The service is operating normally, but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="09e6f-278">Os  \[ valores de \] Propriedade OperationalStatus 1 e **StatusDescriptions** \[ 1 \] podem conter mais informações.</span><span class="sxs-lookup"><span data-stu-id="09e6f-278">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span>

</dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="09e6f-279"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (7)</span><span class="sxs-lookup"><span data-stu-id="09e6f-279"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="09e6f-280">O convidado não oferece suporte a uma versão de protocolo compatível.</span><span class="sxs-lookup"><span data-stu-id="09e6f-280">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="09e6f-281">Os  \[ valores de \] Propriedade OperationalStatus 1 e **StatusDescriptions** \[ 1 \] podem conter mais informações.</span><span class="sxs-lookup"><span data-stu-id="09e6f-281">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span>

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="09e6f-282"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sem contato** (12)</span><span class="sxs-lookup"><span data-stu-id="09e6f-282"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>


</dt> <dd>

<span data-ttu-id="09e6f-283">O serviço convidado não está instalado ou ainda não foi contatado.</span><span class="sxs-lookup"><span data-stu-id="09e6f-283">The guest service is not installed or has not yet been contacted.</span></span>

</dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="09e6f-284"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (13)</span><span class="sxs-lookup"><span data-stu-id="09e6f-284"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>


</dt> <dd>

<span data-ttu-id="09e6f-285">O serviço convidado não está mais respondendo normalmente.</span><span class="sxs-lookup"><span data-stu-id="09e6f-285">The guest service is no longer responding normally.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="09e6f-286"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (15)</span><span class="sxs-lookup"><span data-stu-id="09e6f-286"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (15)</span></span>


</dt> <dd>

<span data-ttu-id="09e6f-287">A máquina virtual está pausada.</span><span class="sxs-lookup"><span data-stu-id="09e6f-287">The virtual machine is paused.</span></span>

</dd> </dl>

<span data-ttu-id="09e6f-288">O  \[ valor da \] Propriedade OperationalStatus 1 indica os valores de estado do aplicativo agrupado.</span><span class="sxs-lookup"><span data-stu-id="09e6f-288">The **OperationalStatus**\[1\] property value indicates the coalesced application state values.</span></span> <span data-ttu-id="09e6f-289">Esse será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="09e6f-289">This will be one of the following values.</span></span>

> [!Note]  
> <span data-ttu-id="09e6f-290">O estado de um aplicativo é definido na máquina virtual usando o método [**Setapplicationstate**](ivmapplicationhealthmonitor-setapplicationstate.md) .</span><span class="sxs-lookup"><span data-stu-id="09e6f-290">The state for an application is set on the virtual machine by using the [**SetApplicationState**](ivmapplicationhealthmonitor-setapplicationstate.md) method.</span></span>

 

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="09e6f-291"><span id="OK"></span><span id="ok"></span>**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="09e6f-291"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd>

<span data-ttu-id="09e6f-292">Os aplicativos em execução na máquina virtual estão funcionando normalmente.</span><span class="sxs-lookup"><span data-stu-id="09e6f-292">The applications running inside the virtual machine are operating normally.</span></span>

</dd> <dt>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>

<span data-ttu-id="09e6f-293"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Incompatibilidade de protocolo** (32775)</span><span class="sxs-lookup"><span data-stu-id="09e6f-293"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Protocol Mismatch** (32775)</span></span>


</dt> <dd>

<span data-ttu-id="09e6f-294">Os componentes convidado e host estão executando versões de protocolo diferentes.</span><span class="sxs-lookup"><span data-stu-id="09e6f-294">The guest and the host components are running different protocol versions.</span></span>

</dd> <dt>

<span id="Application_Critical_State"></span><span id="application_critical_state"></span><span id="APPLICATION_CRITICAL_STATE"></span>

<span data-ttu-id="09e6f-295"><span id="Application_Critical_State"></span><span id="application_critical_state"></span><span id="APPLICATION_CRITICAL_STATE"></span>**Estado crítico do aplicativo** (32782)</span><span class="sxs-lookup"><span data-stu-id="09e6f-295"><span id="Application_Critical_State"></span><span id="application_critical_state"></span><span id="APPLICATION_CRITICAL_STATE"></span>**Application Critical State** (32782)</span></span>


</dt> <dd>

<span data-ttu-id="09e6f-296">Um ou mais dos aplicativos dentro da máquina virtual estão em um estado crítico.</span><span class="sxs-lookup"><span data-stu-id="09e6f-296">One or more of the applications inside the virtual machine are in a critical state.</span></span>

</dd> <dt>

<span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>

<span data-ttu-id="09e6f-297"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Tempo limite de comunicação** (32783)</span><span class="sxs-lookup"><span data-stu-id="09e6f-297"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Communication Timed Out** (32783)</span></span>


</dt> <dd>

<span data-ttu-id="09e6f-298">Tempo limite excedido ao aguardar uma resposta do componente convidado.</span><span class="sxs-lookup"><span data-stu-id="09e6f-298">Timed out waiting for a response from the guest component.</span></span>

</dd> <dt>

<span id="Communication_Failed"></span><span id="communication_failed"></span><span id="COMMUNICATION_FAILED"></span>

<span data-ttu-id="09e6f-299"><span id="Communication_Failed"></span><span id="communication_failed"></span><span id="COMMUNICATION_FAILED"></span>**Falha na comunicação** (32784)</span><span class="sxs-lookup"><span data-stu-id="09e6f-299"><span id="Communication_Failed"></span><span id="communication_failed"></span><span id="COMMUNICATION_FAILED"></span>**Communication Failed** (32784)</span></span>


</dt> <dd>

<span data-ttu-id="09e6f-300">Falha ao se comunicar com o componente convidado.</span><span class="sxs-lookup"><span data-stu-id="09e6f-300">Failed to communicate with the guest component.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="09e6f-301">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="09e6f-301">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-302">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09e6f-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-303">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-304">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="09e6f-304">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="09e6f-305">Essa propriedade deve ser definida como **NULL** quando a propriedade **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="09e6f-305">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="09e6f-306">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="09e6f-306">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-307">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="09e6f-307">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-308">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09e6f-308">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-310">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="09e6f-310">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="09e6f-311">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="09e6f-311">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-312">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="09e6f-312">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-313">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09e6f-313">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-315">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09e6f-315">The power management capabilities of the device.</span></span> <span data-ttu-id="09e6f-316">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="09e6f-316">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-317">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="09e6f-317">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-318">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="09e6f-318">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-319">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-320">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="09e6f-320">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="09e6f-321">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="09e6f-321">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-322">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="09e6f-322">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-323">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="09e6f-323">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-324">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-325">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="09e6f-325">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="09e6f-326">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="09e6f-326">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-327">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="09e6f-327">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-328">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09e6f-328">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-329">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-330">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="09e6f-330">Provides high level status information.</span></span> <span data-ttu-id="09e6f-331">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer informações de status de integridade detalhadas e de alto nível para o elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="09e6f-331">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="09e6f-332">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="09e6f-332">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="09e6f-333">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="09e6f-333">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-334">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="09e6f-334">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-335">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09e6f-335">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-337">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="09e6f-337">The last requested or desired state for the element.</span></span> <span data-ttu-id="09e6f-338">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 12 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="09e6f-338">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-339">**Status**</span><span class="sxs-lookup"><span data-stu-id="09e6f-339">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-340">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09e6f-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-342">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="09e6f-342">The current status of the object.</span></span> <span data-ttu-id="09e6f-343">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) , mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="09e6f-343">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-344">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="09e6f-344">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-345">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09e6f-345">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-346">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-347">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="09e6f-347">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="09e6f-348">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="09e6f-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-349">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="09e6f-349">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-350">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09e6f-350">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-351">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-352">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="09e6f-352">The current state of the logical device.</span></span> <span data-ttu-id="09e6f-353">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="09e6f-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-354">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="09e6f-354">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-355">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09e6f-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-356">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-357">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="09e6f-357">The scoping system's creation class name.</span></span> <span data-ttu-id="09e6f-358">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como "Msvm \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="09e6f-358">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-359">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="09e6f-359">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-360">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09e6f-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-362">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="09e6f-362">The scoping system's name.</span></span> <span data-ttu-id="09e6f-363">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e é o nome do [**\_ ComputerSystem Msvm**](msvm-computersystem.md) que está associado a esse serviço de pulsação.</span><span class="sxs-lookup"><span data-stu-id="09e6f-363">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is the name of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) that is associated with this heartbeat service.</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-364">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="09e6f-364">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-365">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="09e6f-365">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-366">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-367">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="09e6f-367">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="09e6f-368">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="09e6f-368">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-369">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="09e6f-369">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-370">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="09e6f-370">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-371">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-372">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="09e6f-372">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="09e6f-373">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="09e6f-373">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09e6f-374">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="09e6f-374">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e6f-375">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09e6f-375">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09e6f-376">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09e6f-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09e6f-377">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="09e6f-377">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="09e6f-378">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="09e6f-378">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09e6f-379">Comentários</span><span class="sxs-lookup"><span data-stu-id="09e6f-379">Remarks</span></span>

<span data-ttu-id="09e6f-380">O acesso à classe **Msvm \_ HeartbeatComponent** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="09e6f-380">Access to the **Msvm\_HeartbeatComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="09e6f-381">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="09e6f-381">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="09e6f-382">Exemplos</span><span class="sxs-lookup"><span data-stu-id="09e6f-382">Examples</span></span>

<span data-ttu-id="09e6f-383">O exemplo de C# a seguir obtém o status de integridade do aplicativo de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="09e6f-383">The following C# sample obtains the application health status of a virtual machine.</span></span> <span data-ttu-id="09e6f-384">Os utilitários referenciados podem ser encontrados em [utilitários comuns para os exemplos de virtualização (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="09e6f-384">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="09e6f-385">Para funcionar corretamente, o código a seguir deve ser executado com privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="09e6f-385">To function correctly, the following code must be run with Administrator privileges.</span></span>

 


```CSharp
private UInt16 OperationalStatusOk = 2;
private UInt16 OperationalStatusApplicationCriticalState = 32782;

/// <summary>
/// Gets the applications status in the VM.
/// </summary>
/// <param name="hostMachine">The hostname of the machine on which
/// the VM is running.</param>
/// <param name="vmName">The VM name.</param>
public
void
GetAppHealthStatus(
    string hostMachine,
    string vmName
    )
{
    ManagementScope scope = new ManagementScope(
        @"\\" + hostMachine + @"\root\virtualization\v2", null);

    ManagementObject heartBeatComponent = null;

    // Get the VM object and its heart beat component.
    using (ManagementObject vm = WmiUtilities.GetVirtualMachine(vmName, scope))
    using (ManagementObjectCollection heartBeatCollection =
        vm.GetRelated("Msvm_HeartbeatComponent", "Msvm_SystemDevice",
            null, null, null, null, false, null))
    {
        foreach (ManagementObject element in heartBeatCollection)
        {
            heartBeatComponent = element;
            break;
        }
    }

    if (heartBeatComponent == null)
    {
        Console.WriteLine("The VM is not running.");
        return;
    }

    using (heartBeatComponent)
    {
        UInt16[] operationalStatus = (UInt16[])heartBeatComponent["OperationalStatus"];
        UInt16 vmStatus = operationalStatus[0];

        if (vmStatus != OperationalStatusOk)
        {
            Console.WriteLine("The VM heartbeat status is not OK");
            return;
        }

        if (operationalStatus.Length != 2)
        {
            Console.WriteLine("The required Integration Components are not running " +
                "or not installed.");
            return;
        }

        UInt16 appStatus = operationalStatus[1];
        if (appStatus == OperationalStatusOk)
        {
            Console.WriteLine("The VM applications health status: OK");
        }
        else if (appStatus == OperationalStatusApplicationCriticalState)
        {
            Console.WriteLine("The VM applications health status: Critical");
        }
        else
        {
            throw new ManagementException("Unknown application health status");
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="09e6f-386">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09e6f-386">Requirements</span></span>



| <span data-ttu-id="09e6f-387">Requisito</span><span class="sxs-lookup"><span data-stu-id="09e6f-387">Requirement</span></span> | <span data-ttu-id="09e6f-388">Valor</span><span class="sxs-lookup"><span data-stu-id="09e6f-388">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09e6f-389">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09e6f-389">Minimum supported client</span></span><br/> | <span data-ttu-id="09e6f-390">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="09e6f-390">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="09e6f-391">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09e6f-391">Minimum supported server</span></span><br/> | <span data-ttu-id="09e6f-392">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="09e6f-392">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="09e6f-393">Namespace</span><span class="sxs-lookup"><span data-stu-id="09e6f-393">Namespace</span></span><br/>                | <span data-ttu-id="09e6f-394">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="09e6f-394">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="09e6f-395">MOF</span><span class="sxs-lookup"><span data-stu-id="09e6f-395">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09e6f-396"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09e6f-396"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="09e6f-397">DLL</span><span class="sxs-lookup"><span data-stu-id="09e6f-397">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09e6f-398"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="09e6f-398"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="09e6f-399">Confira também</span><span class="sxs-lookup"><span data-stu-id="09e6f-399">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09e6f-400">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="09e6f-400">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="09e6f-401">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="09e6f-401">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> <dt>

[<span data-ttu-id="09e6f-402">**Msvm \_ HeartbeatComponent**</span><span class="sxs-lookup"><span data-stu-id="09e6f-402">**Msvm\_HeartbeatComponent**</span></span>](/previous-versions/windows/desktop/virtual/msvm-heartbeatcomponent)
</dt> </dl>

 

