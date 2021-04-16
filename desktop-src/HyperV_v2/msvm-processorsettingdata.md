---
description: Representa as configurações de processador virtual para uma máquina virtual.
ms.assetid: 2B299793-E1CD-49D4-898C-AE60B49F44F5
title: Classe Msvm_ProcessorSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorSettingData
- Msvm_ProcessorSettingData.InstanceID
- Msvm_ProcessorSettingData.Caption
- Msvm_ProcessorSettingData.Description
- Msvm_ProcessorSettingData.ElementName
- Msvm_ProcessorSettingData.ResourceType
- Msvm_ProcessorSettingData.OtherResourceType
- Msvm_ProcessorSettingData.ResourceSubType
- Msvm_ProcessorSettingData.PoolID
- Msvm_ProcessorSettingData.ConsumerVisibility
- Msvm_ProcessorSettingData.HostResource
- Msvm_ProcessorSettingData.AllocationUnits
- Msvm_ProcessorSettingData.VirtualQuantity
- Msvm_ProcessorSettingData.Reservation
- Msvm_ProcessorSettingData.Limit
- Msvm_ProcessorSettingData.Weight
- Msvm_ProcessorSettingData.AutomaticAllocation
- Msvm_ProcessorSettingData.AutomaticDeallocation
- Msvm_ProcessorSettingData.Parent
- Msvm_ProcessorSettingData.Connection
- Msvm_ProcessorSettingData.Address
- Msvm_ProcessorSettingData.MappingBehavior
- Msvm_ProcessorSettingData.AddressOnParent
- Msvm_ProcessorSettingData.VirtualQuantityUnits
- Msvm_ProcessorSettingData.LimitCPUID
- Msvm_ProcessorSettingData.HwThreadsPerCore
- Msvm_ProcessorSettingData.LimitProcessorFeatures
- Msvm_ProcessorSettingData.MaxProcessorsPerNumaNode
- Msvm_ProcessorSettingData.MaxNumaNodesPerSocket
- Msvm_ProcessorSettingData.EnableHostResourceProtection
- Msvm_ProcessorSettingData.CpuGroupId
- Msvm_ProcessorSettingData.HideHypervisorPresent
- Msvm_ProcessorSettingData.ExposeVirtualizationExtensions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5154105c4deab13f93bb65078a5c9527283620e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757545"
---
# <a name="msvm_processorsettingdata-class"></a><span data-ttu-id="46dac-103">\_Classe Msvm ProcessorSettingData</span><span class="sxs-lookup"><span data-stu-id="46dac-103">Msvm\_ProcessorSettingData class</span></span>

<span data-ttu-id="46dac-104">Representa as configurações de processador virtual para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="46dac-104">Represents the virtual processor settings for a virtual machine.</span></span>

