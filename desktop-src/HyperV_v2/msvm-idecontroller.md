---
description: Representa um controlador IDE.
ms.assetid: DFD4D90E-CA91-42B3-AC88-9E9D26089C36
title: Classe Msvm_IDEController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_IDEController
- Msvm_IDEController.SetPowerState
- Msvm_IDEController.EnableDevice
- Msvm_IDEController.OnlineDevice
- Msvm_IDEController.QuiesceDevice
- Msvm_IDEController.SaveProperties
- Msvm_IDEController.RestoreProperties
- Msvm_IDEController.InstanceID
- Msvm_IDEController.Caption
- Msvm_IDEController.Description
- Msvm_IDEController.ElementName
- Msvm_IDEController.InstallDate
- Msvm_IDEController.Name
- Msvm_IDEController.OperationalStatus
- Msvm_IDEController.StatusDescriptions
- Msvm_IDEController.Status
- Msvm_IDEController.HealthState
- Msvm_IDEController.CommunicationStatus
- Msvm_IDEController.DetailedStatus
- Msvm_IDEController.OperatingStatus
- Msvm_IDEController.PrimaryStatus
- Msvm_IDEController.EnabledState
- Msvm_IDEController.OtherEnabledState
- Msvm_IDEController.RequestedState
- Msvm_IDEController.EnabledDefault
- Msvm_IDEController.TimeOfLastStateChange
- Msvm_IDEController.AvailableRequestedStates
- Msvm_IDEController.TransitioningToState
- Msvm_IDEController.SystemCreationClassName
- Msvm_IDEController.SystemName
- Msvm_IDEController.CreationClassName
- Msvm_IDEController.DeviceID
- Msvm_IDEController.PowerManagementSupported
- Msvm_IDEController.PowerManagementCapabilities
- Msvm_IDEController.Availability
- Msvm_IDEController.StatusInfo
- Msvm_IDEController.LastErrorCode
- Msvm_IDEController.ErrorDescription
- Msvm_IDEController.ErrorCleared
- Msvm_IDEController.OtherIdentifyingInfo
- Msvm_IDEController.PowerOnHours
- Msvm_IDEController.TotalPowerOnHours
- Msvm_IDEController.IdentifyingDescriptions
- Msvm_IDEController.AdditionalAvailability
- Msvm_IDEController.MaxQuiesceTime
- Msvm_IDEController.TimeOfLastReset
- Msvm_IDEController.ProtocolSupported
- Msvm_IDEController.MaxNumberControlled
- Msvm_IDEController.ProtocolDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 25da1bddfa029ca5a6892006283e322d91a328a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768751"
---
# <a name="msvm_idecontroller-class"></a><span data-ttu-id="c24c1-103">\_Classe Msvm IDEController</span><span class="sxs-lookup"><span data-stu-id="c24c1-103">Msvm\_IDEController class</span></span>

<span data-ttu-id="c24c1-104">Representa um controlador IDE.</span><span class="sxs-lookup"><span data-stu-id="c24c1-104">Represents an IDE controller.</span></span> <span data-ttu-id="c24c1-105">Essa classe pode dar suporte a até quatro unidades anexadas ao controlador.</span><span class="sxs-lookup"><span data-stu-id="c24c1-105">This class can support up to four drives attached to the controller.</span></span> <span data-ttu-id="c24c1-106">O controlador IDE é corrigido na máquina virtual e, portanto, não tem um pool de recursos associado a ele.</span><span class="sxs-lookup"><span data-stu-id="c24c1-106">The IDE controller is fixed in the virtual machine and therefore does not have a resource pool associated with it.</span></span>

