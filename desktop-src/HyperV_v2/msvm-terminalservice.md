---
description: Gerencia todas as conexões de terminal remotas para um host específico.
ms.assetid: 7eacb8a6-cb8d-4a2a-951e-f5286cf484e7
title: Classe Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService
- Msvm_TerminalService.InstanceID
- Msvm_TerminalService.Caption
- Msvm_TerminalService.Description
- Msvm_TerminalService.ElementName
- Msvm_TerminalService.InstallDate
- Msvm_TerminalService.OperationalStatus
- Msvm_TerminalService.StatusDescriptions
- Msvm_TerminalService.Status
- Msvm_TerminalService.HealthState
- Msvm_TerminalService.CommunicationStatus
- Msvm_TerminalService.DetailedStatus
- Msvm_TerminalService.OperatingStatus
- Msvm_TerminalService.PrimaryStatus
- Msvm_TerminalService.EnabledState
- Msvm_TerminalService.OtherEnabledState
- Msvm_TerminalService.RequestedState
- Msvm_TerminalService.EnabledDefault
- Msvm_TerminalService.TimeOfLastStateChange
- Msvm_TerminalService.AvailableRequestedStates
- Msvm_TerminalService.TransitioningToState
- Msvm_TerminalService.SystemCreationClassName
- Msvm_TerminalService.SystemName
- Msvm_TerminalService.Name
- Msvm_TerminalService.CreationClassName
- Msvm_TerminalService.PrimaryOwnerName
- Msvm_TerminalService.PrimaryOwnerContact
- Msvm_TerminalService.StartMode
- Msvm_TerminalService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 76b12bb49391909638d20df817a3693938c3222c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757406"
---
# <a name="msvm_terminalservice-class"></a><span data-ttu-id="e2ae0-103">\_Classe Msvm TerminalService</span><span class="sxs-lookup"><span data-stu-id="e2ae0-103">Msvm\_TerminalService class</span></span>

<span data-ttu-id="e2ae0-104">Gerencia todas as conexões de terminal remotas para um host específico.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-104">Manages all remote terminal connections to a particular host.</span></span> <span data-ttu-id="e2ae0-105">O serviço usa uma porta configurável para iniciar todas as conexões de terminal.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-105">The service uses a configurable port to initiate all terminal connections.</span></span>

<span data-ttu-id="e2ae0-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2ae0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2ae0-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TerminalService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Hyper-V Terminal Service";
  string   Description = "Microsoft Virtual Terminal Service";
  string   ElementName = "Hyper-V Terminal Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The virtual terminal connection management service is fully operational" };
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   Name = "termsvc";
  string   CreationClassName = "Msvm_TerminalService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="e2ae0-108">Membros</span><span class="sxs-lookup"><span data-stu-id="e2ae0-108">Members</span></span>

<span data-ttu-id="e2ae0-109">A classe **Msvm \_ TerminalService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e2ae0-109">The **Msvm\_TerminalService** class has these types of members:</span></span>

