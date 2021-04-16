---
description: Agrega os recursos do processador que podem ser alocados a uma máquina virtual.
ms.assetid: 73424568-fa6c-4ed8-9640-a67a6d2829f0
title: Classe Msvm_ProcessorPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorPool
- Msvm_ProcessorPool.InstanceID
- Msvm_ProcessorPool.Caption
- Msvm_ProcessorPool.Description
- Msvm_ProcessorPool.ElementName
- Msvm_ProcessorPool.InstallDate
- Msvm_ProcessorPool.Name
- Msvm_ProcessorPool.OperationalStatus
- Msvm_ProcessorPool.StatusDescriptions
- Msvm_ProcessorPool.Status
- Msvm_ProcessorPool.HealthState
- Msvm_ProcessorPool.CommunicationStatus
- Msvm_ProcessorPool.DetailedStatus
- Msvm_ProcessorPool.OperatingStatus
- Msvm_ProcessorPool.PrimaryStatus
- Msvm_ProcessorPool.PoolID
- Msvm_ProcessorPool.Primordial
- Msvm_ProcessorPool.Capacity
- Msvm_ProcessorPool.Reserved
- Msvm_ProcessorPool.ResourceType
- Msvm_ProcessorPool.OtherResourceType
- Msvm_ProcessorPool.ResourceSubType
- Msvm_ProcessorPool.AllocationUnits
- Msvm_ProcessorPool.ConsumedResourceUnits
- Msvm_ProcessorPool.CurrentlyConsumedResource
- Msvm_ProcessorPool.MaxConsumableResource
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 93927483c23147fd387e24cdc5a550a1771457cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758639"
---
# <a name="msvm_processorpool-class"></a><span data-ttu-id="33454-103">\_Classe Msvm ProcessorPool</span><span class="sxs-lookup"><span data-stu-id="33454-103">Msvm\_ProcessorPool class</span></span>

<span data-ttu-id="33454-104">Agrega os recursos do processador que podem ser alocados a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="33454-104">Aggregates the processor resources that may be allocated to a virtual machine.</span></span>

<span data-ttu-id="33454-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="33454-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="33454-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33454-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProcessorPool : CIM_ResourcePool
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

## <a name="members"></a><span data-ttu-id="33454-107">Membros</span><span class="sxs-lookup"><span data-stu-id="33454-107">Members</span></span>

<span data-ttu-id="33454-108">A classe **Msvm \_ ProcessorPool** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="33454-108">The **Msvm\_ProcessorPool** class has these types of members:</span></span>

-   [<span data-ttu-id="33454-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="33454-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="33454-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="33454-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="33454-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="33454-111">Methods</span></span>

<span data-ttu-id="33454-112">A classe **Msvm \_ ProcessorPool** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="33454-112">The **Msvm\_ProcessorPool** class has these methods.</span></span>



| <span data-ttu-id="33454-113">Método</span><span class="sxs-lookup"><span data-stu-id="33454-113">Method</span></span>                                                                          | <span data-ttu-id="33454-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="33454-114">Description</span></span>                                           |
|:--------------------------------------------------------------------------------|:------------------------------------------------------|
| [<span data-ttu-id="33454-115">**CalculatePossibleReserve**</span><span class="sxs-lookup"><span data-stu-id="33454-115">**CalculatePossibleReserve**</span></span>](calculatepossiblereserve-msvm-processorpool.md) | <span data-ttu-id="33454-116">Usado para encontrar a reserva de processador real.</span><span class="sxs-lookup"><span data-stu-id="33454-116">Used to find the actual processor reserve.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="33454-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="33454-117">Properties</span></span>

<span data-ttu-id="33454-118">A classe **Msvm \_ ProcessorPool** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="33454-118">The **Msvm\_ProcessorPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="33454-119">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="33454-119">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33454-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="33454-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33454-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33454-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33454-122">As unidades de alocação usadas pelo pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="33454-122">The units of allocation used by the resource pool.</span></span> <span data-ttu-id="33454-123">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))e é definida como "megabyte".</span><span class="sxs-lookup"><span data-stu-id="33454-123">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to "Megabyte".</span></span>

</dd> <dt>

