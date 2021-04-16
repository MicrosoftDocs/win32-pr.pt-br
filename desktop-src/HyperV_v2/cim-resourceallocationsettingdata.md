---
description: Representa as configurações de um recurso alocado que estão fora do escopo da classe CIM normalmente usado para representar o próprio recurso.
ms.assetid: 6261bab9-aa51-479e-bd6a-43c4a9b294a6
title: Classe CIM_ResourceAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourceAllocationSettingData
- CIM_ResourceAllocationSettingData.ResourceType
- CIM_ResourceAllocationSettingData.OtherResourceType
- CIM_ResourceAllocationSettingData.ResourceSubType
- CIM_ResourceAllocationSettingData.PoolID
- CIM_ResourceAllocationSettingData.ConsumerVisibility
- CIM_ResourceAllocationSettingData.HostResource
- CIM_ResourceAllocationSettingData.AllocationUnits
- CIM_ResourceAllocationSettingData.VirtualQuantity
- CIM_ResourceAllocationSettingData.Reservation
- CIM_ResourceAllocationSettingData.Limit
- CIM_ResourceAllocationSettingData.Weight
- CIM_ResourceAllocationSettingData.AutomaticAllocation
- CIM_ResourceAllocationSettingData.AutomaticDeallocation
- CIM_ResourceAllocationSettingData.Parent
- CIM_ResourceAllocationSettingData.Connection
- CIM_ResourceAllocationSettingData.Address
- CIM_ResourceAllocationSettingData.MappingBehavior
- CIM_ResourceAllocationSettingData.AddressOnParent
- CIM_ResourceAllocationSettingData.VirtualQuantityUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 22289511f454e0d3b128d0e73d32687924c7a7ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757821"
---
# <a name="cim_resourceallocationsettingdata-class"></a><span data-ttu-id="3e8e8-103">\_Classe CIM ResourceAllocationSettingData</span><span class="sxs-lookup"><span data-stu-id="3e8e8-103">CIM\_ResourceAllocationSettingData class</span></span>

<span data-ttu-id="3e8e8-104">Representa as configurações de um recurso alocado que estão fora do escopo da classe CIM normalmente usado para representar o próprio recurso.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-104">Represents settings for an allocated resource that are outside the scope of the CIM class typically used to represent the resource itself.</span></span> <span data-ttu-id="3e8e8-105">Essas configurações incluem informações específicas para a alocação que podem não estar visíveis para o consumidor do recurso.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-105">These settings include information specific to the allocation that may not be visible to the consumer of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e8e8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e8e8-106">Syntax</span></span>

``` syntax
[Abstract, Version("2.24.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ResourceAllocationSettingData : CIM_SettingData
{
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
};
```

## <a name="members"></a><span data-ttu-id="3e8e8-107">Membros</span><span class="sxs-lookup"><span data-stu-id="3e8e8-107">Members</span></span>

<span data-ttu-id="3e8e8-108">A classe **CIM \_ ResourceAllocationSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3e8e8-108">The **CIM\_ResourceAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="3e8e8-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3e8e8-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3e8e8-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3e8e8-110">Properties</span></span>

<span data-ttu-id="3e8e8-111">A classe **CIM \_ ResourceAllocationSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-111">The **CIM\_ResourceAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3e8e8-112">**Endereço**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e8e8-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e8e8-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e8e8-115">O endereço do recurso, por exemplo, o endereço MAC de uma porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-115">The address of the resource, for example, the MAC address of a Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="3e8e8-116">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-116">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e8e8-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e8e8-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e8e8-119">O endereço deste recurso do contexto do pai.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-119">The address of this resource from the context of the parent.</span></span> <span data-ttu-id="3e8e8-120">Essa propriedade é usada para descrever uma relação de controlador e a ordem dos dispositivos em um controlador.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-120">This property is used to describe a controller relationship and the ordering of devices on a controller.</span></span> <span data-ttu-id="3e8e8-121">Por exemplo, se o pai for um controlador PCI, essa propriedade especificaria o slot PCI desse dispositivo filho.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-121">For example, if the parent is a PCI Controller, this property would specify the PCI slot of this child device.</span></span>

