---
description: Representa um adaptador Ethernet sintético.
ms.assetid: B5CB86A9-015B-42E8-ADF4-2F61970D8437
title: Classe Msvm_SyntheticEthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticEthernetPort
- Msvm_SyntheticEthernetPort.SetPowerState
- Msvm_SyntheticEthernetPort.EnableDevice
- Msvm_SyntheticEthernetPort.OnlineDevice
- Msvm_SyntheticEthernetPort.QuiesceDevice
- Msvm_SyntheticEthernetPort.SaveProperties
- Msvm_SyntheticEthernetPort.RestoreProperties
- Msvm_SyntheticEthernetPort.InstanceID
- Msvm_SyntheticEthernetPort.Caption
- Msvm_SyntheticEthernetPort.Description
- Msvm_SyntheticEthernetPort.ElementName
- Msvm_SyntheticEthernetPort.InstallDate
- Msvm_SyntheticEthernetPort.Name
- Msvm_SyntheticEthernetPort.OperationalStatus
- Msvm_SyntheticEthernetPort.StatusDescriptions
- Msvm_SyntheticEthernetPort.Status
- Msvm_SyntheticEthernetPort.HealthState
- Msvm_SyntheticEthernetPort.CommunicationStatus
- Msvm_SyntheticEthernetPort.DetailedStatus
- Msvm_SyntheticEthernetPort.OperatingStatus
- Msvm_SyntheticEthernetPort.PrimaryStatus
- Msvm_SyntheticEthernetPort.EnabledState
- Msvm_SyntheticEthernetPort.OtherEnabledState
- Msvm_SyntheticEthernetPort.RequestedState
- Msvm_SyntheticEthernetPort.EnabledDefault
- Msvm_SyntheticEthernetPort.TimeOfLastStateChange
- Msvm_SyntheticEthernetPort.AvailableRequestedStates
- Msvm_SyntheticEthernetPort.TransitioningToState
- Msvm_SyntheticEthernetPort.SystemCreationClassName
- Msvm_SyntheticEthernetPort.SystemName
- Msvm_SyntheticEthernetPort.CreationClassName
- Msvm_SyntheticEthernetPort.DeviceID
- Msvm_SyntheticEthernetPort.PowerManagementSupported
- Msvm_SyntheticEthernetPort.PowerManagementCapabilities
- Msvm_SyntheticEthernetPort.Availability
- Msvm_SyntheticEthernetPort.StatusInfo
- Msvm_SyntheticEthernetPort.LastErrorCode
- Msvm_SyntheticEthernetPort.ErrorDescription
- Msvm_SyntheticEthernetPort.ErrorCleared
- Msvm_SyntheticEthernetPort.OtherIdentifyingInfo
- Msvm_SyntheticEthernetPort.PowerOnHours
- Msvm_SyntheticEthernetPort.TotalPowerOnHours
- Msvm_SyntheticEthernetPort.IdentifyingDescriptions
- Msvm_SyntheticEthernetPort.AdditionalAvailability
- Msvm_SyntheticEthernetPort.MaxQuiesceTime
- Msvm_SyntheticEthernetPort.Speed
- Msvm_SyntheticEthernetPort.MaxSpeed
- Msvm_SyntheticEthernetPort.RequestedSpeed
- Msvm_SyntheticEthernetPort.UsageRestriction
- Msvm_SyntheticEthernetPort.PortType
- Msvm_SyntheticEthernetPort.OtherPortType
- Msvm_SyntheticEthernetPort.OtherNetworkPortType
- Msvm_SyntheticEthernetPort.PortNumber
- Msvm_SyntheticEthernetPort.LinkTechnology
- Msvm_SyntheticEthernetPort.OtherLinkTechnology
- Msvm_SyntheticEthernetPort.PermanentAddress
- Msvm_SyntheticEthernetPort.NetworkAddresses
- Msvm_SyntheticEthernetPort.FullDuplex
- Msvm_SyntheticEthernetPort.AutoSense
- Msvm_SyntheticEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_SyntheticEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_SyntheticEthernetPort.MaxDataSize
- Msvm_SyntheticEthernetPort.Capabilities
- Msvm_SyntheticEthernetPort.CapabilityDescriptions
- Msvm_SyntheticEthernetPort.EnabledCapabilities
- Msvm_SyntheticEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c8e2a8c2207e410878a4f5c498ea71a1ce67cd8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827767"
---
# <a name="msvm_syntheticethernetport-class"></a><span data-ttu-id="55cab-103">\_Classe Msvm SyntheticEthernetPort</span><span class="sxs-lookup"><span data-stu-id="55cab-103">Msvm\_SyntheticEthernetPort class</span></span>

