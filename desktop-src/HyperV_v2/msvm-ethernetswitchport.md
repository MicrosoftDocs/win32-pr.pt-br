---
description: Representa uma porta no comutador.
ms.assetid: a2637e53-6b28-41ad-bef9-d3a14b6cf727
title: Classe Msvm_EthernetSwitchPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPort
- Msvm_EthernetSwitchPort.SetPowerState
- Msvm_EthernetSwitchPort.EnableDevice
- Msvm_EthernetSwitchPort.OnlineDevice
- Msvm_EthernetSwitchPort.QuiesceDevice
- Msvm_EthernetSwitchPort.SaveProperties
- Msvm_EthernetSwitchPort.RestoreProperties
- Msvm_EthernetSwitchPort.InstanceID
- Msvm_EthernetSwitchPort.Caption
- Msvm_EthernetSwitchPort.Description
- Msvm_EthernetSwitchPort.ElementName
- Msvm_EthernetSwitchPort.InstallDate
- Msvm_EthernetSwitchPort.Name
- Msvm_EthernetSwitchPort.OperationalStatus
- Msvm_EthernetSwitchPort.StatusDescriptions
- Msvm_EthernetSwitchPort.Status
- Msvm_EthernetSwitchPort.HealthState
- Msvm_EthernetSwitchPort.CommunicationStatus
- Msvm_EthernetSwitchPort.DetailedStatus
- Msvm_EthernetSwitchPort.OperatingStatus
- Msvm_EthernetSwitchPort.PrimaryStatus
- Msvm_EthernetSwitchPort.EnabledState
- Msvm_EthernetSwitchPort.OtherEnabledState
- Msvm_EthernetSwitchPort.RequestedState
- Msvm_EthernetSwitchPort.EnabledDefault
- Msvm_EthernetSwitchPort.TimeOfLastStateChange
- Msvm_EthernetSwitchPort.AvailableRequestedStates
- Msvm_EthernetSwitchPort.TransitioningToState
- Msvm_EthernetSwitchPort.SystemCreationClassName
- Msvm_EthernetSwitchPort.SystemName
- Msvm_EthernetSwitchPort.CreationClassName
- Msvm_EthernetSwitchPort.DeviceID
- Msvm_EthernetSwitchPort.PowerManagementSupported
- Msvm_EthernetSwitchPort.PowerManagementCapabilities
- Msvm_EthernetSwitchPort.Availability
- Msvm_EthernetSwitchPort.StatusInfo
- Msvm_EthernetSwitchPort.LastErrorCode
- Msvm_EthernetSwitchPort.ErrorDescription
- Msvm_EthernetSwitchPort.ErrorCleared
- Msvm_EthernetSwitchPort.OtherIdentifyingInfo
- Msvm_EthernetSwitchPort.PowerOnHours
- Msvm_EthernetSwitchPort.TotalPowerOnHours
- Msvm_EthernetSwitchPort.IdentifyingDescriptions
- Msvm_EthernetSwitchPort.AdditionalAvailability
- Msvm_EthernetSwitchPort.MaxQuiesceTime
- Msvm_EthernetSwitchPort.Speed
- Msvm_EthernetSwitchPort.MaxSpeed
- Msvm_EthernetSwitchPort.RequestedSpeed
- Msvm_EthernetSwitchPort.UsageRestriction
- Msvm_EthernetSwitchPort.PortType
- Msvm_EthernetSwitchPort.OtherPortType
- Msvm_EthernetSwitchPort.OtherNetworkPortType
- Msvm_EthernetSwitchPort.PortNumber
- Msvm_EthernetSwitchPort.LinkTechnology
- Msvm_EthernetSwitchPort.OtherLinkTechnology
- Msvm_EthernetSwitchPort.PermanentAddress
- Msvm_EthernetSwitchPort.NetworkAddresses
- Msvm_EthernetSwitchPort.FullDuplex
- Msvm_EthernetSwitchPort.AutoSense
- Msvm_EthernetSwitchPort.SupportedMaximumTransmissionUnit
- Msvm_EthernetSwitchPort.ActiveMaximumTransmissionUnit
- Msvm_EthernetSwitchPort.MaxDataSize
- Msvm_EthernetSwitchPort.Capabilities
- Msvm_EthernetSwitchPort.CapabilityDescriptions
- Msvm_EthernetSwitchPort.EnabledCapabilities
- Msvm_EthernetSwitchPort.OtherEnabledCapabilities
- Msvm_EthernetSwitchPort.VMQOffloadUsage
- Msvm_EthernetSwitchPort.IOVOffloadUsage
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 76c43cbe8dd053808085346b1874781f354b20dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766895"
---
# <a name="msvm_ethernetswitchport-class"></a><span data-ttu-id="d574a-103">\_Classe Msvm EthernetSwitchPort</span><span class="sxs-lookup"><span data-stu-id="d574a-103">Msvm\_EthernetSwitchPort class</span></span>

