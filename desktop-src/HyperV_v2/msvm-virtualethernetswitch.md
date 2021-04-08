---
description: Representa um comutador Ethernet virtual. Cada comutador tem várias portas diferentes às quais os adaptadores de rede podem ser anexados. O comutador em si não é altamente configurável e atua principalmente como um espaço reservado.
ms.assetid: 9415477a-9423-40fa-a887-3a93da1374af
title: Classe Msvm_VirtualEthernetSwitch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitch
- Msvm_VirtualEthernetSwitch.SetPowerState
- Msvm_VirtualEthernetSwitch.InstanceID
- Msvm_VirtualEthernetSwitch.Caption
- Msvm_VirtualEthernetSwitch.Description
- Msvm_VirtualEthernetSwitch.ElementName
- Msvm_VirtualEthernetSwitch.InstallDate
- Msvm_VirtualEthernetSwitch.OperationalStatus
- Msvm_VirtualEthernetSwitch.StatusDescriptions
- Msvm_VirtualEthernetSwitch.Status
- Msvm_VirtualEthernetSwitch.HealthState
- Msvm_VirtualEthernetSwitch.CommunicationStatus
- Msvm_VirtualEthernetSwitch.DetailedStatus
- Msvm_VirtualEthernetSwitch.OperatingStatus
- Msvm_VirtualEthernetSwitch.PrimaryStatus
- Msvm_VirtualEthernetSwitch.EnabledState
- Msvm_VirtualEthernetSwitch.OtherEnabledState
- Msvm_VirtualEthernetSwitch.RequestedState
- Msvm_VirtualEthernetSwitch.EnabledDefault
- Msvm_VirtualEthernetSwitch.TimeOfLastStateChange
- Msvm_VirtualEthernetSwitch.AvailableRequestedStates
- Msvm_VirtualEthernetSwitch.TransitioningToState
- Msvm_VirtualEthernetSwitch.CreationClassName
- Msvm_VirtualEthernetSwitch.Name
- Msvm_VirtualEthernetSwitch.PrimaryOwnerName
- Msvm_VirtualEthernetSwitch.PrimaryOwnerContact
- Msvm_VirtualEthernetSwitch.Roles
- Msvm_VirtualEthernetSwitch.NameFormat
- Msvm_VirtualEthernetSwitch.OtherIdentifyingInfo
- Msvm_VirtualEthernetSwitch.IdentifyingDescriptions
- Msvm_VirtualEthernetSwitch.Dedicated
- Msvm_VirtualEthernetSwitch.OtherDedicatedDescriptions
- Msvm_VirtualEthernetSwitch.ResetCapability
- Msvm_VirtualEthernetSwitch.PowerManagementCapabilities
- Msvm_VirtualEthernetSwitch.MaxVMQOffloads
- Msvm_VirtualEthernetSwitch.MaxIOVOffloads
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1cd916e24a6e34ed6a70002c4988f55810050c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829026"
---
# <a name="msvm_virtualethernetswitch-class"></a><span data-ttu-id="0423c-105">\_Classe Msvm VirtualEthernetSwitch</span><span class="sxs-lookup"><span data-stu-id="0423c-105">Msvm\_VirtualEthernetSwitch class</span></span>

<span data-ttu-id="0423c-106">Representa um comutador Ethernet virtual.</span><span class="sxs-lookup"><span data-stu-id="0423c-106">Represents a virtual Ethernet switch.</span></span> <span data-ttu-id="0423c-107">Cada comutador tem várias portas diferentes às quais os adaptadores de rede podem ser anexados.</span><span class="sxs-lookup"><span data-stu-id="0423c-107">Each switch has many different ports to which network adapters can be attached.</span></span> <span data-ttu-id="0423c-108">O comutador em si não é altamente configurável e atua principalmente como um espaço reservado.</span><span class="sxs-lookup"><span data-stu-id="0423c-108">The switch itself is not highly configurable and acts mostly as a placeholder.</span></span>

