---
description: Representa um adaptador de rede Wi-Fi (802,11) físico que pode ser associado a um comutador virtual para fornecer conectividade de rede externa a máquinas virtuais.
ms.assetid: c6dae491-607c-4f17-aea9-162d910120c2
title: Classe Msvm_WiFiPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiPort
- Msvm_WiFiPort.RequestStateChange
- Msvm_WiFiPort.SetPowerState
- Msvm_WiFiPort.Reset
- Msvm_WiFiPort.EnableDevice
- Msvm_WiFiPort.OnlineDevice
- Msvm_WiFiPort.QuiesceDevice
- Msvm_WiFiPort.SaveProperties
- Msvm_WiFiPort.RestoreProperties
- Msvm_WiFiPort.InstanceID
- Msvm_WiFiPort.Caption
- Msvm_WiFiPort.Description
- Msvm_WiFiPort.ElementName
- Msvm_WiFiPort.InstallDate
- Msvm_WiFiPort.Name
- Msvm_WiFiPort.OperationalStatus
- Msvm_WiFiPort.StatusDescriptions
- Msvm_WiFiPort.Status
- Msvm_WiFiPort.HealthState
- Msvm_WiFiPort.CommunicationStatus
- Msvm_WiFiPort.DetailedStatus
- Msvm_WiFiPort.OperatingStatus
- Msvm_WiFiPort.PrimaryStatus
- Msvm_WiFiPort.EnabledState
- Msvm_WiFiPort.OtherEnabledState
- Msvm_WiFiPort.RequestedState
- Msvm_WiFiPort.EnabledDefault
- Msvm_WiFiPort.TimeOfLastStateChange
- Msvm_WiFiPort.AvailableRequestedStates
- Msvm_WiFiPort.TransitioningToState
- Msvm_WiFiPort.SystemCreationClassName
- Msvm_WiFiPort.SystemName
- Msvm_WiFiPort.CreationClassName
- Msvm_WiFiPort.DeviceID
- Msvm_WiFiPort.PowerManagementSupported
- Msvm_WiFiPort.PowerManagementCapabilities
- Msvm_WiFiPort.Availability
- Msvm_WiFiPort.StatusInfo
- Msvm_WiFiPort.LastErrorCode
- Msvm_WiFiPort.ErrorDescription
- Msvm_WiFiPort.ErrorCleared
- Msvm_WiFiPort.OtherIdentifyingInfo
- Msvm_WiFiPort.PowerOnHours
- Msvm_WiFiPort.TotalPowerOnHours
- Msvm_WiFiPort.IdentifyingDescriptions
- Msvm_WiFiPort.AdditionalAvailability
- Msvm_WiFiPort.MaxQuiesceTime
- Msvm_WiFiPort.Speed
- Msvm_WiFiPort.MaxSpeed
- Msvm_WiFiPort.RequestedSpeed
- Msvm_WiFiPort.UsageRestriction
- Msvm_WiFiPort.PortType
- Msvm_WiFiPort.OtherPortType
- Msvm_WiFiPort.OtherNetworkPortType
- Msvm_WiFiPort.PortNumber
- Msvm_WiFiPort.LinkTechnology
- Msvm_WiFiPort.OtherLinkTechnology
- Msvm_WiFiPort.PermanentAddress
- Msvm_WiFiPort.NetworkAddresses
- Msvm_WiFiPort.FullDuplex
- Msvm_WiFiPort.AutoSense
- Msvm_WiFiPort.SupportedMaximumTransmissionUnit
- Msvm_WiFiPort.ActiveMaximumTransmissionUnit
- Msvm_WiFiPort.IsBound
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47ec33236c55d281755b50449a8f33a56152a07a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922913"
---
# <a name="msvm_wifiport-class"></a><span data-ttu-id="e58d8-103">\_Classe Msvm WiFiPort</span><span class="sxs-lookup"><span data-stu-id="e58d8-103">Msvm\_WiFiPort class</span></span>

<span data-ttu-id="e58d8-104">Representa um adaptador de rede Wi-Fi (802,11) físico que pode ser associado a um comutador virtual para fornecer conectividade de rede externa a máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="e58d8-104">Represents a physical Wi-Fi (802.11) network adapter that can be bound to a virtual switch to provide external network connectivity to virtual machines.</span></span>

