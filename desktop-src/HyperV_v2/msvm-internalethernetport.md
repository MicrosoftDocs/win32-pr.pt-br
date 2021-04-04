---
description: Representa uma porta Ethernet interna (adaptador de rede).
ms.assetid: 43277FA7-E040-49F2-A086-AF19B29D4F75
title: Classe Msvm_InternalEthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InternalEthernetPort
- Msvm_InternalEthernetPort.SetPowerState
- Msvm_InternalEthernetPort.EnableDevice
- Msvm_InternalEthernetPort.OnlineDevice
- Msvm_InternalEthernetPort.QuiesceDevice
- Msvm_InternalEthernetPort.SaveProperties
- Msvm_InternalEthernetPort.RestoreProperties
- Msvm_InternalEthernetPort.InstanceID
- Msvm_InternalEthernetPort.Caption
- Msvm_InternalEthernetPort.Description
- Msvm_InternalEthernetPort.ElementName
- Msvm_InternalEthernetPort.InstallDate
- Msvm_InternalEthernetPort.Name
- Msvm_InternalEthernetPort.OperationalStatus
- Msvm_InternalEthernetPort.StatusDescriptions
- Msvm_InternalEthernetPort.Status
- Msvm_InternalEthernetPort.HealthState
- Msvm_InternalEthernetPort.CommunicationStatus
- Msvm_InternalEthernetPort.DetailedStatus
- Msvm_InternalEthernetPort.OperatingStatus
- Msvm_InternalEthernetPort.PrimaryStatus
- Msvm_InternalEthernetPort.EnabledState
- Msvm_InternalEthernetPort.OtherEnabledState
- Msvm_InternalEthernetPort.RequestedState
- Msvm_InternalEthernetPort.EnabledDefault
- Msvm_InternalEthernetPort.TimeOfLastStateChange
- Msvm_InternalEthernetPort.AvailableRequestedStates
- Msvm_InternalEthernetPort.TransitioningToState
- Msvm_InternalEthernetPort.SystemCreationClassName
- Msvm_InternalEthernetPort.SystemName
- Msvm_InternalEthernetPort.CreationClassName
- Msvm_InternalEthernetPort.DeviceID
- Msvm_InternalEthernetPort.PowerManagementSupported
- Msvm_InternalEthernetPort.PowerManagementCapabilities
- Msvm_InternalEthernetPort.Availability
- Msvm_InternalEthernetPort.StatusInfo
- Msvm_InternalEthernetPort.LastErrorCode
- Msvm_InternalEthernetPort.ErrorDescription
- Msvm_InternalEthernetPort.ErrorCleared
- Msvm_InternalEthernetPort.OtherIdentifyingInfo
- Msvm_InternalEthernetPort.PowerOnHours
- Msvm_InternalEthernetPort.TotalPowerOnHours
- Msvm_InternalEthernetPort.IdentifyingDescriptions
- Msvm_InternalEthernetPort.AdditionalAvailability
- Msvm_InternalEthernetPort.MaxQuiesceTime
- Msvm_InternalEthernetPort.MaxSpeed
- Msvm_InternalEthernetPort.RequestedSpeed
- Msvm_InternalEthernetPort.UsageRestriction
- Msvm_InternalEthernetPort.OtherPortType
- Msvm_InternalEthernetPort.Speed
- Msvm_InternalEthernetPort.OtherNetworkPortType
- Msvm_InternalEthernetPort.PortNumber
- Msvm_InternalEthernetPort.LinkTechnology
- Msvm_InternalEthernetPort.OtherLinkTechnology
- Msvm_InternalEthernetPort.PermanentAddress
- Msvm_InternalEthernetPort.FullDuplex
- Msvm_InternalEthernetPort.AutoSense
- Msvm_InternalEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_InternalEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_InternalEthernetPort.PortType
- Msvm_InternalEthernetPort.NetworkAddresses
- Msvm_InternalEthernetPort.MaxDataSize
- Msvm_InternalEthernetPort.Capabilities
- Msvm_InternalEthernetPort.CapabilityDescriptions
- Msvm_InternalEthernetPort.EnabledCapabilities
- Msvm_InternalEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a1441055fc7b86b97c69a40758236261b20f75c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647366"
---
# <a name="msvm_internalethernetport-class"></a><span data-ttu-id="d3a6f-103">\_Classe Msvm InternalEthernetPort</span><span class="sxs-lookup"><span data-stu-id="d3a6f-103">Msvm\_InternalEthernetPort class</span></span>

