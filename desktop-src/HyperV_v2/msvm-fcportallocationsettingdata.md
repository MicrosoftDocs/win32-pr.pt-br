---
description: Representa o estado configurado de uma porta de Fibre Channel sintética ou uma porta de comutador Fibre Channel.
ms.assetid: 680badc4-8dba-47e8-859a-0ed472a15eda
title: Classe Msvm_FcPortAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcPortAllocationSettingData
- Msvm_FcPortAllocationSettingData.InstanceID
- Msvm_FcPortAllocationSettingData.Caption
- Msvm_FcPortAllocationSettingData.Description
- Msvm_FcPortAllocationSettingData.ElementName
- Msvm_FcPortAllocationSettingData.ResourceType
- Msvm_FcPortAllocationSettingData.OtherResourceType
- Msvm_FcPortAllocationSettingData.ResourceSubType
- Msvm_FcPortAllocationSettingData.PoolID
- Msvm_FcPortAllocationSettingData.ConsumerVisibility
- Msvm_FcPortAllocationSettingData.HostResource
- Msvm_FcPortAllocationSettingData.AllocationUnits
- Msvm_FcPortAllocationSettingData.VirtualQuantity
- Msvm_FcPortAllocationSettingData.Reservation
- Msvm_FcPortAllocationSettingData.Limit
- Msvm_FcPortAllocationSettingData.Weight
- Msvm_FcPortAllocationSettingData.AutomaticAllocation
- Msvm_FcPortAllocationSettingData.AutomaticDeallocation
- Msvm_FcPortAllocationSettingData.Parent
- Msvm_FcPortAllocationSettingData.Connection
- Msvm_FcPortAllocationSettingData.Address
- Msvm_FcPortAllocationSettingData.MappingBehavior
- Msvm_FcPortAllocationSettingData.AddressOnParent
- Msvm_FcPortAllocationSettingData.VirtualQuantityUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 824f7077eeb3cb9e00ce8733cb5d2f57761716e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768752"
---
# <a name="msvm_fcportallocationsettingdata-class"></a><span data-ttu-id="426c9-103">\_Classe Msvm FcPortAllocationSettingData</span><span class="sxs-lookup"><span data-stu-id="426c9-103">Msvm\_FcPortAllocationSettingData class</span></span>

<span data-ttu-id="426c9-104">Representa o estado configurado de uma porta de Fibre Channel sintética ou uma porta de comutador Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="426c9-104">Represents the configured state of a synthetic Fibre Channel port or a Fibre Channel switch port.</span></span>

