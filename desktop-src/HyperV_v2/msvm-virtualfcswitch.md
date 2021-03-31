---
description: Representa um comutador Fibre Channel virtual.
ms.assetid: 4300747b-3ffc-4caf-8f0b-76cab6d2294e
title: Classe Msvm_VirtualFcSwitch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualFcSwitch
- Msvm_VirtualFcSwitch.SetPowerState
- Msvm_VirtualFcSwitch.InstanceID
- Msvm_VirtualFcSwitch.Caption
- Msvm_VirtualFcSwitch.Description
- Msvm_VirtualFcSwitch.ElementName
- Msvm_VirtualFcSwitch.InstallDate
- Msvm_VirtualFcSwitch.OperationalStatus
- Msvm_VirtualFcSwitch.StatusDescriptions
- Msvm_VirtualFcSwitch.Status
- Msvm_VirtualFcSwitch.HealthState
- Msvm_VirtualFcSwitch.CommunicationStatus
- Msvm_VirtualFcSwitch.DetailedStatus
- Msvm_VirtualFcSwitch.OperatingStatus
- Msvm_VirtualFcSwitch.PrimaryStatus
- Msvm_VirtualFcSwitch.EnabledState
- Msvm_VirtualFcSwitch.OtherEnabledState
- Msvm_VirtualFcSwitch.RequestedState
- Msvm_VirtualFcSwitch.EnabledDefault
- Msvm_VirtualFcSwitch.TimeOfLastStateChange
- Msvm_VirtualFcSwitch.AvailableRequestedStates
- Msvm_VirtualFcSwitch.TransitioningToState
- Msvm_VirtualFcSwitch.CreationClassName
- Msvm_VirtualFcSwitch.Name
- Msvm_VirtualFcSwitch.PrimaryOwnerName
- Msvm_VirtualFcSwitch.PrimaryOwnerContact
- Msvm_VirtualFcSwitch.Roles
- Msvm_VirtualFcSwitch.NameFormat
- Msvm_VirtualFcSwitch.OtherIdentifyingInfo
- Msvm_VirtualFcSwitch.IdentifyingDescriptions
- Msvm_VirtualFcSwitch.Dedicated
- Msvm_VirtualFcSwitch.OtherDedicatedDescriptions
- Msvm_VirtualFcSwitch.ResetCapability
- Msvm_VirtualFcSwitch.PowerManagementCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 66c6b7a284a2751b1c9b664428a9c90db9f468a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090000"
---
# <a name="msvm_virtualfcswitch-class"></a><span data-ttu-id="22bfa-103">\_Classe Msvm VirtualFcSwitch</span><span class="sxs-lookup"><span data-stu-id="22bfa-103">Msvm\_VirtualFcSwitch class</span></span>

<span data-ttu-id="22bfa-104">Representa um comutador Fibre Channel virtual.</span><span class="sxs-lookup"><span data-stu-id="22bfa-104">Represents a virtual Fibre Channel switch.</span></span> <span data-ttu-id="22bfa-105">Cada opção é associada a uma porta de Fibre Channel física à qual muitas portas de Fibre Channel sintéticas podem ser conectadas.</span><span class="sxs-lookup"><span data-stu-id="22bfa-105">Each switch is associated with one physical Fibre Channel port to which many synthetic Fibre Channel ports can be connected.</span></span> <span data-ttu-id="22bfa-106">O comutador em si não é altamente configurável e atua principalmente como um espaço reservado.</span><span class="sxs-lookup"><span data-stu-id="22bfa-106">The switch itself is not highly configurable and acts mostly as a placeholder.</span></span>

<span data-ttu-id="22bfa-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="22bfa-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="22bfa-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22bfa-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualFcSwitch : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   CreationClassName;
  string   Name;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability;
  uint16   PowerManagementCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="22bfa-109">Membros</span><span class="sxs-lookup"><span data-stu-id="22bfa-109">Members</span></span>

<span data-ttu-id="22bfa-110">A classe **Msvm \_ VirtualFcSwitch** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="22bfa-110">The **Msvm\_VirtualFcSwitch** class has these types of members:</span></span>

