---
description: Representa o estado configurado do serviço de sincronização de tempo.
ms.assetid: AACEDE11-3F5B-42AB-A16F-0474FA98D3FD
title: Classe Msvm_TimeSyncComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TimeSyncComponentSettingData
- Msvm_TimeSyncComponentSettingData.InstanceID
- Msvm_TimeSyncComponentSettingData.Caption
- Msvm_TimeSyncComponentSettingData.Description
- Msvm_TimeSyncComponentSettingData.ElementName
- Msvm_TimeSyncComponentSettingData.ResourceType
- Msvm_TimeSyncComponentSettingData.OtherResourceType
- Msvm_TimeSyncComponentSettingData.ResourceSubType
- Msvm_TimeSyncComponentSettingData.PoolID
- Msvm_TimeSyncComponentSettingData.ConsumerVisibility
- Msvm_TimeSyncComponentSettingData.HostResource
- Msvm_TimeSyncComponentSettingData.AllocationUnits
- Msvm_TimeSyncComponentSettingData.VirtualQuantity
- Msvm_TimeSyncComponentSettingData.Reservation
- Msvm_TimeSyncComponentSettingData.Limit
- Msvm_TimeSyncComponentSettingData.Weight
- Msvm_TimeSyncComponentSettingData.AutomaticAllocation
- Msvm_TimeSyncComponentSettingData.AutomaticDeallocation
- Msvm_TimeSyncComponentSettingData.Parent
- Msvm_TimeSyncComponentSettingData.Connection
- Msvm_TimeSyncComponentSettingData.Address
- Msvm_TimeSyncComponentSettingData.MappingBehavior
- Msvm_TimeSyncComponentSettingData.AddressOnParent
- Msvm_TimeSyncComponentSettingData.VirtualQuantityUnits
- Msvm_TimeSyncComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 063c0f7904976d50d7c1914f810e71ff84f740b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921170"
---
# <a name="msvm_timesynccomponentsettingdata-class"></a><span data-ttu-id="203d0-103">\_Classe Msvm TimeSyncComponentSettingData</span><span class="sxs-lookup"><span data-stu-id="203d0-103">Msvm\_TimeSyncComponentSettingData class</span></span>

<span data-ttu-id="203d0-104">Representa o estado configurado do serviço de sincronização de tempo.</span><span class="sxs-lookup"><span data-stu-id="203d0-104">Represents the configured state of the time synchronization service.</span></span>

<span data-ttu-id="203d0-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="203d0-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="203d0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="203d0-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TimeSyncComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Time Synchronization";
  string  Description = "Microsoft Time Synchronization Service Setting Data";
  string  ElementName = "Time Synchronization";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:Time Synchronization Component";
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
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

## <a name="members"></a><span data-ttu-id="203d0-107">Membros</span><span class="sxs-lookup"><span data-stu-id="203d0-107">Members</span></span>

<span data-ttu-id="203d0-108">A classe **Msvm \_ TimeSyncComponentSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="203d0-108">The **Msvm\_TimeSyncComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="203d0-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="203d0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="203d0-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="203d0-110">Properties</span></span>