<span data-ttu-id="426c9-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="426c9-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="426c9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="426c9-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcPortAllocationSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Fibre Channel VDev Default Settings";
  string  Description = "The default settings for the virtual Fibre Channel connection pool.";
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
};
```

## <a name="members"></a><span data-ttu-id="426c9-107">Membros</span><span class="sxs-lookup"><span data-stu-id="426c9-107">Members</span></span>

<span data-ttu-id="426c9-108">A classe **Msvm \_ FcPortAllocationSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="426c9-108">The **Msvm\_FcPortAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="426c9-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="426c9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="426c9-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="426c9-110">Properties</span></span>

<span data-ttu-id="426c9-111">A classe **Msvm \_ FcPortAllocationSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="426c9-111">The **Msvm\_FcPortAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="426c9-112">**Endereço**</span><span class="sxs-lookup"><span data-stu-id="426c9-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426c9-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="426c9-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="426c9-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="426c9-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="426c9-115">O endereço do recurso.</span><span class="sxs-lookup"><span data-stu-id="426c9-115">The address of the resource.</span></span> <span data-ttu-id="426c9-116">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="426c9-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="426c9-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="426c9-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426c9-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="426c9-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="426c9-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="426c9-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="426c9-120">Descreve o endereço deste recurso no contexto do pai.</span><span class="sxs-lookup"><span data-stu-id="426c9-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="426c9-121">As propriedades **pai** e **AddressOnParent** são usadas para descrever a relação do controlador, bem como a ordem dos dispositivos em um controlador.</span><span class="sxs-lookup"><span data-stu-id="426c9-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="426c9-122">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="426c9-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="426c9-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="426c9-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426c9-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="426c9-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="426c9-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="426c9-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="426c9-126">As unidades de alocação usadas pelas propriedades **Reservation** e **Limit** .</span><span class="sxs-lookup"><span data-stu-id="426c9-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="426c9-127">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="426c9-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="426c9-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="426c9-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426c9-129">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="426c9-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="426c9-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="426c9-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="426c9-131">Indica se o recurso será alocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="426c9-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="426c9-132">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="426c9-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="426c9-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="426c9-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426c9-134">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="426c9-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="426c9-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="426c9-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="426c9-136">Indica se o recurso será desalocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="426c9-136">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="426c9-137">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="426c9-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="426c9-138">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="426c9-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426c9-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="426c9-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="426c9-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="426c9-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="426c9-141">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="426c9-141">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="426c9-142">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="426c9-142">A short description of the object.</span></span> <span data-ttu-id="426c9-143">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="426c9-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="426c9-144">**Conexão**</span><span class="sxs-lookup"><span data-stu-id="426c9-144">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426c9-145">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="426c9-145">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="426c9-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="426c9-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="426c9-147">O dispositivo ao qual esse recurso está conectado.</span><span class="sxs-lookup"><span data-stu-id="426c9-147">The device to which this resource is connected.</span></span> <span data-ttu-id="426c9-148">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="426c9-148">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="426c9-149">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="426c9-149">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426c9-150">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="426c9-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="426c9-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="426c9-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="426c9-152">A visibilidade do consumidor para o recurso alocado.</span><span class="sxs-lookup"><span data-stu-id="426c9-152">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="426c9-153">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="426c9-153">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="426c9-154">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="426c9-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426c9-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="426c9-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="426c9-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="426c9-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="426c9-157">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="426c9-157">A description of the object.</span></span> <span data-ttu-id="426c9-158">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="426c9-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="426c9-159">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="426c9-159">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426c9-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="426c9-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="426c9-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="426c9-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="426c9-162">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="426c9-162">A display name for the object.</span></span> <span data-ttu-id="426c9-163">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="426c9-163">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="426c9-164">A alteração dessa propriedade irá alterar o nome do elemento do derivado do dispositivo lógico associado.</span><span class="sxs-lookup"><span data-stu-id="426c9-164">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="426c9-165">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="426c9-165">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="426c9-166">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="426c9-166">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426c9-167">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="426c9-167">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="426c9-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="426c9-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="426c9-169">Somente um recurso de host pode ser atribuído a cada dispositivo na máquina virtual, de modo que somente o primeiro elemento dessa matriz pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="426c9-169">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="426c9-170">Para dispositivos que dão suporte a esse recurso, defina o primeiro elemento da matriz **HostResource** para conter uma referência ao recurso de host subjacente a ser atribuído.</span><span class="sxs-lookup"><span data-stu-id="426c9-170">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="426c9-171">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="426c9-171">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="426c9-172">Esta é uma propriedade somente leitura, mas se a propriedade **ResourceType** for 22 (disco) e a propriedade **ResourceSubType** for "unidade de disco físico da Microsoft", ela poderá ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="426c9-172">This is a read-only property, but if the **ResourceType** property is 22 (Disk) and the **ResourceSubType** property is "Microsoft Physical Disk Drive", then it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="426c9-173">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="426c9-173">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426c9-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="426c9-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="426c9-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="426c9-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="426c9-176">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="426c9-176">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="426c9-177">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="426c9-177">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="426c9-178">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="426c9-178">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="426c9-179">**Limite**</span><span class="sxs-lookup"><span data-stu-id="426c9-179">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426c9-180">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="426c9-180">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="426c9-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="426c9-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="426c9-182">A quantidade máxima de recursos que serão concedidos para essa alocação.</span><span class="sxs-lookup"><span data-stu-id="426c9-182">The maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="426c9-183">A unidade de medida para essa propriedade é especificada pela propriedade **VirtualQuantityUnits** .</span><span class="sxs-lookup"><span data-stu-id="426c9-183">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="426c9-184">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="426c9-184">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="426c9-185">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="426c9-185">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426c9-186">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="426c9-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="426c9-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="426c9-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="426c9-188">Especifica como esse recurso é mapeado para recursos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="426c9-188">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="426c9-189">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="426c9-189">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="426c9-190">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="426c9-190">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426c9-191">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="426c9-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="426c9-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="426c9-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="426c9-193">Uma cadeia de caracteres que descreve o tipo de recurso quando um valor bem definido não está disponível e [**ResourceType**](msvm-processorsettingdata.md) tem o valor 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="426c9-193">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="426c9-194">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="426c9-194">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="426c9-195">**Pai**</span><span class="sxs-lookup"><span data-stu-id="426c9-195">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426c9-196">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="426c9-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="426c9-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="426c9-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="426c9-198">O pai do recurso.</span><span class="sxs-lookup"><span data-stu-id="426c9-198">The parent of the resource.</span></span> <span data-ttu-id="426c9-199">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="426c9-199">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="426c9-200">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="426c9-200">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426c9-201">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="426c9-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="426c9-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="426c9-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="426c9-203">O identificador do pool de recursos do qual esse recurso foi alocado.</span><span class="sxs-lookup"><span data-stu-id="426c9-203">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="426c9-204">Para instâncias associadas a uma máquina virtual, serão "Microsoft:*GUID* \\ *específico de dispositivo-dados*".</span><span class="sxs-lookup"><span data-stu-id="426c9-204">For instances associated with a virtual machine, this will be "Microsoft:*GUID*\\*device-specific data*".</span></span> <span data-ttu-id="426c9-205">Para instâncias que definem configurações potenciais para uma máquina virtual, será "Microsoft: tipo de \\ *GUID* de definição \\ ", em que o *tipo* pode ser um "máximo", "mínimo", "padrão" ou "incremento".</span><span class="sxs-lookup"><span data-stu-id="426c9-205">For instances that define potential settings for a virtual machine, this will be "Microsoft:Definition\\*GUID*\\*Type*", where *Type* can be one of "Maximum", "Minimum", "Default", or "Increment".</span></span> <span data-ttu-id="426c9-206">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="426c9-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="426c9-207">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="426c9-207">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426c9-208">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="426c9-208">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="426c9-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="426c9-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="426c9-210">A quantidade de recursos com garantia disponível para essa alocação.</span><span class="sxs-lookup"><span data-stu-id="426c9-210">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="426c9-211">A unidade de medida para essa propriedade é especificada pela propriedade **VirtualQuantityUnits** .</span><span class="sxs-lookup"><span data-stu-id="426c9-211">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="426c9-212">É garantido que esses recursos estejam disponíveis para consumo pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="426c9-212">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="426c9-213">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="426c9-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="426c9-214">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="426c9-214">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426c9-215">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="426c9-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="426c9-216">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="426c9-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="426c9-217">Uma cadeia de caracteres que descreve um subtipo específico de implementação para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="426c9-217">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="426c9-218">Por exemplo, isso pode ser usado para distinguir modelos diferentes do mesmo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="426c9-218">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="426c9-219">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="426c9-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="426c9-220">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="426c9-220">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426c9-221">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="426c9-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="426c9-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="426c9-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="426c9-223">O tipo de recurso que essa configuração de alocação representa.</span><span class="sxs-lookup"><span data-stu-id="426c9-223">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="426c9-224">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="426c9-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="426c9-225"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="426c9-225"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-226"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Sistema de computador** (2)</span><span class="sxs-lookup"><span data-stu-id="426c9-226"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-227"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processador** (3)</span><span class="sxs-lookup"><span data-stu-id="426c9-227"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-228"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memória** (4)</span><span class="sxs-lookup"><span data-stu-id="426c9-228"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-229"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controlador IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="426c9-229"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-230"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI paralelo** (6)</span><span class="sxs-lookup"><span data-stu-id="426c9-230"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-231"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="426c9-231"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-232"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="426c9-232"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-233"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="426c9-233"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-234"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Adaptador Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="426c9-234"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-235"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Outro adaptador de rede** (11)</span><span class="sxs-lookup"><span data-stu-id="426c9-235"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-236"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Slot de e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="426c9-236"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-237"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo de e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="426c9-237"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-238"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Unidade de disquete** (14)</span><span class="sxs-lookup"><span data-stu-id="426c9-238"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-239"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unidade de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="426c9-239"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-240"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unidade de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="426c9-240"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-241"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Porta serial** (17)</span><span class="sxs-lookup"><span data-stu-id="426c9-241"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (17)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-242"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Porta paralela** (18)</span><span class="sxs-lookup"><span data-stu-id="426c9-242"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (18)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-243"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controlador USB** (19)</span><span class="sxs-lookup"><span data-stu-id="426c9-243"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (19)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-244"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controlador de gráficos** (20)</span><span class="sxs-lookup"><span data-stu-id="426c9-244"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (20)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-245"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extensão de armazenamento** (21)</span><span class="sxs-lookup"><span data-stu-id="426c9-245"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (21)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-246"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disco** (22)</span><span class="sxs-lookup"><span data-stu-id="426c9-246"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disk** (22)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-247"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Fita** (23)</span><span class="sxs-lookup"><span data-stu-id="426c9-247"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Tape** (23)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-248"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Outro dispositivo de armazenamento** (24)</span><span class="sxs-lookup"><span data-stu-id="426c9-248"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (24)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-249"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Controlador FireWire** (25)</span><span class="sxs-lookup"><span data-stu-id="426c9-249"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-250"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unidade particionável** (26)</span><span class="sxs-lookup"><span data-stu-id="426c9-250"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-251"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unidade particionável de base** (27)</span><span class="sxs-lookup"><span data-stu-id="426c9-251"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-252"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Fonte de energia** (28)</span><span class="sxs-lookup"><span data-stu-id="426c9-252"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-253"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Dispositivo de resfriamento** (29)</span><span class="sxs-lookup"><span data-stu-id="426c9-253"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-254"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (30 32767)</span><span class="sxs-lookup"><span data-stu-id="426c9-254"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="426c9-255"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="426c9-255"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="426c9-256">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="426c9-256">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426c9-257">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="426c9-257">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="426c9-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="426c9-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="426c9-259">Especifica a quantidade de recursos apresentados ao consumidor.</span><span class="sxs-lookup"><span data-stu-id="426c9-259">Specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="426c9-260">A unidade de medida para essa propriedade é especificada pela propriedade **VirtualQuantityUnits** .</span><span class="sxs-lookup"><span data-stu-id="426c9-260">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="426c9-261">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="426c9-261">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="426c9-262">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="426c9-262">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426c9-263">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="426c9-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="426c9-264">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="426c9-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="426c9-265">Especifica a unidade de medida para essa alocação de recursos.</span><span class="sxs-lookup"><span data-stu-id="426c9-265">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="426c9-266">O valor dessa propriedade deve ser um valor válido do qualificador de unidades programáticas, conforme definido no anexo C. 1 de DSP0004 V 2.5 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="426c9-266">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="426c9-267">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="426c9-267">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="426c9-268">**Weight**</span><span class="sxs-lookup"><span data-stu-id="426c9-268">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426c9-269">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="426c9-269">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="426c9-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="426c9-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="426c9-271">Um inteiro que define o peso relativo para cada processador de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="426c9-271">An integer that defines the relative weight for each virtual machine processor.</span></span> <span data-ttu-id="426c9-272">Depois que todas as reservas forem atendidas, a capacidade física restante do processador da plataforma de hospedagem será alocada às máquinas virtuais com base em seus pesos relativos.</span><span class="sxs-lookup"><span data-stu-id="426c9-272">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="426c9-273">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="426c9-273">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="426c9-274">Intervalo: 0 1000</span><span class="sxs-lookup"><span data-stu-id="426c9-274">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="426c9-275">Requisitos</span><span class="sxs-lookup"><span data-stu-id="426c9-275">Requirements</span></span>



| <span data-ttu-id="426c9-276">Requisito</span><span class="sxs-lookup"><span data-stu-id="426c9-276">Requirement</span></span> | <span data-ttu-id="426c9-277">Valor</span><span class="sxs-lookup"><span data-stu-id="426c9-277">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="426c9-278">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="426c9-278">Minimum supported client</span></span><br/> | <span data-ttu-id="426c9-279">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="426c9-279">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="426c9-280">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="426c9-280">Minimum supported server</span></span><br/> | <span data-ttu-id="426c9-281">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="426c9-281">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="426c9-282">Namespace</span><span class="sxs-lookup"><span data-stu-id="426c9-282">Namespace</span></span><br/>                | <span data-ttu-id="426c9-283">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="426c9-283">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="426c9-284">MOF</span><span class="sxs-lookup"><span data-stu-id="426c9-284">MOF</span></span><br/>                      | <dl> <span data-ttu-id="426c9-285"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="426c9-285"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="426c9-286">DLL</span><span class="sxs-lookup"><span data-stu-id="426c9-286">DLL</span></span><br/>                      | <dl> <span data-ttu-id="426c9-287"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="426c9-287"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

