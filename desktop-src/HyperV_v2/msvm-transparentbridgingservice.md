---
description: Serve como um espaço reservado para o serviço dentro do comutador que aprende os endereços MAC e serve como uma ponte entre as \_ classes Msvm VirtualEthernetSwitch e Msvm \_ DynamicForwardingEntry.
ms.assetid: E617DBC3-F5DD-4875-B3CC-E120A2218EBE
title: Classe Msvm_TransparentBridgingService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TransparentBridgingService
- Msvm_TransparentBridgingService.InstanceID
- Msvm_TransparentBridgingService.Caption
- Msvm_TransparentBridgingService.Description
- Msvm_TransparentBridgingService.ElementName
- Msvm_TransparentBridgingService.InstallDate
- Msvm_TransparentBridgingService.OperationalStatus
- Msvm_TransparentBridgingService.StatusDescriptions
- Msvm_TransparentBridgingService.Status
- Msvm_TransparentBridgingService.HealthState
- Msvm_TransparentBridgingService.CommunicationStatus
- Msvm_TransparentBridgingService.DetailedStatus
- Msvm_TransparentBridgingService.OperatingStatus
- Msvm_TransparentBridgingService.PrimaryStatus
- Msvm_TransparentBridgingService.EnabledState
- Msvm_TransparentBridgingService.OtherEnabledState
- Msvm_TransparentBridgingService.RequestedState
- Msvm_TransparentBridgingService.EnabledDefault
- Msvm_TransparentBridgingService.TimeOfLastStateChange
- Msvm_TransparentBridgingService.AvailableRequestedStates
- Msvm_TransparentBridgingService.TransitioningToState
- Msvm_TransparentBridgingService.SystemCreationClassName
- Msvm_TransparentBridgingService.SystemName
- Msvm_TransparentBridgingService.CreationClassName
- Msvm_TransparentBridgingService.Name
- Msvm_TransparentBridgingService.PrimaryOwnerName
- Msvm_TransparentBridgingService.PrimaryOwnerContact
- Msvm_TransparentBridgingService.StartMode
- Msvm_TransparentBridgingService.Started
- Msvm_TransparentBridgingService.Keywords
- Msvm_TransparentBridgingService.ServiceURL
- Msvm_TransparentBridgingService.StartupConditions
- Msvm_TransparentBridgingService.StartupParameters
- Msvm_TransparentBridgingService.ProtocolType
- Msvm_TransparentBridgingService.OtherProtocolType
- Msvm_TransparentBridgingService.AgingTime
- Msvm_TransparentBridgingService.FID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f5daacf42bc221fa98f56d0c5b84140e3784c2ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921166"
---
# <a name="msvm_transparentbridgingservice-class"></a><span data-ttu-id="1b6a9-103">\_Classe Msvm TransparentBridgingService</span><span class="sxs-lookup"><span data-stu-id="1b6a9-103">Msvm\_TransparentBridgingService class</span></span>

<span data-ttu-id="1b6a9-104">Serve como um espaço reservado para o serviço dentro do comutador que aprende os endereços MAC e serve como uma ponte entre as classes [**Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) e [**Msvm \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) .</span><span class="sxs-lookup"><span data-stu-id="1b6a9-104">Serves as a placeholder for the service inside the switch that learns MAC addresses and serves as a bridge between the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) and [**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) classes.</span></span>

