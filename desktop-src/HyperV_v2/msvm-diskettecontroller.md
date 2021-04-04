---
description: Representa o controlador de disquete na máquina virtual.
ms.assetid: 38A19BF3-0E8F-4DCE-B2DB-B2E3F8100E00
title: Classe Msvm_DisketteController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteController
- Msvm_DisketteController.SetPowerState
- Msvm_DisketteController.EnableDevice
- Msvm_DisketteController.OnlineDevice
- Msvm_DisketteController.QuiesceDevice
- Msvm_DisketteController.SaveProperties
- Msvm_DisketteController.RestoreProperties
- Msvm_DisketteController.InstanceID
- Msvm_DisketteController.Caption
- Msvm_DisketteController.Description
- Msvm_DisketteController.ElementName
- Msvm_DisketteController.InstallDate
- Msvm_DisketteController.Name
- Msvm_DisketteController.OperationalStatus
- Msvm_DisketteController.StatusDescriptions
- Msvm_DisketteController.Status
- Msvm_DisketteController.HealthState
- Msvm_DisketteController.CommunicationStatus
- Msvm_DisketteController.DetailedStatus
- Msvm_DisketteController.OperatingStatus
- Msvm_DisketteController.PrimaryStatus
- Msvm_DisketteController.EnabledState
- Msvm_DisketteController.OtherEnabledState
- Msvm_DisketteController.RequestedState
- Msvm_DisketteController.EnabledDefault
- Msvm_DisketteController.TimeOfLastStateChange
- Msvm_DisketteController.AvailableRequestedStates
- Msvm_DisketteController.TransitioningToState
- Msvm_DisketteController.SystemCreationClassName
- Msvm_DisketteController.SystemName
- Msvm_DisketteController.CreationClassName
- Msvm_DisketteController.DeviceID
- Msvm_DisketteController.PowerManagementSupported
- Msvm_DisketteController.PowerManagementCapabilities
- Msvm_DisketteController.Availability
- Msvm_DisketteController.StatusInfo
- Msvm_DisketteController.LastErrorCode
- Msvm_DisketteController.ErrorDescription
- Msvm_DisketteController.ErrorCleared
- Msvm_DisketteController.OtherIdentifyingInfo
- Msvm_DisketteController.PowerOnHours
- Msvm_DisketteController.TotalPowerOnHours
- Msvm_DisketteController.IdentifyingDescriptions
- Msvm_DisketteController.AdditionalAvailability
- Msvm_DisketteController.MaxQuiesceTime
- Msvm_DisketteController.TimeOfLastReset
- Msvm_DisketteController.ProtocolSupported
- Msvm_DisketteController.MaxNumberControlled
- Msvm_DisketteController.ProtocolDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f1e4e731464e25dc8e871ebd17cdcddd4e262673
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647068"
---
# <a name="msvm_diskettecontroller-class"></a><span data-ttu-id="e6f75-103">\_Classe Msvm DisketteController</span><span class="sxs-lookup"><span data-stu-id="e6f75-103">Msvm\_DisketteController class</span></span>

<span data-ttu-id="e6f75-104">Representa o controlador de disquete na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e6f75-104">Represents the floppy controller in the virtual machine.</span></span> <span data-ttu-id="e6f75-105">O controlador de disquete é fixo, portanto, não há nenhum pool de recursos associado a ele.</span><span class="sxs-lookup"><span data-stu-id="e6f75-105">The floppy controller is fixed, therefore there is no resource pool associated with it.</span></span>