> [!Note]  
> <span data-ttu-id="c24c1-107">Essa classe não está disponível para máquinas virtuais de geração 2.</span><span class="sxs-lookup"><span data-stu-id="c24c1-107">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="c24c1-108">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c24c1-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c24c1-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c24c1-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_IDEController : CIM_IDEController
{
  string   InstanceID;
  string   Caption;
  string   Description = "Microsoft Virtual IDE Controller";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
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
  string   CreationClassName = "Msvm_IDEController";
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
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 37;
  uint32   MaxNumberControlled = 2;
  string   ProtocolDescription = "IDE";
};
```

## <a name="members"></a><span data-ttu-id="c24c1-110">Membros</span><span class="sxs-lookup"><span data-stu-id="c24c1-110">Members</span></span>

<span data-ttu-id="c24c1-111">A classe **Msvm \_ IDEController** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c24c1-111">The **Msvm\_IDEController** class has these types of members:</span></span>

-   [<span data-ttu-id="c24c1-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="c24c1-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="c24c1-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c24c1-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c24c1-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="c24c1-114">Methods</span></span>

<span data-ttu-id="c24c1-115">A classe **Msvm \_ IDEController** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c24c1-115">The **Msvm\_IDEController** class has these methods.</span></span>



| <span data-ttu-id="c24c1-116">Método</span><span class="sxs-lookup"><span data-stu-id="c24c1-116">Method</span></span>                                                              | <span data-ttu-id="c24c1-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="c24c1-117">Description</span></span>                              |
|:--------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="c24c1-118">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="c24c1-118">**EnableDevice**</span></span>                                                    | <span data-ttu-id="c24c1-119">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="c24c1-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c24c1-120">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="c24c1-120">**OnlineDevice**</span></span>                                                    | <span data-ttu-id="c24c1-121">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="c24c1-121">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c24c1-122">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="c24c1-122">**QuiesceDevice**</span></span>                                                   | <span data-ttu-id="c24c1-123">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="c24c1-123">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="c24c1-124">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="c24c1-124">**RequestStateChange**</span></span>](msvm-idecontroller-requeststatechange.md) | <span data-ttu-id="c24c1-125">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="c24c1-125">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="c24c1-126">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="c24c1-126">**Reset**</span></span>](msvm-idecontroller-reset.md)                           | <span data-ttu-id="c24c1-127">Redefine o dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="c24c1-127">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="c24c1-128">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="c24c1-128">**RestoreProperties**</span></span>                                               | <span data-ttu-id="c24c1-129">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="c24c1-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c24c1-130">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="c24c1-130">**SaveProperties**</span></span>                                                  | <span data-ttu-id="c24c1-131">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="c24c1-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c24c1-132">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c24c1-132">**SetPowerState**</span></span>                                                   | <span data-ttu-id="c24c1-133">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="c24c1-133">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c24c1-134">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c24c1-134">Properties</span></span>

<span data-ttu-id="c24c1-135">A classe **Msvm \_ IDEController** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c24c1-135">The **Msvm\_IDEController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c24c1-136">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="c24c1-136">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-137">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c24c1-137">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-139">Qualquer disponibilidade e status adicionais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c24c1-139">Any additional availability and status of the device.</span></span> <span data-ttu-id="c24c1-140">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c24c1-140">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-141">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="c24c1-141">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-142">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c24c1-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-144">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c24c1-144">The primary availability and status of the device.</span></span> <span data-ttu-id="c24c1-145">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c24c1-145">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-146">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="c24c1-146">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-147">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c24c1-147">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-149">Indica os valores possíveis para o parâmetro *requestedstate* do método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="c24c1-149">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="c24c1-150">Os valores listados serão um subconjunto dos valores contidos na propriedade **RequestedStatesSupported** da instância associada do **CIM \_ EnabledLogicalElementCapabilities**, em que os valores selecionados são uma função do estado atual do objeto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c24c1-150">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="c24c1-151">Essa propriedade pode ser não **nula** se uma implementação for capaz de anunciar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="c24c1-151">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="c24c1-152">Essa propriedade será **nula** se uma implementação não puder determinar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="c24c1-152">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="c24c1-153">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c24c1-153">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-154">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="c24c1-154">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c24c1-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-157">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="c24c1-157">A short description of the object.</span></span> <span data-ttu-id="c24c1-158">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c24c1-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>



| <span data-ttu-id="c24c1-159">Valor</span><span class="sxs-lookup"><span data-stu-id="c24c1-159">Value</span></span>                                                                                         | <span data-ttu-id="c24c1-160">Significado</span><span class="sxs-lookup"><span data-stu-id="c24c1-160">Meaning</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="c24c1-161"><dt>"Controlador IDE 0"</dt></span><span class="sxs-lookup"><span data-stu-id="c24c1-161"><dt>"IDE Controller 0"</dt></span></span> </dl> | <span data-ttu-id="c24c1-162">A instância representa o controlador primário.</span><span class="sxs-lookup"><span data-stu-id="c24c1-162">The instance represents the primary controller.</span></span><br/>   |
| <dl> <span data-ttu-id="c24c1-163"><dt>"Controlador IDE 1"</dt></span><span class="sxs-lookup"><span data-stu-id="c24c1-163"><dt>"IDE Controller 1"</dt></span></span> </dl> | <span data-ttu-id="c24c1-164">A instância representa o controlador secundário.</span><span class="sxs-lookup"><span data-stu-id="c24c1-164">The instance represents the secondary controller.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c24c1-165">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="c24c1-165">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-166">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c24c1-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-168">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="c24c1-168">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="c24c1-169">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="c24c1-169">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c24c1-170">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c24c1-170">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c24c1-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-172">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c24c1-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-174">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="c24c1-174">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c24c1-175">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c24c1-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-176">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c24c1-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c24c1-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-179">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="c24c1-179">A description of the object.</span></span> <span data-ttu-id="c24c1-180">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c24c1-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="c24c1-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-182">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c24c1-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-184">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="c24c1-184">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="c24c1-185">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="c24c1-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c24c1-186">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c24c1-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-187">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c24c1-187">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-188">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c24c1-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-190">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como "Microsoft:*GUID*- \\ *specific-data*".</span><span class="sxs-lookup"><span data-stu-id="c24c1-190">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-191">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c24c1-191">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c24c1-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-194">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="c24c1-194">A display name for the object.</span></span> <span data-ttu-id="c24c1-195">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c24c1-195">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>



| <span data-ttu-id="c24c1-196">Valor</span><span class="sxs-lookup"><span data-stu-id="c24c1-196">Value</span></span>                                                                                         | <span data-ttu-id="c24c1-197">Significado</span><span class="sxs-lookup"><span data-stu-id="c24c1-197">Meaning</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="c24c1-198"><dt>"Controlador IDE 0"</dt></span><span class="sxs-lookup"><span data-stu-id="c24c1-198"><dt>"IDE Controller 0"</dt></span></span> </dl> | <span data-ttu-id="c24c1-199">A instância representa o controlador primário.</span><span class="sxs-lookup"><span data-stu-id="c24c1-199">The instance represents the primary controller.</span></span><br/>   |
| <dl> <span data-ttu-id="c24c1-200"><dt>"Controlador IDE 1"</dt></span><span class="sxs-lookup"><span data-stu-id="c24c1-200"><dt>"IDE Controller 1"</dt></span></span> </dl> | <span data-ttu-id="c24c1-201">A instância representa o controlador secundário.</span><span class="sxs-lookup"><span data-stu-id="c24c1-201">The instance represents the secondary controller.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c24c1-202">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="c24c1-202">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-203">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c24c1-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-205">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="c24c1-205">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="c24c1-206">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c24c1-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-207">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="c24c1-207">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-208">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c24c1-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-210">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="c24c1-210">The enabled and disabled states of an element.</span></span> <span data-ttu-id="c24c1-211">Ele também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="c24c1-211">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="c24c1-212">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c24c1-212">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-213">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="c24c1-213">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-214">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c24c1-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-216">Indica se o erro relatado em **LastErrorCode** agora está limpo.</span><span class="sxs-lookup"><span data-stu-id="c24c1-216">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="c24c1-217">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="c24c1-217">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-218">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c24c1-218">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-219">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c24c1-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-221">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="c24c1-221">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="c24c1-222">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="c24c1-222">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-223">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="c24c1-223">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-224">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c24c1-224">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-225">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-226">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="c24c1-226">The current health of the element.</span></span> <span data-ttu-id="c24c1-227">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="c24c1-227">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="c24c1-228">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="c24c1-228">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="c24c1-229">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c24c1-229">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-230">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c24c1-230">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-231">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c24c1-231">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-232">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-233">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz de propriedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="c24c1-233">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="c24c1-234">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="c24c1-234">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-235">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c24c1-235">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-236">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c24c1-236">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-237">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-238">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="c24c1-238">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="c24c1-239">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c24c1-239">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-240">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c24c1-240">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-241">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c24c1-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-242">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-243">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="c24c1-243">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-244">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="c24c1-244">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c24c1-245">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c24c1-245">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-246">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c24c1-246">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-247">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c24c1-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-249">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c24c1-249">The last error code reported by the logical device.</span></span> <span data-ttu-id="c24c1-250">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="c24c1-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-251">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="c24c1-251">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-252">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c24c1-252">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-253">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-254">O número máximo de entidades diretamente endereçáveis que são suportadas por este controlador.</span><span class="sxs-lookup"><span data-stu-id="c24c1-254">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="c24c1-255">Um valor de 0 deve ser usado se o número for desconhecido ou ilimitado.</span><span class="sxs-lookup"><span data-stu-id="c24c1-255">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="c24c1-256">O protocolo usado pelo controlador para acessar dispositivos controlados.</span><span class="sxs-lookup"><span data-stu-id="c24c1-256">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="c24c1-257">Essa propriedade é herdada [**do \_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="c24c1-257">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-258">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="c24c1-258">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-259">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c24c1-259">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-260">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-261">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="c24c1-261">This property has been deprecated.</span></span> <span data-ttu-id="c24c1-262">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="c24c1-262">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-263">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c24c1-263">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-264">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c24c1-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-265">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-266">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="c24c1-266">The label by which the object is known.</span></span> <span data-ttu-id="c24c1-267">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é a mesma que a propriedade **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="c24c1-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-268">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="c24c1-268">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-269">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c24c1-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-271">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="c24c1-271">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="c24c1-272">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="c24c1-272">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c24c1-273">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c24c1-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-274">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="c24c1-274">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-275">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c24c1-275">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-276">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-277">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="c24c1-277">The current statuses of the object.</span></span> <span data-ttu-id="c24c1-278">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c24c1-278">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-279">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="c24c1-279">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-280">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c24c1-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-281">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-282">O estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="c24c1-282">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="c24c1-283">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="c24c1-283">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="c24c1-284">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c24c1-284">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-285">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="c24c1-285">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-286">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c24c1-286">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-287">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-288">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c24c1-288">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="c24c1-289">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c24c1-289">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-290">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c24c1-290">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-291">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c24c1-291">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-292">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-293">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c24c1-293">The power management capabilities of the device.</span></span> <span data-ttu-id="c24c1-294">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="c24c1-294">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-295">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="c24c1-295">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-296">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c24c1-296">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-297">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-298">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="c24c1-298">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="c24c1-299">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="c24c1-299">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-300">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="c24c1-300">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-301">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c24c1-301">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-303">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="c24c1-303">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="c24c1-304">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="c24c1-304">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-305">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="c24c1-305">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-306">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c24c1-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-307">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-308">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="c24c1-308">Provides high level status information.</span></span> <span data-ttu-id="c24c1-309">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer informações de status de integridade detalhadas e de alto nível para o elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="c24c1-309">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="c24c1-310">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="c24c1-310">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c24c1-311">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c24c1-311">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-312">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="c24c1-312">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-313">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c24c1-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-315">Uma cadeia de caracteres que fornece mais informações relacionadas ao protocolo suportado pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="c24c1-315">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="c24c1-316">Essa propriedade é herdada [**do \_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="c24c1-316">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-317">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="c24c1-317">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-318">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c24c1-318">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-319">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-320">O protocolo usado pelo controlador para acessar dispositivos controlados.</span><span class="sxs-lookup"><span data-stu-id="c24c1-320">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="c24c1-321">Essa propriedade é herdada [**do \_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="c24c1-321">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>



| <span data-ttu-id="c24c1-322">Valor</span><span class="sxs-lookup"><span data-stu-id="c24c1-322">Value</span></span>                                                                         | <span data-ttu-id="c24c1-323">Significado</span><span class="sxs-lookup"><span data-stu-id="c24c1-323">Meaning</span></span>        |
|-------------------------------------------------------------------------------|----------------|
| <dl> <span data-ttu-id="c24c1-324"><dt>37</dt></span><span class="sxs-lookup"><span data-stu-id="c24c1-324"><dt>37</dt></span></span> </dl> | <span data-ttu-id="c24c1-325">IDE</span><span class="sxs-lookup"><span data-stu-id="c24c1-325">IDE</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c24c1-326">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="c24c1-326">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-327">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c24c1-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-329">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="c24c1-329">The last requested or desired state for the element.</span></span> <span data-ttu-id="c24c1-330">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="c24c1-330">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="c24c1-331">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="c24c1-331">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="c24c1-332">Uma instância específica de um elemento lógico habilitado pode não dar suporte a **RequestedStateChange**.</span><span class="sxs-lookup"><span data-stu-id="c24c1-332">A particular instance of an enabled logical element might not support **RequestedStateChange**.</span></span> <span data-ttu-id="c24c1-333">Se isso ocorrer, o valor 12 (não aplicável) será usado.</span><span class="sxs-lookup"><span data-stu-id="c24c1-333">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="c24c1-334">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c24c1-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-335">**Status**</span><span class="sxs-lookup"><span data-stu-id="c24c1-335">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-336">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c24c1-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-338">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c24c1-338">The current status of the object.</span></span> <span data-ttu-id="c24c1-339">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="c24c1-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-340">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c24c1-340">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-341">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c24c1-341">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-342">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-343">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="c24c1-343">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="c24c1-344">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c24c1-344">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-345">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c24c1-345">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-346">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c24c1-346">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-348">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c24c1-348">The current state of the logical device.</span></span> <span data-ttu-id="c24c1-349">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="c24c1-349">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-350">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c24c1-350">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-351">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c24c1-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-352">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-353">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="c24c1-353">The scoping system's creation class name.</span></span> <span data-ttu-id="c24c1-354">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c24c1-354">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-355">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c24c1-355">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-356">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c24c1-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-357">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-358">O identificador exclusivo para a máquina virtual de escopo.</span><span class="sxs-lookup"><span data-stu-id="c24c1-358">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="c24c1-359">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c24c1-359">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-360">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="c24c1-360">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-361">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c24c1-361">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-362">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-363">A última vez em que a máquina virtual estava ligada.</span><span class="sxs-lookup"><span data-stu-id="c24c1-363">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="c24c1-364">Essa propriedade é herdada [**do \_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="c24c1-364">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-365">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="c24c1-365">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-366">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c24c1-366">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-367">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-368">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="c24c1-368">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="c24c1-369">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c24c1-369">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-370">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="c24c1-370">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-371">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c24c1-371">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-372">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-373">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="c24c1-373">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="c24c1-374">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="c24c1-374">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c24c1-375">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="c24c1-375">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c24c1-376">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c24c1-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c24c1-377">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c24c1-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c24c1-378">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="c24c1-378">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="c24c1-379">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="c24c1-379">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c24c1-380">Comentários</span><span class="sxs-lookup"><span data-stu-id="c24c1-380">Remarks</span></span>

<span data-ttu-id="c24c1-381">O acesso à classe **Msvm \_ IDEController** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="c24c1-381">Access to the **Msvm\_IDEController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c24c1-382">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c24c1-382">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c24c1-383">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c24c1-383">Requirements</span></span>



| <span data-ttu-id="c24c1-384">Requisito</span><span class="sxs-lookup"><span data-stu-id="c24c1-384">Requirement</span></span> | <span data-ttu-id="c24c1-385">Valor</span><span class="sxs-lookup"><span data-stu-id="c24c1-385">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c24c1-386">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c24c1-386">Minimum supported client</span></span><br/> | <span data-ttu-id="c24c1-387">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c24c1-387">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c24c1-388">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c24c1-388">Minimum supported server</span></span><br/> | <span data-ttu-id="c24c1-389">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c24c1-389">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c24c1-390">Namespace</span><span class="sxs-lookup"><span data-stu-id="c24c1-390">Namespace</span></span><br/>                | <span data-ttu-id="c24c1-391">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="c24c1-391">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c24c1-392">MOF</span><span class="sxs-lookup"><span data-stu-id="c24c1-392">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c24c1-393"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c24c1-393"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c24c1-394">DLL</span><span class="sxs-lookup"><span data-stu-id="c24c1-394">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c24c1-395"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c24c1-395"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c24c1-396">Confira também</span><span class="sxs-lookup"><span data-stu-id="c24c1-396">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c24c1-397">**\_IDECONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="c24c1-397">**CIM\_IDEController**</span></span>](cim-idecontroller.md)
</dt> <dt>

<span data-ttu-id="c24c1-398">[**\_IDECONTROLLER CIM**](/previous-versions//cc136863(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c24c1-398">[**CIM\_IDEController**](/previous-versions//cc136863(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c24c1-399">Classes de armazenamento</span><span class="sxs-lookup"><span data-stu-id="c24c1-399">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

