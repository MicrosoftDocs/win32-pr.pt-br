---
description: Representa o estado configurado do serviço de pulsação.
ms.assetid: 2946FA02-A751-4576-BB8A-004C80E21E5B
title: Classe Msvm_HeartbeatComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HeartbeatComponentSettingData
- Msvm_HeartbeatComponentSettingData.InstanceID
- Msvm_HeartbeatComponentSettingData.Caption
- Msvm_HeartbeatComponentSettingData.Description
- Msvm_HeartbeatComponentSettingData.ElementName
- Msvm_HeartbeatComponentSettingData.ResourceType
- Msvm_HeartbeatComponentSettingData.OtherResourceType
- Msvm_HeartbeatComponentSettingData.ResourceSubType
- Msvm_HeartbeatComponentSettingData.PoolID
- Msvm_HeartbeatComponentSettingData.ConsumerVisibility
- Msvm_HeartbeatComponentSettingData.HostResource
- Msvm_HeartbeatComponentSettingData.AllocationUnits
- Msvm_HeartbeatComponentSettingData.VirtualQuantity
- Msvm_HeartbeatComponentSettingData.Reservation
- Msvm_HeartbeatComponentSettingData.Limit
- Msvm_HeartbeatComponentSettingData.Weight
- Msvm_HeartbeatComponentSettingData.AutomaticAllocation
- Msvm_HeartbeatComponentSettingData.AutomaticDeallocation
- Msvm_HeartbeatComponentSettingData.Parent
- Msvm_HeartbeatComponentSettingData.Connection
- Msvm_HeartbeatComponentSettingData.Address
- Msvm_HeartbeatComponentSettingData.MappingBehavior
- Msvm_HeartbeatComponentSettingData.AddressOnParent
- Msvm_HeartbeatComponentSettingData.VirtualQuantityUnits
- Msvm_HeartbeatComponentSettingData.EnabledState
- Msvm_HeartbeatComponentSettingData.ErrorThreshold
- Msvm_HeartbeatComponentSettingData.Interval
- Msvm_HeartbeatComponentSettingData.Latency
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a36afbd8ab17a3fc2dfddb99b0a648fddbada415
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761712"
---
# <a name="msvm_heartbeatcomponentsettingdata-class"></a><span data-ttu-id="d1d60-103">\_Classe Msvm HeartbeatComponentSettingData</span><span class="sxs-lookup"><span data-stu-id="d1d60-103">Msvm\_HeartbeatComponentSettingData class</span></span>

<span data-ttu-id="d1d60-104">Representa o estado configurado do serviço de pulsação.</span><span class="sxs-lookup"><span data-stu-id="d1d60-104">Represents the configured state of the heartbeat service.</span></span>

