---
description: Representa o estado configurado de um adaptador Ethernet emulado.
ms.assetid: 8BFD69D8-65B6-4C6F-9972-BD2F3C4FB5B8
title: Classe Msvm_EmulatedEthernetPortSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EmulatedEthernetPortSettingData
- Msvm_EmulatedEthernetPortSettingData.Caption
- Msvm_EmulatedEthernetPortSettingData.Description
- Msvm_EmulatedEthernetPortSettingData.InstanceID
- Msvm_EmulatedEthernetPortSettingData.ElementName
- Msvm_EmulatedEthernetPortSettingData.ResourceType
- Msvm_EmulatedEthernetPortSettingData.OtherResourceType
- Msvm_EmulatedEthernetPortSettingData.ResourceSubType
- Msvm_EmulatedEthernetPortSettingData.PoolID
- Msvm_EmulatedEthernetPortSettingData.ConsumerVisibility
- Msvm_EmulatedEthernetPortSettingData.HostResource
- Msvm_EmulatedEthernetPortSettingData.AllocationUnits
- Msvm_EmulatedEthernetPortSettingData.VirtualQuantity
- Msvm_EmulatedEthernetPortSettingData.Reservation
- Msvm_EmulatedEthernetPortSettingData.Limit
- Msvm_EmulatedEthernetPortSettingData.Weight
- Msvm_EmulatedEthernetPortSettingData.AutomaticAllocation
- Msvm_EmulatedEthernetPortSettingData.AutomaticDeallocation
- Msvm_EmulatedEthernetPortSettingData.Parent
- Msvm_EmulatedEthernetPortSettingData.Connection
- Msvm_EmulatedEthernetPortSettingData.Address
- Msvm_EmulatedEthernetPortSettingData.MappingBehavior
- Msvm_EmulatedEthernetPortSettingData.AddressOnParent
- Msvm_EmulatedEthernetPortSettingData.VirtualQuantityUnits
- Msvm_EmulatedEthernetPortSettingData.DesiredVLANEndpointMode
- Msvm_EmulatedEthernetPortSettingData.OtherEndpointMode
- Msvm_EmulatedEthernetPortSettingData.StaticMacAddress
- Msvm_EmulatedEthernetPortSettingData.ClusterMonitored
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f80a1f14f7a5bd388aec747f19ef84ecf0a32b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827769"
---
# <a name="msvm_emulatedethernetportsettingdata-class"></a><span data-ttu-id="8cd4e-103">\_Classe Msvm EmulatedEthernetPortSettingData</span><span class="sxs-lookup"><span data-stu-id="8cd4e-103">Msvm\_EmulatedEthernetPortSettingData class</span></span>

<span data-ttu-id="8cd4e-104">Representa o estado configurado de um adaptador Ethernet emulado.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-104">Represents the configured state of an emulated Ethernet adapter.</span></span>