<span data-ttu-id="33454-124">**Capacidade**</span><span class="sxs-lookup"><span data-stu-id="33454-124">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33454-125">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="33454-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="33454-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33454-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33454-127">A quantidade máxima (em unidades de **AllocationUnits**) de reservas ativas às quais o pool de recursos pode dar suporte.</span><span class="sxs-lookup"><span data-stu-id="33454-127">The maximum amount (in units of **AllocationUnits**) of active reservations that the resource pool can support.</span></span> <span data-ttu-id="33454-128">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="33454-128">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="33454-129">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="33454-129">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33454-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="33454-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33454-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33454-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33454-132">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="33454-132">A short description of the object.</span></span> <span data-ttu-id="33454-133">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="33454-133">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="33454-134">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="33454-134">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33454-135">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="33454-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="33454-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33454-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33454-137">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="33454-137">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="33454-138">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="33454-138">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="33454-139">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="33454-139">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="33454-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="33454-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="33454-141"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="33454-141"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="33454-142"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="33454-142"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="33454-143"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="33454-143"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="33454-144"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="33454-144"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="33454-145"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="33454-145"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="33454-146"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="33454-146"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="33454-147">)</span><span class="sxs-lookup"><span data-stu-id="33454-147">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33454-148">**ConsumedResourceUnits**</span><span class="sxs-lookup"><span data-stu-id="33454-148">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33454-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="33454-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33454-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33454-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33454-151">Especifica as unidades para as propriedades **MaxConsumableResource** e **CurrentlyConsumedResource** .</span><span class="sxs-lookup"><span data-stu-id="33454-151">Specifies the units for the **MaxConsumableResource** and the **CurrentlyConsumedResource** properties.</span></span> <span data-ttu-id="33454-152">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="33454-152">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="33454-153">**CurrentlyConsumedResource**</span><span class="sxs-lookup"><span data-stu-id="33454-153">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33454-154">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="33454-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="33454-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33454-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33454-156">Especifica a quantidade de recursos que o pool de recursos apresenta atualmente aos consumidores.</span><span class="sxs-lookup"><span data-stu-id="33454-156">Specifies the amount of resource that the resource pool currently presents to consumers.</span></span> <span data-ttu-id="33454-157">Essa propriedade é diferente da propriedade **reservada** , pois descreve a exibição de consumidores do recurso, enquanto a propriedade **reservada** descreve a exibição de produtores do recurso.</span><span class="sxs-lookup"><span data-stu-id="33454-157">This property is different from the **Reserved** property in that it describes the consumers view of the resource, while the **Reserved** property describes the producers view of the resource.</span></span> <span data-ttu-id="33454-158">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="33454-158">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="33454-159">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="33454-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33454-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="33454-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33454-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33454-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33454-162">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="33454-162">A description of the object.</span></span> <span data-ttu-id="33454-163">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="33454-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="33454-164">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="33454-164">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33454-165">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="33454-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="33454-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33454-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33454-167">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="33454-167">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="33454-168">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="33454-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="33454-169">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="33454-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="33454-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="33454-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="33454-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="33454-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="33454-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="33454-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="33454-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="33454-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="33454-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="33454-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="33454-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="33454-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="33454-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="33454-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="33454-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="33454-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="33454-178">)</span><span class="sxs-lookup"><span data-stu-id="33454-178">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33454-179">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="33454-179">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33454-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="33454-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33454-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33454-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33454-182">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="33454-182">A display name for the object.</span></span> <span data-ttu-id="33454-183">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="33454-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="33454-184">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="33454-184">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33454-185">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="33454-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="33454-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33454-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33454-187">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="33454-187">The current health of the element.</span></span> <span data-ttu-id="33454-188">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="33454-188">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="33454-189">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="33454-189">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33454-190">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="33454-190">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="33454-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33454-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33454-192">A data e a hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="33454-192">The date and time when the object was installed.</span></span> <span data-ttu-id="33454-193">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="33454-193">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="33454-194">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="33454-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="33454-195">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="33454-195">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33454-196">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="33454-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33454-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33454-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33454-198">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="33454-198">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="33454-199">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="33454-199">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="33454-200">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="33454-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="33454-201">**MaxConsumableResource**</span><span class="sxs-lookup"><span data-stu-id="33454-201">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33454-202">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="33454-202">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="33454-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33454-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33454-204">Especifica a quantidade máxima de recursos consumíveis que o pool de recursos pode apresentar aos consumidores.</span><span class="sxs-lookup"><span data-stu-id="33454-204">Specifies the maximum amount of consumable resource that the resource pool can present to consumers.</span></span> <span data-ttu-id="33454-205">Essa propriedade é diferente da propriedade **Capacity** , pois descreve a exibição de consumidores do recurso, enquanto a propriedade **Capacity** descreve a exibição de produtores do recurso.</span><span class="sxs-lookup"><span data-stu-id="33454-205">This property is different from the **Capacity** property in that it describes the consumers view of the resource, while the **Capacity** property describes the producers view of the resource.</span></span> <span data-ttu-id="33454-206">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="33454-206">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="33454-207">**Nome**</span><span class="sxs-lookup"><span data-stu-id="33454-207">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33454-208">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="33454-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33454-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33454-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33454-210">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="33454-210">The label by which the object is known.</span></span> <span data-ttu-id="33454-211">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="33454-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="33454-212">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="33454-212">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33454-213">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="33454-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="33454-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33454-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33454-215">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="33454-215">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="33454-216">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="33454-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="33454-217">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="33454-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="33454-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="33454-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="33454-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="33454-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="33454-220"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="33454-220"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="33454-221"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="33454-221"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="33454-222"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="33454-222"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="33454-223"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="33454-223"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="33454-224"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="33454-224"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="33454-225"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="33454-225"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="33454-226"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="33454-226"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="33454-227"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="33454-227"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="33454-228"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="33454-228"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="33454-229"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="33454-229"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="33454-230"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="33454-230"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="33454-231"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="33454-231"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="33454-232"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="33454-232"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="33454-233"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="33454-233"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="33454-234"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="33454-234"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="33454-235"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="33454-235"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="33454-236"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="33454-236"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="33454-237">)</span><span class="sxs-lookup"><span data-stu-id="33454-237">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33454-238">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="33454-238">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33454-239">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="33454-239">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="33454-240">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33454-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33454-241">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="33454-241">The current statuses of the object.</span></span> <span data-ttu-id="33454-242">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="33454-242">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="33454-243">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="33454-243">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33454-244">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="33454-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33454-245">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33454-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33454-246">Uma cadeia de caracteres que descreve o tipo de recurso quando um valor bem definido não está disponível e **ResourceType** é definido como 0 ("other").</span><span class="sxs-lookup"><span data-stu-id="33454-246">A string that describes the resource type when a well-defined value is not available and **ResourceType** is set to 0 ("Other").</span></span> <span data-ttu-id="33454-247">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="33454-247">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="33454-248">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="33454-248">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33454-249">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="33454-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33454-250">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33454-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33454-251">Esse valor é referenciado pelas instâncias do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) que foram alocadas deste pool.</span><span class="sxs-lookup"><span data-stu-id="33454-251">This value is referenced by the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) instances which were allocated from this pool.</span></span> <span data-ttu-id="33454-252">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))e é sempre definida como "Microsoft:*GUID* \\ root".</span><span class="sxs-lookup"><span data-stu-id="33454-252">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to "Microsoft:*GUID*\\Root".</span></span>