</dd> <dt>

<span data-ttu-id="3e8e8-122">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-122">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e8e8-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e8e8-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-125">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**Reservation**","**CIM \_ ResourceAllocationSettingData**.**Limit**"), **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-125">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**Reservation**", "**CIM\_ResourceAllocationSettingData**.**Limit**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="3e8e8-126">As unidades de alocação usadas pelas propriedades **Reservation** e **Limit** .</span><span class="sxs-lookup"><span data-stu-id="3e8e8-126">The allocation units used by the **Reservation** and **Limit** properties.</span></span>

</dd> <dt>

<span data-ttu-id="3e8e8-127">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-127">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e8e8-128">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e8e8-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e8e8-130">**true** para alocar o recurso automaticamente; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-130">**true** to automatically allocate the resource; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="3e8e8-131">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-131">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e8e8-132">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e8e8-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e8e8-134">**true** para desalocar automaticamente o recurso; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-134">**true** to automatically deallocate the resource; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="3e8e8-135">**Conexão**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-135">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e8e8-136">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-136">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e8e8-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e8e8-138">Uma matriz que indica os objetos conectados ao recurso, como uma rede nomeada ou uma porta de comutador.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-138">An array that indicates the objects connected to the resource, such as a named network or switch port.</span></span>

</dd> <dt>

<span data-ttu-id="3e8e8-139">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-139">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e8e8-140">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e8e8-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e8e8-142">A visibilidade dos consumidores para o recurso alocado.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-142">The consumers visibility to the allocated resource.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3e8e8-143">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-143">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>

<span data-ttu-id="3e8e8-144">**Aprovado** (2)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-144">**Passed-Through** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>

<span data-ttu-id="3e8e8-145">**Virtualizado** (3)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-145">**Virtualized** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span>

<span data-ttu-id="3e8e8-146">**Não representado** (4)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-146">**Not represented** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3e8e8-147">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-147">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="3e8e8-148">**Fornecedor reservado** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-148">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3e8e8-149">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-149">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e8e8-150">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-150">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e8e8-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-152">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**ConsumerVisibility**","**CIM \_ ResourceAllocationSettingData**.**MappingBehavior**")</span><span class="sxs-lookup"><span data-stu-id="3e8e8-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**ConsumerVisibility**", "**CIM\_ResourceAllocationSettingData**.**MappingBehavior**")</span></span>
</dt> </dl>

<span data-ttu-id="3e8e8-153">Uma matriz que contém a atribuição dos recursos alocados.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-153">An array that contains the assignment of the allocated resources.</span></span> <span data-ttu-id="3e8e8-154">Cada valor não nulo dessa propriedade deve ser formatado como um URI baseado em RFC3986.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-154">Each non-null value of this property must be formated as an RFC3986 based URI.</span></span> <span data-ttu-id="3e8e8-155">Se o recurso for modelado, o valor deverá ser um URI WBEM.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-155">If the resource is modeled, then the value should be a WBEM URI.</span></span>

</dd> <dt>

<span data-ttu-id="3e8e8-156">**Limite**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-156">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e8e8-157">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e8e8-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-159">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**AllocationUnits**")</span><span class="sxs-lookup"><span data-stu-id="3e8e8-159">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**AllocationUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="3e8e8-160">A quantidade máxima de recursos a serem concedidos à alocação.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-160">The maximum amount of resource to grant to the allocation.</span></span> <span data-ttu-id="3e8e8-161">O tipo de unidade dessa propriedade é especificado pela propriedade **AllocationUnits** .</span><span class="sxs-lookup"><span data-stu-id="3e8e8-161">The unit type of this property is specified by the **AllocationUnits** property.</span></span>

