---
description: Fornece o gerenciamento ativo de pools de recursos.
ms.assetid: 34ee3189-cb89-4d36-b12f-333449103968
title: Classe Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService
- Msvm_ResourcePoolConfigurationService.RequestStateChange
- Msvm_ResourcePoolConfigurationService.StartService
- Msvm_ResourcePoolConfigurationService.StopService
- Msvm_ResourcePoolConfigurationService.InstanceID
- Msvm_ResourcePoolConfigurationService.Caption
- Msvm_ResourcePoolConfigurationService.Description
- Msvm_ResourcePoolConfigurationService.ElementName
- Msvm_ResourcePoolConfigurationService.InstallDate
- Msvm_ResourcePoolConfigurationService.Name
- Msvm_ResourcePoolConfigurationService.OperationalStatus
- Msvm_ResourcePoolConfigurationService.StatusDescriptions
- Msvm_ResourcePoolConfigurationService.Status
- Msvm_ResourcePoolConfigurationService.HealthState
- Msvm_ResourcePoolConfigurationService.CommunicationStatus
- Msvm_ResourcePoolConfigurationService.DetailedStatus
- Msvm_ResourcePoolConfigurationService.OperatingStatus
- Msvm_ResourcePoolConfigurationService.PrimaryStatus
- Msvm_ResourcePoolConfigurationService.EnabledState
- Msvm_ResourcePoolConfigurationService.OtherEnabledState
- Msvm_ResourcePoolConfigurationService.RequestedState
- Msvm_ResourcePoolConfigurationService.EnabledDefault
- Msvm_ResourcePoolConfigurationService.TimeOfLastStateChange
- Msvm_ResourcePoolConfigurationService.AvailableRequestedStates
- Msvm_ResourcePoolConfigurationService.TransitioningToState
- Msvm_ResourcePoolConfigurationService.SystemCreationClassName
- Msvm_ResourcePoolConfigurationService.SystemName
- Msvm_ResourcePoolConfigurationService.CreationClassName
- Msvm_ResourcePoolConfigurationService.PrimaryOwnerName
- Msvm_ResourcePoolConfigurationService.PrimaryOwnerContact
- Msvm_ResourcePoolConfigurationService.StartMode
- Msvm_ResourcePoolConfigurationService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3160e8ac9ba011db70a5d7118e4d1f72733ff23f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837125"
---
# <a name="msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="c9907-103">\_Classe Msvm ResourcePoolConfigurationService</span><span class="sxs-lookup"><span data-stu-id="c9907-103">Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="c9907-104">Fornece o gerenciamento ativo de pools de recursos.</span><span class="sxs-lookup"><span data-stu-id="c9907-104">Provides for active management of resource pools.</span></span>

<span data-ttu-id="c9907-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c9907-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9907-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9907-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ResourcePoolConfigurationService : CIM_Service
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
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="c9907-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c9907-107">Members</span></span>

<span data-ttu-id="c9907-108">A classe **Msvm \_ ResourcePoolConfigurationService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c9907-108">The **Msvm\_ResourcePoolConfigurationService** class has these types of members:</span></span>

