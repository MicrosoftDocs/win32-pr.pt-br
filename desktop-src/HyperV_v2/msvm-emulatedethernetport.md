---
description: Representa um adaptador Ethernet emulado.
ms.assetid: 8E990C76-7D48-42B0-BB4D-C4C07B1C482A
title: Classe Msvm_EmulatedEthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EmulatedEthernetPort
- Msvm_EmulatedEthernetPort.SetPowerState
- Msvm_EmulatedEthernetPort.EnableDevice
- Msvm_EmulatedEthernetPort.OnlineDevice
- Msvm_EmulatedEthernetPort.QuiesceDevice
- Msvm_EmulatedEthernetPort.SaveProperties
- Msvm_EmulatedEthernetPort.RestoreProperties
- Msvm_EmulatedEthernetPort.InstanceID
- Msvm_EmulatedEthernetPort.Caption
- Msvm_EmulatedEthernetPort.Description
- Msvm_EmulatedEthernetPort.ElementName
- Msvm_EmulatedEthernetPort.InstallDate
- Msvm_EmulatedEthernetPort.Name
- Msvm_EmulatedEthernetPort.OperationalStatus
- Msvm_EmulatedEthernetPort.StatusDescriptions
- Msvm_EmulatedEthernetPort.Status
- Msvm_EmulatedEthernetPort.HealthState
- Msvm_EmulatedEthernetPort.CommunicationStatus
- Msvm_EmulatedEthernetPort.DetailedStatus
- Msvm_EmulatedEthernetPort.OperatingStatus
- Msvm_EmulatedEthernetPort.PrimaryStatus
- Msvm_EmulatedEthernetPort.EnabledState
- Msvm_EmulatedEthernetPort.OtherEnabledState
- Msvm_EmulatedEthernetPort.RequestedState
- Msvm_EmulatedEthernetPort.EnabledDefault
- Msvm_EmulatedEthernetPort.TimeOfLastStateChange
- Msvm_EmulatedEthernetPort.AvailableRequestedStates
- Msvm_EmulatedEthernetPort.TransitioningToState
- Msvm_EmulatedEthernetPort.SystemCreationClassName
- Msvm_EmulatedEthernetPort.SystemName
- Msvm_EmulatedEthernetPort.CreationClassName
- Msvm_EmulatedEthernetPort.DeviceID
- Msvm_EmulatedEthernetPort.PowerManagementSupported
- Msvm_EmulatedEthernetPort.PowerManagementCapabilities
- Msvm_EmulatedEthernetPort.Availability
- Msvm_EmulatedEthernetPort.StatusInfo
- Msvm_EmulatedEthernetPort.LastErrorCode
- Msvm_EmulatedEthernetPort.ErrorDescription
- Msvm_EmulatedEthernetPort.ErrorCleared
- Msvm_EmulatedEthernetPort.OtherIdentifyingInfo
- Msvm_EmulatedEthernetPort.PowerOnHours
- Msvm_EmulatedEthernetPort.TotalPowerOnHours
- Msvm_EmulatedEthernetPort.IdentifyingDescriptions
- Msvm_EmulatedEthernetPort.AdditionalAvailability
- Msvm_EmulatedEthernetPort.MaxQuiesceTime
- Msvm_EmulatedEthernetPort.Speed
- Msvm_EmulatedEthernetPort.MaxSpeed
- Msvm_EmulatedEthernetPort.RequestedSpeed
- Msvm_EmulatedEthernetPort.UsageRestriction
- Msvm_EmulatedEthernetPort.PortType
- Msvm_EmulatedEthernetPort.OtherPortType
- Msvm_EmulatedEthernetPort.OtherNetworkPortType
- Msvm_EmulatedEthernetPort.PortNumber
- Msvm_EmulatedEthernetPort.LinkTechnology
- Msvm_EmulatedEthernetPort.OtherLinkTechnology
- Msvm_EmulatedEthernetPort.PermanentAddress
- Msvm_EmulatedEthernetPort.NetworkAddresses
- Msvm_EmulatedEthernetPort.FullDuplex
- Msvm_EmulatedEthernetPort.AutoSense
- Msvm_EmulatedEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_EmulatedEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_EmulatedEthernetPort.MaxDataSize
- Msvm_EmulatedEthernetPort.Capabilities
- Msvm_EmulatedEthernetPort.CapabilityDescriptions
- Msvm_EmulatedEthernetPort.EnabledCapabilities
- Msvm_EmulatedEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1ec13ae369f6d5e3d884f74c96d7df27c2f5fa97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758336"
---
# <a name="msvm_emulatedethernetport-class"></a><span data-ttu-id="b0168-103">\_Classe Msvm EmulatedEthernetPort</span><span class="sxs-lookup"><span data-stu-id="b0168-103">Msvm\_EmulatedEthernetPort class</span></span>