<span data-ttu-id="55cab-104">Representa um adaptador Ethernet sintético.</span><span class="sxs-lookup"><span data-stu-id="55cab-104">Represents a synthetic Ethernet adapter.</span></span> <span data-ttu-id="55cab-105">Esse adaptador é o adaptador de rede preferencial devido ao seu desempenho e porque as alterações podem entrar em vigor imediatamente, enquanto estão em uso (capacidade de configurabilidade a quente).</span><span class="sxs-lookup"><span data-stu-id="55cab-105">This adapter is the preferred network adapter because of its performance and because changes to it can take effect right away, while it is in use (hot configurability).</span></span>

<span data-ttu-id="55cab-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="55cab-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="55cab-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55cab-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
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
  uint16   AdditionalAvailability[] = 6;
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
};
```

## <a name="members"></a><span data-ttu-id="55cab-108">Membros</span><span class="sxs-lookup"><span data-stu-id="55cab-108">Members</span></span>

<span data-ttu-id="55cab-109">A classe **Msvm \_ SyntheticEthernetPort** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="55cab-109">The **Msvm\_SyntheticEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="55cab-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="55cab-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="55cab-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="55cab-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="55cab-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="55cab-112">Methods</span></span>

<span data-ttu-id="55cab-113">A classe **Msvm \_ SyntheticEthernetPort** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="55cab-113">The **Msvm\_SyntheticEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="55cab-114">Método</span><span class="sxs-lookup"><span data-stu-id="55cab-114">Method</span></span>                                                                      | <span data-ttu-id="55cab-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="55cab-115">Description</span></span>                              |
|:----------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="55cab-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="55cab-116">**EnableDevice**</span></span>                                                            | <span data-ttu-id="55cab-117">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="55cab-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="55cab-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="55cab-118">**OnlineDevice**</span></span>                                                            | <span data-ttu-id="55cab-119">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="55cab-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="55cab-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="55cab-120">**QuiesceDevice**</span></span>                                                           | <span data-ttu-id="55cab-121">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="55cab-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="55cab-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="55cab-122">**RequestStateChange**</span></span>](msvm-syntheticethernetport-requeststatechange.md) | <span data-ttu-id="55cab-123">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="55cab-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="55cab-124">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="55cab-124">**Reset**</span></span>](msvm-syntheticethernetport-reset.md)                           | <span data-ttu-id="55cab-125">Redefine o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="55cab-125">Resets the device.</span></span><br/>            |
| <span data-ttu-id="55cab-126">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="55cab-126">**RestoreProperties**</span></span>                                                       | <span data-ttu-id="55cab-127">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="55cab-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="55cab-128">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="55cab-128">**SaveProperties**</span></span>                                                          | <span data-ttu-id="55cab-129">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="55cab-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="55cab-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="55cab-130">**SetPowerState**</span></span>                                                           | <span data-ttu-id="55cab-131">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="55cab-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="55cab-132">Propriedades</span><span class="sxs-lookup"><span data-stu-id="55cab-132">Properties</span></span>

<span data-ttu-id="55cab-133">A classe **Msvm \_ SyntheticEthernetPort** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="55cab-133">The **Msvm\_SyntheticEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="55cab-134">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="55cab-134">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-135">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="55cab-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cab-137">Qualificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="55cab-137">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="55cab-138">A unidade de transmissão máxima (MTU) do negociada ou ativa, que pode ter suporte.</span><span class="sxs-lookup"><span data-stu-id="55cab-138">The active or negotiated maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="55cab-139">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="55cab-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="55cab-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-141">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55cab-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="55cab-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-143">Disponibilidade e status adicionais do dispositivo, além do especificado na propriedade de **disponibilidade** .</span><span class="sxs-lookup"><span data-stu-id="55cab-143">Additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="55cab-144">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como 6 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="55cab-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-145">**Autodetecção**</span><span class="sxs-lookup"><span data-stu-id="55cab-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-146">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="55cab-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-148">Indica se a porta de rede é capaz de determinar automaticamente a velocidade ou outras características de comunicação da mídia de rede anexada.</span><span class="sxs-lookup"><span data-stu-id="55cab-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="55cab-149">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="55cab-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-150">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="55cab-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-151">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55cab-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-153">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="55cab-153">The primary availability and status of the device.</span></span> <span data-ttu-id="55cab-154">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="55cab-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="55cab-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-156">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55cab-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="55cab-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-158">Indica os valores possíveis para o parâmetro *requestedstate* do método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="55cab-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="55cab-159">Os valores listados serão um subconjunto dos valores contidos na propriedade **RequestedStatesSupported** da instância associada do **CIM \_ EnabledLogicalElementCapabilities**, em que os valores selecionados são uma função do estado atual do [**\_ EnabledLogicalElement do CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="55cab-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="55cab-160">Essa propriedade pode ser não **nula** se uma implementação for capaz de anunciar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="55cab-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="55cab-161">Essa propriedade será **nula** se uma implementação não puder determinar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="55cab-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="55cab-162">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="55cab-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="55cab-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="55cab-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="55cab-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="55cab-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="55cab-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="55cab-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="55cab-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="55cab-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="55cab-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="55cab-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="55cab-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="55cab-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="55cab-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="55cab-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="55cab-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="55cab-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="55cab-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="55cab-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="55cab-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="55cab-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="55cab-173">)</span><span class="sxs-lookup"><span data-stu-id="55cab-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="55cab-174">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="55cab-174">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-175">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55cab-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="55cab-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-177">Os recursos da porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="55cab-177">The capabilities of the Ethernet port.</span></span> <span data-ttu-id="55cab-178">Por exemplo, o dispositivo pode dar suporte a AlertOnLan, WakeOnLan, balanceamento de carga ou FailOver.</span><span class="sxs-lookup"><span data-stu-id="55cab-178">For example, the device might support AlertOnLan, WakeOnLan, Load Balancing, or FailOver.</span></span> <span data-ttu-id="55cab-179">Se os recursos de failover ou balanceamento de carga estiverem listados, um reExtraCapacityGroup (failover) ou de carga (balanceamento de carga) também deverá ser definido para descrever completamente o recurso.</span><span class="sxs-lookup"><span data-stu-id="55cab-179">If failover or load balancing capabilities are listed, a SpareGroup (failover) or ExtraCapacityGroup (load balancing) should also be defined to completely describe the capability.</span></span> <span data-ttu-id="55cab-180">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="55cab-180">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="55cab-181">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="55cab-181">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-182">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55cab-182">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="55cab-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-184">Uma matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para qualquer um dos recursos de EthernetPort que são indicados na matriz de propriedades de **recursos** .</span><span class="sxs-lookup"><span data-stu-id="55cab-184">An array of free-form strings that provides more detailed explanations for any of the EthernetPort features that are indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="55cab-185">Observe que cada entrada dessa matriz está relacionada à entrada na matriz de propriedades de **recursos** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="55cab-185">Note, each entry of this array is related to the entry in the **Capabilities** property array that is located at the same index.</span></span> <span data-ttu-id="55cab-186">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="55cab-186">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="55cab-187">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="55cab-187">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-188">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55cab-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-190">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="55cab-190">A short description of the object.</span></span> <span data-ttu-id="55cab-191">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="55cab-191">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-192">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="55cab-192">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-193">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55cab-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-195">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="55cab-195">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="55cab-196">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="55cab-196">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="55cab-197">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="55cab-197">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-198">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="55cab-198">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-199">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55cab-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-201">O nome da classe ou da subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="55cab-201">The name of the class or the subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="55cab-202">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="55cab-202">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-203">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="55cab-203">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-204">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55cab-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-206">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="55cab-206">A description of the object.</span></span> <span data-ttu-id="55cab-207">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="55cab-207">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-208">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="55cab-208">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-209">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55cab-209">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-210">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-211">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="55cab-211">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="55cab-212">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="55cab-212">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="55cab-213">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="55cab-213">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-214">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="55cab-214">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-215">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55cab-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-216">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-217">Um endereço ou outras informações de identificação usadas para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="55cab-217">An address or other identifying information used to uniquely name the logical device.</span></span> <span data-ttu-id="55cab-218">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="55cab-218">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-219">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="55cab-219">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-220">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55cab-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-221">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-222">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="55cab-222">A display name for the object.</span></span> <span data-ttu-id="55cab-223">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="55cab-223">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-224">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="55cab-224">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-225">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55cab-225">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="55cab-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-227">Os recursos que estão habilitados na lista de todos os com suporte, que são definidos na matriz de propriedades **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="55cab-227">The capabilities that are enabled from the list of all supported ones, which are defined in the **Capabilities** property array.</span></span> <span data-ttu-id="55cab-228">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="55cab-228">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="55cab-229">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="55cab-229">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-230">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55cab-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-232">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="55cab-232">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="55cab-233">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="55cab-233">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-234">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="55cab-234">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-235">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55cab-235">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-236">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-237">Os Estados habilitado e desabilitado deste elemento.</span><span class="sxs-lookup"><span data-stu-id="55cab-237">The enabled and disabled states of this element.</span></span> <span data-ttu-id="55cab-238">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="55cab-238">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-239">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="55cab-239">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-240">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="55cab-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-242">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="55cab-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="55cab-243">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="55cab-243">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-244">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55cab-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-245">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-246">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="55cab-246">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="55cab-247">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="55cab-247">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-248">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="55cab-248">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-249">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-250">Indica se a porta está operando no modo full duplex.</span><span class="sxs-lookup"><span data-stu-id="55cab-250">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="55cab-251">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="55cab-251">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-252">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="55cab-252">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-253">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55cab-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-254">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-255">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="55cab-255">The current health of the element.</span></span> <span data-ttu-id="55cab-256">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="55cab-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-257">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="55cab-257">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-258">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55cab-258">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="55cab-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-260">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="55cab-260">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="55cab-261">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="55cab-261">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="55cab-262">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="55cab-262">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-263">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="55cab-263">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-264">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-265">A data em que a porta Ethernet foi adicionada à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="55cab-265">The date the Ethernet port was added to the virtual machine.</span></span> <span data-ttu-id="55cab-266">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="55cab-266">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-267">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="55cab-267">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-268">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55cab-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-269">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cab-270">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="55cab-270">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="55cab-271">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="55cab-271">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="55cab-272">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="55cab-272">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-273">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="55cab-273">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-274">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="55cab-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-275">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-276">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="55cab-276">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="55cab-277">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="55cab-277">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-278">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55cab-278">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-280">Uma enumeração dos tipos de links.</span><span class="sxs-lookup"><span data-stu-id="55cab-280">An enumeration of the types of links.</span></span> <span data-ttu-id="55cab-281">Quando definido como 1 (outro), a propriedade relacionada **OtherLinkTechnology** contém uma descrição de cadeia de caracteres do tipo de link.</span><span class="sxs-lookup"><span data-stu-id="55cab-281">When set to 1 (Other), the related property **OtherLinkTechnology** contains a string description of the type of link.</span></span> <span data-ttu-id="55cab-282">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="55cab-282">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="55cab-283"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="55cab-283"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="55cab-284">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="55cab-284">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-285">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="55cab-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-287">O tamanho máximo do campo de informações (não MAC) que será recebido ou transmitido.</span><span class="sxs-lookup"><span data-stu-id="55cab-287">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="55cab-288">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="55cab-288">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-289">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="55cab-289">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-290">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="55cab-290">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-292">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="55cab-292">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="55cab-293">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="55cab-293">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-294">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="55cab-294">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cab-296">Qualificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="55cab-296">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="55cab-297">A largura de banda máxima da porta em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="55cab-297">The maximum bandwidth of the port in bits per second.</span></span> <span data-ttu-id="55cab-298">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="55cab-298">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-299">**Nome**</span><span class="sxs-lookup"><span data-stu-id="55cab-299">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-300">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55cab-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-301">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-302">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="55cab-302">A display name for the object.</span></span> <span data-ttu-id="55cab-303">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="55cab-303">This property is inherited from [**CIM\_ManagedSystemElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-304">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="55cab-304">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-305">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55cab-305">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="55cab-306">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-307">Endereços MAC Ethernet/802.3 formatados como doze dígitos hexadecimais (por exemplo, "010203040506"), com cada par representando um dos seis octetos do endereço MAC na ordem de bits canônica (o bit de endereço de grupo é encontrado no bit de ordem inferior do primeiro caractere da cadeia de caracteres).</span><span class="sxs-lookup"><span data-stu-id="55cab-307">Ethernet/802.3 MAC addresses formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (the Group address bit is found in the low order bit of the first character of the string).</span></span> <span data-ttu-id="55cab-308">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)e não é usada.</span><span class="sxs-lookup"><span data-stu-id="55cab-308">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="55cab-309">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="55cab-309">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-310">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55cab-310">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-311">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-312">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="55cab-312">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="55cab-313">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="55cab-313">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="55cab-314">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="55cab-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-315">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="55cab-315">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-316">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55cab-316">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="55cab-317">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-318">O status atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="55cab-318">The current status of the element.</span></span> <span data-ttu-id="55cab-319">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="55cab-319">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-320">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="55cab-320">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-321">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55cab-321">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="55cab-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-323">Uma matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para qualquer um dos recursos habilitados que são especificados como "outros".</span><span class="sxs-lookup"><span data-stu-id="55cab-323">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as "Other".</span></span> <span data-ttu-id="55cab-324">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="55cab-324">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="55cab-325">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="55cab-325">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-326">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55cab-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-328">O estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="55cab-328">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="55cab-329">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="55cab-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-330">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="55cab-330">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-331">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55cab-331">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="55cab-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-333">Todos os dados, além das informações de ID do dispositivo, que podem ser usados para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="55cab-333">Any data, in addition to device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="55cab-334">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="55cab-334">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="55cab-335">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="55cab-335">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-336">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55cab-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-338">Um valor de cadeia de caracteres que descreve **LinkTechnology** quando é definido como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="55cab-338">A string value that describes **LinkTechnology** when it is set to 1 (Other).</span></span> <span data-ttu-id="55cab-339">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="55cab-339">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-340">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="55cab-340">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-341">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55cab-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-342">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-343">Essa propriedade é herdada de [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="55cab-343">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) and is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="55cab-344">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="55cab-344">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-345">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55cab-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-346">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-347">O tipo de módulo, quando **PortType** é definido como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="55cab-347">The type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="55cab-348">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="55cab-348">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-349">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="55cab-349">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-350">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55cab-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-351">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-352">O endereço de rede embutido na porta.</span><span class="sxs-lookup"><span data-stu-id="55cab-352">The network address that is hardcoded into the port.</span></span> <span data-ttu-id="55cab-353">Esse endereço codificado pode ser alterado usando uma atualização de firmware ou uma configuração de software.</span><span class="sxs-lookup"><span data-stu-id="55cab-353">This hardcoded address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="55cab-354">Quando essa alteração é feita, o campo deve ser atualizado ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="55cab-354">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="55cab-355">A propriedade **PermanentAddress** deverá ser deixada em branco se não existir nenhum endereço codificado para o adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="55cab-355">The **PermanentAddress** property should be left blank if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="55cab-356">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="55cab-356">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-357">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="55cab-357">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-358">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55cab-358">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-360">As portas de rede geralmente são numeradas em relação a um módulo lógico ou um elemento de rede.</span><span class="sxs-lookup"><span data-stu-id="55cab-360">Network ports are often numbered relative to either a logical module or a network element.</span></span> <span data-ttu-id="55cab-361">Esse valor é 1 para NICs emuladas, 0 para todos os outros.</span><span class="sxs-lookup"><span data-stu-id="55cab-361">This value is 1 for emulated NICs, 0 for all others.</span></span> <span data-ttu-id="55cab-362">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="55cab-362">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-363">**PortType**</span><span class="sxs-lookup"><span data-stu-id="55cab-363">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-364">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55cab-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-365">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-366">O modo específico que está habilitado no momento para a porta.</span><span class="sxs-lookup"><span data-stu-id="55cab-366">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="55cab-367">Quando definido como 1 (outro), a propriedade relacionada **OtherPortType** contém uma descrição de cadeia de caracteres do tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="55cab-367">When set to 1 (Other), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="55cab-368">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="55cab-368">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-369">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="55cab-369">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-370">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55cab-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="55cab-371">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-372">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="55cab-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="55cab-373">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="55cab-373">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-374">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="55cab-374">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-376">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="55cab-376">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="55cab-377">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="55cab-377">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-378">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="55cab-378">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-379">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-380">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="55cab-380">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="55cab-381">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="55cab-381">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-382">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55cab-382">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-383">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-384">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="55cab-384">Provides high level status information.</span></span> <span data-ttu-id="55cab-385">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer informações de status de integridade detalhadas e de alto nível para o elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="55cab-385">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="55cab-386">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="55cab-386">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="55cab-387">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="55cab-387">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-388">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="55cab-388">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-389">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="55cab-389">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-390">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cab-391">Qualificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="55cab-391">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="55cab-392">A largura de banda solicitada da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="55cab-392">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="55cab-393">A largura de banda real é relatada na propriedade **Speed** .</span><span class="sxs-lookup"><span data-stu-id="55cab-393">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="55cab-394">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="55cab-394">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-395">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="55cab-395">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-396">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55cab-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-397">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-398">O último estado solicitado ou desejado para o serviço de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="55cab-398">The last requested or desired state for the management service.</span></span> <span data-ttu-id="55cab-399">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="55cab-399">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-400">**Velocidade**</span><span class="sxs-lookup"><span data-stu-id="55cab-400">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-401">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="55cab-401">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-402">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cab-403">Qualificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="55cab-403">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="55cab-404">A largura de banda atual da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="55cab-404">The current bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="55cab-405">Para portas que variam de largura de banda ou para aquelas em que não é possível fazer nenhuma estimativa precisa, essa propriedade deve conter a largura de banda nominal.</span><span class="sxs-lookup"><span data-stu-id="55cab-405">For ports that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span> <span data-ttu-id="55cab-406">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="55cab-406">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-407">**Status**</span><span class="sxs-lookup"><span data-stu-id="55cab-407">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-408">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55cab-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-409">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-410">O status atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="55cab-410">The current status of the element.</span></span> <span data-ttu-id="55cab-411">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="55cab-411">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-412">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="55cab-412">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-413">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55cab-413">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="55cab-414">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-415">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="55cab-415">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="55cab-416">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="55cab-416">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-417">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="55cab-417">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-418">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55cab-418">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-419">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-420">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="55cab-420">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="55cab-421">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="55cab-421">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-422">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="55cab-422">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-423">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cab-424">Qualificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="55cab-424">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="55cab-425">A MTU (unidade máxima de transmissão) que pode ter suporte.</span><span class="sxs-lookup"><span data-stu-id="55cab-425">The maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="55cab-426">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="55cab-426">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-427">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="55cab-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-428">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55cab-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-429">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-430">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="55cab-430">The creation class name of the scoping system.</span></span> <span data-ttu-id="55cab-431">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="55cab-431">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-432">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="55cab-432">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-433">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55cab-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-434">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-435">O nome NetBIOS do sistema de computador de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="55cab-435">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="55cab-436">Essa propriedade conterá a ID da máquina virtual no formato **GUID** .</span><span class="sxs-lookup"><span data-stu-id="55cab-436">This property will contain the virtual machine ID in **GUID** form.</span></span> <span data-ttu-id="55cab-437">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="55cab-437">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-438">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="55cab-438">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-439">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="55cab-439">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-440">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-441">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="55cab-441">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="55cab-442">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="55cab-442">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-443">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="55cab-443">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-444">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="55cab-444">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-445">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-446">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="55cab-446">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="55cab-447">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="55cab-447">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-448">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55cab-448">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-449">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-450">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="55cab-450">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="55cab-451">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="55cab-451">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="55cab-452">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="55cab-452">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cab-453">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55cab-453">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55cab-454">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55cab-454">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cab-455">Em algumas circunstâncias, uma porta lógica pode ser identificável como uma porta de front-end ou de back-end.</span><span class="sxs-lookup"><span data-stu-id="55cab-455">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="55cab-456">Se não houver nenhuma restrição sobre o uso da porta, o valor deverá ser definido como 4 (não restrito).</span><span class="sxs-lookup"><span data-stu-id="55cab-456">If there is no restriction on the use of the port, then the value should be set to 4 (Not Restricted).</span></span> <span data-ttu-id="55cab-457">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="55cab-457">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55cab-458">Comentários</span><span class="sxs-lookup"><span data-stu-id="55cab-458">Remarks</span></span>

<span data-ttu-id="55cab-459">O acesso à classe **Msvm \_ SyntheticEthernetPort** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="55cab-459">Access to the **Msvm\_SyntheticEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="55cab-460">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="55cab-460">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="55cab-461">Exemplos</span><span class="sxs-lookup"><span data-stu-id="55cab-461">Examples</span></span>

<span data-ttu-id="55cab-462">Consulte [consultando objetos de rede](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="55cab-462">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55cab-463">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55cab-463">Requirements</span></span>



| <span data-ttu-id="55cab-464">Requisito</span><span class="sxs-lookup"><span data-stu-id="55cab-464">Requirement</span></span> | <span data-ttu-id="55cab-465">Valor</span><span class="sxs-lookup"><span data-stu-id="55cab-465">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55cab-466">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55cab-466">Minimum supported client</span></span><br/> | <span data-ttu-id="55cab-467">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="55cab-467">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="55cab-468">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55cab-468">Minimum supported server</span></span><br/> | <span data-ttu-id="55cab-469">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="55cab-469">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="55cab-470">Namespace</span><span class="sxs-lookup"><span data-stu-id="55cab-470">Namespace</span></span><br/>                | <span data-ttu-id="55cab-471">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="55cab-471">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="55cab-472">MOF</span><span class="sxs-lookup"><span data-stu-id="55cab-472">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55cab-473"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55cab-473"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="55cab-474">DLL</span><span class="sxs-lookup"><span data-stu-id="55cab-474">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55cab-475"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="55cab-475"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="55cab-476">Confira também</span><span class="sxs-lookup"><span data-stu-id="55cab-476">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55cab-477">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="55cab-477">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="55cab-478">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="55cab-478">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