<span data-ttu-id="1b6a9-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b6a9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1b6a9-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TransparentBridgingService : CIM_TransparentBridgingService
{
  string   InstanceID;
  string   Caption = "Virtual Switch Transparent Bridging Service";
  string   Description = "Microsoft Virtual Switch Transparent Bridging Service";
  string   ElementName;
  datetime InstallDate;
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
  string   CreationClassName = "Msvm_TransparentBridgingService";
  string   Name;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode = "Automatic";
  boolean  Started = True;
  string   Keywords[];
  string   ServiceURL;
  string   StartupConditions[];
  string   StartupParameters[];
  uint16   ProtocolType = 15;
  string   OtherProtocolType;
  uint32   AgingTime = 300;
  uint32   FID = 0;
};
```

## <a name="members"></a><span data-ttu-id="1b6a9-107">Membros</span><span class="sxs-lookup"><span data-stu-id="1b6a9-107">Members</span></span>

<span data-ttu-id="1b6a9-108">A classe **Msvm \_ TransparentBridgingService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1b6a9-108">The **Msvm\_TransparentBridgingService** class has these types of members:</span></span>

-   [<span data-ttu-id="1b6a9-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="1b6a9-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="1b6a9-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1b6a9-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1b6a9-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="1b6a9-111">Methods</span></span>

<span data-ttu-id="1b6a9-112">A classe **Msvm \_ TransparentBridgingService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-112">The **Msvm\_TransparentBridgingService** class has these methods.</span></span>



| <span data-ttu-id="1b6a9-113">Método</span><span class="sxs-lookup"><span data-stu-id="1b6a9-113">Method</span></span>                                                                           | <span data-ttu-id="1b6a9-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="1b6a9-114">Description</span></span>                         |
|:---------------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="1b6a9-115">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-115">**RequestStateChange**</span></span>](msvm-transparentbridgingservice-requeststatechange.md) | <span data-ttu-id="1b6a9-116">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-116">Requests a state change.</span></span><br/> |
| [<span data-ttu-id="1b6a9-117">**StartService**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-117">**StartService**</span></span>](msvm-transparentbridgingservice-startservice.md)             | <span data-ttu-id="1b6a9-118">Inicia o serviço.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-118">Starts the service.</span></span><br/>      |
| [<span data-ttu-id="1b6a9-119">**StopService**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-119">**StopService**</span></span>](msvm-transparentbridgingservice-stopservice.md)               | <span data-ttu-id="1b6a9-120">Interrompe o serviço.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-120">Stops the service.</span></span><br/>       |



 

### <a name="properties"></a><span data-ttu-id="1b6a9-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1b6a9-121">Properties</span></span>

<span data-ttu-id="1b6a9-122">A classe **Msvm \_ TransparentBridgingService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-122">The **Msvm\_TransparentBridgingService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1b6a9-123">**Envelhecimento**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-123">**AgingTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-126">O período de tempo limite, em segundos, para expiração de endereços MAC aprendidos dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-126">The time-out period, in seconds, for aging out dynamically learned MAC addresses.</span></span> <span data-ttu-id="1b6a9-127">Essa propriedade é herdada do [**CIM \_ TransparentBridgingService**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-127">This property is inherited from [**CIM\_TransparentBridgingService**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-128">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-128">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-129">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-131">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="1b6a9-131">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="1b6a9-132">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-132">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-133">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-136">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-136">A short description of the object.</span></span> <span data-ttu-id="1b6a9-137">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre "serviço de ponte transparente do comutador virtual".</span><span class="sxs-lookup"><span data-stu-id="1b6a9-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always "Virtual Switch Transparent Bridging Service".</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-138">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-138">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-139">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-141">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-141">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="1b6a9-142">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-142">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1b6a9-143">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-143">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1b6a9-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-145"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-145"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-146"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-146"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-147"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-147"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-148"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-148"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-150"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="1b6a9-150"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1b6a9-151">)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-151">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1b6a9-152">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-152">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-155">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-155">A short description of the object.</span></span> <span data-ttu-id="1b6a9-156">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-156">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-157">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-160">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="1b6a9-160">A description of the object.</span></span> <span data-ttu-id="1b6a9-161">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "serviço de ponte transparente do comutador virtual da Microsoft".</span><span class="sxs-lookup"><span data-stu-id="1b6a9-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Virtual Switch Transparent Bridging Service".</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-162">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-162">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-163">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-165">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-165">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="1b6a9-166">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1b6a9-167">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1b6a9-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-169"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-169"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-170"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-170"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-171"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-171"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-172"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-172"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-173"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-173"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="1b6a9-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1b6a9-176">)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-176">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1b6a9-177">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-177">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-180">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-180">A display name for the object.</span></span> <span data-ttu-id="1b6a9-181">Essa propriedade permite que cada instância defina um nome de exibição além de suas propriedades de chave, dados de identidade e informações de descrição.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-181">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="1b6a9-182">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-182">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-183">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-183">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-184">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-186">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-186">An administrator's default or startup configuration for the Enabled State of an element.</span></span> <span data-ttu-id="1b6a9-187">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-187">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-188">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-188">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-189">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-191">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-191">The enabled and disabled states of an element.</span></span> <span data-ttu-id="1b6a9-192">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-192">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-193">**FID**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-193">**FID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-194">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-196">O identificador de banco de dados de filtragem usado por comutadores que dão suporte à VLAN e que têm mais de um banco de dados de filtragem.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-196">The filtering database identifier used by switches that support VLAN and that have more than one filtering database.</span></span> <span data-ttu-id="1b6a9-197">Essa propriedade é herdada do [**CIM \_ TransparentBridgingService**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-197">This property is inherited from [**CIM\_TransparentBridgingService**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-198">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-198">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-199">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-201">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-201">The current health of the element.</span></span> <span data-ttu-id="1b6a9-202">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-202">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="1b6a9-203">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-204">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-204">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-205">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-205">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-207">Especifica a hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-207">Specifies the time when the object was installed.</span></span> <span data-ttu-id="1b6a9-208">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-208">Lack of a value does not indicate that the object is not installed.</span></span> <span data-ttu-id="1b6a9-209">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e não é usada.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-209">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-210">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-210">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-211">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-213">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-213">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-214">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-214">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1b6a9-215">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-215">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-216">**Palavras-chave**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-216">**Keywords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-217">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-217">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-219">Não use.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-219">Do not use.</span></span> <span data-ttu-id="1b6a9-220">Uma matriz de forma livre de cadeias de caracteres que fornece palavras descritivas e frases que podem ser usadas em consultas.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-220">A free-form array of strings that provide descriptive words and phrases that can be used in queries.</span></span> <span data-ttu-id="1b6a9-221">Esta propriedade não está implementada porque não está padronizada.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-221">This property is not implemented because it is not standardized.</span></span> <span data-ttu-id="1b6a9-222">Se essa propriedade fosse um constructo de consulta necessário, ela seria necessária mais alta na hierarquia de herança.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-222">If this property were a necessary query construct, then it would be required higher in the inheritance hierarchy.</span></span> <span data-ttu-id="1b6a9-223">Essa propriedade é herdada do [**CIM \_ NetworkService**](/previous-versions//cc136875(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-223">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-224">**Nome**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-224">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-225">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-227">Um nome que identifica exclusivamente o serviço e fornece uma indicação da funcionalidade que é gerenciada.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-227">A name that uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="1b6a9-228">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-228">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-229">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-229">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-230">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-232">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="1b6a9-232">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="1b6a9-233">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-233">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1b6a9-234">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-234">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1b6a9-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="1b6a9-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1b6a9-254">)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-254">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1b6a9-255">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-255">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-256">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-256">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-257">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-258">O status atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-258">The current status of the element.</span></span> <span data-ttu-id="1b6a9-259">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-260">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-260">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-261">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-262">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-263">O estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-263">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="1b6a9-264">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e não é usada.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-264">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-265">**OtherProtocolType**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-265">**OtherProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-266">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-266">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-267">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-268">O tipo de protocolo que está sendo encaminhado quando o valor de **ProtocolType** é 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-268">The type of protocol that is being forwarded when the value of **ProtocolType** is 1 (Other).</span></span> <span data-ttu-id="1b6a9-269">Essa propriedade é herdada do [**CIM \_ ForwardingService**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-269">This property is inherited from [**CIM\_ForwardingService**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-270">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-270">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-271">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-272">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-273">Uma cadeia de caracteres que fornece informações sobre como o proprietário principal do serviço pode ser alcançado.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-273">A string that provides information about how the primary owner of the Service can be reached.</span></span> <span data-ttu-id="1b6a9-274">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-274">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-275">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-275">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-276">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-277">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-278">O nome do proprietário principal do serviço, se um estiver definido.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-278">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="1b6a9-279">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-279">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-280">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-280">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-281">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-282">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-283">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-283">Provides high level status information.</span></span> <span data-ttu-id="1b6a9-284">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-284">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="1b6a9-285">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-285">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1b6a9-286">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1b6a9-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-288"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-288"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-289"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-289"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-290"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-290"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-291"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-291"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-292"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="1b6a9-292"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1b6a9-293">)</span><span class="sxs-lookup"><span data-stu-id="1b6a9-293">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1b6a9-294">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-294">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-295">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-295">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-296">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-297">O tipo de protocolo que está sendo encaminhado.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-297">The type of protocol that is being forwarded.</span></span> <span data-ttu-id="1b6a9-298">Essa propriedade é herdada do [**CIM \_ ForwardingService**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-298">This property is inherited from [**CIM\_ForwardingService**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-299">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-299">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-300">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-300">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-301">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-302">O último estado solicitado ou desejado para o serviço de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-302">The last requested or desired state for the management service.</span></span> <span data-ttu-id="1b6a9-303">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-303">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-304">**ServiceURL**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-304">**ServiceURL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-305">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-306">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-307">Não use.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-307">Do not use.</span></span> <span data-ttu-id="1b6a9-308">Uma URL que fornece o protocolo, o local de rede e outras informações específicas do serviço necessárias para acessar o serviço.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-308">A URL that provides the protocol, network location, and other service-specific information required to access the service.</span></span> <span data-ttu-id="1b6a9-309">Em vez disso, use a classe **ServiceAccessURI** , que posiciona corretamente a semântica do acesso ao serviço e esclarece o formato das informações.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-309">Instead, use the **ServiceAccessURI** class, which correctly positions the semantics of the service access, and clarifies the format of the information.</span></span> <span data-ttu-id="1b6a9-310">Essa propriedade é herdada do [**CIM \_ NetworkService**](/previous-versions//cc136875(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-310">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-311">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-311">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-312">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-313">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-314">Indica se o serviço foi iniciado (**true**) ou parado (**false**).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-314">Indicates whether the service has been started (**True**), or stopped (**False**).</span></span> <span data-ttu-id="1b6a9-315">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-315">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-316">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-316">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-317">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-319">Indica se o serviço é iniciado automaticamente por um sistema, um sistema operacional e assim por diante ou se é iniciado somente mediante solicitação.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-319">Indicates whether the service is automatically started by a system, an operating system, and so on, or is started only upon request.</span></span> <span data-ttu-id="1b6a9-320">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-320">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-321">**StartupConditions**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-321">**StartupConditions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-322">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-322">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-323">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-324">Não use.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-324">Do not use.</span></span> <span data-ttu-id="1b6a9-325">Uma matriz de forma livre de cadeias de caracteres que especificam as pré-condições específicas que devem ser atendidas para que esse serviço seja iniciado corretamente.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-325">A free-form array of strings that specify any specific preconditions that must be met for this service to start correctly.</span></span> <span data-ttu-id="1b6a9-326">Esta propriedade não é útil porque não está padronizada.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-326">This property is not useful because it is not standardized.</span></span> <span data-ttu-id="1b6a9-327">Se essa propriedade fosse uma construção necessária, ela seria necessária mais alta na hierarquia de herança (no serviço).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-327">If this property were a necessary construct, then it would be required higher in the inheritance hierarchy (on Service).</span></span> <span data-ttu-id="1b6a9-328">Essa propriedade é herdada do [**CIM \_ NetworkService**](/previous-versions//cc136875(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-328">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-329">**StartupParameters**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-329">**StartupParameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-330">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-330">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-331">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-332">Não use.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-332">Do not use.</span></span> <span data-ttu-id="1b6a9-333">Uma matriz de forma livre de cadeias de caracteres que especificam quaisquer parâmetros específicos que devem ser fornecidos ao método **StartService** para que esse serviço seja iniciado corretamente.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-333">A free-form array of strings that specify any specific parameters that must be supplied to the **StartService** method for this service to start correctly.</span></span> <span data-ttu-id="1b6a9-334">Se esse método fosse refinado, seus parâmetros transmitirão formalmente essas informações.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-334">If this method were refined, then its parameters would more formally convey this information.</span></span> <span data-ttu-id="1b6a9-335">Essa propriedade é herdada do [**CIM \_ NetworkService**](/previous-versions//cc136875(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-335">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-336">**Status**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-336">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-337">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-338">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-339">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-339">The current status of the object.</span></span> <span data-ttu-id="1b6a9-340">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-341">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-341">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-342">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-344">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="1b6a9-344">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="1b6a9-345">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-345">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-346">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-346">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-347">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-348">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-349">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-349">The creation class name of the scoping system.</span></span> <span data-ttu-id="1b6a9-350">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-350">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-351">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-351">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-352">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-354">O nome NetBIOS do sistema de computador de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-354">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="1b6a9-355">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-355">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-356">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-356">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-357">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-357">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-358">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-359">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-359">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="1b6a9-360">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e não é usada.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-360">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1b6a9-361">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-361">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b6a9-362">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1b6a9-363">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b6a9-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b6a9-364">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-364">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="1b6a9-365">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-365">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1b6a9-366">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b6a9-366">Remarks</span></span>

<span data-ttu-id="1b6a9-367">O acesso à classe **Msvm \_ TransparentBridgingService** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="1b6a9-367">Access to the **Msvm\_TransparentBridgingService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1b6a9-368">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="1b6a9-368">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="1b6a9-369">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b6a9-369">Requirements</span></span>



| <span data-ttu-id="1b6a9-370">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b6a9-370">Requirement</span></span> | <span data-ttu-id="1b6a9-371">Valor</span><span class="sxs-lookup"><span data-stu-id="1b6a9-371">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b6a9-372">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b6a9-372">Minimum supported client</span></span><br/> | <span data-ttu-id="1b6a9-373">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1b6a9-373">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1b6a9-374">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b6a9-374">Minimum supported server</span></span><br/> | <span data-ttu-id="1b6a9-375">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1b6a9-375">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1b6a9-376">Namespace</span><span class="sxs-lookup"><span data-stu-id="1b6a9-376">Namespace</span></span><br/>                | <span data-ttu-id="1b6a9-377">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="1b6a9-377">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1b6a9-378">MOF</span><span class="sxs-lookup"><span data-stu-id="1b6a9-378">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b6a9-379"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b6a9-379"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b6a9-380">DLL</span><span class="sxs-lookup"><span data-stu-id="1b6a9-380">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b6a9-381"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1b6a9-381"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1b6a9-382">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b6a9-382">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b6a9-383">**\_TRANSPARENTBRIDGINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-383">**CIM\_TransparentBridgingService**</span></span>](cim-transparentbridgingservice.md)
</dt> <dt>

[<span data-ttu-id="1b6a9-384">**\_TRANSPARENTBRIDGINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="1b6a9-384">**CIM\_TransparentBridgingService**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice)
</dt> </dl>

 

