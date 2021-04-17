---
description: Representa o estado configurado de um adaptador Ethernet sintético.
ms.assetid: BE895BAF-7766-43A2-9659-3ABA97A16134
title: Classe Msvm_SyntheticEthernetPortSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticEthernetPortSettingData
- Msvm_SyntheticEthernetPortSettingData.InstanceID
- Msvm_SyntheticEthernetPortSettingData.Caption
- Msvm_SyntheticEthernetPortSettingData.Description
- Msvm_SyntheticEthernetPortSettingData.ElementName
- Msvm_SyntheticEthernetPortSettingData.ResourceType
- Msvm_SyntheticEthernetPortSettingData.OtherResourceType
- Msvm_SyntheticEthernetPortSettingData.ResourceSubType
- Msvm_SyntheticEthernetPortSettingData.PoolID
- Msvm_SyntheticEthernetPortSettingData.ConsumerVisibility
- Msvm_SyntheticEthernetPortSettingData.HostResource
- Msvm_SyntheticEthernetPortSettingData.AllocationUnits
- Msvm_SyntheticEthernetPortSettingData.VirtualQuantity
- Msvm_SyntheticEthernetPortSettingData.Reservation
- Msvm_SyntheticEthernetPortSettingData.Limit
- Msvm_SyntheticEthernetPortSettingData.Weight
- Msvm_SyntheticEthernetPortSettingData.AutomaticAllocation
- Msvm_SyntheticEthernetPortSettingData.AutomaticDeallocation
- Msvm_SyntheticEthernetPortSettingData.Parent
- Msvm_SyntheticEthernetPortSettingData.Connection
- Msvm_SyntheticEthernetPortSettingData.Address
- Msvm_SyntheticEthernetPortSettingData.MappingBehavior
- Msvm_SyntheticEthernetPortSettingData.AddressOnParent
- Msvm_SyntheticEthernetPortSettingData.VirtualQuantityUnits
- Msvm_SyntheticEthernetPortSettingData.DesiredVLANEndpointMode
- Msvm_SyntheticEthernetPortSettingData.OtherEndpointMode
- Msvm_SyntheticEthernetPortSettingData.VirtualSystemIdentifiers
- Msvm_SyntheticEthernetPortSettingData.DeviceNamingEnabled
- Msvm_SyntheticEthernetPortSettingData.AllowPacketDirect
- Msvm_SyntheticEthernetPortSettingData.StaticMacAddress
- Msvm_SyntheticEthernetPortSettingData.ClusterMonitored
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5b31b02782c0f215f70f3bb5d2767b01294c7261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782350"
---
# <a name="msvm_syntheticethernetportsettingdata-class"></a><span data-ttu-id="8428a-103">\_Classe Msvm SyntheticEthernetPortSettingData</span><span class="sxs-lookup"><span data-stu-id="8428a-103">Msvm\_SyntheticEthernetPortSettingData class</span></span>

<span data-ttu-id="8428a-104">Representa o estado configurado de um adaptador Ethernet sintético.</span><span class="sxs-lookup"><span data-stu-id="8428a-104">Represents the configured state of a synthetic Ethernet adapter.</span></span>