<span data-ttu-id="d3a6f-104">Representa uma porta Ethernet interna (adaptador de rede).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-104">Represents an internal Ethernet port (network adapter).</span></span> <span data-ttu-id="d3a6f-105">Esse tipo de porta Ethernet dá acesso às máquinas virtuais ao servidor de virtualização que executa o software de rede.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-105">This type of Ethernet port gives virtual machines access to the virtualization server running the networking software.</span></span> <span data-ttu-id="d3a6f-106">Os adaptadores de rede internos permitem que o tráfego de rede das máquinas virtuais seja roteado ou filtrado antes de sair do sistema físico.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-106">The internal network adapters allow the virtual machines network traffic to be routed or filtered before leaving the physical system.</span></span>

<span data-ttu-id="d3a6f-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3a6f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3a6f-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InternalEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft Internal Ethernet Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
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
  string   CreationClassName = "Msvm_InternalEthernetPort";
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
  uint16   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint64   MaxSpeed = 1000000000;
  uint64   RequestedSpeed = 1000000000;
  uint16   UsageRestriction = 4;
  string   OtherPortType;
  uint64   Speed;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 2;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  boolean  FullDuplex = True;
  boolean  AutoSense = True;
  uint64   SupportedMaximumTransmissionUnit = 1500;
  uint64   ActiveMaximumTransmissionUnit = 1500;
  uint16   PortType;
  string   NetworkAddresses[];
  uint32   MaxDataSize = 1500;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="d3a6f-109">Membros</span><span class="sxs-lookup"><span data-stu-id="d3a6f-109">Members</span></span>

<span data-ttu-id="d3a6f-110">A classe **Msvm \_ InternalEthernetPort** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d3a6f-110">The **Msvm\_InternalEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="d3a6f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="d3a6f-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="d3a6f-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d3a6f-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d3a6f-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="d3a6f-113">Methods</span></span>

<span data-ttu-id="d3a6f-114">A classe **Msvm \_ InternalEthernetPort** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-114">The **Msvm\_InternalEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="d3a6f-115">Método</span><span class="sxs-lookup"><span data-stu-id="d3a6f-115">Method</span></span>                                                                     | <span data-ttu-id="d3a6f-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d3a6f-116">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="d3a6f-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-117">**EnableDevice**</span></span>                                                           | <span data-ttu-id="d3a6f-118">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d3a6f-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-119">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="d3a6f-120">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d3a6f-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-121">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="d3a6f-122">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="d3a6f-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-123">**RequestStateChange**</span></span>](msvm-internalethernetport-requeststatechange.md) | <span data-ttu-id="d3a6f-124">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-124">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="d3a6f-125">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-125">**Reset**</span></span>](msvm-internalethernetport-reset.md)                           | <span data-ttu-id="d3a6f-126">Redefine o dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="d3a6f-127">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-127">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="d3a6f-128">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d3a6f-129">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-129">**SaveProperties**</span></span>                                                         | <span data-ttu-id="d3a6f-130">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d3a6f-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-131">**SetPowerState**</span></span>                                                          | <span data-ttu-id="d3a6f-132">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d3a6f-133">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d3a6f-133">Properties</span></span>

