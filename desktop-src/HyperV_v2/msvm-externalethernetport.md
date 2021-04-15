---
description: Representa uma porta Ethernet externa (adaptador de rede).
ms.assetid: 70901587-641D-46F5-8A35-FEA483D336DE
title: Classe Msvm_ExternalEthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ExternalEthernetPort
- Msvm_ExternalEthernetPort.SetPowerState
- Msvm_ExternalEthernetPort.EnableDevice
- Msvm_ExternalEthernetPort.OnlineDevice
- Msvm_ExternalEthernetPort.QuiesceDevice
- Msvm_ExternalEthernetPort.SaveProperties
- Msvm_ExternalEthernetPort.RestoreProperties
- Msvm_ExternalEthernetPort.InstanceID
- Msvm_ExternalEthernetPort.Caption
- Msvm_ExternalEthernetPort.Description
- Msvm_ExternalEthernetPort.ElementName
- Msvm_ExternalEthernetPort.InstallDate
- Msvm_ExternalEthernetPort.Name
- Msvm_ExternalEthernetPort.OperationalStatus
- Msvm_ExternalEthernetPort.StatusDescriptions
- Msvm_ExternalEthernetPort.Status
- Msvm_ExternalEthernetPort.HealthState
- Msvm_ExternalEthernetPort.CommunicationStatus
- Msvm_ExternalEthernetPort.DetailedStatus
- Msvm_ExternalEthernetPort.OperatingStatus
- Msvm_ExternalEthernetPort.PrimaryStatus
- Msvm_ExternalEthernetPort.EnabledState
- Msvm_ExternalEthernetPort.OtherEnabledState
- Msvm_ExternalEthernetPort.RequestedState
- Msvm_ExternalEthernetPort.EnabledDefault
- Msvm_ExternalEthernetPort.TimeOfLastStateChange
- Msvm_ExternalEthernetPort.AvailableRequestedStates
- Msvm_ExternalEthernetPort.TransitioningToState
- Msvm_ExternalEthernetPort.SystemCreationClassName
- Msvm_ExternalEthernetPort.SystemName
- Msvm_ExternalEthernetPort.CreationClassName
- Msvm_ExternalEthernetPort.DeviceID
- Msvm_ExternalEthernetPort.PowerManagementSupported
- Msvm_ExternalEthernetPort.PowerManagementCapabilities
- Msvm_ExternalEthernetPort.Availability
- Msvm_ExternalEthernetPort.StatusInfo
- Msvm_ExternalEthernetPort.LastErrorCode
- Msvm_ExternalEthernetPort.ErrorDescription
- Msvm_ExternalEthernetPort.ErrorCleared
- Msvm_ExternalEthernetPort.OtherIdentifyingInfo
- Msvm_ExternalEthernetPort.PowerOnHours
- Msvm_ExternalEthernetPort.TotalPowerOnHours
- Msvm_ExternalEthernetPort.IdentifyingDescriptions
- Msvm_ExternalEthernetPort.AdditionalAvailability
- Msvm_ExternalEthernetPort.MaxQuiesceTime
- Msvm_ExternalEthernetPort.Speed
- Msvm_ExternalEthernetPort.MaxSpeed
- Msvm_ExternalEthernetPort.RequestedSpeed
- Msvm_ExternalEthernetPort.UsageRestriction
- Msvm_ExternalEthernetPort.PortType
- Msvm_ExternalEthernetPort.OtherPortType
- Msvm_ExternalEthernetPort.OtherNetworkPortType
- Msvm_ExternalEthernetPort.PortNumber
- Msvm_ExternalEthernetPort.LinkTechnology
- Msvm_ExternalEthernetPort.OtherLinkTechnology
- Msvm_ExternalEthernetPort.PermanentAddress
- Msvm_ExternalEthernetPort.NetworkAddresses
- Msvm_ExternalEthernetPort.FullDuplex
- Msvm_ExternalEthernetPort.AutoSense
- Msvm_ExternalEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_ExternalEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_ExternalEthernetPort.MaxDataSize
- Msvm_ExternalEthernetPort.Capabilities
- Msvm_ExternalEthernetPort.CapabilityDescriptions
- Msvm_ExternalEthernetPort.EnabledCapabilities
- Msvm_ExternalEthernetPort.OtherEnabledCapabilities
- Msvm_ExternalEthernetPort.IsBound
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 507c2235c1fda5f43ba025172e276b30e2f0aa85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501922"
---
# <a name="msvm_externalethernetport-class"></a><span data-ttu-id="8cd8c-103">\_Classe Msvm ExternalEthernetPort</span><span class="sxs-lookup"><span data-stu-id="8cd8c-103">Msvm\_ExternalEthernetPort class</span></span>

