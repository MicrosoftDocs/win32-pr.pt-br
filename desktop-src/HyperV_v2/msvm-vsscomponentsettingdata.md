---
description: Representa o estado configurado do serviço de Serviço de Cópias de Sombra de Volume (VSS).
ms.assetid: FAE8E8F7-525A-4E5A-91B3-B73343337352
title: Classe Msvm_VssComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssComponentSettingData
- Msvm_VssComponentSettingData.InstanceID
- Msvm_VssComponentSettingData.Caption
- Msvm_VssComponentSettingData.Description
- Msvm_VssComponentSettingData.ElementName
- Msvm_VssComponentSettingData.ResourceType
- Msvm_VssComponentSettingData.OtherResourceType
- Msvm_VssComponentSettingData.ResourceSubType
- Msvm_VssComponentSettingData.PoolID
- Msvm_VssComponentSettingData.ConsumerVisibility
- Msvm_VssComponentSettingData.HostResource
- Msvm_VssComponentSettingData.AllocationUnits
- Msvm_VssComponentSettingData.VirtualQuantity
- Msvm_VssComponentSettingData.Reservation
- Msvm_VssComponentSettingData.Limit
- Msvm_VssComponentSettingData.Weight
- Msvm_VssComponentSettingData.AutomaticAllocation
- Msvm_VssComponentSettingData.AutomaticDeallocation
- Msvm_VssComponentSettingData.Parent
- Msvm_VssComponentSettingData.Connection
- Msvm_VssComponentSettingData.Address
- Msvm_VssComponentSettingData.MappingBehavior
- Msvm_VssComponentSettingData.AddressOnParent
- Msvm_VssComponentSettingData.VirtualQuantityUnits
- Msvm_VssComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5d37f46c10cc702c66a30fb484553a8c5da03d8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768503"
---
# <a name="msvm_vsscomponentsettingdata-class"></a><span data-ttu-id="49015-103">\_Classe Msvm VssComponentSettingData</span><span class="sxs-lookup"><span data-stu-id="49015-103">Msvm\_VssComponentSettingData class</span></span>

<span data-ttu-id="49015-104">Representa o estado configurado do serviço de Serviço de Cópias de Sombra de Volume (VSS).</span><span class="sxs-lookup"><span data-stu-id="49015-104">Represents the configured state of the Volume Shadow Copy Service (VSS) service.</span></span>