-   [<span data-ttu-id="22bfa-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="22bfa-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="22bfa-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="22bfa-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="22bfa-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="22bfa-113">Methods</span></span>

<span data-ttu-id="22bfa-114">A classe **Msvm \_ VirtualFcSwitch** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="22bfa-114">The **Msvm\_VirtualFcSwitch** class has these methods.</span></span>



| <span data-ttu-id="22bfa-115">Método</span><span class="sxs-lookup"><span data-stu-id="22bfa-115">Method</span></span>                                                                | <span data-ttu-id="22bfa-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="22bfa-116">Description</span></span>                              |
|:----------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="22bfa-117">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="22bfa-117">**RequestStateChange**</span></span>](msvm-virtualfcswitch-requeststatechange.md) | <span data-ttu-id="22bfa-118">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="22bfa-118">Requests a state change.</span></span><br/>      |
| <span data-ttu-id="22bfa-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="22bfa-119">**SetPowerState**</span></span>                                                     | <span data-ttu-id="22bfa-120">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="22bfa-120">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="22bfa-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="22bfa-121">Properties</span></span>

<span data-ttu-id="22bfa-122">A classe **Msvm \_ VirtualFcSwitch** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="22bfa-122">The **Msvm\_VirtualFcSwitch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="22bfa-123">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="22bfa-123">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-124">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22bfa-124">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-126">Indica os valores possíveis para o parâmetro *requestedstate* do método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="22bfa-126">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="22bfa-127">Os valores listados serão um subconjunto dos valores contidos na propriedade **RequestedStatesSupported** da instância associada do **CIM \_ EnabledLogicalElementCapabilities**, em que os valores selecionados são uma função do estado atual do objeto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="22bfa-127">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="22bfa-128">Essa propriedade pode ser não **nula** se uma implementação for capaz de anunciar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="22bfa-128">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="22bfa-129">Essa propriedade será **nula** se uma implementação não puder determinar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="22bfa-129">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="22bfa-130">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="22bfa-130">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="22bfa-131"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="22bfa-131"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-132"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="22bfa-132"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-133"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="22bfa-133"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-134"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="22bfa-134"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-135"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="22bfa-135"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-136"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="22bfa-136"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-137"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="22bfa-137"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-138"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="22bfa-138"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-139"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="22bfa-139"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-140"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="22bfa-140"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="22bfa-141">)</span><span class="sxs-lookup"><span data-stu-id="22bfa-141">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="22bfa-142">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="22bfa-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22bfa-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-145">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="22bfa-145">A short description of the object.</span></span> <span data-ttu-id="22bfa-146">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="22bfa-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="22bfa-147">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="22bfa-147">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-148">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22bfa-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-150">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="22bfa-150">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="22bfa-151">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="22bfa-151">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="22bfa-152">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="22bfa-152">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="22bfa-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="22bfa-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="22bfa-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="22bfa-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="22bfa-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="22bfa-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="22bfa-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="22bfa-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="22bfa-160">)</span><span class="sxs-lookup"><span data-stu-id="22bfa-160">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="22bfa-161">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="22bfa-161">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22bfa-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-164">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="22bfa-164">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="22bfa-165">Essa propriedade é herdada [**do \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system).</span><span class="sxs-lookup"><span data-stu-id="22bfa-165">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).</span></span>

</dd> <dt>

<span data-ttu-id="22bfa-166">**Dedicado**</span><span class="sxs-lookup"><span data-stu-id="22bfa-166">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-167">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22bfa-167">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-169">Indica se o sistema de computador é um sistema de finalidade especial (dedicado a um uso específico), em vez de ser um sistema de finalidade geral.</span><span class="sxs-lookup"><span data-stu-id="22bfa-169">Indicates whether the computer system is a special-purpose system (dedicated to a particular use), versus being a general-purpose system.</span></span> <span data-ttu-id="22bfa-170">Essa propriedade é herdada do [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)e é sempre definida como 0 (não dedicada).</span><span class="sxs-lookup"><span data-stu-id="22bfa-170">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 0 (Not Dedicated).</span></span>

