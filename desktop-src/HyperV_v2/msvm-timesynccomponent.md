---
description: Representa o estado do serviço de sincronização de tempo, que é responsável por sincronizar a hora do sistema de uma máquina virtual com a hora do sistema operacional em execução no sistema operacional de gerenciamento.
ms.assetid: 551A81E9-E924-4A9C-965D-02FF25EE4A49
title: Classe Msvm_TimeSyncComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TimeSyncComponent
- Msvm_TimeSyncComponent.SetPowerState
- Msvm_TimeSyncComponent.EnableDevice
- Msvm_TimeSyncComponent.OnlineDevice
- Msvm_TimeSyncComponent.QuiesceDevice
- Msvm_TimeSyncComponent.SaveProperties
- Msvm_TimeSyncComponent.RestoreProperties
- Msvm_TimeSyncComponent.InstanceID
- Msvm_TimeSyncComponent.Caption
- Msvm_TimeSyncComponent.Description
- Msvm_TimeSyncComponent.ElementName
- Msvm_TimeSyncComponent.InstallDate
- Msvm_TimeSyncComponent.Name
- Msvm_TimeSyncComponent.OperationalStatus
- Msvm_TimeSyncComponent.StatusDescriptions
- Msvm_TimeSyncComponent.Status
- Msvm_TimeSyncComponent.HealthState
- Msvm_TimeSyncComponent.CommunicationStatus
- Msvm_TimeSyncComponent.DetailedStatus
- Msvm_TimeSyncComponent.OperatingStatus
- Msvm_TimeSyncComponent.PrimaryStatus
- Msvm_TimeSyncComponent.EnabledState
- Msvm_TimeSyncComponent.OtherEnabledState
- Msvm_TimeSyncComponent.RequestedState
- Msvm_TimeSyncComponent.EnabledDefault
- Msvm_TimeSyncComponent.TimeOfLastStateChange
- Msvm_TimeSyncComponent.AvailableRequestedStates
- Msvm_TimeSyncComponent.TransitioningToState
- Msvm_TimeSyncComponent.SystemCreationClassName
- Msvm_TimeSyncComponent.SystemName
- Msvm_TimeSyncComponent.CreationClassName
- Msvm_TimeSyncComponent.DeviceID
- Msvm_TimeSyncComponent.PowerManagementSupported
- Msvm_TimeSyncComponent.PowerManagementCapabilities
- Msvm_TimeSyncComponent.Availability
- Msvm_TimeSyncComponent.StatusInfo
- Msvm_TimeSyncComponent.LastErrorCode
- Msvm_TimeSyncComponent.ErrorDescription
- Msvm_TimeSyncComponent.ErrorCleared
- Msvm_TimeSyncComponent.OtherIdentifyingInfo
- Msvm_TimeSyncComponent.PowerOnHours
- Msvm_TimeSyncComponent.TotalPowerOnHours
- Msvm_TimeSyncComponent.IdentifyingDescriptions
- Msvm_TimeSyncComponent.AdditionalAvailability
- Msvm_TimeSyncComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ea9a33d665a315861d9e6c51fd529f10f07b4aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759667"
---
# <a name="msvm_timesynccomponent-class"></a><span data-ttu-id="980a4-103">\_Classe Msvm TimeSyncComponent</span><span class="sxs-lookup"><span data-stu-id="980a4-103">Msvm\_TimeSyncComponent class</span></span>

<span data-ttu-id="980a4-104">Representa o estado do serviço de sincronização de tempo, que é responsável por sincronizar a hora do sistema de uma máquina virtual com a hora do sistema operacional em execução no sistema operacional de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="980a4-104">Represents the state of the time synchronization service, which is responsible for synchronizing the system time of a virtual machine with the system time of the operating system running in the management operating system.</span></span>