<span data-ttu-id="8cd4e-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cd4e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8cd4e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EmulatedEthernetPortSettingData : CIM_EthernetPortAllocationSettingData
{
  string  Caption = "Ethernet Port";
  string  Description = "Settings for the Microsoft Emulated Ethernet Port";
  string  InstanceID = "Microsoft:VMID\VDID\device-specific-data";
  string  ElementName = "Ethernet Port";
  uint16  ResourceType = 10;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft Emulated Ethernet Port";
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "Ports";
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
  uint16  DesiredVLANEndpointMode;
  string  OtherEndpointMode;
  boolean StaticMacAddress = TRUE;
  boolean ClusterMonitored = TRUE;
};
```

## <a name="members"></a><span data-ttu-id="8cd4e-107">Membros</span><span class="sxs-lookup"><span data-stu-id="8cd4e-107">Members</span></span>

<span data-ttu-id="8cd4e-108">A classe **Msvm \_ EmulatedEthernetPortSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8cd4e-108">The **Msvm\_EmulatedEthernetPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="8cd4e-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8cd4e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8cd4e-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8cd4e-110">Properties</span></span>

<span data-ttu-id="8cd4e-111">A classe **Msvm \_ EmulatedEthernetPortSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-111">The **Msvm\_EmulatedEthernetPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8cd4e-112">**Endereço**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-115">O endereço do recurso.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-115">The address of the resource.</span></span> <span data-ttu-id="8cd4e-116">Por exemplo, o endereço MAC de uma porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-116">For example, the MAC address of a Ethernet port.</span></span> <span data-ttu-id="8cd4e-117">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8cd4e-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="8cd4e-118">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="8cd4e-118">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-119">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-119">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-122">Descreve o endereço deste recurso no contexto do pai.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-122">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="8cd4e-123">As propriedades **pai** e **AddressOnParent** são usadas para descrever a relação do controlador, bem como a ordem dos dispositivos em um controlador.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-123">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="8cd4e-124">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8cd4e-124">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-125">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-125">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-128">As unidades de alocação usadas pelas propriedades **Reservation** e **Limit** .</span><span class="sxs-lookup"><span data-stu-id="8cd4e-128">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="8cd4e-129">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e é sempre definida como "portas".</span><span class="sxs-lookup"><span data-stu-id="8cd4e-129">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to "Ports".</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-130">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-130">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-131">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-133">Indica se o recurso será alocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-133">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="8cd4e-134">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e é sempre definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-134">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-135">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-135">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-136">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-138">Indica se o recurso será desalocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-138">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="8cd4e-139">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e é sempre definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-139">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-140">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-143">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-143">A short description of the object.</span></span> <span data-ttu-id="8cd4e-144">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "porta Ethernet".</span><span class="sxs-lookup"><span data-stu-id="8cd4e-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-145">**ClusterMonitored**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-145">**ClusterMonitored**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-146">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-148">Indica se este adaptador Ethernet é monitorado por um cluster.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-148">Indicates whether this ethernet adapter is monitored by a cluster.</span></span> <span data-ttu-id="8cd4e-149">Essa propriedade assume true como padrão se não estiver configurada.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-149">This property defaults to true if not configured.</span></span>

<span data-ttu-id="8cd4e-150">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="8cd4e-150">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="8cd4e-151">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-151">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-152">**Conexão**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-152">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-153">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-155">A coisa à qual esse recurso está conectado.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-155">The thing to which this resource is connected.</span></span> <span data-ttu-id="8cd4e-156">Por exemplo, uma rede nomeada ou porta de comutador.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-156">For example, a named network or switch port.</span></span> <span data-ttu-id="8cd4e-157">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8cd4e-157">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="8cd4e-158">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="8cd4e-158">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-159">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-159">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-160">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-162">Descreve a visibilidade dos consumidores para o recurso alocado.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-162">Describes the consumers visibility to the allocated resource.</span></span> <span data-ttu-id="8cd4e-163">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e é sempre definida como 3 (virtualizada).</span><span class="sxs-lookup"><span data-stu-id="8cd4e-163">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-164">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-164">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-165">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-167">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="8cd4e-167">A description of the object.</span></span> <span data-ttu-id="8cd4e-168">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações para a porta Ethernet emulada da Microsoft".</span><span class="sxs-lookup"><span data-stu-id="8cd4e-168">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Settings for the Microsoft Emulated Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-169">**DesiredVLANEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-169">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-170">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-172">O modo de configuração desejado para o ponto de extremidade de VLAN.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-172">The desired configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="8cd4e-173">Essa propriedade é usada para definir o valor da propriedade **OperationalEndpointMode** inicial na instância da classe [**Msvm \_ VLANEndpoint**](msvm-vlanendpoint.md) associada à porta Ethernet de destino.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-173">This property is used to set the initial **OperationalEndpointMode** property value in the instance of [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) class associated with the targeted Ethernet port.</span></span> <span data-ttu-id="8cd4e-174">Consulte a propriedade **OperationalEndpointMode** da classe **Msvm \_ VLANEndpoint** para obter os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-174">See the **OperationalEndpointMode** property of the **Msvm\_VLANEndpoint** class for possible values.</span></span> <span data-ttu-id="8cd4e-175">Essa propriedade é herdada do **CIM \_ EthernetPortAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-175">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-176">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-176">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-179">O nome de exibição configurável pelo usuário para o dispositivo ao qual essa instância do RASD está associada.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-179">The user-configurable display name for the device this RASD instance is associated with.</span></span> <span data-ttu-id="8cd4e-180">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))e é definida como "porta Ethernet".</span><span class="sxs-lookup"><span data-stu-id="8cd4e-180">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is set to "Ethernet Port".</span></span> <span data-ttu-id="8cd4e-181">A alteração dessa propriedade irá alterar o nome do elemento do derivado do dispositivo lógico associado.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-181">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="8cd4e-182">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="8cd4e-182">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-183">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-183">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-184">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-184">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-186">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-186">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-187">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-187">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-188">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-190">Dentro do escopo do namespace de instanciação, a **InstanceId** identifica de forma opaca e exclusiva uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-190">Within the scope of the instantiating namespace, **InstanceID** opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8cd4e-191">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))e é sempre definida como "Microsoft:*VMID* \\ *VDID* \\ *Device-specific-data*".</span><span class="sxs-lookup"><span data-stu-id="8cd4e-191">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*VMID*\\*VDID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-192">**Limite**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-192">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-193">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-193">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-195">O limite superior ou a quantidade máxima de recursos que serão concedidos para essa alocação.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-195">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="8cd4e-196">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e é sempre definida como 1.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-196">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-197">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-197">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-198">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-200">Especifica como esse recurso é mapeado para recursos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-200">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="8cd4e-201">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-201">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-202">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-202">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-203">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-205">Uma cadeia de caracteres que descreve o tipo de modelo de ponto de extremidade de VLAN com suporte deste ponto de extremidade de VLAN.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-205">A string that describes the type of VLAN endpoint model that is supported by this VLAN endpoint.</span></span> <span data-ttu-id="8cd4e-206">Essa propriedade só é usada quando a propriedade **DesiredVLANEndpointMode** é definida como 1 (Other).</span><span class="sxs-lookup"><span data-stu-id="8cd4e-206">This property is only used when the **DesiredVLANEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="8cd4e-207">Essa propriedade deve ser definida como **NULL** quando a propriedade **DesiredVLANEndpointMode** é qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-207">This property should be set to **Null** when the **DesiredVLANEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="8cd4e-208">Essa propriedade é herdada do **CIM \_ EthernetPortAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-208">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-209">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-209">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-212">Uma cadeia de caracteres que descreve o tipo de recurso quando um valor bem definido não está disponível e ResourceType é definido como 0 ("other").</span><span class="sxs-lookup"><span data-stu-id="8cd4e-212">A string that describes the resource type when a well-defined value is not available and ResourceType is set to 0 ("Other").</span></span> <span data-ttu-id="8cd4e-213">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e não é usada.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-214">**Pai**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-214">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-215">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-216">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-217">O pai do recurso.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-217">The parent of the resource.</span></span> <span data-ttu-id="8cd4e-218">Por exemplo, um controlador para a alocação atual.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-218">For example, a controller for the current allocation.</span></span> <span data-ttu-id="8cd4e-219">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8cd4e-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-220">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-220">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-221">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-223">O pool no qual o recurso está alocado no momento ou o pool no qual o recurso será alocado quando a alocação ocorrer.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-223">The pool the resource is currently allocated from, or the pool the resource will be allocated from when the allocation occurs.</span></span> <span data-ttu-id="8cd4e-224">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8cd4e-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-225">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-225">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-226">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-226">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-227">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-228">A quantidade de recursos com garantia disponível para essa alocação.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-228">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="8cd4e-229">Em sistemas que dão suporte ao comprometimento excessivo de recursos, esse valor normalmente é usado para o controle de admissão para impedir que uma alocação seja aceita.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-229">On systems that support over-commitment of resources, this value is typically used for admission control to prevent an allocation from being accepted.</span></span> <span data-ttu-id="8cd4e-230">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e é sempre definida como 1.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-230">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-231">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-231">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-232">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-234">Uma cadeia de caracteres que descreve um subtipo específico de implementação para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-234">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="8cd4e-235">Por exemplo, isso pode ser usado para distinguir modelos diferentes do mesmo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-235">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="8cd4e-236">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e é sempre definida como "porta de Ethernet emulada da Microsoft".</span><span class="sxs-lookup"><span data-stu-id="8cd4e-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to "Microsoft Emulated Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-237">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-237">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-238">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-239">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-240">O tipo de recurso ao qual essa configuração se aplica.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-240">The type of resource this setting applies to.</span></span> <span data-ttu-id="8cd4e-241">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e é sempre definida como 10 (adaptador Ethernet).</span><span class="sxs-lookup"><span data-stu-id="8cd4e-241">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 10 (Ethernet Adapter).</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-242">**StaticMacAddress**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-242">**StaticMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-243">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-245">Indica se um endereço MAC estático deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-245">Indicates whether to use a static MAC address.</span></span>

<span data-ttu-id="8cd4e-246">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="8cd4e-246">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-247">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-247">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-248">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-248">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-249">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-250">A quantidade de recursos apresentados ao consumidor.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-250">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="8cd4e-251">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e é sempre definida como 1.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-251">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-252">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-252">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-253">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-254">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-255">Especifica a unidade de medida para essa alocação de recursos.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-255">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="8cd4e-256">O valor dessa propriedade deve ser um valor válido do qualificador de unidades programáticas, conforme definido no anexo C. 1 de DSP0004 V 2.5 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-256">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="8cd4e-257">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8cd4e-257">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8cd4e-258">**Weight**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-258">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cd4e-259">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-259">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8cd4e-260">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8cd4e-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cd4e-261">Uma prioridade relativa para essa alocação em relação a outras alocações do mesmo ResourcePool.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-261">A relative priority for this allocation in relation to other allocations from the same ResourcePool.</span></span> <span data-ttu-id="8cd4e-262">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e é sempre definida como 0.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-262">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8cd4e-263">Comentários</span><span class="sxs-lookup"><span data-stu-id="8cd4e-263">Remarks</span></span>

<span data-ttu-id="8cd4e-264">O acesso à classe **Msvm \_ EmulatedEthernetPortSettingData** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="8cd4e-264">Access to the **Msvm\_EmulatedEthernetPortSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="8cd4e-265">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="8cd4e-265">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="8cd4e-266">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8cd4e-266">Examples</span></span>

<span data-ttu-id="8cd4e-267">Consulte [consultando objetos de rede](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8cd4e-267">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8cd4e-268">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cd4e-268">Requirements</span></span>



| <span data-ttu-id="8cd4e-269">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cd4e-269">Requirement</span></span> | <span data-ttu-id="8cd4e-270">Valor</span><span class="sxs-lookup"><span data-stu-id="8cd4e-270">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cd4e-271">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cd4e-271">Minimum supported client</span></span><br/> | <span data-ttu-id="8cd4e-272">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8cd4e-272">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8cd4e-273">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cd4e-273">Minimum supported server</span></span><br/> | <span data-ttu-id="8cd4e-274">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8cd4e-274">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8cd4e-275">Namespace</span><span class="sxs-lookup"><span data-stu-id="8cd4e-275">Namespace</span></span><br/>                | <span data-ttu-id="8cd4e-276">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="8cd4e-276">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8cd4e-277">MOF</span><span class="sxs-lookup"><span data-stu-id="8cd4e-277">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8cd4e-278"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8cd4e-278"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8cd4e-279">DLL</span><span class="sxs-lookup"><span data-stu-id="8cd4e-279">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cd4e-280"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8cd4e-280"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8cd4e-281">Confira também</span><span class="sxs-lookup"><span data-stu-id="8cd4e-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cd4e-282">**\_ETHERNETPORTALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-282">**CIM\_EthernetPortAllocationSettingData**</span></span>](cim-ethernetportallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="8cd4e-283">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="8cd4e-283">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

