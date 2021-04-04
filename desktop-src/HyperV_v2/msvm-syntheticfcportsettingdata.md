---
description: Representa o estado configurado de uma porta de Fibre Channel sintética.
ms.assetid: 5d47dd80-de34-4ae4-a300-c16da1cd4974
title: Classe Msvm_SyntheticFcPortSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticFcPortSettingData
- Msvm_SyntheticFcPortSettingData.InstanceID
- Msvm_SyntheticFcPortSettingData.Caption
- Msvm_SyntheticFcPortSettingData.Description
- Msvm_SyntheticFcPortSettingData.ElementName
- Msvm_SyntheticFcPortSettingData.ResourceType
- Msvm_SyntheticFcPortSettingData.OtherResourceType
- Msvm_SyntheticFcPortSettingData.ResourceSubType
- Msvm_SyntheticFcPortSettingData.PoolID
- Msvm_SyntheticFcPortSettingData.ConsumerVisibility
- Msvm_SyntheticFcPortSettingData.HostResource
- Msvm_SyntheticFcPortSettingData.AllocationUnits
- Msvm_SyntheticFcPortSettingData.VirtualQuantity
- Msvm_SyntheticFcPortSettingData.Reservation
- Msvm_SyntheticFcPortSettingData.Limit
- Msvm_SyntheticFcPortSettingData.Weight
- Msvm_SyntheticFcPortSettingData.AutomaticAllocation
- Msvm_SyntheticFcPortSettingData.AutomaticDeallocation
- Msvm_SyntheticFcPortSettingData.Parent
- Msvm_SyntheticFcPortSettingData.Connection
- Msvm_SyntheticFcPortSettingData.Address
- Msvm_SyntheticFcPortSettingData.MappingBehavior
- Msvm_SyntheticFcPortSettingData.AddressOnParent
- Msvm_SyntheticFcPortSettingData.VirtualQuantityUnits
- Msvm_SyntheticFcPortSettingData.VirtualPortWWPN
- Msvm_SyntheticFcPortSettingData.VirtualPortWWNN
- Msvm_SyntheticFcPortSettingData.SecondaryWWPN
- Msvm_SyntheticFcPortSettingData.SecondaryWWNN
- Msvm_SyntheticFcPortSettingData.VirtualSystemIdentifiers
- Msvm_SyntheticFcPortSettingData.ChapEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bdd0342f5429f5314f5c744a3a760101dbaa043b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646824"
---
# <a name="msvm_syntheticfcportsettingdata-class"></a><span data-ttu-id="5d178-103">\_Classe Msvm SyntheticFcPortSettingData</span><span class="sxs-lookup"><span data-stu-id="5d178-103">Msvm\_SyntheticFcPortSettingData class</span></span>

<span data-ttu-id="5d178-104">Representa o estado configurado de uma porta de Fibre Channel sintética.</span><span class="sxs-lookup"><span data-stu-id="5d178-104">Represents the configured state of a synthetic Fibre Channel port.</span></span>