<span data-ttu-id="203d0-111">A classe **Msvm \_ TimeSyncComponentSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="203d0-111">The **Msvm\_TimeSyncComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="203d0-112">**Endereço**</span><span class="sxs-lookup"><span data-stu-id="203d0-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="203d0-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="203d0-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="203d0-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="203d0-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="203d0-115">O endereço do recurso.</span><span class="sxs-lookup"><span data-stu-id="203d0-115">The address of the resource.</span></span> <span data-ttu-id="203d0-116">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="203d0-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="203d0-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="203d0-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="203d0-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="203d0-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="203d0-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="203d0-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="203d0-120">Descreve o endereço deste recurso no contexto do pai.</span><span class="sxs-lookup"><span data-stu-id="203d0-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="203d0-121">As propriedades **pai** e **AddressOnParent** são usadas para descrever a relação do controlador, bem como a ordem dos dispositivos em um controlador.</span><span class="sxs-lookup"><span data-stu-id="203d0-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="203d0-122">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="203d0-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="203d0-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="203d0-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="203d0-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="203d0-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="203d0-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="203d0-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="203d0-126">As unidades de alocação usadas pelas propriedades **Reservation** e **Limit** .</span><span class="sxs-lookup"><span data-stu-id="203d0-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="203d0-127">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="203d0-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="203d0-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="203d0-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="203d0-129">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="203d0-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="203d0-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="203d0-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="203d0-131">Indica se o recurso será alocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="203d0-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="203d0-132">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="203d0-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="203d0-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="203d0-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="203d0-134">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="203d0-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="203d0-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="203d0-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="203d0-136">Indica se o recurso será desalocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="203d0-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="203d0-137">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="203d0-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="203d0-138">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="203d0-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="203d0-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="203d0-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="203d0-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="203d0-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="203d0-141">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="203d0-141">A short description of the object.</span></span> <span data-ttu-id="203d0-142">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="203d0-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="203d0-143">**Conexão**</span><span class="sxs-lookup"><span data-stu-id="203d0-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="203d0-144">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="203d0-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="203d0-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="203d0-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="203d0-146">A coisa à qual esse recurso está conectado.</span><span class="sxs-lookup"><span data-stu-id="203d0-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="203d0-147">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="203d0-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="203d0-148">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="203d0-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="203d0-149">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="203d0-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="203d0-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="203d0-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="203d0-151">A visibilidade dos consumidores para o recurso alocado.</span><span class="sxs-lookup"><span data-stu-id="203d0-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="203d0-152">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="203d0-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="203d0-153">Valor</span><span class="sxs-lookup"><span data-stu-id="203d0-153">Value</span></span>                                                                        | <span data-ttu-id="203d0-154">Significado</span><span class="sxs-lookup"><span data-stu-id="203d0-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="203d0-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="203d0-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="203d0-156">Virtualizado</span><span class="sxs-lookup"><span data-stu-id="203d0-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="203d0-157">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="203d0-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="203d0-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="203d0-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="203d0-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="203d0-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="203d0-160">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="203d0-160">A description of the object.</span></span> <span data-ttu-id="203d0-161">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="203d0-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="203d0-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="203d0-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="203d0-163">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="203d0-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="203d0-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="203d0-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="203d0-165">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="203d0-165">A display name for the object.</span></span> <span data-ttu-id="203d0-166">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="203d0-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="203d0-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="203d0-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="203d0-168">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="203d0-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="203d0-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="203d0-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="203d0-170">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="203d0-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="203d0-171">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="203d0-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span></span>

<dt>



 <span data-ttu-id="203d0-172">(2)</span><span class="sxs-lookup"><span data-stu-id="203d0-172">(2)</span></span>


</dt> <dd>

<span data-ttu-id="203d0-173">habilitado</span><span class="sxs-lookup"><span data-stu-id="203d0-173">Enabled</span></span>

</dd> <dt>

<span data-ttu-id="203d0-174">3</span><span class="sxs-lookup"><span data-stu-id="203d0-174">3</span></span>
</dt> <dd>