-   [<span data-ttu-id="c9907-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="c9907-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="c9907-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c9907-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c9907-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="c9907-111">Methods</span></span>

<span data-ttu-id="c9907-112">A classe **Msvm \_ ResourcePoolConfigurationService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c9907-112">The **Msvm\_ResourcePoolConfigurationService** class has these methods.</span></span>



| <span data-ttu-id="c9907-113">Método</span><span class="sxs-lookup"><span data-stu-id="c9907-113">Method</span></span>                                                                                   | <span data-ttu-id="c9907-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="c9907-114">Description</span></span>                                                                                  |
|:-----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9907-115">**CreatePool**</span><span class="sxs-lookup"><span data-stu-id="c9907-115">**CreatePool**</span></span>](createpool-msvm-resourcepoolconfigurationservice.md)                   | <span data-ttu-id="c9907-116">Cria um pool de recursos filho.</span><span class="sxs-lookup"><span data-stu-id="c9907-116">Creates a child resource pool.</span></span><br/>                                                    |
| [<span data-ttu-id="c9907-117">**DeletePool**</span><span class="sxs-lookup"><span data-stu-id="c9907-117">**DeletePool**</span></span>](deletepool-msvm-resourcepoolconfigurationservice.md)                   | <span data-ttu-id="c9907-118">Exclui um pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="c9907-118">Deletes a resource pool.</span></span><br/>                                                          |
| [<span data-ttu-id="c9907-119">**ModifyPoolResources**</span><span class="sxs-lookup"><span data-stu-id="c9907-119">**ModifyPoolResources**</span></span>](modifypoolresources-msvm-resourcepoolconfigurationservice.md) | <span data-ttu-id="c9907-120">Altera as configurações de recurso de pool pai para recursos atribuídos a um pool filho.</span><span class="sxs-lookup"><span data-stu-id="c9907-120">Changes the parent pool resource settings for resources assigned to a child pool.</span></span><br/> |
| [<span data-ttu-id="c9907-121">**ModifyPoolSettings**</span><span class="sxs-lookup"><span data-stu-id="c9907-121">**ModifyPoolSettings**</span></span>](modifypoolsettings-msvm-resourcepoolconfigurationservice.md)   | <span data-ttu-id="c9907-122">Altera as configurações de um pool filho que não estão relacionados à alocação.</span><span class="sxs-lookup"><span data-stu-id="c9907-122">Changes the settings of a child pool that are not allocation related.</span></span><br/>             |
| <span data-ttu-id="c9907-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="c9907-123">**RequestStateChange**</span></span>                                                                   | <span data-ttu-id="c9907-124">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="c9907-124">This method is not supported.</span></span><br/>                                                     |
| <span data-ttu-id="c9907-125">**StartService**</span><span class="sxs-lookup"><span data-stu-id="c9907-125">**StartService**</span></span>                                                                         | <span data-ttu-id="c9907-126">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="c9907-126">This method is not supported.</span></span><br/>                                                     |
| <span data-ttu-id="c9907-127">**StopService**</span><span class="sxs-lookup"><span data-stu-id="c9907-127">**StopService**</span></span>                                                                          | <span data-ttu-id="c9907-128">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="c9907-128">This method is not supported.</span></span><br/>                                                     |



 

### <a name="properties"></a><span data-ttu-id="c9907-129">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c9907-129">Properties</span></span>

<span data-ttu-id="c9907-130">A classe **Msvm \_ ResourcePoolConfigurationService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c9907-130">The **Msvm\_ResourcePoolConfigurationService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c9907-131">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="c9907-131">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-132">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9907-132">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c9907-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9907-134">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="c9907-134">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="c9907-135">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c9907-135">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c9907-136">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="c9907-136">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c9907-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9907-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9907-139">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="c9907-139">A short description of the object.</span></span> <span data-ttu-id="c9907-140">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c9907-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c9907-141">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="c9907-141">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-142">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9907-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c9907-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9907-144">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="c9907-144">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="c9907-145">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="c9907-145">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c9907-146">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c9907-146">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c9907-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="c9907-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-148"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="c9907-148"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-149"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="c9907-149"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-150"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="c9907-150"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-151"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="c9907-151"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-152"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="c9907-152"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-153"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="c9907-153"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c9907-154">)</span><span class="sxs-lookup"><span data-stu-id="c9907-154">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c9907-155">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c9907-155">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c9907-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9907-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9907-158">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="c9907-158">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="c9907-159">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="c9907-159">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c9907-160">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="c9907-160">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="c9907-161">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c9907-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c9907-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9907-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9907-164">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="c9907-164">A description of the object.</span></span> <span data-ttu-id="c9907-165">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c9907-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c9907-166">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="c9907-166">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-167">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9907-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c9907-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9907-169">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="c9907-169">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="c9907-170">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="c9907-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c9907-171">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c9907-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c9907-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="c9907-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="c9907-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="c9907-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="c9907-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="c9907-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="c9907-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="c9907-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="c9907-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c9907-180">)</span><span class="sxs-lookup"><span data-stu-id="c9907-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c9907-181">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c9907-181">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c9907-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9907-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9907-184">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="c9907-184">A display name for the object.</span></span> <span data-ttu-id="c9907-185">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c9907-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c9907-186">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="c9907-186">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-187">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9907-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c9907-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9907-189">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="c9907-189">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="c9907-190">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="c9907-190">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="c9907-191">Valor</span><span class="sxs-lookup"><span data-stu-id="c9907-191">Value</span></span>                                                                        | <span data-ttu-id="c9907-192">Significado</span><span class="sxs-lookup"><span data-stu-id="c9907-192">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="c9907-193"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c9907-193"><dt>2</dt></span></span> </dl> | <span data-ttu-id="c9907-194">habilitado</span><span class="sxs-lookup"><span data-stu-id="c9907-194">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c9907-195">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="c9907-195">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-196">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9907-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c9907-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9907-198">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="c9907-198">The enabled and disabled states of an element.</span></span> <span data-ttu-id="c9907-199">Essa propriedade também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="c9907-199">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="c9907-200">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="c9907-200">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="c9907-201">Valor</span><span class="sxs-lookup"><span data-stu-id="c9907-201">Value</span></span>                                                                        | <span data-ttu-id="c9907-202">Significado</span><span class="sxs-lookup"><span data-stu-id="c9907-202">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="c9907-203"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c9907-203"><dt>2</dt></span></span> </dl> | <span data-ttu-id="c9907-204">habilitado</span><span class="sxs-lookup"><span data-stu-id="c9907-204">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c9907-205">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="c9907-205">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-206">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9907-206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c9907-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9907-208">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="c9907-208">The current health of the element.</span></span> <span data-ttu-id="c9907-209">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="c9907-209">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="c9907-210">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="c9907-210">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="c9907-211">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c9907-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c9907-212">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c9907-212">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-213">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c9907-213">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c9907-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9907-215">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="c9907-215">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="c9907-216">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c9907-216">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c9907-217">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c9907-217">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-218">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c9907-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9907-219">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9907-220">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="c9907-220">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c9907-221">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="c9907-221">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c9907-222">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c9907-222">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c9907-223">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c9907-223">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-224">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c9907-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9907-225">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9907-226">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="c9907-226">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="c9907-227">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="c9907-227">The label by which the object is known.</span></span> <span data-ttu-id="c9907-228">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c9907-228">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c9907-229">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="c9907-229">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-230">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9907-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c9907-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9907-232">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="c9907-232">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="c9907-233">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="c9907-233">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c9907-234">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c9907-234">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c9907-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="c9907-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="c9907-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="c9907-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="c9907-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="c9907-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="c9907-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="c9907-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="c9907-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="c9907-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="c9907-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="c9907-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="c9907-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="c9907-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="c9907-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="c9907-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="c9907-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="c9907-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="c9907-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="c9907-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c9907-254">)</span><span class="sxs-lookup"><span data-stu-id="c9907-254">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c9907-255">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="c9907-255">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-256">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9907-256">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c9907-257">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9907-258">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="c9907-258">The current statuses of the object.</span></span> <span data-ttu-id="c9907-259">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c9907-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c9907-260">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="c9907-260">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-261">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c9907-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9907-262">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9907-263">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="c9907-263">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="c9907-264">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="c9907-264">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="c9907-265">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c9907-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c9907-266">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="c9907-266">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-267">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c9907-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9907-268">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9907-269">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="c9907-269">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="c9907-270">Todas as informações sobre como o proprietário principal do serviço podem ser atingidas (por exemplo, número de telefone, endereço de email e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="c9907-270">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="c9907-271">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="c9907-271">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c9907-272">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="c9907-272">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-273">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c9907-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9907-274">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9907-275">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="c9907-275">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="c9907-276">O nome do proprietário principal do serviço, se um estiver definido.</span><span class="sxs-lookup"><span data-stu-id="c9907-276">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="c9907-277">O proprietário principal é o contato de suporte inicial para o serviço.</span><span class="sxs-lookup"><span data-stu-id="c9907-277">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="c9907-278">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="c9907-278">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c9907-279">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="c9907-279">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-280">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9907-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c9907-281">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9907-282">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="c9907-282">Provides high level status information.</span></span> <span data-ttu-id="c9907-283">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="c9907-283">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="c9907-284">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="c9907-284">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c9907-285">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c9907-285">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c9907-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="c9907-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-287"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="c9907-287"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-288"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="c9907-288"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-289"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="c9907-289"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-290"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="c9907-290"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c9907-291"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="c9907-291"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c9907-292">)</span><span class="sxs-lookup"><span data-stu-id="c9907-292">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c9907-293">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="c9907-293">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-294">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9907-294">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c9907-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9907-296">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="c9907-296">The last requested or desired state for the element.</span></span> <span data-ttu-id="c9907-297">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="c9907-297">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="c9907-298">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais para um elemento.</span><span class="sxs-lookup"><span data-stu-id="c9907-298">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="c9907-299">Uma instância específica da classe [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) pode não oferecer suporte à propriedade **requestedstate** .</span><span class="sxs-lookup"><span data-stu-id="c9907-299">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="c9907-300">Se isso ocorrer, o valor 12 ("não aplicável") será usado.</span><span class="sxs-lookup"><span data-stu-id="c9907-300">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="c9907-301">Essa propriedade é herdada do **CIM \_ EnabledLogicalElement** e é sempre definida como 12 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="c9907-301">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="c9907-302">Valor</span><span class="sxs-lookup"><span data-stu-id="c9907-302">Value</span></span>                                                                         | <span data-ttu-id="c9907-303">Significado</span><span class="sxs-lookup"><span data-stu-id="c9907-303">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="c9907-304"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="c9907-304"><dt>12</dt></span></span> </dl> | <span data-ttu-id="c9907-305">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="c9907-305">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c9907-306">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="c9907-306">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-307">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c9907-307">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c9907-308">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9907-309">Indica se o serviço está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="c9907-309">Indicates whether the service is currently running.</span></span> <span data-ttu-id="c9907-310">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="c9907-310">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="c9907-311">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="c9907-311">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-312">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c9907-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9907-313">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9907-314">Qualificadores: **maxlen** (10)</span><span class="sxs-lookup"><span data-stu-id="c9907-314">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="c9907-315">Um valor de cadeia de caracteres que indica se o serviço é iniciado automaticamente por um sistema, um sistema operacional ou é iniciado somente mediante solicitação.</span><span class="sxs-lookup"><span data-stu-id="c9907-315">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="c9907-316">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="c9907-316">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c9907-317">**Status**</span><span class="sxs-lookup"><span data-stu-id="c9907-317">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-318">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c9907-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9907-319">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9907-320">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="c9907-320">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c9907-321">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c9907-321">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-322">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c9907-322">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c9907-323">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9907-324">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="c9907-324">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="c9907-325">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c9907-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c9907-326">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c9907-326">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-327">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c9907-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9907-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9907-329">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="c9907-329">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="c9907-330">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="c9907-330">The scoping system's creation class name.</span></span> <span data-ttu-id="c9907-331">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="c9907-331">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="c9907-332">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c9907-332">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-333">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c9907-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9907-334">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9907-335">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="c9907-335">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="c9907-336">O nome NetBIOS do sistema de computador de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="c9907-336">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="c9907-337">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="c9907-337">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="c9907-338">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="c9907-338">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-339">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c9907-339">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c9907-340">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9907-341">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="c9907-341">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="c9907-342">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c9907-342">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c9907-343">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="c9907-343">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9907-344">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9907-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c9907-345">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9907-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9907-346">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="c9907-346">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="c9907-347">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c9907-347">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9907-348">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9907-348">Requirements</span></span>



| <span data-ttu-id="c9907-349">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9907-349">Requirement</span></span> | <span data-ttu-id="c9907-350">Valor</span><span class="sxs-lookup"><span data-stu-id="c9907-350">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9907-351">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9907-351">Minimum supported client</span></span><br/> | <span data-ttu-id="c9907-352">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c9907-352">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="c9907-353">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9907-353">Minimum supported server</span></span><br/> | <span data-ttu-id="c9907-354">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="c9907-354">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c9907-355">Namespace</span><span class="sxs-lookup"><span data-stu-id="c9907-355">Namespace</span></span><br/>                | <span data-ttu-id="c9907-356">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="c9907-356">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c9907-357">MOF</span><span class="sxs-lookup"><span data-stu-id="c9907-357">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9907-358"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9907-358"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9907-359">DLL</span><span class="sxs-lookup"><span data-stu-id="c9907-359">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9907-360"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c9907-360"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