<span data-ttu-id="d1d60-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d1d60-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1d60-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1d60-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HeartbeatComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string  Caption = "Heartbeat";
  string  Description = "Microsoft Heartbeat Service Setting Data";
  string  ElementName = "Heartbeat";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft Heartbeat Component";
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "Integration Components";
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
  uint32  ErrorThreshold = 2;
  uint32  Interval = 2000;
  uint32  Latency = 1000;
};
```

## <a name="members"></a><span data-ttu-id="d1d60-107">Membros</span><span class="sxs-lookup"><span data-stu-id="d1d60-107">Members</span></span>

<span data-ttu-id="d1d60-108">A classe **Msvm \_ HeartbeatComponentSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d1d60-108">The **Msvm\_HeartbeatComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d1d60-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d1d60-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1d60-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d1d60-110">Properties</span></span>

<span data-ttu-id="d1d60-111">A classe **Msvm \_ HeartbeatComponentSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d1d60-111">The **Msvm\_HeartbeatComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1d60-112">**Endereço**</span><span class="sxs-lookup"><span data-stu-id="d1d60-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1d60-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-115">O endereço do recurso.</span><span class="sxs-lookup"><span data-stu-id="d1d60-115">The address of the resource.</span></span> <span data-ttu-id="d1d60-116">Essa propriedade é herdada de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e sempre é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d1d60-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d1d60-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="d1d60-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1d60-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-120">Descreve o endereço deste recurso no contexto do pai.</span><span class="sxs-lookup"><span data-stu-id="d1d60-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="d1d60-121">As propriedades **pai** / **AddressOnParent** são usadas para descrever a relação do controlador, bem como a ordem dos dispositivos em um controlador.</span><span class="sxs-lookup"><span data-stu-id="d1d60-121">The **Parent**/**AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="d1d60-122">Por exemplo, se o pai for um controlador PCI, essa propriedade especificaria o slot PCI desse dispositivo filho.</span><span class="sxs-lookup"><span data-stu-id="d1d60-122">For example, if the parent is a PCI Controller, this property would specify the PCI slot of this child device.</span></span> <span data-ttu-id="d1d60-123">Essa propriedade é herdada de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e sempre é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d1d60-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d1d60-124">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="d1d60-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1d60-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-127">As unidades de alocação usadas pelas propriedades **Reservation** e **Limit** .</span><span class="sxs-lookup"><span data-stu-id="d1d60-127">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="d1d60-128">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e é sempre definida como "componentes de integração".</span><span class="sxs-lookup"><span data-stu-id="d1d60-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to "Integration Components".</span></span>

</dd> <dt>

<span data-ttu-id="d1d60-129">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="d1d60-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-130">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d1d60-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-132">Indica se o recurso é alocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="d1d60-132">Indicates whether the resource is automatically allocated.</span></span> <span data-ttu-id="d1d60-133">Essa propriedade é herdada de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e sempre é definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="d1d60-133">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="d1d60-134">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="d1d60-134">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-135">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d1d60-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-137">Indica se o recurso é desalocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="d1d60-137">Indicates whether the resource is automatically de-allocated.</span></span> <span data-ttu-id="d1d60-138">Essa propriedade é herdada de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e sempre é definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="d1d60-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="d1d60-139">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="d1d60-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1d60-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-142">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="d1d60-142">A short description of the object.</span></span> <span data-ttu-id="d1d60-143">Essa propriedade é herdada da classe [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) e é sempre definida como "Heartbeat".</span><span class="sxs-lookup"><span data-stu-id="d1d60-143">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Heartbeat".</span></span>

</dd> <dt>

<span data-ttu-id="d1d60-144">**Conexão**</span><span class="sxs-lookup"><span data-stu-id="d1d60-144">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-145">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1d60-145">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-147">A coisa à qual esse recurso está conectado.</span><span class="sxs-lookup"><span data-stu-id="d1d60-147">The thing to which this resource is connected.</span></span> <span data-ttu-id="d1d60-148">Essa propriedade é herdada de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e sempre é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d1d60-148">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d1d60-149">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="d1d60-149">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-150">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1d60-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-152">Descreve a visibilidade dos consumidores para o recurso alocado.</span><span class="sxs-lookup"><span data-stu-id="d1d60-152">Describes the consumers' visibility to the allocated resource.</span></span> <span data-ttu-id="d1d60-153">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e é sempre definida como 3 (virtualizada).</span><span class="sxs-lookup"><span data-stu-id="d1d60-153">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="d1d60-154">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d1d60-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1d60-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-157">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="d1d60-157">A description of the object.</span></span> <span data-ttu-id="d1d60-158">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "dados de configuração do serviço de pulsação da Microsoft".</span><span class="sxs-lookup"><span data-stu-id="d1d60-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Heartbeat Service Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="d1d60-159">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d1d60-159">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1d60-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-162">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="d1d60-162">A display name for the object.</span></span> <span data-ttu-id="d1d60-163">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))e é sempre definida como "Heartbeat".</span><span class="sxs-lookup"><span data-stu-id="d1d60-163">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Heartbeat".</span></span> <span data-ttu-id="d1d60-164">A alteração dessa propriedade alterará a propriedade **ElementName** do derivativo [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) associado.</span><span class="sxs-lookup"><span data-stu-id="d1d60-164">Changing this property will change the **ElementName** property of the associated [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) derivative.</span></span>

<span data-ttu-id="d1d60-165">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="d1d60-165">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="d1d60-166">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d1d60-166">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-167">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1d60-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-169">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="d1d60-169">The enabled and disabled states of an element.</span></span>

<span data-ttu-id="d1d60-170">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="d1d60-170">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d1d60-171">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="d1d60-171">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d1d60-172">**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="d1d60-172">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1d60-173">**ErrorThreshold**</span><span class="sxs-lookup"><span data-stu-id="d1d60-173">**ErrorThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-174">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1d60-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-176">A configuração de inicialização de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="d1d60-176">An administrator's startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="d1d60-177">Essa propriedade é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="d1d60-177">This property is always set to 2 (Enabled).</span></span>

<span data-ttu-id="d1d60-178">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="d1d60-178">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="d1d60-179">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="d1d60-179">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-180">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1d60-180">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-182">Expõe uma atribuição específica para o host ou recursos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="d1d60-182">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="d1d60-183">Essa propriedade é herdada de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e sempre é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d1d60-183">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d1d60-184">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d1d60-184">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-185">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1d60-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-187">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="d1d60-187">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-188">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="d1d60-188">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d1d60-189">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) e é sempre definida como "Microsoft:*GUID* \\ *DeviceSpecificData*".</span><span class="sxs-lookup"><span data-stu-id="d1d60-189">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="d1d60-190">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="d1d60-190">**Interval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-191">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1d60-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-193">O intervalo, em milissegundos, entre tentativas de ping.</span><span class="sxs-lookup"><span data-stu-id="d1d60-193">The interval, in milliseconds, between ping attempts.</span></span> <span data-ttu-id="d1d60-194">Isso é sempre definido como 2000.</span><span class="sxs-lookup"><span data-stu-id="d1d60-194">This is always set to 2000.</span></span>

<span data-ttu-id="d1d60-195">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="d1d60-195">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="d1d60-196">**Latência**</span><span class="sxs-lookup"><span data-stu-id="d1d60-196">**Latency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-197">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1d60-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-199">A latência máxima esperada, em milissegundos, entre um ping de solicitação e uma resposta antes de uma determinada solicitação ser considerada descartada.</span><span class="sxs-lookup"><span data-stu-id="d1d60-199">The maximum expected latency, in milliseconds, between a request ping and a response before a given request is considered dropped.</span></span> <span data-ttu-id="d1d60-200">Essa propriedade é sempre definida como 1000.</span><span class="sxs-lookup"><span data-stu-id="d1d60-200">This property is always set to 1000.</span></span>

<span data-ttu-id="d1d60-201">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="d1d60-201">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="d1d60-202">**Limite**</span><span class="sxs-lookup"><span data-stu-id="d1d60-202">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-203">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d1d60-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-205">O limite superior ou a quantidade máxima de recursos que serão concedidos para essa alocação.</span><span class="sxs-lookup"><span data-stu-id="d1d60-205">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="d1d60-206">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e é sempre definida como 1.</span><span class="sxs-lookup"><span data-stu-id="d1d60-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="d1d60-207">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="d1d60-207">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-208">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1d60-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-210">Especifica como esse recurso é mapeado para recursos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="d1d60-210">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="d1d60-211">Essa propriedade é herdada de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e sempre é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d1d60-211">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d1d60-212">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="d1d60-212">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-213">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1d60-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-215">Uma cadeia de caracteres que descreve o tipo de recurso quando um valor bem definido não está disponível e a propriedade **ResourceType** tem o valor 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="d1d60-215">A string that describes the resource type when a well-defined value is not available and the **ResourceType** property has the value 1 (Other).</span></span> <span data-ttu-id="d1d60-216">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e é sempre definida como "componente de pulsação da Microsoft".</span><span class="sxs-lookup"><span data-stu-id="d1d60-216">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to "Microsoft Heartbeat Component".</span></span>

</dd> <dt>

<span data-ttu-id="d1d60-217">**Pai**</span><span class="sxs-lookup"><span data-stu-id="d1d60-217">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-218">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1d60-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-219">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-220">O pai do recurso.</span><span class="sxs-lookup"><span data-stu-id="d1d60-220">The parent of the resource.</span></span> <span data-ttu-id="d1d60-221">Essa propriedade é herdada de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e sempre é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d1d60-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d1d60-222">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="d1d60-222">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-223">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1d60-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-225">A ID do pool de recursos do qual o recurso está alocado.</span><span class="sxs-lookup"><span data-stu-id="d1d60-225">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="d1d60-226">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d1d60-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d1d60-227">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="d1d60-227">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-228">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d1d60-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-229">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-230">A quantidade de recursos com garantia disponível para essa alocação.</span><span class="sxs-lookup"><span data-stu-id="d1d60-230">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="d1d60-231">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e é sempre definida como 1.</span><span class="sxs-lookup"><span data-stu-id="d1d60-231">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="d1d60-232">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="d1d60-232">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-233">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1d60-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-234">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-235">Um subtipo específico de implementação para este recurso.</span><span class="sxs-lookup"><span data-stu-id="d1d60-235">An implementation specific subtype for this resource.</span></span> <span data-ttu-id="d1d60-236">Essa propriedade é herdada de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e sempre é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d1d60-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d1d60-237">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="d1d60-237">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-238">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1d60-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-239">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-240">O tipo de recurso que essa configuração de alocação representa.</span><span class="sxs-lookup"><span data-stu-id="d1d60-240">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="d1d60-241">Essa propriedade é herdada da classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e sempre é definida como 1 (outra).</span><span class="sxs-lookup"><span data-stu-id="d1d60-241">This property is inherited from the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class and is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="d1d60-242">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="d1d60-242">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-243">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d1d60-243">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-245">A quantidade de recursos apresentados ao consumidor.</span><span class="sxs-lookup"><span data-stu-id="d1d60-245">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="d1d60-246">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e é sempre definida como 1.</span><span class="sxs-lookup"><span data-stu-id="d1d60-246">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="d1d60-247">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="d1d60-247">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-248">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1d60-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-249">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-250">Especifica as unidades usadas pela propriedade **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="d1d60-250">Specifies the units used by the **VirtualQuantity** property.</span></span> <span data-ttu-id="d1d60-251">Por exemplo, se ResourceType = processador, o valor da propriedade **VirtualQuantityUnits** pode ser definido como "Count", indicando que o valor da propriedade **VirtualQuantity** é expresso como uma contagem.</span><span class="sxs-lookup"><span data-stu-id="d1d60-251">For example, if ResourceType=Processor, the value of the **VirtualQuantityUnits** property can be set to "count", indicating that the value of the **VirtualQuantity** property is expressed as a count.</span></span> <span data-ttu-id="d1d60-252">Se ResourceType = Memory, o valor da propriedade **VirtualQuantityUnits** poderá ser definido como "bytes \* 10 ^ 3", indicando que o valor da propriedade **VirtualQuantity** é expresso em kilobytes.</span><span class="sxs-lookup"><span data-stu-id="d1d60-252">If ResourceType=Memory, the value of the **VirtualQuantityUnits** property can be set to "bytes\*10^3", indicating that the value of the **VirtualQuantity** property is expressed in kilobytes.</span></span> <span data-ttu-id="d1d60-253">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e é sempre definida como "Count".</span><span class="sxs-lookup"><span data-stu-id="d1d60-253">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to "count".</span></span>

</dd> <dt>

<span data-ttu-id="d1d60-254">**Weight**</span><span class="sxs-lookup"><span data-stu-id="d1d60-254">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d60-255">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1d60-255">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1d60-256">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d60-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1d60-257">A prioridade relativa para essa alocação em relação a outras alocações do mesmo pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="d1d60-257">The relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="d1d60-258">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e é sempre definida como 0.</span><span class="sxs-lookup"><span data-stu-id="d1d60-258">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1d60-259">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1d60-259">Remarks</span></span>

<span data-ttu-id="d1d60-260">O acesso à classe **Msvm \_ HeartbeatComponentSettingData** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="d1d60-260">Access to the **Msvm\_HeartbeatComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d1d60-261">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d1d60-261">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1d60-262">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1d60-262">Requirements</span></span>



| <span data-ttu-id="d1d60-263">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1d60-263">Requirement</span></span> | <span data-ttu-id="d1d60-264">Valor</span><span class="sxs-lookup"><span data-stu-id="d1d60-264">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1d60-265">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1d60-265">Minimum supported client</span></span><br/> | <span data-ttu-id="d1d60-266">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d1d60-266">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d1d60-267">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1d60-267">Minimum supported server</span></span><br/> | <span data-ttu-id="d1d60-268">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d1d60-268">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d1d60-269">Namespace</span><span class="sxs-lookup"><span data-stu-id="d1d60-269">Namespace</span></span><br/>                | <span data-ttu-id="d1d60-270">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d1d60-270">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d1d60-271">MOF</span><span class="sxs-lookup"><span data-stu-id="d1d60-271">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1d60-272"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1d60-272"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1d60-273">DLL</span><span class="sxs-lookup"><span data-stu-id="d1d60-273">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1d60-274"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d1d60-274"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d1d60-275">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1d60-275">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1d60-276">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="d1d60-276">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="d1d60-277">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="d1d60-277">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="d1d60-278">**Msvm \_ HeartbeatComponentSettingData**</span><span class="sxs-lookup"><span data-stu-id="d1d60-278">**Msvm\_HeartbeatComponentSettingData**</span></span>](/previous-versions/windows/desktop/virtual/msvm-heartbeatcomponentsettingdata)
</dt> </dl>

 