<span data-ttu-id="8428a-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8428a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8428a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8428a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticEthernetPortSettingData : CIM_EthernetPortAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Ethernet Port Default Settings";
  string  Description = "Describes the default settings for the virtual Ethernet port resources.";
  string  ElementName;
  uint16  ResourceType = 10;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Synthetic Ethernet Port";
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
  uint16  DesiredVLANEndpointMode;
  string  OtherEndpointMode;
  string  VirtualSystemIdentifiers[];
  boolean DeviceNamingEnabled = FALSE;
  boolean AllowPacketDirect = FALSE;
  boolean StaticMacAddress = False;
  boolean ClusterMonitored = TRUE;
};
```

## <a name="members"></a><span data-ttu-id="8428a-107">Membros</span><span class="sxs-lookup"><span data-stu-id="8428a-107">Members</span></span>

<span data-ttu-id="8428a-108">A classe **Msvm \_ SyntheticEthernetPortSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8428a-108">The **Msvm\_SyntheticEthernetPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="8428a-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8428a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8428a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8428a-110">Properties</span></span>

<span data-ttu-id="8428a-111">A classe **Msvm \_ SyntheticEthernetPortSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8428a-111">The **Msvm\_SyntheticEthernetPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8428a-112">**Endereço**</span><span class="sxs-lookup"><span data-stu-id="8428a-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8428a-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-115">O endereço do recurso.</span><span class="sxs-lookup"><span data-stu-id="8428a-115">The address of the resource.</span></span> <span data-ttu-id="8428a-116">Por exemplo, o endereço MAC de uma porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="8428a-116">For example, the MAC address of a Ethernet port.</span></span> <span data-ttu-id="8428a-117">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8428a-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8428a-118">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="8428a-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8428a-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-121">Descreve o endereço deste recurso no contexto do pai.</span><span class="sxs-lookup"><span data-stu-id="8428a-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="8428a-122">As propriedades **pai** e **AddressOnParent** são usadas para descrever a relação do controlador, bem como a ordem dos dispositivos em um controlador.</span><span class="sxs-lookup"><span data-stu-id="8428a-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="8428a-123">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8428a-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8428a-124">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="8428a-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8428a-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-127">As unidades de alocação usadas pelas propriedades **Reservation** e **Limit** .</span><span class="sxs-lookup"><span data-stu-id="8428a-127">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="8428a-128">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8428a-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8428a-129">**AllowPacketDirect**</span><span class="sxs-lookup"><span data-stu-id="8428a-129">**AllowPacketDirect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-130">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8428a-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-131">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8428a-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8428a-132">Indica se a projeção de PacketDirect está habilitada para a VM.</span><span class="sxs-lookup"><span data-stu-id="8428a-132">Indicates if PacketDirect projection is enabled for the VM.</span></span>

> [!Note]  
> <span data-ttu-id="8428a-133">Adicionado no Windows 10, versão 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="8428a-133">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="8428a-134">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="8428a-134">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-135">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8428a-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-137">Indica se o recurso será alocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8428a-137">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="8428a-138">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8428a-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8428a-139">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="8428a-139">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-140">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8428a-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-142">Indica se o recurso será desalocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8428a-142">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="8428a-143">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8428a-143">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8428a-144">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="8428a-144">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8428a-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-147">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="8428a-147">A short description of the object.</span></span> <span data-ttu-id="8428a-148">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8428a-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8428a-149">**ClusterMonitored**</span><span class="sxs-lookup"><span data-stu-id="8428a-149">**ClusterMonitored**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-150">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8428a-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-152">Indica se este adaptador Ethernet é monitorado por um cluster.</span><span class="sxs-lookup"><span data-stu-id="8428a-152">Indicates whether this ethernet adapter is monitored by a cluster.</span></span> <span data-ttu-id="8428a-153">Essa propriedade assume true como padrão se não estiver configurada.</span><span class="sxs-lookup"><span data-stu-id="8428a-153">This property defaults to true if not configured.</span></span>

<span data-ttu-id="8428a-154">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="8428a-154">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="8428a-155">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="8428a-155">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="8428a-156">**Conexão**</span><span class="sxs-lookup"><span data-stu-id="8428a-156">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-157">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8428a-157">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8428a-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-159">A coisa à qual esse recurso está conectado.</span><span class="sxs-lookup"><span data-stu-id="8428a-159">The thing to which this resource is connected.</span></span> <span data-ttu-id="8428a-160">Por exemplo, uma rede nomeada ou porta de comutador.</span><span class="sxs-lookup"><span data-stu-id="8428a-160">For example, a named network or switch port.</span></span> <span data-ttu-id="8428a-161">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8428a-161">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8428a-162">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="8428a-162">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-163">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8428a-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-165">A visibilidade dos consumidores para o recurso alocado.</span><span class="sxs-lookup"><span data-stu-id="8428a-165">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="8428a-166">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e é sempre definida como 3 (virtualizada).</span><span class="sxs-lookup"><span data-stu-id="8428a-166">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="8428a-167">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8428a-167">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8428a-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-170">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="8428a-170">A description of the object.</span></span> <span data-ttu-id="8428a-171">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8428a-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8428a-172">**DesiredVLANEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="8428a-172">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-173">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8428a-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-175">O modo de configuração desejado para o ponto de extremidade de VLAN.</span><span class="sxs-lookup"><span data-stu-id="8428a-175">The desired configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="8428a-176">Essa propriedade é usada para definir o valor da propriedade **OperationalEndpointMode** inicial na instância da classe [**Msvm \_ VLANEndpoint**](msvm-vlanendpoint.md) associada à porta Ethernet de destino.</span><span class="sxs-lookup"><span data-stu-id="8428a-176">This property is used to set the initial **OperationalEndpointMode** property value in the instance of the [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) class associated with the targeted Ethernet port.</span></span> <span data-ttu-id="8428a-177">Consulte a propriedade **OperationalEndpointMode** da classe **Msvm \_ VLANEndpoint** para obter os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="8428a-177">See the **OperationalEndpointMode** property of the **Msvm\_VLANEndpoint** class for possible values.</span></span> <span data-ttu-id="8428a-178">Essa propriedade é herdada do **CIM \_ EthernetPortAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="8428a-178">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="8428a-179">**DeviceNamingEnabled**</span><span class="sxs-lookup"><span data-stu-id="8428a-179">**DeviceNamingEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-180">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8428a-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-182">Indica se este adaptador Ethernet dá suporte à nomenclatura de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="8428a-182">Indicates whether this ethernet adapter supports device naming.</span></span>

<span data-ttu-id="8428a-183">Esta é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyVirtualSystemResources**](https://www.bing.com/search?q=**ModifyVirtualSystemResources**) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="8428a-183">This is a read-only property, but it can be changed using the [**ModifyVirtualSystemResources**](https://www.bing.com/search?q=**ModifyVirtualSystemResources**) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="8428a-184">Adicionado ao Windows 10 e ao Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="8428a-184">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="8428a-185">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8428a-185">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-186">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8428a-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-188">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="8428a-188">A short description of the object.</span></span> <span data-ttu-id="8428a-189">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8428a-189">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8428a-190">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="8428a-190">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-191">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8428a-191">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8428a-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-193">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8428a-193">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8428a-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8428a-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-195">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8428a-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8428a-197">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="8428a-197">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8428a-198">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="8428a-198">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8428a-199">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8428a-199">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8428a-200">**Limite**</span><span class="sxs-lookup"><span data-stu-id="8428a-200">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-201">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8428a-201">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-203">O limite superior ou a quantidade máxima de recursos que serão concedidos para essa alocação.</span><span class="sxs-lookup"><span data-stu-id="8428a-203">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="8428a-204">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8428a-204">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8428a-205">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="8428a-205">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-206">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8428a-206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-208">Especifica como esse recurso é mapeado para recursos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="8428a-208">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="8428a-209">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8428a-209">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8428a-210">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="8428a-210">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-211">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8428a-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-213">Uma cadeia de caracteres que descreve o tipo de modelo de ponto de extremidade de VLAN com suporte deste ponto de extremidade de VLAN.</span><span class="sxs-lookup"><span data-stu-id="8428a-213">A string that describes the type of VLAN endpoint model that is supported by this VLAN endpoint.</span></span> <span data-ttu-id="8428a-214">Essa propriedade só é usada quando a propriedade **DesiredVLANEndpointMode** é definida como 1 (Other).</span><span class="sxs-lookup"><span data-stu-id="8428a-214">This property is only used when the **DesiredVLANEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="8428a-215">Essa propriedade deve ser definida como **NULL** quando a propriedade **DesiredVLANEndpointMode** é qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="8428a-215">This property should be set to **Null** when the **DesiredVLANEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="8428a-216">Essa propriedade é herdada do **CIM \_ EthernetPortAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="8428a-216">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="8428a-217">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="8428a-217">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-218">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8428a-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-219">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-220">Uma cadeia de caracteres que descreve o tipo de recurso quando um valor bem definido não está disponível e **ResourceType** é definido como "other" (0).</span><span class="sxs-lookup"><span data-stu-id="8428a-220">A string that describes the resource type when a well-defined value is not available and **ResourceType** is set to "Other" (0).</span></span> <span data-ttu-id="8428a-221">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e não é usada.</span><span class="sxs-lookup"><span data-stu-id="8428a-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8428a-222">**Pai**</span><span class="sxs-lookup"><span data-stu-id="8428a-222">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-223">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8428a-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-225">O pai do recurso.</span><span class="sxs-lookup"><span data-stu-id="8428a-225">The parent of the resource.</span></span> <span data-ttu-id="8428a-226">Por exemplo, um controlador para a alocação atual.</span><span class="sxs-lookup"><span data-stu-id="8428a-226">For example, a controller for the current allocation.</span></span> <span data-ttu-id="8428a-227">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8428a-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8428a-228">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="8428a-228">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-229">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8428a-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-230">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-231">O pool no qual o recurso está alocado no momento ou a qual pool o recurso será alocado quando a alocação ocorrer.</span><span class="sxs-lookup"><span data-stu-id="8428a-231">The pool the resource is currently allocated from, or which pool the resource will be allocated from when the allocation occurs.</span></span> <span data-ttu-id="8428a-232">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8428a-232">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8428a-233">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="8428a-233">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-234">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8428a-234">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-235">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-236">A quantidade de recursos com garantia disponível para essa alocação.</span><span class="sxs-lookup"><span data-stu-id="8428a-236">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="8428a-237">Em sistemas que dão suporte ao comprometimento excessivo de recursos, esse valor normalmente é usado para o controle de admissão para impedir que uma alocação seja aceita.</span><span class="sxs-lookup"><span data-stu-id="8428a-237">On systems that support over-commitment of resources, this value is typically used for admission control to prevent an allocation from being accepted.</span></span> <span data-ttu-id="8428a-238">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8428a-238">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8428a-239">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="8428a-239">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-240">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8428a-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-242">Uma cadeia de caracteres que descreve um subtipo específico de implementação para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="8428a-242">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="8428a-243">Por exemplo, isso pode ser usado para distinguir modelos diferentes do mesmo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="8428a-243">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="8428a-244">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8428a-244">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8428a-245">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="8428a-245">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-246">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8428a-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-247">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-248">O tipo de recurso ao qual essa configuração se aplica.</span><span class="sxs-lookup"><span data-stu-id="8428a-248">The type of resource this setting applies to.</span></span> <span data-ttu-id="8428a-249">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e é sempre definida como 10 (adaptador Ethernet).</span><span class="sxs-lookup"><span data-stu-id="8428a-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 10 (Ethernet Adapter).</span></span>

</dd> <dt>

<span data-ttu-id="8428a-250">**StaticMacAddress**</span><span class="sxs-lookup"><span data-stu-id="8428a-250">**StaticMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-251">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8428a-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-253">Especifica se o endereço MAC é estático.</span><span class="sxs-lookup"><span data-stu-id="8428a-253">Specifies if the MAC address is static.</span></span>

</dd> <dt>

<span data-ttu-id="8428a-254">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="8428a-254">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-255">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8428a-255">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-256">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-257">A quantidade de recursos apresentados ao consumidor.</span><span class="sxs-lookup"><span data-stu-id="8428a-257">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="8428a-258">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8428a-258">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8428a-259">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="8428a-259">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-260">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8428a-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-261">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-262">Especifica a unidade de medida para a propriedade **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="8428a-262">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="8428a-263">O valor dessa propriedade deve ser um valor válido do qualificador de unidades programáticas, conforme definido no anexo C. 1 de DSP0004 V 2.5 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="8428a-263">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="8428a-264">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8428a-264">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8428a-265">**VirtualSystemIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="8428a-265">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-266">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8428a-266">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8428a-267">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8428a-268">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="8428a-268">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="8428a-269">Uma matriz de cadeia de caracteres de identificadores deste recurso apresentada ao sistema operacional da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8428a-269">A string array of identifiers of this resource presented to the virtual machine's operating system.</span></span> <span data-ttu-id="8428a-270">Os índices e valores por índice são definidos por recurso (ou seja, para cada valor de propriedade **ResourceType** enumerado).</span><span class="sxs-lookup"><span data-stu-id="8428a-270">The indexes and values per index are defined on a per resource basis (that is, for each enumerated **ResourceType** property value).</span></span>

</dd> <dt>

<span data-ttu-id="8428a-271">**Weight**</span><span class="sxs-lookup"><span data-stu-id="8428a-271">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8428a-272">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8428a-272">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8428a-273">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8428a-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8428a-274">Uma prioridade relativa para essa alocação em relação a outras alocações do mesmo pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="8428a-274">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="8428a-275">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8428a-275">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8428a-276">Comentários</span><span class="sxs-lookup"><span data-stu-id="8428a-276">Remarks</span></span>

<span data-ttu-id="8428a-277">O acesso à classe **Msvm \_ SyntheticEthernetPortSettingData** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="8428a-277">Access to the **Msvm\_SyntheticEthernetPortSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="8428a-278">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="8428a-278">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="8428a-279">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8428a-279">Examples</span></span>

<span data-ttu-id="8428a-280">Consulte [consultando objetos de rede](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8428a-280">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8428a-281">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8428a-281">Requirements</span></span>



| <span data-ttu-id="8428a-282">Requisito</span><span class="sxs-lookup"><span data-stu-id="8428a-282">Requirement</span></span> | <span data-ttu-id="8428a-283">Valor</span><span class="sxs-lookup"><span data-stu-id="8428a-283">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8428a-284">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8428a-284">Minimum supported client</span></span><br/> | <span data-ttu-id="8428a-285">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8428a-285">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8428a-286">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8428a-286">Minimum supported server</span></span><br/> | <span data-ttu-id="8428a-287">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8428a-287">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8428a-288">Namespace</span><span class="sxs-lookup"><span data-stu-id="8428a-288">Namespace</span></span><br/>                | <span data-ttu-id="8428a-289">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="8428a-289">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8428a-290">MOF</span><span class="sxs-lookup"><span data-stu-id="8428a-290">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8428a-291"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8428a-291"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8428a-292">DLL</span><span class="sxs-lookup"><span data-stu-id="8428a-292">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8428a-293"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8428a-293"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8428a-294">Confira também</span><span class="sxs-lookup"><span data-stu-id="8428a-294">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8428a-295">**\_ETHERNETPORTALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="8428a-295">**CIM\_EthernetPortAllocationSettingData**</span></span>](cim-ethernetportallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="8428a-296">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="8428a-296">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

