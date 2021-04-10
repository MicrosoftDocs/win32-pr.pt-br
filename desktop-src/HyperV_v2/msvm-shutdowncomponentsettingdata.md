---
description: Representa o estado configurado do serviço de desligamento.
ms.assetid: 434DE26A-E78A-403A-AFAB-2F9272426A16
title: Classe Msvm_ShutdownComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponentSettingData
- Msvm_ShutdownComponentSettingData.InstanceID
- Msvm_ShutdownComponentSettingData.Caption
- Msvm_ShutdownComponentSettingData.Description
- Msvm_ShutdownComponentSettingData.ElementName
- Msvm_ShutdownComponentSettingData.ResourceType
- Msvm_ShutdownComponentSettingData.OtherResourceType
- Msvm_ShutdownComponentSettingData.ResourceSubType
- Msvm_ShutdownComponentSettingData.PoolID
- Msvm_ShutdownComponentSettingData.ConsumerVisibility
- Msvm_ShutdownComponentSettingData.HostResource
- Msvm_ShutdownComponentSettingData.AllocationUnits
- Msvm_ShutdownComponentSettingData.VirtualQuantity
- Msvm_ShutdownComponentSettingData.Reservation
- Msvm_ShutdownComponentSettingData.Limit
- Msvm_ShutdownComponentSettingData.Weight
- Msvm_ShutdownComponentSettingData.AutomaticAllocation
- Msvm_ShutdownComponentSettingData.AutomaticDeallocation
- Msvm_ShutdownComponentSettingData.Parent
- Msvm_ShutdownComponentSettingData.Connection
- Msvm_ShutdownComponentSettingData.Address
- Msvm_ShutdownComponentSettingData.MappingBehavior
- Msvm_ShutdownComponentSettingData.AddressOnParent
- Msvm_ShutdownComponentSettingData.VirtualQuantityUnits
- Msvm_ShutdownComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8ee2fcb910dc788b01a58544bbfe6a06ba215585
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165007"
---
# <a name="msvm_shutdowncomponentsettingdata-class"></a><span data-ttu-id="57ff5-103">\_Classe Msvm ShutdownComponentSettingData</span><span class="sxs-lookup"><span data-stu-id="57ff5-103">Msvm\_ShutdownComponentSettingData class</span></span>

<span data-ttu-id="57ff5-104">Representa o estado configurado do serviço de desligamento.</span><span class="sxs-lookup"><span data-stu-id="57ff5-104">Represents the configured state of the shutdown service.</span></span>

<span data-ttu-id="57ff5-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="57ff5-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="57ff5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57ff5-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ShutdownComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Shutdown";
  string  Description = "Microsoft Shutdown Service Setting Data";
  string  ElementName = "Shutdown";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:Shutdown Component";
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

## <a name="members"></a><span data-ttu-id="57ff5-107">Membros</span><span class="sxs-lookup"><span data-stu-id="57ff5-107">Members</span></span>

<span data-ttu-id="57ff5-108">A classe **Msvm \_ ShutdownComponentSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="57ff5-108">The **Msvm\_ShutdownComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="57ff5-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="57ff5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="57ff5-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="57ff5-110">Properties</span></span>

<span data-ttu-id="57ff5-111">A classe **Msvm \_ ShutdownComponentSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="57ff5-111">The **Msvm\_ShutdownComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="57ff5-112">**Endereço**</span><span class="sxs-lookup"><span data-stu-id="57ff5-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57ff5-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="57ff5-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57ff5-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57ff5-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57ff5-115">O endereço do recurso.</span><span class="sxs-lookup"><span data-stu-id="57ff5-115">The address of the resource.</span></span> <span data-ttu-id="57ff5-116">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="57ff5-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="57ff5-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="57ff5-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57ff5-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="57ff5-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57ff5-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57ff5-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57ff5-120">Descreve o endereço deste recurso no contexto do pai.</span><span class="sxs-lookup"><span data-stu-id="57ff5-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="57ff5-121">As propriedades **pai** e **AddressOnParent** são usadas para descrever a relação do controlador, bem como a ordem dos dispositivos em um controlador.</span><span class="sxs-lookup"><span data-stu-id="57ff5-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="57ff5-122">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="57ff5-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="57ff5-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="57ff5-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57ff5-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="57ff5-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57ff5-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57ff5-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57ff5-126">As unidades de alocação usadas pelas propriedades **Reservation** e **Limit** .</span><span class="sxs-lookup"><span data-stu-id="57ff5-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="57ff5-127">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="57ff5-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="57ff5-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="57ff5-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57ff5-129">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="57ff5-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="57ff5-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57ff5-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57ff5-131">Indica se o recurso será alocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="57ff5-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="57ff5-132">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="57ff5-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="57ff5-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="57ff5-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57ff5-134">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="57ff5-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="57ff5-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57ff5-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57ff5-136">Indica se o recurso será desalocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="57ff5-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="57ff5-137">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="57ff5-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="57ff5-138">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="57ff5-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57ff5-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="57ff5-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57ff5-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57ff5-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57ff5-141">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="57ff5-141">A short description of the object.</span></span> <span data-ttu-id="57ff5-142">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "Shutdown".</span><span class="sxs-lookup"><span data-stu-id="57ff5-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Shutdown".</span></span>