</dd> <dt>

<span data-ttu-id="3e8e8-162">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-162">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e8e8-163">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e8e8-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e8e8-165">Indica como o recurso é mapeado para recursos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-165">Indicates how the resource maps to underlying resources.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3e8e8-166">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-166">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="3e8e8-167">**Sem suporte** (2)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-167">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="3e8e8-168">**Dedicado** (3)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-168">**Dedicated** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>

<span data-ttu-id="3e8e8-169">**Afinidade flexível** (4)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-169">**Soft Affinity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>

<span data-ttu-id="3e8e8-170">**Afinidade rígida** (5)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-170">**Hard Affinity** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3e8e8-171">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-171">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="3e8e8-172">**Fornecedor reservado** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-172">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3e8e8-173">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-173">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e8e8-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e8e8-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-176">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="3e8e8-176">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="3e8e8-177">Uma descrição do tipo de recurso quando a propriedade **ResourceType** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="3e8e8-177">A description of the resource type when the **ResourceType** property is set to 1 (other).</span></span>

</dd> <dt>

<span data-ttu-id="3e8e8-178">**Pai**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-178">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e8e8-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e8e8-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e8e8-181">O pai do recurso, por exemplo, um controlador para a alocação atual.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-181">The parent of the resource, for example, a controller for the current allocation.</span></span>

</dd> <dt>

<span data-ttu-id="3e8e8-182">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-182">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e8e8-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e8e8-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-185">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**Poolid**")</span><span class="sxs-lookup"><span data-stu-id="3e8e8-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**PoolId**")</span></span>
</dt> </dl>

<span data-ttu-id="3e8e8-186">A ID do pool de recursos que gerou o recurso.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-186">The ID of the resource pool that generated the resource.</span></span>

</dd> <dt>

<span data-ttu-id="3e8e8-187">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-187">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e8e8-188">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e8e8-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-190">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**AllocationUnits**")</span><span class="sxs-lookup"><span data-stu-id="3e8e8-190">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**AllocationUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="3e8e8-191">O número de recursos que têm garantia de disponibilidade para essa alocação.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-191">The number of resource that are guaranteed to be available for this allocation.</span></span> <span data-ttu-id="3e8e8-192">Em sistemas que dão suporte ao comprometimento excessivo de recursos, esse valor é normalmente usado para o controle de admissão.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-192">On systems that support over-commitment of resources, this value is typically used for admission control.</span></span>

<span data-ttu-id="3e8e8-193">O tipo de unidade dessa propriedade é especificado pela propriedade **AllocationUnits** .</span><span class="sxs-lookup"><span data-stu-id="3e8e8-193">The unit type of this property is specified by the **AllocationUnits** property.</span></span>

</dd> <dt>

<span data-ttu-id="3e8e8-194">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-194">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e8e8-195">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e8e8-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-197">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="3e8e8-197">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="3e8e8-198">Um subtipo específico de implementação para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-198">An implementation specific sub-type for this resource.</span></span> <span data-ttu-id="3e8e8-199">Por exemplo, isso pode ser usado para distinguir modelos diferentes do mesmo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-199">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="3e8e8-200">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-200">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e8e8-201">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e8e8-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-203">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**OtherResourceType**","**CIM \_ ResourceAllocationSettingData**.**ResourceSubType**")</span><span class="sxs-lookup"><span data-stu-id="3e8e8-203">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**OtherResourceType**", "**CIM\_ResourceAllocationSettingData**.**ResourceSubType**")</span></span>
</dt> </dl>