<span data-ttu-id="d574a-104">Representa uma porta no comutador.</span><span class="sxs-lookup"><span data-stu-id="d574a-104">Represents a port on the switch.</span></span>

<span data-ttu-id="d574a-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d574a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d574a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d574a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Switch Port";
  string   Description = "Microsoft Virtual Ethernet Switch Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
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
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string   SystemName;
  string   CreationClassName = "Msvm_EthernetSwitchPort";
  string   DeviceID;
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
  uint64   Speed;
  uint64   MaxSpeed;
  uint64   RequestedSpeed;
  uint16   UsageRestriction;
  uint16   PortType;
  string   OtherPortType;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex;
  boolean  AutoSense;
  uint64   SupportedMaximumTransmissionUnit;
  uint64   ActiveMaximumTransmissionUnit;
  uint32   MaxDataSize;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
  uint32   VMQOffloadUsage;
  uint32   IOVOffloadUsage;
};
```

## <a name="members"></a><span data-ttu-id="d574a-107">Membros</span><span class="sxs-lookup"><span data-stu-id="d574a-107">Members</span></span>

<span data-ttu-id="d574a-108">A classe **Msvm \_ EthernetSwitchPort** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d574a-108">The **Msvm\_EthernetSwitchPort** class has these types of members:</span></span>

-   [<span data-ttu-id="d574a-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="d574a-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="d574a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d574a-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d574a-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="d574a-111">Methods</span></span>

<span data-ttu-id="d574a-112">A classe **Msvm \_ EthernetSwitchPort** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d574a-112">The **Msvm\_EthernetSwitchPort** class has these methods.</span></span>



| <span data-ttu-id="d574a-113">Método</span><span class="sxs-lookup"><span data-stu-id="d574a-113">Method</span></span>                                                                   | <span data-ttu-id="d574a-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="d574a-114">Description</span></span>                              |
|:-------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="d574a-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="d574a-115">**EnableDevice**</span></span>                                                         | <span data-ttu-id="d574a-116">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d574a-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d574a-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="d574a-117">**OnlineDevice**</span></span>                                                         | <span data-ttu-id="d574a-118">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d574a-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d574a-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="d574a-119">**QuiesceDevice**</span></span>                                                        | <span data-ttu-id="d574a-120">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d574a-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="d574a-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="d574a-121">**RequestStateChange**</span></span>](msvm-ethernetswitchport-requeststatechange.md) | <span data-ttu-id="d574a-122">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="d574a-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="d574a-123">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="d574a-123">**Reset**</span></span>](msvm-ethernetswitchport-reset.md)                           | <span data-ttu-id="d574a-124">Redefine o dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="d574a-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="d574a-125">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="d574a-125">**RestoreProperties**</span></span>                                                    | <span data-ttu-id="d574a-126">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d574a-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d574a-127">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="d574a-127">**SaveProperties**</span></span>                                                       | <span data-ttu-id="d574a-128">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d574a-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d574a-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d574a-129">**SetPowerState**</span></span>                                                        | <span data-ttu-id="d574a-130">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d574a-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d574a-131">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d574a-131">Properties</span></span>

<span data-ttu-id="d574a-132">A classe **Msvm \_ EthernetSwitchPort** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d574a-132">The **Msvm\_EthernetSwitchPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d574a-133">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="d574a-133">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-134">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d574a-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d574a-136">Qualificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="d574a-136">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d574a-137">A unidade de transmissão máxima (MTU) do negociada ou ativa que pode ter suporte, em bytes.</span><span class="sxs-lookup"><span data-stu-id="d574a-137">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="d574a-138">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d574a-138">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-139">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="d574a-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-140">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d574a-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d574a-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-142">Qualquer disponibilidade e status adicionais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d574a-142">Any additional availability and status of the device.</span></span> <span data-ttu-id="d574a-143">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d574a-143">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d574a-144">**Autodetecção**</span><span class="sxs-lookup"><span data-stu-id="d574a-144">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-145">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d574a-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-147">Indica se a porta é capaz de determinar automaticamente a velocidade ou outras características de comunicação da mídia de rede anexada.</span><span class="sxs-lookup"><span data-stu-id="d574a-147">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="d574a-148">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d574a-148">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-149">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="d574a-149">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-150">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d574a-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-152">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d574a-152">The primary availability and status of the device.</span></span> <span data-ttu-id="d574a-153">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d574a-153">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d574a-154">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="d574a-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-155">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d574a-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d574a-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-157">Indica os valores possíveis para o parâmetro *requestedstate* do método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="d574a-157">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="d574a-158">Os valores listados serão um subconjunto dos valores contidos na propriedade **RequestedStatesSupported** da instância associada do **CIM \_ EnabledLogicalElementCapabilities**, em que os valores selecionados são uma função do estado atual do [**\_ EnabledLogicalElement do CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d574a-158">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="d574a-159">Essa propriedade pode ser não **nula** se uma implementação for capaz de anunciar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="d574a-159">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="d574a-160">Essa propriedade será **nula** se uma implementação não puder determinar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="d574a-160">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="d574a-161">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d574a-161">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="d574a-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="d574a-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="d574a-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="d574a-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="d574a-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="d574a-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="d574a-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="d574a-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="d574a-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="d574a-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="d574a-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="d574a-172">)</span><span class="sxs-lookup"><span data-stu-id="d574a-172">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d574a-173">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="d574a-173">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-174">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d574a-174">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d574a-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-176">Uma matriz que especifica os recursos da porta.</span><span class="sxs-lookup"><span data-stu-id="d574a-176">An array that specifies the capabilities of the port.</span></span> <span data-ttu-id="d574a-177">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="d574a-177">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="d574a-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d574a-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="d574a-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-180"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="d574a-180"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-181"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span><span class="sxs-lookup"><span data-stu-id="d574a-181"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-182"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Failover** (4)</span><span class="sxs-lookup"><span data-stu-id="d574a-182"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-183"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**Balanceamento de carga** (5)</span><span class="sxs-lookup"><span data-stu-id="d574a-183"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**LoadBalancing** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d574a-184">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d574a-184">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-185">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d574a-185">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d574a-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-187">Uma matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para os recursos de porta contidos na matriz **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="d574a-187">An array of free-form strings that provides more detailed explanations for the port features that are contained in the **Capabilities** array.</span></span> <span data-ttu-id="d574a-188">Cada entrada dessa matriz está relacionada à entrada correspondente na matriz de **recursos** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="d574a-188">Each entry of this array is related to the corresponding entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="d574a-189">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="d574a-189">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-190">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="d574a-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-191">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d574a-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-193">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="d574a-193">A short description of the object.</span></span> <span data-ttu-id="d574a-194">Essa propriedade é herdada da classe [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) e é sempre definida como "porta do comutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="d574a-194">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class, and it is always set to "Ethernet Switch Port".</span></span>

</dd> <dt>

<span data-ttu-id="d574a-195">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="d574a-195">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-196">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d574a-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-198">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="d574a-198">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="d574a-199">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="d574a-199">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d574a-200">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d574a-200">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-201">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d574a-201">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-202">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d574a-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-204">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="d574a-204">The scoping system's creation class name.</span></span> <span data-ttu-id="d574a-205">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como "Msvm \_ EthernetSwitchPort".</span><span class="sxs-lookup"><span data-stu-id="d574a-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="d574a-206">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d574a-206">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-207">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d574a-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-209">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="d574a-209">A description of the object.</span></span> <span data-ttu-id="d574a-210">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "porta do comutador Ethernet virtual da Microsoft".</span><span class="sxs-lookup"><span data-stu-id="d574a-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Virtual Ethernet Switch Port".</span></span>

</dd> <dt>

<span data-ttu-id="d574a-211">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="d574a-211">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-212">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d574a-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-214">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="d574a-214">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="d574a-215">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="d574a-215">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d574a-216">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d574a-216">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-217">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d574a-217">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-218">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d574a-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-219">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-220">Um endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d574a-220">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="d574a-221">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d574a-221">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-222">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d574a-222">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-223">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d574a-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-225">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="d574a-225">A display name for the object.</span></span> <span data-ttu-id="d574a-226">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d574a-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-227">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d574a-227">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-228">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d574a-228">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d574a-229">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-230">Especifica quais recursos estão habilitados na lista de todos os recursos com suporte na matriz de **recursos** .</span><span class="sxs-lookup"><span data-stu-id="d574a-230">Specifies which capabilities are enabled from the list of all supported capabilities in the **Capabilities** array.</span></span> <span data-ttu-id="d574a-231">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="d574a-231">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="d574a-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d574a-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="d574a-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-234"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="d574a-234"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-235"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span><span class="sxs-lookup"><span data-stu-id="d574a-235"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-236"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Failover** (4)</span><span class="sxs-lookup"><span data-stu-id="d574a-236"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-237"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**Balanceamento de carga** (5)</span><span class="sxs-lookup"><span data-stu-id="d574a-237"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**LoadBalancing** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d574a-238">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="d574a-238">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-239">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d574a-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-240">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-241">A configuração de inicialização ou padrão de um administrador para a propriedade **enabledstate** de um elemento.</span><span class="sxs-lookup"><span data-stu-id="d574a-241">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="d574a-242">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="d574a-242">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-243">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d574a-243">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-244">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d574a-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-245">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-246">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="d574a-246">The enabled and disabled states of an element.</span></span> <span data-ttu-id="d574a-247">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d574a-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="d574a-248">Valor</span><span class="sxs-lookup"><span data-stu-id="d574a-248">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="d574a-249">Significado</span><span class="sxs-lookup"><span data-stu-id="d574a-249">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="d574a-250"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d574a-250"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="d574a-251">O elemento está em execução.</span><span class="sxs-lookup"><span data-stu-id="d574a-251">The element is running.</span></span><br/>    |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="d574a-252"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d574a-252"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="d574a-253">O elemento está desativado.</span><span class="sxs-lookup"><span data-stu-id="d574a-253">The element is turned off.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d574a-254">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d574a-254">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-255">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d574a-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-256">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-257">Indica se o erro relatado em **LastErrorCode** agora está limpo.</span><span class="sxs-lookup"><span data-stu-id="d574a-257">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="d574a-258">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d574a-258">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d574a-259">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d574a-259">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-260">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d574a-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-261">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-262">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="d574a-262">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="d574a-263">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d574a-263">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d574a-264">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="d574a-264">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-265">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d574a-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-266">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-267">Indica se a porta está operando no modo full duplex.</span><span class="sxs-lookup"><span data-stu-id="d574a-267">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="d574a-268">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d574a-268">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-269">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="d574a-269">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-270">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d574a-270">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-271">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-272">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="d574a-272">The current health of the element.</span></span> <span data-ttu-id="d574a-273">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="d574a-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-274">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d574a-274">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-275">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d574a-275">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d574a-276">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-277">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz de propriedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="d574a-277">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="d574a-278">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d574a-278">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d574a-279">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d574a-279">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-280">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d574a-280">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-281">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-282">A data e a hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="d574a-282">The date and time when the object was installed.</span></span> <span data-ttu-id="d574a-283">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="d574a-283">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="d574a-284">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d574a-284">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-285">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d574a-285">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-286">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d574a-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-287">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d574a-288">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="d574a-288">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d574a-289">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="d574a-289">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d574a-290">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d574a-290">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-291">**IOVOffloadUsage**</span><span class="sxs-lookup"><span data-stu-id="d574a-291">**IOVOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-292">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d574a-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-293">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-294">O uso de descarregamento de IOV (virtualização de e/s) atual nesta porta.</span><span class="sxs-lookup"><span data-stu-id="d574a-294">The current I/O virtualization (IOV) offload usage on this port.</span></span> <span data-ttu-id="d574a-295">O uso é a quantidade de recursos de IOV em uso na porta.</span><span class="sxs-lookup"><span data-stu-id="d574a-295">The usage is the amount of IOV resources in use on the port.</span></span>

</dd> <dt>

<span data-ttu-id="d574a-296">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d574a-296">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-297">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d574a-297">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-299">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d574a-299">The last error code reported by the logical device.</span></span> <span data-ttu-id="d574a-300">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d574a-300">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d574a-301">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="d574a-301">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-302">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d574a-302">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-303">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-304">Especifica o tipo de tecnologia de link para a porta.</span><span class="sxs-lookup"><span data-stu-id="d574a-304">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="d574a-305">Quando definido como 1 (outro), a propriedade **OtherLinkTechnology** contém uma descrição de cadeia de caracteres do tipo de link.</span><span class="sxs-lookup"><span data-stu-id="d574a-305">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="d574a-306">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d574a-306">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="d574a-307"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d574a-307"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-308"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="d574a-308"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-309"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="d574a-309"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-310"><span id="IB"></span><span id="ib"></span>**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="d574a-310"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-311"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="d574a-311"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-312"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="d574a-312"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-313"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="d574a-313"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-314"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token ring** (7)</span><span class="sxs-lookup"><span data-stu-id="d574a-314"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-315"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="d574a-315"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-316"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infravermelho** (9)</span><span class="sxs-lookup"><span data-stu-id="d574a-316"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-317"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="d574a-317"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-318"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**LAN sem fio** (11)</span><span class="sxs-lookup"><span data-stu-id="d574a-318"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Wireless LAN** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d574a-319">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="d574a-319">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-320">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d574a-320">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-322">O tamanho máximo do campo de informações (não MAC) que será recebido ou transmitido.</span><span class="sxs-lookup"><span data-stu-id="d574a-322">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="d574a-323">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)e é sempre definida como 1500.</span><span class="sxs-lookup"><span data-stu-id="d574a-323">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="d574a-324">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="d574a-324">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-325">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d574a-325">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-326">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-327">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="d574a-327">This property has been deprecated.</span></span> <span data-ttu-id="d574a-328">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d574a-328">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d574a-329">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="d574a-329">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-330">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d574a-330">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-331">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d574a-332">Qualificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="d574a-332">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="d574a-333">A largura de banda máxima da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="d574a-333">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="d574a-334">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d574a-334">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-335">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d574a-335">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-336">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d574a-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-338">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="d574a-338">The label by which the object is known.</span></span> <span data-ttu-id="d574a-339">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d574a-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-340">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="d574a-340">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-341">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d574a-341">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d574a-342">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d574a-343">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="d574a-343">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="d574a-344">Uma matriz de cadeias de caracteres que contêm os endereços MAC para a porta.</span><span class="sxs-lookup"><span data-stu-id="d574a-344">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="d574a-345">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d574a-345">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-346">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="d574a-346">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-347">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d574a-347">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-348">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-349">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="d574a-349">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="d574a-350">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="d574a-350">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d574a-351">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d574a-351">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-352">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d574a-352">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-353">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d574a-353">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d574a-354">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-355">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="d574a-355">The current statuses of the object.</span></span> <span data-ttu-id="d574a-356">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="d574a-356">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-357">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d574a-357">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-358">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d574a-358">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d574a-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-360">Uma matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para qualquer um dos recursos habilitados que são especificados como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="d574a-360">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as 1 (Other).</span></span> <span data-ttu-id="d574a-361">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="d574a-361">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-362">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="d574a-362">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-363">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d574a-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-364">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-365">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="d574a-365">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="d574a-366">Essa propriedade deve ser definida como **NULL** quando a propriedade **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="d574a-366">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="d574a-367">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d574a-367">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d574a-368">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="d574a-368">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-369">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d574a-369">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d574a-370">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-371">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d574a-371">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="d574a-372">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d574a-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d574a-373">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="d574a-373">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-374">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d574a-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-376">Um valor de cadeia de caracteres que descreve **LinkTechnology** quando é definido como 1, (outro).</span><span class="sxs-lookup"><span data-stu-id="d574a-376">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="d574a-377">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d574a-377">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-378">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="d574a-378">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-379">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d574a-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-380">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-381">O uso dessa propriedade é preterido no lugar da propriedade **PortType** .</span><span class="sxs-lookup"><span data-stu-id="d574a-381">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="d574a-382">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d574a-382">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-383">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="d574a-383">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-384">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d574a-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-385">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-386">Descreve o tipo de módulo, quando **PortType** é definido como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="d574a-386">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="d574a-387">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d574a-387">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-388">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="d574a-388">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-389">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d574a-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-390">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d574a-391">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="d574a-391">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="d574a-392">O endereço de rede embutido em uma porta.</span><span class="sxs-lookup"><span data-stu-id="d574a-392">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="d574a-393">Esse endereço codificado pode ser alterado usando uma atualização de firmware ou uma configuração de software.</span><span class="sxs-lookup"><span data-stu-id="d574a-393">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="d574a-394">Quando essa alteração é feita, o campo deve ser atualizado ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="d574a-394">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="d574a-395">Essa propriedade deverá ser **nula** se não existir nenhum endereço codificado para o adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="d574a-395">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="d574a-396">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d574a-396">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-397">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="d574a-397">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-398">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d574a-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-399">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-400">O número da porta.</span><span class="sxs-lookup"><span data-stu-id="d574a-400">The port number.</span></span> <span data-ttu-id="d574a-401">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d574a-401">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-402">**PortType**</span><span class="sxs-lookup"><span data-stu-id="d574a-402">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-403">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d574a-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-404">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-405">O modo específico que está habilitado no momento para a porta.</span><span class="sxs-lookup"><span data-stu-id="d574a-405">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="d574a-406">Quando definido como 1 (outro), a propriedade **OtherPortType** relacionada contém uma descrição de cadeia de caracteres do tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="d574a-406">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="d574a-407">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d574a-407">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="d574a-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d574a-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-409"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="d574a-409"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-410"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>+ **/50 10BaseT de cobre** (50)</span><span class="sxs-lookup"><span data-stu-id="d574a-410"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-411"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="d574a-411"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-412"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="d574a-412"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-413"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000baseT** (53)</span><span class="sxs-lookup"><span data-stu-id="d574a-413"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-414"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="d574a-414"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-415"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="d574a-415"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-416"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="d574a-416"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-417"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**100 Fibre 100BASE-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="d574a-417"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-418"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="d574a-418"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-419"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="d574a-419"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-420"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="d574a-420"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-421"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000BASE-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="d574a-421"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-422"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-Sr** (105)</span><span class="sxs-lookup"><span data-stu-id="d574a-422"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-423"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="d574a-423"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-424"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="d574a-424"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-425"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="d574a-425"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-426"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="d574a-426"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-427"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="d574a-427"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-428"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-ovo** (111)</span><span class="sxs-lookup"><span data-stu-id="d574a-428"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-429"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="d574a-429"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d574a-430">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d574a-430">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-431">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d574a-431">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d574a-432">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-433">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d574a-433">The power management capabilities of the device.</span></span> <span data-ttu-id="d574a-434">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d574a-434">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d574a-435">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d574a-435">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-436">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d574a-436">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-437">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-438">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="d574a-438">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="d574a-439">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d574a-439">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d574a-440">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="d574a-440">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-441">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d574a-441">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-442">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-443">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="d574a-443">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="d574a-444">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d574a-444">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d574a-445">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="d574a-445">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-446">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d574a-446">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-447">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-448">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="d574a-448">Provides high level status information.</span></span> <span data-ttu-id="d574a-449">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer informações de status de integridade detalhadas e de alto nível para o elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="d574a-449">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="d574a-450">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="d574a-450">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d574a-451">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d574a-451">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-452">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="d574a-452">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-453">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d574a-453">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-454">Tipo de acesso: somente gravação</span><span class="sxs-lookup"><span data-stu-id="d574a-454">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="d574a-455">Qualificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="d574a-455">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="d574a-456">A largura de banda solicitada da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="d574a-456">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="d574a-457">A largura de banda real é relatada na propriedade **Speed** .</span><span class="sxs-lookup"><span data-stu-id="d574a-457">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="d574a-458">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d574a-458">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-459">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="d574a-459">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-460">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d574a-460">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-461">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-461">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-462">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="d574a-462">The last requested or desired state for the element.</span></span> <span data-ttu-id="d574a-463">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 12 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="d574a-463">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-464">**Velocidade**</span><span class="sxs-lookup"><span data-stu-id="d574a-464">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-465">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d574a-465">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-466">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d574a-467">Qualificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="d574a-467">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="d574a-468">A largura de banda da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="d574a-468">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="d574a-469">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d574a-469">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-470">**Status**</span><span class="sxs-lookup"><span data-stu-id="d574a-470">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-471">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d574a-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-472">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-473">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="d574a-473">The current status of the object.</span></span> <span data-ttu-id="d574a-474">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d574a-474">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d574a-475">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d574a-475">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-476">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d574a-476">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d574a-477">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-477">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-478">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="d574a-478">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="d574a-479">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d574a-479">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-480">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d574a-480">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-481">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d574a-481">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-482">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-483">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d574a-483">The current state of the logical device.</span></span> <span data-ttu-id="d574a-484">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d574a-484">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d574a-485">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="d574a-485">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-486">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d574a-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-487">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d574a-488">Qualificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="d574a-488">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d574a-489">A MTU (unidade máxima de transmissão) que pode ter suporte, em bytes.</span><span class="sxs-lookup"><span data-stu-id="d574a-489">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="d574a-490">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d574a-490">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-491">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d574a-491">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-492">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d574a-492">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-493">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-493">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-494">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="d574a-494">The scoping system's creation class name.</span></span> <span data-ttu-id="d574a-495">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como "Msvm \_ VirtualEthernetSwitch".</span><span class="sxs-lookup"><span data-stu-id="d574a-495">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="d574a-496">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d574a-496">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-497">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d574a-497">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-498">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-498">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-499">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="d574a-499">The scoping system's name.</span></span> <span data-ttu-id="d574a-500">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d574a-500">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d574a-501">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="d574a-501">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-502">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d574a-502">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-503">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-503">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-504">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="d574a-504">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="d574a-505">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d574a-505">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d574a-506">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="d574a-506">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-507">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d574a-507">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-508">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-509">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="d574a-509">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="d574a-510">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d574a-510">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d574a-511">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="d574a-511">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-512">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d574a-512">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-513">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-513">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-514">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="d574a-514">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="d574a-515">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d574a-515">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d574a-516">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="d574a-516">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-517">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d574a-517">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-518">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-519">Em algumas circunstâncias, uma porta lógica pode ser identificável como uma porta de front-end ou de back-end.</span><span class="sxs-lookup"><span data-stu-id="d574a-519">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="d574a-520">Um exemplo dessa situação seria uma matriz de armazenamento que pode ter portas de back-end para se comunicar com unidades de disco e portas de front-end para se comunicar com os hosts.</span><span class="sxs-lookup"><span data-stu-id="d574a-520">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="d574a-521">Se não houver nenhuma restrição sobre o uso da porta, o valor deverá ser definido como 4 (não restrito).</span><span class="sxs-lookup"><span data-stu-id="d574a-521">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="d574a-522">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d574a-522">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="d574a-523"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d574a-523"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-524"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Somente front-end** (2)</span><span class="sxs-lookup"><span data-stu-id="d574a-524"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-525"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Somente back-end** (3)</span><span class="sxs-lookup"><span data-stu-id="d574a-525"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d574a-526"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Não restrito** (4)</span><span class="sxs-lookup"><span data-stu-id="d574a-526"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d574a-527">**VMQOffloadUsage**</span><span class="sxs-lookup"><span data-stu-id="d574a-527">**VMQOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d574a-528">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d574a-528">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d574a-529">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d574a-529">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d574a-530">O uso de descarregamento da fila de máquina virtual (VMQ) atual nesta porta.</span><span class="sxs-lookup"><span data-stu-id="d574a-530">The current virtual machine queue (VMQ) offloading usage on this port.</span></span> <span data-ttu-id="d574a-531">O uso é a quantidade de recursos de VMQ em uso na porta.</span><span class="sxs-lookup"><span data-stu-id="d574a-531">The usage is the amount of VMQ resources in use on the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d574a-532">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d574a-532">Requirements</span></span>



| <span data-ttu-id="d574a-533">Requisito</span><span class="sxs-lookup"><span data-stu-id="d574a-533">Requirement</span></span> | <span data-ttu-id="d574a-534">Valor</span><span class="sxs-lookup"><span data-stu-id="d574a-534">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d574a-535">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d574a-535">Minimum supported client</span></span><br/> | <span data-ttu-id="d574a-536">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d574a-536">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d574a-537">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d574a-537">Minimum supported server</span></span><br/> | <span data-ttu-id="d574a-538">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d574a-538">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d574a-539">Namespace</span><span class="sxs-lookup"><span data-stu-id="d574a-539">Namespace</span></span><br/>                | <span data-ttu-id="d574a-540">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d574a-540">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d574a-541">MOF</span><span class="sxs-lookup"><span data-stu-id="d574a-541">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d574a-542"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d574a-542"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d574a-543">DLL</span><span class="sxs-lookup"><span data-stu-id="d574a-543">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d574a-544"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d574a-544"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