<span data-ttu-id="b0168-104">Representa um adaptador Ethernet emulado.</span><span class="sxs-lookup"><span data-stu-id="b0168-104">Represents an emulated Ethernet adapter.</span></span> <span data-ttu-id="b0168-105">Esse adaptador é usado quando uma máquina virtual não é capaz de executar a porta Ethernet sintética quando não há circuitos integrados instalados no convidado.</span><span class="sxs-lookup"><span data-stu-id="b0168-105">This adapter is used when a virtual machine is not capable of running the synthetic Ethernet port when no integrated circuits are installed in the guest.</span></span>

> [!Note]  
> <span data-ttu-id="b0168-106">Essa classe não está disponível para máquinas virtuais de geração 2.</span><span class="sxs-lookup"><span data-stu-id="b0168-106">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="b0168-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b0168-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0168-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0168-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EmulatedEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft Emulated Ethernet Port";
  string   ElementName = "Legacy Network Adapter";
  datetime InstallDate;
  string   Name = "Ethernet Port";
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
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
  string   CreationClassName = "Msvm_EmulatedEthernetPort";
  string   DeviceID = "Microsoft:GUID\device-specific data";
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
  uint64   Speed = 1000000000;
  uint64   MaxSpeed = 1000000000;
  uint64   RequestedSpeed = 1000000000;
  uint16   UsageRestriction = 4;
  uint16   PortType = 1;
  string   OtherPortType = "Virtual Ethernet";
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 2;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex = True;
  boolean  AutoSense = True;
  string   SupportedMaximumTransmissionUnit = 1500;
  uint64   ActiveMaximumTransmissionUnit = 1500;
  uint32   MaxDataSize = 1500;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="b0168-109">Membros</span><span class="sxs-lookup"><span data-stu-id="b0168-109">Members</span></span>

<span data-ttu-id="b0168-110">A classe **Msvm \_ EmulatedEthernetPort** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b0168-110">The **Msvm\_EmulatedEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="b0168-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="b0168-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="b0168-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b0168-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b0168-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="b0168-113">Methods</span></span>

<span data-ttu-id="b0168-114">A classe **Msvm \_ EmulatedEthernetPort** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b0168-114">The **Msvm\_EmulatedEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="b0168-115">Método</span><span class="sxs-lookup"><span data-stu-id="b0168-115">Method</span></span>                                                                     | <span data-ttu-id="b0168-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0168-116">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="b0168-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="b0168-117">**EnableDevice**</span></span>                                                           | <span data-ttu-id="b0168-118">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="b0168-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="b0168-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="b0168-119">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="b0168-120">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="b0168-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="b0168-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="b0168-121">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="b0168-122">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="b0168-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="b0168-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="b0168-123">**RequestStateChange**</span></span>](msvm-emulatedethernetport-requeststatechange.md) | <span data-ttu-id="b0168-124">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="b0168-124">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="b0168-125">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="b0168-125">**Reset**</span></span>](msvm-emulatedethernetport-reset.md)                           | <span data-ttu-id="b0168-126">Redefine o dispositivo emulado.</span><span class="sxs-lookup"><span data-stu-id="b0168-126">Resets the emulated device.</span></span><br/>   |
| <span data-ttu-id="b0168-127">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="b0168-127">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="b0168-128">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="b0168-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="b0168-129">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="b0168-129">**SaveProperties**</span></span>                                                         | <span data-ttu-id="b0168-130">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="b0168-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="b0168-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b0168-131">**SetPowerState**</span></span>                                                          | <span data-ttu-id="b0168-132">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="b0168-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b0168-133">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b0168-133">Properties</span></span>