</dd> <dt>

<span data-ttu-id="33454-253">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="33454-253">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33454-254">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="33454-254">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="33454-255">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33454-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33454-256">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="33454-256">Provides high level status information.</span></span> <span data-ttu-id="33454-257">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="33454-257">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="33454-258">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="33454-258">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="33454-259">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="33454-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="33454-260"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="33454-260"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="33454-261"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="33454-261"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="33454-262"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="33454-262"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="33454-263"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="33454-263"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="33454-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="33454-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="33454-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="33454-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="33454-266">)</span><span class="sxs-lookup"><span data-stu-id="33454-266">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33454-267">**Primordial**</span><span class="sxs-lookup"><span data-stu-id="33454-267">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33454-268">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="33454-268">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33454-269">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33454-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33454-270">**True** se esse pool de recursos for a base da qual os recursos são desenhados e retornados na atividade do gerenciamento de recursos; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="33454-270">**True** if this resource pool is the base from which resources are drawn and returned in the activity of resource management; otherwise, **False**.</span></span> <span data-ttu-id="33454-271">Ser primordial significa que esse pool de recursos não pode ser criado ou excluído por consumidores desse modelo.</span><span class="sxs-lookup"><span data-stu-id="33454-271">Being primordial means that this resource pool cannot be created or deleted by consumers of this model.</span></span> <span data-ttu-id="33454-272">No entanto, outras ações, modeladas ou não, podem afetar as características ou o tamanho dos pools de recursos primordial.</span><span class="sxs-lookup"><span data-stu-id="33454-272">However, other actions, modeled or not, may affect the characteristics or size of primordial resource pools.</span></span> <span data-ttu-id="33454-273">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="33454-273">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="33454-274">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="33454-274">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33454-275">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="33454-275">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="33454-276">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33454-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33454-277">As reservas atuais (em unidades de **AllocationUnits**) se espalham por todas as alocações ativas deste pool.</span><span class="sxs-lookup"><span data-stu-id="33454-277">The current reservations (in units of **AllocationUnits**) spread across all active allocations from this pool.</span></span> <span data-ttu-id="33454-278">Em uma configuração hierárquica, isso representa a soma de todas as reservas atuais do pool de recursos descendentes.</span><span class="sxs-lookup"><span data-stu-id="33454-278">In a hierarchical configuration, this represents the sum of all descendant resource pool current reservations.</span></span> <span data-ttu-id="33454-279">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="33454-279">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="33454-280">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="33454-280">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33454-281">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="33454-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33454-282">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33454-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33454-283">Uma cadeia de caracteres que descreve um subtipo específico de implementação para esse pool.</span><span class="sxs-lookup"><span data-stu-id="33454-283">A string that describes an implementation specific sub-type for this pool.</span></span> <span data-ttu-id="33454-284">Por exemplo, isso pode ser usado para distinguir modelos diferentes do mesmo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="33454-284">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="33454-285">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="33454-285">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="33454-286">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="33454-286">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33454-287">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="33454-287">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="33454-288">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33454-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33454-289">O tipo de recurso que esse pool de recursos pode alocar.</span><span class="sxs-lookup"><span data-stu-id="33454-289">The type of resource this resource pool may allocate.</span></span> <span data-ttu-id="33454-290">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))e é definida como 4 ("memória").</span><span class="sxs-lookup"><span data-stu-id="33454-290">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to 4 ("Memory").</span></span>

