---
description: Representa os Estados de alocação atuais e registrados de um recurso virtual.
ms.assetid: 5C180933-2013-4E16-A9BD-653D5426F468
title: Classe Msvm_ResourceAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceAllocationSettingData
- Msvm_ResourceAllocationSettingData.InstanceID
- Msvm_ResourceAllocationSettingData.Caption
- Msvm_ResourceAllocationSettingData.Description
- Msvm_ResourceAllocationSettingData.ElementName
- Msvm_ResourceAllocationSettingData.ResourceType
- Msvm_ResourceAllocationSettingData.OtherResourceType
- Msvm_ResourceAllocationSettingData.ResourceSubType
- Msvm_ResourceAllocationSettingData.PoolID
- Msvm_ResourceAllocationSettingData.ConsumerVisibility
- Msvm_ResourceAllocationSettingData.HostResource
- Msvm_ResourceAllocationSettingData.AllocationUnits
- Msvm_ResourceAllocationSettingData.VirtualQuantity
- Msvm_ResourceAllocationSettingData.Reservation
- Msvm_ResourceAllocationSettingData.Limit
- Msvm_ResourceAllocationSettingData.Weight
- Msvm_ResourceAllocationSettingData.AutomaticAllocation
- Msvm_ResourceAllocationSettingData.AutomaticDeallocation
- Msvm_ResourceAllocationSettingData.Parent
- Msvm_ResourceAllocationSettingData.Connection
- Msvm_ResourceAllocationSettingData.Address
- Msvm_ResourceAllocationSettingData.MappingBehavior
- Msvm_ResourceAllocationSettingData.AddressOnParent
- Msvm_ResourceAllocationSettingData.VirtualQuantityUnits
- Msvm_ResourceAllocationSettingData.VirtualSystemIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6d1cb2f97dcb3fa144db5cf27c1a82690214b11d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296859"
---
# <a name="msvm_resourceallocationsettingdata-class"></a><span data-ttu-id="68e00-103">\_Classe Msvm ResourceAllocationSettingData</span><span class="sxs-lookup"><span data-stu-id="68e00-103">Msvm\_ResourceAllocationSettingData class</span></span>

<span data-ttu-id="68e00-104">Representa os Estados de alocação atuais e registrados de um recurso virtual.</span><span class="sxs-lookup"><span data-stu-id="68e00-104">Represents the current and recorded allocation states of a virtual resource.</span></span>