<span data-ttu-id="b0168-134">A classe **Msvm \_ EmulatedEthernetPort** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b0168-134">The **Msvm\_EmulatedEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b0168-135">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="b0168-135">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-136">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b0168-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-138">A unidade de transmissão máxima (MTU) do negociada ou ativa, que pode ter suporte.</span><span class="sxs-lookup"><span data-stu-id="b0168-138">The active or negotiated maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="b0168-139">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)e é sempre definida como 1500.</span><span class="sxs-lookup"><span data-stu-id="b0168-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="b0168-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-141">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0168-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b0168-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-143">Qualquer disponibilidade e status adicionais do dispositivo, além do especificado na propriedade de **disponibilidade** .</span><span class="sxs-lookup"><span data-stu-id="b0168-143">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="b0168-144">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como 6 ("não aplicável").</span><span class="sxs-lookup"><span data-stu-id="b0168-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 ("Not Applicable").</span></span>

</dd> <dt>

<span data-ttu-id="b0168-145">**Autodetecção**</span><span class="sxs-lookup"><span data-stu-id="b0168-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-146">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b0168-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-148">Indica se a porta de rede é capaz de determinar automaticamente a velocidade ou outras características de comunicação da mídia de rede anexada.</span><span class="sxs-lookup"><span data-stu-id="b0168-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="b0168-149">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)e é sempre definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="b0168-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-150">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="b0168-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-151">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0168-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-153">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0168-153">The primary availability and status of the device.</span></span> <span data-ttu-id="b0168-154">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b0168-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="b0168-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-156">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0168-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b0168-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-158">Indica os valores possíveis para o parâmetro *requestedstate* do método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="b0168-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="b0168-159">Os valores listados serão um subconjunto dos valores contidos na propriedade **RequestedStatesSupported** da instância associada do **CIM \_ EnabledLogicalElementCapabilities**, em que os valores selecionados são uma função do estado atual do [**\_ EnabledLogicalElement do CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b0168-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="b0168-160">Essa propriedade pode ser não **nula** se uma implementação for capaz de anunciar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="b0168-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="b0168-161">Essa propriedade será **nula** se uma implementação não puder determinar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="b0168-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="b0168-162">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b0168-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="b0168-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="b0168-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b0168-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="b0168-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b0168-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="b0168-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b0168-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="b0168-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="b0168-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="b0168-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="b0168-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="b0168-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="b0168-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="b0168-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="b0168-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="b0168-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="b0168-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="b0168-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="b0168-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="b0168-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="b0168-173">)</span><span class="sxs-lookup"><span data-stu-id="b0168-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b0168-174">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="b0168-174">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-175">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0168-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b0168-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-177">Recursos da porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="b0168-177">Capabilities of the Ethernet port.</span></span> <span data-ttu-id="b0168-178">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="b0168-178">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-179">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="b0168-179">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-180">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0168-180">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b0168-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-182">Uma matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para qualquer um dos recursos de porta Ethernet que são indicados na matriz **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="b0168-182">An array of free-form strings that provides more detailed explanations for any of the Ethernet port features that are indicated in the **Capabilities** array.</span></span> <span data-ttu-id="b0168-183">Observe que cada entrada dessa matriz está relacionada à entrada na matriz de **recursos** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="b0168-183">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="b0168-184">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="b0168-184">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-185">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="b0168-185">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-186">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0168-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-188">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="b0168-188">A short description of the object.</span></span> <span data-ttu-id="b0168-189">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "porta Ethernet".</span><span class="sxs-lookup"><span data-stu-id="b0168-189">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="b0168-190">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="b0168-190">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-191">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0168-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-193">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="b0168-193">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="b0168-194">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="b0168-194">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b0168-195">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b0168-195">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b0168-196">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b0168-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-197">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0168-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-199">O nome da classe ou da subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="b0168-199">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="b0168-200">Quando usado com as outras propriedades de chave dessa classe, essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="b0168-200">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="b0168-201">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como "Msvm \_ EmulatedEthernetPort".</span><span class="sxs-lookup"><span data-stu-id="b0168-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_EmulatedEthernetPort".</span></span>

</dd> <dt>

<span data-ttu-id="b0168-202">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b0168-202">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-203">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0168-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-205">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="b0168-205">A description of the object.</span></span> <span data-ttu-id="b0168-206">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "porta de Ethernet emulada da Microsoft".</span><span class="sxs-lookup"><span data-stu-id="b0168-206">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Emulated Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="b0168-207">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="b0168-207">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-208">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0168-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-210">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="b0168-210">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="b0168-211">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="b0168-211">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b0168-212">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b0168-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b0168-213">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b0168-213">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-214">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0168-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-216">Um endereço ou outras informações de identificação usadas para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b0168-216">An address or other identifying information used to uniquely name the logical device.</span></span> <span data-ttu-id="b0168-217">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como "Microsoft:*GUID* \\ *específico de dados do dispositivo*".</span><span class="sxs-lookup"><span data-stu-id="b0168-217">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*\\*device-specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="b0168-218">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b0168-218">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-219">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0168-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-221">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="b0168-221">A display name for the object.</span></span> <span data-ttu-id="b0168-222">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "adaptador de rede herdado".</span><span class="sxs-lookup"><span data-stu-id="b0168-222">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Legacy Network Adapter".</span></span>

</dd> <dt>

<span data-ttu-id="b0168-223">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b0168-223">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-224">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0168-224">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b0168-225">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-226">Os recursos que estão habilitados na lista de todos os com suporte, que são definidos na matriz de **recursos** .</span><span class="sxs-lookup"><span data-stu-id="b0168-226">The capabilities that are enabled from the list of all supported ones, which are defined in the **Capabilities** array.</span></span> <span data-ttu-id="b0168-227">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="b0168-227">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-228">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="b0168-228">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-229">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0168-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-230">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-231">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="b0168-231">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="b0168-232">Essa propriedade é herdada de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e sempre é definida como 2 ("Enabled").</span><span class="sxs-lookup"><span data-stu-id="b0168-232">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is always set to 2 ("Enabled").</span></span>

</dd> <dt>

<span data-ttu-id="b0168-233">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="b0168-233">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-234">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0168-234">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-235">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-236">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="b0168-236">The enabled and disabled states of an element.</span></span> <span data-ttu-id="b0168-237">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 5 ("não aplicável").</span><span class="sxs-lookup"><span data-stu-id="b0168-237">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 ("Not Applicable").</span></span>

</dd> <dt>

<span data-ttu-id="b0168-238">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="b0168-238">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-239">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b0168-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-240">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-241">Indica se o erro relatado em **LastErrorCode** agora está limpo.</span><span class="sxs-lookup"><span data-stu-id="b0168-241">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="b0168-242">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="b0168-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-243">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b0168-243">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-244">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0168-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-245">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-246">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="b0168-246">A string that provides more information about the error recorded in **LastErrorCode**, and information on any corrective actions that can be taken.</span></span> <span data-ttu-id="b0168-247">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="b0168-247">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-248">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="b0168-248">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-249">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b0168-249">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-250">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-251">Indica se a porta está operando no modo full duplex.</span><span class="sxs-lookup"><span data-stu-id="b0168-251">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="b0168-252">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)e é sempre definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="b0168-252">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-253">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="b0168-253">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-254">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0168-254">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-255">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-256">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="b0168-256">The current health of the element.</span></span> <span data-ttu-id="b0168-257">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="b0168-257">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="b0168-258">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5 ("OK").</span><span class="sxs-lookup"><span data-stu-id="b0168-258">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 ("OK").</span></span>

