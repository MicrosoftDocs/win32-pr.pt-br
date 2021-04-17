---
description: Representa o estado configurado do componente de interface do serviço de convidado.
ms.assetid: 82B58459-9819-4F51-BEE5-AB57E444CF55
title: Classe Msvm_GuestServiceInterfaceComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponentSettingData
- Msvm_GuestServiceInterfaceComponentSettingData.ElementName
- Msvm_GuestServiceInterfaceComponentSettingData.InstanceID
- Msvm_GuestServiceInterfaceComponentSettingData.ResourceType
- Msvm_GuestServiceInterfaceComponentSettingData.OtherResourceType
- Msvm_GuestServiceInterfaceComponentSettingData.ResourceSubType
- Msvm_GuestServiceInterfaceComponentSettingData.PoolID
- Msvm_GuestServiceInterfaceComponentSettingData.ConsumerVisibility
- Msvm_GuestServiceInterfaceComponentSettingData.HostResource
- Msvm_GuestServiceInterfaceComponentSettingData.AllocationUnits
- Msvm_GuestServiceInterfaceComponentSettingData.VirtualQuantity
- Msvm_GuestServiceInterfaceComponentSettingData.Reservation
- Msvm_GuestServiceInterfaceComponentSettingData.Limit
- Msvm_GuestServiceInterfaceComponentSettingData.Weight
- Msvm_GuestServiceInterfaceComponentSettingData.AutomaticAllocation
- Msvm_GuestServiceInterfaceComponentSettingData.AutomaticDeallocation
- Msvm_GuestServiceInterfaceComponentSettingData.Parent
- Msvm_GuestServiceInterfaceComponentSettingData.Connection
- Msvm_GuestServiceInterfaceComponentSettingData.Address
- Msvm_GuestServiceInterfaceComponentSettingData.MappingBehavior
- Msvm_GuestServiceInterfaceComponentSettingData.EnabledState
- Msvm_GuestServiceInterfaceComponentSettingData.DefaultEnabledStatePolicy
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ada39e4428040cf7e6732232ce789f7d837c9c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783295"
---
# <a name="msvm_guestserviceinterfacecomponentsettingdata-class"></a><span data-ttu-id="6f224-103">\_Classe Msvm GuestServiceInterfaceComponentSettingData</span><span class="sxs-lookup"><span data-stu-id="6f224-103">Msvm\_GuestServiceInterfaceComponentSettingData class</span></span>

<span data-ttu-id="6f224-104">Representa o estado configurado do componente de interface do serviço de convidado.</span><span class="sxs-lookup"><span data-stu-id="6f224-104">Represents the configured state of the guest service interface component.</span></span> <span data-ttu-id="6f224-105">Essa classe deriva da classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) .</span><span class="sxs-lookup"><span data-stu-id="6f224-105">This class derives from the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class.</span></span>

