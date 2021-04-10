---
description: Representa um pool de recursos, que é uma entidade lógica fornecida pelo sistema host para alocar e atribuir recursos.
ms.assetid: c8e0b701-1814-4409-a073-017f8fea841a
title: Classe CIM_ResourcePool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePool
- CIM_ResourcePool.InstanceID
- CIM_ResourcePool.PoolID
- CIM_ResourcePool.Primordial
- CIM_ResourcePool.Capacity
- CIM_ResourcePool.Reserved
- CIM_ResourcePool.ResourceType
- CIM_ResourcePool.OtherResourceType
- CIM_ResourcePool.ResourceSubType
- CIM_ResourcePool.AllocationUnits
- CIM_ResourcePool.ConsumedResourceUnits
- CIM_ResourcePool.CurrentlyConsumedResource
- CIM_ResourcePool.MaxConsumableResource
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 11a073f817da27dbbd45be26a008486a776470cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090643"
---
# <a name="cim_resourcepool-class"></a><span data-ttu-id="a11c6-103">\_Classe CIM ResourcePool</span><span class="sxs-lookup"><span data-stu-id="a11c6-103">CIM\_ResourcePool class</span></span>

<span data-ttu-id="a11c6-104">Representa um pool de recursos, que é uma entidade lógica fornecida pelo sistema host para alocar e atribuir recursos.</span><span class="sxs-lookup"><span data-stu-id="a11c6-104">Represents a resource pool, which is a logical entity provided by the host system to allocate and assign resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="a11c6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a11c6-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ResourcePool : CIM_LogicalElement
{
  string  InstanceID;
  string  PoolID;
  boolean Primordial = FALSE;
  uint64  Capacity;
  uint64  Reserved;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  AllocationUnits;
  string  ConsumedResourceUnits = "count";
  uint64  CurrentlyConsumedResource;
  uint64  MaxConsumableResource;
};
```

## <a name="members"></a><span data-ttu-id="a11c6-106">Membros</span><span class="sxs-lookup"><span data-stu-id="a11c6-106">Members</span></span>

<span data-ttu-id="a11c6-107">A classe **CIM \_ ResourcePool** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a11c6-107">The **CIM\_ResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="a11c6-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a11c6-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a11c6-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a11c6-109">Properties</span></span>

<span data-ttu-id="a11c6-110">A classe **CIM \_ ResourcePool** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a11c6-110">The **CIM\_ResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a11c6-111">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="a11c6-111">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a11c6-112">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a11c6-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a11c6-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a11c6-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a11c6-114">Qualificadores: **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="a11c6-114">Qualifiers: **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="a11c6-115">As unidades de alocação usadas pelas propriedades **Reservation** e **Limit** .</span><span class="sxs-lookup"><span data-stu-id="a11c6-115">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="a11c6-116">Por exemplo, quando **ResourceType** é definido como "Processor", **AllocationUnits** pode ser definido como "Hertz \* 10 ^ 6" ou "percent".</span><span class="sxs-lookup"><span data-stu-id="a11c6-116">For example, when **ResourceType** is set to "Processor", **AllocationUnits** may be set to "hertz\*10^6" or "percent".</span></span> <span data-ttu-id="a11c6-117">O valor dessa propriedade deve ser um valor válido do qualificador de unidades programáticas do Apêndice C. 1 de *DSP0004 v 2.4* ou posterior.</span><span class="sxs-lookup"><span data-stu-id="a11c6-117">The value of this property should be a legal value of the Programmatic Units qualifier from Appendix C.1 of *DSP0004 V2.4* or later.</span></span>

</dd> <dt>

<span data-ttu-id="a11c6-118">**Capacidade**</span><span class="sxs-lookup"><span data-stu-id="a11c6-118">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a11c6-119">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a11c6-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a11c6-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a11c6-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a11c6-121">A quantidade máxima de reservas às quais o pool de recursos pode dar suporte.</span><span class="sxs-lookup"><span data-stu-id="a11c6-121">The maximum amount of reservations that the resource pool can support.</span></span> <span data-ttu-id="a11c6-122">A propriedade **AllocationUnits** especifica o tipo de unidade.</span><span class="sxs-lookup"><span data-stu-id="a11c6-122">The **AllocationUnits** property specifies the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="a11c6-123">**ConsumedResourceUnits**</span><span class="sxs-lookup"><span data-stu-id="a11c6-123">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a11c6-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a11c6-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a11c6-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a11c6-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a11c6-126">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**MaxConsumableResource**","**CIM \_ ResourcePool**.**CurrentlyConsumedResource**"), **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="a11c6-126">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**MaxConsumableResource**", "**CIM\_ResourcePool**.**CurrentlyConsumedResource**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="a11c6-127">As unidades para as propriedades **MaxConsumable** e **consumidas** .</span><span class="sxs-lookup"><span data-stu-id="a11c6-127">The units for the **MaxConsumable** and the **Consumed** properties.</span></span>

</dd> <dt>

<span data-ttu-id="a11c6-128">**CurrentlyConsumedResource**</span><span class="sxs-lookup"><span data-stu-id="a11c6-128">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a11c6-129">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a11c6-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a11c6-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a11c6-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a11c6-131">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**ConsumedResourceUnits**")</span><span class="sxs-lookup"><span data-stu-id="a11c6-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ConsumedResourceUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="a11c6-132">A quantidade de recursos que o pool de recursos apresenta atualmente aos consumidores de recursos.</span><span class="sxs-lookup"><span data-stu-id="a11c6-132">The amount of resource that the resource pool currently presents to resource consumers.</span></span> <span data-ttu-id="a11c6-133">Essa propriedade é diferente da propriedade **reservada** porque descreve a exibição de consumidores do recurso, enquanto a propriedade **reservada** descreve a exibição de produtores do recurso.</span><span class="sxs-lookup"><span data-stu-id="a11c6-133">This property is different from the **Reserved** property because it describes the consumers view of the resource while the **Reserved** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="a11c6-134">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a11c6-134">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a11c6-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a11c6-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a11c6-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a11c6-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a11c6-137">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="a11c6-137">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="a11c6-138">Identifica exclusivamente uma instância dessa classe dentro do escopo do namespace que a contém.</span><span class="sxs-lookup"><span data-stu-id="a11c6-138">Uniquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="a11c6-139">Para garantir a exclusividade no namespace, o valor da propriedade **InstanceId** deve ser construído no seguinte padrão: *OrgID*:*LocalId*</span><span class="sxs-lookup"><span data-stu-id="a11c6-139">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> -   <span data-ttu-id="a11c6-140">*OrgID* deve incluir um nome de direitos autorais, com marca registrada ou exclusivo que pertença à entidade de negócios que define a propriedade **InstanceId** ou ser uma ID registrada que é atribuída por uma autoridade global reconhecida.</span><span class="sxs-lookup"><span data-stu-id="a11c6-140">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID** property, or be a registered ID that is assigned by a recognized global authority.</span></span>
> -   <span data-ttu-id="a11c6-141">*OrgID* não deve conter dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="a11c6-141">*OrgID* must not contain a colon.</span></span> <span data-ttu-id="a11c6-142">Os primeiros dois-pontos em **InstanceId** devem estar entre *OrgID* e *LocalId*.</span><span class="sxs-lookup"><span data-stu-id="a11c6-142">The first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span>
> -   <span data-ttu-id="a11c6-143">A *LocalId* é escolhida pela entidade de negócios e não deve ser reutilizada para identificar elementos do mundo real subjacentes diferentes.</span><span class="sxs-lookup"><span data-stu-id="a11c6-143">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
> -   <span data-ttu-id="a11c6-144">Se o padrão acima não for usado, a entidade de definição deverá garantir que o valor de **InstanceId** resultante não seja reutilizado em todas as propriedades **InstanceId** produzidas por este provedor ou por outros provedores para esse namespace.</span><span class="sxs-lookup"><span data-stu-id="a11c6-144">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
> -   <span data-ttu-id="a11c6-145">Para instâncias definidas por DMTF, o padrão deve ser usado com o *OrgID* definido como "CIM".</span><span class="sxs-lookup"><span data-stu-id="a11c6-145">For DMTF defined instances, the pattern must be used with the *OrgID* set to "CIM".</span></span>

 

</dd> <dt>

<span data-ttu-id="a11c6-146">**MaxConsumableResource**</span><span class="sxs-lookup"><span data-stu-id="a11c6-146">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a11c6-147">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a11c6-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a11c6-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a11c6-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a11c6-149">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**ConsumedResourceUnits**")</span><span class="sxs-lookup"><span data-stu-id="a11c6-149">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ConsumedResourceUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="a11c6-150">O máximo da quantidade de recursos consumíveis que o pool de recursos pode apresentar aos consumidores de recursos.</span><span class="sxs-lookup"><span data-stu-id="a11c6-150">The maximum of amount of consumable resources that the resource pool can present to resource consumers.</span></span> <span data-ttu-id="a11c6-151">Essa propriedade é diferente da propriedade **Capacity** porque descreve a exibição de consumidores do recurso, enquanto a propriedade **Capacity** descreve a exibição de produtores do recurso.</span><span class="sxs-lookup"><span data-stu-id="a11c6-151">This property is different from the **Capacity** property because it describes the consumers view of the resource while the **Capacity** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="a11c6-152">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="a11c6-152">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a11c6-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a11c6-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a11c6-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a11c6-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a11c6-155">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="a11c6-155">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="a11c6-156">O tipo de recurso quando a propriedade **ResourceType** é definida como "0" (outra).</span><span class="sxs-lookup"><span data-stu-id="a11c6-156">The resource type when the **ResourceType** property is set to "0" (other).</span></span>

</dd> <dt>

<span data-ttu-id="a11c6-157">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="a11c6-157">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a11c6-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a11c6-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a11c6-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a11c6-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a11c6-160">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**Poolid**")</span><span class="sxs-lookup"><span data-stu-id="a11c6-160">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**PoolId**")</span></span>
</dt> </dl>

<span data-ttu-id="a11c6-161">Um identificador opaco para o pool.</span><span class="sxs-lookup"><span data-stu-id="a11c6-161">An opaque identifier for the pool.</span></span> <span data-ttu-id="a11c6-162">Essa propriedade é usada para fornecer correlação ao salvar e restaurar dados de configuração para o armazenamento persistente subjacente.</span><span class="sxs-lookup"><span data-stu-id="a11c6-162">This property is used to provide correlation when saving and restoring configuration data to underlying persistent storage.</span></span>

</dd> <dt>

<span data-ttu-id="a11c6-163">**Primordial**</span><span class="sxs-lookup"><span data-stu-id="a11c6-163">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a11c6-164">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a11c6-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a11c6-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a11c6-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a11c6-166">**true** se o pool de recursos for primordial.</span><span class="sxs-lookup"><span data-stu-id="a11c6-166">**true** if the resource pool is primordial.</span></span> <span data-ttu-id="a11c6-167">**false** se o pool de recursos for um pool de recursos concreto.</span><span class="sxs-lookup"><span data-stu-id="a11c6-167">**false** if the resource pool is a concrete resource pool.</span></span> <span data-ttu-id="a11c6-168">Um pool de recursos primordial é um pool de recursos que não é criado ou excluído por consumidores do recurso.</span><span class="sxs-lookup"><span data-stu-id="a11c6-168">A primordial resource pool is a resource pool that is not created or deleted by consumers of the resource.</span></span> <span data-ttu-id="a11c6-169">Um pool de recursos concreto pode ser atualizado pelos serviços de alocação de recursos.</span><span class="sxs-lookup"><span data-stu-id="a11c6-169">A concrete resource pool can be updated by resource allocation services.</span></span>

</dd> <dt>

<span data-ttu-id="a11c6-170">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="a11c6-170">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a11c6-171">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a11c6-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a11c6-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a11c6-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a11c6-173">O número atual de reservas espalhadas por todas as alocações ativas deste pool.</span><span class="sxs-lookup"><span data-stu-id="a11c6-173">The current number of reservations spread across all active allocations from this pool.</span></span> <span data-ttu-id="a11c6-174">Em uma configuração hierárquica, isso representa a soma de todas as reservas de descendentes atuais.</span><span class="sxs-lookup"><span data-stu-id="a11c6-174">In a hierarchical configuration, this represents the sum of all current descendant reservations.</span></span> <span data-ttu-id="a11c6-175">A propriedade **AllocationUnits** especifica o tipo de unidade.</span><span class="sxs-lookup"><span data-stu-id="a11c6-175">The **AllocationUnits** property specifies the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="a11c6-176">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="a11c6-176">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a11c6-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a11c6-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a11c6-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a11c6-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a11c6-179">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="a11c6-179">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="a11c6-180">O subtipo específico da implementação para o pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="a11c6-180">The implementation specific sub-type for the resource pool.</span></span> <span data-ttu-id="a11c6-181">Por exemplo, isso pode ser usado para distinguir modelos diferentes do mesmo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="a11c6-181">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="a11c6-182">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="a11c6-182">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a11c6-183">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a11c6-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a11c6-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a11c6-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a11c6-185">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**OtherResourceType**","**CIM \_ ResourcePool**.**ResourceSubType**")</span><span class="sxs-lookup"><span data-stu-id="a11c6-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**OtherResourceType**", "**CIM\_ResourcePool**.**ResourceSubType**")</span></span>
</dt> </dl>

<span data-ttu-id="a11c6-186">O tipo de recurso alocado pelo pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="a11c6-186">The type of resource allocated by the resource pool.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a11c6-187">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="a11c6-187">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="a11c6-188">**Sistema de computador** (2)</span><span class="sxs-lookup"><span data-stu-id="a11c6-188">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="a11c6-189">**Processador** (3)</span><span class="sxs-lookup"><span data-stu-id="a11c6-189">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="a11c6-190">**Memória** (4)</span><span class="sxs-lookup"><span data-stu-id="a11c6-190">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="a11c6-191">**Controlador IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="a11c6-191">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="a11c6-192">**HBA SCSI paralelo** (6)</span><span class="sxs-lookup"><span data-stu-id="a11c6-192">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="a11c6-193">**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="a11c6-193">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="a11c6-194">**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="a11c6-194">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="a11c6-195">**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="a11c6-195">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="a11c6-196">**Adaptador Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="a11c6-196">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="a11c6-197">**Outro adaptador de rede** (11)</span><span class="sxs-lookup"><span data-stu-id="a11c6-197">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="a11c6-198">**Slot de e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="a11c6-198">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="a11c6-199">**Dispositivo de e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="a11c6-199">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="a11c6-200">**Unidade de disquete** (14)</span><span class="sxs-lookup"><span data-stu-id="a11c6-200">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="a11c6-201">**Unidade de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="a11c6-201">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="a11c6-202">**Unidade de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="a11c6-202">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="a11c6-203">**Unidade de disco** (17)</span><span class="sxs-lookup"><span data-stu-id="a11c6-203">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="a11c6-204">**Unidade de fita** (18)</span><span class="sxs-lookup"><span data-stu-id="a11c6-204">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="a11c6-205">**Extensão de armazenamento** (19)</span><span class="sxs-lookup"><span data-stu-id="a11c6-205">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="a11c6-206">**Outro dispositivo de armazenamento** (20)</span><span class="sxs-lookup"><span data-stu-id="a11c6-206">**Other storage device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="a11c6-207">**Porta serial** (21)</span><span class="sxs-lookup"><span data-stu-id="a11c6-207">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="a11c6-208">**Porta paralela** (22)</span><span class="sxs-lookup"><span data-stu-id="a11c6-208">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="a11c6-209">**Controlador USB** (23)</span><span class="sxs-lookup"><span data-stu-id="a11c6-209">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="a11c6-210">**Controlador de gráficos** (24)</span><span class="sxs-lookup"><span data-stu-id="a11c6-210">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="a11c6-211">**Controlador IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="a11c6-211">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="a11c6-212">**Unidade particionável** (26)</span><span class="sxs-lookup"><span data-stu-id="a11c6-212">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="a11c6-213">**Unidade particionável de base** (27)</span><span class="sxs-lookup"><span data-stu-id="a11c6-213">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="a11c6-214">**Energia** (28)</span><span class="sxs-lookup"><span data-stu-id="a11c6-214">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="a11c6-215">**Capacidade de resfriamento** (29)</span><span class="sxs-lookup"><span data-stu-id="a11c6-215">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="a11c6-216">**Porta do comutador Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="a11c6-216">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="a11c6-217">**Disco lógico** (31)</span><span class="sxs-lookup"><span data-stu-id="a11c6-217">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="a11c6-218">**Volume de armazenamento** (32)</span><span class="sxs-lookup"><span data-stu-id="a11c6-218">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="a11c6-219">**Conexão Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="a11c6-219">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="a11c6-220">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a11c6-220">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="a11c6-221">**Fornecedor reservado** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="a11c6-221">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


<span data-ttu-id="a11c6-222"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a11c6-222"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="a11c6-223">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a11c6-223">Requirements</span></span>



| <span data-ttu-id="a11c6-224">Requisito</span><span class="sxs-lookup"><span data-stu-id="a11c6-224">Requirement</span></span> | <span data-ttu-id="a11c6-225">Valor</span><span class="sxs-lookup"><span data-stu-id="a11c6-225">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a11c6-226">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a11c6-226">Minimum supported client</span></span><br/> | <span data-ttu-id="a11c6-227">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a11c6-227">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="a11c6-228">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a11c6-228">Minimum supported server</span></span><br/> | <span data-ttu-id="a11c6-229">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a11c6-229">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="a11c6-230">Namespace</span><span class="sxs-lookup"><span data-stu-id="a11c6-230">Namespace</span></span><br/>                | <span data-ttu-id="a11c6-231">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="a11c6-231">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a11c6-232">MOF</span><span class="sxs-lookup"><span data-stu-id="a11c6-232">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a11c6-233"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a11c6-233"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a11c6-234">DLL</span><span class="sxs-lookup"><span data-stu-id="a11c6-234">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a11c6-235"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a11c6-235"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a11c6-236">Confira também</span><span class="sxs-lookup"><span data-stu-id="a11c6-236">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a11c6-237">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="a11c6-237">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