<span data-ttu-id="d3a6f-134">A classe **Msvm \_ InternalEthernetPort** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-134">The **Msvm\_InternalEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d3a6f-135">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-135">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-136">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-138">A unidade de transmissão máxima (MTU) do negociada ou ativa, que pode ter suporte.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-138">The active or negotiated maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="d3a6f-139">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-141">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-143">Qualquer disponibilidade e status adicionais do dispositivo, além do especificado na propriedade de **disponibilidade** .</span><span class="sxs-lookup"><span data-stu-id="d3a6f-143">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="d3a6f-144">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-145">**Autodetecção**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-146">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-148">Indica se a porta de rede é capaz de determinar automaticamente a velocidade ou outras características de comunicação da mídia de rede anexada.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="d3a6f-149">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-150">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-151">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-153">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-153">The primary availability and status of the device.</span></span> <span data-ttu-id="d3a6f-154">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-156">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-158">Indica os valores possíveis para o parâmetro *requestedstate* do método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="d3a6f-159">Os valores listados serão um subconjunto dos valores contidos na propriedade **RequestedStatesSupported** da instância associada do **CIM \_ EnabledLogicalElementCapabilities**, em que os valores selecionados são uma função do estado atual do objeto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d3a6f-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="d3a6f-160">Essa propriedade pode ser não **nula** se uma implementação for capaz de anunciar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="d3a6f-161">Essa propriedade será **nula** se uma implementação não puder determinar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="d3a6f-162">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-163">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-163">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-164">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-166">Recursos da porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-166">Capabilities of the Ethernet port.</span></span> <span data-ttu-id="d3a6f-167">Se os recursos de failover ou balanceamento de carga estiverem listados, um (failover) [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-sparegroup) ou [**CIM \_ ExtraCapacityGroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (balanceamento de carga) também deverá ser definido para descrever completamente o recurso.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-167">If failover or load balancing capabilities are listed, a [**CIM\_SpareGroup**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (failover) or [**CIM\_ExtraCapacityGroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (load balancing) should also be defined to completely describe the capability.</span></span> <span data-ttu-id="d3a6f-168">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-168">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="d3a6f-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-171"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-171"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-172"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-172"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-173"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Failover** (4)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-173"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-174"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**Balanceamento de carga** (5)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-174"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d3a6f-175">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-175">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-176">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-176">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-178">Uma matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para qualquer um dos recursos de porta Ethernet que são indicados na matriz **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="d3a6f-178">An array of free-form strings that provides more detailed explanations for any of the Ethernet port features that are indicated in the **Capabilities** array.</span></span> <span data-ttu-id="d3a6f-179">Observe que cada entrada dessa matriz está relacionada à entrada na matriz de **recursos** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-179">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="d3a6f-180">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-180">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-181">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-181">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-184">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-184">A short description of the object.</span></span> <span data-ttu-id="d3a6f-185">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-186">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-186">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-187">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-189">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-189">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="d3a6f-190">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d3a6f-191">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-192">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-192">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-193">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-195">O nome da classe ou da subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-195">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="d3a6f-196">Quando usado com as outras propriedades de chave dessa classe, essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-196">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="d3a6f-197">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-197">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-198">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-198">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-199">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-201">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="d3a6f-201">A description of the object.</span></span> <span data-ttu-id="d3a6f-202">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-202">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-203">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-203">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-204">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-206">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-206">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="d3a6f-207">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-207">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d3a6f-208">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-209">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-209">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-212">Um endereço ou outras informações de identificação usadas para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-212">An address or other identifying information used to uniquely name the logical device.</span></span> <span data-ttu-id="d3a6f-213">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como "Microsoft:*GUID* \\ *específico do dispositivo-dados*".</span><span class="sxs-lookup"><span data-stu-id="d3a6f-213">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-214">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-214">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-215">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-216">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d3a6f-216">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-217">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-217">A display name for the object.</span></span> <span data-ttu-id="d3a6f-218">Essa propriedade permite que cada instância defina um nome de exibição além de suas propriedades de chave, dados de identidade e informações de descrição.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-218">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="d3a6f-219">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) e é gerada com base na NIC presente no host.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-219">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) and is generated based on the NIC present in the host.</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-220">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-220">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-221">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-221">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-223">Especifica quais recursos estão habilitados na lista de todos os que têm suporte, que são definidos na matriz de **recursos** .</span><span class="sxs-lookup"><span data-stu-id="d3a6f-223">Specifies which capabilities are enabled from the list of all supported ones, which are defined in the **Capabilities** array.</span></span> <span data-ttu-id="d3a6f-224">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-224">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="d3a6f-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-226"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-226"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-227"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-227"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-228"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-228"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-229"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Failover** (4)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-229"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-230"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**Balanceamento de carga** (5)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-230"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d3a6f-231">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-231">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-232">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-232">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-234">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-234">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="d3a6f-235">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-235">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-236">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-236">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-237">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-239">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-239">The enabled and disabled states of an element.</span></span> <span data-ttu-id="d3a6f-240">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-240">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-241">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-241">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-242">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-243">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-244">Indica se o erro relatado na propriedade **LastErrorCode** agora está apagado.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-244">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="d3a6f-245">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-245">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-246">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-246">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-247">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-249">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado na propriedade **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-249">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="d3a6f-250">Essa propriedade é herdada da propriedade [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) property and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-251">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-251">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-252">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-252">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-253">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-254">Indica se a porta está operando no modo full duplex.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-254">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="d3a6f-255">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-255">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-256">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-256">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-257">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-259">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-259">The current health of the element.</span></span> <span data-ttu-id="d3a6f-260">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-260">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="d3a6f-261">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-262">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-262">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-263">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-263">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-264">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-265">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz de propriedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="d3a6f-265">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="d3a6f-266">Cada entrada dessa matriz está relacionada à entrada na matriz da propriedade **OtherIdentifyingInfo** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-266">Each entry of this array is related to the entry in the **OtherIdentifyingInfo** property array that is located at the same index.</span></span> <span data-ttu-id="d3a6f-267">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-268">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-268">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-269">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-271">Um valor **DateTime** que indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-271">A **datetime** value that indicates when the object was installed.</span></span> <span data-ttu-id="d3a6f-272">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-272">Lack of a value does not indicate that the object is not installed.</span></span> <span data-ttu-id="d3a6f-273">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-274">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-274">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-275">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-276">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-277">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-277">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-278">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-278">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d3a6f-279">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-279">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-280">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-280">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-281">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-281">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-282">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-283">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-283">The last error code reported by the logical device.</span></span> <span data-ttu-id="d3a6f-284">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-284">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-285">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-285">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-286">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-286">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-287">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-288">Os tipos de links.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-288">The types of links.</span></span> <span data-ttu-id="d3a6f-289">Quando definido como 1 (outro), a propriedade relacionada **OtherLinkTechnology** contém uma descrição de cadeia de caracteres do tipo de link.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-289">When set to 1 (Other), the related property **OtherLinkTechnology** contains a string description of the type of link.</span></span> <span data-ttu-id="d3a6f-290">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-290">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>



