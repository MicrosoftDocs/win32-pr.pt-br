---
description: Representa uma máquina virtual planejada.
ms.assetid: 4ce6d34c-66fb-4f4f-bf52-26d19bab6d4a
title: Classe Msvm_PlannedComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PlannedComputerSystem
- Msvm_PlannedComputerSystem.SetPowerState
- Msvm_PlannedComputerSystem.InstanceID
- Msvm_PlannedComputerSystem.Caption
- Msvm_PlannedComputerSystem.Description
- Msvm_PlannedComputerSystem.ElementName
- Msvm_PlannedComputerSystem.InstallDate
- Msvm_PlannedComputerSystem.OperationalStatus
- Msvm_PlannedComputerSystem.StatusDescriptions
- Msvm_PlannedComputerSystem.Status
- Msvm_PlannedComputerSystem.HealthState
- Msvm_PlannedComputerSystem.CommunicationStatus
- Msvm_PlannedComputerSystem.DetailedStatus
- Msvm_PlannedComputerSystem.OperatingStatus
- Msvm_PlannedComputerSystem.PrimaryStatus
- Msvm_PlannedComputerSystem.EnabledState
- Msvm_PlannedComputerSystem.OtherEnabledState
- Msvm_PlannedComputerSystem.RequestedState
- Msvm_PlannedComputerSystem.EnabledDefault
- Msvm_PlannedComputerSystem.TimeOfLastStateChange
- Msvm_PlannedComputerSystem.AvailableRequestedStates
- Msvm_PlannedComputerSystem.TransitioningToState
- Msvm_PlannedComputerSystem.CreationClassName
- Msvm_PlannedComputerSystem.Name
- Msvm_PlannedComputerSystem.NameFormat
- Msvm_PlannedComputerSystem.PrimaryOwnerName
- Msvm_PlannedComputerSystem.PrimaryOwnerContact
- Msvm_PlannedComputerSystem.Roles
- Msvm_PlannedComputerSystem.OtherIdentifyingInfo
- Msvm_PlannedComputerSystem.IdentifyingDescriptions
- Msvm_PlannedComputerSystem.Dedicated
- Msvm_PlannedComputerSystem.OtherDedicatedDescriptions
- Msvm_PlannedComputerSystem.ResetCapability
- Msvm_PlannedComputerSystem.PowerManagementCapabilities
- Msvm_PlannedComputerSystem.AssignedNumaNodeList
- Msvm_PlannedComputerSystem.OnTimeInMilliseconds
- Msvm_PlannedComputerSystem.ProcessID
- Msvm_PlannedComputerSystem.TimeOfLastConfigurationChange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 54bd72567880e97ece02936348d5a091a11d8ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758640"
---
# <a name="msvm_plannedcomputersystem-class"></a><span data-ttu-id="a9157-103">\_Classe Msvm PlannedComputerSystem</span><span class="sxs-lookup"><span data-stu-id="a9157-103">Msvm\_PlannedComputerSystem class</span></span>

<span data-ttu-id="a9157-104">Representa uma máquina virtual planejada.</span><span class="sxs-lookup"><span data-stu-id="a9157-104">Represents a planned virtual machine.</span></span>

