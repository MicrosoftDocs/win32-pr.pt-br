---
description: Representa o estado configurado da memória para uma máquina virtual.
ms.assetid: 4B6FEE50-1C5F-4F41-B14A-E10B40400A1B
title: Classe Msvm_MemorySettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MemorySettingData
- Msvm_MemorySettingData.InstanceID
- Msvm_MemorySettingData.Caption
- Msvm_MemorySettingData.Description
- Msvm_MemorySettingData.ElementName
- Msvm_MemorySettingData.ResourceType
- Msvm_MemorySettingData.OtherResourceType
- Msvm_MemorySettingData.ResourceSubType
- Msvm_MemorySettingData.PoolID
- Msvm_MemorySettingData.ConsumerVisibility
- Msvm_MemorySettingData.HostResource
- Msvm_MemorySettingData.HugePagesEnabled
- Msvm_MemorySettingData.AllocationUnits
- Msvm_MemorySettingData.VirtualQuantity
- Msvm_MemorySettingData.Reservation
- Msvm_MemorySettingData.Limit
- Msvm_MemorySettingData.Weight
- Msvm_MemorySettingData.AutomaticAllocation
- Msvm_MemorySettingData.AutomaticDeallocation
- Msvm_MemorySettingData.Parent
- Msvm_MemorySettingData.Connection
- Msvm_MemorySettingData.Address
- Msvm_MemorySettingData.MappingBehavior
- Msvm_MemorySettingData.AddressOnParent
- Msvm_MemorySettingData.VirtualQuantityUnits
- Msvm_MemorySettingData.DynamicMemoryEnabled
- Msvm_MemorySettingData.TargetMemoryBuffer
- Msvm_MemorySettingData.IsVirtualized
- Msvm_MemorySettingData.SwapFilesInUse
- Msvm_MemorySettingData.MaxMemoryBlocksPerNumaNode
- Msvm_MemorySettingData.SgxSize
- Msvm_MemorySettingData.SgxEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47309fead7ee45936f34e1e4286ee94437823df7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921657"
---
# <a name="msvm_memorysettingdata-class"></a><span data-ttu-id="5a1ad-103">\_Classe Msvm MemorySettingData</span><span class="sxs-lookup"><span data-stu-id="5a1ad-103">Msvm\_MemorySettingData class</span></span>

<span data-ttu-id="5a1ad-104">Representa o estado configurado da memória para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-104">Represents the configured state of the memory for a virtual machine.</span></span>