<span data-ttu-id="68e00-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="68e00-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="68e00-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68e00-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceAllocationSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string  Caption;
  string  Description;
  string  ElementName;
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
  string  VirtualSystemIdentifiers[] = { "GUID" };
};
```

## <a name="members"></a><span data-ttu-id="68e00-107">Membros</span><span class="sxs-lookup"><span data-stu-id="68e00-107">Members</span></span>

<span data-ttu-id="68e00-108">A classe **Msvm \_ ResourceAllocationSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="68e00-108">The **Msvm\_ResourceAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="68e00-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="68e00-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="68e00-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="68e00-110">Properties</span></span>

<span data-ttu-id="68e00-111">A classe **Msvm \_ ResourceAllocationSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="68e00-111">The **Msvm\_ResourceAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68e00-112">**Endereço**</span><span class="sxs-lookup"><span data-stu-id="68e00-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e00-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="68e00-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68e00-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e00-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e00-115">O endereço do recurso.</span><span class="sxs-lookup"><span data-stu-id="68e00-115">The address of the resource.</span></span> <span data-ttu-id="68e00-116">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="68e00-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="68e00-117">Essa é uma propriedade somente leitura, mas se a propriedade **ResourceType** for 20 (controlador de gráficos), ela poderá ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="68e00-117">This is a read-only property, but if the **ResourceType** property is 20 (Graphics controller), it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="68e00-118">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="68e00-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e00-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="68e00-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68e00-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e00-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e00-121">Descreve o endereço deste recurso no contexto do pai.</span><span class="sxs-lookup"><span data-stu-id="68e00-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="68e00-122">As propriedades **pai** e **AddressOnParent** são usadas para descrever a relação do controlador, bem como a ordem dos dispositivos em um controlador.</span><span class="sxs-lookup"><span data-stu-id="68e00-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="68e00-123">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="68e00-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68e00-124">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="68e00-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e00-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="68e00-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68e00-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e00-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e00-127">A unidade de alocação usada pelas propriedades **Reservation** e **Limit** .</span><span class="sxs-lookup"><span data-stu-id="68e00-127">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="68e00-128">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="68e00-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68e00-129">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="68e00-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e00-130">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="68e00-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68e00-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e00-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e00-132">Indica se o recurso será alocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="68e00-132">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="68e00-133">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="68e00-133">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68e00-134">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="68e00-134">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e00-135">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="68e00-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68e00-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e00-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e00-137">Indica se o recurso será desalocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="68e00-137">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="68e00-138">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="68e00-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68e00-139">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="68e00-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e00-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="68e00-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68e00-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e00-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68e00-142">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="68e00-142">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="68e00-143">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="68e00-143">A short description of the object.</span></span> <span data-ttu-id="68e00-144">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="68e00-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="68e00-145">**Conexão**</span><span class="sxs-lookup"><span data-stu-id="68e00-145">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e00-146">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="68e00-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="68e00-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e00-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e00-148">O dispositivo ao qual esse recurso está conectado.</span><span class="sxs-lookup"><span data-stu-id="68e00-148">The device to which this resource is connected.</span></span> <span data-ttu-id="68e00-149">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="68e00-149">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="68e00-150">Trata-se de uma propriedade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="68e00-150">This is a read-only property.</span></span> <span data-ttu-id="68e00-151">Mas se a propriedade **ResourceType** for 21 (porta serial) e a **Propriedade ResourceSubType** for "Microsoft: Hyper-V: porta serial", a propriedade de **conexão** poderá ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="68e00-151">But if the **ResourceType** property is 21 (Serial port) and the **ResourceSubType** property is "Microsoft:Hyper-V:Serial Port", the **Connection** property can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="68e00-152">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="68e00-152">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e00-153">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68e00-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68e00-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e00-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e00-155">A visibilidade do consumidor para o recurso alocado.</span><span class="sxs-lookup"><span data-stu-id="68e00-155">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="68e00-156">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="68e00-156">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68e00-157">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="68e00-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e00-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="68e00-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68e00-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e00-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e00-160">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="68e00-160">A description of the object.</span></span> <span data-ttu-id="68e00-161">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="68e00-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="68e00-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="68e00-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e00-163">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="68e00-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68e00-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e00-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e00-165">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="68e00-165">A display name for the object.</span></span> <span data-ttu-id="68e00-166">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="68e00-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="68e00-167">A alteração dessa propriedade irá alterar o nome do elemento do derivado do dispositivo lógico associado.</span><span class="sxs-lookup"><span data-stu-id="68e00-167">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="68e00-168">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="68e00-168">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="68e00-169">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="68e00-169">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e00-170">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="68e00-170">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="68e00-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e00-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e00-172">Somente um recurso de host pode ser atribuído a cada dispositivo na máquina virtual, de modo que somente o primeiro elemento dessa matriz pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="68e00-172">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="68e00-173">Para dispositivos que dão suporte a esse recurso, defina o primeiro elemento da matriz **HostResource** para conter uma referência ao recurso de host subjacente a ser atribuído.</span><span class="sxs-lookup"><span data-stu-id="68e00-173">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="68e00-174">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="68e00-174">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="68e00-175">Trata-se de uma propriedade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="68e00-175">This is a read-only property.</span></span> <span data-ttu-id="68e00-176">Mas se a propriedade **ResourceType** for 17 (disco) e a **Propriedade ResourceSubType** for "Microsoft: Hyper-V: unidade de disco físico", a propriedade **HostResource** poderá ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="68e00-176">But if the **ResourceType** property is 17 (Disk) and the **ResourceSubType** property is "Microsoft:Hyper-V:Physical Disk Drive", the **HostResource** property can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="68e00-177">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="68e00-177">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e00-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="68e00-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68e00-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e00-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68e00-180">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="68e00-180">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="68e00-181">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="68e00-181">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="68e00-182">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))e é sempre definida como "Microsoft:*GUID* \\ *DeviceSpecificData*".</span><span class="sxs-lookup"><span data-stu-id="68e00-182">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="68e00-183">**Limite**</span><span class="sxs-lookup"><span data-stu-id="68e00-183">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e00-184">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="68e00-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="68e00-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e00-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e00-186">A quantidade máxima de recursos que serão concedidos para essa alocação.</span><span class="sxs-lookup"><span data-stu-id="68e00-186">The maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="68e00-187">A unidade de medida para essa propriedade é especificada pela propriedade **VirtualQuantityUnits** .</span><span class="sxs-lookup"><span data-stu-id="68e00-187">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="68e00-188">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="68e00-188">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68e00-189">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="68e00-189">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e00-190">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68e00-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68e00-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e00-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e00-192">Especifica como esse recurso é mapeado para recursos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="68e00-192">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="68e00-193">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="68e00-193">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68e00-194">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="68e00-194">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e00-195">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="68e00-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68e00-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e00-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e00-197">Uma cadeia de caracteres que descreve o tipo de recurso quando um valor bem definido não está disponível e [**ResourceType**](msvm-processorsettingdata.md) tem o valor 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="68e00-197">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="68e00-198">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="68e00-198">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68e00-199">**Pai**</span><span class="sxs-lookup"><span data-stu-id="68e00-199">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e00-200">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="68e00-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68e00-201">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e00-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e00-202">O pai do recurso.</span><span class="sxs-lookup"><span data-stu-id="68e00-202">The parent of the resource.</span></span> <span data-ttu-id="68e00-203">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="68e00-203">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68e00-204">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="68e00-204">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e00-205">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="68e00-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68e00-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e00-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e00-207">O identificador do pool de recursos do qual esse recurso foi alocado.</span><span class="sxs-lookup"><span data-stu-id="68e00-207">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="68e00-208">Para instâncias associadas a uma máquina virtual, serão "Microsoft:*GUID* \\ *específico de dispositivo-dados*".</span><span class="sxs-lookup"><span data-stu-id="68e00-208">For instances associated with a virtual machine, this will be "Microsoft:*GUID*\\*device-specific data*".</span></span> <span data-ttu-id="68e00-209">Para instâncias que definem configurações potenciais para uma máquina virtual, será "Microsoft: tipo de \\ *GUID* de definição \\ ", em que o *tipo* pode ser um "máximo", "mínimo", "padrão" ou "incremento".</span><span class="sxs-lookup"><span data-stu-id="68e00-209">For instances that define potential settings for a virtual machine, this will be "Microsoft:Definition\\*GUID*\\*Type*", where *Type* can be one of "Maximum", "Minimum", "Default", or "Increment".</span></span> <span data-ttu-id="68e00-210">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="68e00-210">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68e00-211">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="68e00-211">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e00-212">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="68e00-212">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="68e00-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e00-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e00-214">A quantidade de recursos com garantia disponível para essa alocação.</span><span class="sxs-lookup"><span data-stu-id="68e00-214">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="68e00-215">A unidade de medida para essa propriedade é especificada pela propriedade **VirtualQuantityUnits** .</span><span class="sxs-lookup"><span data-stu-id="68e00-215">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="68e00-216">É garantido que esses recursos estejam disponíveis para consumo pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="68e00-216">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="68e00-217">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="68e00-217">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68e00-218">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="68e00-218">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e00-219">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="68e00-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68e00-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e00-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e00-221">Uma cadeia de caracteres que descreve um subtipo específico de implementação para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="68e00-221">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="68e00-222">Por exemplo, isso pode ser usado para distinguir modelos diferentes do mesmo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="68e00-222">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="68e00-223">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="68e00-223">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68e00-224">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="68e00-224">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e00-225">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68e00-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68e00-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e00-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e00-227">O tipo de recurso que essa configuração de alocação representa.</span><span class="sxs-lookup"><span data-stu-id="68e00-227">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="68e00-228">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="68e00-228">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="68e00-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="68e00-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-230"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Sistema de computador** (2)</span><span class="sxs-lookup"><span data-stu-id="68e00-230"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-231"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processador** (3)</span><span class="sxs-lookup"><span data-stu-id="68e00-231"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-232"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memória** (4)</span><span class="sxs-lookup"><span data-stu-id="68e00-232"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-233"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controlador IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="68e00-233"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-234"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI paralelo** (6)</span><span class="sxs-lookup"><span data-stu-id="68e00-234"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-235"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="68e00-235"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-236"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="68e00-236"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-237"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="68e00-237"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-238"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Adaptador Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="68e00-238"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-239"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Outro adaptador de rede** (11)</span><span class="sxs-lookup"><span data-stu-id="68e00-239"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-240"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Slot de e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="68e00-240"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-241"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo de e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="68e00-241"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-242"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Unidade de disquete** (14)</span><span class="sxs-lookup"><span data-stu-id="68e00-242"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Diskette Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-243"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unidade de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="68e00-243"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-244"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unidade de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="68e00-244"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-245"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Unidade de disco** (17)</span><span class="sxs-lookup"><span data-stu-id="68e00-245"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-246"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Unidade de fita** (18)</span><span class="sxs-lookup"><span data-stu-id="68e00-246"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-247"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extensão de armazenamento** (19)</span><span class="sxs-lookup"><span data-stu-id="68e00-247"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-248"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Outro dispositivo de armazenamento** (20)</span><span class="sxs-lookup"><span data-stu-id="68e00-248"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other Storage Device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-249"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Porta serial** (21)</span><span class="sxs-lookup"><span data-stu-id="68e00-249"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-250"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Porta paralela** (22)</span><span class="sxs-lookup"><span data-stu-id="68e00-250"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-251"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controlador USB** (23)</span><span class="sxs-lookup"><span data-stu-id="68e00-251"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-252"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controlador de gráficos** (24)</span><span class="sxs-lookup"><span data-stu-id="68e00-252"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-253"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**Controlador IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="68e00-253"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-254"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unidade particionável** (26)</span><span class="sxs-lookup"><span data-stu-id="68e00-254"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-255"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unidade particionável de base** (27)</span><span class="sxs-lookup"><span data-stu-id="68e00-255"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-256"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Fonte de energia** (28)</span><span class="sxs-lookup"><span data-stu-id="68e00-256"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-257"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Dispositivo de resfriamento** (29)</span><span class="sxs-lookup"><span data-stu-id="68e00-257"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-258"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Porta do comutador Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="68e00-258"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-259"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Disco lógico** (31)</span><span class="sxs-lookup"><span data-stu-id="68e00-259"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-260"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Volume de armazenamento** (32)</span><span class="sxs-lookup"><span data-stu-id="68e00-260"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-261"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Conexão Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="68e00-261"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-262"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (30 32767)</span><span class="sxs-lookup"><span data-stu-id="68e00-262"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="68e00-263"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="68e00-263"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="68e00-264">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="68e00-264">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e00-265">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="68e00-265">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="68e00-266">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e00-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e00-267">Especifica a quantidade de recursos apresentados ao consumidor.</span><span class="sxs-lookup"><span data-stu-id="68e00-267">Specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="68e00-268">A unidade de medida para essa propriedade é especificada pela propriedade **VirtualQuantityUnits** .</span><span class="sxs-lookup"><span data-stu-id="68e00-268">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="68e00-269">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="68e00-269">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68e00-270">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="68e00-270">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e00-271">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="68e00-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68e00-272">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e00-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e00-273">Especifica a unidade de medida para essa alocação de recursos.</span><span class="sxs-lookup"><span data-stu-id="68e00-273">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="68e00-274">O valor dessa propriedade deve ser um valor válido do qualificador de unidades programáticas, conforme definido no anexo C. 1 de DSP0004 V 2.5 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="68e00-274">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="68e00-275">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="68e00-275">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="68e00-276">**VirtualSystemIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="68e00-276">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e00-277">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="68e00-277">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="68e00-278">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e00-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68e00-279">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="68e00-279">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="68e00-280">Uma matriz de cadeia de caracteres de identificadores deste recurso apresentada ao sistema operacional da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="68e00-280">A string array of identifiers of this resource presented to the virtual machine's operating system.</span></span> <span data-ttu-id="68e00-281">Esses valores serão usados somente se a propriedade **ResourceType** estiver definida como 6 (HBA SCSI paralelo) e a propriedade **ResourceSubType** estiver definida como "controlador SCSI sintético da Microsoft".</span><span class="sxs-lookup"><span data-stu-id="68e00-281">These values are used only if the **ResourceType** property is set to 6 (Parallel SCSI HBA) and the **ResourceSubType** property is set to "Microsoft Synthetic SCSI Controller".</span></span> <span data-ttu-id="68e00-282">Essa propriedade é definida como "*GUID*".</span><span class="sxs-lookup"><span data-stu-id="68e00-282">This property is set to "*GUID*".</span></span>

<span data-ttu-id="68e00-283">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="68e00-283">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="68e00-284">**Weight**</span><span class="sxs-lookup"><span data-stu-id="68e00-284">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e00-285">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68e00-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68e00-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e00-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e00-287">Um inteiro que define o peso relativo para cada processador de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="68e00-287">An integer that defines the relative weight for each virtual machine processor.</span></span> <span data-ttu-id="68e00-288">Depois que todas as reservas forem atendidas, a capacidade física restante do processador da plataforma de hospedagem será alocada às máquinas virtuais com base em seus pesos relativos.</span><span class="sxs-lookup"><span data-stu-id="68e00-288">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="68e00-289">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="68e00-289">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="68e00-290">Intervalo: 0 1000</span><span class="sxs-lookup"><span data-stu-id="68e00-290">Range: 0 1000</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68e00-291">Comentários</span><span class="sxs-lookup"><span data-stu-id="68e00-291">Remarks</span></span>

<span data-ttu-id="68e00-292">O acesso à classe **Msvm \_ ResourceAllocationSettingData** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="68e00-292">Access to the **Msvm\_ResourceAllocationSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="68e00-293">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="68e00-293">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="68e00-294">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68e00-294">Requirements</span></span>



| <span data-ttu-id="68e00-295">Requisito</span><span class="sxs-lookup"><span data-stu-id="68e00-295">Requirement</span></span> | <span data-ttu-id="68e00-296">Valor</span><span class="sxs-lookup"><span data-stu-id="68e00-296">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68e00-297">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68e00-297">Minimum supported client</span></span><br/> | <span data-ttu-id="68e00-298">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="68e00-298">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="68e00-299">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68e00-299">Minimum supported server</span></span><br/> | <span data-ttu-id="68e00-300">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="68e00-300">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="68e00-301">Namespace</span><span class="sxs-lookup"><span data-stu-id="68e00-301">Namespace</span></span><br/>                | <span data-ttu-id="68e00-302">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="68e00-302">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="68e00-303">MOF</span><span class="sxs-lookup"><span data-stu-id="68e00-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68e00-304"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68e00-304"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="68e00-305">DLL</span><span class="sxs-lookup"><span data-stu-id="68e00-305">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68e00-306"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="68e00-306"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="68e00-307">Confira também</span><span class="sxs-lookup"><span data-stu-id="68e00-307">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68e00-308">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="68e00-308">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="68e00-309">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="68e00-309">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="68e00-310">**Msvm \_ ResourceAllocationSettingData (v1)**</span><span class="sxs-lookup"><span data-stu-id="68e00-310">**Msvm\_ResourceAllocationSettingData (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="68e00-311">Classes de gerenciamento de recursos</span><span class="sxs-lookup"><span data-stu-id="68e00-311">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

