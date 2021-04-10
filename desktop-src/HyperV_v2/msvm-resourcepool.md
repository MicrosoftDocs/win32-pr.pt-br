---
description: Descreve um tipo de recurso virtual disponível para uso em máquinas virtuais.
ms.assetid: A93D990E-D921-4113-8D88-218D0F84EFA0
title: Classe Msvm_ResourcePool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePool
- Msvm_ResourcePool.InstanceID
- Msvm_ResourcePool.Caption
- Msvm_ResourcePool.Description
- Msvm_ResourcePool.ElementName
- Msvm_ResourcePool.InstallDate
- Msvm_ResourcePool.Name
- Msvm_ResourcePool.OperationalStatus
- Msvm_ResourcePool.StatusDescriptions
- Msvm_ResourcePool.Status
- Msvm_ResourcePool.HealthState
- Msvm_ResourcePool.CommunicationStatus
- Msvm_ResourcePool.DetailedStatus
- Msvm_ResourcePool.OperatingStatus
- Msvm_ResourcePool.PrimaryStatus
- Msvm_ResourcePool.PoolID
- Msvm_ResourcePool.Primordial
- Msvm_ResourcePool.Capacity
- Msvm_ResourcePool.Reserved
- Msvm_ResourcePool.ResourceType
- Msvm_ResourcePool.OtherResourceType
- Msvm_ResourcePool.ResourceSubType
- Msvm_ResourcePool.AllocationUnits
- Msvm_ResourcePool.ConsumedResourceUnits
- Msvm_ResourcePool.CurrentlyConsumedResource
- Msvm_ResourcePool.MaxConsumableResource
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7c45f67a3e1b7c2b4b5291b24beddcdd4cf5e964
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170062"
---
# <a name="msvm_resourcepool-class"></a><span data-ttu-id="9af4e-103">\_Classe Msvm ResourcePool</span><span class="sxs-lookup"><span data-stu-id="9af4e-103">Msvm\_ResourcePool class</span></span>

<span data-ttu-id="9af4e-104">Descreve um tipo de recurso virtual disponível para uso em máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="9af4e-104">Describes a type of virtual resource available for use in virtual machines.</span></span> <span data-ttu-id="9af4e-105">O pool de recursos agrega recursos físicos e é usado para alocar recursos para máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="9af4e-105">The resource pool aggregates physical resources and is used to allocate resources to virtual machines.</span></span> <span data-ttu-id="9af4e-106">No Hyper-V, todos os pools de recursos são primordialmente, e há exatamente um pool para cada tipo específico de recurso que pode ser alocado a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9af4e-106">In Hyper-V, all resource pools are primordial, and there is exactly one pool for each specific type of resource which may be allocated to a virtual machine.</span></span>