</dd> <dt>

<span data-ttu-id="22bfa-171">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="22bfa-171">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-172">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22bfa-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-174">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="22bfa-174">A description of the object.</span></span> <span data-ttu-id="22bfa-175">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="22bfa-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="22bfa-176">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="22bfa-176">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-177">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22bfa-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-179">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="22bfa-179">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="22bfa-180">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="22bfa-180">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="22bfa-181">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="22bfa-181">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="22bfa-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="22bfa-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="22bfa-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="22bfa-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="22bfa-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="22bfa-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="22bfa-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="22bfa-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="22bfa-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="22bfa-190">)</span><span class="sxs-lookup"><span data-stu-id="22bfa-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="22bfa-191">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="22bfa-191">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22bfa-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-194">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="22bfa-194">A display name for the object.</span></span> <span data-ttu-id="22bfa-195">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="22bfa-195">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="22bfa-196">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="22bfa-196">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-197">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22bfa-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-199">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="22bfa-199">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="22bfa-200">Essa propriedade é herdada de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="22bfa-200">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="22bfa-201"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="22bfa-201"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-202"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="22bfa-202"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-203"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Habilitado, mas offline** (6)</span><span class="sxs-lookup"><span data-stu-id="22bfa-203"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="22bfa-204">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="22bfa-204">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-205">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22bfa-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-207">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="22bfa-207">The enabled and disabled states of an element.</span></span> <span data-ttu-id="22bfa-208">Essa propriedade também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="22bfa-208">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="22bfa-209">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 5 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="22bfa-209">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="22bfa-210">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="22bfa-210">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-211">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22bfa-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-213">Especifica a integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="22bfa-213">Specifies the current health of the element.</span></span> <span data-ttu-id="22bfa-214">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="22bfa-214">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="22bfa-215">Quando ocorrer um erro crítico, verifique o log de eventos para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="22bfa-215">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="22bfa-216">A propriedade **enabledstate** também pode conter mais informações.</span><span class="sxs-lookup"><span data-stu-id="22bfa-216">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="22bfa-217">Por exemplo, quando o espaço em disco está muito baixo, o **HealthState** é definido como 25, a máquina virtual pausa e **enabledstate** é definido como 32768 (em pausa).</span><span class="sxs-lookup"><span data-stu-id="22bfa-217">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="22bfa-218">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="22bfa-218">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="22bfa-219">Valor</span><span class="sxs-lookup"><span data-stu-id="22bfa-219">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="22bfa-220">Significado</span><span class="sxs-lookup"><span data-stu-id="22bfa-220">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="22bfa-221"><dt>**OK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="22bfa-221"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="22bfa-222">O elemento é totalmente funcional e está operando em parâmetros operacionais normais e sem erros.</span><span class="sxs-lookup"><span data-stu-id="22bfa-222">The element is fully functional and is operating within normal operational parameters and without error.</span></span><br/> |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="22bfa-223"><dt>**Maior falha**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="22bfa-223"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="22bfa-224">O elemento sofreu uma falha grave.</span><span class="sxs-lookup"><span data-stu-id="22bfa-224">The element has suffered a major failure.</span></span><br/>                                                                |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="22bfa-225"><dt>**Falha crítica**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="22bfa-225"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="22bfa-226">O elemento é não funcional e a recuperação pode não ser possível.</span><span class="sxs-lookup"><span data-stu-id="22bfa-226">The element is nonfunctional and recovery might not be possible.</span></span><br/>                                         |



 

</dd> <dt>