<span data-ttu-id="e6f75-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e6f75-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6f75-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6f75-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DisketteController : CIM_Controller
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
  string   CreationClassName = "Msvm_DisketteController";
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
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 7;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Diskette Protocol";
};
```

## <a name="members"></a><span data-ttu-id="e6f75-108">Membros</span><span class="sxs-lookup"><span data-stu-id="e6f75-108">Members</span></span>

<span data-ttu-id="e6f75-109">A classe **Msvm \_ DisketteController** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e6f75-109">The **Msvm\_DisketteController** class has these types of members:</span></span>

-   [<span data-ttu-id="e6f75-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="e6f75-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="e6f75-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e6f75-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e6f75-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="e6f75-112">Methods</span></span>

<span data-ttu-id="e6f75-113">A classe **Msvm \_ DisketteController** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e6f75-113">The **Msvm\_DisketteController** class has these methods.</span></span>



| <span data-ttu-id="e6f75-114">Método</span><span class="sxs-lookup"><span data-stu-id="e6f75-114">Method</span></span>                                                                   | <span data-ttu-id="e6f75-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6f75-115">Description</span></span>                              |
|:-------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="e6f75-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="e6f75-116">**EnableDevice**</span></span>                                                         | <span data-ttu-id="e6f75-117">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="e6f75-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e6f75-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="e6f75-118">**OnlineDevice**</span></span>                                                         | <span data-ttu-id="e6f75-119">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="e6f75-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e6f75-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="e6f75-120">**QuiesceDevice**</span></span>                                                        | <span data-ttu-id="e6f75-121">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="e6f75-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="e6f75-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="e6f75-122">**RequestStateChange**</span></span>](msvm-diskettecontroller-requeststatechange.md) | <span data-ttu-id="e6f75-123">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="e6f75-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="e6f75-124">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="e6f75-124">**Reset**</span></span>](msvm-diskettecontroller-reset.md)                           | <span data-ttu-id="e6f75-125">Redefine o dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="e6f75-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="e6f75-126">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="e6f75-126">**RestoreProperties**</span></span>                                                    | <span data-ttu-id="e6f75-127">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="e6f75-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e6f75-128">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="e6f75-128">**SaveProperties**</span></span>                                                       | <span data-ttu-id="e6f75-129">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="e6f75-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e6f75-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e6f75-130">**SetPowerState**</span></span>                                                        | <span data-ttu-id="e6f75-131">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="e6f75-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e6f75-132">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e6f75-132">Properties</span></span>

<span data-ttu-id="e6f75-133">A classe **Msvm \_ DisketteController** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e6f75-133">The **Msvm\_DisketteController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e6f75-134">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="e6f75-134">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-135">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6f75-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-137">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como 6 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="e6f75-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-138">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="e6f75-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-139">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6f75-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-141">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como 6 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="e6f75-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-142">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="e6f75-142">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-143">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6f75-143">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-145">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="e6f75-145">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="e6f75-146">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e6f75-146">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-147">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="e6f75-147">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-148">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6f75-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-150">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="e6f75-150">A short description of the object.</span></span> <span data-ttu-id="e6f75-151">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e6f75-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-152">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="e6f75-152">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-153">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6f75-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-155">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="e6f75-155">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="e6f75-156">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="e6f75-156">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e6f75-157">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e6f75-157">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e6f75-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e6f75-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-159"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="e6f75-159"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-160"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="e6f75-160"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-161"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="e6f75-161"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-162"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="e6f75-162"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-163"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="e6f75-163"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-164"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="e6f75-164"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e6f75-165">)</span><span class="sxs-lookup"><span data-stu-id="e6f75-165">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e6f75-166">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e6f75-166">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6f75-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-169">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="e6f75-169">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e6f75-170">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como "Msvm \_ DisketteController".</span><span class="sxs-lookup"><span data-stu-id="e6f75-170">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Msvm\_DisketteController".</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-171">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e6f75-171">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-172">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6f75-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-174">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="e6f75-174">A description of the object.</span></span> <span data-ttu-id="e6f75-175">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e6f75-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-176">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="e6f75-176">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-177">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6f75-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-179">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="e6f75-179">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="e6f75-180">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="e6f75-180">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e6f75-181">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e6f75-181">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e6f75-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="e6f75-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="e6f75-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="e6f75-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="e6f75-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="e6f75-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="e6f75-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="e6f75-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="e6f75-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e6f75-190">)</span><span class="sxs-lookup"><span data-stu-id="e6f75-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e6f75-191">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="e6f75-191">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6f75-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-194">Um endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e6f75-194">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="e6f75-195">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e6f75-195">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-196">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e6f75-196">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-197">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6f75-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-199">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="e6f75-199">A display name for the object.</span></span> <span data-ttu-id="e6f75-200">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e6f75-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-201">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="e6f75-201">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-202">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6f75-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-204">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="e6f75-204">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="e6f75-205">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e6f75-205">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-206">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="e6f75-206">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-207">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6f75-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-209">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="e6f75-209">The enabled and disabled states of an element.</span></span> <span data-ttu-id="e6f75-210">Ele também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="e6f75-210">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="e6f75-211">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e6f75-211">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="e6f75-212">Valor</span><span class="sxs-lookup"><span data-stu-id="e6f75-212">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="e6f75-213">Significado</span><span class="sxs-lookup"><span data-stu-id="e6f75-213">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="e6f75-214"><dt></dt> <dt>0</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="e6f75-214"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="e6f75-215">Não foi possível determinar o estado do elemento.</span><span class="sxs-lookup"><span data-stu-id="e6f75-215">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="e6f75-216"><dt>**Outros**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e6f75-216"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="e6f75-217"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e6f75-217"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="e6f75-218">O elemento está em execução.</span><span class="sxs-lookup"><span data-stu-id="e6f75-218">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="e6f75-219"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e6f75-219"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="e6f75-220">O elemento está desativado.</span><span class="sxs-lookup"><span data-stu-id="e6f75-220">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="e6f75-221"><dt>**Desligando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e6f75-221"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="e6f75-222">O elemento está no processo de ir para um estado desabilitado.</span><span class="sxs-lookup"><span data-stu-id="e6f75-222">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="e6f75-223"><dt>**Não aplicável**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e6f75-223"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="e6f75-224">O elemento não dá suporte a ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="e6f75-224">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="e6f75-225"><dt>**Habilitado, mas offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e6f75-225"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="e6f75-226">O elemento pode estar concluindo comandos e removerá todas as novas solicitações.</span><span class="sxs-lookup"><span data-stu-id="e6f75-226">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="e6f75-227"><dt>**No teste**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="e6f75-227"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="e6f75-228">O elemento está em um estado de teste.</span><span class="sxs-lookup"><span data-stu-id="e6f75-228">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="e6f75-229"><dt>**Adiado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="e6f75-229"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="e6f75-230">O elemento pode estar concluindo comandos, mas colocará todas as novas solicitações na fila.</span><span class="sxs-lookup"><span data-stu-id="e6f75-230">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="e6f75-231"><dt>**Desativar**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="e6f75-231"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="e6f75-232">O elemento está habilitado, mas está em um modo restrito.</span><span class="sxs-lookup"><span data-stu-id="e6f75-232">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="e6f75-233">O comportamento do elemento é semelhante ao estado habilitado (2), mas processa apenas um conjunto restrito de comandos.</span><span class="sxs-lookup"><span data-stu-id="e6f75-233">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="e6f75-234">Todas as outras solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="e6f75-234">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="e6f75-235"><dt>**Iniciando**</dt> em <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="e6f75-235"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="e6f75-236">O elemento está no processo de ir para um estado habilitado (2).</span><span class="sxs-lookup"><span data-stu-id="e6f75-236">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="e6f75-237">Novas solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="e6f75-237">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="e6f75-238">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="e6f75-238">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-239">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e6f75-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-240">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-241">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="e6f75-241">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-242">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e6f75-242">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-243">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6f75-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-245">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="e6f75-245">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-246">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="e6f75-246">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-247">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6f75-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-249">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="e6f75-249">The current health of the element.</span></span> <span data-ttu-id="e6f75-250">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="e6f75-250">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="e6f75-251">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="e6f75-251">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="e6f75-252">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e6f75-252">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-253">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e6f75-253">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-254">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6f75-254">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-255">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-256">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e6f75-256">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-257">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e6f75-257">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-258">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e6f75-258">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-260">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="e6f75-260">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="e6f75-261">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e6f75-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-262">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e6f75-262">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-263">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6f75-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-264">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-265">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="e6f75-265">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-266">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="e6f75-266">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e6f75-267">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e6f75-267">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-268">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e6f75-268">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-269">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e6f75-269">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-271">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="e6f75-271">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-272">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="e6f75-272">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-273">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e6f75-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-274">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-275">O número máximo de entidades diretamente endereçáveis que são suportadas por este controlador.</span><span class="sxs-lookup"><span data-stu-id="e6f75-275">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="e6f75-276">Um valor de 0 deve ser usado se o número for desconhecido ou ilimitado.</span><span class="sxs-lookup"><span data-stu-id="e6f75-276">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="e6f75-277">O protocolo usado pelo controlador para acessar dispositivos controlados.</span><span class="sxs-lookup"><span data-stu-id="e6f75-277">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="e6f75-278">Essa propriedade é herdada [**do \_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller)e é definida como 1.</span><span class="sxs-lookup"><span data-stu-id="e6f75-278">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-279">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="e6f75-279">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-280">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e6f75-280">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-281">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-282">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="e6f75-282">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-283">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e6f75-283">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-284">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6f75-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-285">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-286">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="e6f75-286">The label by which the object is known.</span></span> <span data-ttu-id="e6f75-287">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e6f75-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-288">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="e6f75-288">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-289">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6f75-289">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-290">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-291">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="e6f75-291">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="e6f75-292">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="e6f75-292">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e6f75-293">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e6f75-293">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e6f75-294"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e6f75-294"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-295"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="e6f75-295"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-296"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="e6f75-296"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-297"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="e6f75-297"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-298"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="e6f75-298"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-299"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="e6f75-299"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-300"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="e6f75-300"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-301"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="e6f75-301"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-302"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="e6f75-302"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-303"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="e6f75-303"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-304"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="e6f75-304"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-305"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="e6f75-305"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-306"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="e6f75-306"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-307"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="e6f75-307"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-308"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="e6f75-308"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-309"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="e6f75-309"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-310"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="e6f75-310"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-311"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="e6f75-311"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-312"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="e6f75-312"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e6f75-313">)</span><span class="sxs-lookup"><span data-stu-id="e6f75-313">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e6f75-314">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="e6f75-314">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-315">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6f75-315">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-317">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="e6f75-317">The current statuses of the object.</span></span> <span data-ttu-id="e6f75-318">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e6f75-318">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-319">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="e6f75-319">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-320">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6f75-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-322">O estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="e6f75-322">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="e6f75-323">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="e6f75-323">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="e6f75-324">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e6f75-324">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-325">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="e6f75-325">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-326">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6f75-326">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-328">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e6f75-328">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-329">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e6f75-329">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-330">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6f75-330">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-331">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-332">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="e6f75-332">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-333">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="e6f75-333">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-334">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e6f75-334">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-335">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-336">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="e6f75-336">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-337">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="e6f75-337">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-338">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e6f75-338">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-339">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-340">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="e6f75-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-341">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="e6f75-341">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-342">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6f75-342">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-344">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="e6f75-344">Provides high level status information.</span></span> <span data-ttu-id="e6f75-345">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="e6f75-345">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="e6f75-346">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="e6f75-346">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e6f75-347">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e6f75-347">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e6f75-348"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e6f75-348"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-349"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="e6f75-349"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-350"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="e6f75-350"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-351"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="e6f75-351"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-352"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="e6f75-352"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-353"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="e6f75-353"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e6f75-354">)</span><span class="sxs-lookup"><span data-stu-id="e6f75-354">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e6f75-355">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="e6f75-355">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-356">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6f75-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-357">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-358">Uma cadeia de caracteres que fornece mais informações relacionadas ao protocolo suportado pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="e6f75-358">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="e6f75-359">Essa propriedade é herdada [**do \_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller)e é definida como "protocolo de disquete".</span><span class="sxs-lookup"><span data-stu-id="e6f75-359">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is set to "Diskette Protocol".</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-360">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="e6f75-360">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-361">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6f75-361">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-362">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-363">O protocolo usado pelo controlador para acessar dispositivos controlados.</span><span class="sxs-lookup"><span data-stu-id="e6f75-363">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="e6f75-364">Essa propriedade é herdada [**do \_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller)e é definida como 7 (disquete flexível).</span><span class="sxs-lookup"><span data-stu-id="e6f75-364">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is set to 7 (Flexible Diskette).</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-365">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="e6f75-365">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-366">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6f75-366">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-367">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-368">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="e6f75-368">The last requested or desired state for the element.</span></span> <span data-ttu-id="e6f75-369">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="e6f75-369">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="e6f75-370">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="e6f75-370">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="e6f75-371">Uma instância específica de um elemento lógico habilitado pode não dar suporte a **RequestedStateChange**.</span><span class="sxs-lookup"><span data-stu-id="e6f75-371">A particular instance of an enabled logical element might not support **RequestedStateChange**.</span></span> <span data-ttu-id="e6f75-372">Se isso ocorrer, o valor 12 (não aplicável) será usado.</span><span class="sxs-lookup"><span data-stu-id="e6f75-372">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="e6f75-373">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e6f75-373">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-374">**Status**</span><span class="sxs-lookup"><span data-stu-id="e6f75-374">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-375">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6f75-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-376">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-377">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="e6f75-377">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-378">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e6f75-378">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-379">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6f75-379">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-380">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-381">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="e6f75-381">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="e6f75-382">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e6f75-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-383">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e6f75-383">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-384">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6f75-384">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-385">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-386">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="e6f75-386">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-387">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e6f75-387">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-388">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6f75-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-389">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-390">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="e6f75-390">The scoping system's creation class name.</span></span> <span data-ttu-id="e6f75-391">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e6f75-391">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-392">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e6f75-392">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-393">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6f75-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-394">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-395">O identificador exclusivo para a máquina virtual de escopo.</span><span class="sxs-lookup"><span data-stu-id="e6f75-395">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="e6f75-396">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e6f75-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-397">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="e6f75-397">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-398">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e6f75-398">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-399">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-400">A última vez em que a máquina virtual estava ligada.</span><span class="sxs-lookup"><span data-stu-id="e6f75-400">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="e6f75-401">Essa propriedade é herdada [**do \_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="e6f75-401">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-402">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="e6f75-402">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-403">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e6f75-403">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-404">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-405">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="e6f75-405">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="e6f75-406">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e6f75-406">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-407">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="e6f75-407">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-408">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e6f75-408">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-409">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-410">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="e6f75-410">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6f75-411">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="e6f75-411">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6f75-412">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6f75-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6f75-413">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6f75-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6f75-414">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="e6f75-414">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="e6f75-415">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e6f75-415">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6f75-416">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6f75-416">Remarks</span></span>

<span data-ttu-id="e6f75-417">O acesso à classe **Msvm \_ DisketteController** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="e6f75-417">Access to the **Msvm\_DisketteController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e6f75-418">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e6f75-418">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6f75-419">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6f75-419">Requirements</span></span>



| <span data-ttu-id="e6f75-420">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6f75-420">Requirement</span></span> | <span data-ttu-id="e6f75-421">Valor</span><span class="sxs-lookup"><span data-stu-id="e6f75-421">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6f75-422">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6f75-422">Minimum supported client</span></span><br/> | <span data-ttu-id="e6f75-423">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e6f75-423">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e6f75-424">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6f75-424">Minimum supported server</span></span><br/> | <span data-ttu-id="e6f75-425">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e6f75-425">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e6f75-426">Namespace</span><span class="sxs-lookup"><span data-stu-id="e6f75-426">Namespace</span></span><br/>                | <span data-ttu-id="e6f75-427">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e6f75-427">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e6f75-428">MOF</span><span class="sxs-lookup"><span data-stu-id="e6f75-428">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6f75-429"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6f75-429"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6f75-430">DLL</span><span class="sxs-lookup"><span data-stu-id="e6f75-430">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6f75-431"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e6f75-431"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e6f75-432">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6f75-432">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6f75-433">**\_Controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="e6f75-433">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> <dt>

[<span data-ttu-id="e6f75-434">**\_Controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="e6f75-434">**CIM\_Controller**</span></span>](/windows/desktop/CIMWin32Prov/cim-controller)
</dt> <dt>

[<span data-ttu-id="e6f75-435">Classes de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e6f75-435">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

