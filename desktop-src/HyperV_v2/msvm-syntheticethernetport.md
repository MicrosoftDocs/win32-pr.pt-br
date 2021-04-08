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
# <a name="msvm_syntheticethernetport-class"></a><span data-ttu-id="ea136-103">\_Classe Msvm SyntheticEthernetPort</span><span class="sxs-lookup"><span data-stu-id="ea136-103">Msvm\_SyntheticEthernetPort class</span></span>

<span data-ttu-id="ea136-104">Representa um adaptador Ethernet sintético.</span><span class="sxs-lookup"><span data-stu-id="ea136-104">Represents a synthetic Ethernet adapter.</span></span> <span data-ttu-id="ea136-105">Esse adaptador é o adaptador de rede preferencial devido ao seu desempenho e porque as alterações podem entrar em vigor imediatamente, enquanto estão em uso (capacidade de configurabilidade a quente).</span><span class="sxs-lookup"><span data-stu-id="ea136-105">This adapter is the preferred network adapter because of its performance and because changes to it can take effect right away, while it is in use (hot configurability).</span></span>

<span data-ttu-id="ea136-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ea136-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea136-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea136-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="ea136-108">Membros</span><span class="sxs-lookup"><span data-stu-id="ea136-108">Members</span></span>

<span data-ttu-id="ea136-109">A classe **Msvm \_ SyntheticEthernetPort** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ea136-109">The **Msvm\_SyntheticEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="ea136-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="ea136-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="ea136-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ea136-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ea136-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="ea136-112">Methods</span></span>

<span data-ttu-id="ea136-113">A classe **Msvm \_ SyntheticEthernetPort** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ea136-113">The **Msvm\_SyntheticEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="ea136-114">Método</span><span class="sxs-lookup"><span data-stu-id="ea136-114">Method</span></span>                                                                      | <span data-ttu-id="ea136-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="ea136-115">Description</span></span>                              |
|:----------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="ea136-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="ea136-116">**EnableDevice**</span></span>                                                            | <span data-ttu-id="ea136-117">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="ea136-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="ea136-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="ea136-118">**OnlineDevice**</span></span>                                                            | <span data-ttu-id="ea136-119">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="ea136-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="ea136-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="ea136-120">**QuiesceDevice**</span></span>                                                           | <span data-ttu-id="ea136-121">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="ea136-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="ea136-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="ea136-122">**RequestStateChange**</span></span>](msvm-syntheticethernetport-requeststatechange.md) | <span data-ttu-id="ea136-123">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="ea136-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="ea136-124">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="ea136-124">**Reset**</span></span>](msvm-syntheticethernetport-reset.md)                           | <span data-ttu-id="ea136-125">Redefine o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea136-125">Resets the device.</span></span><br/>            |
| <span data-ttu-id="ea136-126">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="ea136-126">**RestoreProperties**</span></span>                                                       | <span data-ttu-id="ea136-127">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="ea136-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="ea136-128">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="ea136-128">**SaveProperties**</span></span>                                                          | <span data-ttu-id="ea136-129">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="ea136-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="ea136-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="ea136-130">**SetPowerState**</span></span>                                                           | <span data-ttu-id="ea136-131">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="ea136-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ea136-132">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ea136-132">Properties</span></span>