<span data-ttu-id="5d178-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5d178-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d178-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d178-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticFcPortSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Fibre Channel Port Default Settings";
  string  Description = "Describes the default settings for the virtual Fibre Channel port resources.";
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
  string  VirtualPortWWPN;
  string  VirtualPortWWNN;
  string  SecondaryWWPN;
  string  SecondaryWWNN;
  string  VirtualSystemIdentifiers[];
  boolean ChapEnabled;
};
```

## <a name="members"></a><span data-ttu-id="5d178-107">Membros</span><span class="sxs-lookup"><span data-stu-id="5d178-107">Members</span></span>

<span data-ttu-id="5d178-108">A classe **Msvm \_ SyntheticFcPortSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5d178-108">The **Msvm\_SyntheticFcPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="5d178-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5d178-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5d178-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5d178-110">Properties</span></span>

<span data-ttu-id="5d178-111">A classe **Msvm \_ SyntheticFcPortSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5d178-111">The **Msvm\_SyntheticFcPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5d178-112">**Endereço**</span><span class="sxs-lookup"><span data-stu-id="5d178-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d178-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-115">O endereço do recurso.</span><span class="sxs-lookup"><span data-stu-id="5d178-115">The address of the resource.</span></span> <span data-ttu-id="5d178-116">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5d178-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5d178-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="5d178-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d178-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-120">Descreve o endereço deste recurso no contexto do pai.</span><span class="sxs-lookup"><span data-stu-id="5d178-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="5d178-121">As propriedades **pai** e **AddressOnParent** são usadas para descrever a relação do controlador, bem como a ordem dos dispositivos em um controlador.</span><span class="sxs-lookup"><span data-stu-id="5d178-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="5d178-122">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5d178-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5d178-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="5d178-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d178-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-126">A unidade de alocação usada pelas propriedades **Reservation** e **Limit** .</span><span class="sxs-lookup"><span data-stu-id="5d178-126">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="5d178-127">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5d178-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5d178-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="5d178-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-129">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5d178-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-131">Indica se o recurso será alocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="5d178-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="5d178-132">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5d178-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5d178-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="5d178-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-134">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5d178-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-136">Indica se o recurso será desalocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="5d178-136">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="5d178-137">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5d178-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5d178-138">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="5d178-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d178-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d178-141">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="5d178-141">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="5d178-142">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d178-142">A short description of the object.</span></span> <span data-ttu-id="5d178-143">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5d178-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5d178-144">**ChapEnabled**</span><span class="sxs-lookup"><span data-stu-id="5d178-144">**ChapEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-145">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5d178-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-147">Indica que essa porta foi configurada com um segredo compartilhado usando DH-CHAP, que permite que o Fibre Channel Fabric autentique que essa máquina virtual pode usar legitimamente os WWNs (World Wide Names) atribuídos a essa porta.</span><span class="sxs-lookup"><span data-stu-id="5d178-147">Indicates that this port has been configured with a shared secret using DH-CHAP, which allows the Fibre Channel fabric to authenticate that this virtual machine can legitimately use the world wide names that are assigned to this port.</span></span>

</dd> <dt>

<span data-ttu-id="5d178-148">**Conexão**</span><span class="sxs-lookup"><span data-stu-id="5d178-148">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-149">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d178-149">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5d178-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-151">O dispositivo ao qual esse recurso está conectado.</span><span class="sxs-lookup"><span data-stu-id="5d178-151">The device to which this resource is connected.</span></span> <span data-ttu-id="5d178-152">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5d178-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5d178-153">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="5d178-153">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-154">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5d178-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-156">A visibilidade do consumidor para o recurso alocado.</span><span class="sxs-lookup"><span data-stu-id="5d178-156">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="5d178-157">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5d178-157">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5d178-158">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5d178-158">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d178-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-161">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="5d178-161">A description of the object.</span></span> <span data-ttu-id="5d178-162">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5d178-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5d178-163">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5d178-163">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d178-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-166">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="5d178-166">A display name for the object.</span></span> <span data-ttu-id="5d178-167">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5d178-167">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="5d178-168">A alteração dessa propriedade irá alterar o nome do elemento do derivado do dispositivo lógico associado.</span><span class="sxs-lookup"><span data-stu-id="5d178-168">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="5d178-169">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="5d178-169">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="5d178-170">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="5d178-170">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-171">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d178-171">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5d178-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-173">Somente um recurso de host pode ser atribuído a cada dispositivo na máquina virtual, de modo que somente o primeiro elemento dessa matriz pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="5d178-173">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="5d178-174">Para dispositivos que dão suporte a esse recurso, defina o primeiro elemento da matriz **HostResource** para conter uma referência ao recurso de host subjacente a ser atribuído.</span><span class="sxs-lookup"><span data-stu-id="5d178-174">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="5d178-175">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5d178-175">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5d178-176">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5d178-176">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d178-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d178-179">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="5d178-179">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5d178-180">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="5d178-180">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5d178-181">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5d178-181">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5d178-182">**Limite**</span><span class="sxs-lookup"><span data-stu-id="5d178-182">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-183">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5d178-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-185">A quantidade máxima de recursos de host correspondentes que podem ser consumidos pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5d178-185">The maximum amount of corresponding host resources that can be consumed by the virtual machine.</span></span> <span data-ttu-id="5d178-186">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5d178-186">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5d178-187">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="5d178-187">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-188">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5d178-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-190">Especifica como esse recurso é mapeado para recursos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="5d178-190">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="5d178-191">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5d178-191">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5d178-192">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="5d178-192">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-193">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d178-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-195">Uma cadeia de caracteres que descreve o tipo de recurso quando um valor bem definido não está disponível e [**ResourceType**](msvm-processorsettingdata.md) tem o valor 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="5d178-195">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="5d178-196">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="5d178-196">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5d178-197">**Pai**</span><span class="sxs-lookup"><span data-stu-id="5d178-197">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-198">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d178-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-200">O pai do recurso.</span><span class="sxs-lookup"><span data-stu-id="5d178-200">The parent of the resource.</span></span> <span data-ttu-id="5d178-201">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5d178-201">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5d178-202">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="5d178-202">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-203">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d178-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-205">O identificador do pool de recursos do qual esse recurso foi alocado.</span><span class="sxs-lookup"><span data-stu-id="5d178-205">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="5d178-206">Para instâncias associadas a uma máquina virtual, serão "Microsoft:*GUID* \\ *específico de dispositivo-dados*".</span><span class="sxs-lookup"><span data-stu-id="5d178-206">For instances associated with a virtual machine, this will be "Microsoft:*GUID*\\*device-specific data*".</span></span> <span data-ttu-id="5d178-207">Para instâncias que definem configurações potenciais para uma máquina virtual, será "Microsoft: tipo de \\ *GUID* de definição \\ ", em que o *tipo* pode ser um "máximo", "mínimo", "padrão" ou "incremento".</span><span class="sxs-lookup"><span data-stu-id="5d178-207">For instances that define potential settings for a virtual machine, this will be "Microsoft:Definition\\*GUID*\\*Type*", where *Type* can be one of "Maximum", "Minimum", "Default", or "Increment".</span></span> <span data-ttu-id="5d178-208">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5d178-208">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5d178-209">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="5d178-209">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-210">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5d178-210">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-212">A quantidade de recursos que são reservados para uso pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5d178-212">The amount of resources that are reserved for use by the virtual machine.</span></span> <span data-ttu-id="5d178-213">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="5d178-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5d178-214">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="5d178-214">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-215">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d178-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-216">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-217">Uma cadeia de caracteres que descreve um subtipo específico de implementação para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="5d178-217">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="5d178-218">Por exemplo, isso pode ser usado para distinguir modelos diferentes do mesmo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="5d178-218">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="5d178-219">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5d178-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5d178-220">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="5d178-220">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-221">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5d178-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-223">O tipo de recurso que essa configuração de alocação representa.</span><span class="sxs-lookup"><span data-stu-id="5d178-223">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="5d178-224">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5d178-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="5d178-225">Valor</span><span class="sxs-lookup"><span data-stu-id="5d178-225">Value</span></span>                                                                                                                                                                                          | <span data-ttu-id="5d178-226">Significado</span><span class="sxs-lookup"><span data-stu-id="5d178-226">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="FC_HBA"></span><span id="fc_hba"></span><dl> <span data-ttu-id="5d178-227"><dt>**FC HBA**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="5d178-227"><dt>**FC HBA**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="5d178-228">Fibre Channel</span><span class="sxs-lookup"><span data-stu-id="5d178-228">Fibre Channel</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5d178-229">**SecondaryWWNN**</span><span class="sxs-lookup"><span data-stu-id="5d178-229">**SecondaryWWNN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-230">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d178-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-232">Indica o WWN (World Wide Name) de nó da porta do HBA virtual a ser usado durante a migração dinâmica da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5d178-232">Indicates the world wide node name of the virtual HBA port to be used during live migration of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="5d178-233">**SecondaryWWPN**</span><span class="sxs-lookup"><span data-stu-id="5d178-233">**SecondaryWWPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-234">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d178-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-235">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-236">Indica o WWN (World Wide Name) da porta do HBA virtual a ser usada durante a migração dinâmica da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5d178-236">Indicates the world wide port name of the virtual HBA port to be used during live migration of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="5d178-237">**VirtualPortWWNN**</span><span class="sxs-lookup"><span data-stu-id="5d178-237">**VirtualPortWWNN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-238">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d178-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-239">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-240">Indica o WWN (World Wide Name) de nó da porta do HBA virtual.</span><span class="sxs-lookup"><span data-stu-id="5d178-240">Indicates the world wide node name of the virtual HBA port.</span></span>

</dd> <dt>

<span data-ttu-id="5d178-241">**VirtualPortWWPN**</span><span class="sxs-lookup"><span data-stu-id="5d178-241">**VirtualPortWWPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-242">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d178-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-243">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-244">Indica o WWN (World Wide Name) da porta do HBA virtual.</span><span class="sxs-lookup"><span data-stu-id="5d178-244">Indicates the world wide port name of the virtual HBA port.</span></span>

</dd> <dt>

<span data-ttu-id="5d178-245">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="5d178-245">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-246">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5d178-246">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-247">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-248">Especifica a quantidade de recursos apresentados ao consumidor.</span><span class="sxs-lookup"><span data-stu-id="5d178-248">Specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="5d178-249">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5d178-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5d178-250">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="5d178-250">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-251">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d178-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-253">Especifica a unidade de medida para a propriedade **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="5d178-253">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="5d178-254">O valor dessa propriedade deve ser um valor válido do qualificador de unidades programáticas, conforme definido no anexo C. 1 de DSP0004 V 2.5 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="5d178-254">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="5d178-255">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5d178-255">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5d178-256">**VirtualSystemIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="5d178-256">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-257">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d178-257">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5d178-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d178-259">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="5d178-259">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="5d178-260">Uma matriz de cadeia de caracteres de identificadores deste recurso apresentada ao sistema operacional da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5d178-260">A string array of identifiers of this resource presented to the virtual machine's operating system.</span></span> <span data-ttu-id="5d178-261">Os índices e valores por índice são definidos por recurso (ou seja, para cada valor de **ResourceType** enumerado).</span><span class="sxs-lookup"><span data-stu-id="5d178-261">The indexes and values per index are defined on a per resource basis (that is, for each enumerated **ResourceType** value).</span></span> <span data-ttu-id="5d178-262">Esta propriedade não é usada</span><span class="sxs-lookup"><span data-stu-id="5d178-262">This property is not used</span></span>

</dd> <dt>

<span data-ttu-id="5d178-263">**Weight**</span><span class="sxs-lookup"><span data-stu-id="5d178-263">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d178-264">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5d178-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5d178-265">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d178-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d178-266">Um inteiro que define o peso relativo para cada processador de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5d178-266">An integer that defines the relative weight for each virtual machine processor.</span></span> <span data-ttu-id="5d178-267">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="5d178-267">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5d178-268">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d178-268">Requirements</span></span>



| <span data-ttu-id="5d178-269">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d178-269">Requirement</span></span> | <span data-ttu-id="5d178-270">Valor</span><span class="sxs-lookup"><span data-stu-id="5d178-270">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d178-271">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d178-271">Minimum supported client</span></span><br/> | <span data-ttu-id="5d178-272">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5d178-272">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5d178-273">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d178-273">Minimum supported server</span></span><br/> | <span data-ttu-id="5d178-274">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5d178-274">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5d178-275">Namespace</span><span class="sxs-lookup"><span data-stu-id="5d178-275">Namespace</span></span><br/>                | <span data-ttu-id="5d178-276">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="5d178-276">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5d178-277">MOF</span><span class="sxs-lookup"><span data-stu-id="5d178-277">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d178-278"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d178-278"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d178-279">DLL</span><span class="sxs-lookup"><span data-stu-id="5d178-279">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d178-280"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5d178-280"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