<span data-ttu-id="5a1ad-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a1ad-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a1ad-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MemorySettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Memory Default Settings";
  string  Description = "Describes the default settings for the memory resources.";
  string  ElementName;
  uint16  ResourceType = 4;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Memory";
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  boolean HugePagesEnabled;
  string  AllocationUnits = "byte * 2^20";
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "byte * 2^20";
  boolean DynamicMemoryEnabled;
  uint32  TargetMemoryBuffer;
  boolean IsVirtualized = True;
  boolean SwapFilesInUse;
  uint64  MaxMemoryBlocksPerNumaNode;
  uint64  SgxSize;
  boolean SgxEnabled;
};
```

## <a name="members"></a><span data-ttu-id="5a1ad-107">Membros</span><span class="sxs-lookup"><span data-stu-id="5a1ad-107">Members</span></span>

<span data-ttu-id="5a1ad-108">A classe **Msvm \_ MemorySettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5a1ad-108">The **Msvm\_MemorySettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="5a1ad-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5a1ad-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5a1ad-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5a1ad-110">Properties</span></span>

<span data-ttu-id="5a1ad-111">A classe **Msvm \_ MemorySettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-111">The **Msvm\_MemorySettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5a1ad-112">**Endereço**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-115">O endereço do recurso.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-115">The address of the resource.</span></span> <span data-ttu-id="5a1ad-116">Por exemplo, o endereço MAC de uma porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-116">For example, the MAC address of an Ethernet port.</span></span> <span data-ttu-id="5a1ad-117">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5a1ad-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-118">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-121">Descreve o endereço deste recurso no contexto do pai.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="5a1ad-122">As propriedades **pai** e **AddressOnParent** são usadas para descrever a relação do controlador, bem como a ordem dos dispositivos em um controlador.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="5a1ad-123">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5a1ad-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-124">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-127">As unidades de alocação usadas pelas propriedades **Reservation** e **Limit** .</span><span class="sxs-lookup"><span data-stu-id="5a1ad-127">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="5a1ad-128">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5a1ad-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-129">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-130">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-132">Indica se o recurso será alocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-132">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="5a1ad-133">Por exemplo, quando essa propriedade é definida como **true** e a máquina virtual de consumo está ligada, esse recurso seria alocado.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-133">For example, when this property is set to **True** and the consuming virtual machine is powered on, this resource would be allocated.</span></span> <span data-ttu-id="5a1ad-134">Um valor **false** indica que o recurso deve ser alocado explicitamente.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-134">A value of **False** indicates the resource must be explicitly allocated.</span></span> <span data-ttu-id="5a1ad-135">Por exemplo, a configuração pode representar uma mídia removível (como um CD-ROM ou um disquete) em que, na inicialização, a mídia não está presente.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-135">For example, the setting may represent removable media (such as a CD-ROM or a floppy disk) where at startup, the media is not present.</span></span> <span data-ttu-id="5a1ad-136">Uma operação explícita é necessária para alocar o recurso.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-136">An explicit operation is required to allocate the resource.</span></span> <span data-ttu-id="5a1ad-137">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5a1ad-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-138">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-138">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-139">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-141">Indica se o recurso será alocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-141">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="5a1ad-142">Por exemplo, quando essa propriedade é definida como **true** e a máquina virtual de consumo está ligada, esse recurso seria alocado.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-142">For example when this property is set to **True** and the consuming virtual machine is powered on, this resource would be allocated.</span></span> <span data-ttu-id="5a1ad-143">Quando essa propriedade é **falsa**, o recurso deve ser alocado explicitamente.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-143">When this property is **False**, the resource must be explicitly allocated.</span></span> <span data-ttu-id="5a1ad-144">Por exemplo, a configuração pode representar uma mídia removível (como um CD-ROM ou um disquete) em que, na inicialização, a mídia não está presente.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-144">For example, the setting may represent removable media (such as a CD-ROM or a floppy disk) where at startup, the media is not present.</span></span> <span data-ttu-id="5a1ad-145">Uma operação explícita é necessária para alocar o recurso.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-145">An explicit operation is required to allocate the resource.</span></span> <span data-ttu-id="5a1ad-146">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5a1ad-146">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-147">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-147">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-148">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-150">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="5a1ad-150">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-151">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-151">A short description of the object.</span></span> <span data-ttu-id="5a1ad-152">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5a1ad-152">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-153">**Conexão**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-153">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-154">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-156">O dispositivo ao qual esse recurso está conectado.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-156">The device to which this resource is connected.</span></span> <span data-ttu-id="5a1ad-157">Por exemplo, uma rede nomeada ou porta de comutador.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-157">For example, a named network or switch port.</span></span> <span data-ttu-id="5a1ad-158">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5a1ad-158">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-159">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-159">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-160">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-162">Descreve a visibilidade dos consumidores para o recurso alocado.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-162">Describes the consumers visibility to the allocated resource.</span></span> <span data-ttu-id="5a1ad-163">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5a1ad-163">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-164">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-164">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-165">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-167">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="5a1ad-167">A description of the object.</span></span> <span data-ttu-id="5a1ad-168">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5a1ad-168">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-169">**DynamicMemoryEnabled**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-169">**DynamicMemoryEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-170">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-172">Indica se a memória dinâmica está habilitada para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-172">Indicates whether dynamic memory is enabled for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-173">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-173">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-176">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-176">A display name for the object.</span></span> <span data-ttu-id="5a1ad-177">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5a1ad-177">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-178">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-178">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-179">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-181">O primeiro elemento dessa matriz contém uma referência ao recurso de host subjacente a ser atribuído.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-181">The first element of this array contains a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="5a1ad-182">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-182">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but it is not used.</span></span>

</dd> <dt>
  
<span data-ttu-id="5a1ad-183">**HugePagesEnabled**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-183">**HugePagesEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-184">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-186">Se a memória é apoiada por 1 GB de páginas ou não.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-186">Whether the memory is backed by 1GB pages or not.</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-187">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-187">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-188">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-190">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-190">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-191">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-191">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5a1ad-192">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5a1ad-192">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-193">**Isvirtualizado**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-193">**IsVirtualized**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-194">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-194">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-196">Indica se este dispositivo é virtualizado ou passado.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-196">Indicates whether this device is virtualized or passed through.</span></span> <span data-ttu-id="5a1ad-197">Quando definido como **false**, o recurso de host ou subjacente é usado.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-197">When set to **False**, the underlying or host resource is used.</span></span> <span data-ttu-id="5a1ad-198">Pelo menos um item deve estar presente na propriedade **DeviceID** .</span><span class="sxs-lookup"><span data-stu-id="5a1ad-198">At least one item should be present in the **DeviceID** property.</span></span> <span data-ttu-id="5a1ad-199">Quando definido como **true**, o recurso é virtualizado e não pode ser mapeado diretamente para um recurso de host/base.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-199">When set to **True**, the resource is virtualized and may not map directly to an underlying/host resource.</span></span> <span data-ttu-id="5a1ad-200">Algumas implementações podem dar suporte a uma atribuição específica para recursos virtualizados; nesse caso, os recursos do host são expostos usando a propriedade **DeviceID** .</span><span class="sxs-lookup"><span data-stu-id="5a1ad-200">Some implementations may support specific assignment for virtualized resources, in which case the host resources are exposed by using the **DeviceID** property.</span></span> <span data-ttu-id="5a1ad-201">Essa propriedade é sempre definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-201">This property is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-202">**Limite**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-202">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-203">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-205">A quantidade máxima de memória que pode ser consumida pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-205">The maximum amount of memory that may be consumed by the virtual machine.</span></span> <span data-ttu-id="5a1ad-206">Para uma máquina virtual com memória dinâmica habilitada, isso representa a configuração de memória máxima.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-206">For a virtual machine with dynamic memory enabled, this represents the maximum memory setting.</span></span> <span data-ttu-id="5a1ad-207">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5a1ad-207">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-208">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-208">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-209">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-209">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-210">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-211">Especifica como esse recurso é mapeado para recursos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-211">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="5a1ad-212">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5a1ad-212">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-213">**MaxMemoryBlocksPerNumaNode**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-213">**MaxMemoryBlocksPerNumaNode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-214">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-214">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-216">A quantidade máxima de memória que pode ser observada na máquina virtual como pertencente a um único nó NUMA.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-216">The maximum amount of memory that can be observed within the virtual machine as belonging to a single NUMA node.</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-217">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-217">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-218">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-219">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-220">Uma cadeia de caracteres que descreve o tipo de recurso quando um valor bem definido não está disponível e **ResourceType** tem o valor "other".</span><span class="sxs-lookup"><span data-stu-id="5a1ad-220">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value "Other".</span></span> <span data-ttu-id="5a1ad-221">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5a1ad-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-222">**Pai**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-222">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-223">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-225">O pai do recurso.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-225">The parent of the resource.</span></span> <span data-ttu-id="5a1ad-226">Por exemplo, um controlador para a alocação atual.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-226">For example, a controller for the current allocation.</span></span> <span data-ttu-id="5a1ad-227">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5a1ad-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-228">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-228">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-229">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-230">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-231">O identificador do pool de recursos do qual esse recurso foi alocado.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-231">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="5a1ad-232">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5a1ad-232">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-233">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-233">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-234">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-234">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-235">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-236">Especifica a quantidade de memória garantida disponível para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-236">Specifies the amount of memory guaranteed to be available for this virtual machine.</span></span> <span data-ttu-id="5a1ad-237">Para uma máquina virtual com memória dinâmica habilitada, isso representa a configuração de memória mínima.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-237">For a virtual machine with dynamic memory enabled, this represents the minimum memory setting.</span></span> <span data-ttu-id="5a1ad-238">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5a1ad-238">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-239">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-239">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-240">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-242">Uma cadeia de caracteres que descreve um subtipo específico de implementação para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-242">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="5a1ad-243">Por exemplo, isso pode ser usado para distinguir modelos diferentes do mesmo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-243">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="5a1ad-244">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5a1ad-244">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-245">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-245">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-246">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-247">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-248">O tipo de recurso que essa configuração de alocação representa.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-248">The type of resource that this allocation setting represents.</span></span> <span data-ttu-id="5a1ad-249">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e é sempre definida como 4 (memória).</span><span class="sxs-lookup"><span data-stu-id="5a1ad-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 4 (Memory).</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-250">**SgxEnabled**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-250">**SgxEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-251">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-253">Indica se o SGX está habilitado.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-253">Indicates if SGX is enabled.</span></span>

> [!Note]  
> <span data-ttu-id="5a1ad-254">Essa propriedade foi adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-254">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="5a1ad-255">**SgxSize**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-255">**SgxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-256">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-256">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-257">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-258">A quantidade de memória de SGX a ser alocada para a VM, em MB.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-258">The amount of SGX memory to allocate for the VM, in MB.</span></span>

> [!Note]  
> <span data-ttu-id="5a1ad-259">Essa propriedade foi adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-259">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="5a1ad-260">**SwapFilesInUse**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-260">**SwapFilesInUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-261">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-261">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-262">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-263">**True** se a paginação de segundo nível estiver ativa; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-263">**True** if second level paging is active; otherwise, **False**.</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-264">**TargetMemoryBuffer**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-264">**TargetMemoryBuffer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-265">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-266">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-267">Define a quantidade de memória extra que deve ser reservada para uma máquina virtual em tempo de execução, como um percentual da memória total que a máquina virtual deve precisar.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-267">Defines the amount of extra memory that should be reserved for a virtual machine at runtime, as a percentage of the total memory that the virtual machine is thought to need.</span></span> <span data-ttu-id="5a1ad-268">Isso se aplica somente a máquinas virtuais com memória dinâmica habilitada.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-268">This only applies to virtual machines with dynamic memory enabled.</span></span>

<span data-ttu-id="5a1ad-269">Essa propriedade pode estar no intervalo de 5 a 2000.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-269">This property can be in the range of 5 to 2000.</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-270">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-270">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-271">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-272">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-273">A quantidade total de RAM na máquina virtual, conforme visto pelo sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-273">The total amount of RAM in the virtual machine, as seen by the guest operating system.</span></span> <span data-ttu-id="5a1ad-274">Para uma máquina virtual com memória dinâmica habilitada, isso representa a memória inicial disponível na inicialização.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-274">For a virtual machine with dynamic memory enabled, this represents the initial memory available at startup.</span></span> <span data-ttu-id="5a1ad-275">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5a1ad-275">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-276">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-276">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-277">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-278">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-279">Especifica a unidade de medida para essa alocação de recursos.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-279">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="5a1ad-280">O valor dessa propriedade deve ser um valor válido do qualificador de unidades programáticas, conforme definido no anexo C. 1 de DSP0004 V 2.5 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-280">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="5a1ad-281">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5a1ad-281">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5a1ad-282">**Weight**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-282">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1ad-283">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5a1ad-284">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a1ad-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a1ad-285">Define o valor de peso de alocação de memória para cada máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-285">Defines the memory allocation weighting value for each virtual machine.</span></span> <span data-ttu-id="5a1ad-286">Depois que todas as reservas forem atendidas, a memória restante da plataforma de hospedagem será alocada às máquinas virtuais com base em seus pesos relativos (sem exceder o valor especificado pela propriedade **Limit** ).</span><span class="sxs-lookup"><span data-stu-id="5a1ad-286">After all reserves have been met, the remaining memory of the hosting platform will be allocated to virtual machines based on their relative weights (not to exceed the value specified by the **Limit** property).</span></span> <span data-ttu-id="5a1ad-287">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5a1ad-287">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a1ad-288">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a1ad-288">Remarks</span></span>

<span data-ttu-id="5a1ad-289">O acesso à classe **Msvm \_ MemorySettingData** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="5a1ad-289">Access to the **Msvm\_MemorySettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="5a1ad-290">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="5a1ad-290">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="5a1ad-291">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5a1ad-291">Examples</span></span>

```powershell
function WaitForResult
{
  param($result)
  if ($result.ReturnValue -eq 4096)
  {
    while($true)
    {
      $result.Job
      if ($result.Job -ne $null)
      {
        if ($result.Job.JobState -gt 4)
        {
          return $result.Job.ErrorCode
        }
      }
      start-sleep 1
    }
  }
  else
  {
    return $result.ReturnValue
  }
}

