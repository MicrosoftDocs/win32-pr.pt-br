---
description: Representa uma solicitação de alocação para uma porta de comutador estática ou dinâmica ou representa a configuração ativa de uma porta de comutador estática ou dinâmica atualmente alocada.
ms.assetid: ef70b72f-75a0-448e-a648-6a28c12f0da1
title: Classe Msvm_EthernetPortAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortAllocationSettingData
- Msvm_EthernetPortAllocationSettingData.InstanceID
- Msvm_EthernetPortAllocationSettingData.Caption
- Msvm_EthernetPortAllocationSettingData.Description
- Msvm_EthernetPortAllocationSettingData.ElementName
- Msvm_EthernetPortAllocationSettingData.ResourceType
- Msvm_EthernetPortAllocationSettingData.OtherResourceType
- Msvm_EthernetPortAllocationSettingData.ResourceSubType
- Msvm_EthernetPortAllocationSettingData.PoolID
- Msvm_EthernetPortAllocationSettingData.ConsumerVisibility
- Msvm_EthernetPortAllocationSettingData.HostResource
- Msvm_EthernetPortAllocationSettingData.AllocationUnits
- Msvm_EthernetPortAllocationSettingData.VirtualQuantity
- Msvm_EthernetPortAllocationSettingData.Reservation
- Msvm_EthernetPortAllocationSettingData.Limit
- Msvm_EthernetPortAllocationSettingData.Weight
- Msvm_EthernetPortAllocationSettingData.AutomaticAllocation
- Msvm_EthernetPortAllocationSettingData.AutomaticDeallocation
- Msvm_EthernetPortAllocationSettingData.Parent
- Msvm_EthernetPortAllocationSettingData.Connection
- Msvm_EthernetPortAllocationSettingData.Address
- Msvm_EthernetPortAllocationSettingData.MappingBehavior
- Msvm_EthernetPortAllocationSettingData.AddressOnParent
- Msvm_EthernetPortAllocationSettingData.VirtualQuantityUnits
- Msvm_EthernetPortAllocationSettingData.DesiredVLANEndpointMode
- Msvm_EthernetPortAllocationSettingData.OtherEndpointMode
- Msvm_EthernetPortAllocationSettingData.EnabledState
- Msvm_EthernetPortAllocationSettingData.LastKnownSwitchName
- Msvm_EthernetPortAllocationSettingData.RequiredFeatures
- Msvm_EthernetPortAllocationSettingData.RequiredFeatureHints
- Msvm_EthernetPortAllocationSettingData.TestReplicaPoolID
- Msvm_EthernetPortAllocationSettingData.TestReplicaSwitchName
- Msvm_EthernetPortAllocationSettingData.CompartmentGuid
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a310daf30127aec5069efcf7ca4fd5ead9277e6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105767639"
---
# <a name="msvm_ethernetportallocationsettingdata-class"></a><span data-ttu-id="d8f20-103">\_Classe Msvm EthernetPortAllocationSettingData</span><span class="sxs-lookup"><span data-stu-id="d8f20-103">Msvm\_EthernetPortAllocationSettingData class</span></span>

<span data-ttu-id="d8f20-104">Representa uma solicitação de alocação para uma porta de comutador estática ou dinâmica ou representa a configuração ativa de uma porta de comutador estática ou dinâmica atualmente alocada.</span><span class="sxs-lookup"><span data-stu-id="d8f20-104">Represents an allocation request for a static or dynamic switch port, or represents the active configuration of a currently allocated static or dynamic switch port.</span></span> <span data-ttu-id="d8f20-105">Uma solicitação de alocação para uma porta de comutador dinâmico também é conhecida como uma solicitação de conexão.</span><span class="sxs-lookup"><span data-stu-id="d8f20-105">An allocation request for a dynamic switch port is also known as a connection request.</span></span>