<span data-ttu-id="203d0-175">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="203d0-175">Disabled</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="203d0-176">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="203d0-176">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="203d0-177">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="203d0-177">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="203d0-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="203d0-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="203d0-179">Expõe uma atribuição específica para o host ou recursos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="203d0-179">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="203d0-180">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="203d0-180">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="203d0-181">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="203d0-181">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="203d0-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="203d0-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="203d0-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="203d0-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="203d0-184">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="203d0-184">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="203d0-185">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="203d0-185">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="203d0-186">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="203d0-186">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="203d0-187">**Limite**</span><span class="sxs-lookup"><span data-stu-id="203d0-187">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="203d0-188">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="203d0-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="203d0-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="203d0-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="203d0-190">O limite superior ou a quantidade máxima de recursos que serão concedidos para essa alocação.</span><span class="sxs-lookup"><span data-stu-id="203d0-190">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="203d0-191">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="203d0-191">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="203d0-192">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="203d0-192">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="203d0-193">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="203d0-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="203d0-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="203d0-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="203d0-195">Especifica como esse recurso é mapeado para recursos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="203d0-195">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="203d0-196">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="203d0-196">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="203d0-197">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="203d0-197">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="203d0-198">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="203d0-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="203d0-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="203d0-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="203d0-200">O tipo de recurso quando um valor bem definido não está disponível e **ResourceType** tem o valor "other".</span><span class="sxs-lookup"><span data-stu-id="203d0-200">The resource type when a well-defined value is not available and **ResourceType** has the value "Other".</span></span> <span data-ttu-id="203d0-201">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="203d0-201">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="203d0-202">**Pai**</span><span class="sxs-lookup"><span data-stu-id="203d0-202">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="203d0-203">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="203d0-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="203d0-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="203d0-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="203d0-205">O pai do recurso.</span><span class="sxs-lookup"><span data-stu-id="203d0-205">The parent of the resource.</span></span> <span data-ttu-id="203d0-206">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="203d0-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="203d0-207">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="203d0-207">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="203d0-208">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="203d0-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="203d0-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="203d0-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="203d0-210">A ID do pool de recursos do qual o recurso está alocado.</span><span class="sxs-lookup"><span data-stu-id="203d0-210">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="203d0-211">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="203d0-211">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="203d0-212">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="203d0-212">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="203d0-213">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="203d0-213">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="203d0-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="203d0-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="203d0-215">A quantidade de recursos com garantia disponível para essa alocação.</span><span class="sxs-lookup"><span data-stu-id="203d0-215">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="203d0-216">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="203d0-216">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="203d0-217">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="203d0-217">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="203d0-218">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="203d0-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="203d0-219">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="203d0-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="203d0-220">Uma cadeia de caracteres que descreve um subtipo específico de implementação para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="203d0-220">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="203d0-221">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="203d0-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="203d0-222">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="203d0-222">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="203d0-223">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="203d0-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="203d0-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="203d0-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="203d0-225">O tipo de recurso que essa configuração de alocação representa.</span><span class="sxs-lookup"><span data-stu-id="203d0-225">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="203d0-226">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="203d0-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="203d0-227">Valor</span><span class="sxs-lookup"><span data-stu-id="203d0-227">Value</span></span>                                                                        | <span data-ttu-id="203d0-228">Significado</span><span class="sxs-lookup"><span data-stu-id="203d0-228">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="203d0-229"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="203d0-229"><dt>1</dt></span></span> </dl> | <span data-ttu-id="203d0-230">Outro</span><span class="sxs-lookup"><span data-stu-id="203d0-230">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="203d0-231">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="203d0-231">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="203d0-232">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="203d0-232">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="203d0-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="203d0-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="203d0-234">A quantidade de recursos apresentados ao consumidor.</span><span class="sxs-lookup"><span data-stu-id="203d0-234">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="203d0-235">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="203d0-235">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="203d0-236">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="203d0-236">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="203d0-237">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="203d0-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="203d0-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="203d0-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="203d0-239">Especifica a unidade de medida para essa alocação de recursos.</span><span class="sxs-lookup"><span data-stu-id="203d0-239">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="203d0-240">O valor dessa propriedade deve ser um valor válido do qualificador de unidades programáticas, conforme definido no anexo C. 1 de DSP0004 V 2.5 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="203d0-240">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="203d0-241">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="203d0-241">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="203d0-242">**Weight**</span><span class="sxs-lookup"><span data-stu-id="203d0-242">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="203d0-243">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="203d0-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="203d0-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="203d0-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="203d0-245">Uma prioridade relativa para essa alocação em relação a outras alocações do mesmo pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="203d0-245">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="203d0-246">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="203d0-246">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="203d0-247">Comentários</span><span class="sxs-lookup"><span data-stu-id="203d0-247">Remarks</span></span>

<span data-ttu-id="203d0-248">O acesso à classe **Msvm \_ TimeSyncComponentSettingData** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="203d0-248">Access to the **Msvm\_TimeSyncComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="203d0-249">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="203d0-249">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="203d0-250">Requisitos</span><span class="sxs-lookup"><span data-stu-id="203d0-250">Requirements</span></span>



| <span data-ttu-id="203d0-251">Requisito</span><span class="sxs-lookup"><span data-stu-id="203d0-251">Requirement</span></span> | <span data-ttu-id="203d0-252">Valor</span><span class="sxs-lookup"><span data-stu-id="203d0-252">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="203d0-253">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="203d0-253">Minimum supported client</span></span><br/> | <span data-ttu-id="203d0-254">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="203d0-254">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="203d0-255">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="203d0-255">Minimum supported server</span></span><br/> | <span data-ttu-id="203d0-256">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="203d0-256">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="203d0-257">Namespace</span><span class="sxs-lookup"><span data-stu-id="203d0-257">Namespace</span></span><br/>                | <span data-ttu-id="203d0-258">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="203d0-258">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="203d0-259">MOF</span><span class="sxs-lookup"><span data-stu-id="203d0-259">MOF</span></span><br/>                      | <dl> <span data-ttu-id="203d0-260"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="203d0-260"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="203d0-261">DLL</span><span class="sxs-lookup"><span data-stu-id="203d0-261">DLL</span></span><br/>                      | <dl> <span data-ttu-id="203d0-262"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="203d0-262"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="203d0-263">Confira também</span><span class="sxs-lookup"><span data-stu-id="203d0-263">See also</span></span>

<dl> <dt>

[<span data-ttu-id="203d0-264">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="203d0-264">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="203d0-265">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="203d0-265">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