<span data-ttu-id="0423c-109">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0423c-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0423c-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0423c-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitch : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption = "Virtual Switch";
  string   Description = "Microsoft Virtual Switch";
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
  string   CreationClassName = "Msvm_VirtualEthernetSwitch";
  string   Name = "GUID";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability = 5;
  uint16   PowerManagementCapabilities[];
  uint32   MaxVMQOffloads;
  uint32   MaxIOVOffloads;
};
```

## <a name="members"></a><span data-ttu-id="0423c-111">Membros</span><span class="sxs-lookup"><span data-stu-id="0423c-111">Members</span></span>

<span data-ttu-id="0423c-112">A classe **Msvm \_ VirtualEthernetSwitch** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0423c-112">The **Msvm\_VirtualEthernetSwitch** class has these types of members:</span></span>

-   [<span data-ttu-id="0423c-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="0423c-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="0423c-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0423c-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0423c-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="0423c-115">Methods</span></span>

<span data-ttu-id="0423c-116">A classe **Msvm \_ VirtualEthernetSwitch** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="0423c-116">The **Msvm\_VirtualEthernetSwitch** class has these methods.</span></span>



| <span data-ttu-id="0423c-117">Método</span><span class="sxs-lookup"><span data-stu-id="0423c-117">Method</span></span>                                                                      | <span data-ttu-id="0423c-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="0423c-118">Description</span></span>                              |
|:----------------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="0423c-119">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="0423c-119">**RequestStateChange**</span></span>](msvm-virtualethernetswitch-requeststatechange.md) | <span data-ttu-id="0423c-120">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="0423c-120">Requests a state change.</span></span><br/>      |
| <span data-ttu-id="0423c-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0423c-121">**SetPowerState**</span></span>                                                           | <span data-ttu-id="0423c-122">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="0423c-122">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0423c-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0423c-123">Properties</span></span>

<span data-ttu-id="0423c-124">A classe **Msvm \_ VirtualEthernetSwitch** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0423c-124">The **Msvm\_VirtualEthernetSwitch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0423c-125">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="0423c-125">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-126">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0423c-126">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0423c-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-128">Indica os valores possíveis para o parâmetro *requestedstate* do método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="0423c-128">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="0423c-129">Os valores listados serão um subconjunto dos valores contidos na propriedade **RequestedStatesSupported** da instância associada do **CIM \_ EnabledLogicalElementCapabilities**, em que os valores selecionados são uma função do estado atual do objeto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0423c-129">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="0423c-130">Essa propriedade pode ser não **nula** se uma implementação for capaz de anunciar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="0423c-130">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="0423c-131">Essa propriedade será **nula** se uma implementação não puder determinar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="0423c-131">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="0423c-132">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0423c-132">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="0423c-133"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="0423c-133"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-134"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="0423c-134"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-135"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="0423c-135"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-136"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="0423c-136"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-137"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="0423c-137"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-138"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="0423c-138"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-139"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="0423c-139"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-140"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="0423c-140"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-141"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="0423c-141"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-142"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="0423c-142"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="0423c-143">)</span><span class="sxs-lookup"><span data-stu-id="0423c-143">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0423c-144">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="0423c-144">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0423c-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0423c-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-147">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="0423c-147">A short description of the object.</span></span> <span data-ttu-id="0423c-148">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "comutador virtual".</span><span class="sxs-lookup"><span data-stu-id="0423c-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Switch".</span></span>

</dd> <dt>

<span data-ttu-id="0423c-149">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="0423c-149">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-150">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0423c-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0423c-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-152">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="0423c-152">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="0423c-153">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="0423c-153">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0423c-154">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0423c-154">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0423c-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="0423c-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-156"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="0423c-156"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-157"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="0423c-157"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-158"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="0423c-158"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-159"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="0423c-159"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-160"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0423c-160"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-161"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="0423c-161"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0423c-162">)</span><span class="sxs-lookup"><span data-stu-id="0423c-162">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0423c-163">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0423c-163">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0423c-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0423c-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-166">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="0423c-166">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="0423c-167">Essa propriedade é herdada [**do \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)e é sempre definida como "Msvm \_ VirtualEthernetSwitch".</span><span class="sxs-lookup"><span data-stu-id="0423c-167">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="0423c-168">**Dedicado**</span><span class="sxs-lookup"><span data-stu-id="0423c-168">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-169">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0423c-169">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0423c-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-171">Indica se o sistema de computador é um sistema de finalidade especial (dedicado a um uso específico), em vez de ser um sistema de finalidade geral.</span><span class="sxs-lookup"><span data-stu-id="0423c-171">Indicates whether the computer system is a special-purpose system (dedicated to a particular use), versus being a general-purpose system.</span></span> <span data-ttu-id="0423c-172">Essa propriedade é herdada do [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)e é sempre definida como 0 (não dedicada).</span><span class="sxs-lookup"><span data-stu-id="0423c-172">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 0 (Not Dedicated).</span></span>

</dd> <dt>

<span data-ttu-id="0423c-173">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0423c-173">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0423c-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0423c-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-176">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="0423c-176">A description of the object.</span></span> <span data-ttu-id="0423c-177">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "comutador virtual da Microsoft".</span><span class="sxs-lookup"><span data-stu-id="0423c-177">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Virtual Switch".</span></span>

</dd> <dt>

<span data-ttu-id="0423c-178">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="0423c-178">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-179">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0423c-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0423c-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-181">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="0423c-181">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="0423c-182">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="0423c-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0423c-183">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0423c-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0423c-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="0423c-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="0423c-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="0423c-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="0423c-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="0423c-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="0423c-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0423c-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="0423c-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0423c-192">)</span><span class="sxs-lookup"><span data-stu-id="0423c-192">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0423c-193">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0423c-193">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-194">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0423c-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0423c-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-196">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="0423c-196">A display name for the object.</span></span> <span data-ttu-id="0423c-197">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0423c-197">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0423c-198">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="0423c-198">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-199">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0423c-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0423c-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-201">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="0423c-201">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="0423c-202">Essa propriedade é herdada de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="0423c-202">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0423c-203"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="0423c-203"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-204"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="0423c-204"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-205"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Habilitado, mas offline** (6)</span><span class="sxs-lookup"><span data-stu-id="0423c-205"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0423c-206">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="0423c-206">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-207">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0423c-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0423c-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-209">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="0423c-209">The enabled and disabled states of an element.</span></span> <span data-ttu-id="0423c-210">Essa propriedade também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="0423c-210">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="0423c-211">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 5 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="0423c-211">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="0423c-212">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="0423c-212">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-213">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0423c-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0423c-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-215">Especifica a integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="0423c-215">Specifies the current health of the element.</span></span> <span data-ttu-id="0423c-216">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="0423c-216">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="0423c-217">Quando ocorrer um erro crítico, verifique o log de eventos para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="0423c-217">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="0423c-218">A propriedade **enabledstate** também pode conter mais informações.</span><span class="sxs-lookup"><span data-stu-id="0423c-218">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="0423c-219">Por exemplo, quando o espaço em disco está muito baixo, o **HealthState** é definido como 25, a máquina virtual pausa e **enabledstate** é definido como 32768 (em pausa).</span><span class="sxs-lookup"><span data-stu-id="0423c-219">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="0423c-220">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0423c-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="0423c-221">Valor</span><span class="sxs-lookup"><span data-stu-id="0423c-221">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="0423c-222">Significado</span><span class="sxs-lookup"><span data-stu-id="0423c-222">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="0423c-223"><dt>**OK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="0423c-223"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="0423c-224">O elemento é totalmente funcional e está operando em parâmetros operacionais normais e sem erros.</span><span class="sxs-lookup"><span data-stu-id="0423c-224">The element is fully functional and is operating within normal operational parameters and without error.</span></span><br/> |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="0423c-225"><dt>**Maior falha**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="0423c-225"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="0423c-226">O elemento sofreu uma falha grave.</span><span class="sxs-lookup"><span data-stu-id="0423c-226">The element has suffered a major failure.</span></span><br/>                                                                |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="0423c-227"><dt>**Falha crítica**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="0423c-227"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="0423c-228">O elemento não é funcional e a recuperação pode não ser possível.</span><span class="sxs-lookup"><span data-stu-id="0423c-228">The element is nonfunctional, and recovery might not be possible.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="0423c-229">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0423c-229">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-230">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0423c-230">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0423c-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-232">Essa propriedade é herdada do [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0423c-232">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0423c-233">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0423c-233">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-234">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0423c-234">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0423c-235">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-236">A data e a hora em que a configuração de máquina virtual foi criada para uma máquina virtual, ou **nula**, para um sistema operacional de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="0423c-236">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="0423c-237">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0423c-237">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0423c-238">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0423c-238">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-239">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0423c-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0423c-240">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0423c-241">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="0423c-241">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0423c-242">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="0423c-242">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0423c-243">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0423c-243">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0423c-244">**MaxIOVOffloads**</span><span class="sxs-lookup"><span data-stu-id="0423c-244">**MaxIOVOffloads**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-245">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0423c-245">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0423c-246">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-247">O número máximo de descarregamentos de função virtual de SR-IOV (virtualização de e/s de raiz única) disponíveis nesta opção.</span><span class="sxs-lookup"><span data-stu-id="0423c-247">The maximum number of single root IO virtualization (SR-IOV) virtual function offloads available on this switch.</span></span>

</dd> <dt>

<span data-ttu-id="0423c-248">**MaxVMQOffloads**</span><span class="sxs-lookup"><span data-stu-id="0423c-248">**MaxVMQOffloads**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-249">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0423c-249">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0423c-250">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0423c-250">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0423c-251">O número máximo de descarregamentos de VMQ (fila de máquina virtual) permitidos para uma porta nesse comutador.</span><span class="sxs-lookup"><span data-stu-id="0423c-251">The maximum number of virtual machine queue (VMQ) offloads allowed for a port on this switch.</span></span>

</dd> <dt>

<span data-ttu-id="0423c-252">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0423c-252">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-253">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0423c-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0423c-254">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-255">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="0423c-255">The label by which the object is known.</span></span> <span data-ttu-id="0423c-256">Essa propriedade é herdada [**do \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)e é sempre definida como "*GUID*".</span><span class="sxs-lookup"><span data-stu-id="0423c-256">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="0423c-257">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="0423c-257">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-258">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0423c-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0423c-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-260">Uma cadeia de caracteres que identifica como o nome do sistema foi gerado, usando a heurística de subclasse.</span><span class="sxs-lookup"><span data-stu-id="0423c-260">A string that identifies how the system name was generated, using the subclass heuristic.</span></span> <span data-ttu-id="0423c-261">Essa propriedade é herdada do [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0423c-261">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0423c-262">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="0423c-262">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-263">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0423c-263">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0423c-264">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-265">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="0423c-265">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="0423c-266">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="0423c-266">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0423c-267">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0423c-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0423c-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="0423c-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-269"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="0423c-269"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-270"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="0423c-270"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-271"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="0423c-271"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-272"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="0423c-272"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-273"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="0423c-273"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-274"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="0423c-274"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-275"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="0423c-275"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-276"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="0423c-276"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-277"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="0423c-277"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-278"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="0423c-278"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-279"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="0423c-279"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-280"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="0423c-280"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-281"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="0423c-281"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-282"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="0423c-282"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-283"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="0423c-283"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-284"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="0423c-284"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-285"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0423c-285"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-286"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="0423c-286"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0423c-287">)</span><span class="sxs-lookup"><span data-stu-id="0423c-287">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0423c-288">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="0423c-288">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-289">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0423c-289">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0423c-290">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-291">Uma matriz que contém os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="0423c-291">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="0423c-292">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0423c-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0423c-293">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0423c-293">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-294">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0423c-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0423c-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-296">Uma cadeia de caracteres que descreve como ou por que o sistema é dedicado quando a matriz **dedicada** inclui o valor 2 (outro).</span><span class="sxs-lookup"><span data-stu-id="0423c-296">A string that describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span> <span data-ttu-id="0423c-297">Essa propriedade é herdada do [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0423c-297">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0423c-298">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="0423c-298">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-299">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0423c-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0423c-300">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-301">O estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="0423c-301">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="0423c-302">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="0423c-302">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="0423c-303">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0423c-303">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0423c-304">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="0423c-304">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-305">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0423c-305">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0423c-306">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-307">Essa propriedade é herdada do [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0423c-307">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0423c-308">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0423c-308">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-309">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0423c-309">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0423c-310">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-311">Essa propriedade é herdada do [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="0423c-311">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0423c-312">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="0423c-312">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-313">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0423c-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0423c-314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-315">Uma cadeia de caracteres que indica como o proprietário do sistema primário pode ser alcançado (por exemplo, um número de telefone ou um endereço de email).</span><span class="sxs-lookup"><span data-stu-id="0423c-315">A string that indicates how the primary system owner can be reached (for example, a phone number or an email address).</span></span> <span data-ttu-id="0423c-316">Essa propriedade é herdada [**do \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="0423c-316">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0423c-317">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="0423c-317">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-318">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0423c-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0423c-319">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-320">O nome do proprietário do sistema primário.</span><span class="sxs-lookup"><span data-stu-id="0423c-320">The name of the primary system owner.</span></span> <span data-ttu-id="0423c-321">Essa propriedade é herdada [**do \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="0423c-321">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0423c-322">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="0423c-322">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-323">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0423c-323">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0423c-324">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-325">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="0423c-325">Provides high level status information.</span></span> <span data-ttu-id="0423c-326">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="0423c-326">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="0423c-327">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="0423c-327">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0423c-328">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0423c-328">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0423c-329"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="0423c-329"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-330"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="0423c-330"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-331"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="0423c-331"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-332"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="0423c-332"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0423c-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0423c-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="0423c-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0423c-335">)</span><span class="sxs-lookup"><span data-stu-id="0423c-335">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0423c-336">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="0423c-336">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-337">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0423c-337">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0423c-338">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-339">O último estado solicitado ou desejado para o elemento como passado para o método **RequestStateChange** , ou 12 (não aplicável) se nenhuma alteração de estado estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="0423c-339">The last requested or desired state for the element as passed to the **RequestStateChange** method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="0423c-340">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="0423c-340">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="0423c-341">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="0423c-341">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="0423c-342">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0423c-342">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0423c-343">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="0423c-343">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-344">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0423c-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0423c-345">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-346">Essa propriedade é herdada do [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)e é sempre definida como 5 (não implementado).</span><span class="sxs-lookup"><span data-stu-id="0423c-346">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 5 (Not implemented).</span></span>

</dd> <dt>

<span data-ttu-id="0423c-347">**Funções**</span><span class="sxs-lookup"><span data-stu-id="0423c-347">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-348">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0423c-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0423c-349">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-350">Uma matriz de cadeias de caracteres que descreve as funções que o sistema desempenha no ambiente de tecnologia da informação.</span><span class="sxs-lookup"><span data-stu-id="0423c-350">An array of strings that describe the roles the system plays in the information technology environment.</span></span> <span data-ttu-id="0423c-351">Essa propriedade é herdada [**do \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="0423c-351">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0423c-352">**Status**</span><span class="sxs-lookup"><span data-stu-id="0423c-352">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-353">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0423c-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0423c-354">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-355">Uma cadeia de caracteres que especifica o status do elemento.</span><span class="sxs-lookup"><span data-stu-id="0423c-355">A string that specifies the status of the element.</span></span> <span data-ttu-id="0423c-356">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0423c-356">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0423c-357">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0423c-357">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-358">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0423c-358">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0423c-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0423c-360">Qualificadores: **ArrayType** ("indexado")</span><span class="sxs-lookup"><span data-stu-id="0423c-360">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="0423c-361">Uma matriz que contém cadeias de caracteres que descrevem os valores correspondentes da matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="0423c-361">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="0423c-362">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0423c-362">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0423c-363">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="0423c-363">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-364">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0423c-364">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0423c-365">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-366">A data e a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="0423c-366">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="0423c-367">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0423c-367">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0423c-368">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="0423c-368">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0423c-369">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0423c-369">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0423c-370">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0423c-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0423c-371">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="0423c-371">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="0423c-372">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0423c-372">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0423c-373">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0423c-373">Requirements</span></span>



| <span data-ttu-id="0423c-374">Requisito</span><span class="sxs-lookup"><span data-stu-id="0423c-374">Requirement</span></span> | <span data-ttu-id="0423c-375">Valor</span><span class="sxs-lookup"><span data-stu-id="0423c-375">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0423c-376">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0423c-376">Minimum supported client</span></span><br/> | <span data-ttu-id="0423c-377">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0423c-377">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0423c-378">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0423c-378">Minimum supported server</span></span><br/> | <span data-ttu-id="0423c-379">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0423c-379">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0423c-380">Namespace</span><span class="sxs-lookup"><span data-stu-id="0423c-380">Namespace</span></span><br/>                | <span data-ttu-id="0423c-381">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="0423c-381">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0423c-382">MOF</span><span class="sxs-lookup"><span data-stu-id="0423c-382">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0423c-383"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0423c-383"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0423c-384">DLL</span><span class="sxs-lookup"><span data-stu-id="0423c-384">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0423c-385"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0423c-385"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