<span data-ttu-id="ea136-133">A classe **Msvm \_ SyntheticEthernetPort** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ea136-133">The **Msvm\_SyntheticEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ea136-134">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="ea136-134">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-135">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ea136-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea136-137">Qualificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="ea136-137">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ea136-138">A unidade de transmissão máxima (MTU) do negociada ou ativa, que pode ter suporte.</span><span class="sxs-lookup"><span data-stu-id="ea136-138">The active or negotiated maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="ea136-139">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ea136-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="ea136-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-141">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea136-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ea136-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-143">Disponibilidade e status adicionais do dispositivo, além do especificado na propriedade de **disponibilidade** .</span><span class="sxs-lookup"><span data-stu-id="ea136-143">Additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="ea136-144">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como 6 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="ea136-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-145">**Autodetecção**</span><span class="sxs-lookup"><span data-stu-id="ea136-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-146">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ea136-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-148">Indica se a porta de rede é capaz de determinar automaticamente a velocidade ou outras características de comunicação da mídia de rede anexada.</span><span class="sxs-lookup"><span data-stu-id="ea136-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="ea136-149">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ea136-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-150">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="ea136-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-151">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea136-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-153">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea136-153">The primary availability and status of the device.</span></span> <span data-ttu-id="ea136-154">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="ea136-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="ea136-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-156">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea136-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ea136-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-158">Indica os valores possíveis para o parâmetro *requestedstate* do método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="ea136-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="ea136-159">Os valores listados serão um subconjunto dos valores contidos na propriedade **RequestedStatesSupported** da instância associada do **CIM \_ EnabledLogicalElementCapabilities**, em que os valores selecionados são uma função do estado atual do [**\_ EnabledLogicalElement do CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea136-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="ea136-160">Essa propriedade pode ser não **nula** se uma implementação for capaz de anunciar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="ea136-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="ea136-161">Essa propriedade será **nula** se uma implementação não puder determinar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="ea136-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="ea136-162">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea136-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="ea136-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="ea136-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ea136-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="ea136-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ea136-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="ea136-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ea136-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="ea136-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ea136-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="ea136-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="ea136-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="ea136-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="ea136-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="ea136-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="ea136-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="ea136-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="ea136-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="ea136-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="ea136-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="ea136-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="ea136-173">)</span><span class="sxs-lookup"><span data-stu-id="ea136-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ea136-174">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="ea136-174">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-175">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea136-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ea136-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-177">Os recursos da porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="ea136-177">The capabilities of the Ethernet port.</span></span> <span data-ttu-id="ea136-178">Por exemplo, o dispositivo pode dar suporte a AlertOnLan, WakeOnLan, balanceamento de carga ou FailOver.</span><span class="sxs-lookup"><span data-stu-id="ea136-178">For example, the device might support AlertOnLan, WakeOnLan, Load Balancing, or FailOver.</span></span> <span data-ttu-id="ea136-179">Se os recursos de failover ou balanceamento de carga estiverem listados, um reExtraCapacityGroup (failover) ou de carga (balanceamento de carga) também deverá ser definido para descrever completamente o recurso.</span><span class="sxs-lookup"><span data-stu-id="ea136-179">If failover or load balancing capabilities are listed, a SpareGroup (failover) or ExtraCapacityGroup (load balancing) should also be defined to completely describe the capability.</span></span> <span data-ttu-id="ea136-180">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="ea136-180">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea136-181">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ea136-181">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-182">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea136-182">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ea136-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-184">Uma matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para qualquer um dos recursos de EthernetPort que são indicados na matriz de propriedades de **recursos** .</span><span class="sxs-lookup"><span data-stu-id="ea136-184">An array of free-form strings that provides more detailed explanations for any of the EthernetPort features that are indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="ea136-185">Observe que cada entrada dessa matriz está relacionada à entrada na matriz de propriedades de **recursos** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="ea136-185">Note, each entry of this array is related to the entry in the **Capabilities** property array that is located at the same index.</span></span> <span data-ttu-id="ea136-186">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="ea136-186">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea136-187">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="ea136-187">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-188">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea136-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-190">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="ea136-190">A short description of the object.</span></span> <span data-ttu-id="ea136-191">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ea136-191">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-192">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="ea136-192">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-193">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea136-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-195">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="ea136-195">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="ea136-196">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="ea136-196">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ea136-197">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ea136-197">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-198">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ea136-198">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-199">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea136-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-201">O nome da classe ou da subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="ea136-201">The name of the class or the subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="ea136-202">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="ea136-202">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-203">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ea136-203">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-204">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea136-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-206">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="ea136-206">A description of the object.</span></span> <span data-ttu-id="ea136-207">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ea136-207">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-208">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="ea136-208">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-209">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea136-209">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-210">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-211">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="ea136-211">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="ea136-212">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="ea136-212">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ea136-213">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ea136-213">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-214">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="ea136-214">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-215">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea136-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-216">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-217">Um endereço ou outras informações de identificação usadas para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ea136-217">An address or other identifying information used to uniquely name the logical device.</span></span> <span data-ttu-id="ea136-218">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="ea136-218">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-219">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ea136-219">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-220">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea136-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-221">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-222">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="ea136-222">A display name for the object.</span></span> <span data-ttu-id="ea136-223">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ea136-223">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-224">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ea136-224">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-225">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea136-225">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ea136-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-227">Os recursos que estão habilitados na lista de todos os com suporte, que são definidos na matriz de propriedades **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="ea136-227">The capabilities that are enabled from the list of all supported ones, which are defined in the **Capabilities** property array.</span></span> <span data-ttu-id="ea136-228">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="ea136-228">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea136-229">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="ea136-229">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-230">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea136-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-232">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="ea136-232">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="ea136-233">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea136-233">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-234">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="ea136-234">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-235">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea136-235">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-236">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-237">Os Estados habilitado e desabilitado deste elemento.</span><span class="sxs-lookup"><span data-stu-id="ea136-237">The enabled and disabled states of this element.</span></span> <span data-ttu-id="ea136-238">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea136-238">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-239">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="ea136-239">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-240">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ea136-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-242">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="ea136-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea136-243">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="ea136-243">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-244">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea136-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-245">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-246">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="ea136-246">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea136-247">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="ea136-247">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-248">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ea136-248">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-249">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-250">Indica se a porta está operando no modo full duplex.</span><span class="sxs-lookup"><span data-stu-id="ea136-250">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="ea136-251">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ea136-251">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-252">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="ea136-252">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-253">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea136-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-254">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-255">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="ea136-255">The current health of the element.</span></span> <span data-ttu-id="ea136-256">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ea136-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-257">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ea136-257">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-258">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea136-258">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ea136-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-260">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="ea136-260">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="ea136-261">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="ea136-261">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea136-262">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ea136-262">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-263">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ea136-263">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-264">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-265">A data em que a porta Ethernet foi adicionada à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ea136-265">The date the Ethernet port was added to the virtual machine.</span></span> <span data-ttu-id="ea136-266">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ea136-266">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-267">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ea136-267">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-268">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea136-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-269">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea136-270">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="ea136-270">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ea136-271">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="ea136-271">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ea136-272">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ea136-272">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-273">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="ea136-273">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-274">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ea136-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-275">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-276">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="ea136-276">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea136-277">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="ea136-277">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-278">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea136-278">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-280">Uma enumeração dos tipos de links.</span><span class="sxs-lookup"><span data-stu-id="ea136-280">An enumeration of the types of links.</span></span> <span data-ttu-id="ea136-281">Quando definido como 1 (outro), a propriedade relacionada **OtherLinkTechnology** contém uma descrição de cadeia de caracteres do tipo de link.</span><span class="sxs-lookup"><span data-stu-id="ea136-281">When set to 1 (Other), the related property **OtherLinkTechnology** contains a string description of the type of link.</span></span> <span data-ttu-id="ea136-282">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ea136-282">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="ea136-283"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="ea136-283"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ea136-284">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="ea136-284">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-285">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ea136-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-287">O tamanho máximo do campo de informações (não MAC) que será recebido ou transmitido.</span><span class="sxs-lookup"><span data-stu-id="ea136-287">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="ea136-288">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="ea136-288">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-289">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="ea136-289">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-290">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ea136-290">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-292">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="ea136-292">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea136-293">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="ea136-293">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-294">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ea136-294">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea136-296">Qualificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="ea136-296">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="ea136-297">A largura de banda máxima da porta em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="ea136-297">The maximum bandwidth of the port in bits per second.</span></span> <span data-ttu-id="ea136-298">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea136-298">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-299">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ea136-299">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-300">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea136-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-301">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-302">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="ea136-302">A display name for the object.</span></span> <span data-ttu-id="ea136-303">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ea136-303">This property is inherited from [**CIM\_ManagedSystemElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-304">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="ea136-304">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-305">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea136-305">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ea136-306">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-307">Endereços MAC Ethernet/802.3 formatados como doze dígitos hexadecimais (por exemplo, "010203040506"), com cada par representando um dos seis octetos do endereço MAC na ordem de bits canônica (o bit de endereço de grupo é encontrado no bit de ordem inferior do primeiro caractere da cadeia de caracteres).</span><span class="sxs-lookup"><span data-stu-id="ea136-307">Ethernet/802.3 MAC addresses formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (the Group address bit is found in the low order bit of the first character of the string).</span></span> <span data-ttu-id="ea136-308">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)e não é usada.</span><span class="sxs-lookup"><span data-stu-id="ea136-308">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea136-309">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="ea136-309">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-310">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea136-310">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-311">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-312">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="ea136-312">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="ea136-313">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="ea136-313">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ea136-314">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ea136-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-315">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="ea136-315">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-316">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea136-316">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ea136-317">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-318">O status atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="ea136-318">The current status of the element.</span></span> <span data-ttu-id="ea136-319">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="ea136-319">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-320">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ea136-320">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-321">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea136-321">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ea136-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-323">Uma matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para qualquer um dos recursos habilitados que são especificados como "outros".</span><span class="sxs-lookup"><span data-stu-id="ea136-323">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as "Other".</span></span> <span data-ttu-id="ea136-324">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="ea136-324">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea136-325">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="ea136-325">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-326">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea136-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-328">O estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="ea136-328">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="ea136-329">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea136-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-330">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="ea136-330">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-331">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea136-331">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ea136-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-333">Todos os dados, além das informações de ID do dispositivo, que podem ser usados para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ea136-333">Any data, in addition to device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="ea136-334">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="ea136-334">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea136-335">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="ea136-335">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-336">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea136-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-338">Um valor de cadeia de caracteres que descreve **LinkTechnology** quando é definido como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="ea136-338">A string value that describes **LinkTechnology** when it is set to 1 (Other).</span></span> <span data-ttu-id="ea136-339">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ea136-339">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-340">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="ea136-340">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-341">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea136-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-342">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-343">Essa propriedade é herdada de [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ea136-343">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) and is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ea136-344">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="ea136-344">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-345">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea136-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-346">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-347">O tipo de módulo, quando **PortType** é definido como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="ea136-347">The type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="ea136-348">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea136-348">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-349">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="ea136-349">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-350">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea136-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-351">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-352">O endereço de rede embutido na porta.</span><span class="sxs-lookup"><span data-stu-id="ea136-352">The network address that is hardcoded into the port.</span></span> <span data-ttu-id="ea136-353">Esse endereço codificado pode ser alterado usando uma atualização de firmware ou uma configuração de software.</span><span class="sxs-lookup"><span data-stu-id="ea136-353">This hardcoded address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="ea136-354">Quando essa alteração é feita, o campo deve ser atualizado ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="ea136-354">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="ea136-355">A propriedade **PermanentAddress** deverá ser deixada em branco se não existir nenhum endereço codificado para o adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="ea136-355">The **PermanentAddress** property should be left blank if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="ea136-356">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ea136-356">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-357">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="ea136-357">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-358">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea136-358">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-360">As portas de rede geralmente são numeradas em relação a um módulo lógico ou um elemento de rede.</span><span class="sxs-lookup"><span data-stu-id="ea136-360">Network ports are often numbered relative to either a logical module or a network element.</span></span> <span data-ttu-id="ea136-361">Esse valor é 1 para NICs emuladas, 0 para todos os outros.</span><span class="sxs-lookup"><span data-stu-id="ea136-361">This value is 1 for emulated NICs, 0 for all others.</span></span> <span data-ttu-id="ea136-362">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ea136-362">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-363">**PortType**</span><span class="sxs-lookup"><span data-stu-id="ea136-363">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-364">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea136-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-365">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-366">O modo específico que está habilitado no momento para a porta.</span><span class="sxs-lookup"><span data-stu-id="ea136-366">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="ea136-367">Quando definido como 1 (outro), a propriedade relacionada **OtherPortType** contém uma descrição de cadeia de caracteres do tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="ea136-367">When set to 1 (Other), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="ea136-368">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="ea136-368">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-369">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ea136-369">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-370">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea136-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ea136-371">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-372">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="ea136-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea136-373">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="ea136-373">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-374">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ea136-374">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-376">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="ea136-376">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea136-377">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="ea136-377">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-378">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ea136-378">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-379">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-380">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="ea136-380">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea136-381">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="ea136-381">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-382">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea136-382">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-383">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-384">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="ea136-384">Provides high level status information.</span></span> <span data-ttu-id="ea136-385">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer informações de status de integridade detalhadas e de alto nível para o elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="ea136-385">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="ea136-386">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="ea136-386">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ea136-387">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ea136-387">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-388">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="ea136-388">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-389">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ea136-389">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-390">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea136-391">Qualificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="ea136-391">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="ea136-392">A largura de banda solicitada da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="ea136-392">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="ea136-393">A largura de banda real é relatada na propriedade **Speed** .</span><span class="sxs-lookup"><span data-stu-id="ea136-393">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="ea136-394">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea136-394">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-395">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="ea136-395">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-396">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea136-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-397">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-398">O último estado solicitado ou desejado para o serviço de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="ea136-398">The last requested or desired state for the management service.</span></span> <span data-ttu-id="ea136-399">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea136-399">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-400">**Velocidade**</span><span class="sxs-lookup"><span data-stu-id="ea136-400">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-401">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ea136-401">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-402">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea136-403">Qualificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="ea136-403">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="ea136-404">A largura de banda atual da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="ea136-404">The current bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="ea136-405">Para portas que variam de largura de banda ou para aquelas em que não é possível fazer nenhuma estimativa precisa, essa propriedade deve conter a largura de banda nominal.</span><span class="sxs-lookup"><span data-stu-id="ea136-405">For ports that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span> <span data-ttu-id="ea136-406">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ea136-406">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-407">**Status**</span><span class="sxs-lookup"><span data-stu-id="ea136-407">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-408">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea136-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-409">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-410">O status atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="ea136-410">The current status of the element.</span></span> <span data-ttu-id="ea136-411">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ea136-411">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-412">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ea136-412">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-413">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea136-413">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ea136-414">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-415">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="ea136-415">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="ea136-416">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ea136-416">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-417">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="ea136-417">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-418">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea136-418">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-419">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-420">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="ea136-420">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea136-421">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="ea136-421">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-422">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ea136-422">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-423">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea136-424">Qualificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="ea136-424">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ea136-425">A MTU (unidade máxima de transmissão) que pode ter suporte.</span><span class="sxs-lookup"><span data-stu-id="ea136-425">The maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="ea136-426">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ea136-426">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-427">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ea136-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-428">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea136-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-429">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-430">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="ea136-430">The creation class name of the scoping system.</span></span> <span data-ttu-id="ea136-431">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="ea136-431">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-432">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ea136-432">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-433">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea136-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-434">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-435">O nome NetBIOS do sistema de computador de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="ea136-435">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="ea136-436">Essa propriedade conterá a ID da máquina virtual no formato **GUID** .</span><span class="sxs-lookup"><span data-stu-id="ea136-436">This property will contain the virtual machine ID in **GUID** form.</span></span> <span data-ttu-id="ea136-437">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="ea136-437">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-438">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="ea136-438">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-439">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ea136-439">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-440">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-441">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="ea136-441">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="ea136-442">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea136-442">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-443">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="ea136-443">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-444">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ea136-444">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-445">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-446">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="ea136-446">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea136-447">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="ea136-447">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-448">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea136-448">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-449">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-450">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="ea136-450">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="ea136-451">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea136-451">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ea136-452">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="ea136-452">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea136-453">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea136-453">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea136-454">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea136-454">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea136-455">Em algumas circunstâncias, uma porta lógica pode ser identificável como uma porta de front-end ou de back-end.</span><span class="sxs-lookup"><span data-stu-id="ea136-455">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="ea136-456">Se não houver nenhuma restrição sobre o uso da porta, o valor deverá ser definido como 4 (não restrito).</span><span class="sxs-lookup"><span data-stu-id="ea136-456">If there is no restriction on the use of the port, then the value should be set to 4 (Not Restricted).</span></span> <span data-ttu-id="ea136-457">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea136-457">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ea136-458">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea136-458">Remarks</span></span>