| <span data-ttu-id="d3a6f-291">Valor</span><span class="sxs-lookup"><span data-stu-id="d3a6f-291">Value</span></span>                                                                        | <span data-ttu-id="d3a6f-292">Significado</span><span class="sxs-lookup"><span data-stu-id="d3a6f-292">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="d3a6f-293"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d3a6f-293"><dt>2</dt></span></span> </dl> | <span data-ttu-id="d3a6f-294">Ethernet</span><span class="sxs-lookup"><span data-stu-id="d3a6f-294">Ethernet</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d3a6f-295">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-295">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-296">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-296">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-297">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-298">O tamanho máximo do campo de informações (não MAC) que será recebido ou transmitido.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-298">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="d3a6f-299">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-299">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-300">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-300">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-301">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-301">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-303">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-303">This property has been deprecated.</span></span> <span data-ttu-id="d3a6f-304">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-304">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-305">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-305">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-306">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-306">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-307">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-308">A largura de banda máxima da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-308">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="d3a6f-309">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-309">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-310">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-310">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-311">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-312">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-313">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-313">The label by which the object is known.</span></span> <span data-ttu-id="d3a6f-314">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-314">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="d3a6f-315">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-316">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-316">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-317">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-317">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-319">Os endereços MAC Ethernet/802.3 formatados como doze dígitos hexadecimais (por exemplo, "010203040506"), com cada par representando um dos seis octetos do endereço MAC na ordem de bits canônica (o bit de endereço do grupo é encontrado no bit inferior do primeiro caractere da cadeia de caracteres). Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-319">The Ethernet/802.3 MAC addresses formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (the Group address bit is found in the low order bit of the first character of the string.) This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-320">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-320">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-321">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-323">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="d3a6f-323">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="d3a6f-324">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-324">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d3a6f-325">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-326">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-326">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-327">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-327">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-329">O status atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-329">The current statuses of the element.</span></span> <span data-ttu-id="d3a6f-330">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-330">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-331">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-331">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-332">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-332">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-333">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-334">Uma matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para qualquer um dos recursos habilitados que são especificados como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-334">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as 1 (Other).</span></span> <span data-ttu-id="d3a6f-335">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-335">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-336">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-336">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-337">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-338">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-339">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro.) Essa propriedade deve ser definida como **NULL** quando a propriedade **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-339">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other.) This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="d3a6f-340">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-340">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-341">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-341">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-342">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-344">Todos os dados, além das informações de ID do dispositivo, que podem ser usados para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-344">Any data, in addition to device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="d3a6f-345">Por exemplo, você pode usar essa propriedade para armazenar o nome de exibição do sistema operacional para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-345">For example, you could use this property to hold the operating system's display name for the device.</span></span> <span data-ttu-id="d3a6f-346">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-346">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-347">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-347">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-348">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-349">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-350">Um valor de cadeia de caracteres que descreve a propriedade **LinkTechnology** quando ela é definida como 1 (outra).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-350">A string value that describes the **LinkTechnology** property when it is set to 1 (Other).</span></span> <span data-ttu-id="d3a6f-351">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-351">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-352">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-352">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-353">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-354">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-355">Essa propriedade é preterida.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-355">This property is deprecated.</span></span> <span data-ttu-id="d3a6f-356">Use a propriedade **PortType** .</span><span class="sxs-lookup"><span data-stu-id="d3a6f-356">Use the **PortType** property.</span></span> <span data-ttu-id="d3a6f-357">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-357">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<span data-ttu-id="d3a6f-358">Descrição preterida: o tipo de módulo, quando a propriedade **PortType** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-358">Deprecated description: The type of module, when the **PortType** property is set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-359">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-359">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-360">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-362">O tipo de módulo, quando a propriedade **PortType** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-362">The type of module, when the **PortType** property is set to 1 (Other).</span></span> <span data-ttu-id="d3a6f-363">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d3a6f-363">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)) .</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-364">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-364">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-365">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-366">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-367">O endereço de rede embutido em uma porta.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-367">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="d3a6f-368">Esse endereço pode ser alterado usando uma atualização de firmware ou uma configuração de software.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-368">This address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="d3a6f-369">Quando essa alteração é feita, o campo deve ser atualizado ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-369">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="d3a6f-370">Isso deve ser deixado em branco se não existir nenhum endereço codificado para o adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-370">This should be left blank if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="d3a6f-371">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-371">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-372">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-372">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-373">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-374">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-375">As portas de rede geralmente são numeradas em relação a um módulo lógico ou um elemento de rede.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-375">Network ports are often numbered relative to either a logical module or a network element.</span></span> <span data-ttu-id="d3a6f-376">Esse valor é 1 para NICs emuladas, 0 para todos os outros.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-376">This value is 1 for emulated NICs, 0 for all others.</span></span> <span data-ttu-id="d3a6f-377">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-377">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-378">**PortType**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-378">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-379">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-380">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-381">O modo específico que está habilitado no momento para a porta.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-381">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="d3a6f-382">Quando definido como 1 (outro), a propriedade relacionada **OtherPortType** contém uma descrição de cadeia de caracteres do tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-382">When set to 1 (Other), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="d3a6f-383">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-383">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="d3a6f-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-385"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-385"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-386"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>+ **/50 10BaseT de cobre** (50)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-386"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-387"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-387"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-388"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-388"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-389"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000baseT** (53)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-389"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-390"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-390"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-391"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-391"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-392"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-392"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-393"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**100 Fibre 100BASE-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-393"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-394"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-394"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-395"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-395"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-396"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-396"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-397"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000BASE-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-397"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-398"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-Sr** (105)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-398"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-399"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-399"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-400"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-400"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-401"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-401"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-402"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-402"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-403"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-403"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-404"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-ovo** (111)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-404"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-405"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (16000 65535)</span><span class="sxs-lookup"><span data-stu-id="d3a6f-405"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (16000 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d3a6f-406">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-406">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-407">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-407">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-408">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-409">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-409">The power management capabilities of the device.</span></span> <span data-ttu-id="d3a6f-410">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-410">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-411">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-411">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-412">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-413">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-414">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-414">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="d3a6f-415">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-415">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-416">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-416">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-417">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-417">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-418">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-419">O número de horas consecutivas em que este dispositivo foi ligado, desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-419">The number of consecutive hours that this device has been powered, since its last power cycle.</span></span> <span data-ttu-id="d3a6f-420">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-420">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-421">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-421">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-422">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-422">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-423">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-424">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-424">Provides high level status information.</span></span> <span data-ttu-id="d3a6f-425">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer informações de status de integridade detalhadas e de alto nível para o elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-425">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="d3a6f-426">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-426">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d3a6f-427">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-428">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-428">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-429">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-429">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-430">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-431">A largura de banda solicitada da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-431">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="d3a6f-432">A largura de banda real é relatada na propriedade **Speed** .</span><span class="sxs-lookup"><span data-stu-id="d3a6f-432">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="d3a6f-433">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-433">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-434">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-434">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-435">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-436">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-437">O último estado solicitado ou desejado para o serviço de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-437">The last requested or desired state for the management service.</span></span> <span data-ttu-id="d3a6f-438">Quando a propriedade **enabledstate** é definida como 5 (não aplicável), essa propriedade não tem significado.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-438">When the **EnabledState** property is set to 5 (Not Applicable), then this property has no meaning.</span></span> <span data-ttu-id="d3a6f-439">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-439">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-440">**Velocidade**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-440">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-441">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-441">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-442">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-442">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-443">Qualificadores: **substituição**, **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="d3a6f-443">Qualifiers: **Override**, **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-444">A largura de banda atual da porta em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-444">The current bandwidth of the port in bits per second.</span></span> <span data-ttu-id="d3a6f-445">Para portas que variam de largura de banda ou para aquelas em que não é possível fazer nenhuma estimativa precisa, essa propriedade deve conter a largura de banda nominal.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-445">For ports that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span> <span data-ttu-id="d3a6f-446">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-446">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-447">**Status**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-447">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-448">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-449">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-450">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-450">The current status of the object.</span></span> <span data-ttu-id="d3a6f-451">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-451">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-452">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-452">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-453">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-453">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-454">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-454">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-455">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="d3a6f-455">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="d3a6f-456">As entradas nessa matriz são correlacionadas com aquelas no mesmo índice de matriz em **OperationalStatus**.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-456">Entries in this array are correlated with those at the same array index in **OperationalStatus**.</span></span> <span data-ttu-id="d3a6f-457">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-457">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-458">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-458">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-459">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-460">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-461">O estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-461">The state of the logical device.</span></span> <span data-ttu-id="d3a6f-462">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-463">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-463">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-464">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-464">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-465">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-466">A MTU (unidade máxima de transmissão) que pode ter suporte.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-466">The maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="d3a6f-467">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-467">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-468">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-468">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-469">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-470">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-471">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-471">The scoping system's creation class name.</span></span> <span data-ttu-id="d3a6f-472">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é suportada</span><span class="sxs-lookup"><span data-stu-id="d3a6f-472">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not supported</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-473">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-473">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-474">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-475">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-476">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-476">The name of the scoping system.</span></span> <span data-ttu-id="d3a6f-477">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-477">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-478">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-478">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-479">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-479">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-480">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-481">A data ou a hora em que a propriedade **enabledstate** do elemento foi alterada pela última vez.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-481">The date or time when the **EnabledState** property of the element last changed.</span></span> <span data-ttu-id="d3a6f-482">Se o estado do elemento não tiver sido alterado e essa propriedade for populada, ela deverá ser definida como um valor de intervalo de 0.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-482">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="d3a6f-483">Se uma alteração de estado foi solicitada, mas rejeitada ou ainda não processada, a propriedade não deve ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-483">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="d3a6f-484">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-484">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-485">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-485">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-486">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-487">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-488">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-488">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="d3a6f-489">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-489">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-490">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-490">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-491">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-491">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-492">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-492">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-493">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-493">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="d3a6f-494">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-494">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d3a6f-495">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-495">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3a6f-496">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-496">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d3a6f-497">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3a6f-497">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3a6f-498">Em algumas circunstâncias, uma porta lógica pode ser identificável como uma porta de front-end ou de back-end.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-498">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="d3a6f-499">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-499">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>