<span data-ttu-id="d8f20-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d8f20-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8f20-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8f20-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortAllocationSettingData : CIM_EthernetPortAllocationSettingData
{
  string  InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string  Caption = "Ethernet Switch Port Settings";
  string  Description = "Ethernet Switch Port Settings";
  string  ElementName;
  uint16  ResourceType = 33;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight = 0;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint16  DesiredVLANEndpointMode;
  string  OtherEndpointMode;
  uint16  EnabledState;
  string  LastKnownSwitchName;
  string  RequiredFeatures[];
  string  RequiredFeatureHints[];
  string  TestReplicaPoolID;
  string  TestReplicaSwitchName;
  string  CompartmentGuid;
};
```

## <a name="members"></a><span data-ttu-id="d8f20-108">Membros</span><span class="sxs-lookup"><span data-stu-id="d8f20-108">Members</span></span>

<span data-ttu-id="d8f20-109">A classe **Msvm \_ EthernetPortAllocationSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d8f20-109">The **Msvm\_EthernetPortAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d8f20-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d8f20-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d8f20-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d8f20-111">Properties</span></span>

<span data-ttu-id="d8f20-112">A classe **Msvm \_ EthernetPortAllocationSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d8f20-112">The **Msvm\_EthernetPortAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d8f20-113">**Endereço**</span><span class="sxs-lookup"><span data-stu-id="d8f20-113">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d8f20-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-116">O endereço do recurso.</span><span class="sxs-lookup"><span data-stu-id="d8f20-116">The address of the resource.</span></span> <span data-ttu-id="d8f20-117">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8f20-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-118">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="d8f20-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d8f20-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-121">Descreve o endereço deste recurso no contexto do pai.</span><span class="sxs-lookup"><span data-stu-id="d8f20-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="d8f20-122">As propriedades **pai** e **AddressOnParent** são usadas para descrever a relação do controlador, bem como a ordem dos dispositivos em um controlador.</span><span class="sxs-lookup"><span data-stu-id="d8f20-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="d8f20-123">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8f20-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-124">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="d8f20-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d8f20-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-127">A unidade de alocação usada pelas propriedades **Reservation** e **Limit** .</span><span class="sxs-lookup"><span data-stu-id="d8f20-127">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="d8f20-128">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8f20-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-129">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="d8f20-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-130">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d8f20-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-132">Indica se o recurso será alocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="d8f20-132">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="d8f20-133">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8f20-133">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-134">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="d8f20-134">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-135">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d8f20-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-137">Indica se o recurso será desalocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="d8f20-137">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="d8f20-138">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8f20-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-139">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="d8f20-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d8f20-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-142">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="d8f20-142">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-143">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="d8f20-143">A short description of the object.</span></span> <span data-ttu-id="d8f20-144">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações de porta do comutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="d8f20-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-145">**CompartmentGuid**</span><span class="sxs-lookup"><span data-stu-id="d8f20-145">**CompartmentGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d8f20-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-147">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d8f20-147">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-148">Essa propriedade especifica o compartimento de rede de destino para a porta.</span><span class="sxs-lookup"><span data-stu-id="d8f20-148">This property specifies the target network compartment for the port.</span></span> <span data-ttu-id="d8f20-149">Só há suporte para adaptadores internos.</span><span class="sxs-lookup"><span data-stu-id="d8f20-149">It is only supported for internal adapters.</span></span>

> [!Note]  
> <span data-ttu-id="d8f20-150">Propriedade adicionada no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d8f20-150">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="d8f20-151">**Conexão**</span><span class="sxs-lookup"><span data-stu-id="d8f20-151">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-152">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d8f20-152">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-154">O dispositivo ao qual esse recurso está conectado.</span><span class="sxs-lookup"><span data-stu-id="d8f20-154">The device to which this resource is connected.</span></span> <span data-ttu-id="d8f20-155">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8f20-155">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-156">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="d8f20-156">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-157">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8f20-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-159">A visibilidade do consumidor para o recurso alocado.</span><span class="sxs-lookup"><span data-stu-id="d8f20-159">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="d8f20-160">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e é sempre definida como 3 (virtualizada).</span><span class="sxs-lookup"><span data-stu-id="d8f20-160">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-161">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d8f20-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d8f20-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-164">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="d8f20-164">A description of the object.</span></span> <span data-ttu-id="d8f20-165">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações de porta do comutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="d8f20-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-166">**DesiredVLANEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="d8f20-166">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-167">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8f20-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-169">O modo de configuração desejado para o ponto de extremidade de VLAN.</span><span class="sxs-lookup"><span data-stu-id="d8f20-169">The desired configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="d8f20-170">Essa propriedade é usada para definir o valor da propriedade **OperationalEndpointMode** inicial na instância da classe [**Msvm \_ VLANEndpoint**](msvm-vlanendpoint.md) associada à porta Ethernet de destino.</span><span class="sxs-lookup"><span data-stu-id="d8f20-170">This property is used to set the initial **OperationalEndpointMode** property value in the instance of [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) class associated with the targeted Ethernet port.</span></span> <span data-ttu-id="d8f20-171">Consulte a propriedade **OperationalEndpointMode** da classe **Msvm \_ VLANEndpoint** para obter os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="d8f20-171">See the **OperationalEndpointMode** property of the **Msvm\_VLANEndpoint** class for possible values.</span></span> <span data-ttu-id="d8f20-172">Essa propriedade é herdada do **CIM \_ EthernetPortAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="d8f20-172">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-173">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d8f20-173">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d8f20-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-176">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="d8f20-176">A display name for the object.</span></span> <span data-ttu-id="d8f20-177">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d8f20-177">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="d8f20-178">A alteração dessa propriedade irá alterar o nome do elemento do derivado do dispositivo lógico associado.</span><span class="sxs-lookup"><span data-stu-id="d8f20-178">Changing this property will change the element name of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-179">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d8f20-179">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-180">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8f20-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-182">Indica se a solicitação de alocação está habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="d8f20-182">Indicates whether the allocation request is enabled or disabled.</span></span> <span data-ttu-id="d8f20-183">Quando uma solicitação de alocação é marcada como desabilitada (3), a alocação não é processada.</span><span class="sxs-lookup"><span data-stu-id="d8f20-183">When an allocation request is marked as Disabled (3), then the allocation is not processed.</span></span> <span data-ttu-id="d8f20-184">O **enabledstate** para uma configuração ativa é sempre marcado como habilitado (2).</span><span class="sxs-lookup"><span data-stu-id="d8f20-184">The **EnabledState** for an active configuration is always marked as Enabled (2).</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d8f20-185">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="d8f20-185">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d8f20-186">**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="d8f20-186">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d8f20-187">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="d8f20-187">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-188">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d8f20-188">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-190">Somente um recurso de host pode ser atribuído a cada dispositivo no comutador virtual, de modo que somente o primeiro elemento dessa matriz pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="d8f20-190">Only one host resource can be assigned to each device in the virtual switch, so only the first element of this array can be set.</span></span> <span data-ttu-id="d8f20-191">Para dispositivos que dão suporte a esse recurso, defina o primeiro elemento da matriz **HostResource** para conter uma referência ao recurso de host subjacente a ser atribuído.</span><span class="sxs-lookup"><span data-stu-id="d8f20-191">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="d8f20-192">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8f20-192">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-193">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d8f20-193">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-194">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d8f20-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-196">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="d8f20-196">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-197">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="d8f20-197">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d8f20-198">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))e é sempre definida como "Microsoft:*GUID* \\ *DeviceSpecificData*".</span><span class="sxs-lookup"><span data-stu-id="d8f20-198">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-199">**LastKnownSwitchName**</span><span class="sxs-lookup"><span data-stu-id="d8f20-199">**LastKnownSwitchName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-200">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d8f20-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-201">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-202">O último nome amigável conhecido do comutador para o qual essa porta tinha uma afinidade rígida, se houver.</span><span class="sxs-lookup"><span data-stu-id="d8f20-202">The last known friendly name of the switch this port had a hard affinity to, if any.</span></span>

> [!Note]  
> <span data-ttu-id="d8f20-203">Propriedade adicionada no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d8f20-203">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="d8f20-204">**Limite**</span><span class="sxs-lookup"><span data-stu-id="d8f20-204">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-205">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d8f20-205">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-207">A quantidade máxima de recursos de host correspondentes que podem ser consumidos pelo comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="d8f20-207">The maximum amount of corresponding host resources that can be consumed by the virtual switch.</span></span> <span data-ttu-id="d8f20-208">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8f20-208">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-209">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="d8f20-209">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-210">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8f20-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-212">Especifica como esse recurso é mapeado para recursos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="d8f20-212">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="d8f20-213">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8f20-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-214">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="d8f20-214">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-215">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d8f20-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-216">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-217">Uma cadeia de caracteres que descreve o tipo de modelo de ponto de extremidade de VLAN com suporte deste ponto de extremidade de VLAN.</span><span class="sxs-lookup"><span data-stu-id="d8f20-217">A string that describes the type of VLAN endpoint model that is supported by this VLAN endpoint.</span></span> <span data-ttu-id="d8f20-218">Essa propriedade só é usada quando a propriedade **DesiredVLANEndpointMode** é definida como 1 (Other).</span><span class="sxs-lookup"><span data-stu-id="d8f20-218">This property is only used when the **DesiredVLANEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="d8f20-219">Essa propriedade deve ser definida como **NULL** quando a propriedade **DesiredVLANEndpointMode** é qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="d8f20-219">This property should be set to **Null** when the **DesiredVLANEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="d8f20-220">Essa propriedade é herdada do **CIM \_ EthernetPortAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="d8f20-220">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-221">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="d8f20-221">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-222">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d8f20-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-223">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-224">Uma cadeia de caracteres que descreve o tipo de recurso quando um valor bem definido não está disponível e [**ResourceType**](msvm-processorsettingdata.md) tem o valor 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="d8f20-224">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1 (Other).</span></span> <span data-ttu-id="d8f20-225">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e não é usada.</span><span class="sxs-lookup"><span data-stu-id="d8f20-225">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-226">**Pai**</span><span class="sxs-lookup"><span data-stu-id="d8f20-226">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-227">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d8f20-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-229">O pai do recurso.</span><span class="sxs-lookup"><span data-stu-id="d8f20-229">The parent of the resource.</span></span> <span data-ttu-id="d8f20-230">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8f20-230">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-231">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="d8f20-231">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-232">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d8f20-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-234">O identificador do pool de recursos do qual esse recurso foi alocado.</span><span class="sxs-lookup"><span data-stu-id="d8f20-234">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="d8f20-235">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8f20-235">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-236">**RequiredFeatureHints**</span><span class="sxs-lookup"><span data-stu-id="d8f20-236">**RequiredFeatureHints**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-237">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d8f20-237">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-239">A lista de nomes de exibição que correspondem a cada entrada na matriz **RequiredFeatures** .</span><span class="sxs-lookup"><span data-stu-id="d8f20-239">The list of display names that correspond to each entry in the **RequiredFeatures** array.</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-240">**RequiredFeatures**</span><span class="sxs-lookup"><span data-stu-id="d8f20-240">**RequiredFeatures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-241">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d8f20-241">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-242">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d8f20-242">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-243">A lista de identificadores de recurso que representam todos os recursos necessários para uma porta.</span><span class="sxs-lookup"><span data-stu-id="d8f20-243">The list of feature identifiers that represent all the features that are required for a port.</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-244">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="d8f20-244">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-245">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d8f20-245">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-246">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-247">A quantidade de recursos que são reservados para uso pelo comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="d8f20-247">The amount of resources that are reserved for use by the virtual switch.</span></span> <span data-ttu-id="d8f20-248">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8f20-248">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-249">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="d8f20-249">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-250">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d8f20-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-251">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-252">Uma cadeia de caracteres que descreve um subtipo específico de implementação para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="d8f20-252">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="d8f20-253">Por exemplo, isso pode ser usado para distinguir modelos diferentes do mesmo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="d8f20-253">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="d8f20-254">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8f20-254">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-255">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="d8f20-255">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-256">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8f20-256">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-257">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-258">O tipo de recurso que essa configuração de alocação representa.</span><span class="sxs-lookup"><span data-stu-id="d8f20-258">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="d8f20-259">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e é sempre definida como 33 (conexão Ethernet).</span><span class="sxs-lookup"><span data-stu-id="d8f20-259">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 33 (Ethernet connection).</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-260">**TestReplicaPoolID**</span><span class="sxs-lookup"><span data-stu-id="d8f20-260">**TestReplicaPoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-261">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d8f20-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-262">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d8f20-262">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-263">Especifica o pool de recursos de rede do qual uma conexão será alocada para o sistema de réplica de teste quando ela for criada.</span><span class="sxs-lookup"><span data-stu-id="d8f20-263">Specifies the network resource pool from which a connection will be allocated to the test replica system when it is created.</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-264">**TestReplicaSwitchName**</span><span class="sxs-lookup"><span data-stu-id="d8f20-264">**TestReplicaSwitchName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-265">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d8f20-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-266">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d8f20-266">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-267">Especifica o nome de exibição do comutador de rede virtual para o qual uma conexão será alocada para o sistema de réplica de teste quando ele for criado.</span><span class="sxs-lookup"><span data-stu-id="d8f20-267">Specifies the display name of the virtual network switch to which a connection will be allocated for the test replica system when it is created.</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-268">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="d8f20-268">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-269">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d8f20-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-271">O número total de portas no comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="d8f20-271">The total number of ports in the virtual switch.</span></span> <span data-ttu-id="d8f20-272">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8f20-272">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-273">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="d8f20-273">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-274">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d8f20-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-275">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-276">Especifica a unidade de medida para a propriedade **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="d8f20-276">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="d8f20-277">O valor dessa propriedade deve ser um valor válido do qualificador de unidades programáticas, conforme definido no anexo C. 1 de DSP0004 V 2.5 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="d8f20-277">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="d8f20-278">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8f20-278">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d8f20-279">**Weight**</span><span class="sxs-lookup"><span data-stu-id="d8f20-279">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f20-280">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d8f20-280">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d8f20-281">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8f20-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f20-282">Um inteiro que define o peso de cada comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="d8f20-282">An integer that defines the weight for each virtual switch.</span></span> <span data-ttu-id="d8f20-283">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d8f20-283">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="d8f20-284">Intervalo: 0 1000</span><span class="sxs-lookup"><span data-stu-id="d8f20-284">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8f20-285">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8f20-285">Requirements</span></span>



| <span data-ttu-id="d8f20-286">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8f20-286">Requirement</span></span> | <span data-ttu-id="d8f20-287">Valor</span><span class="sxs-lookup"><span data-stu-id="d8f20-287">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8f20-288">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8f20-288">Minimum supported client</span></span><br/> | <span data-ttu-id="d8f20-289">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d8f20-289">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d8f20-290">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8f20-290">Minimum supported server</span></span><br/> | <span data-ttu-id="d8f20-291">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d8f20-291">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d8f20-292">Namespace</span><span class="sxs-lookup"><span data-stu-id="d8f20-292">Namespace</span></span><br/>                | <span data-ttu-id="d8f20-293">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d8f20-293">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d8f20-294">MOF</span><span class="sxs-lookup"><span data-stu-id="d8f20-294">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8f20-295"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8f20-295"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8f20-296">DLL</span><span class="sxs-lookup"><span data-stu-id="d8f20-296">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8f20-297"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d8f20-297"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