<span data-ttu-id="a9157-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a9157-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9157-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9157-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PlannedComputerSystem : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption = "Planned Virtual Machine";
  string   Description = "Microsoft Planned Virtual Machine";
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The service is running normally" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
  string   CreationClassName;
  string   Name;
  string   NameFormat;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability;
  uint16   PowerManagementCapabilities[];
  uint16   AssignedNumaNodeList[];
  uint64   OnTimeInMilliseconds;
  uint32   ProcessID;
  datetime TimeOfLastConfigurationChange;
};
```

## <a name="members"></a><span data-ttu-id="a9157-107">Membros</span><span class="sxs-lookup"><span data-stu-id="a9157-107">Members</span></span>

<span data-ttu-id="a9157-108">A classe **Msvm \_ PlannedComputerSystem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a9157-108">The **Msvm\_PlannedComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="a9157-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="a9157-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="a9157-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a9157-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a9157-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="a9157-111">Methods</span></span>

<span data-ttu-id="a9157-112">A classe **Msvm \_ PlannedComputerSystem** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a9157-112">The **Msvm\_PlannedComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="a9157-113">Método</span><span class="sxs-lookup"><span data-stu-id="a9157-113">Method</span></span>                                                                      | <span data-ttu-id="a9157-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="a9157-114">Description</span></span>                                                                                 |
|:----------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9157-115">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="a9157-115">**RequestStateChange**</span></span>](requeststatechange-msvm-plannedcomputersystem.md) | <span data-ttu-id="a9157-116">Solicita que o estado do sistema planejado seja alterado para o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="a9157-116">Requests that the state of the planned system be changed to the value specified.</span></span><br/> |
| <span data-ttu-id="a9157-117">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a9157-117">**SetPowerState**</span></span>                                                           | <span data-ttu-id="a9157-118">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="a9157-118">This method is not supported.</span></span><br/>                                                    |



 

### <a name="properties"></a><span data-ttu-id="a9157-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a9157-119">Properties</span></span>

<span data-ttu-id="a9157-120">A classe **Msvm \_ PlannedComputerSystem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a9157-120">The **Msvm\_PlannedComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a9157-121">**AssignedNumaNodeList**</span><span class="sxs-lookup"><span data-stu-id="a9157-121">**AssignedNumaNodeList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-122">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9157-122">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a9157-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9157-124">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="a9157-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="a9157-125">Uma matriz de nós NUMA (acesso não uniforme à memória) que estão atualmente atribuídos à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a9157-125">An array of nonuniform memory access (NUMA) nodes that are currently assigned to the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="a9157-126">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="a9157-126">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-127">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9157-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a9157-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-129">Indica os valores possíveis para o parâmetro *requestedstate* do método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="a9157-129">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="a9157-130">Os valores listados serão um subconjunto dos valores contidos na propriedade **RequestedStatesSupported** da instância associada do **CIM \_ EnabledLogicalElementCapabilities**, em que os valores selecionados são uma função do estado atual do objeto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a9157-130">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="a9157-131">Essa propriedade pode ser não **nula** se uma implementação for capaz de anunciar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="a9157-131">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="a9157-132">Essa propriedade será **nula** se uma implementação não puder determinar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="a9157-132">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="a9157-133">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9157-133">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="a9157-134"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="a9157-134"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a9157-135"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="a9157-135"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a9157-136"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="a9157-136"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a9157-137"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="a9157-137"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a9157-138"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="a9157-138"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="a9157-139"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="a9157-139"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a9157-140"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="a9157-140"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a9157-141"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="a9157-141"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="a9157-142"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="a9157-142"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="a9157-143"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="a9157-143"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="a9157-144">)</span><span class="sxs-lookup"><span data-stu-id="a9157-144">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a9157-145">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="a9157-145">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a9157-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-148">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="a9157-148">A short description of the object.</span></span> <span data-ttu-id="a9157-149">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "máquina virtual planejada".</span><span class="sxs-lookup"><span data-stu-id="a9157-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Planned Virtual Machine".</span></span>

</dd> <dt>

<span data-ttu-id="a9157-150">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="a9157-150">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-151">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9157-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-153">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="a9157-153">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="a9157-154">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="a9157-154">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a9157-155">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a9157-155">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9157-156">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a9157-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a9157-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9157-159">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="a9157-159">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="a9157-160">Indica o nome da classe ou a subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="a9157-160">Indicates the name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="a9157-161">Quando usado com as outras propriedades de chave dessa classe, essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="a9157-161">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="a9157-162">Essa propriedade é herdada da classe de [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="a9157-162">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="a9157-163">**Dedicado**</span><span class="sxs-lookup"><span data-stu-id="a9157-163">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-164">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9157-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a9157-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-166">Uma matriz de valores que indica as finalidades às quais o sistema planejado é dedicado, se houver, e qual funcionalidade é fornecida.</span><span class="sxs-lookup"><span data-stu-id="a9157-166">An array of values that indicate the purposes to which the planned system is dedicated, if any, and what functionality is provided.</span></span> <span data-ttu-id="a9157-167">Por exemplo, é possível especificar que o sistema é dedicado a "Print" (valor = 11) ou atua como um "Hub" (valor = 8).</span><span class="sxs-lookup"><span data-stu-id="a9157-167">For example, one could specify that the System is dedicated to "Print" (value=11) or acts as a "Hub" (value=8).</span></span> <span data-ttu-id="a9157-168">Várias finalidades também podem ser indicadas.</span><span class="sxs-lookup"><span data-stu-id="a9157-168">Multiple purposes can also be indicated.</span></span> <span data-ttu-id="a9157-169">Por exemplo, esse é um sistema de uso geral que indica "não dedicado" (valor = 0), mas que também hospeda serviços de "impressão" (valor = 11) ou "dispositivo de usuário móvel" (valor = 17).</span><span class="sxs-lookup"><span data-stu-id="a9157-169">For example, this is a general purpose system indicating "Not Dedicated" (value=0) but that it also hosts "Print" (value=11) or "Mobile User Device" (value=17) services.</span></span>

<span data-ttu-id="a9157-170">Essa propriedade é herdada da classe de [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) .</span><span class="sxs-lookup"><span data-stu-id="a9157-170">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class.</span></span>



| <span data-ttu-id="a9157-171">Valor</span><span class="sxs-lookup"><span data-stu-id="a9157-171">Value</span></span>                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="a9157-172">Significado</span><span class="sxs-lookup"><span data-stu-id="a9157-172">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span><dl> <span data-ttu-id="a9157-173"><dt>**Não dedicado**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-173"><dt>**Not Dedicated**</dt> <dt>0</dt></span></span> </dl>                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="a9157-174"><dt>**Desconhecido**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-174"><dt>**Unknown**</dt> <dt>1</dt></span></span> </dl>                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="a9157-175"><dt>**Outros**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-175"><dt>**Other**</dt> <dt>2</dt></span></span> </dl>                                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span><dl> <span data-ttu-id="a9157-176"><dt>**Armazenamento**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-176"><dt>**Storage**</dt> <dt>3</dt></span></span> </dl>                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Router"></span><span id="router"></span><span id="ROUTER"></span><dl> <span data-ttu-id="a9157-177"><dt>**Roteador**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-177"><dt>**Router**</dt> <dt>4</dt></span></span> </dl>                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span><dl> <span data-ttu-id="a9157-178"><dt>**Opção**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-178"><dt>**Switch**</dt> <dt>5</dt></span></span> </dl>                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span><dl> <span data-ttu-id="a9157-179"><dt>**Opção de camada 3**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-179"><dt>**Layer 3 Switch**</dt> <dt>6</dt></span></span> </dl>                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span><dl> <span data-ttu-id="a9157-180"><dt>**Comutador central do Office**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-180"><dt>**Central Office Switch**</dt> <dt>7</dt></span></span> </dl>                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Hub"></span><span id="hub"></span><span id="HUB"></span><dl> <span data-ttu-id="a9157-181"><dt>**Hub**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-181"><dt>**Hub**</dt> <dt>8</dt></span></span> </dl>                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span><dl> <span data-ttu-id="a9157-182"><dt>**Servidor de acesso**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-182"><dt>**Access Server**</dt> <dt>9</dt></span></span> </dl>                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span><dl> <span data-ttu-id="a9157-183"><dt>**Firewall**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-183"><dt>**Firewall**</dt> <dt>10</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Print"></span><span id="print"></span><span id="PRINT"></span><dl> <span data-ttu-id="a9157-184"><dt>**Impressão**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-184"><dt>**Print**</dt> <dt>11</dt></span></span> </dl>                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="I_O"></span><span id="i_o"></span><dl> <span data-ttu-id="a9157-185"><dt>**E/s**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-185"><dt>**I/O**</dt> <dt>12</dt></span></span> </dl>                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span><dl> <span data-ttu-id="a9157-186"><dt>**Cache da Web**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-186"><dt>**Web Caching**</dt> <dt>13</dt></span></span> </dl>                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span><dl> <span data-ttu-id="a9157-187"><dt>**Gerenciamento**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-187"><dt>**Management**</dt> <dt>14</dt></span></span> </dl>                                                                 | <span data-ttu-id="a9157-188">Indica que essa instância é dedicada à hospedagem do software de gerenciamento do sistema.</span><span class="sxs-lookup"><span data-stu-id="a9157-188">Indicates this instance is dedicated to hosting system management software.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span><dl> <span data-ttu-id="a9157-189"><dt>**Servidor de blocos**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-189"><dt>**Block Server**</dt> <dt>15</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span><dl> <span data-ttu-id="a9157-190"><dt>**Servidor de arquivos**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-190"><dt>**File Server**</dt> <dt>16</dt></span></span> </dl>                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span><dl> <span data-ttu-id="a9157-191"><dt>**Dispositivo de usuário móvel**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-191"><dt>**Mobile User Device**</dt> <dt>17</dt></span></span> </dl>                                 | <span data-ttu-id="a9157-192">Um exemplo de um dispositivo de usuário móvel dedicado é um celular ou um scanner de código de barras em um repositório que se comunica por meio da radiofrequência.</span><span class="sxs-lookup"><span data-stu-id="a9157-192">An example of a dedicated mobile user device is a mobile phone or a bar code scanner in a store that communicates through radio frequency.</span></span> <span data-ttu-id="a9157-193">Esses sistemas são bastante limitados em funcionalidade e programação e não são considerados plataformas de computação de uso geral.</span><span class="sxs-lookup"><span data-stu-id="a9157-193">These systems are quite limited in functionality and programmability, and are not considered general purpose computing platforms.</span></span> <span data-ttu-id="a9157-194">Como alternativa, um exemplo de um sistema móvel que é de uso geral (ou seja, não é dedicado) é um computador de bolso.</span><span class="sxs-lookup"><span data-stu-id="a9157-194">Alternately, an example of a mobile system that is general purpose (that is, is NOT dedicated) is a hand-held computer.</span></span> <span data-ttu-id="a9157-195">Embora limitado em sua programação, o novo software pode ser baixado e sua funcionalidade expandida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="a9157-195">Although limited in its programmability, new software can be downloaded and its functionality expanded by the user.</span></span> <br/> |
| <span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span><dl> <span data-ttu-id="a9157-196"><dt>**Repeater**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-196"><dt>**Repeater**</dt> <dt>18</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span><dl> <span data-ttu-id="a9157-197"><dt>**Ponte/extensor**</dt> <dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-197"><dt>**Bridge/Extender**</dt> <dt>19</dt></span></span> </dl>                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span><dl> <span data-ttu-id="a9157-198"><dt>**Gateway**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-198"><dt>**Gateway**</dt> <dt>20</dt></span></span> </dl>                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span><dl> <span data-ttu-id="a9157-199"><dt>**Virtualização de armazenamento**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-199"><dt>**Storage Virtualizer**</dt> <dt>21</dt></span></span> </dl>                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span><dl> <span data-ttu-id="a9157-200"><dt>**Biblioteca de mídia**</dt> <dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-200"><dt>**Media Library**</dt> <dt>22</dt></span></span> </dl>                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span><dl> <span data-ttu-id="a9157-201"><dt>**ExtenderNode**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-201"><dt>**ExtenderNode**</dt> <dt>23</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span><dl> <span data-ttu-id="a9157-202"><dt>**Cabeça do nas**</dt> <dt>24</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-202"><dt>**NAS Head**</dt> <dt>24</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span><dl> <span data-ttu-id="a9157-203">O <dt>**nas**</dt> <dt>25</dt> independente</span><span class="sxs-lookup"><span data-stu-id="a9157-203"><dt>**Self-contained NAS**</dt> <dt>25</dt></span></span> </dl>                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="UPS"></span><span id="ups"></span><dl> <span data-ttu-id="a9157-204"><dt>26</dt> de <dt>**no-break**</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-204"><dt>**UPS**</dt> <dt>26</dt></span></span> </dl>                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span><dl> <span data-ttu-id="a9157-205"><dt>**Telefone IP**</dt> <dt>27</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-205"><dt>**IP Phone**</dt> <dt>27</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span><dl> <span data-ttu-id="a9157-206"><dt>**Controlador de gerenciamento**</dt> <dt>28</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-206"><dt>**Management Controller**</dt> <dt>28</dt></span></span> </dl>                     | <span data-ttu-id="a9157-207">Indica que essa instância representa um hardware especializado dedicado ao gerenciamento de sistemas (ou seja, um controlador BMC ou processador de serviços).</span><span class="sxs-lookup"><span data-stu-id="a9157-207">Indicates this instance represents specialized hardware dedicated to systems management (that is, a Baseboard Management Controller (BMC) or service processor).</span></span> <span data-ttu-id="a9157-208">O escopo de gerenciamento de um controlador de gerenciamento é normalmente um único sistema gerenciado no qual ele está contido.</span><span class="sxs-lookup"><span data-stu-id="a9157-208">The management scope of a Management Controller is typically a single managed system in which it is contained.</span></span><br/>                                                                                                                                                                                                                                           |
| <span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span><dl> <span data-ttu-id="a9157-209"><dt>**Gerente de chassi**</dt> <dt>29</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-209"><dt>**Chassis Manager**</dt> <dt>29</dt></span></span> </dl>                                             | <span data-ttu-id="a9157-210">Indica que essa instância representa um sistema dedicado ao gerenciamento de um chassi de folha e seus dispositivos contidos.</span><span class="sxs-lookup"><span data-stu-id="a9157-210">Indicates this instance represents a system dedicated to management of a blade chassis and its contained devices.</span></span> <span data-ttu-id="a9157-211">Esse valor seria usado para representar um controlador de prateleira.</span><span class="sxs-lookup"><span data-stu-id="a9157-211">This value would be used to represent a Shelf Controller.</span></span> <span data-ttu-id="a9157-212">Um gerente de chassi é um ponto de agregação para gerenciamento e pode depender de controladores de gerenciamento subordinados para o gerenciamento de partes constituintes.</span><span class="sxs-lookup"><span data-stu-id="a9157-212">A Chassis Manager is an aggregation point for management and may rely on subordinate management controllers for the management of constituent parts.</span></span> <br/>                                                                                                                                                                                         |
| <span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span><dl> <span data-ttu-id="a9157-213"><dt>**Controlador RAID com base em host**</dt> <dt>30</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-213"><dt>**Host-based RAID controller**</dt> <dt>30</dt></span></span> </dl> | <span data-ttu-id="a9157-214">Indica que essa instância representa um controlador de armazenamento RAID contido em um computador host.</span><span class="sxs-lookup"><span data-stu-id="a9157-214">Indicates this instance represents a RAID storage controller contained within a host computer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span><dl> <span data-ttu-id="a9157-215"><dt>**Compartimento de dispositivo de armazenamento**</dt> <dt>31</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-215"><dt>**Storage Device Enclosure**</dt> <dt>31</dt></span></span> </dl>         | <span data-ttu-id="a9157-216">Indica que essa instância representa um compartimento que contém dispositivos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a9157-216">Indicates this instance represents an enclosure that contains storage devices.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span><dl> <span data-ttu-id="a9157-217"><dt>**Área de trabalho**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-217"><dt>**Desktop**</dt> <dt>32</dt></span></span> </dl>                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span><dl> <span data-ttu-id="a9157-218"><dt>**Laptop**</dt> <dt>33</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-218"><dt>**Laptop**</dt> <dt>33</dt></span></span> </dl>                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span><dl> <span data-ttu-id="a9157-219"><dt>**Biblioteca de fitas virtuais**</dt> <dt>34</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-219"><dt>**Virtual Tape Library**</dt> <dt>34</dt></span></span> </dl>                         | <span data-ttu-id="a9157-220">A emulação de uma biblioteca de fitas por um sistema de biblioteca virtual.</span><span class="sxs-lookup"><span data-stu-id="a9157-220">The emulation of a tape library by a Virtual Library System.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span><dl> <span data-ttu-id="a9157-221"><dt>**Sistema de Biblioteca Virtual**</dt> <dt>35</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-221"><dt>**Virtual Library System**</dt> <dt>35</dt></span></span> </dl>                 | <span data-ttu-id="a9157-222">Usa o armazenamento em disco para emular bibliotecas de fitas.</span><span class="sxs-lookup"><span data-stu-id="a9157-222">Uses disk storage to emulate tape libraries.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span><dl> <span data-ttu-id="a9157-223"><dt>**PC de rede/cliente fino**</dt> <dt>36</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-223"><dt>**Network PC/Thin Client**</dt> <dt>36</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span><dl> <span data-ttu-id="a9157-224"><dt>**Comutador FC**</dt> <dt>37</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-224"><dt>**FC Switch**</dt> <dt>37</dt></span></span> </dl>                                                                     | <span data-ttu-id="a9157-225">Indica que essa instância é dedicada a alternar quadros de Fibre Channel de camada 2.</span><span class="sxs-lookup"><span data-stu-id="a9157-225">Indicates this instance is dedicated to switching layer 2 Fibre Channel frames.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span><dl> <span data-ttu-id="a9157-226"><dt>**Comutador Ethernet**</dt> <dt>38</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-226"><dt>**Ethernet Switch**</dt> <dt>38</dt></span></span> </dl>                                             | <span data-ttu-id="a9157-227">Indica que essa instância é dedicada à alternância de quadros de Ethernet de camada 2.</span><span class="sxs-lookup"><span data-stu-id="a9157-227">Indicates this instance is dedicated to switching layer 2 Ethernet frames.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="a9157-228">O <dt>**DMTF reservou**</dt> <dt>39.. 32567</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-228"><dt>**DMTF Reserved**</dt> <dt>39..32567</dt></span></span> </dl>                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="a9157-229">32568 <dt> **reservado pelo fornecedor**</dt> <dt>.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-229"><dt>**Vendor Reserved** </dt> <dt>32568..65535</dt></span></span> </dl>                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="a9157-230">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a9157-230">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-231">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a9157-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-232">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-233">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="a9157-233">A description of the object.</span></span> <span data-ttu-id="a9157-234">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "máquina virtual planejada da Microsoft".</span><span class="sxs-lookup"><span data-stu-id="a9157-234">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Planned Virtual Machine".</span></span>

</dd> <dt>

<span data-ttu-id="a9157-235">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="a9157-235">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-236">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9157-236">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-237">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-238">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="a9157-238">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="a9157-239">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="a9157-239">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a9157-240">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a9157-240">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9157-241">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a9157-241">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-242">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a9157-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-243">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-244">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="a9157-244">A display name for the object.</span></span> <span data-ttu-id="a9157-245">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a9157-245">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9157-246">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="a9157-246">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-247">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9157-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-249">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="a9157-249">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="a9157-250">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a9157-250">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and can be one of the following values.</span></span>



| <span data-ttu-id="a9157-251">Valor</span><span class="sxs-lookup"><span data-stu-id="a9157-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="a9157-252">Significado</span><span class="sxs-lookup"><span data-stu-id="a9157-252">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="a9157-253"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-253"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="a9157-254">O sistema está desligado.</span><span class="sxs-lookup"><span data-stu-id="a9157-254">The system is turned off.</span></span><br/>                                             |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="a9157-255"><dt>**Habilitado, mas offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-255"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="a9157-256">O sistema está habilitado, mas offline.</span><span class="sxs-lookup"><span data-stu-id="a9157-256">The system is enabled, but offline.</span></span> <span data-ttu-id="a9157-257">Todas as novas solicitações serão descartadas.</span><span class="sxs-lookup"><span data-stu-id="a9157-257">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a9157-258">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="a9157-258">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-259">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9157-259">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-260">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-261">Especifica o estado habilitado do sistema planejado.</span><span class="sxs-lookup"><span data-stu-id="a9157-261">Specifies the enabled state of the planned system.</span></span> <span data-ttu-id="a9157-262">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a9157-262">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it can be one of the following values.</span></span>



| <span data-ttu-id="a9157-263">Valor</span><span class="sxs-lookup"><span data-stu-id="a9157-263">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="a9157-264">Significado</span><span class="sxs-lookup"><span data-stu-id="a9157-264">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="a9157-265"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-265"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="a9157-266">O sistema está desligado.</span><span class="sxs-lookup"><span data-stu-id="a9157-266">The system is turned off.</span></span><br/>                                             |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="a9157-267"><dt>**Habilitado, mas offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-267"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="a9157-268">O sistema está habilitado, mas offline.</span><span class="sxs-lookup"><span data-stu-id="a9157-268">The system is enabled, but offline.</span></span> <span data-ttu-id="a9157-269">Todas as novas solicitações serão descartadas.</span><span class="sxs-lookup"><span data-stu-id="a9157-269">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a9157-270">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="a9157-270">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-271">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9157-271">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-272">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-273">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="a9157-273">The current health of the element.</span></span> <span data-ttu-id="a9157-274">Essa propriedade expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="a9157-274">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="a9157-275">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="a9157-275">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="a9157-276">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="a9157-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="a9157-277">Valor</span><span class="sxs-lookup"><span data-stu-id="a9157-277">Value</span></span>                                                                        | <span data-ttu-id="a9157-278">Significado</span><span class="sxs-lookup"><span data-stu-id="a9157-278">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="a9157-279"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-279"><dt>5</dt></span></span> </dl> | <span data-ttu-id="a9157-280">O status de integridade é normal.</span><span class="sxs-lookup"><span data-stu-id="a9157-280">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a9157-281">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a9157-281">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-282">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a9157-282">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a9157-283">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-284">Uma matriz de cadeias de caracteres que fornece explicações e detalhes por trás das entradas na matriz **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="a9157-284">An array of strings providing explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="a9157-285">Cada entrada dessa matriz está relacionada à entrada em **OtherIdentifyingInfo** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="a9157-285">Each entry of this array is related to the entry in **OtherIdentifyingInfo** that is located at the same index.</span></span> <span data-ttu-id="a9157-286">Essa propriedade é herdada da classe de [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="a9157-286">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="a9157-287">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a9157-287">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-288">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a9157-288">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-290">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="a9157-290">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="a9157-291">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a9157-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9157-292">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a9157-292">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-293">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a9157-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-294">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9157-295">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="a9157-295">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a9157-296">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="a9157-296">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a9157-297">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a9157-297">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9157-298">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a9157-298">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-299">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a9157-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-300">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9157-301">Qualificadores: **chave**, **substituição**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="a9157-301">Qualifiers: **Key**, **Override**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="a9157-302">O nome herdado serve como a chave de uma instância do sistema em um ambiente corporativo.</span><span class="sxs-lookup"><span data-stu-id="a9157-302">The inherited name serves as the key of a system instance in an enterprise environment.</span></span> <span data-ttu-id="a9157-303">Essa propriedade é herdada da classe de [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="a9157-303">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="a9157-304">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="a9157-304">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-305">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a9157-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-306">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9157-307">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="a9157-307">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="a9157-308">Identifica como o nome do sistema foi gerado, usando a heurística da subclasse.</span><span class="sxs-lookup"><span data-stu-id="a9157-308">Identifies how the system name was generated, using the heuristic of the subclass.</span></span> <span data-ttu-id="a9157-309">O objeto System e seus derivados são objetos de nível superior do CIM.</span><span class="sxs-lookup"><span data-stu-id="a9157-309">The system object and its derivatives are top-level objects of CIM.</span></span> <span data-ttu-id="a9157-310">Eles fornecem o escopo para vários componentes.</span><span class="sxs-lookup"><span data-stu-id="a9157-310">They provide the scope for numerous components.</span></span> <span data-ttu-id="a9157-311">É necessário ter chaves de sistema exclusivas.</span><span class="sxs-lookup"><span data-stu-id="a9157-311">Having unique system keys is required.</span></span> <span data-ttu-id="a9157-312">Uma heurística pode ser definida em subclasses individuais do sistema para tentar gerar sempre a mesma chave de nome do sistema.</span><span class="sxs-lookup"><span data-stu-id="a9157-312">A heuristic can be defined in individual system subclasses to attempt to always generate the same system name key.</span></span> <span data-ttu-id="a9157-313">Essa propriedade é herdada da classe de [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="a9157-313">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="a9157-314">**OnTimeInMilliseconds**</span><span class="sxs-lookup"><span data-stu-id="a9157-314">**OnTimeInMilliseconds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-315">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a9157-315">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9157-317">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milissegundos")</span><span class="sxs-lookup"><span data-stu-id="a9157-317">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds")</span></span>
</dt> </dl>

<span data-ttu-id="a9157-318">O tempo total, em milissegundos, desde a última vez em que a máquina virtual foi ativada, redefinida ou restaurada.</span><span class="sxs-lookup"><span data-stu-id="a9157-318">The total time, in milliseconds, since the virtual machine was last turned on, reset, or restored.</span></span> <span data-ttu-id="a9157-319">Esse tempo exclui a hora em que a máquina virtual estava no estado em pausa.</span><span class="sxs-lookup"><span data-stu-id="a9157-319">This time excludes the time the virtual machine was in the paused state.</span></span>

</dd> <dt>

<span data-ttu-id="a9157-320">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="a9157-320">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-321">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9157-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-323">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="a9157-323">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="a9157-324">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="a9157-324">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a9157-325">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a9157-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9157-326">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="a9157-326">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-327">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9157-327">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a9157-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-329">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="a9157-329">The current statuses of the object.</span></span> <span data-ttu-id="a9157-330">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="a9157-330">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="a9157-331">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a9157-331">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-332">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a9157-332">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a9157-333">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-334">Uma cadeia de caracteres que descreve como ou por que o sistema é dedicado quando a matriz dedicada inclui o valor 2, "other".</span><span class="sxs-lookup"><span data-stu-id="a9157-334">A string describing how or why the system is dedicated when the Dedicated array includes the value 2, "Other".</span></span> <span data-ttu-id="a9157-335">Essa propriedade é herdada da classe de [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) .</span><span class="sxs-lookup"><span data-stu-id="a9157-335">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class.</span></span>

</dd> <dt>

<span data-ttu-id="a9157-336">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="a9157-336">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-337">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a9157-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-338">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-339">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="a9157-339">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="a9157-340">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="a9157-340">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="a9157-341">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a9157-341">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a9157-342">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="a9157-342">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-343">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a9157-343">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a9157-344">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9157-345">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="a9157-345">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="a9157-346">Contém dados adicionais, além das informações de nome do sistema, que podem ser usadas para identificar um ComputerSystem.</span><span class="sxs-lookup"><span data-stu-id="a9157-346">Contains additional data, beyond system name information, that can be used to identify a ComputerSystem.</span></span> <span data-ttu-id="a9157-347">Um exemplo seria manter o Fibre Channel WWN (World-Wide Name) de um nó.</span><span class="sxs-lookup"><span data-stu-id="a9157-347">One example would be to hold the Fibre Channel World-Wide Name (WWN) of a node.</span></span> <span data-ttu-id="a9157-348">Se apenas o nome do Fibre Channel estiver disponível e for exclusivo (capaz de ser usado como a chave do sistema), essa propriedade seria **nula** e o WWN se tornaria a chave do sistema, seus dados colocados na propriedade **Name** .</span><span class="sxs-lookup"><span data-stu-id="a9157-348">If only the Fibre Channel name is available and is unique (able to be used as the system key), then this property would be **Null** and the WWN would become the system key, its data placed in the **Name** property.</span></span> <span data-ttu-id="a9157-349">Essa propriedade é herdada da classe de [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="a9157-349">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="a9157-350">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a9157-350">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-351">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9157-351">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a9157-352">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-353">Essa propriedade é herdada da classe de [**\_ ComputerSystem do CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) , mas não é suportada.</span><span class="sxs-lookup"><span data-stu-id="a9157-353">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class, but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="a9157-354">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="a9157-354">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-355">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a9157-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-356">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a9157-356">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a9157-357">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="a9157-357">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="a9157-358">Uma cadeia de caracteres que fornece informações sobre como o proprietário do sistema primário pode ser alcançado (por exemplo, número de telefone, endereço de email e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="a9157-358">A string that provides information on how the primary system owner can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="a9157-359">Essa propriedade é herdada da classe de [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="a9157-359">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="a9157-360">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="a9157-360">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-361">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a9157-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-362">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a9157-362">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a9157-363">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="a9157-363">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="a9157-364">O nome do proprietário do sistema primário.</span><span class="sxs-lookup"><span data-stu-id="a9157-364">The name of the primary system owner.</span></span> <span data-ttu-id="a9157-365">O proprietário do sistema é o usuário principal do sistema.</span><span class="sxs-lookup"><span data-stu-id="a9157-365">The system owner is the primary user of the system.</span></span> <span data-ttu-id="a9157-366">Essa propriedade é herdada da classe de [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="a9157-366">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="a9157-367">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="a9157-367">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-368">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9157-368">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-369">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-370">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="a9157-370">Provides high level status information.</span></span> <span data-ttu-id="a9157-371">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer informações de status de integridade detalhadas e de alto nível para o elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="a9157-371">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="a9157-372">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="a9157-372">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a9157-373">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a9157-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9157-374">**ProcessID**</span><span class="sxs-lookup"><span data-stu-id="a9157-374">**ProcessID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-375">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a9157-375">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-376">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-377">O identificador do processo no qual esta máquina virtual está em execução.</span><span class="sxs-lookup"><span data-stu-id="a9157-377">The identifier of the process under which this virtual machine is running.</span></span> <span data-ttu-id="a9157-378">Esse valor pode ser usado para identificar exclusivamente a instância do Vmwp.exe no sistema que está executando a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a9157-378">This value can be used to uniquely identify the instance of Vmwp.exe on the system that is running the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="a9157-379">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="a9157-379">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-380">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9157-380">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-381">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-382">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="a9157-382">The last requested or desired state for the element.</span></span> <span data-ttu-id="a9157-383">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="a9157-383">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="a9157-384">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais para um elemento.</span><span class="sxs-lookup"><span data-stu-id="a9157-384">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="a9157-385">Uma instância específica da classe [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) pode não oferecer suporte à propriedade **requestedstate** .</span><span class="sxs-lookup"><span data-stu-id="a9157-385">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="a9157-386">Se isso ocorrer, o valor 12 ("não aplicável") será usado.</span><span class="sxs-lookup"><span data-stu-id="a9157-386">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="a9157-387">Essa propriedade é herdada do **CIM \_ EnabledLogicalElement** e é sempre definida como 12 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="a9157-387">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="a9157-388">Valor</span><span class="sxs-lookup"><span data-stu-id="a9157-388">Value</span></span>                                                                         | <span data-ttu-id="a9157-389">Significado</span><span class="sxs-lookup"><span data-stu-id="a9157-389">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="a9157-390"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-390"><dt>12</dt></span></span> </dl> | <span data-ttu-id="a9157-391">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="a9157-391">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a9157-392">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="a9157-392">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-393">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9157-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-394">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-395">Especifica os recursos de redefinição do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="a9157-395">Specifies the reset capabilities of the computer system.</span></span> <span data-ttu-id="a9157-396">Essa propriedade é herdada da classe de [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) .</span><span class="sxs-lookup"><span data-stu-id="a9157-396">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class.</span></span>



| <span data-ttu-id="a9157-397">Valor</span><span class="sxs-lookup"><span data-stu-id="a9157-397">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="a9157-398">Significado</span><span class="sxs-lookup"><span data-stu-id="a9157-398">Meaning</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="a9157-399"><dt>**Outros**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-399"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                              |                                                                                                            |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="a9157-400"><dt>**Desconhecido**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-400"><dt>**Unknown**</dt> <dt>2</dt></span></span> </dl>                                      |                                                                                                            |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="a9157-401"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-401"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                  | <span data-ttu-id="a9157-402">A redefinição de hardware não é permitida.</span><span class="sxs-lookup"><span data-stu-id="a9157-402">Hardware reset is not allowed.</span></span> <br/>                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="a9157-403"><dt>**Habilitado**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-403"><dt>**Enabled**</dt> <dt>4</dt></span></span> </dl>                                      | <span data-ttu-id="a9157-404">O sistema de computador pode ser redefinido usando hardware (por exemplo, os botões potência e redefinição).</span><span class="sxs-lookup"><span data-stu-id="a9157-404">The computer system can be reset by using hardware (for example, the power and reset buttons).</span></span> <br/> |
| <span id="Not_Implemented_"></span><span id="not_implemented_"></span><span id="NOT_IMPLEMENTED_"></span><dl> <span data-ttu-id="a9157-405"><dt> **Não implementado**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-405"><dt>**Not Implemented** </dt> <dt>5 </dt></span></span> </dl> |                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="a9157-406">**Funções**</span><span class="sxs-lookup"><span data-stu-id="a9157-406">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-407">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a9157-407">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a9157-408">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a9157-408">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a9157-409">Uma matriz de cadeias de caracteres que especifica as funções definidas pelo administrador que esse sistema desempenha no ambiente gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a9157-409">An array of strings that specifies the administrator-defined roles this system plays in the managed environment.</span></span> <span data-ttu-id="a9157-410">Os exemplos podem ser "Build 8 servidor de impressão" ou "Boise de diretórios de usuário".</span><span class="sxs-lookup"><span data-stu-id="a9157-410">Examples might be "Building 8 print server" or "Boise user directories".</span></span> <span data-ttu-id="a9157-411">Um único sistema pode executar várias funções.</span><span class="sxs-lookup"><span data-stu-id="a9157-411">A single system may perform multiple roles.</span></span> <span data-ttu-id="a9157-412">A exibição de instrumentação das funções de um sistema é definida pela instanciação de uma subclasse específica do sistema, ou por propriedades em uma subclasse, ou ambos.</span><span class="sxs-lookup"><span data-stu-id="a9157-412">The instrumentation view of the roles of a system is defined by instantiating a specific subclass of system, or by properties in a subclass, or both.</span></span> <span data-ttu-id="a9157-413">Por exemplo, a finalidade de um ComputerSystem é definida usando as propriedades **dedicadas** e **OtherDedicatedDescription** .</span><span class="sxs-lookup"><span data-stu-id="a9157-413">For example, the purpose of a ComputerSystem is defined using the **Dedicated** and **OtherDedicatedDescription** properties.</span></span> <span data-ttu-id="a9157-414">Essa propriedade é herdada da classe de [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="a9157-414">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="a9157-415">**Status**</span><span class="sxs-lookup"><span data-stu-id="a9157-415">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-416">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a9157-416">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-417">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-418">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="a9157-418">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a9157-419">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a9157-419">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-420">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a9157-420">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a9157-421">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-422">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="a9157-422">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="a9157-423">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), e cada elemento da matriz é sempre definido como "o serviço está sendo executado normalmente".</span><span class="sxs-lookup"><span data-stu-id="a9157-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "The service is running normally".</span></span>

</dd> <dt>

<span data-ttu-id="a9157-424">**TimeOfLastConfigurationChange**</span><span class="sxs-lookup"><span data-stu-id="a9157-424">**TimeOfLastConfigurationChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-425">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a9157-425">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-426">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-427">A data e a hora da última modificação do arquivo de configuração da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a9157-427">The date and time when the virtual machine configuration file was last modified.</span></span> <span data-ttu-id="a9157-428">O arquivo de configuração é modificado durante determinadas operações de máquina virtual, bem como quando qualquer uma das configurações da máquina virtual ou do dispositivo é adicionada, modificada ou removida.</span><span class="sxs-lookup"><span data-stu-id="a9157-428">The configuration file is modified during certain virtual machine operations, as well as when any of the virtual machine or device settings are added, modified, or removed.</span></span>

</dd> <dt>

<span data-ttu-id="a9157-429">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="a9157-429">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-430">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a9157-430">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-431">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-432">A data e a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="a9157-432">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="a9157-433">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é suportada.</span><span class="sxs-lookup"><span data-stu-id="a9157-433">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="a9157-434">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="a9157-434">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9157-435">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9157-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9157-436">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9157-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9157-437">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="a9157-437">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="a9157-438">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9157-438">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="a9157-439">Valor</span><span class="sxs-lookup"><span data-stu-id="a9157-439">Value</span></span>                                                                                                                                                                                                                                                     | <span data-ttu-id="a9157-440">Significado</span><span class="sxs-lookup"><span data-stu-id="a9157-440">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="a9157-441"><dt></dt> <dt>0</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="a9157-441"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                               |                                                                                  |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="a9157-442"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-442"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                               |                                                                                  |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="a9157-443"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-443"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                           |                                                                                  |
| <span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span><dl> <span data-ttu-id="a9157-444"><dt>**Desligar**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-444"><dt>**Shut Down**</dt> <dt>4</dt></span></span> </dl>                       |                                                                                  |
| <span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span><dl> <span data-ttu-id="a9157-445"><dt>**Nenhuma alteração**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-445"><dt>**No Change**</dt> <dt>5</dt></span></span> </dl>                       | <span data-ttu-id="a9157-446">Nenhuma transição em andamento.</span><span class="sxs-lookup"><span data-stu-id="a9157-446">No transition is in progress.</span></span><br/>                                         |
| <span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span><dl> <span data-ttu-id="a9157-447"><dt>**Offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-447"><dt>**Offline**</dt> <dt>6</dt></span></span> </dl>                               |                                                                                  |
| <span id="Test"></span><span id="test"></span><span id="TEST"></span><dl> <span data-ttu-id="a9157-448"><dt>**Teste**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-448"><dt>**Test**</dt> <dt>7</dt></span></span> </dl>                                           |                                                                                  |
| <span id="Defer"></span><span id="defer"></span><span id="DEFER"></span><dl> <span data-ttu-id="a9157-449"><dt>**Adiar**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-449"><dt>**Defer**</dt> <dt>8</dt></span></span> </dl>                                       |                                                                                  |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="a9157-450"><dt>**Desativar**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-450"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                               |                                                                                  |
| <span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span><dl> <span data-ttu-id="a9157-451"><dt>**Reinicializar**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-451"><dt>**Reboot**</dt> <dt>10</dt></span></span> </dl>                                  |                                                                                  |
| <span id="Reset"></span><span id="reset"></span><span id="RESET"></span><dl> <span data-ttu-id="a9157-452"><dt>**Redefinir**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-452"><dt>**Reset**</dt> <dt>11</dt></span></span> </dl>                                      |                                                                                  |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="a9157-453"><dt>**Não aplicável**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-453"><dt>**Not Applicable**</dt> <dt>12</dt></span></span> </dl>  | <span data-ttu-id="a9157-454">A implementação não dá suporte à representação de transições em andamento.</span><span class="sxs-lookup"><span data-stu-id="a9157-454">The implementation does not support representing ongoing transitions.</span></span><br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="a9157-455"><dt> **DMTF reservado**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-455"><dt>**DMTF Reserved** </dt> <dt>.. </dt></span></span> </dl> |                                                                                  |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a9157-456">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9157-456">Requirements</span></span>



| <span data-ttu-id="a9157-457">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9157-457">Requirement</span></span> | <span data-ttu-id="a9157-458">Valor</span><span class="sxs-lookup"><span data-stu-id="a9157-458">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9157-459">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9157-459">Minimum supported client</span></span><br/> | <span data-ttu-id="a9157-460">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a9157-460">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a9157-461">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9157-461">Minimum supported server</span></span><br/> | <span data-ttu-id="a9157-462">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a9157-462">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a9157-463">Namespace</span><span class="sxs-lookup"><span data-stu-id="a9157-463">Namespace</span></span><br/>                | <span data-ttu-id="a9157-464">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="a9157-464">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a9157-465">MOF</span><span class="sxs-lookup"><span data-stu-id="a9157-465">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9157-466"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-466"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9157-467">DLL</span><span class="sxs-lookup"><span data-stu-id="a9157-467">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9157-468"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a9157-468"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a9157-469">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9157-469">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9157-470">**\_Sistema de COMPUTERSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="a9157-470">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> <dt>

[<span data-ttu-id="a9157-471">**Msvm \_ VirtualSystemManagementService. Método ImportSystemDefinition**</span><span class="sxs-lookup"><span data-stu-id="a9157-471">**Msvm\_VirtualSystemManagementService .ImportSystemDefinition method**</span></span>](importsystemdefinition-msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