<span data-ttu-id="980a4-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="980a4-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="980a4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="980a4-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TimeSyncComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Time Synchronization";
  string   Description = "Microsoft Time Synchronization Service";
  string   ElementName = "Time Synchronization";
  datetime InstallDate;
  string   Name = "Time Synchronization";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = {"OK"};
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 7;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_TimeSyncComponent";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = {6};
  uint64   MaxQuiesceTime;
};
```

## <a name="members"></a><span data-ttu-id="980a4-107">Membros</span><span class="sxs-lookup"><span data-stu-id="980a4-107">Members</span></span>

<span data-ttu-id="980a4-108">A classe **Msvm \_ TimeSyncComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="980a4-108">The **Msvm\_TimeSyncComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="980a4-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="980a4-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="980a4-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="980a4-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="980a4-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="980a4-111">Methods</span></span>

<span data-ttu-id="980a4-112">A classe **Msvm \_ TimeSyncComponent** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="980a4-112">The **Msvm\_TimeSyncComponent** class has these methods.</span></span>



| <span data-ttu-id="980a4-113">Método</span><span class="sxs-lookup"><span data-stu-id="980a4-113">Method</span></span>                                                                  | <span data-ttu-id="980a4-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="980a4-114">Description</span></span>                              |
|:------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="980a4-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="980a4-115">**EnableDevice**</span></span>                                                        | <span data-ttu-id="980a4-116">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="980a4-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="980a4-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="980a4-117">**OnlineDevice**</span></span>                                                        | <span data-ttu-id="980a4-118">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="980a4-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="980a4-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="980a4-119">**QuiesceDevice**</span></span>                                                       | <span data-ttu-id="980a4-120">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="980a4-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="980a4-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="980a4-121">**RequestStateChange**</span></span>](msvm-timesynccomponent-requeststatechange.md) | <span data-ttu-id="980a4-122">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="980a4-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="980a4-123">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="980a4-123">**Reset**</span></span>](msvm-timesynccomponent-reset.md)                           | <span data-ttu-id="980a4-124">Redefine o componente.</span><span class="sxs-lookup"><span data-stu-id="980a4-124">Resets the component.</span></span><br/>         |
| <span data-ttu-id="980a4-125">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="980a4-125">**RestoreProperties**</span></span>                                                   | <span data-ttu-id="980a4-126">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="980a4-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="980a4-127">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="980a4-127">**SaveProperties**</span></span>                                                      | <span data-ttu-id="980a4-128">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="980a4-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="980a4-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="980a4-129">**SetPowerState**</span></span>                                                       | <span data-ttu-id="980a4-130">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="980a4-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="980a4-131">Propriedades</span><span class="sxs-lookup"><span data-stu-id="980a4-131">Properties</span></span>

<span data-ttu-id="980a4-132">A classe **Msvm \_ TimeSyncComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="980a4-132">The **Msvm\_TimeSyncComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="980a4-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="980a4-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-134">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980a4-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="980a4-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-136">Qualquer disponibilidade e status adicionais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="980a4-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="980a4-137">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como 6 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="980a4-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="980a4-138">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="980a4-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-139">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980a4-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-141">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="980a4-141">The primary availability and status of the device.</span></span> <span data-ttu-id="980a4-142">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="980a4-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="980a4-143">Valor</span><span class="sxs-lookup"><span data-stu-id="980a4-143">Value</span></span>                                                                        | <span data-ttu-id="980a4-144">Significado</span><span class="sxs-lookup"><span data-stu-id="980a4-144">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="980a4-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="980a4-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="980a4-146">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="980a4-146">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="980a4-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="980a4-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-148">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980a4-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="980a4-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-150">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="980a4-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="980a4-151">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="980a4-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="980a4-152">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="980a4-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="980a4-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-155">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="980a4-155">A short description of the object.</span></span> <span data-ttu-id="980a4-156">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="980a4-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="980a4-157">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="980a4-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-158">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980a4-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-160">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="980a4-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="980a4-161">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="980a4-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="980a4-162">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="980a4-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="980a4-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="980a4-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="980a4-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="980a4-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="980a4-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="980a4-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="980a4-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="980a4-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="980a4-170">)</span><span class="sxs-lookup"><span data-stu-id="980a4-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="980a4-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="980a4-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-172">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="980a4-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-174">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="980a4-174">The scoping system's creation class name.</span></span> <span data-ttu-id="980a4-175">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="980a4-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="980a4-176">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="980a4-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="980a4-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-179">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="980a4-179">A description of the object.</span></span> <span data-ttu-id="980a4-180">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="980a4-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="980a4-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="980a4-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-182">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980a4-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-184">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="980a4-184">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="980a4-185">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="980a4-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="980a4-186">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="980a4-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="980a4-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="980a4-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="980a4-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="980a4-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="980a4-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="980a4-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="980a4-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="980a4-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="980a4-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="980a4-195">)</span><span class="sxs-lookup"><span data-stu-id="980a4-195">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="980a4-196">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="980a4-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-197">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="980a4-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-199">Um endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="980a4-199">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="980a4-200">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como "Microsoft:*VMGUID* \\ *GUID*", em *que VMGUID* é a propriedade **Name** da instância do [**Msvm \_ ComputerSystem**](msvm-computersystem.md) associada a este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="980a4-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) instance associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="980a4-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="980a4-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-202">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="980a4-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-204">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="980a4-204">A display name for the object.</span></span> <span data-ttu-id="980a4-205">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="980a4-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="980a4-206">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="980a4-206">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-207">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980a4-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-209">A configuração de inicialização ou padrão de um administrador para o **enabledstate** de um elemento.</span><span class="sxs-lookup"><span data-stu-id="980a4-209">An administrator's default or startup configuration for the **EnabledState** of an element.</span></span> <span data-ttu-id="980a4-210">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="980a4-210">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="980a4-211">Valor</span><span class="sxs-lookup"><span data-stu-id="980a4-211">Value</span></span>                                                                        | <span data-ttu-id="980a4-212">Significado</span><span class="sxs-lookup"><span data-stu-id="980a4-212">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="980a4-213"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="980a4-213"><dt>7</dt></span></span> </dl> | <span data-ttu-id="980a4-214">Nenhum padrão</span><span class="sxs-lookup"><span data-stu-id="980a4-214">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="980a4-215">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="980a4-215">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-216">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980a4-216">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-218">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="980a4-218">The enabled and disabled states of an element.</span></span> <span data-ttu-id="980a4-219">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e é definida como 2 (habilitado) ou 3 (desabilitado).</span><span class="sxs-lookup"><span data-stu-id="980a4-219">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is either set to 2 (Enabled) or 3 (Disabled).</span></span>



| <span data-ttu-id="980a4-220">Valor</span><span class="sxs-lookup"><span data-stu-id="980a4-220">Value</span></span>                                                                        | <span data-ttu-id="980a4-221">Significado</span><span class="sxs-lookup"><span data-stu-id="980a4-221">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="980a4-222"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="980a4-222"><dt>2</dt></span></span> </dl> | <span data-ttu-id="980a4-223">habilitado</span><span class="sxs-lookup"><span data-stu-id="980a4-223">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="980a4-224"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="980a4-224"><dt>3</dt></span></span> </dl> | <span data-ttu-id="980a4-225">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="980a4-225">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="980a4-226">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="980a4-226">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-227">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="980a4-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-229">Indica se o erro relatado na propriedade **LastErrorCode** agora está apagado.</span><span class="sxs-lookup"><span data-stu-id="980a4-229">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="980a4-230">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="980a4-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="980a4-231">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="980a4-231">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-232">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="980a4-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-234">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado na propriedade **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="980a4-234">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="980a4-235">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="980a4-235">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="980a4-236">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="980a4-236">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-237">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980a4-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-239">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="980a4-239">The current health of the element.</span></span> <span data-ttu-id="980a4-240">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="980a4-240">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="980a4-241">Valor</span><span class="sxs-lookup"><span data-stu-id="980a4-241">Value</span></span>                                                                        | <span data-ttu-id="980a4-242">Significado</span><span class="sxs-lookup"><span data-stu-id="980a4-242">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="980a4-243"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="980a4-243"><dt>5</dt></span></span> </dl> | <span data-ttu-id="980a4-244">OK</span><span class="sxs-lookup"><span data-stu-id="980a4-244">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="980a4-245">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="980a4-245">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-246">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="980a4-246">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="980a4-247">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-248">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz de propriedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="980a4-248">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="980a4-249">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="980a4-249">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="980a4-250">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="980a4-250">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-251">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="980a4-251">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-253">A data e a hora em que o serviço de integração foi instalado na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="980a4-253">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="980a4-254">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="980a4-254">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="980a4-255">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="980a4-255">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-256">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="980a4-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-257">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="980a4-258">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="980a4-258">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="980a4-259">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="980a4-259">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="980a4-260">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="980a4-260">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="980a4-261">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="980a4-261">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-262">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="980a4-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-263">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-264">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="980a4-264">The last error code reported by the logical device.</span></span> <span data-ttu-id="980a4-265">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="980a4-265">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="980a4-266">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="980a4-266">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-267">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="980a4-267">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-268">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-269">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="980a4-269">This property has been deprecated.</span></span> <span data-ttu-id="980a4-270">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="980a4-270">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="980a4-271">**Nome**</span><span class="sxs-lookup"><span data-stu-id="980a4-271">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-272">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="980a4-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-273">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-274">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="980a4-274">The label by which the object is known.</span></span> <span data-ttu-id="980a4-275">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="980a4-275">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="980a4-276">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="980a4-276">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-277">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980a4-277">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-278">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-279">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="980a4-279">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="980a4-280">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="980a4-280">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="980a4-281">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="980a4-281">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="980a4-282"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="980a4-282"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-283"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="980a4-283"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-284"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="980a4-284"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-285"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="980a4-285"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-286"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="980a4-286"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-287"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="980a4-287"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-288"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="980a4-288"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-289"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="980a4-289"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-290"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="980a4-290"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-291"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="980a4-291"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-292"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="980a4-292"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-293"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="980a4-293"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-294"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="980a4-294"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-295"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="980a4-295"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-296"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="980a4-296"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-297"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="980a4-297"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-298"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="980a4-298"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="980a4-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="980a4-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="980a4-301">)</span><span class="sxs-lookup"><span data-stu-id="980a4-301">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="980a4-302">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="980a4-302">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-303">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980a4-303">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="980a4-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-305">O status atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="980a4-305">The current status of the element.</span></span> <span data-ttu-id="980a4-306">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="980a4-306">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="980a4-307">A seguir estão os valores possíveis para o  \[ valor da \] Propriedade OperationalStatus 0.</span><span class="sxs-lookup"><span data-stu-id="980a4-307">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="980a4-308">Valor</span><span class="sxs-lookup"><span data-stu-id="980a4-308">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="980a4-309">Significado</span><span class="sxs-lookup"><span data-stu-id="980a4-309">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="980a4-310"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="980a4-310"><dt>{ 2 }</dt></span></span> </dl>                                                                                                                                                                                                    |                                                                                                                                                                                                                                          |
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="980a4-311"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="980a4-311"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="980a4-312">O serviço está funcionando normalmente.</span><span class="sxs-lookup"><span data-stu-id="980a4-312">The service is operating normally.</span></span> <span data-ttu-id="980a4-313">Os  \[ valores de \] Propriedade OperationalStatus 1 e **StatusDescriptions** \[ 1 \] podem conter mais informações.</span><span class="sxs-lookup"><span data-stu-id="980a4-313">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="980a4-314"><dt>**Degradado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="980a4-314"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="980a4-315">O serviço está funcionando normalmente, mas o serviço convidado negocia uma versão de protocolo de comunicação compatível.</span><span class="sxs-lookup"><span data-stu-id="980a4-315">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="980a4-316">Os  \[ valores de \] Propriedade OperationalStatus 1 e **StatusDescriptions** \[ 1 \] podem conter mais informações.</span><span class="sxs-lookup"><span data-stu-id="980a4-316">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="980a4-317"><dt>**Erro não recuperável**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="980a4-317"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="980a4-318">O convidado não oferece suporte a uma versão de protocolo compatível.</span><span class="sxs-lookup"><span data-stu-id="980a4-318">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="980a4-319">Os  \[ valores de \] Propriedade OperationalStatus 1 e **StatusDescriptions** \[ 1 \] podem conter mais informações.</span><span class="sxs-lookup"><span data-stu-id="980a4-319">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="980a4-320"><dt>**Nenhum contato**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="980a4-320"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="980a4-321">O serviço convidado não está instalado ou ainda não foi contatado.</span><span class="sxs-lookup"><span data-stu-id="980a4-321">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="980a4-322"><dt>**Comunicação perdida**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="980a4-322"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="980a4-323">O serviço convidado não está mais respondendo normalmente.</span><span class="sxs-lookup"><span data-stu-id="980a4-323">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="980a4-324">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="980a4-324">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-325">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="980a4-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-326">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-327">O estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="980a4-327">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="980a4-328">Essa propriedade deve ser definida como **NULL** quando a propriedade **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="980a4-328">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="980a4-329">Essa propriedade é herdada de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e sempre é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="980a4-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="980a4-330">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="980a4-330">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-331">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="980a4-331">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="980a4-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-333">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="980a4-333">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="980a4-334">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="980a4-334">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="980a4-335">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="980a4-335">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-336">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980a4-336">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="980a4-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-338">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="980a4-338">The power management capabilities of the device.</span></span> <span data-ttu-id="980a4-339">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="980a4-339">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="980a4-340">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="980a4-340">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-341">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="980a4-341">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-342">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-343">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="980a4-343">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="980a4-344">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="980a4-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="980a4-345">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="980a4-345">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-346">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="980a4-346">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-348">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="980a4-348">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="980a4-349">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="980a4-349">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="980a4-350">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="980a4-350">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-351">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980a4-351">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-352">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-353">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="980a4-353">Provides high level status information.</span></span> <span data-ttu-id="980a4-354">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="980a4-354">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="980a4-355">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="980a4-355">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="980a4-356">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="980a4-356">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="980a4-357"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="980a4-357"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-358"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="980a4-358"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-359"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="980a4-359"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-360"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="980a4-360"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-361"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="980a4-361"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="980a4-362"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="980a4-362"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="980a4-363">)</span><span class="sxs-lookup"><span data-stu-id="980a4-363">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="980a4-364">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="980a4-364">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-365">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980a4-365">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-366">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-367">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="980a4-367">The last requested or desired state for the element.</span></span> <span data-ttu-id="980a4-368">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="980a4-368">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="980a4-369">Valor</span><span class="sxs-lookup"><span data-stu-id="980a4-369">Value</span></span>                                                                         | <span data-ttu-id="980a4-370">Significado</span><span class="sxs-lookup"><span data-stu-id="980a4-370">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="980a4-371"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="980a4-371"><dt>12</dt></span></span> </dl> | <span data-ttu-id="980a4-372">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="980a4-372">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="980a4-373">**Status**</span><span class="sxs-lookup"><span data-stu-id="980a4-373">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-374">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="980a4-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-376">Uma cadeia de caracteres que especifica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="980a4-376">A string that specifies the current status of the object.</span></span> <span data-ttu-id="980a4-377">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) , mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="980a4-377">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="980a4-378">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="980a4-378">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-379">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="980a4-379">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="980a4-380">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-381">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="980a4-381">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="980a4-382">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="980a4-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="980a4-383">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="980a4-383">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-384">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980a4-384">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-385">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-386">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="980a4-386">The current state of the logical device.</span></span> <span data-ttu-id="980a4-387">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="980a4-387">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="980a4-388">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="980a4-388">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-389">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="980a4-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-390">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-391">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="980a4-391">The creation class name of the scoping system.</span></span> <span data-ttu-id="980a4-392">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="980a4-392">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="980a4-393">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="980a4-393">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-394">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="980a4-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-395">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-396">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="980a4-396">The name of the scoping system.</span></span> <span data-ttu-id="980a4-397">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="980a4-397">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="980a4-398">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="980a4-398">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-399">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="980a4-399">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-400">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-401">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="980a4-401">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="980a4-402">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="980a4-402">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="980a4-403">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="980a4-403">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-404">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="980a4-404">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-405">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-406">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="980a4-406">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="980a4-407">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="980a4-407">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="980a4-408">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="980a4-408">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980a4-409">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980a4-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980a4-410">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="980a4-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980a4-411">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="980a4-411">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="980a4-412">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="980a4-412">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="980a4-413">Valor</span><span class="sxs-lookup"><span data-stu-id="980a4-413">Value</span></span>                                                                         | <span data-ttu-id="980a4-414">Significado</span><span class="sxs-lookup"><span data-stu-id="980a4-414">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="980a4-415"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="980a4-415"><dt>12</dt></span></span> </dl> | <span data-ttu-id="980a4-416">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="980a4-416">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="980a4-417">Comentários</span><span class="sxs-lookup"><span data-stu-id="980a4-417">Remarks</span></span>

<span data-ttu-id="980a4-418">O acesso à classe **Msvm \_ TimeSyncComponent** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="980a4-418">Access to the **Msvm\_TimeSyncComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="980a4-419">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="980a4-419">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="980a4-420">Requisitos</span><span class="sxs-lookup"><span data-stu-id="980a4-420">Requirements</span></span>



| <span data-ttu-id="980a4-421">Requisito</span><span class="sxs-lookup"><span data-stu-id="980a4-421">Requirement</span></span> | <span data-ttu-id="980a4-422">Valor</span><span class="sxs-lookup"><span data-stu-id="980a4-422">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="980a4-423">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="980a4-423">Minimum supported client</span></span><br/> | <span data-ttu-id="980a4-424">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="980a4-424">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="980a4-425">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="980a4-425">Minimum supported server</span></span><br/> | <span data-ttu-id="980a4-426">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="980a4-426">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="980a4-427">Namespace</span><span class="sxs-lookup"><span data-stu-id="980a4-427">Namespace</span></span><br/>                | <span data-ttu-id="980a4-428">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="980a4-428">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="980a4-429">MOF</span><span class="sxs-lookup"><span data-stu-id="980a4-429">MOF</span></span><br/>                      | <dl> <span data-ttu-id="980a4-430"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="980a4-430"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="980a4-431">DLL</span><span class="sxs-lookup"><span data-stu-id="980a4-431">DLL</span></span><br/>                      | <dl> <span data-ttu-id="980a4-432"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="980a4-432"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="980a4-433">Confira também</span><span class="sxs-lookup"><span data-stu-id="980a4-433">See also</span></span>

<dl> <dt>

[<span data-ttu-id="980a4-434">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="980a4-434">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="980a4-435">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="980a4-435">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