<span data-ttu-id="46dac-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="46dac-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="46dac-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46dac-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProcessorSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Processor";
  string  Description = "A logical processor of the hypervisor running on the host computer system.";
  string  ElementName;
  uint16  ResourceType = 3;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Processor";
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits = "percent / 1000";
  uint64  VirtualQuantity = "count";
  uint64  Reservation = 0;
  uint64  Limit = 100000;
  uint32  Weight = 100;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  boolean LimitCPUID;
  uint64  HwThreadsPerCore;
  boolean LimitProcessorFeatures;
  uint64  MaxProcessorsPerNumaNode;
  uint64  MaxNumaNodesPerSocket;
  boolean EnableHostResourceProtection;
  string  CpuGroupId;
  boolean HideHypervisorPresent;
  boolean ExposeVirtualizationExtensions;
};
```

## <a name="members"></a><span data-ttu-id="46dac-107">Membros</span><span class="sxs-lookup"><span data-stu-id="46dac-107">Members</span></span>

<span data-ttu-id="46dac-108">A classe **Msvm \_ ProcessorSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="46dac-108">The **Msvm\_ProcessorSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="46dac-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="46dac-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="46dac-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="46dac-110">Properties</span></span>

<span data-ttu-id="46dac-111">A classe **Msvm \_ ProcessorSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="46dac-111">The **Msvm\_ProcessorSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="46dac-112">**Endereço**</span><span class="sxs-lookup"><span data-stu-id="46dac-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46dac-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-115">O endereço do recurso.</span><span class="sxs-lookup"><span data-stu-id="46dac-115">The address of the resource.</span></span> <span data-ttu-id="46dac-116">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46dac-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46dac-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="46dac-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46dac-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-120">Descreve o endereço deste recurso no contexto do pai.</span><span class="sxs-lookup"><span data-stu-id="46dac-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="46dac-121">As propriedades **pai** e **AddressOnParent** são usadas para descrever a relação do controlador, bem como a ordem dos dispositivos em um controlador.</span><span class="sxs-lookup"><span data-stu-id="46dac-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="46dac-122">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46dac-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46dac-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="46dac-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46dac-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-126">As unidades de alocação usadas pelas propriedades **Reservation** e **Limit** .</span><span class="sxs-lookup"><span data-stu-id="46dac-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="46dac-127">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46dac-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46dac-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="46dac-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-129">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="46dac-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-131">Indica se o recurso será alocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="46dac-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="46dac-132">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46dac-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46dac-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="46dac-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-134">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="46dac-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-136">Indica se o recurso será desalocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="46dac-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="46dac-137">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46dac-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46dac-138">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="46dac-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46dac-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46dac-141">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="46dac-141">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="46dac-142">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="46dac-142">A short description of the object.</span></span> <span data-ttu-id="46dac-143">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="46dac-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="46dac-144">**Conexão**</span><span class="sxs-lookup"><span data-stu-id="46dac-144">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-145">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46dac-145">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="46dac-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-147">O dispositivo ao qual esse recurso está conectado.</span><span class="sxs-lookup"><span data-stu-id="46dac-147">The device to which this resource is connected.</span></span> <span data-ttu-id="46dac-148">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46dac-148">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46dac-149">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="46dac-149">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-150">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46dac-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-152">Descreve a visibilidade do consumidor para o recurso alocado.</span><span class="sxs-lookup"><span data-stu-id="46dac-152">Describes the consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="46dac-153">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46dac-153">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46dac-154">**CpuGroupId**</span><span class="sxs-lookup"><span data-stu-id="46dac-154">**CpuGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46dac-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-157">A ID do grupo de CPU ao qual esta VM está associada.</span><span class="sxs-lookup"><span data-stu-id="46dac-157">The Cpu Group Id this VM is bound to.</span></span> <span data-ttu-id="46dac-158">Quando o valor é 0, isso significa que não está associado a um grupo de CPU específico.</span><span class="sxs-lookup"><span data-stu-id="46dac-158">When value is 0 it means is not bound to a specific CPU group.</span></span>

> [!Note]  
> <span data-ttu-id="46dac-159">Essa propriedade foi adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="46dac-159">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="46dac-160">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="46dac-160">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46dac-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-163">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="46dac-163">A description of the object.</span></span> <span data-ttu-id="46dac-164">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="46dac-164">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="46dac-165">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="46dac-165">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46dac-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-168">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="46dac-168">A display name for the object.</span></span> <span data-ttu-id="46dac-169">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="46dac-169">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="46dac-170">A alteração dessa propriedade alterará a **ElementName** do derivado do dispositivo lógico associado.</span><span class="sxs-lookup"><span data-stu-id="46dac-170">Changing this property will change the **ElementName** of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="46dac-171">**EnableHostResourceProtection**</span><span class="sxs-lookup"><span data-stu-id="46dac-171">**EnableHostResourceProtection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-172">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="46dac-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-174">Indica se a VM deve habilitar recursos que aumentam a proteção dos recursos de host da carga de trabalho em execução na VM.</span><span class="sxs-lookup"><span data-stu-id="46dac-174">Indicates whether the VM should enable features that increase the protection of host resources from workload running in the VM.</span></span>

> [!Note]  
> <span data-ttu-id="46dac-175">Adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="46dac-175">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="46dac-176">**ExposeVirtualizationExtensions**</span><span class="sxs-lookup"><span data-stu-id="46dac-176">**ExposeVirtualizationExtensions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-177">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="46dac-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-179">Indica se o Hyper-V deve expor extensões de virtualização de hardware virtualizadas para a VM.</span><span class="sxs-lookup"><span data-stu-id="46dac-179">Indicates whether Hyper-V should expose virtualized hardware virtualization extensions to the VM.</span></span>

> [!Note]  
> <span data-ttu-id="46dac-180">Essa propriedade foi adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="46dac-180">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="46dac-181">**HideHypervisorPresent**</span><span class="sxs-lookup"><span data-stu-id="46dac-181">**HideHypervisorPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-182">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="46dac-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-184">Indica se o Hyper-V deve relatar que um hipervisor está presente para o convidado aninhado.</span><span class="sxs-lookup"><span data-stu-id="46dac-184">Indicates whether Hyper-V should report that a hypervisor is present to the nested guest.</span></span>

> [!Note]  
> <span data-ttu-id="46dac-185">Essa propriedade foi adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="46dac-185">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="46dac-186">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="46dac-186">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-187">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46dac-187">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="46dac-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-189">Expõe uma atribuição específica para o host ou recursos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="46dac-189">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="46dac-190">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="46dac-190">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="46dac-191">**HwThreadsPerCore**</span><span class="sxs-lookup"><span data-stu-id="46dac-191">**HwThreadsPerCore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-192">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="46dac-192">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-194">Indica o número de threads SMT por núcleo relatados para o convidado.</span><span class="sxs-lookup"><span data-stu-id="46dac-194">Indicates the number of SMT threads per core reported to the guest.</span></span> <span data-ttu-id="46dac-195">Esse relatório não depende se o hardware para SMT está presente.</span><span class="sxs-lookup"><span data-stu-id="46dac-195">This reporting is independent of whether the hardware for SMT is present.</span></span>

> [!Note]  
> <span data-ttu-id="46dac-196">Essa propriedade foi adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="46dac-196">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="46dac-197">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="46dac-197">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-198">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46dac-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46dac-200">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="46dac-200">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="46dac-201">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="46dac-201">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="46dac-202">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="46dac-202">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="46dac-203">**Limite**</span><span class="sxs-lookup"><span data-stu-id="46dac-203">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-204">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="46dac-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-206">A quantidade máxima de recursos de CPU que podem ser consumidos pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="46dac-206">The maximum amount of CPU resources that may be consumed by the virtual machine.</span></span> <span data-ttu-id="46dac-207">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46dac-207">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="46dac-208">100000</span><span class="sxs-lookup"><span data-stu-id="46dac-208">100000</span></span>

<span data-ttu-id="46dac-209">Intervalo: 0 100000</span><span class="sxs-lookup"><span data-stu-id="46dac-209">Range: 0 100000</span></span>

</dd> <dt>

<span data-ttu-id="46dac-210">**LimitCPUID**</span><span class="sxs-lookup"><span data-stu-id="46dac-210">**LimitCPUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-211">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="46dac-211">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-213">Indica se a máquina virtual deve reduzir o identificador de CPU.</span><span class="sxs-lookup"><span data-stu-id="46dac-213">Indicates whether the virtual machine should lower the CPU identifier.</span></span> <span data-ttu-id="46dac-214">Alguns sistemas operacionais mais antigos podem exigir que você limite a funcionalidade do processador dessa maneira para ser executado.</span><span class="sxs-lookup"><span data-stu-id="46dac-214">Some older operating systems may require you to limit processor functionality in this way in order to run.</span></span>

</dd> <dt>

<span data-ttu-id="46dac-215">**LimitProcessorFeatures**</span><span class="sxs-lookup"><span data-stu-id="46dac-215">**LimitProcessorFeatures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-216">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="46dac-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-218">Indica se a máquina virtual deve limitar os recursos de CPU expostos ao sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="46dac-218">Indicates whether the virtual machine should limit the CPU features exposed to the operating system.</span></span> <span data-ttu-id="46dac-219">Limitar os recursos do processador permite que a máquina virtual seja migrada para sistemas de computador host diferentes com processadores diferentes.</span><span class="sxs-lookup"><span data-stu-id="46dac-219">Limiting the processor features enables the virtual machine to be migrated to different host computer systems with different processors.</span></span> <span data-ttu-id="46dac-220">Não há suporte para a migração de máquinas virtuais entre computadores com processadores de fornecedores diferentes.</span><span class="sxs-lookup"><span data-stu-id="46dac-220">Migrating virtual machines between computers with processors from different vendors is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="46dac-221">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="46dac-221">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-222">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46dac-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-223">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-224">Especifica como esse recurso é mapeado para recursos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="46dac-224">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="46dac-225">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46dac-225">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46dac-226">**MaxNumaNodesPerSocket**</span><span class="sxs-lookup"><span data-stu-id="46dac-226">**MaxNumaNodesPerSocket**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-227">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="46dac-227">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-229">O número máximo de nós NUMA que podem ser observados na máquina virtual como pertencente a um único soquete de processador.</span><span class="sxs-lookup"><span data-stu-id="46dac-229">The maximum number of NUMA nodes that can be observed within the virtual machine as belonging to a single processor socket.</span></span>

</dd> <dt>

<span data-ttu-id="46dac-230">**MaxProcessorsPerNumaNode**</span><span class="sxs-lookup"><span data-stu-id="46dac-230">**MaxProcessorsPerNumaNode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-231">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="46dac-231">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-232">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-233">O número máximo de processadores virtuais que podem ser observados na máquina virtual como pertencente a um único nó NUMA virtual.</span><span class="sxs-lookup"><span data-stu-id="46dac-233">The maximum number of virtual processors that can be observed within the virtual machine as belonging to a single virtual NUMA node.</span></span>

</dd> <dt>

<span data-ttu-id="46dac-234">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="46dac-234">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-235">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46dac-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-236">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-237">Uma cadeia de caracteres que descreve o tipo de recurso quando um valor bem definido não está disponível e **ResourceType** tem o valor 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="46dac-237">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="46dac-238">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46dac-238">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46dac-239">**Pai**</span><span class="sxs-lookup"><span data-stu-id="46dac-239">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-240">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46dac-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-242">O pai do recurso.</span><span class="sxs-lookup"><span data-stu-id="46dac-242">The parent of the resource.</span></span> <span data-ttu-id="46dac-243">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46dac-243">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46dac-244">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="46dac-244">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-245">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46dac-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-246">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-247">O identificador do pool de recursos do qual esse recurso foi alocado.</span><span class="sxs-lookup"><span data-stu-id="46dac-247">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="46dac-248">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46dac-248">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46dac-249">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="46dac-249">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-250">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="46dac-250">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-251">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-252">A quantidade de recursos de CPU que são reservados para uso pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="46dac-252">The amount of CPU resources that are reserved for use by the virtual machine.</span></span> <span data-ttu-id="46dac-253">É garantido que esses recursos estejam disponíveis para consumo pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="46dac-253">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="46dac-254">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46dac-254">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="46dac-255">0</span><span class="sxs-lookup"><span data-stu-id="46dac-255">0</span></span>

<span data-ttu-id="46dac-256">Intervalo: 0 100000</span><span class="sxs-lookup"><span data-stu-id="46dac-256">Range: 0 100000</span></span>

</dd> <dt>

<span data-ttu-id="46dac-257">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="46dac-257">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-258">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46dac-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-260">Uma cadeia de caracteres que descreve um subtipo específico de implementação para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="46dac-260">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="46dac-261">Por exemplo, isso pode ser usado para distinguir modelos diferentes do mesmo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="46dac-261">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="46dac-262">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46dac-262">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46dac-263">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="46dac-263">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-264">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46dac-264">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-265">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-266">O tipo de recurso que essa configuração de alocação representa.</span><span class="sxs-lookup"><span data-stu-id="46dac-266">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="46dac-267">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46dac-267">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46dac-268">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="46dac-268">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-269">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="46dac-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-271">O número total de núcleos na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="46dac-271">The total number of cores in the virtual machine.</span></span> <span data-ttu-id="46dac-272">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46dac-272">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46dac-273">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="46dac-273">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-274">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46dac-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-275">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-276">Especifica a unidade de medida para essa alocação de recursos.</span><span class="sxs-lookup"><span data-stu-id="46dac-276">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="46dac-277">O valor dessa propriedade deve ser um valor válido do qualificador de unidades programáticas, conforme definido no anexo C. 1 de DSP0004 V 2.5 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="46dac-277">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="46dac-278">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46dac-278">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46dac-279">**Weight**</span><span class="sxs-lookup"><span data-stu-id="46dac-279">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dac-280">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46dac-280">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46dac-281">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46dac-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dac-282">O peso de cada processador de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="46dac-282">The weight for each virtual machine processor.</span></span> <span data-ttu-id="46dac-283">Depois que todas as reservas forem atendidas, a capacidade física restante do processador da plataforma de hospedagem será alocada às máquinas virtuais com base em seus pesos relativos.</span><span class="sxs-lookup"><span data-stu-id="46dac-283">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="46dac-284">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46dac-284">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="46dac-285">100</span><span class="sxs-lookup"><span data-stu-id="46dac-285">100</span></span>

<span data-ttu-id="46dac-286">Intervalo: 0 10000</span><span class="sxs-lookup"><span data-stu-id="46dac-286">Range: 0 10000</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46dac-287">Comentários</span><span class="sxs-lookup"><span data-stu-id="46dac-287">Remarks</span></span>

<span data-ttu-id="46dac-288">O acesso à classe **Msvm \_ ProcessorSettingData** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="46dac-288">Access to the **Msvm\_ProcessorSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="46dac-289">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="46dac-289">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="46dac-290">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46dac-290">Requirements</span></span>



| <span data-ttu-id="46dac-291">Requisito</span><span class="sxs-lookup"><span data-stu-id="46dac-291">Requirement</span></span> | <span data-ttu-id="46dac-292">Valor</span><span class="sxs-lookup"><span data-stu-id="46dac-292">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46dac-293">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46dac-293">Minimum supported client</span></span><br/> | <span data-ttu-id="46dac-294">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="46dac-294">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="46dac-295">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46dac-295">Minimum supported server</span></span><br/> | <span data-ttu-id="46dac-296">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="46dac-296">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="46dac-297">Namespace</span><span class="sxs-lookup"><span data-stu-id="46dac-297">Namespace</span></span><br/>                | <span data-ttu-id="46dac-298">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="46dac-298">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="46dac-299">MOF</span><span class="sxs-lookup"><span data-stu-id="46dac-299">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46dac-300"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46dac-300"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="46dac-301">DLL</span><span class="sxs-lookup"><span data-stu-id="46dac-301">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46dac-302"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="46dac-302"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="46dac-303">Confira também</span><span class="sxs-lookup"><span data-stu-id="46dac-303">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46dac-304">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="46dac-304">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="46dac-305">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="46dac-305">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="46dac-306">Classes de processador</span><span class="sxs-lookup"><span data-stu-id="46dac-306">Processor Classes</span></span>](processor-classes.md)
</dt> </dl>

 