<span data-ttu-id="3e8e8-204">O tipo de recurso que é representado pelas configurações de alocação.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-204">The type of resource that is represented by the allocation settings.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3e8e8-205">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-205">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="3e8e8-206">**Sistema de computador** (2)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-206">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="3e8e8-207">**Processador** (3)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-207">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="3e8e8-208">**Memória** (4)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-208">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="3e8e8-209">**Controlador IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-209">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="3e8e8-210">**HBA SCSI paralelo** (6)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-210">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="3e8e8-211">**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-211">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="3e8e8-212">**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-212">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="3e8e8-213">**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-213">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="3e8e8-214">**Adaptador Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-214">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="3e8e8-215">**Outro adaptador de rede** (11)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-215">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="3e8e8-216">**Slot de e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-216">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="3e8e8-217">**Dispositivo de e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-217">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="3e8e8-218">**Unidade de disquete** (14)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-218">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="3e8e8-219">**Unidade de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-219">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="3e8e8-220">**Unidade de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-220">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="3e8e8-221">**Unidade de disco** (17)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-221">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="3e8e8-222">**Unidade de fita** (18)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-222">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="3e8e8-223">**Extensão de armazenamento** (19)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-223">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="3e8e8-224">**Outro dispositivo de armazenamento** (20)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-224">**Other storage device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="3e8e8-225">**Porta serial** (21)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-225">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="3e8e8-226">**Porta paralela** (22)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-226">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="3e8e8-227">**Controlador USB** (23)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-227">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="3e8e8-228">**Controlador de gráficos** (24)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-228">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="3e8e8-229">**Controlador IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-229">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="3e8e8-230">**Unidade particionável** (26)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-230">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="3e8e8-231">**Unidade particionável de base** (27)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-231">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="3e8e8-232">**Energia** (28)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-232">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="3e8e8-233">**Capacidade de resfriamento** (29)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-233">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="3e8e8-234">**Porta do comutador Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-234">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="3e8e8-235">**Disco lógico** (31)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-235">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="3e8e8-236">**Volume de armazenamento** (32)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-236">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="3e8e8-237">**Conexão Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-237">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3e8e8-238">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3e8e8-238">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="3e8e8-239">**Fornecedor reservado** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="3e8e8-239">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3e8e8-240">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-240">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e8e8-241">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-241">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-242">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e8e8-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-243">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**VirtualQuantityUnits**")</span><span class="sxs-lookup"><span data-stu-id="3e8e8-243">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**VirtualQuantityUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="3e8e8-244">O número de recursos apresentados ao consumidor do recurso.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-244">The number of resources presented to the consumer of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="3e8e8-245">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-245">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e8e8-246">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-247">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e8e8-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-248">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-248">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="3e8e8-249">As unidades usadas pela propriedade **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="3e8e8-249">The units used by the **VirtualQuantity** property.</span></span>

</dd> <dt>

<span data-ttu-id="3e8e8-250">**Weight**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-250">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e8e8-251">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-251">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e8e8-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e8e8-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e8e8-253">A prioridade relativa para essa alocação em relação a outras alocações do mesmo pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="3e8e8-253">The relative priority for this allocation in relation to other allocations from the same resource pool.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e8e8-254">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e8e8-254">Requirements</span></span>



| <span data-ttu-id="3e8e8-255">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e8e8-255">Requirement</span></span> | <span data-ttu-id="3e8e8-256">Valor</span><span class="sxs-lookup"><span data-stu-id="3e8e8-256">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e8e8-257">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e8e8-257">Minimum supported client</span></span><br/> | <span data-ttu-id="3e8e8-258">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3e8e8-258">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="3e8e8-259">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e8e8-259">Minimum supported server</span></span><br/> | <span data-ttu-id="3e8e8-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3e8e8-260">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="3e8e8-261">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e8e8-261">Namespace</span></span><br/>                | <span data-ttu-id="3e8e8-262">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="3e8e8-262">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3e8e8-263">MOF</span><span class="sxs-lookup"><span data-stu-id="3e8e8-263">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e8e8-264"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e8e8-264"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e8e8-265">DLL</span><span class="sxs-lookup"><span data-stu-id="3e8e8-265">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e8e8-266"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3e8e8-266"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3e8e8-267">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e8e8-267">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e8e8-268">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="3e8e8-268">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