<span data-ttu-id="49015-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="49015-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="49015-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49015-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "VSS";
  string  Description = "Microsoft VSS Service Setting Data";
  string  ElementName = "VSS";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:VSS Component";
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource;
  string  AllocationUnits = "count";
  uint64  VirtualQuantity = 1;
  uint64  Reservation = 1;
  uint64  Limit = 1;
  uint32  Weight = 0;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint16  EnabledState = 2;
};
```

## <a name="members"></a><span data-ttu-id="49015-107">Membros</span><span class="sxs-lookup"><span data-stu-id="49015-107">Members</span></span>

<span data-ttu-id="49015-108">A classe **Msvm \_ VssComponentSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="49015-108">The **Msvm\_VssComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="49015-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="49015-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="49015-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="49015-110">Properties</span></span>

<span data-ttu-id="49015-111">A classe **Msvm \_ VssComponentSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="49015-111">The **Msvm\_VssComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="49015-112">**Endereço**</span><span class="sxs-lookup"><span data-stu-id="49015-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49015-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="49015-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49015-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="49015-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49015-115">O endereço do recurso.</span><span class="sxs-lookup"><span data-stu-id="49015-115">The address of the resource.</span></span> <span data-ttu-id="49015-116">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="49015-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="49015-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="49015-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49015-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="49015-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49015-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="49015-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49015-120">Descreve o endereço deste recurso no contexto do pai.</span><span class="sxs-lookup"><span data-stu-id="49015-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="49015-121">As propriedades **pai** e **AddressOnParent** são usadas para descrever a relação do controlador, bem como a ordem dos dispositivos em um controlador.</span><span class="sxs-lookup"><span data-stu-id="49015-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="49015-122">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="49015-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="49015-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="49015-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49015-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="49015-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49015-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="49015-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49015-126">As unidades de alocação usadas pelas propriedades **Reservation** e **Limit** .</span><span class="sxs-lookup"><span data-stu-id="49015-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="49015-127">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="49015-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="49015-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="49015-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49015-129">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="49015-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="49015-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="49015-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49015-131">Indica se o recurso será alocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="49015-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="49015-132">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="49015-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="49015-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="49015-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49015-134">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="49015-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="49015-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="49015-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49015-136">Indica se o recurso será desalocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="49015-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="49015-137">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="49015-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="49015-138">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="49015-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49015-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="49015-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49015-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="49015-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49015-141">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="49015-141">A short description of the object.</span></span> <span data-ttu-id="49015-142">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="49015-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="49015-143">**Conexão**</span><span class="sxs-lookup"><span data-stu-id="49015-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49015-144">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="49015-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="49015-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="49015-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49015-146">A coisa à qual esse recurso está conectado.</span><span class="sxs-lookup"><span data-stu-id="49015-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="49015-147">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="49015-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="49015-148">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="49015-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49015-149">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="49015-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="49015-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="49015-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49015-151">A visibilidade dos consumidores para o recurso alocado.</span><span class="sxs-lookup"><span data-stu-id="49015-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="49015-152">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="49015-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="49015-153">Valor</span><span class="sxs-lookup"><span data-stu-id="49015-153">Value</span></span>                                                                        | <span data-ttu-id="49015-154">Significado</span><span class="sxs-lookup"><span data-stu-id="49015-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="49015-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="49015-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="49015-156">Virtualizado</span><span class="sxs-lookup"><span data-stu-id="49015-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="49015-157">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="49015-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49015-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="49015-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49015-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="49015-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49015-160">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="49015-160">A description of the object.</span></span> <span data-ttu-id="49015-161">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="49015-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="49015-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="49015-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49015-163">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="49015-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49015-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="49015-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49015-165">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="49015-165">A display name for the object.</span></span> <span data-ttu-id="49015-166">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="49015-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="49015-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="49015-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49015-168">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="49015-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="49015-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="49015-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49015-170">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="49015-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="49015-171">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e tem um valor padrão de 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="49015-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and has a default value of 2 (Enabled).</span></span>

<span data-ttu-id="49015-172">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="49015-172">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<dt>



 <span data-ttu-id="49015-173">(2)</span><span class="sxs-lookup"><span data-stu-id="49015-173">(2)</span></span>


</dt> <dd>

<span data-ttu-id="49015-174">habilitado</span><span class="sxs-lookup"><span data-stu-id="49015-174">Enabled</span></span>

</dd> <dt>

<span data-ttu-id="49015-175">3</span><span class="sxs-lookup"><span data-stu-id="49015-175">3</span></span>
</dt> <dd>

<span data-ttu-id="49015-176">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="49015-176">Disabled</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="49015-177">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="49015-177">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49015-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="49015-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49015-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="49015-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49015-180">Expõe uma atribuição específica para o host ou recursos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="49015-180">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="49015-181">Essa propriedade é herdada de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e sempre é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="49015-181">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="49015-182">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="49015-182">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49015-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="49015-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49015-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="49015-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49015-185">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="49015-185">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="49015-186">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="49015-186">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="49015-187">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="49015-187">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="49015-188">**Limite**</span><span class="sxs-lookup"><span data-stu-id="49015-188">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49015-189">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="49015-189">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="49015-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="49015-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49015-191">O limite superior ou a quantidade máxima de recursos que serão concedidos para essa alocação.</span><span class="sxs-lookup"><span data-stu-id="49015-191">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="49015-192">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="49015-192">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="49015-193">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="49015-193">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49015-194">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="49015-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="49015-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="49015-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49015-196">Indica como esse recurso é mapeado para recursos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="49015-196">Indicates how this resource maps to underlying resources.</span></span> <span data-ttu-id="49015-197">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="49015-197">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="49015-198">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="49015-198">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49015-199">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="49015-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49015-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="49015-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49015-201">Uma cadeia de caracteres que descreve o tipo de recurso quando um valor bem definido não está disponível e **ResourceType** tem o valor 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="49015-201">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="49015-202">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="49015-202">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="49015-203">**Pai**</span><span class="sxs-lookup"><span data-stu-id="49015-203">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49015-204">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="49015-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49015-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="49015-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49015-206">O pai do recurso.</span><span class="sxs-lookup"><span data-stu-id="49015-206">The parent of the resource.</span></span> <span data-ttu-id="49015-207">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="49015-207">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="49015-208">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="49015-208">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49015-209">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="49015-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49015-210">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="49015-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49015-211">A ID do pool de recursos do qual o recurso está alocado.</span><span class="sxs-lookup"><span data-stu-id="49015-211">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="49015-212">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="49015-212">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="49015-213">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="49015-213">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49015-214">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="49015-214">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="49015-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="49015-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49015-216">A quantidade de recursos com garantia disponível para essa alocação.</span><span class="sxs-lookup"><span data-stu-id="49015-216">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="49015-217">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="49015-217">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="49015-218">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="49015-218">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49015-219">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="49015-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49015-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="49015-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49015-221">Uma cadeia de caracteres que descreve um subtipo específico de implementação para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="49015-221">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="49015-222">Essa propriedade é herdada de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e sempre é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="49015-222">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="49015-223">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="49015-223">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49015-224">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="49015-224">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="49015-225">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="49015-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49015-226">O tipo de recurso que essa configuração de alocação representa.</span><span class="sxs-lookup"><span data-stu-id="49015-226">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="49015-227">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e é sempre definida como 1 (outra).</span><span class="sxs-lookup"><span data-stu-id="49015-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1 (Other).</span></span>



| <span data-ttu-id="49015-228">Valor</span><span class="sxs-lookup"><span data-stu-id="49015-228">Value</span></span>                                                                        | <span data-ttu-id="49015-229">Significado</span><span class="sxs-lookup"><span data-stu-id="49015-229">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="49015-230"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="49015-230"><dt>1</dt></span></span> </dl> | <span data-ttu-id="49015-231">Outro</span><span class="sxs-lookup"><span data-stu-id="49015-231">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="49015-232">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="49015-232">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49015-233">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="49015-233">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="49015-234">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="49015-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49015-235">A quantidade de recursos apresentados ao consumidor.</span><span class="sxs-lookup"><span data-stu-id="49015-235">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="49015-236">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="49015-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="49015-237">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="49015-237">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49015-238">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="49015-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49015-239">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="49015-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49015-240">Especifica a unidade de medida para essa alocação de recursos.</span><span class="sxs-lookup"><span data-stu-id="49015-240">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="49015-241">O valor dessa propriedade é um valor válido do qualificador de unidades programáticas, conforme definido no anexo C. 1 de DSP0004 V 2.5 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="49015-241">The value of this property is a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="49015-242">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="49015-242">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="49015-243">**Weight**</span><span class="sxs-lookup"><span data-stu-id="49015-243">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49015-244">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="49015-244">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49015-245">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="49015-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49015-246">Uma prioridade relativa para essa alocação em relação a outras alocações do mesmo pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="49015-246">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="49015-247">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="49015-247">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49015-248">Comentários</span><span class="sxs-lookup"><span data-stu-id="49015-248">Remarks</span></span>

<span data-ttu-id="49015-249">O acesso à classe **Msvm \_ VssComponentSettingData** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="49015-249">Access to the **Msvm\_VssComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="49015-250">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="49015-250">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="49015-251">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49015-251">Requirements</span></span>



| <span data-ttu-id="49015-252">Requisito</span><span class="sxs-lookup"><span data-stu-id="49015-252">Requirement</span></span> | <span data-ttu-id="49015-253">Valor</span><span class="sxs-lookup"><span data-stu-id="49015-253">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49015-254">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49015-254">Minimum supported client</span></span><br/> | <span data-ttu-id="49015-255">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="49015-255">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="49015-256">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49015-256">Minimum supported server</span></span><br/> | <span data-ttu-id="49015-257">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="49015-257">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="49015-258">Namespace</span><span class="sxs-lookup"><span data-stu-id="49015-258">Namespace</span></span><br/>                | <span data-ttu-id="49015-259">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="49015-259">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="49015-260">MOF</span><span class="sxs-lookup"><span data-stu-id="49015-260">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49015-261"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="49015-261"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="49015-262">DLL</span><span class="sxs-lookup"><span data-stu-id="49015-262">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49015-263"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="49015-263"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="49015-264">Confira também</span><span class="sxs-lookup"><span data-stu-id="49015-264">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49015-265">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="49015-265">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="49015-266">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="49015-266">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

