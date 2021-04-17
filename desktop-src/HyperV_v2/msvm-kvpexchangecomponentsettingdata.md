---
description: Representa o estado configurado do serviço de troca de pares chave/valor.
ms.assetid: B7ED1091-E49A-4C38-9794-E074E6B9EF48
title: Classe Msvm_KvpExchangeComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeComponentSettingData
- Msvm_KvpExchangeComponentSettingData.DisableHostKVPItems
- Msvm_KvpExchangeComponentSettingData.InstanceID
- Msvm_KvpExchangeComponentSettingData.Caption
- Msvm_KvpExchangeComponentSettingData.Description
- Msvm_KvpExchangeComponentSettingData.ElementName
- Msvm_KvpExchangeComponentSettingData.ResourceType
- Msvm_KvpExchangeComponentSettingData.OtherResourceType
- Msvm_KvpExchangeComponentSettingData.ResourceSubType
- Msvm_KvpExchangeComponentSettingData.PoolID
- Msvm_KvpExchangeComponentSettingData.ConsumerVisibility
- Msvm_KvpExchangeComponentSettingData.HostResource
- Msvm_KvpExchangeComponentSettingData.AllocationUnits
- Msvm_KvpExchangeComponentSettingData.VirtualQuantity
- Msvm_KvpExchangeComponentSettingData.Reservation
- Msvm_KvpExchangeComponentSettingData.Limit
- Msvm_KvpExchangeComponentSettingData.Weight
- Msvm_KvpExchangeComponentSettingData.AutomaticAllocation
- Msvm_KvpExchangeComponentSettingData.AutomaticDeallocation
- Msvm_KvpExchangeComponentSettingData.Parent
- Msvm_KvpExchangeComponentSettingData.Connection
- Msvm_KvpExchangeComponentSettingData.Address
- Msvm_KvpExchangeComponentSettingData.MappingBehavior
- Msvm_KvpExchangeComponentSettingData.AddressOnParent
- Msvm_KvpExchangeComponentSettingData.VirtualQuantityUnits
- Msvm_KvpExchangeComponentSettingData.EnabledState
- Msvm_KvpExchangeComponentSettingData.HostExchangeItems
- Msvm_KvpExchangeComponentSettingData.HostOnlyItems
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2fe2ef128d3212ba2dfd47a3d71f713c26ba2435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754666"
---
# <a name="msvm_kvpexchangecomponentsettingdata-class"></a><span data-ttu-id="eba27-103">\_Classe Msvm KvpExchangeComponentSettingData</span><span class="sxs-lookup"><span data-stu-id="eba27-103">Msvm\_KvpExchangeComponentSettingData class</span></span>

<span data-ttu-id="eba27-104">Representa o estado configurado do serviço de troca de pares chave/valor.</span><span class="sxs-lookup"><span data-stu-id="eba27-104">Represents the configured state of the key/value pair exchange service.</span></span>