</dd> <dt>

<span data-ttu-id="b0168-259">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="b0168-259">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-260">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0168-260">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b0168-261">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-262">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="b0168-262">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="b0168-263">Cada entrada dessa matriz está relacionada à entrada em **OtherIdentifyingInfo** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="b0168-263">Each entry of this array is related to the entry in **OtherIdentifyingInfo** that is located at the same index.</span></span> <span data-ttu-id="b0168-264">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="b0168-264">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-265">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b0168-265">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-266">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b0168-266">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-267">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-268">Um valor **DateTime** que indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="b0168-268">A **datetime** value that indicates when the object was installed.</span></span> <span data-ttu-id="b0168-269">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="b0168-269">Lack of a value does not indicate that the object is not installed.</span></span> <span data-ttu-id="b0168-270">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b0168-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b0168-271">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b0168-271">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-272">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0168-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-273">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0168-274">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="b0168-274">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b0168-275">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="b0168-275">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b0168-276">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b0168-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b0168-277">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b0168-277">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-278">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b0168-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-280">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b0168-280">The last error code reported by the logical device.</span></span> <span data-ttu-id="b0168-281">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="b0168-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-282">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="b0168-282">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-283">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0168-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-284">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-285">Os tipos de links.</span><span class="sxs-lookup"><span data-stu-id="b0168-285">The types of links.</span></span> <span data-ttu-id="b0168-286">Quando definido como 1 ("other"), a propriedade relacionada **OtherLinkTechnology** contém uma descrição de cadeia de caracteres do tipo de link.</span><span class="sxs-lookup"><span data-stu-id="b0168-286">When set to 1 ("Other"), the related property **OtherLinkTechnology** contains a string description of the type of link.</span></span> <span data-ttu-id="b0168-287">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) e é sempre definida como 2 ("Ethernet").</span><span class="sxs-lookup"><span data-stu-id="b0168-287">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) and is always set to 2 ("Ethernet").</span></span>