<span data-ttu-id="ea136-459">O acesso à classe **Msvm \_ SyntheticEthernetPort** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="ea136-459">Access to the **Msvm\_SyntheticEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ea136-460">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ea136-460">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="ea136-461">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ea136-461">Examples</span></span>

<span data-ttu-id="ea136-462">Consulte [consultando objetos de rede](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ea136-462">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ea136-463">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea136-463">Requirements</span></span>



| <span data-ttu-id="ea136-464">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea136-464">Requirement</span></span> | <span data-ttu-id="ea136-465">Valor</span><span class="sxs-lookup"><span data-stu-id="ea136-465">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea136-466">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea136-466">Minimum supported client</span></span><br/> | <span data-ttu-id="ea136-467">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ea136-467">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ea136-468">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea136-468">Minimum supported server</span></span><br/> | <span data-ttu-id="ea136-469">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ea136-469">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ea136-470">Namespace</span><span class="sxs-lookup"><span data-stu-id="ea136-470">Namespace</span></span><br/>                | <span data-ttu-id="ea136-471">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="ea136-471">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ea136-472">MOF</span><span class="sxs-lookup"><span data-stu-id="ea136-472">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea136-473"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea136-473"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ea136-474">DLL</span><span class="sxs-lookup"><span data-stu-id="ea136-474">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea136-475"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ea136-475"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ea136-476">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea136-476">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea136-477">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="ea136-477">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="ea136-478">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="ea136-478">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