<span data-ttu-id="22bfa-227">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="22bfa-227">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-228">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22bfa-228">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-229">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-230">Essa propriedade é herdada do [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="22bfa-230">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="22bfa-231">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="22bfa-231">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-232">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="22bfa-232">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-234">A data e a hora em que a configuração de máquina virtual foi criada para uma máquina virtual, ou **nula**, para um sistema operacional de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="22bfa-234">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="22bfa-235">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="22bfa-235">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22bfa-236">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="22bfa-236">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-237">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22bfa-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-239">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="22bfa-239">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-240">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="22bfa-240">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="22bfa-241">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="22bfa-241">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="22bfa-242">**Nome**</span><span class="sxs-lookup"><span data-stu-id="22bfa-242">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-243">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22bfa-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-245">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="22bfa-245">The label by which the object is known.</span></span> <span data-ttu-id="22bfa-246">Essa propriedade é herdada [**do \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system).</span><span class="sxs-lookup"><span data-stu-id="22bfa-246">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).</span></span>

</dd> <dt>

<span data-ttu-id="22bfa-247">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="22bfa-247">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-248">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22bfa-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-249">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-250">Uma cadeia de caracteres que identifica como o nome do sistema foi gerado, usando a heurística de subclasse.</span><span class="sxs-lookup"><span data-stu-id="22bfa-250">A string that identifies how the system name was generated, using the subclass heuristic.</span></span> <span data-ttu-id="22bfa-251">Essa propriedade é herdada do [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="22bfa-251">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="22bfa-252">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="22bfa-252">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-253">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22bfa-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-254">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-255">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="22bfa-255">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="22bfa-256">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="22bfa-256">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="22bfa-257">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="22bfa-257">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="22bfa-258"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="22bfa-258"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-259"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="22bfa-259"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-260"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="22bfa-260"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-261"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="22bfa-261"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-262"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="22bfa-262"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-263"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="22bfa-263"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-264"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="22bfa-264"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-265"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="22bfa-265"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-266"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="22bfa-266"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-267"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="22bfa-267"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-268"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="22bfa-268"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-269"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="22bfa-269"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-270"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="22bfa-270"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-271"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="22bfa-271"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-272"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="22bfa-272"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-273"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="22bfa-273"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-274"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="22bfa-274"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-275"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="22bfa-275"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-276"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="22bfa-276"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="22bfa-277">)</span><span class="sxs-lookup"><span data-stu-id="22bfa-277">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="22bfa-278">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="22bfa-278">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-279">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22bfa-279">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-281">Uma matriz que contém os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="22bfa-281">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="22bfa-282">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="22bfa-282">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22bfa-283">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="22bfa-283">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-284">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22bfa-284">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-285">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-286">Uma cadeia de caracteres que descreve como ou por que o sistema é dedicado quando a matriz **dedicada** inclui o valor 2 (outro).</span><span class="sxs-lookup"><span data-stu-id="22bfa-286">A string that describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span> <span data-ttu-id="22bfa-287">Essa propriedade é herdada do [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="22bfa-287">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="22bfa-288">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="22bfa-288">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-289">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22bfa-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-290">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-291">O estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="22bfa-291">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="22bfa-292">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="22bfa-292">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="22bfa-293">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="22bfa-293">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="22bfa-294">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="22bfa-294">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-295">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22bfa-295">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-296">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-297">Essa propriedade é herdada do [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="22bfa-297">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="22bfa-298">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="22bfa-298">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-299">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22bfa-299">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-300">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-301">Essa propriedade é herdada do [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="22bfa-301">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="22bfa-302">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="22bfa-302">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-303">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22bfa-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-305">Uma cadeia de caracteres que indica como o proprietário do sistema primário pode ser alcançado (por exemplo, um número de telefone ou um endereço de email).</span><span class="sxs-lookup"><span data-stu-id="22bfa-305">A string that indicates how the primary system owner can be reached (for example, a phone number or an email address).</span></span> <span data-ttu-id="22bfa-306">Essa propriedade é herdada [**do \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="22bfa-306">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="22bfa-307">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="22bfa-307">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-308">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22bfa-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-310">O nome do proprietário do sistema primário.</span><span class="sxs-lookup"><span data-stu-id="22bfa-310">The name of the primary system owner.</span></span> <span data-ttu-id="22bfa-311">Essa propriedade é herdada [**do \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="22bfa-311">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="22bfa-312">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="22bfa-312">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-313">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22bfa-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-315">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="22bfa-315">Provides high level status information.</span></span> <span data-ttu-id="22bfa-316">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="22bfa-316">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="22bfa-317">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="22bfa-317">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="22bfa-318">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="22bfa-318">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="22bfa-319"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="22bfa-319"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-320"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="22bfa-320"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-321"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="22bfa-321"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-322"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="22bfa-322"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-323"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="22bfa-323"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-324"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="22bfa-324"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="22bfa-325">)</span><span class="sxs-lookup"><span data-stu-id="22bfa-325">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="22bfa-326">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="22bfa-326">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-327">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22bfa-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-329">O último estado solicitado ou desejado para o elemento como passado para o método **RequestStateChange** , ou 12 (não aplicável) se nenhuma alteração de estado estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="22bfa-329">The last requested or desired state for the element as passed to the **RequestStateChange** method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="22bfa-330">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="22bfa-330">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="22bfa-331">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="22bfa-331">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="22bfa-332">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="22bfa-332">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="22bfa-333">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="22bfa-333">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-334">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22bfa-334">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-335">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-336">Essa propriedade é herdada do [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem).</span><span class="sxs-lookup"><span data-stu-id="22bfa-336">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem).</span></span>