<span data-ttu-id="eba27-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="eba27-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eba27-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eba27-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_KvpExchangeComponentSettingData : CIM_ResourceAllocationSettingData
{
  boolean DisableHostKVPItems;
  string  InstanceID;
  string  Caption = "Key-Value Pair Exchange";
  string  Description = "Microsoft Key-Value Pair Exchange Service Setting Data";
  string  ElementName = "Key-Value Pair Exchange";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:Key-Value Pair Exchange Component";
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
  String  HostExchangeItems[];
  String  HostOnlyItems[];
};
```

## <a name="members"></a><span data-ttu-id="eba27-107">Membros</span><span class="sxs-lookup"><span data-stu-id="eba27-107">Members</span></span>

<span data-ttu-id="eba27-108">A classe **Msvm \_ KvpExchangeComponentSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="eba27-108">The **Msvm\_KvpExchangeComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="eba27-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="eba27-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eba27-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="eba27-110">Properties</span></span>

<span data-ttu-id="eba27-111">A classe **Msvm \_ KvpExchangeComponentSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="eba27-111">The **Msvm\_KvpExchangeComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eba27-112">**Endereço**</span><span class="sxs-lookup"><span data-stu-id="eba27-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eba27-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eba27-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eba27-115">O endereço do recurso.</span><span class="sxs-lookup"><span data-stu-id="eba27-115">The address of the resource.</span></span> <span data-ttu-id="eba27-116">Essa propriedade é herdada de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e sempre é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="eba27-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="eba27-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="eba27-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eba27-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eba27-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eba27-120">Descreve o endereço deste recurso no contexto do pai.</span><span class="sxs-lookup"><span data-stu-id="eba27-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="eba27-121">As propriedades **pai** e **AddressOnParent** são usadas para descrever a relação do controlador, bem como a ordem dos dispositivos em um controlador.</span><span class="sxs-lookup"><span data-stu-id="eba27-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="eba27-122">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="eba27-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="eba27-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="eba27-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eba27-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eba27-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eba27-126">As unidades de alocação usadas pelas propriedades **Reservation** e **Limit** .</span><span class="sxs-lookup"><span data-stu-id="eba27-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="eba27-127">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="eba27-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="eba27-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="eba27-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-129">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="eba27-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eba27-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eba27-131">Indica se o recurso será alocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="eba27-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="eba27-132">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="eba27-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="eba27-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="eba27-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-134">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="eba27-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eba27-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eba27-136">Indica se o recurso será desalocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="eba27-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="eba27-137">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="eba27-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="eba27-138">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="eba27-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eba27-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eba27-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eba27-141">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="eba27-141">A short description of the object.</span></span> <span data-ttu-id="eba27-142">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="eba27-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="eba27-143">**Conexão**</span><span class="sxs-lookup"><span data-stu-id="eba27-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-144">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eba27-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="eba27-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eba27-146">A coisa à qual esse recurso está conectado.</span><span class="sxs-lookup"><span data-stu-id="eba27-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="eba27-147">Essa propriedade é herdada de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e sempre é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="eba27-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="eba27-148">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="eba27-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-149">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eba27-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eba27-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eba27-151">A visibilidade dos consumidores para o recurso alocado.</span><span class="sxs-lookup"><span data-stu-id="eba27-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="eba27-152">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="eba27-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="eba27-153">Valor</span><span class="sxs-lookup"><span data-stu-id="eba27-153">Value</span></span>                                                                        | <span data-ttu-id="eba27-154">Significado</span><span class="sxs-lookup"><span data-stu-id="eba27-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="eba27-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="eba27-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="eba27-156">Virtualizado</span><span class="sxs-lookup"><span data-stu-id="eba27-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="eba27-157">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="eba27-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eba27-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eba27-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eba27-160">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="eba27-160">A description of the object.</span></span> <span data-ttu-id="eba27-161">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="eba27-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="eba27-162">**DisableHostKVPItems**</span><span class="sxs-lookup"><span data-stu-id="eba27-162">**DisableHostKVPItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-163">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="eba27-163">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eba27-164">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eba27-164">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="eba27-165">Essa propriedade desabilita o host de populatinghost automaticamente o nome e as informações do sistema operacional dentro do convidado.</span><span class="sxs-lookup"><span data-stu-id="eba27-165">This property disables the host from automatically populatinghost name and OS information inside the guest.</span></span>

> [!Note]  
> <span data-ttu-id="eba27-166">Essa propriedade foi adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="eba27-166">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="eba27-167">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="eba27-167">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eba27-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eba27-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eba27-170">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="eba27-170">A display name for the object.</span></span> <span data-ttu-id="eba27-171">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="eba27-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="eba27-172">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="eba27-172">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-173">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eba27-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eba27-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eba27-175">O estado habilitado do elemento.</span><span class="sxs-lookup"><span data-stu-id="eba27-175">The enabled state of the element.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="eba27-176">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="eba27-176">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="eba27-177">**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="eba27-177">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eba27-178">**HostExchangeItems**</span><span class="sxs-lookup"><span data-stu-id="eba27-178">**HostExchangeItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-179">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eba27-179">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="eba27-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eba27-181">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), **HyperVEmbeddedInstance** ("Msvm \_ KvpExchangeDataItem")</span><span class="sxs-lookup"><span data-stu-id="eba27-181">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="eba27-182">Uma matriz de instâncias [**Msvm \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) inseridas que representam os pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="eba27-182">An array of embedded [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances that represent the key/value pairs.</span></span>

</dd> <dt>

<span data-ttu-id="eba27-183">**HostOnlyItems**</span><span class="sxs-lookup"><span data-stu-id="eba27-183">**HostOnlyItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-184">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eba27-184">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="eba27-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eba27-186">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), **HyperVEmbeddedInstance** ("Msvm \_ KvpExchangeDataItem")</span><span class="sxs-lookup"><span data-stu-id="eba27-186">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="eba27-187">Uma matriz de instâncias [**Msvm \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) que contém os pares de chave/valor que são armazenados no arquivo de configuração, mas não trocados com o sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="eba27-187">An array of [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances containing the key/value pairs that are stored in the configuration file but not exchanged with the guest operating system.</span></span> <span data-ttu-id="eba27-188">Isso permite que os aplicativos armazenem dados específicos da máquina virtual que não precisam ser visíveis para o sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="eba27-188">This allows applications to store virtual machine-specific data that does not need to be visible to the guest operating system.</span></span> <span data-ttu-id="eba27-189">Os itens são formatados da mesma forma que os itens na propriedade **HostExchangeItems** , exceto que a propriedade **Source** da instância **Msvm \_ KvpExchangeDataItem** é definida como 4.</span><span class="sxs-lookup"><span data-stu-id="eba27-189">The items are formatted the same as the items in the **HostExchangeItems** property except the **Source** property of the **Msvm\_KvpExchangeDataItem** instance is set to 4.</span></span> <span data-ttu-id="eba27-190">Cada arquivo de configuração é limitado a 128 pares chave/valor, em que cada campo de valor pode ter até 16 KB de tamanho e o campo de chave pode ter até 512 bytes.</span><span class="sxs-lookup"><span data-stu-id="eba27-190">Each configuration file is limited to 128 key/value pairs, where each value field is allowed to be up to 16 KB in size and the key field is allowed to be up to 512 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="eba27-191">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="eba27-191">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-192">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eba27-192">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="eba27-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eba27-194">Expõe uma atribuição específica para o host ou recursos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="eba27-194">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="eba27-195">Essa propriedade é herdada de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e sempre é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="eba27-195">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="eba27-196">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="eba27-196">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-197">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eba27-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eba27-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eba27-199">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="eba27-199">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="eba27-200">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="eba27-200">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="eba27-201">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="eba27-201">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="eba27-202">**Limite**</span><span class="sxs-lookup"><span data-stu-id="eba27-202">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-203">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eba27-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eba27-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eba27-205">O limite superior ou a quantidade máxima de recursos que serão concedidos para essa alocação.</span><span class="sxs-lookup"><span data-stu-id="eba27-205">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="eba27-206">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="eba27-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="eba27-207">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="eba27-207">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-208">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eba27-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eba27-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eba27-210">Especifica como esse recurso é mapeado para recursos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="eba27-210">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="eba27-211">Essa propriedade é herdada de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e sempre é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="eba27-211">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="eba27-212">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="eba27-212">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-213">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eba27-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eba27-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eba27-215">Uma cadeia de caracteres que descreve o tipo de recurso quando um valor bem definido não está disponível e **ResourceType** tem o valor 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="eba27-215">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="eba27-216">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="eba27-216">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="eba27-217">**Pai**</span><span class="sxs-lookup"><span data-stu-id="eba27-217">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-218">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eba27-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eba27-219">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eba27-220">O pai do recurso.</span><span class="sxs-lookup"><span data-stu-id="eba27-220">The parent of the resource.</span></span> <span data-ttu-id="eba27-221">Essa propriedade é herdada de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) e sempre é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="eba27-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="eba27-222">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="eba27-222">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-223">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eba27-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eba27-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eba27-225">A ID do pool de recursos do qual o recurso está alocado.</span><span class="sxs-lookup"><span data-stu-id="eba27-225">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="eba27-226">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="eba27-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="eba27-227">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="eba27-227">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-228">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eba27-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eba27-229">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eba27-230">A quantidade de recursos com garantia disponível para essa alocação.</span><span class="sxs-lookup"><span data-stu-id="eba27-230">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="eba27-231">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="eba27-231">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="eba27-232">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="eba27-232">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-233">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eba27-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eba27-234">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eba27-235">Uma cadeia de caracteres que descreve um subtipo específico de implementação para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="eba27-235">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="eba27-236">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="eba27-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="eba27-237">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="eba27-237">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-238">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eba27-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eba27-239">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eba27-240">O tipo de recurso que essa configuração de alocação representa.</span><span class="sxs-lookup"><span data-stu-id="eba27-240">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="eba27-241">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="eba27-241">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="eba27-242">Valor</span><span class="sxs-lookup"><span data-stu-id="eba27-242">Value</span></span>                                                                        | <span data-ttu-id="eba27-243">Significado</span><span class="sxs-lookup"><span data-stu-id="eba27-243">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="eba27-244"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="eba27-244"><dt>1</dt></span></span> </dl> | <span data-ttu-id="eba27-245">Outro</span><span class="sxs-lookup"><span data-stu-id="eba27-245">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="eba27-246">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="eba27-246">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-247">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eba27-247">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eba27-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eba27-249">A quantidade de recursos apresentados ao consumidor.</span><span class="sxs-lookup"><span data-stu-id="eba27-249">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="eba27-250">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="eba27-250">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="eba27-251">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="eba27-251">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-252">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eba27-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eba27-253">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eba27-254">Especifica a unidade de medida para essa alocação de recursos.</span><span class="sxs-lookup"><span data-stu-id="eba27-254">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="eba27-255">O valor dessa propriedade deve ser um valor válido do qualificador de unidades programáticas, conforme definido no anexo C. 1 de DSP0004 V 2.5 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="eba27-255">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="eba27-256">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="eba27-256">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="eba27-257">**Weight**</span><span class="sxs-lookup"><span data-stu-id="eba27-257">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eba27-258">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eba27-258">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eba27-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eba27-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eba27-260">Uma prioridade relativa para essa alocação em relação a outras alocações do mesmo pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="eba27-260">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="eba27-261">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="eba27-261">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eba27-262">Comentários</span><span class="sxs-lookup"><span data-stu-id="eba27-262">Remarks</span></span>

<span data-ttu-id="eba27-263">O acesso à classe **Msvm \_ KvpExchangeComponentSettingData** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="eba27-263">Access to the **Msvm\_KvpExchangeComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="eba27-264">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="eba27-264">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="eba27-265">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eba27-265">Requirements</span></span>



| <span data-ttu-id="eba27-266">Requisito</span><span class="sxs-lookup"><span data-stu-id="eba27-266">Requirement</span></span> | <span data-ttu-id="eba27-267">Valor</span><span class="sxs-lookup"><span data-stu-id="eba27-267">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eba27-268">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eba27-268">Minimum supported client</span></span><br/> | <span data-ttu-id="eba27-269">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="eba27-269">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="eba27-270">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eba27-270">Minimum supported server</span></span><br/> | <span data-ttu-id="eba27-271">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="eba27-271">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eba27-272">Namespace</span><span class="sxs-lookup"><span data-stu-id="eba27-272">Namespace</span></span><br/>                | <span data-ttu-id="eba27-273">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="eba27-273">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="eba27-274">MOF</span><span class="sxs-lookup"><span data-stu-id="eba27-274">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eba27-275"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eba27-275"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eba27-276">DLL</span><span class="sxs-lookup"><span data-stu-id="eba27-276">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eba27-277"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eba27-277"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="eba27-278">Confira também</span><span class="sxs-lookup"><span data-stu-id="eba27-278">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eba27-279">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="eba27-279">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="eba27-280">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="eba27-280">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

