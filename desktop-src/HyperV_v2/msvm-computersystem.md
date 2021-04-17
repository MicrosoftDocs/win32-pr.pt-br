---
description: Representa um sistema de computador físico ou uma máquina virtual.
ms.assetid: 1db9e169-1466-4898-ab95-e9d622fe43cb
title: Classe Msvm_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem
- Msvm_ComputerSystem.SetPowerState
- Msvm_ComputerSystem.InstanceID
- Msvm_ComputerSystem.Caption
- Msvm_ComputerSystem.Description
- Msvm_ComputerSystem.ElementName
- Msvm_ComputerSystem.InstallDate
- Msvm_ComputerSystem.OperationalStatus
- Msvm_ComputerSystem.StatusDescriptions
- Msvm_ComputerSystem.Status
- Msvm_ComputerSystem.HealthState
- Msvm_ComputerSystem.CommunicationStatus
- Msvm_ComputerSystem.DetailedStatus
- Msvm_ComputerSystem.OperatingStatus
- Msvm_ComputerSystem.PrimaryStatus
- Msvm_ComputerSystem.EnabledState
- Msvm_ComputerSystem.OtherEnabledState
- Msvm_ComputerSystem.RequestedState
- Msvm_ComputerSystem.EnabledDefault
- Msvm_ComputerSystem.TimeOfLastStateChange
- Msvm_ComputerSystem.AvailableRequestedStates
- Msvm_ComputerSystem.TransitioningToState
- Msvm_ComputerSystem.CreationClassName
- Msvm_ComputerSystem.Name
- Msvm_ComputerSystem.PrimaryOwnerName
- Msvm_ComputerSystem.PrimaryOwnerContact
- Msvm_ComputerSystem.Roles
- Msvm_ComputerSystem.NameFormat
- Msvm_ComputerSystem.OtherIdentifyingInfo
- Msvm_ComputerSystem.IdentifyingDescriptions
- Msvm_ComputerSystem.Dedicated
- Msvm_ComputerSystem.OtherDedicatedDescriptions
- Msvm_ComputerSystem.ResetCapability
- Msvm_ComputerSystem.PowerManagementCapabilities
- Msvm_ComputerSystem.OnTimeInMilliseconds
- Msvm_ComputerSystem.ProcessID
- Msvm_ComputerSystem.TimeOfLastConfigurationChange
- Msvm_ComputerSystem.NumberOfNumaNodes
- Msvm_ComputerSystem.ReplicationState
- Msvm_ComputerSystem.ReplicationHealth
- Msvm_ComputerSystem.ReplicationMode
- Msvm_ComputerSystem.FailedOverReplicationType
- Msvm_ComputerSystem.LastReplicationType
- Msvm_ComputerSystem.LastApplicationConsistentReplicationTime
- Msvm_ComputerSystem.LastReplicationTime
- Msvm_ComputerSystem.LastSuccessfulBackupTime
- Msvm_ComputerSystem.EnhancedSessionModeState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae36179e14b584bad4e68350e27d485cdc10c42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571658"
---
# <a name="msvm_computersystem-class"></a><span data-ttu-id="526ed-103">\_Classe de ComputerSystem Msvm</span><span class="sxs-lookup"><span data-stu-id="526ed-103">Msvm\_ComputerSystem class</span></span>

<span data-ttu-id="526ed-104">Representa um sistema de computador físico ou uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-104">Represents a physical computer system or virtual machine.</span></span>