</dd> <dt>

<span data-ttu-id="33454-291">**Status**</span><span class="sxs-lookup"><span data-stu-id="33454-291">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33454-292">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="33454-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33454-293">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33454-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33454-294">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="33454-294">The current status of the object.</span></span> <span data-ttu-id="33454-295">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="33454-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="33454-296">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="33454-296">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33454-297">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="33454-297">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="33454-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33454-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33454-299">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="33454-299">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="33454-300">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="33454-300">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33454-301">Comentários</span><span class="sxs-lookup"><span data-stu-id="33454-301">Remarks</span></span>

<span data-ttu-id="33454-302">O acesso à classe **Msvm \_ ProcessorPool** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="33454-302">Access to the **Msvm\_ProcessorPool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="33454-303">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="33454-303">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="33454-304">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33454-304">Requirements</span></span>



| <span data-ttu-id="33454-305">Requisito</span><span class="sxs-lookup"><span data-stu-id="33454-305">Requirement</span></span> | <span data-ttu-id="33454-306">Valor</span><span class="sxs-lookup"><span data-stu-id="33454-306">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33454-307">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33454-307">Minimum supported client</span></span><br/> | <span data-ttu-id="33454-308">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="33454-308">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="33454-309">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33454-309">Minimum supported server</span></span><br/> | <span data-ttu-id="33454-310">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="33454-310">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="33454-311">Namespace</span><span class="sxs-lookup"><span data-stu-id="33454-311">Namespace</span></span><br/>                | <span data-ttu-id="33454-312">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="33454-312">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="33454-313">MOF</span><span class="sxs-lookup"><span data-stu-id="33454-313">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33454-314"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33454-314"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="33454-315">DLL</span><span class="sxs-lookup"><span data-stu-id="33454-315">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33454-316"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="33454-316"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="33454-317">Confira também</span><span class="sxs-lookup"><span data-stu-id="33454-317">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33454-318">**\_RESOURCEPOOL CIM**</span><span class="sxs-lookup"><span data-stu-id="33454-318">**CIM\_ResourcePool**</span></span>](cim-resourcepool.md)
</dt> <dt>

<span data-ttu-id="33454-319">[**\_RESOURCEPOOL CIM**](/previous-versions//cc136903(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="33454-319">[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="33454-320">Classes de processador</span><span class="sxs-lookup"><span data-stu-id="33454-320">Processor Classes</span></span>](processor-classes.md)
</dt> </dl>

 