</dd> <dt>

<span data-ttu-id="b0168-288">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="b0168-288">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-289">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b0168-289">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-290">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-291">O tamanho máximo do campo de informações (não MAC) que será recebido ou transmitido.</span><span class="sxs-lookup"><span data-stu-id="b0168-291">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="b0168-292">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)e é sempre definida como 1500.</span><span class="sxs-lookup"><span data-stu-id="b0168-292">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-293">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="b0168-293">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-294">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b0168-294">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-296">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="b0168-296">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-297">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="b0168-297">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-298">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b0168-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-299">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-300">A largura de banda máxima da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="b0168-300">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="b0168-301">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))e é sempre definida como 1000000000.</span><span class="sxs-lookup"><span data-stu-id="b0168-301">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)), and it is always set to 1000000000.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-302">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b0168-302">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-303">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0168-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-305">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="b0168-305">The label by which the object is known.</span></span> <span data-ttu-id="b0168-306">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="b0168-306">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="b0168-307">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como "porta Ethernet".</span><span class="sxs-lookup"><span data-stu-id="b0168-307">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="b0168-308">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="b0168-308">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-309">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0168-309">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b0168-310">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-311">Os endereços MAC Ethernet/802.3, formatados como doze dígitos hexadecimais (por exemplo, "010203040506"), com cada par que representa um dos seis octetos do endereço MAC na ordem de bits canônica (o bit de endereço do grupo é encontrado no menor bit de ordem do primeiro caractere da cadeia de caracteres).</span><span class="sxs-lookup"><span data-stu-id="b0168-311">The Ethernet/802.3 MAC addresses, formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (the group address bit is found in the low order bit of the first character of the string).</span></span> <span data-ttu-id="b0168-312">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="b0168-312">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-313">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="b0168-313">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-314">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0168-314">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-315">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-316">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="b0168-316">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="b0168-317">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="b0168-317">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b0168-318">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b0168-318">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b0168-319">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="b0168-319">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-320">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0168-320">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b0168-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-322">O status atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="b0168-322">The current statuses of the element.</span></span> <span data-ttu-id="b0168-323">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 2 ("OK").</span><span class="sxs-lookup"><span data-stu-id="b0168-323">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 ("OK").</span></span>

</dd> <dt>