-   [<span data-ttu-id="e2ae0-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="e2ae0-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="e2ae0-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e2ae0-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e2ae0-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="e2ae0-112">Methods</span></span>

<span data-ttu-id="e2ae0-113">A classe **Msvm \_ TerminalService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-113">The **Msvm\_TerminalService** class has these methods.</span></span>



| <span data-ttu-id="e2ae0-114">Método</span><span class="sxs-lookup"><span data-stu-id="e2ae0-114">Method</span></span>                                                                                        | <span data-ttu-id="e2ae0-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="e2ae0-115">Description</span></span>                                                                                                      |
|:----------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2ae0-116">**GetInteractiveSessionACL**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-116">**GetInteractiveSessionACL**</span></span>](getinteractivesessionacl-msvm-terminalservice.md)             | <span data-ttu-id="e2ae0-117">Recupera a DACL atual que controla o acesso à sessão interativa de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-117">Retrieves the current DACL that controls access to the interactive session of a virtual machine.</span></span><br/>      |
| [<span data-ttu-id="e2ae0-118">**GrantInteractiveSessionAccess**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-118">**GrantInteractiveSessionAccess**</span></span>](grantinteractivesessionaccess-msvm-terminalservice.md)   | <span data-ttu-id="e2ae0-119">Concede acesso à sessão interativa da máquina virtual à lista especificada de relações de confiança.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-119">Grants access to the interactive session of the virtual machine to the specified list of trustees.</span></span><br/>    |
| [<span data-ttu-id="e2ae0-120">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-120">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-terminalservice.md)                   | <span data-ttu-id="e2ae0-121">Modifica os dados de configuração para o serviço.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-121">Modifies the setting data for the service.</span></span><br/>                                                            |
| [<span data-ttu-id="e2ae0-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-122">**RequestStateChange**</span></span>](msvm-terminalservice-requeststatechange.md)                         | <span data-ttu-id="e2ae0-123">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-123">Requests a state change.</span></span><br/>                                                                              |
| [<span data-ttu-id="e2ae0-124">**RevokeInteractiveSessionAccess**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-124">**RevokeInteractiveSessionAccess**</span></span>](revokeinteractivesessionaccess-msvm-terminalservice.md) | <span data-ttu-id="e2ae0-125">Revoga o acesso à sessão interativa da máquina virtual da lista especificada de relações de confiança.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-125">Revokes access to the interactive session of the virtual machine from the specified list of trustees.</span></span><br/> |
| [<span data-ttu-id="e2ae0-126">**StartService**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-126">**StartService**</span></span>](msvm-terminalservice-startservice.md)                                     | <span data-ttu-id="e2ae0-127">Inicia o serviço.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-127">Starts the service.</span></span><br/>                                                                                   |
| [<span data-ttu-id="e2ae0-128">**StopService**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-128">**StopService**</span></span>](msvm-terminalservice-stopservice.md)                                       | <span data-ttu-id="e2ae0-129">Interrompe o serviço.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-129">Stops the service.</span></span><br/>                                                                                    |



 

### <a name="properties"></a><span data-ttu-id="e2ae0-130">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e2ae0-130">Properties</span></span>

<span data-ttu-id="e2ae0-131">A classe **Msvm \_ TerminalService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-131">The **Msvm\_TerminalService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2ae0-132">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-132">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-133">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-133">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-135">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="e2ae0-135">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="e2ae0-136">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-136">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e2ae0-137">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-137">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-140">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-140">A short description of the object.</span></span> <span data-ttu-id="e2ae0-141">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2ae0-142">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-142">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-143">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-145">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-145">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="e2ae0-146">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-146">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e2ae0-147">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-147">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e2ae0-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-149"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-149"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-150"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-150"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-151"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-151"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-152"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-152"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="e2ae0-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e2ae0-155">)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-155">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e2ae0-156">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-159">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-159">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e2ae0-160">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-160">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="e2ae0-161">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-164">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="e2ae0-164">A description of the object.</span></span> <span data-ttu-id="e2ae0-165">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2ae0-166">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-166">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-167">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-169">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-169">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="e2ae0-170">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e2ae0-171">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e2ae0-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="e2ae0-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e2ae0-180">)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e2ae0-181">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-181">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-184">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-184">A display name for the object.</span></span> <span data-ttu-id="e2ae0-185">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2ae0-186">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-186">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-187">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-189">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-189">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="e2ae0-190">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-190">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e2ae0-191">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-191">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-194">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-194">The enabled and disabled states of an element.</span></span> <span data-ttu-id="e2ae0-195">Ele também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-195">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="e2ae0-196">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-196">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e2ae0-197">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-197">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-198">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-200">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-200">The current health of the element.</span></span> <span data-ttu-id="e2ae0-201">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-201">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="e2ae0-202">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-202">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="e2ae0-203">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2ae0-204">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-204">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-205">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-205">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-207">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-207">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="e2ae0-208">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2ae0-209">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-209">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-212">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-212">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-213">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-213">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e2ae0-214">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-214">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e2ae0-215">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-215">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-216">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-218">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-218">The label by which the object is known.</span></span> <span data-ttu-id="e2ae0-219">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-219">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="e2ae0-220">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-220">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-221">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-223">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="e2ae0-223">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="e2ae0-224">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-224">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e2ae0-225">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-225">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e2ae0-226"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-226"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-227"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-227"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-228"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-228"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-229"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-229"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-230"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-230"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-231"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-231"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-232"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-232"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-233"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-233"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-234"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-234"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-235"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-235"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-236"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-236"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-237"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-237"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-238"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-238"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-239"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-239"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-240"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-240"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-241"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-241"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-242"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-242"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-243"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-243"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-244"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="e2ae0-244"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e2ae0-245">)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-245">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e2ae0-246">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-246">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-247">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-247">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-249">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-249">The current statuses of the object.</span></span> <span data-ttu-id="e2ae0-250">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-250">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2ae0-251">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-251">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-252">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-253">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-254">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-254">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="e2ae0-255">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-255">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="e2ae0-256">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-256">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e2ae0-257">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-257">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-258">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-260">Um valor que fornece informações sobre como o proprietário principal do serviço pode ser alcançado (por exemplo, número de telefone, endereço de email e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-260">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="e2ae0-261">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-261">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="e2ae0-262">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-262">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-263">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-264">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-265">O nome do proprietário principal do serviço, se um estiver definido.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-265">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="e2ae0-266">O proprietário principal é o contato de suporte inicial para o serviço.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-266">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="e2ae0-267">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-267">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="e2ae0-268">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-268">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-269">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-271">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-271">Provides high level status information.</span></span> <span data-ttu-id="e2ae0-272">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-272">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="e2ae0-273">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-273">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e2ae0-274">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-274">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e2ae0-275"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-275"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-276"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-276"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-277"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-277"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-278"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-278"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="e2ae0-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e2ae0-281">)</span><span class="sxs-lookup"><span data-stu-id="e2ae0-281">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e2ae0-282">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-282">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-283">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-284">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-285">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-285">The last requested or desired state for the element.</span></span> <span data-ttu-id="e2ae0-286">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-286">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="e2ae0-287">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-287">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="e2ae0-288">Uma determinada instância do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) pode não dar suporte ao método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="e2ae0-288">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="e2ae0-289">Se isso ocorrer, o valor 12 (não aplicável) será usado.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-289">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="e2ae0-290">Essa propriedade é herdada do **CIM \_ EnabledLogicalElement**.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-290">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="e2ae0-291">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-291">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-292">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-293">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-294">Indica se o serviço está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-294">Indicates whether the service is currently running.</span></span> <span data-ttu-id="e2ae0-295">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-295">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="e2ae0-296">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-296">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-297">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-299">Um valor de cadeia de caracteres que indica se o serviço é iniciado automaticamente por um sistema, um sistema operacional ou é iniciado somente mediante solicitação.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-299">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="e2ae0-300">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-300">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="e2ae0-301">**Status**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-301">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-302">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-303">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-304">O status do elemento.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-304">The status of the element.</span></span> <span data-ttu-id="e2ae0-305">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2ae0-306">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-306">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-307">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-307">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-308">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-309">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="e2ae0-309">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="e2ae0-310">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2ae0-311">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-311">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-312">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-313">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-314">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-314">The scoping system's creation class name.</span></span> <span data-ttu-id="e2ae0-315">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-315">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="e2ae0-316">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-316">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-317">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-319">O nome do sistema de computador de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-319">The name of the hosting computer system.</span></span> <span data-ttu-id="e2ae0-320">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-320">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="e2ae0-321">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-321">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-322">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-323">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-324">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-324">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="e2ae0-325">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-325">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e2ae0-326">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-326">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2ae0-327">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2ae0-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ae0-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2ae0-329">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-329">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="e2ae0-330">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-330">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2ae0-331">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2ae0-331">Remarks</span></span>

<span data-ttu-id="e2ae0-332">O acesso à classe **Msvm \_ TerminalService** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-332">Access to the **Msvm\_TerminalService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e2ae0-333">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e2ae0-333">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2ae0-334">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2ae0-334">Requirements</span></span>



| <span data-ttu-id="e2ae0-335">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2ae0-335">Requirement</span></span> | <span data-ttu-id="e2ae0-336">Valor</span><span class="sxs-lookup"><span data-stu-id="e2ae0-336">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2ae0-337">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2ae0-337">Minimum supported client</span></span><br/> | <span data-ttu-id="e2ae0-338">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e2ae0-338">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e2ae0-339">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2ae0-339">Minimum supported server</span></span><br/> | <span data-ttu-id="e2ae0-340">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e2ae0-340">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e2ae0-341">Namespace</span><span class="sxs-lookup"><span data-stu-id="e2ae0-341">Namespace</span></span><br/>                | <span data-ttu-id="e2ae0-342">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e2ae0-342">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e2ae0-343">MOF</span><span class="sxs-lookup"><span data-stu-id="e2ae0-343">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2ae0-344"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2ae0-344"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2ae0-345">DLL</span><span class="sxs-lookup"><span data-stu-id="e2ae0-345">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2ae0-346"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e2ae0-346"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e2ae0-347">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2ae0-347">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2ae0-348">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="e2ae0-348">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