</dd> <dt>

<span data-ttu-id="57ff5-143">**Conexão**</span><span class="sxs-lookup"><span data-stu-id="57ff5-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57ff5-144">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="57ff5-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="57ff5-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57ff5-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57ff5-146">A coisa à qual esse recurso está conectado.</span><span class="sxs-lookup"><span data-stu-id="57ff5-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="57ff5-147">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="57ff5-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="57ff5-148">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="57ff5-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57ff5-149">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57ff5-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="57ff5-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57ff5-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57ff5-151">A visibilidade dos consumidores para o recurso alocado.</span><span class="sxs-lookup"><span data-stu-id="57ff5-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="57ff5-152">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="57ff5-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="57ff5-153">Valor</span><span class="sxs-lookup"><span data-stu-id="57ff5-153">Value</span></span>                                                                        | <span data-ttu-id="57ff5-154">Significado</span><span class="sxs-lookup"><span data-stu-id="57ff5-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="57ff5-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="57ff5-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="57ff5-156">Virtualizado</span><span class="sxs-lookup"><span data-stu-id="57ff5-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="57ff5-157">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="57ff5-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57ff5-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="57ff5-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57ff5-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57ff5-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57ff5-160">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="57ff5-160">A description of the object.</span></span> <span data-ttu-id="57ff5-161">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="57ff5-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="57ff5-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="57ff5-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57ff5-163">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="57ff5-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57ff5-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57ff5-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57ff5-165">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="57ff5-165">A display name for the object.</span></span> <span data-ttu-id="57ff5-166">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="57ff5-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="57ff5-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="57ff5-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57ff5-168">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57ff5-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="57ff5-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57ff5-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57ff5-170">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="57ff5-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="57ff5-171">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="57ff5-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="57ff5-172">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="57ff5-172">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="57ff5-173">**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="57ff5-173">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="57ff5-174">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="57ff5-174">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57ff5-175">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="57ff5-175">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="57ff5-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57ff5-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57ff5-177">Expõe uma atribuição específica para o host ou recursos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="57ff5-177">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="57ff5-178">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="57ff5-178">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="57ff5-179">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="57ff5-179">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57ff5-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="57ff5-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57ff5-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57ff5-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57ff5-182">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="57ff5-182">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="57ff5-183">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="57ff5-183">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="57ff5-184">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="57ff5-184">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="57ff5-185">**Limite**</span><span class="sxs-lookup"><span data-stu-id="57ff5-185">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57ff5-186">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="57ff5-186">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="57ff5-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57ff5-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57ff5-188">O limite superior ou a quantidade máxima de recursos que serão concedidos para essa alocação.</span><span class="sxs-lookup"><span data-stu-id="57ff5-188">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="57ff5-189">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="57ff5-189">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="57ff5-190">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="57ff5-190">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57ff5-191">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57ff5-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="57ff5-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57ff5-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57ff5-193">Especifica como esse recurso é mapeado para recursos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="57ff5-193">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="57ff5-194">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="57ff5-194">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="57ff5-195">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="57ff5-195">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57ff5-196">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="57ff5-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57ff5-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57ff5-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57ff5-198">Uma cadeia de caracteres que descreve o tipo de recurso quando um valor bem definido não está disponível e **ResourceType** tem o valor 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="57ff5-198">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="57ff5-199">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="57ff5-199">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="57ff5-200">**Pai**</span><span class="sxs-lookup"><span data-stu-id="57ff5-200">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57ff5-201">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="57ff5-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57ff5-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57ff5-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57ff5-203">O pai do recurso.</span><span class="sxs-lookup"><span data-stu-id="57ff5-203">The parent of the resource.</span></span> <span data-ttu-id="57ff5-204">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="57ff5-204">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="57ff5-205">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="57ff5-205">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57ff5-206">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="57ff5-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57ff5-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57ff5-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57ff5-208">A ID do pool de recursos do qual o recurso está alocado.</span><span class="sxs-lookup"><span data-stu-id="57ff5-208">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="57ff5-209">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="57ff5-209">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="57ff5-210">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="57ff5-210">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57ff5-211">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="57ff5-211">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="57ff5-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57ff5-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57ff5-213">A quantidade de recursos com garantia disponível para essa alocação.</span><span class="sxs-lookup"><span data-stu-id="57ff5-213">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="57ff5-214">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="57ff5-214">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="57ff5-215">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="57ff5-215">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57ff5-216">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="57ff5-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57ff5-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57ff5-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57ff5-218">Uma cadeia de caracteres que descreve um subtipo específico de implementação para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="57ff5-218">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="57ff5-219">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="57ff5-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="57ff5-220">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="57ff5-220">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57ff5-221">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57ff5-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="57ff5-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57ff5-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57ff5-223">O tipo de recurso que essa configuração de alocação representa.</span><span class="sxs-lookup"><span data-stu-id="57ff5-223">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="57ff5-224">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="57ff5-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="57ff5-225">Valor</span><span class="sxs-lookup"><span data-stu-id="57ff5-225">Value</span></span>                                                                        | <span data-ttu-id="57ff5-226">Significado</span><span class="sxs-lookup"><span data-stu-id="57ff5-226">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="57ff5-227"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="57ff5-227"><dt>1</dt></span></span> </dl> | <span data-ttu-id="57ff5-228">Outro</span><span class="sxs-lookup"><span data-stu-id="57ff5-228">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="57ff5-229">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="57ff5-229">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57ff5-230">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="57ff5-230">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="57ff5-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57ff5-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57ff5-232">A quantidade de recursos apresentados ao consumidor.</span><span class="sxs-lookup"><span data-stu-id="57ff5-232">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="57ff5-233">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="57ff5-233">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="57ff5-234">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="57ff5-234">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57ff5-235">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="57ff5-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57ff5-236">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57ff5-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57ff5-237">Especifica a unidade de medida para essa alocação de recursos.</span><span class="sxs-lookup"><span data-stu-id="57ff5-237">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="57ff5-238">O valor dessa propriedade deve ser um valor válido do qualificador de unidades programáticas, conforme definido no anexo C. 1 de DSP0004 V 2.5 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="57ff5-238">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="57ff5-239">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="57ff5-239">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="57ff5-240">**Weight**</span><span class="sxs-lookup"><span data-stu-id="57ff5-240">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57ff5-241">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57ff5-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57ff5-242">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57ff5-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57ff5-243">Uma prioridade relativa para essa alocação em relação a outras alocações do mesmo pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="57ff5-243">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="57ff5-244">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="57ff5-244">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57ff5-245">Comentários</span><span class="sxs-lookup"><span data-stu-id="57ff5-245">Remarks</span></span>