<span data-ttu-id="b0168-324">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b0168-324">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-325">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0168-325">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b0168-326">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-327">Uma matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para qualquer um dos recursos habilitados que são especificados como "outros".</span><span class="sxs-lookup"><span data-stu-id="b0168-327">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as "Other".</span></span> <span data-ttu-id="b0168-328">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="b0168-328">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-329">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="b0168-329">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-330">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0168-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-331">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-332">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="b0168-332">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="b0168-333">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="b0168-333">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="b0168-334">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="b0168-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-335">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="b0168-335">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-336">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0168-336">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b0168-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-338">Todos os dados, além das informações de ID do dispositivo, que podem ser usados para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b0168-338">Any data, in addition to device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="b0168-339">Por exemplo, você pode usar essa propriedade para armazenar o nome de exibição do sistema operacional para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0168-339">For example, you could use this property to hold the operating system's display name for the device.</span></span> <span data-ttu-id="b0168-340">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="b0168-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-341">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="b0168-341">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-342">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0168-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-344">Um valor de cadeia de caracteres que descreve **LinkTechnology** quando é definido como 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="b0168-344">A string value that describes **LinkTechnology** when it is set to 1 ("Other").</span></span> <span data-ttu-id="b0168-345">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="b0168-345">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-346">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="b0168-346">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-347">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0168-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-348">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-349">Essa propriedade é herdada de [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b0168-349">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) and is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-350">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="b0168-350">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-351">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0168-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-352">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-353">O tipo de módulo, quando **PortType** é definido como 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="b0168-353">The type of module, when **PortType** is set to 1 ("Other").</span></span> <span data-ttu-id="b0168-354">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)) e é sempre definida como "virtual Ethernet".</span><span class="sxs-lookup"><span data-stu-id="b0168-354">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)) and is always set to "Virtual Ethernet".</span></span>

</dd> <dt>

<span data-ttu-id="b0168-355">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="b0168-355">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-356">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0168-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-357">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-358">O endereço de rede embutido em uma porta.</span><span class="sxs-lookup"><span data-stu-id="b0168-358">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="b0168-359">Esse endereço pode ser alterado usando uma atualização de firmware ou uma configuração de software.</span><span class="sxs-lookup"><span data-stu-id="b0168-359">This address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="b0168-360">Quando essa alteração é feita, o campo deve ser atualizado ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="b0168-360">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="b0168-361">Isso deve ser deixado em branco se não existir nenhum endereço codificado para o adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="b0168-361">This should be left blank if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="b0168-362">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="b0168-362">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="b0168-363">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="b0168-363">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-364">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0168-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-365">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-366">As portas de rede geralmente são numeradas em relação a um módulo lógico ou um elemento de rede.</span><span class="sxs-lookup"><span data-stu-id="b0168-366">Network ports are often numbered relative to either a logical module or a network element.</span></span> <span data-ttu-id="b0168-367">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="b0168-367">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>



| <span data-ttu-id="b0168-368">Valor</span><span class="sxs-lookup"><span data-stu-id="b0168-368">Value</span></span>                                                                        | <span data-ttu-id="b0168-369">Significado</span><span class="sxs-lookup"><span data-stu-id="b0168-369">Meaning</span></span>                             |
|------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="b0168-370"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b0168-370"><dt>0</dt></span></span> </dl> | <span data-ttu-id="b0168-371">A NIC não está emulada.</span><span class="sxs-lookup"><span data-stu-id="b0168-371">The NIC is not emulated.</span></span><br/> |
| <dl> <span data-ttu-id="b0168-372"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b0168-372"><dt>1</dt></span></span> </dl> | <span data-ttu-id="b0168-373">A NIC é emulada.</span><span class="sxs-lookup"><span data-stu-id="b0168-373">The NIC is emulated.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="b0168-374">**PortType**</span><span class="sxs-lookup"><span data-stu-id="b0168-374">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-375">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0168-375">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-376">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-377">O modo específico que está habilitado no momento para a porta.</span><span class="sxs-lookup"><span data-stu-id="b0168-377">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="b0168-378">Quando definido como 1 ("other"), a propriedade relacionada **OtherPortType** contém uma descrição de cadeia de caracteres do tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="b0168-378">When set to 1 ("Other"), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="b0168-379">Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)e é sempre definida como 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="b0168-379">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1 ("Other").</span></span>