</dd> <dt>

<span data-ttu-id="22bfa-337">**Funções**</span><span class="sxs-lookup"><span data-stu-id="22bfa-337">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-338">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22bfa-338">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-339">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-340">Uma matriz de cadeias de caracteres que descreve as funções que o sistema desempenha no ambiente de tecnologia da informação.</span><span class="sxs-lookup"><span data-stu-id="22bfa-340">An array of strings that describe the roles the system plays in the information technology environment.</span></span> <span data-ttu-id="22bfa-341">Essa propriedade é herdada [**do \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="22bfa-341">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="22bfa-342">**Status**</span><span class="sxs-lookup"><span data-stu-id="22bfa-342">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-343">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22bfa-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-344">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-345">Uma cadeia de caracteres que especifica o status do elemento.</span><span class="sxs-lookup"><span data-stu-id="22bfa-345">A string that specifies the status of the element.</span></span> <span data-ttu-id="22bfa-346">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="22bfa-346">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22bfa-347">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="22bfa-347">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-348">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22bfa-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-349">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-350">Qualificadores: **ArrayType** ("indexado")</span><span class="sxs-lookup"><span data-stu-id="22bfa-350">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-351">Uma matriz que contém cadeias de caracteres que descrevem os valores correspondentes da matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="22bfa-351">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="22bfa-352">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="22bfa-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22bfa-353">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="22bfa-353">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-354">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="22bfa-354">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-355">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-356">A data e a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="22bfa-356">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="22bfa-357">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="22bfa-357">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="22bfa-358">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="22bfa-358">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22bfa-359">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22bfa-359">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22bfa-360">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22bfa-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22bfa-361">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="22bfa-361">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="22bfa-362">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="22bfa-362">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="22bfa-363">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22bfa-363">Requirements</span></span>



| <span data-ttu-id="22bfa-364">Requisito</span><span class="sxs-lookup"><span data-stu-id="22bfa-364">Requirement</span></span> | <span data-ttu-id="22bfa-365">Valor</span><span class="sxs-lookup"><span data-stu-id="22bfa-365">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22bfa-366">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22bfa-366">Minimum supported client</span></span><br/> | <span data-ttu-id="22bfa-367">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="22bfa-367">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="22bfa-368">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22bfa-368">Minimum supported server</span></span><br/> | <span data-ttu-id="22bfa-369">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="22bfa-369">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="22bfa-370">Namespace</span><span class="sxs-lookup"><span data-stu-id="22bfa-370">Namespace</span></span><br/>                | <span data-ttu-id="22bfa-371">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="22bfa-371">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="22bfa-372">MOF</span><span class="sxs-lookup"><span data-stu-id="22bfa-372">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22bfa-373"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="22bfa-373"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="22bfa-374">DLL</span><span class="sxs-lookup"><span data-stu-id="22bfa-374">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22bfa-375"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="22bfa-375"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