<span data-ttu-id="9af4e-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9af4e-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9af4e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9af4e-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourcePool : CIM_ResourcePool
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
  string   PoolID = "Microsoft:GUID\Root";
  boolean  Primordial = False;
  uint64   Capacity;
  uint64   Reserved;
  uint16   ResourceType = 4;
  string   OtherResourceType;
  string   ResourceSubType;
  string   AllocationUnits = "Megabyte";
  string   ConsumedResourceUnits = "count";
  uint64   CurrentlyConsumedResource;
  uint64   MaxConsumableResource;
};
```

## <a name="members"></a><span data-ttu-id="9af4e-109">Membros</span><span class="sxs-lookup"><span data-stu-id="9af4e-109">Members</span></span>

<span data-ttu-id="9af4e-110">A classe **Msvm \_ ResourcePool** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9af4e-110">The **Msvm\_ResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="9af4e-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9af4e-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9af4e-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9af4e-112">Properties</span></span>

<span data-ttu-id="9af4e-113">A classe **Msvm \_ ResourcePool** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9af4e-113">The **Msvm\_ResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9af4e-114">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="9af4e-114">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af4e-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9af4e-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9af4e-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af4e-117">As unidades de alocação usadas pelo pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="9af4e-117">The units of allocation used by the resource pool.</span></span> <span data-ttu-id="9af4e-118">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))e é definida como "megabyte".</span><span class="sxs-lookup"><span data-stu-id="9af4e-118">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to "Megabyte".</span></span>

</dd> <dt>

<span data-ttu-id="9af4e-119">**Capacidade**</span><span class="sxs-lookup"><span data-stu-id="9af4e-119">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af4e-120">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9af4e-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9af4e-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af4e-122">A quantidade máxima (em unidades de **AllocationUnits**) de reservas ativas às quais o pool de recursos pode dar suporte.</span><span class="sxs-lookup"><span data-stu-id="9af4e-122">The maximum amount (in units of **AllocationUnits**) of active reservations that the resource pool can support.</span></span> <span data-ttu-id="9af4e-123">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9af4e-123">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9af4e-124">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="9af4e-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af4e-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9af4e-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9af4e-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af4e-127">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="9af4e-127">A short description of the object.</span></span> <span data-ttu-id="9af4e-128">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9af4e-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9af4e-129">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="9af4e-129">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af4e-130">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9af4e-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9af4e-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af4e-132">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="9af4e-132">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="9af4e-133">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="9af4e-133">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9af4e-134">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9af4e-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9af4e-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="9af4e-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="9af4e-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="9af4e-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="9af4e-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="9af4e-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9af4e-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="9af4e-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9af4e-142">)</span><span class="sxs-lookup"><span data-stu-id="9af4e-142">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9af4e-143">**ConsumedResourceUnits**</span><span class="sxs-lookup"><span data-stu-id="9af4e-143">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af4e-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9af4e-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9af4e-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af4e-146">Especifica as unidades para as propriedades **MaxConsumableResource** e **CurrentlyConsumedResource** .</span><span class="sxs-lookup"><span data-stu-id="9af4e-146">Specifies the units for the **MaxConsumableResource** and the **CurrentlyConsumedResource** properties.</span></span>

</dd> <dt>

<span data-ttu-id="9af4e-147">**CurrentlyConsumedResource**</span><span class="sxs-lookup"><span data-stu-id="9af4e-147">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af4e-148">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9af4e-148">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9af4e-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af4e-150">Especifica a quantidade de recursos que o pool de recursos apresenta atualmente aos consumidores.</span><span class="sxs-lookup"><span data-stu-id="9af4e-150">Specifies the amount of resource that the resource pool currently presents to consumers.</span></span> <span data-ttu-id="9af4e-151">Essa propriedade é diferente da propriedade **reservada** , pois descreve a exibição de consumidores do recurso, enquanto a propriedade **reservada** descreve a exibição de produtores do recurso.</span><span class="sxs-lookup"><span data-stu-id="9af4e-151">This property is different from the **Reserved** property in that it describes the consumers view of the resource, while the **Reserved** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="9af4e-152">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9af4e-152">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af4e-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9af4e-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9af4e-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af4e-155">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="9af4e-155">A description of the object.</span></span> <span data-ttu-id="9af4e-156">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9af4e-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9af4e-157">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="9af4e-157">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af4e-158">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9af4e-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9af4e-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af4e-160">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="9af4e-160">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="9af4e-161">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="9af4e-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9af4e-162">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9af4e-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9af4e-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="9af4e-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="9af4e-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="9af4e-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="9af4e-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="9af4e-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="9af4e-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9af4e-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="9af4e-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9af4e-171">)</span><span class="sxs-lookup"><span data-stu-id="9af4e-171">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9af4e-172">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9af4e-172">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af4e-173">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9af4e-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9af4e-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af4e-175">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="9af4e-175">A display name for the object.</span></span> <span data-ttu-id="9af4e-176">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9af4e-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9af4e-177">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="9af4e-177">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af4e-178">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9af4e-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9af4e-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af4e-180">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="9af4e-180">The current health of the element.</span></span> <span data-ttu-id="9af4e-181">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9af4e-181">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9af4e-182">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9af4e-182">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af4e-183">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9af4e-183">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9af4e-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af4e-185">A data e a hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="9af4e-185">The date and time when the object was installed.</span></span> <span data-ttu-id="9af4e-186">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="9af4e-186">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="9af4e-187">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9af4e-187">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9af4e-188">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9af4e-188">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af4e-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9af4e-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9af4e-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-191">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="9af4e-191">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9af4e-192">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="9af4e-192">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9af4e-193">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9af4e-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9af4e-194">**MaxConsumableResource**</span><span class="sxs-lookup"><span data-stu-id="9af4e-194">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af4e-195">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9af4e-195">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9af4e-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af4e-197">Especifica a quantidade máxima de recursos consumíveis que o pool de recursos pode apresentar aos consumidores.</span><span class="sxs-lookup"><span data-stu-id="9af4e-197">Specifies the maximum amount of consumable resource that the resource pool can present to consumers.</span></span> <span data-ttu-id="9af4e-198">Essa propriedade é diferente da propriedade **Capacity** , pois descreve a exibição de consumidores do recurso, enquanto a propriedade **Capacity** descreve a exibição de produtores do recurso.</span><span class="sxs-lookup"><span data-stu-id="9af4e-198">This property is different from the **Capacity** property in that it describes the consumers view of the resource, while the **Capacity** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="9af4e-199">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9af4e-199">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af4e-200">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9af4e-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-201">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9af4e-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af4e-202">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="9af4e-202">The label by which the object is known.</span></span> <span data-ttu-id="9af4e-203">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9af4e-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9af4e-204">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="9af4e-204">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af4e-205">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9af4e-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9af4e-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af4e-207">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="9af4e-207">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="9af4e-208">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="9af4e-208">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9af4e-209">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9af4e-209">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9af4e-210"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="9af4e-210"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-211"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="9af4e-211"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-212"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="9af4e-212"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-213"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="9af4e-213"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-214"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="9af4e-214"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-215"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="9af4e-215"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-216"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="9af4e-216"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-217"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="9af4e-217"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-218"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="9af4e-218"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-219"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="9af4e-219"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-220"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="9af4e-220"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-221"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="9af4e-221"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-222"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="9af4e-222"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-223"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="9af4e-223"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-224"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="9af4e-224"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-225"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="9af4e-225"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-226"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="9af4e-226"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9af4e-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="9af4e-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9af4e-229">)</span><span class="sxs-lookup"><span data-stu-id="9af4e-229">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9af4e-230">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="9af4e-230">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af4e-231">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9af4e-231">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-232">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9af4e-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-233">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="9af4e-233">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="9af4e-234">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="9af4e-234">The current statuses of the object.</span></span> <span data-ttu-id="9af4e-235">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9af4e-235">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="9af4e-236">Se nenhuma condição relacionada a QoS for detectada, o status principal (OperationalStatus \[ 0 \] ) será definido como OK (2).</span><span class="sxs-lookup"><span data-stu-id="9af4e-236">If no QoS related conditions have been detected, the primary status (OperationalStatus\[0\]) is set to OK (2).</span></span> <span data-ttu-id="9af4e-237">Caso contrário, o status principal será definido como degradado (3) e um ou mais valores de status secundários serão preenchidos na matriz, começando no índice 1, que relata condições mais específicas, de acordo com esta tabela.</span><span class="sxs-lookup"><span data-stu-id="9af4e-237">Otherwise, the primary status is set to Degraded (3), and one or more secondary status values is filled in the array, starting at index 1, which report more specific conditions, according to this table.</span></span>



| <span data-ttu-id="9af4e-238">Valor</span><span class="sxs-lookup"><span data-stu-id="9af4e-238">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="9af4e-239">Descrição</span><span class="sxs-lookup"><span data-stu-id="9af4e-239">Description</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9af4e-240"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Taxa de transferência insuficiente (32788)</span><span class="sxs-lookup"><span data-stu-id="9af4e-240"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Insufficient Throughput  (32788)</span></span><br/> | <span data-ttu-id="9af4e-241">No momento, pelo menos um dos discos virtuais alocados no pool está relatando um status de taxa de transferência insuficiente.</span><span class="sxs-lookup"><span data-stu-id="9af4e-241">At least one of the virtual disks allocated from the pool is currently reporting an  Insufficient Throughput  status.</span></span><br/> |



 

<span data-ttu-id="9af4e-242">O provedor WMI do Hyper-V gera um evento [**Msvm \_ StorageAlert**](msvm-storagealert.md) toda vez que o OperationalStatus da classe **Msvm \_ ResourcePool** é alterado.</span><span class="sxs-lookup"><span data-stu-id="9af4e-242">The Hyper-V WMI provider raises an [**Msvm\_StorageAlert**](msvm-storagealert.md) event each time the OperationalStatus of the **Msvm\_ResourcePool** class changes.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9af4e-243">**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="9af4e-243">**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9af4e-244">**Degradado** (3)</span><span class="sxs-lookup"><span data-stu-id="9af4e-244">**Degraded** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="9af4e-245">**Erro não recuperável** (7)</span><span class="sxs-lookup"><span data-stu-id="9af4e-245">**Non-Recoverable Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9af4e-246">**Sem contato** (12)</span><span class="sxs-lookup"><span data-stu-id="9af4e-246">**No Contact** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="9af4e-247">**Comunicação perdida** (13)</span><span class="sxs-lookup"><span data-stu-id="9af4e-247">**Lost Communication** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>

<span data-ttu-id="9af4e-248">**Incompatibilidade de protocolo** (32775)</span><span class="sxs-lookup"><span data-stu-id="9af4e-248">**Protocol Mismatch** (32775)</span></span>


</dt> <dd></dd> <dt>

<span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>

<span data-ttu-id="9af4e-249">**Taxa de transferência insuficiente** (32788)</span><span class="sxs-lookup"><span data-stu-id="9af4e-249">**Insufficient Throughput** (32788)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9af4e-250">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="9af4e-250">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af4e-251">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9af4e-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9af4e-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af4e-253">Uma cadeia de caracteres que descreve o tipo de recurso quando um valor bem definido não está disponível e [**ResourceType**](msvm-processorpool.md) é definido como 0 ("other").</span><span class="sxs-lookup"><span data-stu-id="9af4e-253">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorpool.md) is set to 0 ("Other").</span></span> <span data-ttu-id="9af4e-254">Essa propriedade é herdada de [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)) e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9af4e-254">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)) and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9af4e-255">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="9af4e-255">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af4e-256">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9af4e-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-257">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9af4e-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af4e-258">Esse valor é referenciado pelas instâncias do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) que foram alocadas deste pool.</span><span class="sxs-lookup"><span data-stu-id="9af4e-258">This value is referenced by the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) instances which were allocated from this pool.</span></span> <span data-ttu-id="9af4e-259">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))e é sempre definida como "Microsoft:*GUID* \\ root".</span><span class="sxs-lookup"><span data-stu-id="9af4e-259">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to "Microsoft:*GUID*\\Root".</span></span>

</dd> <dt>

<span data-ttu-id="9af4e-260">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="9af4e-260">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af4e-261">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9af4e-261">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-262">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9af4e-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af4e-263">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="9af4e-263">Provides high level status information.</span></span> <span data-ttu-id="9af4e-264">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="9af4e-264">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="9af4e-265">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="9af4e-265">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9af4e-266">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9af4e-266">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9af4e-267"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="9af4e-267"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-268"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="9af4e-268"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-269"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="9af4e-269"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="9af4e-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-271"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9af4e-271"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-272"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="9af4e-272"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9af4e-273">)</span><span class="sxs-lookup"><span data-stu-id="9af4e-273">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9af4e-274">**Primordial**</span><span class="sxs-lookup"><span data-stu-id="9af4e-274">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af4e-275">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9af4e-275">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-276">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9af4e-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af4e-277">**True** se esse pool de recursos for a base da qual os recursos são desenhados e retornados na atividade do gerenciamento de recursos; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="9af4e-277">**True** if this resource pool is the base from which resources are drawn and returned in the activity of resource management; otherwise, **False**.</span></span> <span data-ttu-id="9af4e-278">Ser primordial significa que esse pool de recursos não pode ser criado ou excluído por consumidores desse modelo.</span><span class="sxs-lookup"><span data-stu-id="9af4e-278">Being primordial means that this resource pool cannot be created or deleted by consumers of this model.</span></span> <span data-ttu-id="9af4e-279">No entanto, outras ações, modeladas ou não, podem afetar as características ou o tamanho dos pools de recursos primordial.</span><span class="sxs-lookup"><span data-stu-id="9af4e-279">However, other actions, modeled or not, may affect the characteristics or size of primordial resource pools.</span></span> <span data-ttu-id="9af4e-280">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9af4e-280">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9af4e-281">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="9af4e-281">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af4e-282">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9af4e-282">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-283">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9af4e-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af4e-284">As reservas atuais (em unidades de **AllocationUnits**) se espalham por todas as alocações ativas deste pool.</span><span class="sxs-lookup"><span data-stu-id="9af4e-284">The current reservations (in units of **AllocationUnits**) spread across all active allocations from this pool.</span></span> <span data-ttu-id="9af4e-285">Em uma configuração hierárquica, isso representa a soma de todas as reservas atuais do pool de recursos descendentes.</span><span class="sxs-lookup"><span data-stu-id="9af4e-285">In a hierarchical configuration, this represents the sum of all descendant resource pool current reservations.</span></span> <span data-ttu-id="9af4e-286">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9af4e-286">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9af4e-287">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="9af4e-287">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af4e-288">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9af4e-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9af4e-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af4e-290">Uma cadeia de caracteres que descreve um subtipo específico de implementação para esse pool.</span><span class="sxs-lookup"><span data-stu-id="9af4e-290">A string that describes an implementation specific sub-type for this pool.</span></span> <span data-ttu-id="9af4e-291">Por exemplo, isso pode ser usado para distinguir modelos diferentes do mesmo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="9af4e-291">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="9af4e-292">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9af4e-292">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9af4e-293">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="9af4e-293">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af4e-294">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9af4e-294">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9af4e-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af4e-296">O tipo de recurso que esse pool de recursos pode alocar.</span><span class="sxs-lookup"><span data-stu-id="9af4e-296">The type of resource this resource pool may allocate.</span></span> <span data-ttu-id="9af4e-297">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))e é definida como 4 ("memória").</span><span class="sxs-lookup"><span data-stu-id="9af4e-297">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to 4 ("Memory").</span></span>

</dd> <dt>

<span data-ttu-id="9af4e-298">**Status**</span><span class="sxs-lookup"><span data-stu-id="9af4e-298">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af4e-299">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9af4e-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-300">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9af4e-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af4e-301">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="9af4e-301">The current status of the object.</span></span> <span data-ttu-id="9af4e-302">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="9af4e-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9af4e-303">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9af4e-303">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af4e-304">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9af4e-304">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9af4e-305">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9af4e-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9af4e-306">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="9af4e-306">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="9af4e-307">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9af4e-307">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9af4e-308">Comentários</span><span class="sxs-lookup"><span data-stu-id="9af4e-308">Remarks</span></span>

<span data-ttu-id="9af4e-309">O acesso à classe **Msvm \_ ResourcePool** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="9af4e-309">Access to the **Msvm\_ResourcePool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9af4e-310">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="9af4e-310">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="9af4e-311">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9af4e-311">Requirements</span></span>



| <span data-ttu-id="9af4e-312">Requisito</span><span class="sxs-lookup"><span data-stu-id="9af4e-312">Requirement</span></span> | <span data-ttu-id="9af4e-313">Valor</span><span class="sxs-lookup"><span data-stu-id="9af4e-313">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9af4e-314">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9af4e-314">Minimum supported client</span></span><br/> | <span data-ttu-id="9af4e-315">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9af4e-315">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9af4e-316">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9af4e-316">Minimum supported server</span></span><br/> | <span data-ttu-id="9af4e-317">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9af4e-317">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9af4e-318">Namespace</span><span class="sxs-lookup"><span data-stu-id="9af4e-318">Namespace</span></span><br/>                | <span data-ttu-id="9af4e-319">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="9af4e-319">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9af4e-320">MOF</span><span class="sxs-lookup"><span data-stu-id="9af4e-320">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9af4e-321"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9af4e-321"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9af4e-322">DLL</span><span class="sxs-lookup"><span data-stu-id="9af4e-322">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9af4e-323"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9af4e-323"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9af4e-324">Confira também</span><span class="sxs-lookup"><span data-stu-id="9af4e-324">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9af4e-325">**\_RESOURCEPOOL CIM**</span><span class="sxs-lookup"><span data-stu-id="9af4e-325">**CIM\_ResourcePool**</span></span>](cim-resourcepool.md)
</dt> <dt>

<span data-ttu-id="9af4e-326">[**\_RESOURCEPOOL CIM**](/previous-versions//cc136903(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9af4e-326">[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9af4e-327">**Msvm \_ ResourcePool (v1)**</span><span class="sxs-lookup"><span data-stu-id="9af4e-327">**Msvm\_ResourcePool (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-resourcepool)
</dt> <dt>

[<span data-ttu-id="9af4e-328">**Msvm \_ StorageAlert**</span><span class="sxs-lookup"><span data-stu-id="9af4e-328">**Msvm\_StorageAlert**</span></span>](msvm-storagealert.md)
</dt> <dt>

[<span data-ttu-id="9af4e-329">Classes de gerenciamento de recursos</span><span class="sxs-lookup"><span data-stu-id="9af4e-329">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