</dd> <dt>

<span data-ttu-id="b0168-380">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b0168-380">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-381">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0168-381">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b0168-382">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-383">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0168-383">The power management capabilities of the device.</span></span> <span data-ttu-id="b0168-384">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="b0168-384">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-385">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="b0168-385">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-386">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b0168-386">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-387">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-388">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="b0168-388">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="b0168-389">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="b0168-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-390">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="b0168-390">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-391">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b0168-391">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-392">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-393">O número de horas consecutivas em que este dispositivo foi ligado, desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="b0168-393">The number of consecutive hours that this device has been powered, since its last power cycle.</span></span> <span data-ttu-id="b0168-394">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="b0168-394">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-395">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="b0168-395">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-396">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0168-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-397">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-398">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="b0168-398">Provides high level status information.</span></span> <span data-ttu-id="b0168-399">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer informações de status de integridade detalhadas e de alto nível para o elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="b0168-399">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="b0168-400">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="b0168-400">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b0168-401">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b0168-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b0168-402">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="b0168-402">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-403">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b0168-403">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-404">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-405">A largura de banda solicitada da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="b0168-405">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="b0168-406">A largura de banda real é relatada em LogicalPort. Speed.</span><span class="sxs-lookup"><span data-stu-id="b0168-406">The actual bandwidth is reported in LogicalPort.Speed.</span></span> <span data-ttu-id="b0168-407">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))e é sempre definida como 1000000000.</span><span class="sxs-lookup"><span data-stu-id="b0168-407">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)), and it is always set to 1000000000.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-408">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="b0168-408">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-409">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0168-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-410">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-411">O último estado solicitado ou desejado para o serviço de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="b0168-411">The last requested or desired state for the management service.</span></span> <span data-ttu-id="b0168-412">Quando **enabledstate** é definido como 5 ("não aplicável"), essa propriedade não tem significado.</span><span class="sxs-lookup"><span data-stu-id="b0168-412">When **EnabledState** is set to 5 ("Not Applicable"), then this property has no meaning.</span></span> <span data-ttu-id="b0168-413">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 12 ("não aplicável").</span><span class="sxs-lookup"><span data-stu-id="b0168-413">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 ("Not Applicable").</span></span>

</dd> <dt>