<span data-ttu-id="e58d8-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e58d8-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e58d8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e58d8-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiPort : CIM_WiFiPort
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
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
  boolean  IsBound;
};
```

## <a name="members"></a><span data-ttu-id="e58d8-107">Membros</span><span class="sxs-lookup"><span data-stu-id="e58d8-107">Members</span></span>

<span data-ttu-id="e58d8-108">A classe **Msvm \_ WiFiPort** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e58d8-108">The **Msvm\_WiFiPort** class has these types of members:</span></span>

-   [<span data-ttu-id="e58d8-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="e58d8-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="e58d8-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e58d8-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e58d8-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="e58d8-111">Methods</span></span>

<span data-ttu-id="e58d8-112">A classe **Msvm \_ WiFiPort** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e58d8-112">The **Msvm\_WiFiPort** class has these methods.</span></span>



| <span data-ttu-id="e58d8-113">Método</span><span class="sxs-lookup"><span data-stu-id="e58d8-113">Method</span></span>                 | <span data-ttu-id="e58d8-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="e58d8-114">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="e58d8-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="e58d8-115">**EnableDevice**</span></span>       | <span data-ttu-id="e58d8-116">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="e58d8-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e58d8-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="e58d8-117">**OnlineDevice**</span></span>       | <span data-ttu-id="e58d8-118">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="e58d8-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e58d8-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="e58d8-119">**QuiesceDevice**</span></span>      | <span data-ttu-id="e58d8-120">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="e58d8-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e58d8-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="e58d8-121">**RequestStateChange**</span></span> | <span data-ttu-id="e58d8-122">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="e58d8-122">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e58d8-123">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="e58d8-123">**Reset**</span></span>              | <span data-ttu-id="e58d8-124">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="e58d8-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e58d8-125">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="e58d8-125">**RestoreProperties**</span></span>  | <span data-ttu-id="e58d8-126">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="e58d8-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e58d8-127">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="e58d8-127">**SaveProperties**</span></span>     | <span data-ttu-id="e58d8-128">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="e58d8-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e58d8-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e58d8-129">**SetPowerState**</span></span>      | <span data-ttu-id="e58d8-130">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="e58d8-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e58d8-131">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e58d8-131">Properties</span></span>

<span data-ttu-id="e58d8-132">A classe **Msvm \_ WiFiPort** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e58d8-132">The **Msvm\_WiFiPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e58d8-133">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="e58d8-133">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-134">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e58d8-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-136">Qualificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="e58d8-136">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-137">A unidade de transmissão máxima (MTU) do negociada ou ativa que pode ter suporte, em bytes.</span><span class="sxs-lookup"><span data-stu-id="e58d8-137">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="e58d8-138">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="e58d8-138">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-139">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="e58d8-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-140">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e58d8-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-142">Qualquer disponibilidade e status adicionais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e58d8-142">Any additional availability and status of the device.</span></span> <span data-ttu-id="e58d8-143">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e58d8-143">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-144">**Autodetecção**</span><span class="sxs-lookup"><span data-stu-id="e58d8-144">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-145">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e58d8-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-147">Indica se a porta é capaz de determinar automaticamente a velocidade ou outras características de comunicação da mídia de rede anexada.</span><span class="sxs-lookup"><span data-stu-id="e58d8-147">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="e58d8-148">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="e58d8-148">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-149">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="e58d8-149">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-150">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e58d8-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-152">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e58d8-152">The primary availability and status of the device.</span></span> <span data-ttu-id="e58d8-153">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e58d8-153">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-154">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="e58d8-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-155">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e58d8-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-157">Indica os valores possíveis para o parâmetro *requestedstate* do método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="e58d8-157">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="e58d8-158">Os valores listados serão um subconjunto dos valores contidos na propriedade **RequestedStatesSupported** da instância associada do **CIM \_ EnabledLogicalElementCapabilities**, em que os valores selecionados são uma função do estado atual do [**\_ EnabledLogicalElement do CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e58d8-158">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="e58d8-159">Essa propriedade pode ser não **nula** se uma implementação for capaz de anunciar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="e58d8-159">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="e58d8-160">Essa propriedade será **nula** se uma implementação não puder determinar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="e58d8-160">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="e58d8-161">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e58d8-161">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="e58d8-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="e58d8-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="e58d8-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="e58d8-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="e58d8-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="e58d8-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="e58d8-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="e58d8-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="e58d8-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="e58d8-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="e58d8-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="e58d8-172">)</span><span class="sxs-lookup"><span data-stu-id="e58d8-172">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e58d8-173">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="e58d8-173">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e58d8-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-176">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="e58d8-176">A short description of the object.</span></span> <span data-ttu-id="e58d8-177">Essa propriedade é herdada da classe [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) .</span><span class="sxs-lookup"><span data-stu-id="e58d8-177">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class.</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-178">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="e58d8-178">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-179">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e58d8-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-181">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="e58d8-181">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="e58d8-182">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="e58d8-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e58d8-183">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e58d8-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-184">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e58d8-184">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-185">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e58d8-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-187">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="e58d8-187">The scoping system's creation class name.</span></span> <span data-ttu-id="e58d8-188">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e58d8-188">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-189">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e58d8-189">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-190">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e58d8-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-192">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="e58d8-192">A description of the object.</span></span> <span data-ttu-id="e58d8-193">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e58d8-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-194">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="e58d8-194">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-195">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e58d8-195">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-197">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="e58d8-197">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="e58d8-198">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="e58d8-198">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e58d8-199">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e58d8-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-200">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="e58d8-200">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-201">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e58d8-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-203">Um endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e58d8-203">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="e58d8-204">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e58d8-204">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-205">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e58d8-205">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-206">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e58d8-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-208">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="e58d8-208">A display name for the object.</span></span> <span data-ttu-id="e58d8-209">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e58d8-209">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-210">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="e58d8-210">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-211">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e58d8-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-213">A configuração de inicialização ou padrão de um administrador para a propriedade **enabledstate** de um elemento.</span><span class="sxs-lookup"><span data-stu-id="e58d8-213">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="e58d8-214">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e58d8-214">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-215">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="e58d8-215">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-216">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e58d8-216">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-218">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="e58d8-218">The enabled and disabled states of an element.</span></span> <span data-ttu-id="e58d8-219">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e58d8-219">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="e58d8-220">Valor</span><span class="sxs-lookup"><span data-stu-id="e58d8-220">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="e58d8-221">Significado</span><span class="sxs-lookup"><span data-stu-id="e58d8-221">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="e58d8-222"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e58d8-222"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="e58d8-223">O elemento está em execução.</span><span class="sxs-lookup"><span data-stu-id="e58d8-223">The element is running.</span></span><br/>    |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="e58d8-224"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e58d8-224"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="e58d8-225">O elemento está desativado.</span><span class="sxs-lookup"><span data-stu-id="e58d8-225">The element is turned off.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e58d8-226">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="e58d8-226">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-227">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e58d8-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-229">Indica se o erro relatado em **LastErrorCode** agora está limpo.</span><span class="sxs-lookup"><span data-stu-id="e58d8-229">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="e58d8-230">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e58d8-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-231">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e58d8-231">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-232">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e58d8-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-234">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="e58d8-234">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="e58d8-235">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e58d8-235">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-236">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="e58d8-236">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-237">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e58d8-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-239">Indica se a porta está operando no modo full duplex.</span><span class="sxs-lookup"><span data-stu-id="e58d8-239">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="e58d8-240">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="e58d8-240">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-241">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="e58d8-241">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-242">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e58d8-242">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-243">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-244">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="e58d8-244">The current health of the element.</span></span> <span data-ttu-id="e58d8-245">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e58d8-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-246">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e58d8-246">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-247">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e58d8-247">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-249">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz de propriedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="e58d8-249">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="e58d8-250">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e58d8-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-251">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e58d8-251">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-252">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e58d8-252">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-253">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-254">A data e a hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="e58d8-254">The date and time when the object was installed.</span></span> <span data-ttu-id="e58d8-255">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="e58d8-255">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="e58d8-256">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e58d8-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-257">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e58d8-257">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-258">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e58d8-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-260">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="e58d8-260">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-261">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="e58d8-261">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e58d8-262">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e58d8-262">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-263">**IsBound**</span><span class="sxs-lookup"><span data-stu-id="e58d8-263">**IsBound**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-264">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e58d8-264">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-265">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-266">Especifica se a porta Wi-Fi está associada à arquitetura de rede da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e58d8-266">Specifies if the Wi-Fi port is bound to the virtual machine networking architecture.</span></span> <span data-ttu-id="e58d8-267">Esse será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e58d8-267">This will be one of the following values.</span></span>



| <span data-ttu-id="e58d8-268">Valor</span><span class="sxs-lookup"><span data-stu-id="e58d8-268">Value</span></span>                                                                                                                                                        | <span data-ttu-id="e58d8-269">Significado</span><span class="sxs-lookup"><span data-stu-id="e58d8-269">Meaning</span></span>                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="True"></span><span id="true"></span><span id="TRUE"></span><dl> <span data-ttu-id="e58d8-270"><dt>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="e58d8-270"><dt>**True**</dt></span></span> </dl>     | <span data-ttu-id="e58d8-271">A porta Wi-Fi está associada à arquitetura de rede da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e58d8-271">The Wi-Fi port is bound to the virtual machine networking architecture.</span></span> <br/>     |
| <span id="False"></span><span id="false"></span><span id="FALSE"></span><dl> <span data-ttu-id="e58d8-272"><dt>**For**</dt></span><span class="sxs-lookup"><span data-stu-id="e58d8-272"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="e58d8-273">A porta Wi-Fi não está associada à arquitetura de rede da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e58d8-273">The Wi-Fi port is not bound to the virtual machine networking architecture.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="e58d8-274">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e58d8-274">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-275">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e58d8-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-276">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-277">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e58d8-277">The last error code reported by the logical device.</span></span> <span data-ttu-id="e58d8-278">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e58d8-278">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-279">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="e58d8-279">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-280">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e58d8-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-281">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-282">Especifica o tipo de tecnologia de link para a porta.</span><span class="sxs-lookup"><span data-stu-id="e58d8-282">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="e58d8-283">Quando definido como 1 (outro), a propriedade **OtherLinkTechnology** contém uma descrição de cadeia de caracteres do tipo de link.</span><span class="sxs-lookup"><span data-stu-id="e58d8-283">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="e58d8-284">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="e58d8-284">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="e58d8-285"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e58d8-285"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-286"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="e58d8-286"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-287"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="e58d8-287"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-288"><span id="IB"></span><span id="ib"></span>**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="e58d8-288"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-289"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="e58d8-289"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-290"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="e58d8-290"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-291"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="e58d8-291"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-292"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token ring** (7)</span><span class="sxs-lookup"><span data-stu-id="e58d8-292"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-293"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="e58d8-293"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-294"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infravermelho** (9)</span><span class="sxs-lookup"><span data-stu-id="e58d8-294"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-295"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="e58d8-295"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-296"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**LAN sem fio** (11)</span><span class="sxs-lookup"><span data-stu-id="e58d8-296"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Wireless LAN** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e58d8-297">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="e58d8-297">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-298">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e58d8-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-299">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-300">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="e58d8-300">This property has been deprecated.</span></span> <span data-ttu-id="e58d8-301">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e58d8-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-302">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="e58d8-302">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-303">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e58d8-303">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-305">Qualificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="e58d8-305">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-306">A largura de banda máxima da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="e58d8-306">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="e58d8-307">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e58d8-307">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-308">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e58d8-308">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-309">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e58d8-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-310">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-311">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="e58d8-311">The label by which the object is known.</span></span> <span data-ttu-id="e58d8-312">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e58d8-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-313">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="e58d8-313">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-314">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e58d8-314">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-315">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-316">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="e58d8-316">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-317">Uma matriz de cadeias de caracteres que contêm os endereços MAC para a porta.</span><span class="sxs-lookup"><span data-stu-id="e58d8-317">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="e58d8-318">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="e58d8-318">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-319">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="e58d8-319">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-320">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e58d8-320">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-322">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="e58d8-322">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="e58d8-323">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="e58d8-323">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e58d8-324">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e58d8-324">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-325">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="e58d8-325">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-326">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e58d8-326">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-328">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="e58d8-328">The current statuses of the object.</span></span> <span data-ttu-id="e58d8-329">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e58d8-329">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-330">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="e58d8-330">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-331">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e58d8-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-333">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="e58d8-333">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="e58d8-334">Essa propriedade deve ser definida como **NULL** quando a propriedade **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="e58d8-334">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="e58d8-335">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e58d8-335">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-336">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="e58d8-336">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-337">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e58d8-337">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-338">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-339">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e58d8-339">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="e58d8-340">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e58d8-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-341">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="e58d8-341">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-342">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e58d8-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-344">Um valor de cadeia de caracteres que descreve **LinkTechnology** quando é definido como 1, (outro).</span><span class="sxs-lookup"><span data-stu-id="e58d8-344">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="e58d8-345">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="e58d8-345">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-346">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="e58d8-346">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-347">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e58d8-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-348">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-349">O uso dessa propriedade é preterido no lugar da propriedade **PortType** .</span><span class="sxs-lookup"><span data-stu-id="e58d8-349">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="e58d8-350">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="e58d8-350">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-351">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="e58d8-351">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-352">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e58d8-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-354">Descreve o tipo de módulo, quando **PortType** é definido como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="e58d8-354">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="e58d8-355">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e58d8-355">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-356">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="e58d8-356">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-357">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e58d8-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-358">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-359">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="e58d8-359">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-360">O endereço de rede embutido em uma porta.</span><span class="sxs-lookup"><span data-stu-id="e58d8-360">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="e58d8-361">Esse endereço codificado pode ser alterado usando uma atualização de firmware ou uma configuração de software.</span><span class="sxs-lookup"><span data-stu-id="e58d8-361">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="e58d8-362">Quando essa alteração é feita, o campo deve ser atualizado ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="e58d8-362">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="e58d8-363">Essa propriedade deverá ser **nula** se não existir nenhum endereço codificado para o adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="e58d8-363">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="e58d8-364">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="e58d8-364">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-365">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="e58d8-365">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-366">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e58d8-366">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-367">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-368">O número da porta.</span><span class="sxs-lookup"><span data-stu-id="e58d8-368">The port number.</span></span> <span data-ttu-id="e58d8-369">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="e58d8-369">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-370">**PortType**</span><span class="sxs-lookup"><span data-stu-id="e58d8-370">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-371">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e58d8-371">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-372">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-373">O modo específico que está habilitado no momento para a porta.</span><span class="sxs-lookup"><span data-stu-id="e58d8-373">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="e58d8-374">Quando definido como 1 (outro), a propriedade **OtherPortType** relacionada contém uma descrição de cadeia de caracteres do tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="e58d8-374">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="e58d8-375">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e58d8-375">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="e58d8-376"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e58d8-376"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-377"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="e58d8-377"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-378"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>+ **/50 10BaseT de cobre** (50)</span><span class="sxs-lookup"><span data-stu-id="e58d8-378"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-379"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="e58d8-379"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-380"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="e58d8-380"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-381"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000baseT** (53)</span><span class="sxs-lookup"><span data-stu-id="e58d8-381"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-382"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="e58d8-382"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-383"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="e58d8-383"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-384"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="e58d8-384"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-385"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**100 Fibre 100BASE-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="e58d8-385"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-386"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="e58d8-386"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-387"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="e58d8-387"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-388"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="e58d8-388"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-389"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000BASE-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="e58d8-389"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-390"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-Sr** (105)</span><span class="sxs-lookup"><span data-stu-id="e58d8-390"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-391"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="e58d8-391"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-392"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="e58d8-392"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-393"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="e58d8-393"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-394"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="e58d8-394"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-395"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="e58d8-395"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-396"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-ovo** (111)</span><span class="sxs-lookup"><span data-stu-id="e58d8-396"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-397"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e58d8-397"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e58d8-398">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e58d8-398">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-399">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e58d8-399">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-400">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-401">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e58d8-401">The power management capabilities of the device.</span></span> <span data-ttu-id="e58d8-402">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e58d8-402">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-403">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="e58d8-403">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-404">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e58d8-404">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-405">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-406">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="e58d8-406">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="e58d8-407">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e58d8-407">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-408">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="e58d8-408">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-409">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e58d8-409">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-410">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-411">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="e58d8-411">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="e58d8-412">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e58d8-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-413">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="e58d8-413">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-414">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e58d8-414">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-415">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-416">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="e58d8-416">Provides high level status information.</span></span> <span data-ttu-id="e58d8-417">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer informações de status de integridade detalhadas e de alto nível para o elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="e58d8-417">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="e58d8-418">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="e58d8-418">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e58d8-419">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e58d8-419">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-420">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="e58d8-420">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-421">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e58d8-421">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-422">Tipo de acesso: somente gravação</span><span class="sxs-lookup"><span data-stu-id="e58d8-422">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-423">Qualificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="e58d8-423">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-424">A largura de banda solicitada da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="e58d8-424">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="e58d8-425">A largura de banda real é relatada na propriedade **Speed** .</span><span class="sxs-lookup"><span data-stu-id="e58d8-425">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="e58d8-426">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e58d8-426">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-427">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="e58d8-427">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-428">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e58d8-428">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-429">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-430">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="e58d8-430">The last requested or desired state for the element.</span></span> <span data-ttu-id="e58d8-431">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e58d8-431">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-432">**Velocidade**</span><span class="sxs-lookup"><span data-stu-id="e58d8-432">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-433">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e58d8-433">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-434">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-435">Qualificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="e58d8-435">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-436">A largura de banda da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="e58d8-436">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="e58d8-437">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e58d8-437">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-438">**Status**</span><span class="sxs-lookup"><span data-stu-id="e58d8-438">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-439">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e58d8-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-440">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-441">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e58d8-441">The current status of the object.</span></span> <span data-ttu-id="e58d8-442">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e58d8-442">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-443">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e58d8-443">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-444">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e58d8-444">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-445">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-446">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="e58d8-446">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="e58d8-447">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e58d8-447">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-448">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e58d8-448">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-449">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e58d8-449">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-450">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-451">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e58d8-451">The current state of the logical device.</span></span> <span data-ttu-id="e58d8-452">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e58d8-452">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-453">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="e58d8-453">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-454">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e58d8-454">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-455">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-456">Qualificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="e58d8-456">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-457">A MTU (unidade máxima de transmissão) que pode ter suporte, em bytes.</span><span class="sxs-lookup"><span data-stu-id="e58d8-457">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="e58d8-458">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="e58d8-458">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-459">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e58d8-459">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-460">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e58d8-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-461">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-461">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-462">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="e58d8-462">The scoping system's creation class name.</span></span> <span data-ttu-id="e58d8-463">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e58d8-463">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-464">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e58d8-464">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-465">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e58d8-465">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-466">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-466">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-467">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="e58d8-467">The scoping system's name.</span></span> <span data-ttu-id="e58d8-468">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e58d8-468">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-469">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="e58d8-469">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-470">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e58d8-470">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-471">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-471">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-472">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="e58d8-472">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="e58d8-473">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e58d8-473">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-474">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="e58d8-474">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-475">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e58d8-475">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-476">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-477">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="e58d8-477">The total number of hours that this device has been powered on.</span></span> <span data-ttu-id="e58d8-478">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e58d8-478">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-479">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="e58d8-479">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-480">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e58d8-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-481">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-482">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="e58d8-482">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="e58d8-483">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="e58d8-483">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e58d8-484">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="e58d8-484">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e58d8-485">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e58d8-485">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-486">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e58d8-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e58d8-487">Em algumas circunstâncias, uma porta lógica pode ser identificável como uma porta de front-end ou de back-end.</span><span class="sxs-lookup"><span data-stu-id="e58d8-487">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="e58d8-488">Um exemplo dessa situação seria uma matriz de armazenamento que pode ter portas de back-end para se comunicar com unidades de disco e portas de front-end para se comunicar com os hosts.</span><span class="sxs-lookup"><span data-stu-id="e58d8-488">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="e58d8-489">Se não houver nenhuma restrição sobre o uso da porta, o valor deverá ser definido como 4 (não restrito).</span><span class="sxs-lookup"><span data-stu-id="e58d8-489">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="e58d8-490">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e58d8-490">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="e58d8-491"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e58d8-491"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-492"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Somente front-end** (2)</span><span class="sxs-lookup"><span data-stu-id="e58d8-492"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-493"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Somente back-end** (3)</span><span class="sxs-lookup"><span data-stu-id="e58d8-493"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e58d8-494"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Não restrito** (4)</span><span class="sxs-lookup"><span data-stu-id="e58d8-494"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e58d8-495">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e58d8-495">Requirements</span></span>



| <span data-ttu-id="e58d8-496">Requisito</span><span class="sxs-lookup"><span data-stu-id="e58d8-496">Requirement</span></span> | <span data-ttu-id="e58d8-497">Valor</span><span class="sxs-lookup"><span data-stu-id="e58d8-497">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e58d8-498">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e58d8-498">Minimum supported client</span></span><br/> | <span data-ttu-id="e58d8-499">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e58d8-499">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e58d8-500">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e58d8-500">Minimum supported server</span></span><br/> | <span data-ttu-id="e58d8-501">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e58d8-501">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e58d8-502">Namespace</span><span class="sxs-lookup"><span data-stu-id="e58d8-502">Namespace</span></span><br/>                | <span data-ttu-id="e58d8-503">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e58d8-503">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e58d8-504">MOF</span><span class="sxs-lookup"><span data-stu-id="e58d8-504">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e58d8-505"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e58d8-505"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e58d8-506">DLL</span><span class="sxs-lookup"><span data-stu-id="e58d8-506">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e58d8-507"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e58d8-507"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