<span data-ttu-id="6f224-106">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="6f224-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f224-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f224-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  ElementName;
  string  InstanceID;
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
  uint16  EnabledState = 3;
  uint16  DefaultEnabledStatePolicy = 2;
};
```

## <a name="members"></a><span data-ttu-id="6f224-108">Membros</span><span class="sxs-lookup"><span data-stu-id="6f224-108">Members</span></span>

<span data-ttu-id="6f224-109">A classe **Msvm \_ GuestServiceInterfaceComponentSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6f224-109">The **Msvm\_GuestServiceInterfaceComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="6f224-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6f224-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6f224-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6f224-111">Properties</span></span>

<span data-ttu-id="6f224-112">A classe **Msvm \_ GuestServiceInterfaceComponentSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6f224-112">The **Msvm\_GuestServiceInterfaceComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f224-113">**Endereço**</span><span class="sxs-lookup"><span data-stu-id="6f224-113">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f224-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6f224-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f224-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f224-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f224-116">O endereço do recurso.</span><span class="sxs-lookup"><span data-stu-id="6f224-116">The address of the resource.</span></span> <span data-ttu-id="6f224-117">Por exemplo, o endereço MAC de uma porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="6f224-117">For example, the MAC address of a Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="6f224-118">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="6f224-118">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f224-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6f224-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f224-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f224-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f224-121">Essa propriedade especifica as unidades de alocação usadas pelas propriedades Reservation e Limit.</span><span class="sxs-lookup"><span data-stu-id="6f224-121">This property specifies the units of allocation used by the Reservation and Limit properties.</span></span> <span data-ttu-id="6f224-122">Por exemplo, quando ResourceType = Processor, AllocationUnits pode ser definido como MHz.</span><span class="sxs-lookup"><span data-stu-id="6f224-122">For example, when ResourceType=Processor, AllocationUnits may be set to MHz.</span></span> <span data-ttu-id="6f224-123">Quando ResourceType = Memory, AllocationUnits pode ser definido como MB</span><span class="sxs-lookup"><span data-stu-id="6f224-123">When ResourceType=Memory, AllocationUnits may be set to MB</span></span>

</dd> <dt>

<span data-ttu-id="6f224-124">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="6f224-124">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f224-125">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6f224-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6f224-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f224-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f224-127">Esta propriedade especifica se o recurso será alocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="6f224-127">This property specifies if the resource will be automatically allocated.</span></span> <span data-ttu-id="6f224-128">Por exemplo, quando definido como true, quando o sistema de máquina virtual de consumo estiver ligado, esse recurso será alocado.</span><span class="sxs-lookup"><span data-stu-id="6f224-128">For example when set to true, when the consuming virtual computer system is powered on, this resource would be allocated.</span></span> <span data-ttu-id="6f224-129">Um valor false indica que o recurso deve ser alocado explicitamente.</span><span class="sxs-lookup"><span data-stu-id="6f224-129">A value of false indicates the resource must be explicitly allocated.</span></span> <span data-ttu-id="6f224-130">Por exemplo, a configuração pode representar mídia removível (ou seja, cdrom ou disquete) em que, no momento da ativação, a mídia não está presente.</span><span class="sxs-lookup"><span data-stu-id="6f224-130">For example, the setting may represent removable media (that is, cdrom or floppy) where at power on time, the media is not present.</span></span> <span data-ttu-id="6f224-131">Uma operação explícita é necessária para alocar o recurso.</span><span class="sxs-lookup"><span data-stu-id="6f224-131">An explicit operation is required to allocate the resource.</span></span>

</dd> <dt>

<span data-ttu-id="6f224-132">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="6f224-132">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f224-133">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6f224-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6f224-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f224-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f224-135">Esta propriedade especifica se o recurso será desalocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="6f224-135">This property specifies if the resource will be automatically deallocated.</span></span> <span data-ttu-id="6f224-136">Por exemplo, quando definido como true, quando o sistema de máquina virtual de consumo é desligado, esse recurso seria desalocado.</span><span class="sxs-lookup"><span data-stu-id="6f224-136">For example, when set to true, when the consuming virtual computer system is powered off, this resource would be deallocated.</span></span> <span data-ttu-id="6f224-137">Quando definido como false, o recurso permanecerá alocado e deverá ser explicitamente desalocado.</span><span class="sxs-lookup"><span data-stu-id="6f224-137">When set to false, the resource will remain allocated and must be explicitly deallocated.</span></span>

</dd> <dt>

<span data-ttu-id="6f224-138">**Conexão**</span><span class="sxs-lookup"><span data-stu-id="6f224-138">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f224-139">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6f224-139">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6f224-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f224-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f224-141">A coisa à qual esse recurso está conectado.</span><span class="sxs-lookup"><span data-stu-id="6f224-141">The thing to which this resource is connected.</span></span> <span data-ttu-id="6f224-142">Por exemplo, uma rede nomeada ou porta de comutador.</span><span class="sxs-lookup"><span data-stu-id="6f224-142">For example, a named network or switch port.</span></span>

</dd> <dt>

<span data-ttu-id="6f224-143">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="6f224-143">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f224-144">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f224-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f224-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f224-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f224-146">Descreve a visibilidade dos consumidores para o recurso alocado.</span><span class="sxs-lookup"><span data-stu-id="6f224-146">Describes the consumers visibility to the allocated resource.</span></span>



| <span data-ttu-id="6f224-147">Valor</span><span class="sxs-lookup"><span data-stu-id="6f224-147">Value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="6f224-148">Significado</span><span class="sxs-lookup"><span data-stu-id="6f224-148">Meaning</span></span>                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="6f224-149"><dt></dt> <dt>0</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="6f224-149"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                            | <span data-ttu-id="6f224-150">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="6f224-150">Unknown.</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span><dl> <span data-ttu-id="6f224-151"><dt>**Aprovado por**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6f224-151"><dt>**Passed-Through**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="6f224-152">O recurso de host ou subjacente é utilizado e passado para o consumidor, possivelmente usando o particionamento.</span><span class="sxs-lookup"><span data-stu-id="6f224-152">The underlying or host resource is utilized and passed through to the consumer, possibly using partitioning.</span></span> <span data-ttu-id="6f224-153">Pelo menos um item deve estar presente na propriedade DeviceID.</span><span class="sxs-lookup"><span data-stu-id="6f224-153">At least one item shall be present in the DeviceID property.</span></span><br/>                                                                        |
| <span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span><dl> <span data-ttu-id="6f224-154"><dt>**Virtualizado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6f224-154"><dt>**Virtualized**</dt> <dt>3</dt></span></span> </dl>                            | <span data-ttu-id="6f224-155">O recurso é virtualizado e não pode ser mapeado diretamente para um recurso de host/base.</span><span class="sxs-lookup"><span data-stu-id="6f224-155">The resource is virtualized and may not map directly to an underlying/host resource.</span></span> <span data-ttu-id="6f224-156">Algumas implementações podem dar suporte a uma atribuição específica para recursos virtualizados; nesse caso, os recursos do host são expostos usando a propriedade DeviceID.</span><span class="sxs-lookup"><span data-stu-id="6f224-156">Some implementations may support specific assignment for virtualized resources, in which case the host resource(s) are exposed using the DeviceID property.</span></span><br/> |
| <span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span><dl> <span data-ttu-id="6f224-157"><dt>**Não representado**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="6f224-157"><dt>**Not represented**</dt> <dt>4</dt></span></span> </dl>            | <span data-ttu-id="6f224-158">Uma representação do recurso não existe no contexto do consumidor do recurso.</span><span class="sxs-lookup"><span data-stu-id="6f224-158">A representation of the resource does not exist within the context of the resource consumer.</span></span><br/>                                                                                                                                                     |
| <span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="6f224-159"><dt>**DMTF reservado**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="6f224-159"><dt>**DMTF reserved**</dt> <dt>..</dt></span></span> </dl>                   |                                                                                                                                                                                                                                                             |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="6f224-160">O <dt>**fornecedor reservou**</dt> <dt>32767.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="6f224-160"><dt>**Vendor Reserved**</dt> <dt>32767..65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="6f224-161">**DefaultEnabledStatePolicy**</span><span class="sxs-lookup"><span data-stu-id="6f224-161">**DefaultEnabledStatePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f224-162">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f224-162">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f224-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f224-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f224-164">Os Estados habilitado e desabilitado dos serviços de comunicação de convidado por padrão.</span><span class="sxs-lookup"><span data-stu-id="6f224-164">The enabled and disabled states of guest communication services by default.</span></span>

<span data-ttu-id="6f224-165">Esta é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="6f224-165">This is a read-only property, but it can be changed using the [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="6f224-166">Adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="6f224-166">Added in Windows 10.</span></span>

 

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6f224-167">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="6f224-167">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6f224-168">**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="6f224-168">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6f224-169">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="6f224-169">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f224-170">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6f224-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f224-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f224-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f224-172">O nome de exibição para esta instância de SettingData.</span><span class="sxs-lookup"><span data-stu-id="6f224-172">The display name for this instance of SettingData.</span></span> <span data-ttu-id="6f224-173">Além disso, o nome de exibição pode ser usado como uma propriedade de índice para uma pesquisa ou consulta.</span><span class="sxs-lookup"><span data-stu-id="6f224-173">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="6f224-174">(Observação: o nome não precisa ser exclusivo em um namespace.)</span><span class="sxs-lookup"><span data-stu-id="6f224-174">(Note: The name does not have to be unique within a namespace.)</span></span>

</dd> <dt>

<span data-ttu-id="6f224-175">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="6f224-175">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f224-176">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f224-176">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f224-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f224-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f224-178">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="6f224-178">The enabled and disabled states of an element.</span></span>

<span data-ttu-id="6f224-179">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) (ou [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) no Windows 10 ou posterior) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="6f224-179">This is a read-only property, but it can be changed by using the [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) method (or [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) in Windows 10 or later) of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="6f224-180">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="6f224-180">Valid values are:</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6f224-181">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="6f224-181">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6f224-182">**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="6f224-182">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6f224-183">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="6f224-183">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f224-184">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6f224-184">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6f224-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f224-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f224-186">Essa propriedade expõe uma atribuição específica ao host ou a recursos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="6f224-186">This property exposes specific assignment to host or underlying resources.</span></span> <span data-ttu-id="6f224-187">As instâncias inseridas devem conter apenas as propriedades de chave e ser tratadas como caminhos de objeto.</span><span class="sxs-lookup"><span data-stu-id="6f224-187">The embedded instances shall contain only key properties and be treated as Object Paths.</span></span> <span data-ttu-id="6f224-188">Se o recurso virtual puder ser agendado em vários recursos subjacentes, essa propriedade deverá permanecer **nula**.</span><span class="sxs-lookup"><span data-stu-id="6f224-188">If the virtual resource may be scheduled on a number of underlying resources, this property should remain **NULL**.</span></span> <span data-ttu-id="6f224-189">Nesse caso, as associações DeviceAllocatedFromPool ou ResourceAllocationFromPool podem ser usadas para determinar o pool de recursos do host no qual esse recurso virtual pode ser agendado.</span><span class="sxs-lookup"><span data-stu-id="6f224-189">In that case, the DeviceAllocatedFromPool or ResourceAllocationFromPool associations may be used to determine the pool of host resources on which this virtual resource may be scheduled.</span></span> <span data-ttu-id="6f224-190">Se uma atribuição específica for utilizada, todos os recursos subjacentes usados por esse recurso virtual deverão ser listados nessa matriz.</span><span class="sxs-lookup"><span data-stu-id="6f224-190">If specific assignment is utilized, all underlying resources used by this virtual resource shall be listed in this array.</span></span> <span data-ttu-id="6f224-191">Normalmente, a matriz conterá um item, no entanto, para alocações agregadas, como vários processadores, vários recursos de host poderão ser especificados.</span><span class="sxs-lookup"><span data-stu-id="6f224-191">Typically, the array will contain one item, however for aggregate allocations, such as multiple processors, multiple host resources may be specified.</span></span>

</dd> <dt>

<span data-ttu-id="6f224-192">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6f224-192">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f224-193">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6f224-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f224-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f224-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f224-195">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="6f224-195">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6f224-196">Dentro do escopo do namespace de instanciação, a InstanceID identifica de forma opaca e exclusiva uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="6f224-196">Within the scope of the instantiating Namespace, InstanceID opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="6f224-197">Para garantir a exclusividade no NameSpace, o valor de InstanceID deve ser construído usando o seguinte algoritmo "preferencial": *OrgID*:*LocalId* em que *OrgID* e *LocalId* são separados por dois-pontos (:) e onde *OrgID* deve incluir um nome de direitos autorais, com marca registrada ou exclusivo que pertença à entidade de negócios que está criando ou definindo a InstanceId ou que é uma ID registrada atribuída à entidade de negócios por uma autoridade global reconhecida.</span><span class="sxs-lookup"><span data-stu-id="6f224-197">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm: *OrgID*:*LocalID* Where *OrgID* and *LocalID* are separated by a colon (:), and where *OrgID* must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="6f224-198">(Esse requisito é semelhante ao *SchemaName* \_ Estrutura *ClassName* de nomes de classe de esquema.) Além disso, para garantir a exclusividade, *OrgID* não deve conter dois-pontos (:).</span><span class="sxs-lookup"><span data-stu-id="6f224-198">(This requirement is similar to the *SchemaName*\_*ClassName* structure of Schema class names.) In addition, to ensure uniqueness, *OrgID* must not contain a colon (:).</span></span> <span data-ttu-id="6f224-199">Ao usar esse algoritmo, os primeiros dois-pontos para aparecer em InstanceID devem aparecer entre *OrgID* e *LocalId*.</span><span class="sxs-lookup"><span data-stu-id="6f224-199">When using this algorithm, the first colon to appear in InstanceID must appear between *OrgID* and *LocalID*.</span></span> <span data-ttu-id="6f224-200">A *LocalId* é escolhida pela entidade de negócios e não deve ser reutilizada para identificar elementos subjacentes (reais) diferentes.</span><span class="sxs-lookup"><span data-stu-id="6f224-200">*LocalID* is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="6f224-201">Se o algoritmo "preferencial" acima não for usado, a entidade de definição deverá garantir que a InstanceID resultante não seja reutilizada em quaisquer InstanceIDs produzidas por este ou outros provedores para o NameSpace dessa instância.</span><span class="sxs-lookup"><span data-stu-id="6f224-201">If the above "preferred" algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span> <span data-ttu-id="6f224-202">Para instâncias definidas por DMTF, o algoritmo "preferencial" deve ser usado com o *OrgID* definido como CIM.</span><span class="sxs-lookup"><span data-stu-id="6f224-202">For DMTF-defined instances, the "preferred" algorithm must be used with the *OrgID* set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="6f224-203">**Limite**</span><span class="sxs-lookup"><span data-stu-id="6f224-203">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f224-204">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6f224-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6f224-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f224-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f224-206">Esta propriedade especifica o limite superior ou a quantidade máxima de recursos que serão concedidos para essa alocação.</span><span class="sxs-lookup"><span data-stu-id="6f224-206">This property specifies the upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="6f224-207">Por exemplo, um sistema que dá suporte à paginação de memória pode dar suporte à definição do limite de uma alocação de memória abaixo do VirtualQuantity, forçando assim a ocorrência da paginação para essa alocação.</span><span class="sxs-lookup"><span data-stu-id="6f224-207">For example, a system which supports memory paging may support setting the Limit of a Memory allocation below that of the VirtualQuantity, thus forcing paging to occur for this allocation.</span></span>

</dd> <dt>

<span data-ttu-id="6f224-208">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="6f224-208">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f224-209">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f224-209">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f224-210">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f224-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f224-211">Especifica como esse recurso é mapeado para recursos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="6f224-211">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="6f224-212">Se a matriz HostResource contiver entradas, essa propriedade refletirá como o recurso é mapeado para esses recursos específicos.</span><span class="sxs-lookup"><span data-stu-id="6f224-212">If the HostResource array contains any entries, this property reflects how the resource maps to those specific resources.</span></span>

<dl> <dt>

<span data-ttu-id="6f224-213"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="6f224-213"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-214"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="6f224-214"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-215"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (2)</span><span class="sxs-lookup"><span data-stu-id="6f224-215"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-216"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Afinidade flexível** (3)</span><span class="sxs-lookup"><span data-stu-id="6f224-216"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Soft Affinity** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-217"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Afinidade rígida** (4)</span><span class="sxs-lookup"><span data-stu-id="6f224-217"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Hard Affinity** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="6f224-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-219"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="6f224-219"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32767..65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6f224-220">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="6f224-220">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f224-221">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6f224-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f224-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f224-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f224-223">Uma cadeia de caracteres que descreve o tipo de recurso quando um valor bem definido não está disponível e ResourceType tem o valor "other".</span><span class="sxs-lookup"><span data-stu-id="6f224-223">A string that describes the resource type when a well defined value is not available and ResourceType has the value "Other".</span></span>

</dd> <dt>

<span data-ttu-id="6f224-224">**Pai**</span><span class="sxs-lookup"><span data-stu-id="6f224-224">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f224-225">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6f224-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f224-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f224-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f224-227">O pai do recurso.</span><span class="sxs-lookup"><span data-stu-id="6f224-227">The Parent of the resource.</span></span> <span data-ttu-id="6f224-228">Por exemplo, um controlador para a alocação atual.</span><span class="sxs-lookup"><span data-stu-id="6f224-228">For example, a controller for the current allocation.</span></span>

</dd> <dt>

<span data-ttu-id="6f224-229">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="6f224-229">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f224-230">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6f224-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f224-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f224-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f224-232">Essa propriedade especifica para qual ResourcePool o recurso está alocado no momento ou qual ResourcePool o recurso será alocado quando a alocação ocorrer.</span><span class="sxs-lookup"><span data-stu-id="6f224-232">This property specifies which ResourcePool the resource is currently allocated from, or which ResourcePool the resource will be allocated from when the allocation occurs.</span></span>

</dd> <dt>

<span data-ttu-id="6f224-233">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="6f224-233">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f224-234">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6f224-234">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6f224-235">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f224-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f224-236">Esta propriedade especifica a quantidade de recursos garantidos que estarão disponíveis para essa alocação.</span><span class="sxs-lookup"><span data-stu-id="6f224-236">This property specifies the amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="6f224-237">No sistema que dá suporte ao comprometimento excessivo de recursos, esse valor normalmente é usado para o controle de admissão para impedir que uma alocação seja aceita, impedindo assim o esgotamento de recursos.</span><span class="sxs-lookup"><span data-stu-id="6f224-237">On system which support over-commitment of resources, this value is typically used for admission control to prevent an an allocation from being accepted thus preventing resource depletion.</span></span>

</dd> <dt>

<span data-ttu-id="6f224-238">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="6f224-238">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f224-239">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6f224-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f224-240">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f224-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f224-241">Uma cadeia de caracteres que descreve um subtipo específico de implementação para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="6f224-241">A string describing an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="6f224-242">Por exemplo, isso pode ser usado para distinguir modelos diferentes do mesmo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="6f224-242">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="6f224-243">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="6f224-243">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f224-244">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f224-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f224-245">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f224-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f224-246">O tipo de recurso que essa configuração de alocação representa.</span><span class="sxs-lookup"><span data-stu-id="6f224-246">The type of resource this allocation setting represents.</span></span>

<dl> <dt>

<span data-ttu-id="6f224-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="6f224-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-248"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Sistema de computador** (2)</span><span class="sxs-lookup"><span data-stu-id="6f224-248"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-249"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processador** (3)</span><span class="sxs-lookup"><span data-stu-id="6f224-249"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-250"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memória** (4)</span><span class="sxs-lookup"><span data-stu-id="6f224-250"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-251"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controlador IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="6f224-251"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-252"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI paralelo** (6)</span><span class="sxs-lookup"><span data-stu-id="6f224-252"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-253"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="6f224-253"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-254"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="6f224-254"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-255"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="6f224-255"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-256"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Adaptador Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="6f224-256"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-257"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Outro adaptador de rede** (11)</span><span class="sxs-lookup"><span data-stu-id="6f224-257"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-258"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Slot de e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="6f224-258"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-259"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo de e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="6f224-259"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-260"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Unidade de disquete** (14)</span><span class="sxs-lookup"><span data-stu-id="6f224-260"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-261"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unidade de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="6f224-261"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-262"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unidade de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="6f224-262"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-263"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Porta serial** (17)</span><span class="sxs-lookup"><span data-stu-id="6f224-263"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (17)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-264"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Porta paralela** (18)</span><span class="sxs-lookup"><span data-stu-id="6f224-264"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (18)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-265"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controlador USB** (19)</span><span class="sxs-lookup"><span data-stu-id="6f224-265"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (19)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-266"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controlador de gráficos** (20)</span><span class="sxs-lookup"><span data-stu-id="6f224-266"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (20)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-267"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extensão de armazenamento** (21)</span><span class="sxs-lookup"><span data-stu-id="6f224-267"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (21)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-268"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disco** (22)</span><span class="sxs-lookup"><span data-stu-id="6f224-268"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disk** (22)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-269"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Fita** (23)</span><span class="sxs-lookup"><span data-stu-id="6f224-269"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Tape** (23)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-270"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Outro dispositivo de armazenamento** (24)</span><span class="sxs-lookup"><span data-stu-id="6f224-270"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (24)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-271"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Controlador FireWire** (25)</span><span class="sxs-lookup"><span data-stu-id="6f224-271"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-272"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unidade particionável** (26)</span><span class="sxs-lookup"><span data-stu-id="6f224-272"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-273"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unidade particionável de base** (27)</span><span class="sxs-lookup"><span data-stu-id="6f224-273"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-274"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Fonte de energia** (28)</span><span class="sxs-lookup"><span data-stu-id="6f224-274"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-275"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Dispositivo de resfriamento** (29)</span><span class="sxs-lookup"><span data-stu-id="6f224-275"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-276"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="6f224-276"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6f224-277"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="6f224-277"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32767..65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6f224-278">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="6f224-278">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f224-279">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6f224-279">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6f224-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f224-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f224-281">Essa propriedade especifica a quantidade de recursos apresentados ao consumidor.</span><span class="sxs-lookup"><span data-stu-id="6f224-281">This property specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="6f224-282">Por exemplo, quando ResourceType = processador, essa propriedade refletiria o número de processadores discretos apresentados ao sistema de computador virtual.</span><span class="sxs-lookup"><span data-stu-id="6f224-282">For example, when ResourceType=Processor, this property would reflect the number of discrete Processors presented to the virtual computer system.</span></span> <span data-ttu-id="6f224-283">Quando ResourceType = Memory, essa propriedade pode refletir o número de MB relatados para o sistema de computador virtual.</span><span class="sxs-lookup"><span data-stu-id="6f224-283">When ResourceType=Memory, this property could reflect the number of MB reported to the virtual computer system.</span></span>

</dd> <dt>

<span data-ttu-id="6f224-284">**Weight**</span><span class="sxs-lookup"><span data-stu-id="6f224-284">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f224-285">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6f224-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f224-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f224-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f224-287">Esta propriedade especifica uma prioridade relativa para essa alocação em relação a outras alocações do mesmo ResourcePool.</span><span class="sxs-lookup"><span data-stu-id="6f224-287">This property specifies a relative priority for this allocation in relation to other allocations from the same ResourcePool.</span></span> <span data-ttu-id="6f224-288">Essa propriedade não tem nenhuma unidade de medida e só é relevante quando comparada com outras alocações que conpetem para os mesmos recursos do host.</span><span class="sxs-lookup"><span data-stu-id="6f224-288">This property has no unit of measure, and is only relevant when compared to other allocations competing for the same host resources.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f224-289">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f224-289">Requirements</span></span>



| <span data-ttu-id="6f224-290">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f224-290">Requirement</span></span> | <span data-ttu-id="6f224-291">Valor</span><span class="sxs-lookup"><span data-stu-id="6f224-291">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f224-292">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f224-292">Minimum supported client</span></span><br/> | <span data-ttu-id="6f224-293">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6f224-293">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="6f224-294">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f224-294">Minimum supported server</span></span><br/> | <span data-ttu-id="6f224-295">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="6f224-295">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6f224-296">Namespace</span><span class="sxs-lookup"><span data-stu-id="6f224-296">Namespace</span></span><br/>                | <span data-ttu-id="6f224-297">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="6f224-297">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6f224-298">MOF</span><span class="sxs-lookup"><span data-stu-id="6f224-298">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f224-299"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f224-299"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f224-300">DLL</span><span class="sxs-lookup"><span data-stu-id="6f224-300">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f224-301"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6f224-301"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6f224-302">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f224-302">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f224-303">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="6f224-303">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="6f224-304">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="6f224-304">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