<span data-ttu-id="8cd8c-104">Representa uma porta Ethernet externa (adaptador de rede).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-104">Represents an external Ethernet port (network adapter).</span></span> <span data-ttu-id="8cd8c-105">Esses tipos de portas Ethernet dão acesso às máquinas virtuais à rede externa.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-105">These types of Ethernet ports give virtual machines access to the external network.</span></span>

<span data-ttu-id="8cd8c-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cd8c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8cd8c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ExternalEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft External Ethernet Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
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
  string   CreationClassName = "Msvm_ExternalEthernetPort";
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
  string   AdditionalAvailability[];
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
  boolean  IsBound;
};
```

## <a name="members"></a><span data-ttu-id="8cd8c-108">Membros</span><span class="sxs-lookup"><span data-stu-id="8cd8c-108">Members</span></span>

<span data-ttu-id="8cd8c-109">A classe **Msvm \_ ExternalEthernetPort** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8cd8c-109">The **Msvm\_ExternalEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="8cd8c-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="8cd8c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="8cd8c-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8cd8c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8cd8c-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="8cd8c-112">Methods</span></span>

<span data-ttu-id="8cd8c-113">A classe **Msvm \_ ExternalEthernetPort** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-113">The **Msvm\_ExternalEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="8cd8c-114">Método</span><span class="sxs-lookup"><span data-stu-id="8cd8c-114">Method</span></span>                                                                     | <span data-ttu-id="8cd8c-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="8cd8c-115">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="8cd8c-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-116">**EnableDevice**</span></span>                                                           | <span data-ttu-id="8cd8c-117">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="8cd8c-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-118">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="8cd8c-119">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="8cd8c-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-120">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="8cd8c-121">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="8cd8c-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-122">**RequestStateChange**</span></span>](msvm-externalethernetport-requeststatechange.md) | <span data-ttu-id="8cd8c-123">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="8cd8c-124">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-124">**Reset**</span></span>](msvm-externalethernetport-reset.md)                           | <span data-ttu-id="8cd8c-125">Redefine o dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="8cd8c-126">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-126">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="8cd8c-127">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="8cd8c-128">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-128">**SaveProperties**</span></span>                                                         | <span data-ttu-id="8cd8c-129">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="8cd8c-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-130">**SetPowerState**</span></span>                                                          | <span data-ttu-id="8cd8c-131">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8cd8c-132">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8cd8c-132">Properties</span></span>

<span data-ttu-id="8cd8c-133">A classe **Msvm \_ ExternalEthernetPort** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-133">The **Msvm\_ExternalEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8cd8c-134">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-134">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-135">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-137">Qualificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="8cd8c-137">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-138">A unidade de transmissão máxima (MTU) do negociada ou ativa que pode ter suporte, em bytes.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-138">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="8cd8c-139">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-141">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-141">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-143">Qualquer disponibilidade e status adicionais do dispositivo, além do especificado na propriedade de **disponibilidade** .</span><span class="sxs-lookup"><span data-stu-id="8cd8c-143">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="8cd8c-144">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-145">**Autodetecção**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-146">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-148">Indica se a porta de rede é capaz de determinar automaticamente a velocidade ou outras características de comunicação da mídia de rede anexada.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="8cd8c-149">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-150">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-151">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-153">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-153">The primary availability and status of the device.</span></span> <span data-ttu-id="8cd8c-154">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-156">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-158">Indica os valores possíveis para o parâmetro *requestedstate* do método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="8cd8c-159">Os valores listados serão um subconjunto dos valores contidos na propriedade **RequestedStatesSupported** da instância associada do **CIM \_ EnabledLogicalElementCapabilities**, em que os valores selecionados são uma função do estado atual do [**\_ EnabledLogicalElement do CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="8cd8c-160">Essa propriedade pode ser não **nula** se uma implementação for capaz de anunciar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="8cd8c-161">Essa propriedade será **nula** se uma implementação não puder determinar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="8cd8c-162">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="8cd8c-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="8cd8c-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="8cd8c-173">)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8cd8c-174">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-174">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-175">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-177">Uma matriz que especifica os recursos da porta.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-177">An array that specifies the capabilities of the port.</span></span> <span data-ttu-id="8cd8c-178">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-178">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="8cd8c-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-180"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-180"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-181"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-181"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-182"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-182"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-183"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Failover** (4)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-183"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-184"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**Balanceamento de carga** (5)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-184"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8cd8c-185">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-185">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-186">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-188">Uma matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para os recursos de porta contidos na matriz **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="8cd8c-188">An array of free-form strings that provides more detailed explanations for the port features that are contained in the **Capabilities** array.</span></span> <span data-ttu-id="8cd8c-189">Cada entrada dessa matriz está relacionada à entrada correspondente na matriz de **recursos** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-189">Each entry of this array is related to the corresponding entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="8cd8c-190">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-190">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-191">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-191">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-194">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-194">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-195">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-195">A short description of the object.</span></span> <span data-ttu-id="8cd8c-196">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "porta Ethernet".</span><span class="sxs-lookup"><span data-stu-id="8cd8c-196">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-197">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-197">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-198">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-200">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-200">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="8cd8c-201">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-201">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8cd8c-202">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-202">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-203">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-203">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-204">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-206">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-206">The scoping system's creation class name.</span></span> <span data-ttu-id="8cd8c-207">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como "Msvm \_ ExternalEthernetPort".</span><span class="sxs-lookup"><span data-stu-id="8cd8c-207">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ExternalEthernetPort".</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-208">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-208">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-209">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-210">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-211">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="8cd8c-211">A description of the object.</span></span> <span data-ttu-id="8cd8c-212">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "porta de Ethernet externa da Microsoft".</span><span class="sxs-lookup"><span data-stu-id="8cd8c-212">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft External Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-213">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-213">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-214">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-216">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-216">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="8cd8c-217">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-217">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8cd8c-218">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-218">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-219">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-219">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-220">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-221">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-222">Um endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-222">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="8cd8c-223">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-223">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-224">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-224">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-225">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-227">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-227">A display name for the object.</span></span> <span data-ttu-id="8cd8c-228">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-228">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-229">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-229">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-230">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-230">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-232">Especifica quais recursos estão habilitados na lista de todos os recursos com suporte na matriz de **recursos** .</span><span class="sxs-lookup"><span data-stu-id="8cd8c-232">Specifies which capabilities are enabled from the list of all supported capabilities in the **Capabilities** array.</span></span> <span data-ttu-id="8cd8c-233">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-233">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="8cd8c-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-235"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-235"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-236"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-236"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-237"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-237"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-238"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Failover** (4)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-238"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-239"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**Balanceamento de carga** (5)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-239"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8cd8c-240">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-240">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-241">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-242">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-243">A configuração de inicialização ou padrão de um administrador para a propriedade **enabledstate** de um elemento.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-243">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="8cd8c-244">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-244">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-245">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-245">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-246">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-247">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-248">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-248">The enabled and disabled states of an element.</span></span> <span data-ttu-id="8cd8c-249">Ele também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-249">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="8cd8c-250">Por exemplo, desligar (4) e iniciar (10) são estados transitórios entre habilitado e desabilitado.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-250">For example, shutting down (4) and starting (10) are transient states between enabled and disabled.</span></span> <span data-ttu-id="8cd8c-251">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-251">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="8cd8c-252">Valor</span><span class="sxs-lookup"><span data-stu-id="8cd8c-252">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="8cd8c-253">Significado</span><span class="sxs-lookup"><span data-stu-id="8cd8c-253">Meaning</span></span>                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="8cd8c-254"><dt></dt> <dt>0</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="8cd8c-254"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 |                                                                                                                                                                                                             |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="8cd8c-255"><dt>**Outros**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8cd8c-255"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                             |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="8cd8c-256"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8cd8c-256"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="8cd8c-257">O elemento é ou pode estar executando comandos, processará qualquer comando na fila e enfileirará novas solicitações.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-257">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span><br/>                                                                                        |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="8cd8c-258"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8cd8c-258"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="8cd8c-259">O elemento não executará comandos e descartará as novas solicitações.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-259">The element will not execute commands and will drop any new requests.</span></span><br/>                                                                                                                            |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="8cd8c-260"><dt>**Desligando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="8cd8c-260"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="8cd8c-261">O elemento está no processo de ir para um estado desabilitado.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-261">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                      |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="8cd8c-262"><dt>**Não aplicável**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="8cd8c-262"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="8cd8c-263">O elemento não dá suporte a ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-263">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                          |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="8cd8c-264"><dt>**Habilitado, mas offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="8cd8c-264"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="8cd8c-265">O elemento pode estar concluindo comandos e removerá todas as novas solicitações.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-265">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                     |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="8cd8c-266"><dt>**No teste**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="8cd8c-266"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="8cd8c-267">O elemento está em um estado de teste.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-267">The element is in a test state.</span></span><br/>                                                                                                                                                                  |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="8cd8c-268"><dt>**Adiado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="8cd8c-268"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="8cd8c-269">O elemento pode estar concluindo comandos, mas colocará todas as novas solicitações na fila.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-269">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                    |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="8cd8c-270"><dt>**Desativar**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="8cd8c-270"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="8cd8c-271">O elemento está habilitado, mas em um modo restrito.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-271">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="8cd8c-272">O comportamento do elemento é semelhante ao estado habilitado, mas processa apenas um conjunto restrito de comandos.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-272">The behavior of the element is similar to the Enabled state, but it processes only a restricted set of commands.</span></span> <span data-ttu-id="8cd8c-273">Todas as outras solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-273">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="8cd8c-274"><dt>**Iniciando**</dt> em <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="8cd8c-274"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="8cd8c-275">O elemento está no processo de ir para um estado habilitado.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-275">The element is in the process of going to an Enabled state.</span></span> <span data-ttu-id="8cd8c-276">Novas solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-276">New requests are queued.</span></span><br/>                                                                                                             |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="8cd8c-277"><dt>**DMTF reservado**</dt> <dt>11 32767</dt></span><span class="sxs-lookup"><span data-stu-id="8cd8c-277"><dt>**DMTF Reserved**</dt> <dt>11 32767</dt></span></span> </dl>                  | <span data-ttu-id="8cd8c-278">Reservado.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-278">Reserved.</span></span><br/>                                                                                                                                                                                        |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="8cd8c-279"><dt>**Fornecedor reservado**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="8cd8c-279"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl>       | <span data-ttu-id="8cd8c-280">Reservado.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-280">Reserved.</span></span><br/>                                                                                                                                                                                        |



 

</dd> <dt>

<span data-ttu-id="8cd8c-281">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-281">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-282">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-283">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-284">Indica se o erro relatado em **LastErrorCode** agora está limpo.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-284">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="8cd8c-285">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-285">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-286">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-286">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-287">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-288">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-289">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-289">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="8cd8c-290">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-290">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-291">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-291">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-292">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-293">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-294">Indica se a porta está operando no modo full duplex.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-294">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="8cd8c-295">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-295">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-296">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-296">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-297">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-297">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-299">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-299">The current health of the element.</span></span> <span data-ttu-id="8cd8c-300">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-300">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="8cd8c-301">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-301">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="8cd8c-302">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-303">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-303">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-304">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-304">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-305">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-306">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz de propriedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="8cd8c-306">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="8cd8c-307">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-307">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-308">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-308">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-309">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-310">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-311">A data e a hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-311">The date and time when the object was installed.</span></span> <span data-ttu-id="8cd8c-312">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-312">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="8cd8c-313">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-313">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-314">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-314">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-315">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-317">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-317">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-318">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-318">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8cd8c-319">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-319">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-320">**IsBound**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-320">**IsBound**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-321">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-323">Se essa propriedade for **true**, essa porta Ethernet poderá ser conectada aos comutadores e, portanto, poderá fornecer conectividade a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-323">If this property is **True**, then this Ethernet port can be connected to the switches and thus can provide connectivity to a virtual machine.</span></span> <span data-ttu-id="8cd8c-324">Se essa propriedade for **false**, essa porta Ethernet não será usada pela arquitetura de rede da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-324">If this property is **False**, then this Ethernet port is not being used by the virtual machine networking architecture.</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-325">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-325">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-326">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-326">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-328">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-328">The last error code reported by the logical device.</span></span> <span data-ttu-id="8cd8c-329">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-329">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-330">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-330">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-331">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-333">Especifica o tipo de tecnologia de link para a porta.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-333">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="8cd8c-334">Quando definido como 1 (outro), a propriedade **OtherLinkTechnology** contém uma descrição de cadeia de caracteres do tipo de link.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-334">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="8cd8c-335">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-335">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="8cd8c-336"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-336"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-337"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-337"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-338"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-338"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-339"><span id="IB"></span><span id="ib"></span>**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-339"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-340"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-340"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-341"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-341"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-342"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-342"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-343"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token ring** (7)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-343"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-344"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-344"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-345"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infravermelho** (9)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-345"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-346"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-346"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-347"><span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>**LAN sem fio** (11)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-347"><span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>**Wireless LAN** (11)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8cd8c-348">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-348">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-349">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-349">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-350">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-351">O tamanho máximo do campo de informações (não MAC) que será recebido ou transmitido.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-351">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="8cd8c-352">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)e é sempre definida como 1500.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-352">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-353">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-353">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-354">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-354">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-355">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-356">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-356">This property has been deprecated.</span></span> <span data-ttu-id="8cd8c-357">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-357">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-358">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-358">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-359">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-359">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-360">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-361">Qualificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="8cd8c-361">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-362">A largura de banda máxima da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-362">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="8cd8c-363">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-363">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-364">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-364">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-365">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-366">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-367">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-367">The label by which the object is known.</span></span> <span data-ttu-id="8cd8c-368">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-368">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-369">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-369">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-370">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-370">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-371">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-372">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-372">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-373">Uma matriz de cadeias de caracteres que contêm os endereços MAC para a porta.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-373">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="8cd8c-374">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-374">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-375">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-375">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-376">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-377">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-378">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="8cd8c-378">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="8cd8c-379">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-379">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8cd8c-380">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-380">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-381">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-381">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-382">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-382">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-383">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-384">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-384">The current statuses of the object.</span></span> <span data-ttu-id="8cd8c-385">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-385">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-386">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-386">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-387">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-387">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-389">Uma matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para qualquer um dos recursos habilitados que são especificados como 1 (outro.) Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-389">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as 1 (Other.) This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-390">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-390">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-391">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-392">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-393">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-393">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="8cd8c-394">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-394">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="8cd8c-395">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-395">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-396">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-396">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-397">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-397">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-398">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-399">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-399">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="8cd8c-400">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-400">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-401">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-401">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-402">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-403">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-404">Um valor de cadeia de caracteres que descreve **LinkTechnology** quando é definido como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-404">A string value that describes **LinkTechnology** when it is set to 1 (Other).</span></span> <span data-ttu-id="8cd8c-405">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-405">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-406">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-406">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-407">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-408">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-409">O uso dessa propriedade é preterido no lugar da propriedade **PortType** .</span><span class="sxs-lookup"><span data-stu-id="8cd8c-409">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="8cd8c-410">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-410">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-411">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-411">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-412">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-413">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-414">O tipo de módulo, quando **PortType** é definido como 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="8cd8c-414">The type of module, when **PortType** is set to 1 ("Other").</span></span> <span data-ttu-id="8cd8c-415">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-415">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-416">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-416">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-417">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-418">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-419">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-419">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-420">O endereço de rede embutido em uma porta.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-420">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="8cd8c-421">Esse endereço codificado pode ser alterado usando uma atualização de firmware ou uma configuração de software.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-421">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="8cd8c-422">Quando essa alteração é feita, o campo deve ser atualizado ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-422">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="8cd8c-423">Essa propriedade deverá ser **nula** se não existir nenhum endereço codificado para o adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-423">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="8cd8c-424">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-424">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-425">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-425">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-426">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-426">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-427">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-427">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-428">O número da porta.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-428">The port number.</span></span> <span data-ttu-id="8cd8c-429">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-429">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-430">**PortType**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-430">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-431">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-431">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-432">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-433">O modo específico que está habilitado no momento para a porta.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-433">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="8cd8c-434">Quando definido como 1 ("other"), a propriedade relacionada **OtherPortType** contém uma descrição de cadeia de caracteres do tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-434">When set to 1 ("Other"), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="8cd8c-435">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-435">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="8cd8c-436"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-436"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-437"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-437"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-438"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>+ **/50 10BaseT de cobre** (50)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-438"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-439"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-439"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-440"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-440"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-441"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000baseT** (53)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-441"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-442"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-442"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-443"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-443"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-444"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-444"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-445"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**100 Fibre 100BASE-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-445"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-446"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-446"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-447"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-447"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-448"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-448"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-449"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000BASE-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-449"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-450"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-Sr** (105)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-450"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-451"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-451"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-452"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-452"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-453"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-453"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-454"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-454"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-455"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-455"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-456"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-ovo** (111)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-456"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-457"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (16000 65535)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-457"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (16000 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8cd8c-458">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-458">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-459">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-459">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-460">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-461">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-461">The power management capabilities of the device.</span></span> <span data-ttu-id="8cd8c-462">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-463">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-463">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-464">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-464">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-465">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-466">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-466">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="8cd8c-467">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-467">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-468">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-468">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-469">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-469">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-470">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-471">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-471">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="8cd8c-472">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-472">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-473">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-473">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-474">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-474">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-475">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-476">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-476">Provides high level status information.</span></span> <span data-ttu-id="8cd8c-477">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer informações de status de integridade detalhadas e de alto nível para o elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-477">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="8cd8c-478">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-478">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8cd8c-479">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-479">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-480">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-480">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-481">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-481">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-482">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-483">Qualificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="8cd8c-483">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-484">A largura de banda solicitada da porta em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-484">The requested bandwidth of the port in bits per second.</span></span> <span data-ttu-id="8cd8c-485">A largura de banda real é relatada na propriedade **Speed** .</span><span class="sxs-lookup"><span data-stu-id="8cd8c-485">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="8cd8c-486">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-486">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-487">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-487">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-488">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-488">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-489">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-490">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-490">The last requested or desired state for the element.</span></span> <span data-ttu-id="8cd8c-491">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 12 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-491">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-492">**Velocidade**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-492">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-493">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-493">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-494">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-495">Qualificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="8cd8c-495">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-496">A largura de banda da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-496">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="8cd8c-497">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-497">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-498">**Status**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-498">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-499">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-500">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-501">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-501">The current status of the object.</span></span> <span data-ttu-id="8cd8c-502">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-502">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8cd8c-503">PROBLEMAS</span><span class="sxs-lookup"><span data-stu-id="8cd8c-503">"OK"</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-504"><span id="OK"></span><span id="ok"></span>**Okey**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-504"><span id="OK"></span><span id="ok"></span>**OK**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-505"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ao**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-505"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-506"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-506"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-507"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Conhecidos**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-507"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-508"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Falha de Pred**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-508"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Pred Fail**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-509"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Comece**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-509"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-510"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Impedir**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-510"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-511"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Serviço**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-511"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-512"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Analisa**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-512"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-513"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**Não recuperar**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-513"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**NonRecover**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-514"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sem contato**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-514"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-515"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Com perda de comunicação**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-515"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Lost Comm**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8cd8c-516">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-516">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-517">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-517">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-518">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-519">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="8cd8c-519">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="8cd8c-520">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como "OK".</span><span class="sxs-lookup"><span data-stu-id="8cd8c-520">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-521">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-521">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-522">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-522">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-523">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-523">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-524">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-524">The current state of the logical device.</span></span> <span data-ttu-id="8cd8c-525">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-525">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-526">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-526">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-527">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-527">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-528">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-528">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-529">Qualificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="8cd8c-529">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-530">A MTU (unidade máxima de transmissão) que pode ter suporte, em bytes.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-530">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="8cd8c-531">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-531">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-532">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-532">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-533">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-533">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-534">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-534">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-535">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-535">The scoping system's creation class name.</span></span> <span data-ttu-id="8cd8c-536">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como "Msvm \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="8cd8c-536">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-537">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-537">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-538">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-539">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-539">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-540">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-540">The name of the scoping system.</span></span> <span data-ttu-id="8cd8c-541">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-541">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-542">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-542">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-543">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-543">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-544">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-544">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-545">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-545">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="8cd8c-546">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-546">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-547">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-547">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-548">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-548">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-549">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-549">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-550">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-550">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="8cd8c-551">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-551">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-552">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-552">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-553">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-553">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-554">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-554">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-555">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-555">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="8cd8c-556">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-556">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8cd8c-557">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-557">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd8c-558">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-558">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-559">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd8c-559">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd8c-560">Em algumas circunstâncias, uma porta lógica pode ser identificável como uma porta de front-end ou de back-end.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-560">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="8cd8c-561">Um exemplo dessa situação seria uma matriz de armazenamento que pode ter portas de back-end para se comunicar com unidades de disco e portas de front-end para se comunicar com os hosts.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-561">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="8cd8c-562">Se não houver nenhuma restrição sobre o uso da porta, o valor deverá ser definido como "não restrito".</span><span class="sxs-lookup"><span data-stu-id="8cd8c-562">If there is no restriction on the use of the port, then the value should be set to "Not restricted".</span></span> <span data-ttu-id="8cd8c-563">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-563">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="8cd8c-564"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-564"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-565"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Somente front-end** (2)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-565"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-566"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Somente back-end** (3)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-566"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8cd8c-567"><span id="Not_restricted"></span><span id="not_restricted"></span><span id="NOT_RESTRICTED"></span>**Não restrito** (4)</span><span class="sxs-lookup"><span data-stu-id="8cd8c-567"><span id="Not_restricted"></span><span id="not_restricted"></span><span id="NOT_RESTRICTED"></span>**Not restricted** (4)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8cd8c-568">Comentários</span><span class="sxs-lookup"><span data-stu-id="8cd8c-568">Remarks</span></span>

<span data-ttu-id="8cd8c-569">O acesso à classe **Msvm \_ ExternalEthernetPort** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-569">Access to the **Msvm\_ExternalEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="8cd8c-570">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-570">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="8cd8c-571">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8cd8c-571">Examples</span></span>

<span data-ttu-id="8cd8c-572">Consulte [consultando objetos de rede](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-572">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8cd8c-573">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cd8c-573">Requirements</span></span>



| <span data-ttu-id="8cd8c-574">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cd8c-574">Requirement</span></span> | <span data-ttu-id="8cd8c-575">Valor</span><span class="sxs-lookup"><span data-stu-id="8cd8c-575">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cd8c-576">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cd8c-576">Minimum supported client</span></span><br/> | <span data-ttu-id="8cd8c-577">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8cd8c-577">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8cd8c-578">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cd8c-578">Minimum supported server</span></span><br/> | <span data-ttu-id="8cd8c-579">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8cd8c-579">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8cd8c-580">Namespace</span><span class="sxs-lookup"><span data-stu-id="8cd8c-580">Namespace</span></span><br/>                | <span data-ttu-id="8cd8c-581">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="8cd8c-581">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8cd8c-582">MOF</span><span class="sxs-lookup"><span data-stu-id="8cd8c-582">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8cd8c-583"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8cd8c-583"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8cd8c-584">DLL</span><span class="sxs-lookup"><span data-stu-id="8cd8c-584">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cd8c-585"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8cd8c-585"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8cd8c-586">Confira também</span><span class="sxs-lookup"><span data-stu-id="8cd8c-586">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cd8c-587">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-587">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="8cd8c-588">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-588">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