<span data-ttu-id="57ff5-246">O acesso à classe **Msvm \_ ShutdownComponentSettingData** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="57ff5-246">Access to the **Msvm\_ShutdownComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="57ff5-247">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="57ff5-247">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="57ff5-248">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57ff5-248">Requirements</span></span>



| <span data-ttu-id="57ff5-249">Requisito</span><span class="sxs-lookup"><span data-stu-id="57ff5-249">Requirement</span></span> | <span data-ttu-id="57ff5-250">Valor</span><span class="sxs-lookup"><span data-stu-id="57ff5-250">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57ff5-251">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57ff5-251">Minimum supported client</span></span><br/> | <span data-ttu-id="57ff5-252">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="57ff5-252">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="57ff5-253">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57ff5-253">Minimum supported server</span></span><br/> | <span data-ttu-id="57ff5-254">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="57ff5-254">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="57ff5-255">Namespace</span><span class="sxs-lookup"><span data-stu-id="57ff5-255">Namespace</span></span><br/>                | <span data-ttu-id="57ff5-256">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="57ff5-256">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="57ff5-257">MOF</span><span class="sxs-lookup"><span data-stu-id="57ff5-257">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57ff5-258"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="57ff5-258"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="57ff5-259">DLL</span><span class="sxs-lookup"><span data-stu-id="57ff5-259">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57ff5-260"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="57ff5-260"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="57ff5-261">Confira também</span><span class="sxs-lookup"><span data-stu-id="57ff5-261">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57ff5-262">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="57ff5-262">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="57ff5-263">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="57ff5-263">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

