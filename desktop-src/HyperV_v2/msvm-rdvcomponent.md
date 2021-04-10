---
description: Representa o estado do componente RDV, que é responsável por fornecer um transporte para o pai para o convidado para fins de configuração.
ms.assetid: 240d2659-01ec-4300-a17e-0b1ec90483df
title: Classe Msvm_RdvComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponent
- Msvm_RdvComponent.RequestStateChange
- Msvm_RdvComponent.SetPowerState
- Msvm_RdvComponent.Reset
- Msvm_RdvComponent.EnableDevice
- Msvm_RdvComponent.OnlineDevice
- Msvm_RdvComponent.QuiesceDevice
- Msvm_RdvComponent.SaveProperties
- Msvm_RdvComponent.RestoreProperties
- Msvm_RdvComponent.InstanceID
- Msvm_RdvComponent.Caption
- Msvm_RdvComponent.Description
- Msvm_RdvComponent.ElementName
- Msvm_RdvComponent.InstallDate
- Msvm_RdvComponent.Name
- Msvm_RdvComponent.OperationalStatus
- Msvm_RdvComponent.StatusDescriptions
- Msvm_RdvComponent.Status
- Msvm_RdvComponent.HealthState
- Msvm_RdvComponent.CommunicationStatus
- Msvm_RdvComponent.DetailedStatus
- Msvm_RdvComponent.OperatingStatus
- Msvm_RdvComponent.PrimaryStatus
- Msvm_RdvComponent.EnabledState
- Msvm_RdvComponent.OtherEnabledState
- Msvm_RdvComponent.RequestedState
- Msvm_RdvComponent.EnabledDefault
- Msvm_RdvComponent.TimeOfLastStateChange
- Msvm_RdvComponent.AvailableRequestedStates
- Msvm_RdvComponent.TransitioningToState
- Msvm_RdvComponent.SystemCreationClassName
- Msvm_RdvComponent.SystemName
- Msvm_RdvComponent.CreationClassName
- Msvm_RdvComponent.DeviceID
- Msvm_RdvComponent.PowerManagementSupported
- Msvm_RdvComponent.PowerManagementCapabilities
- Msvm_RdvComponent.Availability
- Msvm_RdvComponent.StatusInfo
- Msvm_RdvComponent.LastErrorCode
- Msvm_RdvComponent.ErrorDescription
- Msvm_RdvComponent.ErrorCleared
- Msvm_RdvComponent.OtherIdentifyingInfo
- Msvm_RdvComponent.PowerOnHours
- Msvm_RdvComponent.TotalPowerOnHours
- Msvm_RdvComponent.IdentifyingDescriptions
- Msvm_RdvComponent.AdditionalAvailability
- Msvm_RdvComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e1dbffb7db18ef2441d4c8e06cff23af2648e5a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169733"
---
# <a name="msvm_rdvcomponent-class"></a><span data-ttu-id="4292b-103">\_Classe Msvm RdvComponent</span><span class="sxs-lookup"><span data-stu-id="4292b-103">Msvm\_RdvComponent class</span></span>

<span data-ttu-id="4292b-104">Representa o estado do componente RDV, que é responsável por fornecer um transporte para o pai para o convidado para fins de configuração.</span><span class="sxs-lookup"><span data-stu-id="4292b-104">Represents the state of the RDV component, which is responsible for providing a transport for the parent to the guest for configuration purposes.</span></span>