<span data-ttu-id="b0168-414">**Velocidade**</span><span class="sxs-lookup"><span data-stu-id="b0168-414">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-415">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b0168-415">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-416">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-417">A largura de banda atual da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="b0168-417">The current bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="b0168-418">Para portas que variam de largura de banda ou para aquelas em que não é possível fazer nenhuma estimativa precisa, essa propriedade deve conter a largura de banda nominal.</span><span class="sxs-lookup"><span data-stu-id="b0168-418">For ports that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span> <span data-ttu-id="b0168-419">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)e é sempre definida como 1000000000.</span><span class="sxs-lookup"><span data-stu-id="b0168-419">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to 1000000000.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-420">**Status**</span><span class="sxs-lookup"><span data-stu-id="b0168-420">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-421">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0168-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-422">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-423">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="b0168-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-424">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="b0168-424">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-425">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0168-425">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b0168-426">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-427">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="b0168-427">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="b0168-428">As entradas nessa matriz são correlacionadas com aquelas no mesmo índice de matriz em **OperationalStatus**.</span><span class="sxs-lookup"><span data-stu-id="b0168-428">Entries in this array are correlated with those at the same array index in **OperationalStatus**.</span></span> <span data-ttu-id="b0168-429">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como "OK".</span><span class="sxs-lookup"><span data-stu-id="b0168-429">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="b0168-430">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b0168-430">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-431">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0168-431">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-432">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-433">O estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b0168-433">The state of the logical device.</span></span> <span data-ttu-id="b0168-434">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="b0168-434">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-435">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="b0168-435">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-436">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0168-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-437">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0168-438">Qualificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="b0168-438">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b0168-439">A MTU (unidade máxima de transmissão) que pode ter suporte, em bytes.</span><span class="sxs-lookup"><span data-stu-id="b0168-439">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="b0168-440">Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)e é sempre definida como 1500.</span><span class="sxs-lookup"><span data-stu-id="b0168-440">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-441">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b0168-441">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-442">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0168-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-443">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-444">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="b0168-444">The creation class name of the scoping system.</span></span> <span data-ttu-id="b0168-445">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como "Msvm \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="b0168-445">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="b0168-446">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b0168-446">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-447">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0168-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-448">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-449">A ID da máquina virtual no formato **GUID** .</span><span class="sxs-lookup"><span data-stu-id="b0168-449">The virtual machine ID in **GUID** form.</span></span> <span data-ttu-id="b0168-450">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b0168-450">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b0168-451">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="b0168-451">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-452">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b0168-452">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-453">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-454">A data ou a hora em que o **enabledstate** do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="b0168-454">The date or time when the **EnabledState** of the element last changed.</span></span> <span data-ttu-id="b0168-455">Se o estado do elemento não tiver sido alterado e essa propriedade for populada, ela deverá ser definida como um valor de intervalo de 0.</span><span class="sxs-lookup"><span data-stu-id="b0168-455">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="b0168-456">Se uma alteração de estado foi solicitada, mas rejeitada ou ainda não processada, a propriedade não deve ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="b0168-456">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="b0168-457">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="b0168-457">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-458">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="b0168-458">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-459">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0168-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-460">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-461">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="b0168-461">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="b0168-462">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="b0168-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-463">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="b0168-463">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-464">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0168-464">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-465">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-466">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="b0168-466">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="b0168-467">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="b0168-467">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0168-468">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="b0168-468">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0168-469">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0168-469">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0168-470">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0168-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0168-471">Em algumas circunstâncias, uma porta lógica pode ser identificável como uma porta de front-end ou de back-end.</span><span class="sxs-lookup"><span data-stu-id="b0168-471">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="b0168-472">Se não houver nenhuma restrição sobre o uso da porta, o valor deverá ser definido como 4 ("não restrito").</span><span class="sxs-lookup"><span data-stu-id="b0168-472">If there is no restriction on the use of the port, then the value should be set to 4 ("Not Restricted").</span></span> <span data-ttu-id="b0168-473">Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)) e é sempre definida como 4 ("não restrito").</span><span class="sxs-lookup"><span data-stu-id="b0168-473">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)) and is always set to 4 ("Not Restricted").</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0168-474">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0168-474">Remarks</span></span>

<span data-ttu-id="b0168-475">O acesso à classe **Msvm \_ EmulatedEthernetPort** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="b0168-475">Access to the **Msvm\_EmulatedEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b0168-476">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b0168-476">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="b0168-477">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b0168-477">Examples</span></span>

<span data-ttu-id="b0168-478">Consulte [consultando objetos de rede](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="b0168-478">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b0168-479">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0168-479">Requirements</span></span>



| <span data-ttu-id="b0168-480">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0168-480">Requirement</span></span> | <span data-ttu-id="b0168-481">Valor</span><span class="sxs-lookup"><span data-stu-id="b0168-481">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0168-482">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0168-482">Minimum supported client</span></span><br/> | <span data-ttu-id="b0168-483">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b0168-483">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b0168-484">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0168-484">Minimum supported server</span></span><br/> | <span data-ttu-id="b0168-485">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b0168-485">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b0168-486">Namespace</span><span class="sxs-lookup"><span data-stu-id="b0168-486">Namespace</span></span><br/>                | <span data-ttu-id="b0168-487">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="b0168-487">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b0168-488">MOF</span><span class="sxs-lookup"><span data-stu-id="b0168-488">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0168-489"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b0168-489"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0168-490">DLL</span><span class="sxs-lookup"><span data-stu-id="b0168-490">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0168-491"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b0168-491"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b0168-492">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0168-492">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0168-493">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="b0168-493">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="b0168-494">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="b0168-494">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