if ($($args.count) -ne 2)
{
  Write-Host "EnableHugePages.ps1 VMName SizeInMB"
  return
}

$vmName = $args[0]
$sizeInMB = $args[1]
 
$namespace = "root\virtualization\v2"
$vm = Get-WmiObject -class MSVM_ComputerSystem -filter "ElementName='$vmName'" -namespace $namespace
$settings = Get-WmiObject -query "Associators of {$vm} where ResultClass = Msvm_VirtualSystemSettingData" -namespace $namespace
$vmSettings = $settings | ? VirtualSystemType -eq "Microsoft:Hyper-V:System:Realized"
$memorySettings = Get-WmiObject -query "Associators of {$vmSettings} where ResultClass = Msvm_MemorySettingData" -namespace $namespace

$memorySettings.MaxMemoryBlocksPerNumaNode = $sizeInMB
$memorySettings.Reservation = $sizeInMB
$memorySettings.Limit = $sizeInMB
$memorySettings.VirtualQuantity = $sizeInMB
$memorySettings.HugePagesEnabled = $True

$vmSvc = Get-WmiObject -class Msvm_VirtualSystemManagementService -namespace $namespace
$res = $vmSvc.ModifyResourceSettings($memorySettings.GetText(2))
if (WaitForResult($res) -ne 0)
{
  Write-Host "Failed."
}
```

## <a name="requirements"></a><span data-ttu-id="5a1ad-292">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a1ad-292">Requirements</span></span>



| <span data-ttu-id="5a1ad-293">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a1ad-293">Requirement</span></span> | <span data-ttu-id="5a1ad-294">Valor</span><span class="sxs-lookup"><span data-stu-id="5a1ad-294">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a1ad-295">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a1ad-295">Minimum supported client</span></span><br/> | <span data-ttu-id="5a1ad-296">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5a1ad-296">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5a1ad-297">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a1ad-297">Minimum supported server</span></span><br/> | <span data-ttu-id="5a1ad-298">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5a1ad-298">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5a1ad-299">Namespace</span><span class="sxs-lookup"><span data-stu-id="5a1ad-299">Namespace</span></span><br/>                | <span data-ttu-id="5a1ad-300">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="5a1ad-300">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5a1ad-301">MOF</span><span class="sxs-lookup"><span data-stu-id="5a1ad-301">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a1ad-302"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a1ad-302"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5a1ad-303">DLL</span><span class="sxs-lookup"><span data-stu-id="5a1ad-303">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a1ad-304"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5a1ad-304"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5a1ad-305">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a1ad-305">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a1ad-306">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-306">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="5a1ad-307">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="5a1ad-307">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="5a1ad-308">Classes de memória</span><span class="sxs-lookup"><span data-stu-id="5a1ad-308">Memory Classes</span></span>](memory-classes.md)
</dt> </dl>

 