<span data-ttu-id="4292b-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="4292b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4292b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4292b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RdvComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "RDV";
  string   Description = "Remote Desktop Virtualization Service";
  string   ElementName = "RDV";
  datetime InstallDate;
  string   Name = "RDV";
  uint16   OperationalStatus[] = {2};
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
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_RdvComponent";
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
};
```

## <a name="members"></a><span data-ttu-id="4292b-107">Membros</span><span class="sxs-lookup"><span data-stu-id="4292b-107">Members</span></span>

<span data-ttu-id="4292b-108">A classe **Msvm \_ RdvComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4292b-108">The **Msvm\_RdvComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="4292b-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="4292b-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="4292b-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4292b-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4292b-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="4292b-111">Methods</span></span>

<span data-ttu-id="4292b-112">A classe **Msvm \_ RdvComponent** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="4292b-112">The **Msvm\_RdvComponent** class has these methods.</span></span>



| <span data-ttu-id="4292b-113">Método</span><span class="sxs-lookup"><span data-stu-id="4292b-113">Method</span></span>                                                       | <span data-ttu-id="4292b-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="4292b-114">Description</span></span>                                                                                                                                                                                                                         |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4292b-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="4292b-115">**EnableDevice**</span></span>                                             | <span data-ttu-id="4292b-116">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="4292b-116">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="4292b-117">**EnableEndPoints**</span><span class="sxs-lookup"><span data-stu-id="4292b-117">**EnableEndPoints**</span></span>](enableendpoints-msvm-rdvcomponent.md) | <span data-ttu-id="4292b-118">Solicita que o dispositivo virtual Serviços de Área de Trabalho Remota inicie uma conexão de pipe com a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4292b-118">Requests the Remote Desktop Services virtual device to start a pipe connection with the virtual machine.</span></span> <span data-ttu-id="4292b-119">Se zero (0) for retornado, a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4292b-119">If zero (0) is returned, then the operation was successful.</span></span> <span data-ttu-id="4292b-120">Qualquer outro código de retorno indica uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="4292b-120">Any other return code indicates an error condition.</span></span><br/> |
| <span data-ttu-id="4292b-121">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="4292b-121">**OnlineDevice**</span></span>                                             | <span data-ttu-id="4292b-122">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="4292b-122">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="4292b-123">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="4292b-123">**QuiesceDevice**</span></span>                                            | <span data-ttu-id="4292b-124">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="4292b-124">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="4292b-125">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="4292b-125">**RequestStateChange**</span></span>                                       | <span data-ttu-id="4292b-126">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="4292b-126">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="4292b-127">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="4292b-127">**Reset**</span></span>                                                    | <span data-ttu-id="4292b-128">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="4292b-128">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="4292b-129">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="4292b-129">**RestoreProperties**</span></span>                                        | <span data-ttu-id="4292b-130">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="4292b-130">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="4292b-131">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="4292b-131">**SaveProperties**</span></span>                                           | <span data-ttu-id="4292b-132">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="4292b-132">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="4292b-133">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="4292b-133">**SetPowerState**</span></span>                                            | <span data-ttu-id="4292b-134">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="4292b-134">This method is not supported.</span></span><br/>                                                                                                                                                                                            |



 

### <a name="properties"></a><span data-ttu-id="4292b-135">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4292b-135">Properties</span></span>

<span data-ttu-id="4292b-136">A classe **Msvm \_ RdvComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4292b-136">The **Msvm\_RdvComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4292b-137">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="4292b-137">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-138">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4292b-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4292b-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-140">Qualquer disponibilidade e status adicionais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4292b-140">Any additional availability and status of the device.</span></span> <span data-ttu-id="4292b-141">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="4292b-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4292b-142">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="4292b-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-143">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4292b-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-145">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4292b-145">The primary availability and status of the device.</span></span> <span data-ttu-id="4292b-146">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="4292b-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4292b-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="4292b-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-148">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4292b-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4292b-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-150">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="4292b-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="4292b-151">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4292b-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4292b-152">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="4292b-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4292b-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-155">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="4292b-155">A short description of the object.</span></span> <span data-ttu-id="4292b-156">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4292b-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4292b-157">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="4292b-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-158">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4292b-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-160">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="4292b-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="4292b-161">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="4292b-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4292b-162">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4292b-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4292b-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="4292b-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="4292b-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="4292b-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="4292b-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="4292b-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="4292b-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="4292b-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4292b-170">)</span><span class="sxs-lookup"><span data-stu-id="4292b-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4292b-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4292b-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-172">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4292b-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-174">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="4292b-174">The scoping system's creation class name.</span></span> <span data-ttu-id="4292b-175">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="4292b-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4292b-176">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4292b-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4292b-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-179">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="4292b-179">A description of the object.</span></span> <span data-ttu-id="4292b-180">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4292b-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4292b-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="4292b-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-182">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4292b-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-184">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="4292b-184">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="4292b-185">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="4292b-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4292b-186">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4292b-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4292b-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="4292b-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="4292b-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="4292b-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="4292b-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="4292b-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="4292b-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="4292b-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="4292b-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4292b-195">)</span><span class="sxs-lookup"><span data-stu-id="4292b-195">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4292b-196">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="4292b-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-197">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4292b-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-199">Um endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4292b-199">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="4292b-200">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="4292b-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4292b-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4292b-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-202">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4292b-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-204">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="4292b-204">A display name for the object.</span></span> <span data-ttu-id="4292b-205">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4292b-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4292b-206">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="4292b-206">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-207">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4292b-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-209">A configuração de inicialização ou padrão de um administrador para a propriedade **enabledstate** de um elemento.</span><span class="sxs-lookup"><span data-stu-id="4292b-209">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="4292b-210">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4292b-210">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4292b-211">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="4292b-211">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-212">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4292b-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-214">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="4292b-214">The enabled and disabled states of an element.</span></span> <span data-ttu-id="4292b-215">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="4292b-215">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="4292b-216">Valor</span><span class="sxs-lookup"><span data-stu-id="4292b-216">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="4292b-217">Significado</span><span class="sxs-lookup"><span data-stu-id="4292b-217">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="4292b-218"><dt></dt> <dt>0</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="4292b-218"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="4292b-219">Não foi possível determinar o estado do elemento.</span><span class="sxs-lookup"><span data-stu-id="4292b-219">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="4292b-220"><dt>**Outros**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4292b-220"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="4292b-221"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4292b-221"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="4292b-222">O elemento está em execução.</span><span class="sxs-lookup"><span data-stu-id="4292b-222">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="4292b-223"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4292b-223"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="4292b-224">O elemento está desativado.</span><span class="sxs-lookup"><span data-stu-id="4292b-224">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="4292b-225"><dt>**Desligando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="4292b-225"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="4292b-226">O elemento está no processo de ir para um estado desabilitado.</span><span class="sxs-lookup"><span data-stu-id="4292b-226">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="4292b-227"><dt>**Não aplicável**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="4292b-227"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="4292b-228">O elemento não dá suporte a ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="4292b-228">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="4292b-229"><dt>**Habilitado, mas offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="4292b-229"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="4292b-230">O elemento pode estar concluindo comandos e removerá todas as novas solicitações.</span><span class="sxs-lookup"><span data-stu-id="4292b-230">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="4292b-231"><dt>**No teste**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="4292b-231"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="4292b-232">O elemento está em um estado de teste.</span><span class="sxs-lookup"><span data-stu-id="4292b-232">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="4292b-233"><dt>**Adiado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="4292b-233"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="4292b-234">O elemento pode estar concluindo comandos, mas colocará todas as novas solicitações na fila.</span><span class="sxs-lookup"><span data-stu-id="4292b-234">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="4292b-235"><dt>**Desativar**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="4292b-235"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="4292b-236">O elemento está habilitado, mas em um modo restrito.</span><span class="sxs-lookup"><span data-stu-id="4292b-236">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="4292b-237">O comportamento do elemento é semelhante ao estado habilitado (2), mas processa apenas um conjunto restrito de comandos.</span><span class="sxs-lookup"><span data-stu-id="4292b-237">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="4292b-238">Todas as outras solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="4292b-238">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="4292b-239"><dt>**Iniciando**</dt> em <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="4292b-239"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="4292b-240">O elemento está no processo de ir para um estado habilitado (2).</span><span class="sxs-lookup"><span data-stu-id="4292b-240">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="4292b-241">Novas solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="4292b-241">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="4292b-242">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="4292b-242">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-243">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="4292b-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-245">Indica se o erro relatado em **LastErrorCode** agora está limpo.</span><span class="sxs-lookup"><span data-stu-id="4292b-245">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="4292b-246">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="4292b-246">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4292b-247">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="4292b-247">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-248">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4292b-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-249">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-250">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="4292b-250">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="4292b-251">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="4292b-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4292b-252">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="4292b-252">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-253">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4292b-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-254">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-255">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="4292b-255">The current health of the element.</span></span> <span data-ttu-id="4292b-256">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4292b-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4292b-257">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4292b-257">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-258">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4292b-258">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4292b-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-260">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz de propriedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="4292b-260">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="4292b-261">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="4292b-261">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4292b-262">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4292b-262">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-263">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4292b-263">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-264">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-265">A data e a hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="4292b-265">The date and time when the object was installed.</span></span> <span data-ttu-id="4292b-266">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="4292b-266">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="4292b-267">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4292b-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4292b-268">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4292b-268">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-269">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4292b-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4292b-271">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="4292b-271">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4292b-272">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="4292b-272">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4292b-273">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4292b-273">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4292b-274">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="4292b-274">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-275">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4292b-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-276">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-277">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4292b-277">The last error code reported by the logical device.</span></span> <span data-ttu-id="4292b-278">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="4292b-278">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4292b-279">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="4292b-279">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-280">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4292b-280">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-281">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-282">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="4292b-282">This property has been deprecated.</span></span> <span data-ttu-id="4292b-283">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="4292b-283">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4292b-284">**Nome**</span><span class="sxs-lookup"><span data-stu-id="4292b-284">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-285">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4292b-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-287">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="4292b-287">The label by which the object is known.</span></span> <span data-ttu-id="4292b-288">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4292b-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4292b-289">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="4292b-289">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-290">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4292b-290">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-292">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="4292b-292">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="4292b-293">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="4292b-293">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4292b-294">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4292b-294">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4292b-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="4292b-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-296"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="4292b-296"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-297"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="4292b-297"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-298"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="4292b-298"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-299"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="4292b-299"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-300"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="4292b-300"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-301"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="4292b-301"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-302"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="4292b-302"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-303"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="4292b-303"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-304"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="4292b-304"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-305"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="4292b-305"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-306"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="4292b-306"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-307"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="4292b-307"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-308"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="4292b-308"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-309"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="4292b-309"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-310"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="4292b-310"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-311"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="4292b-311"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-312"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="4292b-312"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-313"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="4292b-313"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4292b-314">)</span><span class="sxs-lookup"><span data-stu-id="4292b-314">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4292b-315">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="4292b-315">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-316">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4292b-316">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4292b-317">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-318">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="4292b-318">The current statuses of the object.</span></span> <span data-ttu-id="4292b-319">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4292b-319">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4292b-320">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="4292b-320">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-321">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4292b-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-323">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="4292b-323">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="4292b-324">Essa propriedade deve ser definida como **NULL** quando a propriedade **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="4292b-324">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="4292b-325">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4292b-325">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4292b-326">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="4292b-326">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-327">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4292b-327">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4292b-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-329">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4292b-329">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="4292b-330">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="4292b-330">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4292b-331">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4292b-331">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-332">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4292b-332">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4292b-333">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-334">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4292b-334">The power management capabilities of the device.</span></span> <span data-ttu-id="4292b-335">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="4292b-335">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4292b-336">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="4292b-336">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-337">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="4292b-337">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-338">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-339">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="4292b-339">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="4292b-340">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="4292b-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4292b-341">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="4292b-341">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-342">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4292b-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-344">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="4292b-344">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="4292b-345">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="4292b-345">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4292b-346">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="4292b-346">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-347">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4292b-347">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-348">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-349">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="4292b-349">Provides high level status information.</span></span> <span data-ttu-id="4292b-350">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="4292b-350">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="4292b-351">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="4292b-351">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4292b-352">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4292b-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4292b-353"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="4292b-353"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-354"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="4292b-354"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-355"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="4292b-355"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-356"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="4292b-356"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="4292b-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4292b-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="4292b-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4292b-359">)</span><span class="sxs-lookup"><span data-stu-id="4292b-359">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4292b-360">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="4292b-360">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-361">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4292b-361">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-362">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-363">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="4292b-363">The last requested or desired state for the element.</span></span> <span data-ttu-id="4292b-364">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 12 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="4292b-364">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="4292b-365">**Status**</span><span class="sxs-lookup"><span data-stu-id="4292b-365">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-366">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4292b-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-367">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-368">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="4292b-368">The current status of the object.</span></span> <span data-ttu-id="4292b-369">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="4292b-369">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4292b-370">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4292b-370">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-371">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4292b-371">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4292b-372">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-373">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="4292b-373">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="4292b-374">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4292b-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4292b-375">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="4292b-375">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-376">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4292b-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-377">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-378">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4292b-378">The current state of the logical device.</span></span> <span data-ttu-id="4292b-379">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="4292b-379">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4292b-380">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4292b-380">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-381">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4292b-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-382">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-383">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="4292b-383">The scoping system's creation class name.</span></span> <span data-ttu-id="4292b-384">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="4292b-384">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4292b-385">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="4292b-385">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-386">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4292b-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-387">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-388">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="4292b-388">The scoping system's name.</span></span> <span data-ttu-id="4292b-389">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="4292b-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4292b-390">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="4292b-390">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-391">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4292b-391">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-392">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-393">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="4292b-393">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="4292b-394">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4292b-394">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4292b-395">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="4292b-395">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-396">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4292b-396">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-397">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-398">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="4292b-398">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="4292b-399">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="4292b-399">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4292b-400">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="4292b-400">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4292b-401">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4292b-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4292b-402">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4292b-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4292b-403">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="4292b-403">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="4292b-404">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4292b-404">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4292b-405">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4292b-405">Requirements</span></span>



| <span data-ttu-id="4292b-406">Requisito</span><span class="sxs-lookup"><span data-stu-id="4292b-406">Requirement</span></span> | <span data-ttu-id="4292b-407">Valor</span><span class="sxs-lookup"><span data-stu-id="4292b-407">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4292b-408">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4292b-408">Minimum supported client</span></span><br/> | <span data-ttu-id="4292b-409">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4292b-409">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4292b-410">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4292b-410">Minimum supported server</span></span><br/> | <span data-ttu-id="4292b-411">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4292b-411">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4292b-412">Namespace</span><span class="sxs-lookup"><span data-stu-id="4292b-412">Namespace</span></span><br/>                | <span data-ttu-id="4292b-413">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="4292b-413">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4292b-414">MOF</span><span class="sxs-lookup"><span data-stu-id="4292b-414">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4292b-415"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4292b-415"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4292b-416">DLL</span><span class="sxs-lookup"><span data-stu-id="4292b-416">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4292b-417"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4292b-417"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