| <span data-ttu-id="d3a6f-500">Valor</span><span class="sxs-lookup"><span data-stu-id="d3a6f-500">Value</span></span>                                                                        | <span data-ttu-id="d3a6f-501">Significado</span><span class="sxs-lookup"><span data-stu-id="d3a6f-501">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="d3a6f-502"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d3a6f-502"><dt>4</dt></span></span> </dl> | <span data-ttu-id="d3a6f-503">Não restrito</span><span class="sxs-lookup"><span data-stu-id="d3a6f-503">Not Restricted</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d3a6f-504">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3a6f-504">Remarks</span></span>

<span data-ttu-id="d3a6f-505">O acesso à classe **Msvm \_ InternalEthernetPort** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-505">Access to the **Msvm\_InternalEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d3a6f-506">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-506">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="d3a6f-507">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d3a6f-507">Examples</span></span>

<span data-ttu-id="d3a6f-508">Consulte [consultando objetos de rede](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d3a6f-508">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3a6f-509">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3a6f-509">Requirements</span></span>



| <span data-ttu-id="d3a6f-510">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3a6f-510">Requirement</span></span> | <span data-ttu-id="d3a6f-511">Valor</span><span class="sxs-lookup"><span data-stu-id="d3a6f-511">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3a6f-512">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3a6f-512">Minimum supported client</span></span><br/> | <span data-ttu-id="d3a6f-513">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d3a6f-513">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d3a6f-514">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3a6f-514">Minimum supported server</span></span><br/> | <span data-ttu-id="d3a6f-515">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d3a6f-515">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d3a6f-516">Namespace</span><span class="sxs-lookup"><span data-stu-id="d3a6f-516">Namespace</span></span><br/>                | <span data-ttu-id="d3a6f-517">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d3a6f-517">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d3a6f-518">MOF</span><span class="sxs-lookup"><span data-stu-id="d3a6f-518">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3a6f-519"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3a6f-519"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3a6f-520">DLL</span><span class="sxs-lookup"><span data-stu-id="d3a6f-520">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3a6f-521"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d3a6f-521"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d3a6f-522">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3a6f-522">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3a6f-523">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-523">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="d3a6f-524">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="d3a6f-524">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