<span data-ttu-id="526ed-105">Para recuperar informações para o VMMS, use a classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="526ed-105">To retrieve information for the VMMS, use the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="526ed-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="526ed-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="526ed-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="526ed-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ComputerSystem : CIM_ComputerSystem
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
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   CreationClassName;
  string   Name = "GUID";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability = 1;
  uint16   PowerManagementCapabilities[];
  uint64   OnTimeInMilliseconds;
  uint32   ProcessID;
  datetime TimeOfLastConfigurationChange;
  uint16   NumberOfNumaNodes;
  uint16   ReplicationState;
  uint16   ReplicationHealth;
  uint16   ReplicationMode;
  uint16   FailedOverReplicationType;
  uint16   LastReplicationType;
  DateTime LastApplicationConsistentReplicationTime;
  DateTime LastReplicationTime;
  DateTime LastSuccessfulBackupTime;
  uint16   EnhancedSessionModeState;
};
```

## <a name="members"></a><span data-ttu-id="526ed-108">Membros</span><span class="sxs-lookup"><span data-stu-id="526ed-108">Members</span></span>

<span data-ttu-id="526ed-109">A classe de **\_ ComputerSystem Msvm** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="526ed-109">The **Msvm\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="526ed-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="526ed-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="526ed-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="526ed-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="526ed-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="526ed-112">Methods</span></span>

<span data-ttu-id="526ed-113">A classe **Msvm \_ ComputerSystem** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="526ed-113">The **Msvm\_ComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="526ed-114">Método</span><span class="sxs-lookup"><span data-stu-id="526ed-114">Method</span></span>                                                                                         | <span data-ttu-id="526ed-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="526ed-115">Description</span></span>                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="526ed-116">**InjectNonMaskableInterrupt**</span><span class="sxs-lookup"><span data-stu-id="526ed-116">**InjectNonMaskableInterrupt**</span></span>](injectnonmaskableinterrupt-msvm-computersystem.md)           | <span data-ttu-id="526ed-117">Injeta uma interrupção não mascarável na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-117">Injects a non-maskable interrupt into the virtual machine.</span></span> <span data-ttu-id="526ed-118">Esse método só tem suporte para instâncias da classe **Msvm \_ ComputerSystem** que representam uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-118">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/> <span data-ttu-id="526ed-119">**Windows 8.1:** Não há suporte para este método até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="526ed-119">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                                    |
| [<span data-ttu-id="526ed-120">**RequestReplicationStateChange**</span><span class="sxs-lookup"><span data-stu-id="526ed-120">**RequestReplicationStateChange**</span></span>](msvm-computersystem-requestreplicationstatechange.md)     | <span data-ttu-id="526ed-121">Solicita que o estado de replicação da máquina virtual seja alterado para o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="526ed-121">Requests that the replication state of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="526ed-122">Esse método só tem suporte para instâncias da classe **Msvm \_ ComputerSystem** que representam uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-122">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="526ed-123">**RequestReplicationStateChangeEx**</span><span class="sxs-lookup"><span data-stu-id="526ed-123">**RequestReplicationStateChangeEx**</span></span>](msvm-requestreplicationstatechangeex-computersystem.md) | <span data-ttu-id="526ed-124">Solicita que o estado de replicação da máquina virtual seja alterado para o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="526ed-124">Requests that the replication state of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="526ed-125">Esse método só tem suporte para instâncias da classe **Msvm \_ ComputerSystem** que representam uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-125">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/> <span data-ttu-id="526ed-126">**Windows 8.1:** Não há suporte para este método até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="526ed-126">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="526ed-127">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="526ed-127">**RequestStateChange**</span></span>](requeststatechange-msvm-computersystem.md)                           | <span data-ttu-id="526ed-128">Solicita que o estado da máquina virtual seja alterado.</span><span class="sxs-lookup"><span data-stu-id="526ed-128">Requests that the state of the virtual machine be changed.</span></span> <span data-ttu-id="526ed-129">Esse método só tem suporte para instâncias da classe **Msvm \_ ComputerSystem** que representam uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-129">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="526ed-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="526ed-130">**SetPowerState**</span></span>                                                                              | <span data-ttu-id="526ed-131">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="526ed-131">This method is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                            |



 

### <a name="properties"></a><span data-ttu-id="526ed-132">Propriedades</span><span class="sxs-lookup"><span data-stu-id="526ed-132">Properties</span></span>

<span data-ttu-id="526ed-133">A classe **Msvm \_ ComputerSystem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="526ed-133">The **Msvm\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="526ed-134">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="526ed-134">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-135">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="526ed-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="526ed-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-137">Indica os valores possíveis para o parâmetro *requestedstate* do método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="526ed-137">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="526ed-138">Os valores listados serão um subconjunto dos valores contidos na propriedade **RequestedStatesSupported** da instância associada do **CIM \_ EnabledLogicalElementCapabilities**, em que os valores selecionados são uma função do estado atual do objeto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="526ed-138">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="526ed-139">Essa propriedade pode ser não **nula** se uma implementação for capaz de anunciar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="526ed-139">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="526ed-140">Essa propriedade será **nula** se uma implementação não puder determinar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="526ed-140">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="526ed-141">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="526ed-141">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="526ed-142"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="526ed-142"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="526ed-143"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="526ed-143"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="526ed-144"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="526ed-144"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="526ed-145"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="526ed-145"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="526ed-146"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="526ed-146"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="526ed-147"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="526ed-147"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="526ed-148"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="526ed-148"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="526ed-149"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="526ed-149"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="526ed-150"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="526ed-150"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="526ed-151"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="526ed-151"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="526ed-152">)</span><span class="sxs-lookup"><span data-stu-id="526ed-152">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="526ed-153">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="526ed-153">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-154">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="526ed-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-156">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="526ed-156">A short description of the object.</span></span> <span data-ttu-id="526ed-157">Essa propriedade é herdada da classe [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) e conterá um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="526ed-157">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class, and it will contain one of the following values.</span></span>



| <span data-ttu-id="526ed-158">Valor</span><span class="sxs-lookup"><span data-stu-id="526ed-158">Value</span></span>                                                                                                | <span data-ttu-id="526ed-159">Significado</span><span class="sxs-lookup"><span data-stu-id="526ed-159">Meaning</span></span>                                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="526ed-160"><dt>"Máquina virtual"</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-160"><dt>"Virtual Machine"</dt></span></span> </dl>         | <span data-ttu-id="526ed-161">A instância representa uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-161">The instance represents a virtual machine.</span></span><br/>    |
| <dl> <span data-ttu-id="526ed-162"><dt>"Sistema de computador de hospedagem"</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-162"><dt>"Hosting Computer System"</dt></span></span> </dl> | <span data-ttu-id="526ed-163">A instância representa o computador de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="526ed-163">The instance represents the hosting computer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="526ed-164">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="526ed-164">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-165">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="526ed-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-167">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="526ed-167">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="526ed-168">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="526ed-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="526ed-169">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="526ed-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="526ed-170">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="526ed-170">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-171">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="526ed-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-173">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="526ed-173">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="526ed-174">Essa propriedade é herdada [**do \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)e é sempre definida como "Msvm \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="526ed-174">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="526ed-175">**Dedicado**</span><span class="sxs-lookup"><span data-stu-id="526ed-175">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-176">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="526ed-176">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="526ed-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-178">Indica se o sistema de computador é um sistema de finalidade especial (dedicado a um uso específico), em vez de ser um sistema de finalidade geral.</span><span class="sxs-lookup"><span data-stu-id="526ed-178">Indicates whether the computer system is a special-purpose system (dedicated to a particular use), versus being a general-purpose system.</span></span> <span data-ttu-id="526ed-179">Essa propriedade é herdada do [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)e é sempre definida como 0 (não dedicada).</span><span class="sxs-lookup"><span data-stu-id="526ed-179">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 0 (Not Dedicated).</span></span>

</dd> <dt>

<span data-ttu-id="526ed-180">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="526ed-180">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-181">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="526ed-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-183">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="526ed-183">A description of the object.</span></span> <span data-ttu-id="526ed-184">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e conterá um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="526ed-184">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it will contain one of the following values.</span></span>



| <span data-ttu-id="526ed-185">Valor</span><span class="sxs-lookup"><span data-stu-id="526ed-185">Value</span></span>                                                                                                          | <span data-ttu-id="526ed-186">Significado</span><span class="sxs-lookup"><span data-stu-id="526ed-186">Meaning</span></span>                                                  |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="526ed-187"><dt>"Sistema de computador virtual da Microsoft"</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-187"><dt>"Microsoft Virtual Computer System"</dt></span></span> </dl> | <span data-ttu-id="526ed-188">A instância representa uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-188">The instance represents a virtual machine.</span></span><br/>    |
| <dl> <span data-ttu-id="526ed-189"><dt>"Sistema de computador de hospedagem da Microsoft"</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-189"><dt>"Microsoft Hosting Computer System"</dt></span></span> </dl> | <span data-ttu-id="526ed-190">A instância representa o computador de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="526ed-190">The instance represents the hosting computer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="526ed-191">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="526ed-191">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-192">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="526ed-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-194">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="526ed-194">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="526ed-195">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="526ed-195">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="526ed-196">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="526ed-196">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="526ed-197">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="526ed-197">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-198">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="526ed-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-200">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="526ed-200">A display name for the object.</span></span> <span data-ttu-id="526ed-201">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como o nome de exibição do computador para uma máquina virtual ou o nome NetBIOS do sistema operacional de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="526ed-201">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to the display name of the computer for a virtual machine or the NetBIOS name of the management operating system.</span></span>

</dd> <dt>

<span data-ttu-id="526ed-202">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="526ed-202">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-203">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="526ed-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-205">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="526ed-205">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="526ed-206">Essa propriedade é herdada de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="526ed-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="526ed-207"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="526ed-207"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="526ed-208"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="526ed-208"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="526ed-209"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Habilitado, mas offline** (6)</span><span class="sxs-lookup"><span data-stu-id="526ed-209"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="526ed-210">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="526ed-210">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-211">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="526ed-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-213">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="526ed-213">The enabled and disabled states of an element.</span></span> <span data-ttu-id="526ed-214">Essa propriedade também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="526ed-214">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="526ed-215">Essa propriedade é herdada da classe [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e é definida como 2 (habilitada) para um computador físico ou um dos valores a seguir para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-215">This property is inherited from the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class, and it is set to 2 (Enabled) for a physical computer or one of the following values for a virtual machine.</span></span> <span data-ttu-id="526ed-216">Para ver uma exibição gráfica desses Estados, consulte comentários.</span><span class="sxs-lookup"><span data-stu-id="526ed-216">For a graphical view of these states, see Remarks.</span></span>



| <span data-ttu-id="526ed-217">Valor</span><span class="sxs-lookup"><span data-stu-id="526ed-217">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="526ed-218">Significado</span><span class="sxs-lookup"><span data-stu-id="526ed-218">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="526ed-219"><dt></dt> <dt>0</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="526ed-219"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="526ed-220">Não foi possível determinar o estado do elemento.</span><span class="sxs-lookup"><span data-stu-id="526ed-220">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="526ed-221"><dt>**Outros**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-221"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="526ed-222"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-222"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="526ed-223">O elemento está em execução.</span><span class="sxs-lookup"><span data-stu-id="526ed-223">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="526ed-224"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-224"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="526ed-225">O elemento está desativado.</span><span class="sxs-lookup"><span data-stu-id="526ed-225">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="526ed-226"><dt>**Desligando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-226"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="526ed-227">O elemento está no processo de ir para um estado desabilitado.</span><span class="sxs-lookup"><span data-stu-id="526ed-227">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="526ed-228"><dt>**Não aplicável**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-228"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="526ed-229">O elemento não dá suporte a ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="526ed-229">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="526ed-230"><dt>**Habilitado, mas offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-230"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="526ed-231">O elemento pode estar concluindo comandos e removerá todas as novas solicitações.</span><span class="sxs-lookup"><span data-stu-id="526ed-231">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="526ed-232"><dt>**No teste**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-232"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="526ed-233">O elemento está em um estado de teste.</span><span class="sxs-lookup"><span data-stu-id="526ed-233">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="526ed-234"><dt>**Adiado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-234"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="526ed-235">O elemento pode estar concluindo comandos, mas colocará todas as novas solicitações na fila.</span><span class="sxs-lookup"><span data-stu-id="526ed-235">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="526ed-236"><dt>**Desativar**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-236"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="526ed-237">O elemento está habilitado, mas em um modo restrito.</span><span class="sxs-lookup"><span data-stu-id="526ed-237">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="526ed-238">O comportamento do elemento é semelhante ao estado habilitado (2), mas processa apenas um conjunto restrito de comandos.</span><span class="sxs-lookup"><span data-stu-id="526ed-238">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="526ed-239">Todas as outras solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="526ed-239">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="526ed-240"><dt>**Iniciando**</dt> em <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-240"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="526ed-241">O elemento está no processo de ir para um estado habilitado (2).</span><span class="sxs-lookup"><span data-stu-id="526ed-241">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="526ed-242">Novas solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="526ed-242">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="526ed-243">**EnhancedSessionModeState**</span><span class="sxs-lookup"><span data-stu-id="526ed-243">**EnhancedSessionModeState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-244">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="526ed-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-245">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-246">Especifica o estado atual do modo de sessão avançado na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-246">Specifies the current state of enhanced session mode on the virtual machine.</span></span>

<span data-ttu-id="526ed-247">O provedor WMI do Hyper-V gera um [**\_ \_ InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) cada vez que o **EnhancedSessionModeState** da classe **Msvm \_ ComputerSystem** é alterado.</span><span class="sxs-lookup"><span data-stu-id="526ed-247">The Hyper-V WMI provider raises an [**\_\_InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) each time the **EnhancedSessionModeState** of the **Msvm\_ComputerSystem** class changes.</span></span> <span data-ttu-id="526ed-248">Se uma sessão ativa do vmconnection receber um **\_ \_ InstanceModificationEvent**, ele tentará alternar para o modo de sessão avançado se o usuário tiver habilitado essa configuração.</span><span class="sxs-lookup"><span data-stu-id="526ed-248">If an active vmconnection session receives an **\_\_InstanceModificationEvent**, it attempts to switch to enhanced session mode if the user enabled that setting.</span></span>

<span data-ttu-id="526ed-249">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="526ed-249">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<span data-ttu-id="526ed-250">**EnhancedSessionModeState** pode ser um destes valores:</span><span class="sxs-lookup"><span data-stu-id="526ed-250">**EnhancedSessionModeState** can be one of these values:</span></span>

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span data-ttu-id="526ed-251"><span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>**Permitido e disponível** (2)</span><span class="sxs-lookup"><span data-stu-id="526ed-251"><span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>**Allowed and available** (2)</span></span>


</dt> <dd>

<span data-ttu-id="526ed-252">O modo avançado é permitido e está disponível na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-252">Enhanced mode is allowed and available on the virtual machine.</span></span>

</dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="526ed-253"><span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Não permitido** (3)</span><span class="sxs-lookup"><span data-stu-id="526ed-253"><span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Not allowed** (3)</span></span>


</dt> <dd>

<span data-ttu-id="526ed-254">O modo avançado não é permitido na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-254">Enhanced mode is not allowed on the virtual machine.</span></span>

</dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span data-ttu-id="526ed-255"><span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>**Permitido, mas não disponível** (6)</span><span class="sxs-lookup"><span data-stu-id="526ed-255"><span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>**Allowed but not available** (6)</span></span>


</dt> <dd>

<span data-ttu-id="526ed-256">O modo avançado é permitido e, porém, não está disponível na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-256">Enhanced mode is allowed and but not currently available on the virtual machine.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="526ed-257">**FailedOverReplicationType**</span><span class="sxs-lookup"><span data-stu-id="526ed-257">**FailedOverReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-258">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="526ed-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="526ed-260">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**FailedOverReplicationType**")</span><span class="sxs-lookup"><span data-stu-id="526ed-260">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**FailedOverReplicationType**")</span></span>
</dt> </dl>

<span data-ttu-id="526ed-261">O tipo de ponto de dados de recuperação que foi aplicado durante a operação de failover.</span><span class="sxs-lookup"><span data-stu-id="526ed-261">The type of recovery data point that was applied during the failover operation.</span></span>

> [!Note]  
> <span data-ttu-id="526ed-262">Esta propriedade foi preterida a partir de Windows 8.1; em vez disso, use a propriedade de mesmo nome na classe [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) para obter o valor para a relação primária ou estendida.</span><span class="sxs-lookup"><span data-stu-id="526ed-262">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="526ed-263">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="526ed-263">Possible values are:</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="526ed-264">**Nenhum** (0)</span><span class="sxs-lookup"><span data-stu-id="526ed-264">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="526ed-265">**Regular** (1)</span><span class="sxs-lookup"><span data-stu-id="526ed-265">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="526ed-266">**Consistente** com o aplicativo (2)</span><span class="sxs-lookup"><span data-stu-id="526ed-266">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="526ed-267">**Planejado** (3)</span><span class="sxs-lookup"><span data-stu-id="526ed-267">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="526ed-268">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="526ed-268">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-269">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="526ed-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-271">Especifica a integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="526ed-271">Specifies the current health of the element.</span></span> <span data-ttu-id="526ed-272">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="526ed-272">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="526ed-273">Quando ocorrer um erro crítico, verifique o log de eventos para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="526ed-273">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="526ed-274">A propriedade **enabledstate** também pode conter mais informações.</span><span class="sxs-lookup"><span data-stu-id="526ed-274">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="526ed-275">Por exemplo, quando o espaço em disco está muito baixo, o **HealthState** é definido como 25, a máquina virtual pausa e **enabledstate** é definido como 32768 (em pausa).</span><span class="sxs-lookup"><span data-stu-id="526ed-275">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="526ed-276">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="526ed-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="526ed-277">Valor</span><span class="sxs-lookup"><span data-stu-id="526ed-277">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="526ed-278">Significado</span><span class="sxs-lookup"><span data-stu-id="526ed-278">Meaning</span></span>                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="526ed-279"><dt>**OK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-279"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="526ed-280">A máquina virtual é totalmente funcional e está operando em parâmetros operacionais normais e sem erros.</span><span class="sxs-lookup"><span data-stu-id="526ed-280">The virtual machine is fully functional and is operating within normal operational parameters and without error.</span></span><br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="526ed-281"><dt>**Maior falha**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-281"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="526ed-282">A máquina virtual sofreu uma falha grave.</span><span class="sxs-lookup"><span data-stu-id="526ed-282">The virtual machine has suffered a major failure.</span></span> <span data-ttu-id="526ed-283">Esse valor é usado quando um ou mais discos que contêm VHDs da máquina virtual estão com pouco espaço em disco e a máquina virtual foi pausada.</span><span class="sxs-lookup"><span data-stu-id="526ed-283">This value is used when one or more disks that contain the virtual machine's VHDs is low on disk space and the virtual machine has been paused.</span></span><br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="526ed-284"><dt>**Falha crítica**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-284"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="526ed-285">O elemento não é funcional e a recuperação pode não ser possível.</span><span class="sxs-lookup"><span data-stu-id="526ed-285">The element is nonfunctional, and recovery might not be possible.</span></span> <span data-ttu-id="526ed-286">Isso pode indicar que o processo de trabalho para a máquina virtual (Vmwp.exe) não está respondendo às solicitações de controle ou de informações, ou que um ou mais discos que contêm VHDs para a máquina virtual estão com pouco espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="526ed-286">This can indicate that the worker process for the virtual machine (Vmwp.exe) is not responding to control or information requests, or that one or more disks that contain the VHDs for the virtual machine are low on disk space.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="526ed-287">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="526ed-287">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-288">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="526ed-288">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="526ed-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-290">Essa propriedade é herdada do [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="526ed-290">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="526ed-291">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="526ed-291">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-292">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="526ed-292">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-293">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-294">A data e a hora em que a configuração de máquina virtual foi criada para uma máquina virtual, ou **nula**, para um sistema operacional de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="526ed-294">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="526ed-295">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="526ed-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="526ed-296">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="526ed-296">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-297">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="526ed-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="526ed-299">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="526ed-299">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="526ed-300">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="526ed-300">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="526ed-301">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="526ed-301">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="526ed-302">No Windows 8, há uma única instância de [**ReplicationSettingData**](msvm-replicationsettingdata.md) para cada sistema de computador ou máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-302">In Windows 8, there is a single instance of [**ReplicationSettingData**](msvm-replicationsettingdata.md) for every computer system or virtual machine.</span></span> <span data-ttu-id="526ed-303">Por Windows 8.1, uma máquina virtual de recuperação tem duas instâncias de **ReplicationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="526ed-303">For Windows 8.1, a recovery virtual machine has two instances of **ReplicationSettingData**.</span></span> <span data-ttu-id="526ed-304">Essa alteração diferencia e associa dados de configuração com relação de replicação.</span><span class="sxs-lookup"><span data-stu-id="526ed-304">This change differentiates and associates setting data with replication relationship.</span></span>



| <span data-ttu-id="526ed-305">Nome da propriedade</span><span class="sxs-lookup"><span data-stu-id="526ed-305">Property name</span></span>  | <span data-ttu-id="526ed-306">Valor do Windows 8</span><span class="sxs-lookup"><span data-stu-id="526ed-306">Windows 8 value</span></span>               | <span data-ttu-id="526ed-307">Valor Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="526ed-307">Windows 8.1 value</span></span>                          |
|----------------|-------------------------------|--------------------------------------------|
| <span data-ttu-id="526ed-308">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="526ed-308">**InstanceID**</span></span> | <span data-ttu-id="526ed-309">Microsoft: <vmguid> \\ HVR</span><span class="sxs-lookup"><span data-stu-id="526ed-309">Microsoft:<vmguid>\\HVR</span></span> | <span data-ttu-id="526ed-310">Microsoft: <vmguid> \\ HVR \\<0/1></span><span class="sxs-lookup"><span data-stu-id="526ed-310">Microsoft:<vmguid>\\HVR\\<0/1></span></span> |



 

<span data-ttu-id="526ed-311">No Windows 8.1 valor, 0 indica primário e 1 indica replicação estendida.</span><span class="sxs-lookup"><span data-stu-id="526ed-311">In the Windows 8.1 value, 0 indicates primary and 1 indicates extended replication.</span></span> <span data-ttu-id="526ed-312">Para obter mais informações sobre a replicação estendida, consulte [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).</span><span class="sxs-lookup"><span data-stu-id="526ed-312">For more info about extended replication, see [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).</span></span>

</dd> <dt>

<span data-ttu-id="526ed-313">**LastApplicationConsistentReplicationTime**</span><span class="sxs-lookup"><span data-stu-id="526ed-313">**LastApplicationConsistentReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-314">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="526ed-314">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-315">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="526ed-316">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastApplicationConsistentReplicationTime**")</span><span class="sxs-lookup"><span data-stu-id="526ed-316">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**LastApplicationConsistentReplicationTime**")</span></span>
</dt> </dl>

<span data-ttu-id="526ed-317">A hora em que a última replicação consistente com o aplicativo foi recebida para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-317">The time at which the last application-consistent replication was received for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="526ed-318">Esta propriedade foi preterida a partir de Windows 8.1; em vez disso, use a propriedade de mesmo nome na classe [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) para obter o valor para a relação primária ou estendida.</span><span class="sxs-lookup"><span data-stu-id="526ed-318">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

</dd> <dt>

<span data-ttu-id="526ed-319">**LastReplicationTime**</span><span class="sxs-lookup"><span data-stu-id="526ed-319">**LastReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-320">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="526ed-320">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="526ed-322">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationTime**")</span><span class="sxs-lookup"><span data-stu-id="526ed-322">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationTime**")</span></span>
</dt> </dl>

<span data-ttu-id="526ed-323">A hora em que a última replicação é recebida na recuperação para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-323">The time at which the last replication is received on recovery for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="526ed-324">Esta propriedade foi preterida a partir de Windows 8.1; em vez disso, use a propriedade de mesmo nome na classe [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) para obter o valor para a relação primária ou estendida.</span><span class="sxs-lookup"><span data-stu-id="526ed-324">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

</dd> <dt>

<span data-ttu-id="526ed-325">**LastReplicationType**</span><span class="sxs-lookup"><span data-stu-id="526ed-325">**LastReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-326">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="526ed-326">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="526ed-328">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationType**")</span><span class="sxs-lookup"><span data-stu-id="526ed-328">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationType**")</span></span>
</dt> </dl>

<span data-ttu-id="526ed-329">O tipo da última replicação que foi recebida para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-329">The type of the last replication that was received for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="526ed-330">Esta propriedade foi preterida a partir de Windows 8.1; em vez disso, use a propriedade de mesmo nome na classe [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) para obter o valor para a relação primária ou estendida.</span><span class="sxs-lookup"><span data-stu-id="526ed-330">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="526ed-331">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="526ed-331">Possible values are:</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="526ed-332">**Nenhum** (0)</span><span class="sxs-lookup"><span data-stu-id="526ed-332">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="526ed-333">**Regular** (1)</span><span class="sxs-lookup"><span data-stu-id="526ed-333">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="526ed-334">**Consistente** com o aplicativo (2)</span><span class="sxs-lookup"><span data-stu-id="526ed-334">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="526ed-335">**Planejado** (3)</span><span class="sxs-lookup"><span data-stu-id="526ed-335">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="526ed-336">**LastSuccessfulBackupTime**</span><span class="sxs-lookup"><span data-stu-id="526ed-336">**LastSuccessfulBackupTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-337">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="526ed-337">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-338">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-339">A hora em que o último backup bem-sucedido foi concluído para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-339">The time at which the last successful backup has completed for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="526ed-340">**Nome**</span><span class="sxs-lookup"><span data-stu-id="526ed-340">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-341">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="526ed-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-342">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-343">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="526ed-343">The label by which the object is known.</span></span> <span data-ttu-id="526ed-344">Essa propriedade é herdada [**do \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)e é sempre definida como "*GUID*".</span><span class="sxs-lookup"><span data-stu-id="526ed-344">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="526ed-345">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="526ed-345">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-346">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="526ed-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-348">Uma cadeia de caracteres que identifica como o nome do sistema foi gerado, usando a heurística de subclasse.</span><span class="sxs-lookup"><span data-stu-id="526ed-348">A string that identifies how the system name was generated, using the subclass heuristic.</span></span> <span data-ttu-id="526ed-349">Essa propriedade é herdada do [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="526ed-349">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="526ed-350">**NumberOfNumaNodes**</span><span class="sxs-lookup"><span data-stu-id="526ed-350">**NumberOfNumaNodes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-351">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="526ed-351">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-352">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-353">O número de nós NUMA (acesso não uniforme à memória) do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="526ed-353">The number of nonuniform memory access (NUMA) nodes of the computer system.</span></span> <span data-ttu-id="526ed-354">Quando o **Msvm \_ ComputerSystem** representa o sistema de computador de hospedagem, essa propriedade contém a contagem de nós numa físicos.</span><span class="sxs-lookup"><span data-stu-id="526ed-354">When **Msvm\_ComputerSystem** represents the hosting computer system, this property contains the count of physical NUMA nodes.</span></span> <span data-ttu-id="526ed-355">Quando o **Msvm \_ ComputerSystem** representa uma máquina virtual, essa propriedade contém o número de nós numa virtuais que são apresentados ao sistema operacional convidado por meio da SRAT (tabela de afinidade de recursos do sistema) do ACPI.</span><span class="sxs-lookup"><span data-stu-id="526ed-355">When **Msvm\_ComputerSystem** represents a virtual machine, this property contains the number of virtual NUMA nodes that are presented to the guest operating system through the ACPI System Resource Affinity Table (SRAT).</span></span>

</dd> <dt>

<span data-ttu-id="526ed-356">**OnTimeInMilliseconds**</span><span class="sxs-lookup"><span data-stu-id="526ed-356">**OnTimeInMilliseconds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-357">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="526ed-357">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-358">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="526ed-359">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milissegundos")</span><span class="sxs-lookup"><span data-stu-id="526ed-359">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds")</span></span>
</dt> </dl>

<span data-ttu-id="526ed-360">Para a máquina virtual, essa propriedade indica o tempo, em milissegundos, desde a última vez em que a máquina foi ativada, redefinida ou restaurada.</span><span class="sxs-lookup"><span data-stu-id="526ed-360">For the virtual machine, this property indicates the time, in milliseconds, since the machine was last turned on, reset, or restored.</span></span> <span data-ttu-id="526ed-361">Esse tempo exclui a hora em que a máquina virtual estava no estado em pausa.</span><span class="sxs-lookup"><span data-stu-id="526ed-361">This time excludes the time the virtual machine was in the paused state.</span></span> <span data-ttu-id="526ed-362">Para o sistema operacional de gerenciamento, essa propriedade é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="526ed-362">For the management operating system, this property is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="526ed-363">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="526ed-363">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-364">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="526ed-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-365">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-366">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="526ed-366">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="526ed-367">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="526ed-367">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="526ed-368">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="526ed-368">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="526ed-369">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="526ed-369">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-370">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="526ed-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="526ed-371">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-372">Uma matriz que contém os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="526ed-372">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="526ed-373">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="526ed-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="526ed-374">O valor no índice zero (0) é um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="526ed-374">The value at index zero (0) is one of the following values.</span></span>



| <span data-ttu-id="526ed-375">Valor</span><span class="sxs-lookup"><span data-stu-id="526ed-375">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="526ed-376">Significado</span><span class="sxs-lookup"><span data-stu-id="526ed-376">Meaning</span></span>                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="526ed-377"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-377"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                      | <span data-ttu-id="526ed-378">A máquina virtual está funcional e funcionando normalmente.</span><span class="sxs-lookup"><span data-stu-id="526ed-378">The virtual machine is functional and operating normally.</span></span><br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="526ed-379"><dt>**Degradado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-379"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                         | <span data-ttu-id="526ed-380">A máquina virtual só está parcialmente funcional.</span><span class="sxs-lookup"><span data-stu-id="526ed-380">The virtual machine is only partially functional.</span></span> <span data-ttu-id="526ed-381">Isso indica que o armazenamento que contém a configuração não está acessível.</span><span class="sxs-lookup"><span data-stu-id="526ed-381">This indicates that the storage that contains the configuration is not accessible.</span></span> <span data-ttu-id="526ed-382">Uma máquina virtual nesse estado só pode ser desativada ou excluída.</span><span class="sxs-lookup"><span data-stu-id="526ed-382">A virtual machine in this state can only be turned off or deleted.</span></span> <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <span data-ttu-id="526ed-383"><dt>**Falha preditiva**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-383"><dt>**Predictive Failure**</dt> <dt>5</dt></span></span> </dl> | <span data-ttu-id="526ed-384">A máquina virtual é funcional, mas pode falhar no futuro.</span><span class="sxs-lookup"><span data-stu-id="526ed-384">The virtual machine is functional but may fail in the future.</span></span> <span data-ttu-id="526ed-385">Isso indica que o armazenamento que contém o disco rígido virtual da máquina virtual está com pouco espaço livre.</span><span class="sxs-lookup"><span data-stu-id="526ed-385">This indicates that the storage that contains the virtual machine's virtual hard disk is low on free space.</span></span> <span data-ttu-id="526ed-386">A máquina virtual será pausada se mais espaço em disco não for disponibilizado.</span><span class="sxs-lookup"><span data-stu-id="526ed-386">The virtual machine will be paused if more disk space is not made available.</span></span><br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <span data-ttu-id="526ed-387"><dt>**Parado**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-387"><dt>**Stopped**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="526ed-388">Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="526ed-388">This value is not supported.</span></span> <span data-ttu-id="526ed-389">Se a máquina virtual for interrompida, a propriedade **enabledstate** terá um valor de 3 (desabilitado).</span><span class="sxs-lookup"><span data-stu-id="526ed-389">If the virtual machine is stopped, the **EnabledState** property will have a value of 3 (Disabled).</span></span><br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <span data-ttu-id="526ed-390"><dt>**No serviço**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-390"><dt>**In Service**</dt> <dt>11</dt></span></span> </dl>                                | <span data-ttu-id="526ed-391">A máquina virtual está processando uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="526ed-391">The virtual machine is processing a request.</span></span><br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <span data-ttu-id="526ed-392"><dt>15</dt> <dt>**inativos**</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-392"><dt>**Dormant**</dt> <dt>15</dt></span></span> </dl>                                            | <span data-ttu-id="526ed-393">Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="526ed-393">This value is not supported.</span></span> <span data-ttu-id="526ed-394">Se a máquina virtual for suspensa ou pausada, a propriedade **enabledstate** terá um valor de 32769 (suspenso) ou 32768 (em pausa).</span><span class="sxs-lookup"><span data-stu-id="526ed-394">If the virtual machine is suspended or paused, the **EnabledState** property will have a value of 32769 (Suspended) or 32768 (Paused).</span></span><br/>                                                                                    |



 

<span data-ttu-id="526ed-395">O valor no índice one (1) é opcional e contém informações de status secundárias.</span><span class="sxs-lookup"><span data-stu-id="526ed-395">The value at index one (1) is optional and contains secondary status information.</span></span> <span data-ttu-id="526ed-396">Um cliente deve usar o status principal do índice zero (0) para determinar se uma nova solicitação pode ser emitida para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-396">A client should use the primary status from index zero (0) to determine whether a new request can be issued to the virtual machine.</span></span> <span data-ttu-id="526ed-397">Se **OperationalStatus** \[ 0 \] for 2 (OK), a operação indicada por **OperationalStatus** \[ 1 \] poderá ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="526ed-397">If **OperationalStatus**\[0\] is 2 (OK), then the operation indicated by **OperationalStatus**\[1\] can be interrupted.</span></span>

<span data-ttu-id="526ed-398">O valor em **OperationalStatus** \[ 1 \] é um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="526ed-398">The value at **OperationalStatus**\[1\] is one of the following values.</span></span>



| <span data-ttu-id="526ed-399">Valor</span><span class="sxs-lookup"><span data-stu-id="526ed-399">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="526ed-400">Significado</span><span class="sxs-lookup"><span data-stu-id="526ed-400">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <span data-ttu-id="526ed-401"><dt>**Criando o instantâneo**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-401"><dt>**Creating Snapshot**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="526ed-402">Um instantâneo está em processo de criação para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-402">A snapshot is in the process of being created for the virtual machine.</span></span><br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <span data-ttu-id="526ed-403"><dt>**Aplicando o instantâneo**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-403"><dt>**Applying Snapshot**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="526ed-404">Um instantâneo está no processo de ser aplicado à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-404">A snapshot is in the process of being applied to the virtual machine.</span></span><br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <span data-ttu-id="526ed-405"><dt>**Excluindo o instantâneo**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-405"><dt>**Deleting Snapshot**</dt> <dt>32770</dt></span></span> </dl>                                 | <span data-ttu-id="526ed-406">Um instantâneo está no processo de ser excluído da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-406">A snapshot is in the process of being deleted from the virtual machine.</span></span><br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <span data-ttu-id="526ed-407"><dt>**Aguardando para iniciar**</dt> o <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-407"><dt>**Waiting to Start**</dt> <dt>32771</dt></span></span> </dl>                                     | <span data-ttu-id="526ed-408">A máquina virtual será iniciada depois que o atraso de inicialização automática tiver decorrido.</span><span class="sxs-lookup"><span data-stu-id="526ed-408">The virtual machine will be started after the automatic startup delay has elapsed.</span></span><br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <span data-ttu-id="526ed-409"><dt>**Mesclando discos**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-409"><dt>**Merging Disks**</dt> <dt>32772</dt></span></span> </dl>                                                 | <span data-ttu-id="526ed-410">Os discos rígidos virtuais dos instantâneos excluídos anteriormente estão sendo mesclados.</span><span class="sxs-lookup"><span data-stu-id="526ed-410">Virtual hard disks from previously deleted snapshots are being merged.</span></span><br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="526ed-411"><dt>**Exportando a máquina Virtual**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-411"><dt>**Exporting Virtual Machine**</dt> <dt>32773</dt></span></span> </dl> | <span data-ttu-id="526ed-412">A máquina virtual está sendo exportada.</span><span class="sxs-lookup"><span data-stu-id="526ed-412">The virtual machine is being exported.</span></span><br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="526ed-413"><dt>**Migrando a máquina Virtual**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-413"><dt>**Migrating Virtual Machine**</dt> <dt>32774</dt></span></span> </dl> | <span data-ttu-id="526ed-414">A máquina virtual está sendo migrada ao vivo de um computador físico para outro.</span><span class="sxs-lookup"><span data-stu-id="526ed-414">The virtual machine is being migrated live from one physical computer to another.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="526ed-415">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="526ed-415">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-416">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="526ed-416">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="526ed-417">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-418">Uma cadeia de caracteres que descreve como ou por que o sistema é dedicado quando a matriz **dedicada** inclui o valor 2 (outro).</span><span class="sxs-lookup"><span data-stu-id="526ed-418">A string that describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span> <span data-ttu-id="526ed-419">Essa propriedade é herdada do [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="526ed-419">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="526ed-420">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="526ed-420">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-421">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="526ed-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-422">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-423">O estado habilitado ou desabilitado da máquina virtual quando a propriedade **enabledstate** é definida como 1 (Other).</span><span class="sxs-lookup"><span data-stu-id="526ed-423">The enabled or disabled state of the virtual machine when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="526ed-424">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="526ed-424">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="526ed-425">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="526ed-425">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="526ed-426">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="526ed-426">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-427">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="526ed-427">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="526ed-428">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-429">Essa propriedade é herdada do [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="526ed-429">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="526ed-430">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="526ed-430">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-431">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="526ed-431">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="526ed-432">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-433">Essa propriedade é herdada do [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="526ed-433">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="526ed-434">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="526ed-434">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-435">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="526ed-435">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-436">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-437">Uma cadeia de caracteres que indica como o proprietário do sistema primário pode ser alcançado (por exemplo, um número de telefone ou um endereço de email).</span><span class="sxs-lookup"><span data-stu-id="526ed-437">A string that indicates how the primary system owner can be reached (for example, a phone number or an email address).</span></span> <span data-ttu-id="526ed-438">Essa propriedade é herdada [**do \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="526ed-438">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="526ed-439">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="526ed-439">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-440">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="526ed-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-441">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-442">O nome do proprietário do sistema primário.</span><span class="sxs-lookup"><span data-stu-id="526ed-442">The name of the primary system owner.</span></span> <span data-ttu-id="526ed-443">Essa propriedade é herdada [**do \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="526ed-443">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="526ed-444">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="526ed-444">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-445">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="526ed-445">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-446">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-447">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="526ed-447">Provides high level status information.</span></span> <span data-ttu-id="526ed-448">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer informações de status de integridade detalhadas e de alto nível para o elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="526ed-448">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="526ed-449">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="526ed-449">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="526ed-450">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="526ed-450">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="526ed-451">**ProcessID**</span><span class="sxs-lookup"><span data-stu-id="526ed-451">**ProcessID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-452">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="526ed-452">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-453">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-454">O identificador do processo no qual esta máquina virtual está em execução.</span><span class="sxs-lookup"><span data-stu-id="526ed-454">The identifier of the process under which this virtual machine is running.</span></span> <span data-ttu-id="526ed-455">Esse valor pode ser usado para identificar exclusivamente a instância do Vmwp.exe no sistema que está executando a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-455">This value can be used to uniquely identify the instance of Vmwp.exe on the system that is running the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="526ed-456">**ReplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="526ed-456">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-457">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="526ed-457">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-458">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="526ed-459">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationHealth**")</span><span class="sxs-lookup"><span data-stu-id="526ed-459">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationHealth**")</span></span>
</dt> </dl>

<span data-ttu-id="526ed-460">A integridade da replicação para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-460">The replication health for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="526ed-461">Esta propriedade foi preterida a partir de Windows 8.1; em vez disso, use a propriedade de mesmo nome na classe [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) para obter o valor para a relação primária ou estendida.</span><span class="sxs-lookup"><span data-stu-id="526ed-461">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="526ed-462">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="526ed-462">Possible values are:</span></span>

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="526ed-463">**Não aplicável** (0)</span><span class="sxs-lookup"><span data-stu-id="526ed-463">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="526ed-464">**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="526ed-464">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="526ed-465">**Aviso** (2)</span><span class="sxs-lookup"><span data-stu-id="526ed-465">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="526ed-466">**Crítico** (3)</span><span class="sxs-lookup"><span data-stu-id="526ed-466">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="526ed-467">**ReplicationMode**</span><span class="sxs-lookup"><span data-stu-id="526ed-467">**ReplicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-468">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="526ed-468">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-469">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-470">Especifica o modo de replicação para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-470">Specifies the replication mode for the virtual machine.</span></span> <span data-ttu-id="526ed-471">Esse será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="526ed-471">This will be one of the following values.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="526ed-472"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Nenhum** (0)</span><span class="sxs-lookup"><span data-stu-id="526ed-472"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="526ed-473"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primário** (1)</span><span class="sxs-lookup"><span data-stu-id="526ed-473"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primary** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span data-ttu-id="526ed-474"><span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>**Réplica** (2)</span><span class="sxs-lookup"><span data-stu-id="526ed-474"><span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>**Replica** (2)</span></span>


</dt> <dd>

<span data-ttu-id="526ed-475">Recuperação</span><span class="sxs-lookup"><span data-stu-id="526ed-475">Recovery</span></span>

</dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span data-ttu-id="526ed-476"><span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>**Réplica de teste** (3)</span><span class="sxs-lookup"><span data-stu-id="526ed-476"><span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>**Test Replica** (3)</span></span>


</dt> <dd>

<span data-ttu-id="526ed-477">Réplica</span><span class="sxs-lookup"><span data-stu-id="526ed-477">Replica</span></span>

</dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

<span data-ttu-id="526ed-478"><span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>**Réplica estendida** (4)</span><span class="sxs-lookup"><span data-stu-id="526ed-478"><span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>**Extended Replica** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="526ed-479">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="526ed-479">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-480">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="526ed-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-481">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="526ed-482">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**Replicationstate**")</span><span class="sxs-lookup"><span data-stu-id="526ed-482">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationState**")</span></span>
</dt> </dl>

<span data-ttu-id="526ed-483">O estado de replicação para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-483">The replication state for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="526ed-484">Esta propriedade foi preterida a partir de Windows 8.1; em vez disso, use a propriedade de mesmo nome na classe [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) para obter o valor para a relação primária ou estendida.</span><span class="sxs-lookup"><span data-stu-id="526ed-484">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="526ed-485">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="526ed-485">Possible values are:</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="526ed-486">**Desabilitado** (0)</span><span class="sxs-lookup"><span data-stu-id="526ed-486">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="526ed-487">**Pronto para replicação** (1)</span><span class="sxs-lookup"><span data-stu-id="526ed-487">**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="526ed-488">**Aguardando para concluir a replicação inicial** (2)</span><span class="sxs-lookup"><span data-stu-id="526ed-488">**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="526ed-489">**Replicando** (3)</span><span class="sxs-lookup"><span data-stu-id="526ed-489">**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="526ed-490">**Replicação sincronizada concluída** (4)</span><span class="sxs-lookup"><span data-stu-id="526ed-490">**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="526ed-491">**Recuperado** (5)</span><span class="sxs-lookup"><span data-stu-id="526ed-491">**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="526ed-492">**Confirmado** (6)</span><span class="sxs-lookup"><span data-stu-id="526ed-492">**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="526ed-493">**Suspenso** (7)</span><span class="sxs-lookup"><span data-stu-id="526ed-493">**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="526ed-494">**Crítico** (8)</span><span class="sxs-lookup"><span data-stu-id="526ed-494">**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="526ed-495">**Aguardando para iniciar a ressincronização** (9)</span><span class="sxs-lookup"><span data-stu-id="526ed-495">**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="526ed-496">**Ressincronização** (10)</span><span class="sxs-lookup"><span data-stu-id="526ed-496">**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="526ed-497">**Ressincronização suspensa** (11)</span><span class="sxs-lookup"><span data-stu-id="526ed-497">**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="526ed-498">**Failover em andamento** (12)</span><span class="sxs-lookup"><span data-stu-id="526ed-498">**Failover in progress** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span data-ttu-id="526ed-499">**Failback em andamento** (13)</span><span class="sxs-lookup"><span data-stu-id="526ed-499">**Failback in progress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span data-ttu-id="526ed-500">**Failback concluído** (14)</span><span class="sxs-lookup"><span data-stu-id="526ed-500">**Failback complete** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="526ed-501">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="526ed-501">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-502">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="526ed-502">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-503">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-503">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-504">O último estado solicitado ou desejado para a máquina virtual, conforme passado para o método [**RequestStateChange**](requeststatechange-msvm-computersystem.md) , ou 12 (não aplicável) se nenhuma alteração de estado estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="526ed-504">The last requested or desired state for the virtual machine as passed to the [**RequestStateChange**](requeststatechange-msvm-computersystem.md) method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="526ed-505">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="526ed-505">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="526ed-506">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="526ed-506">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="526ed-507">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="526ed-507">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="526ed-508">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="526ed-508">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-509">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="526ed-509">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-510">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-511">Essa propriedade é herdada do [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)e é sempre definida como 1 (outra).</span><span class="sxs-lookup"><span data-stu-id="526ed-511">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="526ed-512">**Funções**</span><span class="sxs-lookup"><span data-stu-id="526ed-512">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-513">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="526ed-513">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="526ed-514">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-515">Uma matriz de cadeias de caracteres que descreve as funções que o sistema desempenha no ambiente de tecnologia da informação.</span><span class="sxs-lookup"><span data-stu-id="526ed-515">An array of strings that describe the roles the system plays in the information technology environment.</span></span> <span data-ttu-id="526ed-516">Essa propriedade é herdada [**do \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="526ed-516">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="526ed-517">**Status**</span><span class="sxs-lookup"><span data-stu-id="526ed-517">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-518">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="526ed-518">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-519">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-520">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="526ed-520">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="526ed-521">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="526ed-521">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-522">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="526ed-522">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="526ed-523">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-523">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="526ed-524">Qualificadores: **ArrayType** ("indexado")</span><span class="sxs-lookup"><span data-stu-id="526ed-524">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="526ed-525">Uma matriz que contém cadeias de caracteres que descrevem os valores correspondentes da matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="526ed-525">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="526ed-526">Por exemplo, se 11 (em serviço) for o valor atribuído a **OperationalStatus** \[ 0 \] , **StatusDescriptions** \[ 0 \] poderá conter uma explicação sobre o motivo pelo qual a máquina virtual está processando uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="526ed-526">For example, if 11 (In Service) is the value assigned to **OperationalStatus**\[0\], then **StatusDescriptions**\[0\] may contain an explanation as to why the virtual machine is processing a request.</span></span> <span data-ttu-id="526ed-527">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="526ed-527">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="526ed-528">**TimeOfLastConfigurationChange**</span><span class="sxs-lookup"><span data-stu-id="526ed-528">**TimeOfLastConfigurationChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-529">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="526ed-529">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-530">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-531">A data e a hora da última modificação do arquivo de configuração da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="526ed-531">The date and time when the virtual machine configuration file was last modified.</span></span> <span data-ttu-id="526ed-532">O arquivo de configuração é modificado durante determinadas operações de máquina virtual, bem como quando qualquer uma das configurações da máquina virtual ou do dispositivo é adicionada, modificada ou removida.</span><span class="sxs-lookup"><span data-stu-id="526ed-532">The configuration file is modified during certain virtual machine operations, as well as when any of the virtual machine or device settings are added, modified, or removed.</span></span>

</dd> <dt>

<span data-ttu-id="526ed-533">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="526ed-533">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-534">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="526ed-534">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-535">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-535">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-536">A data e a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="526ed-536">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="526ed-537">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="526ed-537">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="526ed-538">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="526ed-538">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="526ed-539">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="526ed-539">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="526ed-540">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="526ed-540">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="526ed-541">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="526ed-541">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="526ed-542">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="526ed-542">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="526ed-543">Comentários</span><span class="sxs-lookup"><span data-stu-id="526ed-543">Remarks</span></span>

<span data-ttu-id="526ed-544">A ilustração a seguir mostra os valores **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="526ed-544">The following illustration shows the **EnabledState** values.</span></span>

![diagrama de estado dos valores enabledstate para o Windows Server 2008 R2](images/msvm-computersystem-enabledstate-win2008r2.png)

<span data-ttu-id="526ed-546">Quando uma propriedade da classe **Msvm \_ ComputerSystem** é alterada, o provedor WMI indica um evento [**\_ \_ InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) que descreve as alterações.</span><span class="sxs-lookup"><span data-stu-id="526ed-546">When a property of the **Msvm\_ComputerSystem** class changes, the WMI provider indicates an [**\_\_InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) event that describes the changes.</span></span> <span data-ttu-id="526ed-547">O estado anterior está contido na propriedade **PreviousInstance** e o novo estado está contido na propriedade **TargetInstance** .</span><span class="sxs-lookup"><span data-stu-id="526ed-547">The previous state is contained in the **PreviousInstance** property, and the new state is contained in the **TargetInstance** property.</span></span> <span data-ttu-id="526ed-548">Esse evento é assíncrono; no momento em que o evento **\_ \_ InstanceModificationEvent** é processado, a propriedade **TargetInstance** pode não refletir o estado atual.</span><span class="sxs-lookup"><span data-stu-id="526ed-548">This event is asynchronous; by the time the **\_\_InstanceModificationEvent** event is processed, the **TargetInstance** property may not reflect the current state.</span></span>

<span data-ttu-id="526ed-549">O acesso à classe de **\_ ComputerSystem Msvm** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="526ed-549">Access to the **Msvm\_ComputerSystem** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="526ed-550">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="526ed-550">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="526ed-551">Exemplos</span><span class="sxs-lookup"><span data-stu-id="526ed-551">Examples</span></span>

<span data-ttu-id="526ed-552">Consulte [consultando objetos de rede](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="526ed-552">See [Querying Networking Objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="526ed-553">Requisitos</span><span class="sxs-lookup"><span data-stu-id="526ed-553">Requirements</span></span>



| <span data-ttu-id="526ed-554">Requisito</span><span class="sxs-lookup"><span data-stu-id="526ed-554">Requirement</span></span> | <span data-ttu-id="526ed-555">Valor</span><span class="sxs-lookup"><span data-stu-id="526ed-555">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="526ed-556">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="526ed-556">Minimum supported client</span></span><br/> | <span data-ttu-id="526ed-557">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="526ed-557">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="526ed-558">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="526ed-558">Minimum supported server</span></span><br/> | <span data-ttu-id="526ed-559">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="526ed-559">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="526ed-560">Namespace</span><span class="sxs-lookup"><span data-stu-id="526ed-560">Namespace</span></span><br/>                | <span data-ttu-id="526ed-561">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="526ed-561">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="526ed-562">MOF</span><span class="sxs-lookup"><span data-stu-id="526ed-562">MOF</span></span><br/>                      | <dl> <span data-ttu-id="526ed-563"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-563"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="526ed-564">DLL</span><span class="sxs-lookup"><span data-stu-id="526ed-564">DLL</span></span><br/>                      | <dl> <span data-ttu-id="526ed-565"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="526ed-565"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="526ed-566">Confira também</span><span class="sxs-lookup"><span data-stu-id="526ed-566">See also</span></span>

<dl> <dt>

[<span data-ttu-id="526ed-567">**\_Sistema de COMPUTERSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="526ed-567">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> <dt>

[<span data-ttu-id="526ed-568">**\_\_InstanceModificationEvent**</span><span class="sxs-lookup"><span data-stu-id="526ed-568">**\_\_InstanceModificationEvent**</span></span>](/windows/desktop/WmiSdk/--instancemodificationevent)
</dt> <dt>

[<span data-ttu-id="526ed-569">**\_Sistema de COMPUTERSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="526ed-569">**CIM\_ComputerSystem**</span></span>](/windows/desktop/CIMWin32Prov/cim-computersystem)
</dt> <dt>

[<span data-ttu-id="526ed-570">**Msvm \_ ComputerSystem (v1)**</span><span class="sxs-lookup"><span data-stu-id="526ed-570">**Msvm\_ComputerSystem (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-computersystem)
</dt> <dt>

[<span data-ttu-id="526ed-571">Classes de sistema virtual</span><span class="sxs-lookup"><span data-stu-id="526ed-571">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

